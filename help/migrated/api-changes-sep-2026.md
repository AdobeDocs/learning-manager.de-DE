---
description: Öffentliche API-Endpunkte für Teilnehmer zum Auflisten, Abrufen, Registrieren und Löschen von personalisierten Lernpfaden in Adobe Learning Manager und API-Endpunkten zum Überprüfen, ob ein oder mehrere Lernobjekte einem bestimmten Teilnehmer direkt über einen Katalog, der ihm zugewiesen wurde, zugänglich sind.
jcr-language: en_us
title: API-Änderungen im September 2026
source-git-commit: 328d899c05384ff522f7f6413d2a451139f066ee
workflow-type: tm+mt
source-wordcount: '1374'
ht-degree: 3%
---

# API-Änderungen in der Version September 2026 von Adobe Learning Manager

## API zum Überprüfen des Katalogzugriffs für Lernobjekte

Bestimmen Sie, ob der aktuelle Teilnehmer direkten Katalogzugriff auf ein oder mehrere Lernobjekte hat, unabhängig davon, ob der Teilnehmer diesen Inhalt über einen Lernpfad oder eine Zertifizierung erreicht hat.

### Zweck der API

Wenn ein Teilnehmer einen Lernpfad oder eine Zertifizierung öffnet, kann er die einzelnen darin enthaltenen Kurse durchsuchen, auch wenn ihm ein bestimmter Kurs nicht direkt über einen Katalog zugewiesen wurde. Dies unterstützt die Suche nach Inhalten: können Teilnehmer den Inhalt eines Lernpfads untersuchen, bevor sie entscheiden, ob sie ihn weiterverfolgen möchten.

Wenn Sie einen Kurs auf diese Weise anzeigen können, sollte dies jedoch nicht automatisch bedeuten, dass sich der Teilnehmer dafür registrieren kann. Die Registrierung sollte davon abhängen, ob der Teilnehmer direkten Katalogzugriff auf diesen bestimmten Kurs hat, nicht nur den indirekten Zugriff über einen enthaltenden Lernpfad.

Mit dieser API können Sie für einen bestimmten Teilnehmer überprüfen, ob auf ein oder mehrere Lernobjekte direkt über einen Katalog zugegriffen werden kann, der ihm zugewiesen wurde. Verwenden Sie das Ergebnis, um die Benutzeroberfläche für die Registrierung zu steuern, z. B. wenn die Option &quot;Registrieren&quot; nur angezeigt wird, wenn der direkte Katalogzugriff bestätigt wurde, während die Kursseite selbst in beiden Fällen sichtbar bleibt.

### Endpunkt

`GET /primeapi/v2/learningObjects/isMemberOfVisibleCatalogs`

| Eigenschaft | Wert |
|---|---|
| **Umfang** | Lesezugriff für Teilnehmer |
| **Antwortformat** | application/vnd.api+json |

### Abfrageparameter

| Parameter | Erforderlich | Typ | Beschreibung |
|---|---|---|---|
| IDs | Ja | Zeichenfolge oder Array | Mindestens eine zu überprüfende Lernobjekt-ID. Akzeptiert eine einzelne ID oder eine durch Kommas getrennte Liste. Maximal 10 IDs pro Anforderung. |

### Beispielanforderung

```
GET /primeapi/v2/learningObjects/isMemberOfVisibleCatalogs?ids=course%3A2400159%2Ccourse%3A2400160%2Ccourse%3A2400161%2Ccourse%3A2400162
Accept: application/vnd.api+json
Authorization: oauth <access-token>
```

>[!NOTE]
>
>Lernobjekt-IDs müssen URL-codiert sein. Der Doppelpunkt in einer ID wie course:2400159 ist als %3A und das Komma zwischen mehreren IDs als %2C codiert.

### Beispielantwort - 200 OK

```json
{
  "course:2400162": false,
  "course:2400161": false,
  "course:2400160": true,
  "course:2400159": true
}
```

| Wert | Bedeutung |
|---|---|
| korrekt | Der aufrufende Teilnehmer hat direkten Katalogzugriff auf dieses Lernobjekt. |
| falsch | Das Lernobjekt steht dem anrufenden Teilnehmer nicht direkt über einen Katalog zur Verfügung. Der Teilnehmer kann es weiterhin anzeigen, wenn es über einen Lernpfad oder eine Zertifizierung erreichbar ist, auf die er Zugriff hat. |

### Antwortcodes

| Status | Bedeutung |
|---|---|
| 200 | Die Anforderung war erfolgreich. Die Antwort enthält ein Ergebnis für jede angeforderte ID. |
| 400 | Ein allgemeiner Fehler bei einer ungültigen Anforderung. Beispielsweise wurden mehr als 10 IDs angegeben, oder eine ID war fehlerhaft. |
| 401 | Der Anforderung fehlen gültige Teilnehmeranmeldeinformationen oder der Zugriff wurde aufgrund ungültiger Anmeldedaten verweigert. |

### Beispielfehlerantwort

```json
{
  "status": "BAD_REQUEST",
  "title": "Bad request. Check url, params and headers",
  "source": {
    "info": "Either LO id is blank or not as per public api specification"
  }
}
```

### Diese API in Ihrer Integration verwenden

Ein häufiger Anwendungsfall ist eine Kursseite, die ein Teilnehmer erreicht, indem er von einem Lernpfad aus navigiert. Sie möchten, dass die Kursseite selbst für die Erkennung zugänglich bleibt, während die Aktion **Registrieren** nur angezeigt wird, wenn der Teilnehmer direkten Katalogzugriff auf diesen Kurs hat.

1. Wenn die Kursseite geladen wird, rufen Sie diesen Endpunkt mit der Lernobjekt-ID des Kurses auf.
2. Wenn die Antwort für diese ID &quot;true&quot; zurückgibt, zeigen Sie die Option **Registrieren** an.
3. Wenn die Antwort &quot;false&quot; zurückgibt, halten Sie die Kursseite sichtbar, den Titel, die Beschreibung und die Kursdetails, aber blenden Sie die Option **Registrieren** aus.

## Job-API für Administratorprüfprotokollbericht {#apiaudittrailreport}

### Zweck der API

Der Administrator Audit Trail-Bericht listet die Konfigurationsänderungen auf, die an einer
Adobe Learning Manager-Konto bearbeiten. Beispielsweise Änderungen an &quot;Grundlagen&quot;, &quot;Integrationen&quot; oder
Erweiterte Kontoeinstellungen für einen bestimmten Datumsbereich. Zum Generieren des Prüfprotokollberichts müssen Konfigurationsänderungsdatensätze für den angeforderten Datumsbereich und die Einstellungstypen abgefragt und aggregiert werden. Je nach Größe des Bereichs und der Menge der Änderungen kann dies die Zeitlimits einer synchronen HTTP-Anforderung überschreiten, wodurch Client- oder Gateway-Timeouts riskiert werden.

Um dies zu vermeiden, wird der Bericht asynchron über die generische Job-API generiert:

1. **Auftrag erstellen.** Der Administrator sendet eine Anforderung, in der er den Berichtstyp, den Datumsbereich und die Einstellungstypen angibt. Die API gibt sofort eine Job-ID zurück, ohne auf die Kompilierung des Berichts zu warten.

2. **Auftrag abfragen.** Der Administrator ruft den Job regelmäßig anhand seiner ID ab, um seinen Status zu überprüfen. Wenn der Auftrag abgeschlossen ist, enthält die Antwort das Ergebnis oder einen Verweis darauf.

### Basis-URL und Konventionen

| Element | Wert |
|---|---|
| Basispfad | `/primeapi/v2` |
| Inhaltstyp | `application/vnd.api+json;charset=UTF-8` (JSON:API) |
| Authentifizierung | OAuth-Bearer-Token, auf einen Kontoadministrator beschränkt |
| Kontokontext | `x-acap-account`-Kopfzeile, die das Konto des anrufenden Administrators identifiziert |
| Abfrage | Es wird kein festes Intervall erzwungen. den Endpunkt &quot;Auftragsstatus abrufen&quot; abfragen, bis `status` nicht mehr `QUEUED` oder `IN_PROGRESS` ist |

### IDs

Der bei der Erstellung eines Auftrags zurückgegebene Auftrag &quot;`id`&quot; ist eine undurchsichtige Zeichenfolge (z. B.
`4593`). Immer genau den `id`-Wert zurückgeben, den Sie vom Erstellungsvorgang erhalten haben
Antwort beim Abfragen des Status. Sie niemals konstruieren oder analysieren.

### Authentifizierungsbereiche

Für jeden Endpunkt ist ein OAuth-Token mit dem folgenden Gültigkeitsbereich erforderlich. Das
Der aufrufende Benutzer muss über die Kontoadministratorrolle verfügen:

- `admin:write` Berichtsauftrag erstellen (`ROLE_ADMIN` erforderlich)
- `admin:read` hat den Status und das Ergebnis eines Auftrags gelesen (`ROLE_ADMIN` erforderlich).

Anforderungen eines Anrufers, der nicht `ROLE_ADMIN` für das Konto besitzt, sind
zurückgewiesen; Siehe [Fehlerbehandlung](/help/migrated/api-changes-sep-2026.md#error-handling)

### Endpunkte

#### Auftrag für einen Audit-Protokoll-Bericht erstellen

`POST /primeapi/v2/jobs`

Erstellt einen asynchronen Auftrag, der einen Bericht zum Konfigurationsänderungs-Audit-Protokoll generiert.
für den angegebenen Datumsbereich und die Einstellungstypen. Die Antwort wird sofort zurückgegeben
mit einer Auftragsressource im Status &quot;`QUEUED`&quot;; der Bericht selbst wird in der
Hintergrund.

Umfang: `admin:write`

| Parameter | In | Erforderlich | Beschreibung |
|---|---|---|---|
| `jobType` | body | Ja | Für diesen Bericht muss `generateConfigChangeAuditReport` sein. |
| `payload.fromDate` | body | Ja | Start des Berichtsfensters, ISO-8601 mit Offset, z. B. `2026-09-15T00:00:00.000+05:30` |
| `payload.toDate` | body | Ja | Ende des Berichtsfensters, ISO-8601 mit Offset, z. B. `2026-09-23T23:59:59.000+05:30` |
| `payload.settingTypes` | body | Ja | Array aus einer oder mehreren Einstellungskategorien, die einbezogen werden sollen; Die unterstützten Werte sind `Basics`, `Integrations` und `Advanced`. |

Beispielanforderungstext

```json
{
  "data": {
    "type": "job",
    "attributes": {
      "jobType": "generateConfigChangeAuditReport",
      "payload": {
        "fromDate": "2026-09-15T00:00:00.000+05:30",
        "toDate": "2026-09-23T23:59:59.000+05:30",
        "settingTypes": ["Basics", "Integrations", "Advanced"]
      }
    }
  }
}
```

Antwort: `202 Created` Der Antworttext ist die Auftragsressource in seinem ursprünglichen
Status &quot;`QUEUED`&quot;.

```json
{
  "data": {
    "id": "4593",
    "type": "job",
    "attributes": {
      "jobType": "generateConfigChangeAuditReport",
      "status": "QUEUED",
      "dateCreated": "2026-09-23T18:12:04.000+05:30"
    }
  }
}
```

>[!NOTE]
>
>Ein `fromDate`/`toDate`-Fenster, das sich über einen sehr großen Datumsbereich erstreckt, oder das
>alle Einstellungstypen für ein Konto mit einem langen Änderungsverlauf anfordert, kann
>die Verarbeitung dauert länger. Umfrage zum Endpunkt &quot;Status abrufen&quot; statt zum
>vorausgesetzt, der Bericht ist nach einer festen Verzögerung fertig.

#### Abrufen des Status eines Prüfprotokollberichtsauftrags

`GET /primeapi/v2/jobs/{id}`

Gibt den aktuellen Status eines zuvor erstellten Auftrags zurück. Solange der Auftrag
wird noch ausgeführt, `attributes.status` ist `QUEUED` oder `IN_PROGRESS` und
`attributes.result` ist nicht vorhanden. Sobald der Auftrag abgeschlossen ist, wird `attributes.status`
entweder `COMPLETED` mit dem Berichtsspeicherort in `attributes.result` oder
`FAILED`, mit Fehlerdetails in `attributes.error`.

Umfang: `admin:read`

| Parameter | In | Erforderlich | Beschreibung |
|---|---|---|---|
| `id` | Pfad | Ja | Auftrags-ID, die beim Erstellen des Auftrags zurückgegeben wurde |

Beispielantwort, während der Auftrag noch ausgeführt wird

```json
{
  "data": {
    "id": "4593",
    "type": "job",
    "attributes": {
      "jobType": "generateConfigChangeAuditReport",
      "status": "IN_PROGRESS",
      "dateCreated": "2026-09-23T18:12:04.000+05:30"
    }
  }
}
```

Beispielantwort nach Abschluss des Auftrags

```json
{
  "data": {
    "id": "4593",
    "type": "job",
    "attributes": {
      "jobType": "generateConfigChangeAuditReport",
      "status": "COMPLETED",
      "dateCreated": "2026-09-23T18:12:04.000+05:30",
      "dateCompleted": "2026-09-23T18:12:41.000+05:30",
      "result": {
        "downloadUrl": "https://learningmanager.adobe.com/primeapi/v2/jobs/4593/download",
        "expiresAt": "2026-09-24T18:12:41.000+05:30"
      }
    }
  }
}
```

### Ressourcenschema

#### Auftragsattribute

| Feld | Typ | Beschreibung |
|---|---|---|
| `id` | Zeichenfolge | Undurchsichtige Job-ID |
| `jobType` | Zeichenfolge | `generateConfigChangeAuditReport` für diesen Bericht |
| `status` | Zeichenfolge | `QUEUED`, `IN_PROGRESS`, `COMPLETED` oder `FAILED` |
| `dateCreated` | Zeichenfolge (ISO-8601) | Zeitpunkt der Auftragserstellung |
| `dateCompleted` | Zeichenfolge (ISO-8601) | Wenn der Auftrag beendet wurde; vorhanden, wenn `status` `COMPLETED` oder `FAILED` ist |
| `payload` | Einspruch | Die Anforderungsparameter, mit denen der Auftrag erstellt wurde (eingebettet - siehe unten) |
| `result` | Einspruch | Wo kann der fertige Bericht heruntergeladen werden? Nur vorhanden, wenn `status` `COMPLETED` ist (eingebettet - siehe unten) |
| `error` | Einspruch | Fehlerdetails; Nur vorhanden, wenn `status` `FAILED` ist |

#### Nutzlast (eingebettet in die Erstellungsanforderung)

| Feld | Beschreibung |
|---|---|
| `fromDate` | Beginn des Berichtsfensters |
| `toDate` | Ende des Berichtsfensters |
| `settingTypes` | Im Bericht enthaltene Kategorien festlegen: `Basics`, `Integrations`, `Advanced` |

#### Ergebnis (eingebettet in einen abgeschlossenen Auftrag)

| Feld | Beschreibung |
|---|---|
| `downloadUrl` | Signierte URL, von der der generierte Bericht heruntergeladen werden kann |
| `expiresAt` | Wenn `downloadUrl` nicht mehr gültig ist; eine neue Statusprüfung anfordern, um nach diesem Zeitpunkt einen neuen Link zu erhalten |

### Fehlerbehandlung {#audit-trail-report-error-handling}

Für diese Endpunkte gelten die folgenden Codes:

| HTTP-Status | Fehlercode | Wenn es auftritt |
|---|---|---|
| 400 | `BAD_REQUEST` | `toDate` ist älter als `fromDate`, `settingTypes` ist leer oder enthält einen nicht unterstützten Wert, oder ein Datum ist ungültig ISO-8601 - nur Endpunkt erstellen |
| 401 | `UNAUTHORIZED_ACCESS` | Das Token fehlt, ist ungültig oder abgelaufen |
| 403 | `FORBIDDEN` | Der Aufrufer enthält `ROLE_ADMIN` nicht im Konto. |
| 400 | `OBJECT_DOESNT_EXIST` | Per ID abrufen: job nicht vorhanden oder die ID ist fehlerhaft - beide Fälle werden in derselben Antwort zusammengeführt |

Beispielfehlerantwort

```json
{
  "status": "BAD_REQUEST",
  "title": "Bad request. Check url, params and headers",
  "source": {
    "info": "toDate must be on or after fromDate"
  }
}
```

### Diese API in Ihrer Integration verwenden

Ein typischer Anwendungsfall ist eine Administratoraktion zum Herunterladen des Audit-Protokolls im Dialogfeld &quot;
Kontoeinstellungen angezeigt.

1. Wenn der Administrator einen Datumsbereich und einen oder mehrere Einstellungstypen auswählt und
bestätigt, rufen Sie den Endpunkt create-job mit diesen Werten auf.
2. Speichern Sie den zurückgegebenen Auftrag &quot;`id`&quot;, und rufen Sie den Endpunkt &quot;Auftragsstatus abrufen&quot; auf einer
ein angemessenes Intervall (beispielsweise alle paar Sekunden).
3. Während `status` `QUEUED` oder `IN_PROGRESS` ist, zeigen Sie weiterhin einen Fortschrittsstatus an
in der Benutzeroberfläche.
4. Wenn `status` zu `COMPLETED` wird, verwenden Sie `result.downloadUrl`, um die
Der Administrator lädt den Bericht herunter, bevor `expiresAt` erfolgreich ist.
5. Wenn `status` zu `FAILED` wird, übergeben Sie `error` an den Administrator und lassen Sie ihn
erneut versuchen.

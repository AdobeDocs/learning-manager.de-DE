---
description: API-Änderungen in ALM
jcr-language: en_us
title: API-Änderungen in der Version August 2026 von Adobe Learning Manager
source-git-commit: 857c94b5e9a7460d63a6dacc0beeddd41f362bf9
workflow-type: tm+mt
source-wordcount: '3354'
ht-degree: 3%

---


# API-Änderungen in der Version August 2026 von Adobe Learning Manager

## Admin-API für Benutzergruppen in Adobe Learning Manager

In dieser Version werden drei neue öffentliche API-Endpunkte mit Administratorbereich für die programmgesteuerte Verwaltung benutzerdefinierter Benutzergruppen hinzugefügt. Sie können benutzerdefinierte Benutzergruppen ohne die Admin-App erstellen, umbenennen und löschen. So können Sie die Gruppenverwaltung als Teil Ihrer Identitäts- oder Bereitstellungsarbeitsabläufe automatisieren.

Diese Endpunkte funktionieren nur mit benutzerdefinierten Benutzergruppen. Systemverwaltete Gruppen wie die Gruppe Alle Benutzer und automatisch generierte Benutzergruppen verfügen über den Schreibschutz: true in der API-Antwort und kann nicht über diese Endpunkte geändert oder gelöscht werden.

Anforderungen für die API-Authentifizierung finden Sie unter [Adobe Learning Manager API-Authentifizierung](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual#authentication-using-oauth-20).

### API-Endpunkte für Benutzergruppen

Für alle drei Endpunkte ist ein Administratorzugriffstoken mit Schreibberechtigungen (ROLE_ADMIN) erforderlich.

| **Methode** | **Pfad** | **Vorgang** | **Erfolgscode** |
|---|---|---|---|
| POST | /primeapi/v2/userGroups | Erstellen einer benutzerdefinierten Benutzergruppe | 201 Erstellt |
| PUT | /primeapi/v2/userGroups/{id} | Aktualisieren des Namens oder der Beschreibung einer Gruppe | 200 OK |
| DELETE | /primeapi/v2/userGroups/{id} | Löschen einer benutzerdefinierten Benutzergruppe | 204 Kein Inhalt |

## **Häufige Anforderungsheader**

Für alle drei Endpunkte sind die folgenden Kopfzeilen erforderlich.

```
Authorization: Bearer \<access-token\>
X-acap-user: \<user-id\>
X-acap-account: \<account-id\>
X-acap-caller-role: ROLE_ADMIN
Content-Type: application/vnd.api+json
Accept: application/vnd.api+json
```

### **Benutzergruppe erstellen**

```
POST /primeapi/v2/userGroups
```

Erstellt eine neue benutzerdefinierte Benutzergruppe mit einer anfänglichen Liste von Mitgliedern. Die Gruppe steht sofort für die Verwendung in der Admin-App zur Verfügung.

#### **Anforderungstext**

```
{
  "name": "Marketing Team",
  "description": "Custom user group for marketing onboarding",
  "data": [
    { "type": "user", "id": "11282373" },
    { "type": "user", "id": "11282374" }
  ]
}
```

#### **Anforderungsparameter**

| **Parameter** | **Erforderlich** | **Typ** | **Beschreibung** |
|---------------|--------------|----------|-------------------------------------------------------------------------------------|
| name | Ja | Zeichenfolge | Anzeigename der Gruppe. Darf nicht leer oder nur Leerraum sein. |
| Beschreibung | Nein | Zeichenfolge | Optionale Beschreibung des Zwecks der Gruppe. |
| data | Ja | Feld | Ursprüngliche Mitgliederliste. Mindestens 1 Element, maximal 100 Elemente. |
| data[].type | Ja | Zeichenfolge | Muss &quot;Benutzer&quot; sein. Andere Ressourcentypen werden nicht akzeptiert. |
| data[].id | Ja | Zeichenfolge | Zeichenfolge für numerische Benutzer-ID. Der Benutzer muss dem Konto angehören und den Status AKTIV aufweisen. |

> **Hinweis:** Das Datenarray wird nur bei der Erstellung verwendet, um die erste Elementliste festzulegen. Um Mitglieder nach der Erstellung hinzuzufügen oder zu entfernen, verwenden Sie die vorhandenen Endpunkte der Benutzergruppenmitgliedschaft.

#### **Antwort 201 erstellt**

```
{
  "links": {
    "self": "https://<host>/primeapi/v2/userGroups"
  },
  "data": {
    "id": "2769204",
    "type": "userGroup",
    "attributes": {
      "dateCreated": "2026-06-04T14:19:53.000Z",
      "description": "Custom user group for marketing onboarding",
      "name": "Marketing Team",
      "readOnly": false,
      "userCount": 2
    }
  }
}
```

#### **POST der Validierungsregeln**

| **#** | **Validierung** | **Fehlercode** | **Trigger** |
|-------|-------------------------------------------------------|----------------------------------------------------------|------------------------------------------------|
| 1 | Name vorhanden und nicht leer | USERGROUP_CREATE_NAME_REQUIRED | Name weggelassen oder nur Leerraum |
| 2 | Daten enthalten mindestens 1 Benutzer | USERGROUP_CREATE_USERS_REQUIRED | Daten fehlen oder leeres Array |
| 3 | enthält mindestens 100 Benutzer. | USERGROUP_USERS_MAX_LIMIT_EXCEEDED | Mehr als 100 Einträge in Daten[] |
| 4 | Alle Benutzer-IDs sind numerische Zeichenfolgen. | INVALID_USER_IDS | Nicht-numerische Zeichenfolge in [] gefunden.id |
| 5 | Alle Benutzer sind im Konto vorhanden und haben den Status AKTIV . | INVALID_USER_IDS / USERGROUP_CREATE_USERS_NOT_IN_ACCOUNT | Benutzer nicht gefunden oder nicht aktiv |
| 6 | Konto hat das Limit für benutzerdefinierte Gruppen nicht erreicht | 400 | Grenzwert auf Kontoebene für benutzerdefinierte Gruppen überschritten |

### **Benutzergruppe aktualisieren**

```
PUT /primeapi/v2/userGroups/{id}
```

Aktualisiert den Namen und/oder die Beschreibung einer vorhandenen benutzerdefinierten Benutzergruppe. Dieser Endpunkt kann keine Gruppenmitglieder hinzufügen oder entfernen.

Beide Felder können weggelassen werden. Wenn ein Feld weggelassen wird, bleibt sein aktueller Wert unverändert. Durch Übergeben des NULL-Werts für die Beschreibung wird dieser gelöscht. Das Übergeben einer leeren Zeichenfolge für den Namen wird abgelehnt.

#### **Anforderungstext**

```json
{
  "name": "Updated Group Name",
  "description": "Updated description text"
}
```

#### **Anforderungsparameter**

| **Parameter** | **Erforderlich** | **Typ** | **Beschreibung** |
|---------------|--------------|----------|---------------------------------------------------------------------------|
| name | Ja | Zeichenfolge | Neuer Anzeigename. Darf nicht leer sein, falls angegeben. Lassen Sie es unverändert. |
| Beschreibung | Nein | Zeichenfolge | Neue Beschreibung. Übergeben Sie null zum Löschen. Lassen Sie es unverändert. |

#### **Antwort 200 OK**

```
{
  "data": {
    "type": "userGroup",
    "id": "2767870",
    "attributes": {
      "name": "Updated Group Name",
      "description": "Updated description text",
      "readOnly": false,
      "state": "Active",
      "userCount": 3
    }
  }
}
```

#### **Validierungsregeln PUT**

| **#** | **Validierung** | **Fehlercode** | **Trigger** |
|-------|-------------------------------------|----------------------------------------|----------------------------------------------------------|
| 1 | Daten sind NULL oder nicht vorhanden. | USERGROUP_UPDATE_USERS_NOT_ALLOWED | Der Aufrufer hat Daten übergeben, die nicht NULL sind, um eine Änderung der Mitgliedschaft zu versuchen. |
| 2 | Name, sofern angegeben, ist nicht leer | USERGROUP_UPDATE_NAME_BLANK | Name, der als Zeichenfolge gesendet wird, der nur Leerräume enthält |
| 3 | Gruppe ist in diesem Konto vorhanden | INVALID_USER_GROUP_ID | Unbekannter {id}-Pfadparameter |
| 4 | Gruppe wurde noch nicht gelöscht | DELETED_USERGROUP | Gruppe wurde zuvor gelöscht |
| 5 | Group readOnly ist false. | READ_ONLY_USERGROUP | Vom System verwaltete Gruppe |
| 6 | Gruppe ist ein benutzerdefinierter Typ (kein System) | USERGROUP_UPDATE_OPERATION_NOT_ALLOWED | Systeminterner Gruppentyp |

### **Benutzergruppe löschen**

```
DELETE /primeapi/v2/userGroups/{id}
```

Markiert die angegebene benutzerdefinierte Benutzergruppe als gelöscht. Der Gruppendatensatz wird nicht endgültig entfernt . Sein Status ist auf GELÖSCHT festgelegt, was ihn in der Admin-App nicht sichtbar und für die Verwendung in neuen Konfigurationen nicht berechtigt macht. Die Gruppen-ID kann nicht wiederverwendet werden.

#### **Anforderungsbeispiel**

```
DELETE /primeapi/v2/userGroups/2767870
Authorization: Bearer <access-token>
X-acap-user: <user-id>
X-acap-account: <account-id>
X-acap-caller-role: ROLE_ADMIN
```

#### **Antwort 204 Kein Inhalt**

Der Antworttext ist leer.

> **Hinweis:** DELETE ist nicht imposant. Wenn Sie eine zweite DELETE-Anforderung an dieselbe Gruppen-ID senden, wird der Fehler 400 mit dem Code DELETED_USERGROUP zurückgegeben, nicht 204. Behandeln Sie eine 400 DELETED_USERGROUP-Antwort als Bestätigung, dass die Gruppe bereits gelöscht wurde. Das Massenlöschen wird nicht unterstützt. jede Gruppe erfordert eine separate DELETE-Anforderung.

#### **DELETE für Validierungsregeln**

| **#** | **Validierung** | **Fehlercode** | **Trigger** |
|-------|-------------------------------------|----------------------------------------|---------------------------------------------------|
| 1 | Gruppe ist in diesem Konto vorhanden | INVALID_USER_GROUP_ID | Unbekannter {id}-Pfadparameter |
| 2 | Gruppe wurde noch nicht gelöscht | DELETED_USERGROUP | Wiederholen Sie das DELETE für eine Gruppe, die bereits den Status GELÖSCHT aufweist. |
| 3 | Group readOnly ist false. | READ_ONLY_USERGROUP | Vom System verwaltete Gruppe |
| 4 | Gruppe ist ein benutzerdefinierter Typ (kein System) | USERGROUP_UPDATE_OPERATION_NOT_ALLOWED | Systeminterner Gruppentyp |

## Externe Lern-API in Adobe Learning Manager

In dieser Version werden fünf neue API-Endpunkte für Teilnehmer für die Funktion &quot;Externes Lernen&quot; hinzugefügt. Mit diesen Endpunkten können Teilnehmer externe Lernübermittlungen programmgesteuert erstellen, abrufen und aktualisieren, z. B. über eine mobile App, ein integriertes HR-System oder ein benutzerdefiniertes Lernportal.

Der externe Lern-Workflow über die API spiegelt den Workflow in der Teilnehmer-App wider: Wenn ein Teilnehmer Schulungsdetails und ein optionales Nachweisdokument einreicht, erhält sein direkter Manager eine Benachrichtigung, um die Einreichung zu überprüfen, und bei Genehmigung wird der Datensatz im Transkript des Teilnehmers angezeigt.

Alle fünf Endpunkte sind teilnehmerspezifisch. Ein Teilnehmer kann nur auf seine eigenen Einreichungen zugreifen - die API gibt einen Fehler zurück, wenn ein Teilnehmer versucht, auf die Daten eines anderen Teilnehmers zuzugreifen.

Anforderungen für die API-Authentifizierung finden Sie unter [Adobe Learning Manager API-Authentifizierung](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual#authentication-using-oauth-20).

### Externe Lern-API-Endpunkte

Alle Endpunkte erfordern ein Teilnehmerzugriffstoken (ROLE_LEARNER).

| **Methode** | **Pfad** | **Vorgang** | **Erfolgscode** |
|------------|---------------------------------------|----------------------------------|------------------|
| GET | /primeapi/v2/externalLearningSettings | Kontoformularkonfiguration abrufen | 200 OK |
| GET | /primeapi/v2/externalLearnings | Liste der Einreichungen des Anrufers | 200 OK |
| GET | /primeapi/v2/externalLearnings/{id} | Einzelne Einreichung abrufen | 200 OK |
| POST | /primeapi/v2/externalLearnings | Neue Einreichung erstellen | 201 Erstellt |
| PUT | /primeapi/v2/externalLearnings/{id} | Ausstehende Einreichung aktualisieren | 200 OK |

### Häufige Anforderungsheader

```
Authorization: Bearer <access-token>
X-acap-user: <user-id>
X-acap-account: <account-id>
X-acap-caller-role: ROLE_LEARNER
Accept: application/vnd.api+json
Content-Type: application/vnd.api+json (POST and PUT only)
```

### Lebenszyklus des Übermittlungsstatus

| **Status** | **festgelegt von** | **Bedeutung** | **Kann der Teilnehmer ein Update durchführen?** |
|------------|------------------|-----------------------------------------|-----------------------------|
| AUSSTEHEND | System beim Erstellen | Warten auf Manager-Review | Ja - über PUT |
| GENEHMIGT | Manager | Akzeptiert; wird im Teilnehmertranskript angezeigt | Nein - PUT gibt 409 zurück |
| ABGELEHNT | Manager | Abgelehnt; Überprüfungskommentar angehängt | Nein - neue Einreichung erstellen |

APPROVED (Genehmigt) und REJECTED (Zurückgewiesen) sind Terminalstatus. Eine abgelehnte Einreichung kann nicht erneut geöffnet werden. der Teilnehmer muss eine neue Einreichung erstellen.

### Kontoformularkonfiguration abrufen

```
GET /primeapi/v2/externalLearningSettings
```

Gibt die Formularkonfiguration auf Kontoebene zurück. Rufen Sie diesen Endpunkt auf, bevor Sie ein Übermittlungsformular rendern. Die Antwort definiert, welche Felder angezeigt werden sollen, welche obligatorisch sind, ihre Datentypen und alle vom Administrator konfigurierten benutzerdefinierten Felder.

Überprüfen Sie das aktivierte Attribut der obersten Ebene, bevor Sie fortfahren. Wenn &quot;false&quot;, ist die Funktion &quot;Externes Lernen&quot; für dieses Konto nicht aktiv, und die Übermittlungsendpunkte geben Fehler zurück.

#### Antwort 200 OK

```
{
  "data": {
    "id": "8627",
    "type": "externalLearningSettings",
    "attributes": {
      "enabled": true,
      "updatedAt": "2026-06-05T06:51:20.000Z",
      "coreFields": [
        { "id": "title", "type": "TEXT", "mandatory": true, "editable": false, "order": 0 },
        { "id": "description_notes", "type": "TEXT", "mandatory": false, "editable": true, "order": 1 },
        { "id": "date", "type": "TIMESTAMP", "mandatory": false, "editable": true, "order": 2 },
        { "id": "score", "type": "NUMBER", "mandatory": true, "editable": true, "order": 3 },
        { "id": "duration", "type": "TEXT", "mandatory": false, "editable": true, "order": 4 },
        { "id": "attachments", "type": "FILE_UPLOAD", "mandatory": true, "editable": true, "order": 5 }
      ],
      "customFields": [
        {
          "id": "960369b2-...",
          "type": "NUMBER",
          "mandatory": true,
          "order": 0,
          "label": { "en_US": "Employee Code" }
        },
        {
          "id": "3c6cc6d9-...",
          "type": "DROPDOWN",
          "mandatory": true,
          "order": 1,
          "label": { "en_US": "Department" },
          "options": [
            { "option_id": "opt_1", "label": { "en_US": "IT" } },
            { "option_id": "opt_2", "label": { "en_US": "HR" } },
            { "option_id": "opt_3", "label": { "en_US": "FIN" } }
          ]
        }
      ]
    }
  }
}
```

#### Kernfeldreferenz

| **Feld-ID** | **Typ** | **Standard obligatorisch** | **Hinweise** |
|-------------------|-------------|-----------------------|----------------------------------------------------------------------------------------------------------|
| title | TEXT | Ja | Schulungsname. Immer präsent. Kann vom Administrator nicht deaktiviert werden. |
| description_notes | TEXT | Nein | Freitextbeschreibung oder Notizen. |
| Datum | ZEITSTEMPEL | Nein | Datumsbereich Wert-Form: { &quot;start_date&quot;: &quot;<ISO-Z>&quot;end_date&quot;: &quot;<ISO-Z>&quot; }. Beide Werte können NULL sein. |
| Ergebnis | ZAHL | Ja | Wert-Form: { &quot;erzielte_Punktzahl&quot;: <number>, &quot;max_score&quot;: <number> }. Beide Werte müssen numerisch sein. |
| Dauer | TEXT | Nein | Freiformzeichenfolge, zum Beispiel &quot;40 Stunden&quot;. |
| Zubehörteil | FILE_UPLOAD | Ja | Abschlussnachweis. **Nicht** in Feldern übergeben[] — verwenden Sie stattdessen das übergeordnete submitUrl-Attribut. |

Benutzerdefinierte Felder werden vom Administrator definiert und in customFields[] zurückgegeben. Ihre IDs, Typen, obligatorischen Markierungen, Beschriftungen und Dropdown-Optionen variieren je nach Kontokonfiguration.

### Einreichungen auflisten

```
GET /primeapi/v2/externalLearnings
```

Gibt eine paginierte Liste der eigenen Übertragungen des authentifizierten Teilnehmers zurück, sortiert nach modifiedAt absteigend (zuletzt geändert zuerst).

#### **Abfrageparameter**

| **Parameter** | **Standard** | **Maximal** | **Beschreibung** |
|---------------|-------------|-------------|-------------------------------------------------------------------------------------------------------|
| page[offset] | 0 | 5000 | Nullbasierter Datensatzoffset. |
| page[limit] | 10 | 100 | Datensätze pro Seite. Werte über 100 werden leise auf 100 geklemmt. |
| ls_qp_status | — | — | Nach Status filtern. Für alle Ergebnisse auslassen. Gültige Werte: &quot;AUSSTEHEND&quot;, &quot;GENEHMIGT&quot;, &quot;ABGELEHNT&quot; (Groß- und Kleinschreibung werden nicht berücksichtigt). |

#### **Antwort 200 OK**

```
{
  "links": {
    "next": "/primeapi/v2/externalLearnings?page[offset]=10&page[limit]=10"
  },
  "data": [
    { "id": "1001", "type": "externalLearning", "attributes": { "status": "PENDING", ... } },
    { "id": "1002", "type": "externalLearning", "attributes": { "status": "APPROVED", ... } }
  ]
}
```

### Einreichen abrufen

```
GET /primeapi/v2/externalLearnings/{id}
```

Gibt den vollständigen Datensatz für eine einzelne Übermittlung zurück, die dem authentifizierten Teilnehmer gehört.

#### **Antwort 200 OK

```
{
  "data": {
    "id": "1001",
    "type": "externalLearning",
    "attributes": {
      "submissionUrl": "https://<cdn-url>/cert.pdf",
      "title": "Java Fundamentals Certification",
      "status": "PENDING",
      "creationSource": "LEARNER",
      "createdAt": "2026-04-14T08:30:00.000Z",
      "modifiedAt": "2026-04-16T11:45:00.000Z",
      "fields": [ "...resolved against live settings..." ]
    },
    "relationships": {
      "reviewerUser": { "data": null }
    }
  }
}
```

### Einreichung erstellen

```
POST /primeapi/v2/externalLearnings
```

Erstellt eine neue externe Lernoberfläche im Status &quot;AUSSTEHEND&quot;. Alle in den Kontoeinstellungen definierten Pflichtfelder müssen einbezogen werden. Nach einer erfolgreichen POST erhält der Manager des Teilnehmers eine plattforminterne Benachrichtigung, um die Einreichung zu überprüfen.

### **Datei-Upload**

Das Feld &quot;Anlagen&quot; wird getrennt von den anderen Feldern behandelt. Fügen Sie es nicht in die Felder &quot;[]&quot; ein. Stattdessen:

&#x200B;1. Rufen Sie eine vorsignierte S3-Upload-URL vom ALM-Datei-Upload-Endpunkt ab.

&#x200B;2. Laden Sie die Datei auf diese URL hoch.

&#x200B;3. Übergeben Sie die resultierende URL als das übergeordnete submissionUrl-Attribut in Ihrer POST-Anforderung.

#### **Anforderungstext**

```
{
  "data": {
    "type": "externalLearning",
    "attributes": {
      "submissionUrl": "<pre-signed-upload-url>",
      "fields": [
        { "id": "title", "type": "TEXT", "value": "Java Fundamentals Certification" },
        { "id": "description_notes", "type": "TEXT", "value": "Completed via online course platform." },
        { "id": "date", "type": "TIMESTAMP", "value": { "start_date": "2026-05-01T00:00:00.000Z", "end_date": "2026-05-15T00:00:00.000Z" } },
        { "id": "score", "type": "NUMBER", "value": { "achieved_score": 88, "max_score": 100 } },
        { "id": "duration", "type": "TEXT", "value": "40 hours" },
        { "id": "960369b2-...", "type": "NUMBER", "value": "1225" },
        { "id": "3c6cc6d9-...", "type": "DROPDOWN", "value": "opt_3" }
      ]
    }
  }
}
```

#### Feldwert-Formen

| **Feldtyp** | **Wert-Shape** | **Beispiel** |
|----------------|---------------------------------------------------------|----------------------------------------------------------------|
| TEXT | Zeichenfolge | &quot;Java-Grundlagen&quot; |
| ZAHL | Objekt mit erreichter_Punktzahl und maximaler_Punktzahl | { &quot;erzielte_Punktzahl&quot;: 8, &quot;max_score&quot;: 100 } |
| ZEITSTEMPEL | Objekt mit start_date und end_date (ISO 8601 oder null) | { &quot;start_date&quot;: &quot;2026-05-01T00:00:00.000Z&quot;, &quot;end_date&quot;: null } |
| DROPDOWN | option_id Zeichenfolge aus Kontoeinstellungen | &quot;Option_3&quot; |
| FILE_UPLOAD | In den Feldern &quot;[]&quot; nicht zulässig — verwenden Sie &quot;submissionUrl&quot;. | — |

#### POST der Validierungsregeln

| **#** | **Validierung** | **Trigger** |
|-------|-----------------------------------------------------------------|----------------------------------------------------------|
| 1 | Externes Lernen ist für das Konto aktiviert | Feature-Flag deaktiviert |
| 2 | Alle Pflichtfelder sind in den Feldern &quot;[]&quot; vorhanden. | Obligatorisches Feld nicht angegeben |
| 3 | Jede Feld-ID, jeder Typ und jedes Wert-Shape entsprechen den Kontoeinstellungen. | Falscher Typ oder ungültiges Wertobjekt |
| 4 | Der Typ &quot;FILE_UPLOAD&quot; ist in den Feldern &quot;[]&quot; nicht vorhanden. | Anhang in Feldern [] anstelle von &quot;submissionUrl&quot; gesendet |
| 5 | submitUrl ist eine gültige vorsignierte S3-URL. | CDN-URLs und Nicht-S3-URLs, die bei der Erstellung abgelehnt wurden |
| 6 | submitUrl vorhanden, wenn attachments.mandatory auf true festgelegt ist | Anhänge sind erforderlich, aber &quot;submitUrl&quot; fehlt. |

### Einreichung aktualisieren

```
PUT /primeapi/v2/externalLearnings/{id}
```

Aktualisiert eine vorhandene ausstehende Übermittlung. Nur ausstehende Einreichungen können aktualisiert werden. Wenn Sie versuchen, eine APPROVED- oder REJECTED-Übermittlung PUT, wird der Fehler 409 zurückgegeben.

**Dieser Endpunkt verwendet die Semantik für die vollständige Ersetzung.** Geben Sie in jeder PUT-Anforderung das vollständige Feld &quot;[]&quot; an, nicht nur die Felder, die Sie ändern. Aus dem Array ausgelassene Felder werden gelöscht.

#### Felder, die der Teilnehmer aktualisieren kann

| **Feld/Attribut** | **Teilnehmer kann** aktualisieren | **Hinweise** |
|-----------------------|------------------------|----------------------------------------------------------------------------|
| Felder [] | Ja | Vollständige Ersetzung - alle Felder einschließen, nicht nur geänderte |
| submissionUrl | Ja | CDN-URLs werden unter PUT akzeptiert. Vorsignierte S3-URLs sind nur für die POST erforderlich. |
| reviewerUserId | Nein | Vom Manager festgelegte Aktion schreibgeschützt für Teilnehmer |
| reviewAt | Nein | Vom Manager festgelegte Aktion schreibgeschützt für Teilnehmer |
| reviewerComment | Nein | Vom Manager festgelegte Aktion schreibgeschützt für Teilnehmer |
| Status | Nein | Gesteuert durch Manager: AUSSTEHEND → GENEHMIGT ODER ABGELEHNT |
| creationSource | Nein | Always LEARNER für API-erstellte Übertragungen |
| createdAt | Nein | Zur Erstellungszeit festlegen unveränderlich |

#### Anforderungstext

```
{
  "data": {
    "type": "externalLearning",
    "attributes": {
      "submissionUrl": "<cdn-url>/cert-v2.pdf",
      "fields": [
        { "id": "title", "type": "TEXT", "value": "Java Fundamentals — Updated" },
        { "id": "description_notes", "type": "TEXT", "value": "Updated notes." },
        { "id": "date", "type": "TIMESTAMP", "value": { "start_date": null, "end_date": null } },
        { "id": "score", "type": "NUMBER", "value": { "achieved_score": 92, "max_score": 100 } },
        { "id": "duration", "type": "TEXT", "value": "42 hours" },
        { "id": "960369b2-...", "type": "NUMBER", "value": "1227" },
        { "id": "3c6cc6d9-...", "type": "DROPDOWN", "value": "opt_2" }
      ]
    }
  }
}
```

## API für die lernerrelevante Zertifizierungs-ID und die Stammzertifizierungs-ID in LT

Wenn eine wiederkehrende Zertifizierung verlängert wird, erstellt Adobe Learning Manager eine neue Version der Zertifizierung und registriert automatisch aktive Teilnehmer dafür. Wenn Ihre Integration Zertifizierungsdaten direkt abfragt, anstatt sich auf das Adobe Learning Manager-Lernerlebnis zu verlassen, können Sie mit dieser API jederzeit genau bestimmen, welche Version einer wiederkehrenden Zertifizierung für einen bestimmten Teilnehmer relevant ist.

### Zweck der API

Wiederkehrende Zertifizierungen generieren bei jeder Verlängerung eine neue Zertifizierungs-ID. Im nativen Adobe Learning Manager-Lernerlebnis wird nur die Version angezeigt, die für jeden Teilnehmer relevant ist. Ältere Versionen werden automatisch ausgeblendet, wenn ein Teilnehmer zu einer neueren Version wechselt.

Wenn Ihre Integration Zertifizierungsdaten unabhängig abruft, um z. B. Zertifizierungsinformationen in einem externen Portal anzuzeigen, wird diese Filterung möglicherweise nicht automatisch angewendet. Ohne diese Möglichkeit könnte ein Teilnehmer jede historische Version einer wiederkehrenden Zertifizierung sehen, einschließlich derjenigen, die für ihn nicht mehr relevant sind, ohne Angabe, auf welche er reagieren sollte.

Diese Lücke wurde mit dieser API geschlossen. Aufgrund der Stammzertifizierungs-ID gibt es die spezifische Zertifizierungsversion zurück, die für einen bestimmten Teilnehmer gilt, wobei dessen Registrierungsverlauf und etwaige Wiederholungen berücksichtigt werden.

### Wiederkehrende Zertifizierungen

Wenn eine Zertifizierung so konfiguriert ist, dass sie wiederholt wird, erstellt jede Verlängerung eine neue Zertifizierungsversion mit einer eigenen eindeutigen ID. Alle Versionen werden auf eine einzige **Stammzertifizierungs-ID zurückverfolgt,** auf die ID der ursprünglichen Zertifizierung, als diese erstmalig erstellt wurde.

Eine Zertifizierung, die jeden Monat wiederholt wird, kann beispielsweise zu einer Abfolge von Versionen im Zeitverlauf führen, bei denen jede neue Version automatisch generiert wird, wenn das Wiederholungsintervall erreicht wird. Teilnehmer, die aktiv registriert sind, wenn ein Wiederholungsfall auftritt, werden automatisch für die neue Version registriert.

Da jede Version eine eigene ID hat, hängt die relevante Version eines Teilnehmers von seiner individuellen Registrierungszeitleiste ab:

- Ein Teilnehmer, der sich vor einer Wiederholung registriert und seine Zertifizierung abgeschlossen hat, bevor die nächste Wiederholung stattgefunden hat, hat im Laufe der Zeit mehrere Versionen durchlaufen.

- Ein Teilnehmer, der sich teilweise über einen Wiederholungszyklus registriert, wird direkt bei der Version registriert, die zum Zeitpunkt der Registrierung aktuell ist.

### Ermitteln der entsprechenden Zertifizierungsversion

Verwenden Sie die API für die Zertifizierungsversion, um zu ermitteln, welche Version einer wiederkehrenden Zertifizierung für einen bestimmten Teilnehmer relevant ist.

Geben Sie die **Stammzertifizierungs-ID** als Eingabe an. Die API wertet den Registrierungsverlauf des Teilnehmers aus und gibt die entsprechende Version basierend auf den folgenden Regeln zurück:

| **Teilnehmerstatus** | **Von der API zurückgegebene Informationen** |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Der Teilnehmer ist noch nicht für die Zertifizierung registriert | Die neueste verfügbare Version der Zertifizierung |
| Teilnehmer ist derzeit registriert | Die spezifische Version, in der sich der Teilnehmer derzeit registriert, wobei alle Wiederholungen berücksichtigt werden, die seit der ursprünglichen Registrierung aufgetreten sind |

Dies bedeutet, dass zwei Teilnehmer, die gleichzeitig dieselbe Stammzertifizierungs-ID abfragen, je nach individuellem Registrierungsverlauf jedes Teilnehmers unterschiedliche Ergebnisse erhalten.

**Hinweis**: Während der Erstellung der neuen Version und der Migration von Registrierungen kann es während einer Wiederholung zu einem kurzen Fenster kommen, in dem die API möglicherweise die Version zurückgibt, die bald ersetzt wird, nicht die neu erstellte.

**Beispiel**

Nehmen wir an, es handelt sich um eine Zertifizierung, die monatlich wiederholt wird und bei der im Laufe der Zeit aufgrund aufeinander folgender Wiederholungen vier Versionen erstellt wurden:

- Ein Teilnehmer, der sich für die erste Version registriert hat und jede Wiederholung durchlaufen hat, wird an die Version zurückgegeben, in der er derzeit aktiv ist. Dies spiegelt seinen eigenen Abschluss- und Wiederholungsverlauf wider, nicht unbedingt die neueste Version, die vorhanden ist.

- Ein Teilnehmer, der sich noch nicht registriert hat, wird zur zuletzt erstellten Version zurückgeleitet, da dies die Version ist, der neue Registrierungen beitreten sollten.

Dadurch kann die Integration einen Teilnehmer immer zur für ihn relevanten Zertifizierungsversion leiten, anstatt jede ältere Version anzuzeigen oder zu erraten, welche zutreffend ist.

### API-Referenz

**Erhalten Sie die entsprechende Zertifizierung für eine Stammzertifizierung**

```
GET /primeapi/v2/learningObjects/{loId}/applicableCertification
```

Löst die Zertifizierungsversion auf, die für den aktuellen Teilnehmer gilt, wenn die ID einer Stammzertifizierung angegeben wird. Bei Teilnehmern, für die eine Registrierung vorliegt, wird hiermit die Version zurückgegeben, für die sie derzeit registriert sind. Für Teilnehmer, die nicht registriert sind, gibt dies die neueste aktive Version zurück.

| **Eigenschaft** | **Wert** |
|----------------------------------------------------------|--------------------------|
| **Umfang** | Lesezugriff für Teilnehmer |
| **Rate Limit (Standardanrufe von Teilnehmern)** | 70 Anfragen pro Minute |
| **Ratenbeschränkung (erhöhte oder API-Zugangsberechtigungen auf Administratorebene)** | 500 Anfragen pro Stunde |
| **Antwortformat** | application/vnd.api+json |

**Hinweis**: Diese API gibt Versionsinformationen für jeweils einen einzelnen Teilnehmer zurück. Es wird keine Liste aller Versionen einer Zertifizierung zurückgegeben.

**Pfadparameter**

| **Parameter** | **Erforderlich** | **Typ** | **Beschreibung** |
|---------------|--------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| loID | Ja | Zeichenfolge | Die ID des Lernobjekts, insbesondere die Stammzertifizierung, für die die entsprechende Version angefordert wird. Dies unterliegt den Standardzugriffsberechtigungen. |

**Abfrageparameter**

| **Parameter** | **Erforderlich** | **Typ** | **Beschreibung** |
|---------------|--------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mitrechnen | Nein | Zeichenfolge | Eine durch Kommas getrennte Liste verwandter Modelle, die in die Antwort neben der aufgelösten Zertifizierung aufgenommen werden sollen, z. B. Sub-LOs oder Registrierung. Verwendet dieselbe Include-Syntax wie andere Adobe Learning Manager-Lernobjektendpunkte. |

**Beispielanforderung**

```
GET /primeapi/v2/learningObjects/certification%3A167658/applicableCertification?include=subLOs
Accept: application/vnd.api+json
Authorization: oauth <access-token>
```

```
curl -X GET --header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
'https://<host>/primeapi/v2/learningObjects/certification%3A167658/applicableCertification?include=subLOs'
```

**Hinweis**: Der loId-Wert muss URL-codiert sein. Der Doppelpunkt in einer Zertifizierungs-ID wie certification:167658 ist als %3A codiert.

**Beispielantwort 200 OK**

Die Antwort verwendet dieselbe Struktur wie eine standardmäßige Lernobjektreaktion und gibt die aufgelöste Zertifizierung zurück.

**Wichtig:** Das ID-Feld in der Antwort ist die ID der **aufgelösten**-Zertifizierung, die spezifische Version, die für diesen Teilnehmer gilt. Sie unterscheidet sich in der Regel von der Stammzertifizierungs-ID, die Sie als loId übergeben haben, da der gesamte Zweck dieser API darin besteht, eine Stammzertifizierungs-ID in die richtige aktuelle Version zu übersetzen.

```
{
  "data": {
    "id": "string",
    "type": "string",
    "attributes": {
      "authorNames": [
        "string"
      ],
      "bannerUrl": "string",
      "catalogs": [
        ...
      ]
    }
  }
}
```

**Antwortcodes**

| **Status** | **Bedeutung** |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 200 | Die entsprechende Zertifizierung wurde erfolgreich behoben und wird als Antwort zurückgegeben. |
| 400 | Die angegebene loId ist entweder keine Zertifizierung oder keine Stammzertifizierung. Übergeben Sie die ID der ursprünglichen Zertifizierung, nicht eine Serienversion, als loId. |
| 401 / 403 | In der Anforderung fehlen gültige Teilnehmeranmeldeinformationen, oder die Anmeldeinformationen verfügen nicht über den erforderlichen Zugriff. |
| 404 | Für diese Stammzertifizierung konnte keine aktive Zertifizierung aufgelöst werden. Zum Beispiel, weil jede Version in der Kette zurückgezogen oder gelöscht wurde oder weil die Zertifizierung überhaupt keine registrierte Stammzertifizierungsreferenz hat. Ein 404-Fehler kann auch auftreten, wenn eine Version erfolgreich aufgelöst wurde, der aufrufende Teilnehmer jedoch keinen Katalogzugriff darauf hat. |
| 500 | Unerwarteter Serverfehler beim Auflösen der Zertifizierung. Wiederholen Sie die Anforderung. Wenn der Fehler weiterhin auftritt, wenden Sie sich an den Support. |

**Beispielfehlerantwort**

```
{
  "meta": {
    "error": "string",
    "detail": "string"
  }
}
```

**Hinweis:** Diese API löst die Version für einen Teilnehmer pro Aufruf auf. Es wird keine Liste aller Versionen zurückgegeben, die für eine Stammzertifizierung vorhanden sind.

**Wichtige Punkte**

- **Nicht wiederkehrende Zertifizierungen: I** Wenn die von Ihnen übergebene loId eine Zertifizierung ist, die nicht für eine erneute Zertifizierung konfiguriert ist, gibt die API diese Zertifizierung selbst zurück.

- **Übersprungene Zwischenversionen: I** Wenn die aktive Registrierung eines Teilnehmers direkt von einer früheren Version auf eine spätere verschoben wurde, ohne dass eine aktive Registrierung zwischen den Versionen stattgefunden hat, wird die API weiterhin korrekt in die aktuelle Version des Teilnehmers aufgelöst. Das Vorhandensein von Zwischenversionen, mit denen der Teilnehmer nicht aktiv interagiert hat, hat keine Auswirkungen auf die Auflösung.

- **Gelöschte und eingestellte Zertifizierungen:** Eine gelöschte Zertifizierungsversion wird vollständig von der Lösung ausgeschlossen. Eine eingestellte Zertifizierung kann je nach Status weiterhin in Betracht gezogen werden. Wenn Sie sich darauf verlassen, dass eine bestimmte Version lösbar bleibt, bestätigen Sie ihren aktuellen Status, anstatt den Eintritt in den Ruhestand allein zu akzeptieren, damit sie nicht mehr berücksichtigt wird.

- **Die Auflösung ist deterministisch:** Wenn sich die Registrierungsdaten eines Teilnehmers in einem inkonsistenten Zustand befinden (z. B. sind mehrere Registrierungen als aktuell markiert), wird die API in die zuletzt erstellte Version aufgelöst, anstatt ein unvorhersehbares Ergebnis oder einen Fehler zurückzugeben.

**Hinweis**: Ein Äquivalent dieser API, das für Administratoren vorgesehen ist, ist derzeit nicht verfügbar und wird für eine zukünftige Version bewertet.

### Diese API in Ihrer Integration verwenden

Ein häufiger Anwendungsfall ist eine externe Seite oder ein Portal, auf der bzw. in dem Zertifizierungen aufgeführt sind, auf die ein Teilnehmer zugreifen kann. Anstatt eine direkte Verknüpfung mit einer bestimmten Zertifizierungs-ID herzustellen, die nach einer Wiederholung möglicherweise veraltet ist. Verwenden Sie die Stammzertifizierungs-ID und lösen Sie die richtige Version auf, wenn der Teilnehmer sie auswählt.

&#x200B;1. Speichern oder verweisen Sie Zertifizierungen in Ihrer Integration mit der **Stammzertifizierungs-ID,** der ID der Zertifizierung, wie sie zuerst erstellt wurde, bevor es erneut vorkommt.

&#x200B;2. Wenn ein Teilnehmer eine Zertifizierung auswählt, die er anzeigen oder bearbeiten möchte, rufen Sie GET /primeapi/v2/learningObjects/{loId}/applicableCertification auf, wobei Sie die Stammzertifizierungs-ID als loId übergeben.

&#x200B;3. Verwenden Sie die in der Antwort zurückgegebene Zertifizierungsversion, um den Teilnehmer zum richtigen Ziel zu leiten, unabhängig davon, ob es sich um eine Registrierungsaktion oder eine Ansicht seines aktuellen Fortschritts handelt.

Dadurch wird sichergestellt, dass Teilnehmer immer auf der Version der Zertifizierung landen, die ihrer tatsächlichen Registrierung und ihrem Fortschritt entspricht, auch wenn die Zertifizierung im Laufe der Zeit immer wieder vorkommt und neue Versionen generiert.

## Berichte: Stammtrainings-ID im Teilnehmertranskript

Die Spalte **Stammtrainings-ID** ist standardmäßig im Teilnehmertranskript für alle Konten verfügbar.

| **Zeilentyp** | **Wert der Stammprüfungs-ID** |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| Für die erneute Zertifizierung konfiguriert | Die Stammzertifizierungs-ID, zu der diese Version zurückverfolgt wird |
| Die Zertifizierung ist nicht für die Wiederholung konfiguriert. | Der gleiche Wert wie die Schulungs-ID für diese Zeile |
| Ein in eine Zertifizierung eingebetteter Kurs | Die Stammzertifizierungs-ID der übergeordneten Zertifizierung, nicht die eigene ID des Kurses |
| Ein Kurs oder Lernpfad, der bzw. der nicht Teil einer Zertifizierung ist | Der gleiche Wert wie die Schulungs-ID oder die eingebettete Kurs-ID für diese Zeile. |

**Hinweis**: Bei sehr großen Konten mit einem hohen Volumen von Zertifizierungen werden die Stammtrainings-ID-Werte im Teilnehmertranskript stapelweise aufgelöst. Dies ändert die Genauigkeit der Daten nicht, aber die Erstellung sehr großer Transkripte kann länger dauern.

In dieser Spalte können Sie den vollständigen Verlauf eines Teilnehmers in jeder Version einer wiederkehrenden Zertifizierung gruppieren und Bericht erstatten, anstatt jede Wiederholung als unabhängigen, unabhängigen Datensatz zu behandeln. Jede Wiederholung wird weiterhin als eigene Zeile im Teilnehmertranskript angezeigt. Die Spalte &quot;Stammtrainings-ID&quot; gibt einfach an, welche Zeilen zu derselben zugrunde liegenden Zertifizierung gehören.

**Hinweis:** Verwenden Sie die Spalte &quot;Ursprüngliche Schulungs-ID&quot;, wenn Sie den vollständigen Teilnahmeverlauf eines Teilnehmers über eine wiederkehrende Zertifizierung nachverfolgen müssen.


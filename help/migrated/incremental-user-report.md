---
description: Mit der API für inkrementelle Benutzerberichtsaufträge können Administratoren nur Benutzer exportieren, deren Daten innerhalb eines bestimmten Datumsbereichs geändert wurden. Dadurch entfällt die Notwendigkeit für vollständige Benutzerexporte und eine effizientere Synchronisierung neuer oder aktualisierter Benutzerdatensätze ist möglich.
jcr-language: en_us
title: Inkrementeller Benutzerbericht (Job-API)
source-git-commit: d61e81b0df6a6043b938c65adaabecb5699c2ce9
workflow-type: tm+mt
source-wordcount: '1602'
ht-degree: 1%

---


# Inkrementeller Benutzerbericht (Job-API)

## Übersicht

Der inkrementelle Benutzerbericht von Adobe Learning Manager ist eine neue Job-API-Funktion, mit der Administratoren und Integrationsentwickler nur die Benutzer exportieren können, deren Daten sich in einem bestimmten Datum- und Uhrzeitfenster geändert haben. Anstatt jedes Mal die vollständige Benutzerliste abzurufen, können Sie ein gezieltes Slice anfordern, das nur neue oder geänderte Benutzer abdeckt.

Dieses Dokument behandelt Folgendes:

- Gründe für inkrementelle Berichte und Zeitpunkt ihrer Verwendung
- Funktionsweise - einschließlich des Änderungsverfolgungsmodells
- Die neue Job-API für inkrementelle Benutzerberichte (Payload, Parameter, Paginierung)
- So gehen Sie mit großen Konten um (über 5.000.000 Benutzer)
- Verfolgte und nicht verfolgte Felder
- Einschränkungen und Nicht-Ziele

## Gründe für die Verwendung von inkrementellen Berichten

Dieser Abschnitt erläutert die Motivation für die Funktion und sollte Ihnen bei der Entscheidung helfen, ob inkrementelle oder vollständige Exporte am besten zu Ihrer Integration passen.

## Das Problem mit Vollbenutzer-Exporten

Der aktuelle Vollbenutzerexport (generateUsers-Auftragstyp) gibt bei jeder Ausführung jeden Benutzer in einem Konto zurück. Bei Großunternehmen führt dies zu zwei erheblichen Problemen:

| Kunde | Benutzervolume |
|----------|-------------|
| Kunde A | 2,1 Millionen Anwender |
| Kunde B | 7 Millionen Anwender |
| Kunde C | über 1 Million Benutzer |
| Kunde D | 7,7 Millionen Benutzer (Migration) |


&#x200B;* Bei diesen Größenordnungen läuft die Export-Pipeline bei einer CPU-Auslastung von ca. 90 %, während Daten abgerufen, verarbeitet und gespeichert werden.
&#x200B;* Nachgeschaltete Dashboards (PowerBI, Salesforce, benutzerdefinierte Integrationen) führen bei jedem Durchlauf unveränderte Benutzerdatensätze ein, wodurch Bandbreite und Verarbeitungszeit verschwendet werden.
&#x200B;* Es gibt keine Möglichkeit zu fragen, &quot;welche Benutzer sich seit meinem letzten Export geändert haben?&quot; mit der aktuellen API verwenden.

## Verwendung von inkrementellen Berichten

Verwenden Sie den inkrementellen Export, wenn ein externes System mit den Adobe Learning Manager-Benutzerdaten synchronisiert bleiben muss. Typische Anwendungsfälle:

&#x200B;* Aktualisieren eines Unternehmens-Dashboards (PowerBI, Tableau, SFDC) mit Änderungen an Benutzerprofilen
&#x200B;* Einspeisung nachgelagerter Identitätsverwaltungssysteme mit Rollen-, Status- oder Metadatenänderungen.
&#x200B;* Delta-Sync-Pipelines werden nachts oder stündlich ausgeführt, anstatt vollständige Neuladungen vorzunehmen.
&#x200B;* Reduzierung der Kosten für API-Laden und -Datenübertragung für Konten mit Millionen von Benutzern.

Verwenden Sie den vollständigen Export (generateUsers), wenn Sie eine autoritative Grundlinie benötigen, z. B. bei der ersten Einrichtung oder nach einer langen Lücke zwischen den Synchronisationen.

| Exportmodus | Verwenden, wenn... |
|-------------|-----------|
| Vollständiger Export (generateUsers) | Initial-Bootstrap Konten mit weniger als 50.000 Benutzern; Wiederherstellung nach einem versäumten Synchronisationsfenster. |
| Inkrementeller Export (generateUserIncrementalReport) | Reguläre Delta-Synchronisation; Großkonten; Pipelines, die nur geänderte Datensätze benötigen |

## Aktueller vollständiger Benutzerbericht

(generateUsers) Dieser Abschnitt dokumentiert den vorhandenen Bericht des Job-API-Benutzers als Referenz. Wenn Sie bereits damit vertraut sind, fahren Sie mit dem nächsten Abschnitt fort.

## Funktionsweise

Der aktuelle CSV-Benutzerbericht wird als Auftrag über die Jobs-API gesendet. Eine Snaplogic-Pipeline nimmt den Task auf, führt eine MySQL-Abfrage für die CAPTIVATE-Datenbank aus (user, usergroup, usergroup_user-Tabellen) und generiert eine CSV-Datei.

## Verfügbare Filter

Die Nutzlast unterstützt drei optionale Filter:

&#x200B;* `expandMetadata` - Übergeben Sie true, um Metadaten als separate Spalte zu exportieren.
&#x200B;* `fetchActiveUsers` - Übergeben Sie true, um nur aktive Benutzer zu exportieren.
&#x200B;* `peerAccountId` - So generieren Sie den Benutzerbericht für ein Peer-Konto.

## CSV-Spalten

Die exportierte CSV-Datei enthält die folgenden Spalten:

```
internalUserID, userEmail, customerDefinedUniqueUserId, name, managerEmail,

userType, state, excludedFromGamification, pointsEarned, profile, roles,

dateCreated, lastLoginDate, dateDeleted, uiLocale, contentLocale,

timeZoneCode, userSource, group, AF_location, AF_login, AF_externalaf,

lastSocialActivityDate
```

## Nutzlast anfordern

Jobtyp: generateUsers an. Nur Administratorrolle.

```
{

  "data": {

    "type": "job",

    "attributes": {

      "description": "<description of your choice>",

      "jobType": "generateUsers",

      "payload": {

        "expandMetadata": "<true to export metadata as separate column>",

        "fetchActiveUsers": "<true to export ACTIVE users only>",

        "peerAccountId": "<peerAccountId for peer account report>"

      }

    }

  }

}
```

## Einschränkungen

&#x200B;* Keine datumsbasierte Filterung - jede Ausführung exportiert alle Benutzer.
&#x200B;* Bei großen Konten nicht möglich - Pipeline-Ressourcenauslastung über ~1 Million Benutzer.
&#x200B;* Keine inkrementelle oder Delta-Funktion.

## Inkrementeller Benutzerbericht (generateUserIncrementalReport)

Dieser Abschnitt beschreibt die neue inkrementelle Benutzerberichtfunktion, die in M46 eingeführt wurde. Dies ist der Hauptgegenstand dieses Dokuments.

## Was ist ein inkrementeller Export?

Ein inkrementeller Export gibt nur Benutzer zurück, deren verfolgte Daten sich in einem angegebenen Start- und Enddatum-Zeit-Fenster geändert haben. Das Backend speichert einen Zeitstempel der letzten Änderung für die verfolgten Felder jedes Benutzers. Wenn Sie einen Bericht für ein bestimmtes Fenster anfordern, werden nur Benutzer einbezogen, deren letzte Änderung in dieses Fenster fällt.

## Funktionsweise des Änderungsverfolgungsmodells

Adobe Learning Manager behält einen Zeitstempel der letzten Änderung bei, der aktualisiert wird, wenn sich ein nachverfolgtes Feld für einen Benutzer ändert.

Wenn Sie einen inkrementellen Bericht mit einem start_date_time und end_date_time anfordern, gibt das System Benutzer zurück, deren Zeitstempel der letzten Änderung innerhalb von [start_date_time, end_date_time] liegt. Wenn ein Benutzer sowohl innerhalb als auch nach dem Fenster geändert wurde (d. h. wenn er nach end_date_time erneut geändert wurde), wird dieser Benutzer nicht in den Bericht aufgenommen, da sein Zeitstempel der letzten Änderung jetzt außerhalb des Fensters liegt.

>[!NOTE]
>
>Dies bedeutet, dass ein inkrementeller Export Benutzer erfasst, deren letzte Änderung im angegebenen Fenster vorgenommen wurde - nicht alle Benutzer, die während des Fensters berührt wurden.

## Für Änderungen verfolgte Felder

Ein Benutzer wird in einen inkrementellen Bericht aufgenommen, wenn eines der folgenden Felder geändert wurde:

| Feld | Hinweise |
|---|---|
| userEmail | E-Mail-Adresse des Benutzers |
| name | Vorname des Benutzers |
| managerId | Benutzertabelle speichert managerId. Wenn sich die managerId ändert, wird das Feld als geändert gekennzeichnet. Wenn sich nur die E-Mail-Adresse des Managers ändert (dieselbe managerId), gilt dieses Feld NICHT als geändert. |
| type | Interne oder externe Benutzerklassifizierung |
| state | Aktiv oder gelöscht |
| profile | Benutzerprofilzuweisung |
| Rollen | Hinzufügen oder Löschen von Rollen |
| uiLocale | Gebietsschema der Benutzeroberfläche |
| contentLocale | Inhaltsgebietsschema |
| timeZoneCode | Benutzerzeitzone |
| Aktive Felder (AF_*) | Alle konfigurierten aktiven Felder, z. B. AF_location, AF_login |
| Metadaten | Alle konfigurierten Metadatenfelder |

## Felder, die für Änderungen NICHT verfolgt werden

Die folgenden Felder werden in der CSV-Ausgabe angezeigt, lösen aber keine Aufnahme in einen inkrementellen Export aus, wenn sie sich ändern:

&#x200B;* excludedFromGamification
&#x200B;* pointsEarned
&#x200B;* lastLoginDate
&#x200B;* dateDeleted
&#x200B;* dateCreated
&#x200B;* userSource
&#x200B;* lastSocialActivityDate

## Ausgabeformat

Der inkrementelle CSV-Bericht hat dieselben Spalten und dasselbe Format wie der vollständige Benutzer-CSV-Bericht. Alle Spalten werden in derselben Reihenfolge angezeigt, einschließlich aller aktiven Feld- und Metadatenspalten - unabhängig davon, welche Felder für die exportierten Benutzer geändert wurden.

>[!NOTE]
>
>Wenn ein neues aktives Feld hinzugefügt oder ein vorhandenes Feld entfernt wird, werden alle von dieser Änderung betroffenen Benutzer beim nächsten inkrementellen Export angezeigt. Neue Spalten aus neuen aktiven Feldern werden am Ende des Berichts angehängt, sodass vorhandene Integrationen, die auf die Spaltenposition geklickt werden, nicht beschädigt werden.

## Neue Job-API für inkrementellen Benutzerbericht

Der inkrementelle Benutzerbericht verwendet die Job-API zum Generieren einer CSV-Datei, die Benutzer enthält, deren verfolgte Daten im angegebenen Datum- und Uhrzeitfenster geändert wurden. Verwenden Sie für große Resultsets dasselbe Paginierungsmodell, das weiter unten in diesem Dokument beschrieben wird: reichen Sie in jeder Anforderung dasselbe Datumsfenster ein und übergeben Sie die letzte in der vorherigen Antwort erhaltene Benutzer-ID als fromUserId, um den nächsten Textbaustein abzurufen.

## Arbeitstyp

Jobtyp: generateUserIncrementalReport

## Nutzlast anfordern

```
{

    "data": {

        "type": "job",

        "attributes": {

            "description": "description of your choice",

            "jobType": "generateUserIncrementalReport",

            "payload":{

                 "fullExport": <Pass true to export all users. If fullExport is true, fromDate and toDate are ignored>,

                 "expandMetadata": <Pass true to export metadata as separate columns>,

                 "fromDate": <Start of the change window in ISO format, for example 2020-01-01T18:30:00.000Z>,

                 "toDate": <End of the change window in ISO format, for example 2020-01-31T18:30:00.000Z>,

                 "fromUserId": <For paginated requests, pass the last userId received in the previous response>

            }

        }

   }

}
```

## Nutzlastparameter

| Parameter | Typ | Beschreibung |
|---|---|---|
| fromDate | Zeichenfolge (ISO 8601) | Erforderlich für den inkrementellen Export. Beginn des Änderungsfensters. ISO 8601-Format verwenden. |
| bisDatum | Zeichenfolge (ISO 8601) | Erforderlich für den inkrementellen Export. Ende des Änderungsfensters. ISO 8601-Format verwenden. |
| fromUserId | Zeichenfolge | Optional. Übergeben Sie bei paginierten Anforderungen die letzte in der vorherigen Antwort erhaltene Benutzer-ID als fromUserId. Lassen Sie diesen Parameter für die erste Anforderung aus. |
| expandMetadata | Boolesch | Optional. Wenn dieser Wert auf &quot;true&quot; gesetzt ist, werden Metadaten als separate Spalten exportiert. |

Übergeben Sie für den inkrementellen Export `fromDate` und `toDate`, um das Änderungsfenster zu definieren. Wenn die Ergebnismenge größer als ein Textbaustein ist, setzen Sie den Paginierungsvorgang fort, indem Sie dieselben `fromDate` und `toDate` senden und die letzten `userId` aus der vorherigen Antwort als `fromUserId` übergeben. Wenn fullExport auf &quot;true&quot; gesetzt ist, wird das Datumsfenster ignoriert und die API generiert einen Export für den gesamten Benutzer.

## Verarbeitung großer Konten (500 KB+ Benutzer)

Benutzerberichte werden mithilfe einer Datenplattform-Pipeline generiert und die Ausgabe wird in Blöcken zurückgegeben, um große Konten zu unterstützen. Wenn ein inkrementeller Export mehr als 500.000 Benutzer umfasst, wird der Bericht umbrochen.

## Seitenumbruchmodell

Um alle Seiten für einen großen inkrementellen Export abzurufen, übergeben Sie in jeder Anforderung die gleiche startDateTime und endDateTime und übergeben Sie außerdem die Benutzer-ID des letzten im vorherigen Textbaustein empfangenen Benutzers als fromUserId. Die API gibt die nächste Gruppe von bis zu 500.000 Benutzern zurück, deren Benutzer-ID größer ist als die übergebene fromUserId.

## Paginierungsarbeitsablauf

Schritt 1: Senden Sie die erste Anforderung ohne fromUserId.

```
// First request – no fromUserId

{

  "payload": {

    "startDateTime": "2026-05-01T00:00:00Z",

    "endDateTime": "2026-05-31T23:59:59Z"

  }

}
```

Schritt 2: Erhalten Sie den ersten Block (bis zu 500.000 Benutzer). Notieren Sie sich die letzte Benutzer-ID in der Antwort.

Schritt 3: Senden Sie die nächste Anforderung, wobei Sie dasselbe Datumsfenster und die letzte Benutzer-ID aus der vorherigen Antwort als fromUserId übergeben.

```
// Subsequent request – pass last userId from previous response as fromUserId

{

  "payload": {

    "startDateTime": "2026-05-01T00:00:00Z",

    "endDateTime": "2026-05-31T23:59:59Z",

    "fromUserId": "<last userId from previous response>"

  }

}
```

Schritt 4: Wiederholen Sie diesen Vorgang so lange, bis eine Antwort weniger als 500.000 Datensätze zurückgibt. Dies weist darauf hin, dass Sie die letzte Seite erreicht haben.

| Anforderung | fromUserId-Parameter |
|---|---|
| Erste Seite | VonUserId auslassen |
| Zweite Seite | Übergeben Sie die letzte Benutzer-ID von der ersten Seite als fromUserId. |
| Dritte Seite | Übergeben Sie die letzte Benutzer-ID von der zweiten Seite als fromUserId. |
| ... (Fortsetzung) | ... |
| Letzte Seite | Die Antwort enthält weniger als 500.000 Datensätze |

>[!NOTE]
>
>Stellen Sie sicher, dass `startDateTime` und `endDateTime` in allen paginierten Anforderungen für einen einzelnen Exportlauf identisch bleiben. Eine Änderung des Seitenumbruchs im Datumsfenster führt zu inkonsistenten Ergebnissen.

## Einschränkungen

Der inkrementelle Benutzerbericht ist absichtlich bereichsspezifisch. Die folgenden Funktionen befinden sich außerhalb des Anwendungsbereichs:

&#x200B;* Kein Benutzerprüfungsbericht: Es wird nicht aufgeführt, welche spezifischen Felder geändert wurden.
&#x200B;* Kein Vergleich alter/neuer Werte - der Bericht zeigt nur die aktuellen Feldwerte an.
&#x200B;* Keine Zeitstempel pro Änderung - der Zeitpunkt einzelner Feldänderungen wird nicht angezeigt.
&#x200B;* Keine Angabe der Anzahl der Änderungen - ein Benutzer, der einmal und ein Benutzer, der zehnmal geändert wurde, werden beim Export identisch angezeigt.
&#x200B;* Das vorhandene Berichtsformat bleibt unverändert - die CSV-Spaltenstruktur ist mit dem vollständigen Benutzerbericht identisch.

## Connector-Integration

Der inkrementelle Benutzerbericht wurde für die Verwendung in Adobe Learning Manager-Connectors (PowerBI, Salesforce und andere) als Dropdown-Ersatz für den vollständigen Benutzerbericht in regulären Synchronisierungs-Pipelines entwickelt. Auf diese Weise können Connectors, die heute generateUsers verwenden, zum inkrementellen Modell migrieren, ohne Änderungen am Downstream-Datenschema vorzunehmen.

&#x200B;* Die Ausgabe-CSV ist mit dem vollständigen Benutzerbericht spaltenkompatibel.
&#x200B;* Connectors können den inkrementellen Bericht für Delta-Sync verwenden und für Bootstrap oder Recovery auf den vollständigen Bericht zurückgreifen.
&#x200B;* Unterstützung für Connector-Integration (PowerBI, SFDC)

---
title: Neue Funktionen in dieser Version (Juli 2023)
description: Erfahren Sie mehr über die neuen Funktionen und Verbesserungen im Adobe-Lernmanager
hidefromtoc: true
source-git-commit: c55f9448082c9971c065eec95b59992db95e53dc
workflow-type: tm+mt
source-wordcount: '2052'
ht-degree: 0%

---

# Neue Funktionen in dieser Version (Juli 2023)

## Verbesserte Empfehlungen

Der Adobe Learning Manager hat ein neues und überarbeitetes Empfehlungssystem für Kurse eingeführt. Diese Empfehlungsfunktion nutzt KI-Algorithmen und Nutzerinteressen wie Produkte, Rollen und Stufen, um personalisierte Inhaltsempfehlungen bereitzustellen.

Weitere Informationen finden Sie unter [Recommendations im Adobe-Lernmanager](recommendations-adobe-learning-manager.md).

## Mehrfacheinschreibung

In dieser Version des Adobe-Lernmanagers führen wir eine Multi-Registrierung für Teilnehmer ein, die es Teilnehmern ermöglicht, sich in mehr als einer Instanz eines Kurses zu einem oder verschiedenen Zeitpunkten zu registrieren.

Weitere Informationen finden Sie unter [Mehrere Registrierungen](/help/migrated/authors/feature-summary/courses.md).

### Mehrere Registrierungen in der mobilen App oder immersive Kurse

Teilnehmer können sich nicht für mehrere Instanzen über eine mobile App/in einer immersiven App registrieren. Die Mehrfacheinschreibung wird in der mobilen App und im immersiven mobilen Web nicht unterstützt.

>[!NOTE]
>
>Wenn Sie die Mehrfacheinschreibung aktivieren, werden dem Teilnehmertranskriptbericht für jeden Kurs mehrere Zeilen hinzugefügt (eine Zeile für jede Instanz).
>
>Wenn Sie die Berichtsautomatisierung eingerichtet haben, die nur eine Zeile pro Kurs vorwegnimmt, müssen Sie die erforderlichen Anpassungen an der Berichtsautomatisierung vornehmen, bevor Sie die Funktion zur Mehrfacheinschreibung aktivieren.

### Format der Abzeichen in einer Instanz mit mehreren Registrierungen

Um Abzeichen in einer Instanz mit mehreren Registrierungen zu unterstützen, wird das Abzeichenformat in `userId_badgeId_COURSE_courseId_courseInstanceId`.

### Starten des Players mit mehreren Registrierungen mithilfe eines Headless-Modus

In dieser Version haben wir die Bibliothek geändert, die für die Kommunikation mit dem Headless Player verwendet wird.

Bei der Mehrfachregistrierung müssen Sie die Argumente übergeben, die in ein Objekt eingeschlossen sind.

```
{{startplayer(argument_object) ,
where
argument_object=
{ loId = <loId>, accountId = <accountId>, userId =<userId>, accessToken = <accessToken>, domId = <elementId>, onModuleLoaded = fn(), isMultiEnrolled=<boolean>, instanceId=<instanceId> }
}}
```

## Abschaffung des exavault-Connectors

Diese Version von Adobe Learning Manager enthält einen neuen Connector, der das SFTP-Protokoll der AWS Transfer-Familie verwendet.

Diese Änderung ersetzt auch den ExaVault-Connector, der neuen Benutzern nicht mehr zur Verfügung steht. Sie können jeden Open-Source-FTP-Client als Ersatz für ExaVault verwenden. Weitere Informationen finden Sie unter [Übergang vom Adobe FTP Manager](transition-from-ftp-manager.md).

## Erinnerungen in Outlook für Unterrichtsräume und virtuelle Sitzungen

Von Adobe Learning Manager erstellte Klassenzimmer- und virtuelle Klassenzimmersitzungen, die dem Outlook-Kalender des Teilnehmers hinzugefügt wurden, unterstützen jetzt Erinnerungen aus Outlook konsistent (ähnlich wie Meetingerinnerungen in Outlook).

## Verbesserungen beim Zuweisen von Kenntnissen zu Kursen

Wir haben den Arbeitsablauf für die Zuweisung von Kenntnissen für Autoren verbessert. Die Liste der Qualifikationsvorschläge auf der Seite &quot;Kurseinstellungen&quot; enthält jetzt eine Typeahead-Suchfunktion. Autoren können jetzt nach Kenntnissen suchen, indem sie die ersten Zeichen eingeben, und Vorschläge werden basierend auf der Eingabe in der Dropdown-Liste Kenntnisse angezeigt. Dank dieser Verbesserung müssen Autoren nicht durch die vollständige Liste blättern, um Kenntnisse zu Kursen zu suchen und zuzuweisen.

## Verbesserungen des vom Manager genehmigten Kursarbeitsablaufs

Von einem Manager genehmigte Kurse stellen jetzt sowohl Managern als auch Teilnehmern geeignete Fehlerinformationen zur Verfügung.

![Fehlermeldungen](assets/error-messages.png)

Manager können jetzt relevante Fehlermeldungen mit Informationen anzeigen (z. B. wenn die Registrierungsfrist verstrichen ist), wenn sie eine Kursanforderung nicht genehmigen können. Teilnehmern werden der Fehler und die Abhilfemaßnahme angezeigt.

## Neuer Lernplanbericht

Administratoren/benutzerdefinierte Administratoren können jetzt eine Liste aller Lernpläne im Konto und Metadaten wie Status, anwendbare Benutzergruppen, Triggerinformationen, Kurse/Lernpfade im Lernplan und Erinnerungsinformationen exportieren.

## Bericht zum Verfolgen anstehender eingestellter Instanzen

Der Schulungsbericht enthält eine zusätzliche Spalte, in der der Ausfülltermin der in den Kursen oder Lernpfaden vorhandenen Instanzen angezeigt wird, sodass Administratoren und Autoren wissen, welche Instanzen eingestellt werden, und die erforderlichen Maßnahmen ergreifen können.

## Verbesserungen zum Erfassen von Kursbewertungen von Teilnehmern

Ein Popup-Fenster zum Erfassen der Sternebewertung für einen Kurs wird angezeigt, sobald der Benutzer das letzte Modul im Kurs abgeschlossen hat.

![Einschaltquote](assets/ratings.png)

## E-Mail-Vorlagen anpassen

E-Mail-Vorlagen im Learning Manager enthalten jetzt vollständig bearbeitbare Abschnitte, was eine größere Flexibilität bei der Anpassung der E-Mail-Kommunikation basierend auf Messaging- und Branding-Präferenzen bietet.

Weitere Informationen finden Sie unter [E-Mail-Vorlage anpassen](/help/migrated/administrators/feature-summary/email-templates.md#flexibility-in-customizing-the-templates).

## Verbesserungen für den Planungsassistenten

Optimieren Sie den Prozess der Auswahl eines Kursleiters für Klassenzimmer oder virtuelle Sitzungen. Dem Feld &quot;Kursleiter&quot; im Planungsassistenten wurde ein Benutzergruppenfilter hinzugefügt. Autoren können Kursleiter jetzt basierend auf &quot;Kursleiterkenntnisse&quot; und beliebigen zusätzlichen Parametern wie Standort, Sprache, Bezeichnung usw. filtern.

Weitere Informationen finden Sie unter [Benutzergruppenfilter im Planungsassistenten](/help/migrated/authors/feature-summary/courses.md#user-group-filter).

## Verbesserungen am Arbeitsablauf für das Einstellen von Lernobjekten

Autoren können jetzt ein **Automatische Einstellung** Datum für einen Kurs. Dadurch wird eine Kataloginflation im Laufe der Zeit verhindert, und die Kurse müssen manuell zurückgesetzt werden.

Administratoren können auch auf Kontoebene die Art des Zugriffs auf eingestellte Lernobjekte festlegen.

Der Schulungsbericht enthält eine neue Spalte, **Automatisches Abgangsdatum**, um das Einstellungsdatum für jedes Lernobjekt anzuzeigen (sofern festgelegt).

## Katalogbeschriftungswerte nach Autoren

Autoren können jetzt ihre Werte für Katalogbeschriftungen beim Erstellen oder Bearbeiten eines Kurses hinzufügen. Administratoren können diese Funktion auf Kontoebene aktivieren. Nachdem ein Autor einen neuen Katalogbeschriftungswert hinzugefügt hat, wird er Teil der Typeahead-Suche.

![Katalog auswählen](assets/select-catalog.png)

## Verbesserungen an der Kurssuche für Administrator-, Autoren- und Managerrollen

Es wurden Suchverbesserungen für Administrator-, Autoren- und Managerrollen vorgenommen. Sie können jetzt mit Stichwörtern nach den Titeln suchen. Dies gilt für Kurse, Lernpfade und Zertifizierungen.

## Benachrichtigungen für Migrationsfehler

Integrations-Administratoren werden per E-Mail benachrichtigt, wenn Import- oder Exportvorgänge während der Migration oder bei Verwendung von Daten-Connectors wie PowerBI, FTP, Box usw. fehlschlagen.

## Konfiguration mehrerer Manager über APIs

Der Gruppe von APIs für verwaltete Büros wurde eine neue API zur Unterstützung der Konfiguration mit mehreren Managern hinzugefügt.

## Verbesserungen an der Registrierungs-API

Die Enrollment API wurde verbessert, um Massenanmeldungen in großem Umfang zu unterstützen und zu optimieren.

## Mobile App - Anzeigen von Inhalten offline

Teilnehmer können Inhalte im Offline-Modus herunterladen und nutzen. Verschachtelte und flexible Lernpfade werden für die Offline-Anzeige nicht unterstützt.

*In dieser Version wird die Offline-Inhaltsanzeige nur für englische Inhalte unterstützt.*

## Barrierefreiheit

Es wurden mehrere Verbesserungen zur Verbesserung der Barrierefreiheit implementiert, einschließlich Verbesserungen zur Optimierung der Lesbarkeit für Bildschirmleseprogramme.

## Unterstützung für mobile Apps

Mit der nächsten Hauptversion unterstützt die mobile Adobe Learning Manager-App nur die drei neuesten mobilen Betriebssystemversionen.

## Inhalte auf LinkedIn

LinkedIn-Inhalte werden in der immersiven App im Safari-Browser nicht wie erwartet geladen. Um dieses Problem zu umgehen, führen Sie die folgenden Schritte aus:

1. Wählen Sie auf dem Gerät **[!UICONTROL Einstellungen]** > **[!UICONTROL Safari]**.
1. Deaktivieren **Cross-Site-Tracking verhindern**.
1. Deaktivieren **Alle Cookies blockieren**.
1. Melden Sie sich bei der Immersive App an.
1. Spielen Sie den Inhalt ab.
1. Lassen Sie die Popups zu.

## Weitere Verbesserungen

### Wechseln von Instanzen in MS Teams

Ein Teilnehmer kann bis zu seinem Abschluss zu einer anderen Kursinstanz wechseln und den Kursfortschritt beibehalten.

### Unterstützung mehrerer Anmeldungen in MS Teams

Ein Teilnehmer kann sich in einer anderen Kursinstanz registrieren, unabhängig vom Abschlussstatus in allen vorherigen Instanzen. Dadurch kann sich der Teilnehmer in mehreren Instanzen desselben Kurses registrieren.

### Kurshinweise unterstützen die Mehrfacheinschreibung in MS Teams

Kurshinweise sind auf Kursinstanzebene verfügbar, um die Mehrfacheinschreibung zu unterstützen.

## API-Änderungen

Weitere Informationen zu den API-Änderungen finden Sie unter [Adobe Learning Manager-API-Referenz](https://captivateprime.adobe.com/docs/primeapi/v2/).

### API-Unterstützung für neue Empfehlungen

**GET /account**

Gibt zurück, wenn prlRecommendations aktiviert ist.

**Anfrage**

`https://learningmanagerstage1.adobe.com/primeapi/v2/account`

**GET /data?filter.recommendationCriteria=product**

Gibt die Liste der Produkte/Themen zurück. Die Ergebnisse hängen von den Kontoeinstellungen ab, die bestätigen, ob alle Produkte für den Teilnehmer oder den Katalog sichtbar sind, der für Produkte/Themen sichtbar ist.

**Anfrage**

`https://learningmanagerqe.adobe.com/primeapi/v2/data?filter.recommendationCriteria=product&filter.showAllRecommenda`

**`GET /data?filter.recommendationCriteria=role`**

Gibt die Liste der empfohlenen Rollen zurück.

**Anfrage**

`https://learningmanagerqe.adobe.com/primeapi/v2/data?filter.recommendationCriteria=role&filter.showAllRecommendationCriteria=false`

**`GET /data?filter.recommendationCriteria=level`**

Gibt die Liste der empfohlenen Rollen zurück.

**Anfrage**

`https://learningmanagerqe.adobe.com/primeapi/v2/data?filter.recommendationCriteria=level&filter.showAllRecommendationCriteria=false`

**POST /search/query**

Die Suche umfasst auch Produkte und Rollenparameter in der Abfrage. Es gibt keine Änderungen in Abfrage und Text. Wir werden neue Sortieroptionen hinzufügen.

**Anfrage**

`https://learningmanagerstage1.adobe.com/primeapi/v2/search/query?...`

**GET /learningObjects**

Das Lernobjektmodell gibt Empfehlungen mit dem Tag &quot;Autor&quot; zurück, wenn die PRL-Empfehlung live ist.

**Anforderungs-URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/learningObjects?sort=recommendationScore&filter.recommendationProducts=...&filter.recommendationRoles=...&filter.excludeIgnoredRecommendations=true`

POST /learningObjects/query

Die folgenden Attribute werden im Hauptteil des Abfrageaufrufs unterstützt:

```javascript {line-numbers="true"}
{
  "filter.announcedGroups": [
    "string"
  ],
  "filter.bookmarks": true,
  "filter.catalogIds": [
    "string"
  ],
  "filter.cityName": [
    "string"
  ],
  "filter.duration.range": [
    "string"
  ],
  "filter.effectiveModifiedDate.fromDate": "string",
  "filter.effectiveModifiedDate.toDate": "string",
  "filter.excludeIgnoredRecommendations": true,
  "filter.ignoreEnhancedLP": true,
  "filter.ignoreHigherOrderLOEnrollment": true,
  "filter.lang.subLOs": true,
  "filter.lang.twoLetterCode": true,
  "filter.learnerState": [
    "string"
  ],
  "filter.loFormat": [
    "string"
  ],
  "filter.loTypes": [
    "string"
  ],
  "filter.price": "string",
  "filter.priceRange": [
    "string"
  ],
  "filter.recommendationLevels": [
    "string"
  ],
  "filter.skill.level": [
    "string"
  ],
  "filter.skillName": [
    "string"
  ],
  "filter.tagName": [
    "string"
  ],
  "language": [
    "string"
  ],
  "preferredSortPartitionOrder": [
    "string"
  ],
  "showLoContentSource": true,
  "useCache": true,
  "filter.recommendationProducts": [
    {
      "levels": [
        "string"
      ],
      "name": "string"
    }
  ],
  "filter.recommendationRoles": [
    {
      "levels": [
        "string"
      ],
      "name": "string"
    }
  ]
}
```

**GET /recommendationProducts**

Ruft das PRL-Produkt nach recommendationProduct Id ab.

**Anforderungs-URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/recommendationProducts`

GET /recommendationRoles

Ruft das PRL-Produkt nach recommendationProduct Id ab. Es werden nur sichtbare Rollen von (Lernobjekte) zurückgegeben.

**Anforderungs-URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/prlRecommendations/roles`

`POST /users/{id}/recommendationPreferences`

Erstellt PRL-Empfehlungsvoreinstellungen/erstellt diese neu (Override). Beispiel-Nutzlast:

```javascript {line-numbers="true"}
{
    "data": {
        "id": "userRecommendationPreferences:14755328",
        "type": "userRecommendationPreferences",
        "attributes": {
            "products": [
                {
                    "id": "recommendationProduct:1",
                    "dateCreated": "2023-05-07T20:00:00.000Z"
                },
                {
                    "id": "recommendationProduct:37",
                    "dateCreated": "2023-05-07T21:00:00.000Z"
                }
            ],
            "roles": [
                {
                    "id": "recommendationRole:23",
                    "dateCreated": "2023-05-07'T'21:00:00.000'Z'"
                },
                {
                    "id": "recommendationRole:1",
                    "dateCreated": "2023-05-07'T'20:01:00.000'Z'"
                },
                {
                    "id": "recommendationRole:2",
                    "dateCreated": "2023-05-07'T'19:02:00.000'Z'"
                },
                 {
                    "id": "recommendationRole:3",
                    "dateCreated": "2023-05-07'T'18:02:00.000'Z'"
                },
                {
                    "id": "recommendationRole:20",
                    "dateCreated": "2023-05-07'T'17:02:00.000'Z'",
                    "levels": [
                        "INTERMEDIATE"
                    ]
                }
            ]
        }
    }
}
```

**`GET /users/{id}/recommendationPreferences`**

**Anforderungs-URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2//users/123/recommendationPreferences`

**`DELETE /users/{id}/recommendationPreferences`**

Löscht die Benutzereinstellungen für PRL-Empfehlungen für ein Produkt oder eine Rolle.

**Anforderungs-URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/users/123/recommendationPreferences?ids=recommendationRole:123,recommendationRole:234`

Parameter :

IDs = Liste der zu löschenden IDs

**PATCH /users/{id}/recommendationPreferences**

Teilweise Hinzufügung/Aktualisierung. Beispiel-Nutzlast:

```javascript {line-numbers="true"}
{
  "data": {
    "id": "userRecommendationPreferences:<USER_ID>",
    "type": "userRecommendationPreferences",
    "attributes": {
      "roles": [
        {
          "id": "recommendationRole:123",
          "type": "recommendationRole",
          "attributes": {
            "levels": [
              "INTERMEDIATE"
            ]
          }
        },
        {
          "id": "recommendationRole:123",
          "type": "recommendationRole",
          "attributes": {
            "levels": [
              "ADVANCED"
            ]
          }
        }
      ]
    }
  }
}
```

**POST /recommendationPreferences/learningObjects/{id}/ignore**

Fügen Sie gesperrten Empfehlungen LO hinzu.

**Anforderungs-URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/recommendationPreferences/learningObjects/{id}/ignored`

**`DELETE /recommendationPreferences/learningObjects/{id}/ignore`**

Löscht LO aus gesperrten Empfehlungen.

**Anforderungs-URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/recommendationPreferences/learningObjects/{id}/ignored`

**`GET /users/{id}/recommendationStrips`**

Ruft alle Streifen ab, die zum Anzeigen von PRL-Empfehlungen verwendet werden sollen

### Unterstützung mehrerer Registrierungen für API

**GET /primeapi/v2/account**

Zwei neue Attribute werden hinzugefügt:

* instanceSwitchEnabled
* multiEnrollmentEnabled

**GET /users/{userId}/userNotifications**

Die Kursinstanz-ID wurde in Benachrichtigungen im neuen Metadatenattribut hinzugefügt.

**GET /learningObjects**

In der Registrierungsbeziehung wird nur die primäre Registrierung angezeigt, d. h. die zuerst registrierte oder die zuerst abgeschlossene Registrierung.

**`GET /learningObjects/{id}`**

In der Registrierungsbeziehung wird nur die primäre Registrierung angezeigt, d. h. die zuerst registrierte oder die zuerst abgeschlossene Registrierung.

**`GET /learningObjects/{loId}/instances/{loInstanceId}`**

Dem LO-Instanzmodell wird eine neue Beziehung hinzugefügt.

**`GET /enrollments/{id}`**

Abrufen der Registrierung für mehrere Kurse.

**`DELETE /enrollments/{id}`**

Hebt die Registrierung für eine bestimmte Lernobjektinstanz auf.

**POST /Registrierungen**

Unterstützt die Registrierung in verschiedenen Instanzen.

**GET /enrollments**

Ruft Registrierungen nur für primäre Registrierungen für das Lernobjekt ab.

**`GET /learningObjects/{id}/note`**

Ruft eine Liste mit Anmerkungen für einen Kurs ab.

**`GET /learningObjects/{lo_id}/instances/{loi_id}/note`**

Ruft eine Liste mit Anmerkungen für einen Kurs und die Instanz ab.

**`GET /learningObjects/{id}/resources/{loResourceId}/note`**

Ruft eine Liste mit Anmerkungen für eine Ressource in einem Kurs ab.

**`POST /learningObjects/{id}/resources/{loResourceId}/note`**

Fügt eine Notiz in einem Modul für einen Kurs für einen bestimmten Kurs hinzu.

**`DELETE /learningObjects/{id}/resources/{loResourceId}/note/{noteId}`**

Löscht bestimmte Notizen aus einem gegebenen Modul für eine bestimmte Instanz (Teil der loResource-ID).

**`GET /learningObjects/{id}/resources/{loResourceId}/note/{noteId}`**

Ruft eine bestimmte Notiz in einem Modul in einem Kurs für eine bestimmte Instanz ab (Teil von loResourceId).

**`PATCH /learningObjects/{id}/resources/{loResourceId}/note/{noteId}`**

Aktualisiert bestimmte Anmerkungen aus einem gegebenen Modul für eine bestimmte Instanz (Teil der loResource-ID).

**Änderungen an der Admin-API**

* GET /users/{id}/enrollments
* POST /users/{id}/enrollments
* DELETE /users/{id}/enrollments/{enrollmentId}
* PATCH /users/{id}/enrollments/{enrollmentId}

### Erzwungene Felder für Endpunkte

Produkte und Rollen werden nur geladen, wenn sie erzwungen werden.

Beispielanforderung

* GET `https://learningmanagerstage1.adobe.com/primeapi/v2/learningObjects/course%3A7418798?enforcedFields[learningObject]=products`
* GET `https://learningmanagerstage1.adobe.com/primeapi/v2/users/11255638/userBadges?include=model&page[offset]=0&page[limit]=10&sort=dateAchieved&enforcedFields[learningObject]=products,roles`

### API-Änderungen in der Stemmingimplementierung für die Suche (englisches Gebietsschema)

Wortstamm ist der Prozess, bei dem ein Wort auf seine Grundform reduziert wird. Dadurch werden die Varianten einer Wortübereinstimmung während einer Suche sichergestellt. Gehen und Gehen können beispielsweise auf das gleiche Wort wie im Stamm zurückgeführt werden: Gehen. Nach dem Wortstamm würde ein Vorkommen eines der Wörter dem anderen in einer Suche entsprechen.

In dieser Version haben wir Stemming für englische Gebietsschemas hinzugefügt, der die folgenden Varianten enthält: en_US, en_AU, en_GB.

Das Attribut stemmed gibt an, ob stemming in den Suchergebnissen erforderlich ist. Dies ist standardmäßig auf False festgelegt.

### Entfernen von V1-Endpunkten

V1-APIs funktionieren mit dieser Version nicht mehr. Weitere Informationen finden Sie unter [Entwicklerhandbuch](/help/migrated/integration-admin/feature-summary/developer-manual.md).

### Benachrichtigungen für die Kursregistrierung oder -abmeldung

Diese Version bietet Unterstützung für die Kursinstanzen-ID mit Benachrichtigungen im neuen Metadatenattribut.

### L1-Feedback-Unterstützung

Ermöglicht es dem Teilnehmer, Feedback auf jeder Instanzebene der Funktion für mehrere Registrierungen abzugeben.

**API:** `POST /enrollments/{id}/l1Feedback`

### LO erzwungene Feldliste

In dieser Version müssen Sie Abschnitte, prequisiteConstraints, prerequisiteLOs, subLOs, additionalResources, additionalLOs, Instanzen, catalogLabels explizit an das learningObject senden.

Beispiel:

`enforcedFields[learningObject]=prerequisiteLOs,instances`

### Hinweis zur Aufhebung der Registrierung für die nächste Version

* Überschreiben-Flag für Teilnehmer-APIs.
* Wir ändern den Standardwert für highlightResults=false. Außerdem ändern wir den Standard von snippetType=courseName.
* Wir verwerfen matchType=bool im Suchendpunkt.
* autoCompleteMode verfügt über das Attribut [Veraltet] -Tag und um dieselbe Funktionalität von autoCompleteMode =false bereitzustellen, wurde ein matchType mit dem Namen Match hinzugefügt.

### Abzeichen-ID-Format mit mehrfacher Registrierung

Um Abzeichen mit mehreren registrierten Instanzen zu unterstützen, ändern wir das Format von Kursabzeichen von `userId_badgeId_COURSE_courseId to userId_badgeId_COURSE_courseId_courseInstanceId` zur eindeutigen Identifizierung von Abzeichen.

## Versionshinweise

Weitere Informationen zu aktuellen und früheren Versionen der Learning Manager-Webanwendung und -Geräte-App finden Sie unter [Versionshinweise](/help/migrated/release-note/release-notes.md).

## Bekannte Probleme oder Einschränkungen in dieser Version

Im Folgenden sind die Einschränkungen dieser Version aufgeführt:

### Anzeigen von Offline-Inhalten in der mobilen App

Folgendes wird beim Anzeigen von Offlineinhalten in der App nicht unterstützt:

* Flex-Kurse, Lernpläne oder Zertifizierungen.
* Erweiterte Kurse, Lernpläne oder Zertifizierungen.
* Mehrere Quiz aktiviert - Kurse, Lernpläne oder Zertifizierungen.
* Harvard Manage Mentor, Content Marketplace, GetAbstract oder LinkedIn Courses, Learning Plans oder Certifications.
* Lernpläne und Zertifikate mit aktivierten Voraussetzungen.
* Eingestellte Kurse, Lernpläne oder Zertifizierungen.
* Kurse, Lernpläne oder Zertifizierungen, deren Frist abgelaufen ist.
* Externe Zertifikate.
* E-Commerce-fähige Kurse, Lernpläne oder Zertifizierungen.

Bei den folgenden Lernpfaden, Kursen oder Zertifizierungen gibt es einige Probleme mit der Offline-Synchronisierung:

* Alle Lernpfade.
* Alle internen Zertifikate.
* Content mit POST.

### Recommendations

Folgende Elemente werden im neuen Empfehlungssystem nicht für &quot;Produkt/Rolle/Ebene&quot; unterstützt:

* Adobe Experience Manager, Teams, SFDC und Nicht angemeldet.
* Die mobile App unterstützt das Bearbeiten von Produkten und Rollen auf der Seite &quot;Empfehlung&quot; nicht.
* Die Zuordnung ist während der Migration nicht möglich.
* Automatisches Tagging von LinkedIn, Inhalts-Marketplace und anderen externen Kursen, Lernplänen oder Zertifizierungen.
* Wiederherstellen der Option &quot;Kenntnisbasiert&quot; oder &quot;Klassisch&quot; nach dem Livestream.
* Das Suchmenü für Produkte und Rollen in der Teilnehmer-App.
* Massen-Zuordnung von Kursen, Lernplänen oder Zertifizierungen und Benutzern in der Admin-App.

## Systemanforderungen

[Systemanforderungen für Learning Manager](/help/migrated/system-requirements.md)

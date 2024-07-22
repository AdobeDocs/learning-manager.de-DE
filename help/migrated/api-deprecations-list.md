---
jcr-language: en_us
title: API-Veraltungen in Adobe Learning Manager
description: Wenn sich die APIs in Adobe Learning Manager weiterentwickeln, werden APIs regelmäßig neu organisiert oder aktualisiert. Wenn sich APIs weiterentwickeln, wird die alte API verworfen und schließlich entfernt. Diese Seite enthält Informationen, die Sie benötigen, wenn Sie von veralteten API-Versionen zu neueren und stabileren API-Versionen migrieren.
contentowner: saghosh
exl-id: 0fe9a3cb-9114-42d6-81ae-1a4f28c984fa
source-git-commit: 670d0477b246af2a0257e41eca799817e391b348
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 32%

---

# API-Veraltungen und -Änderungen in Adobe Learning Manager

## API-Veraltungen in der Version März 2024 von Adobe Learning Manager

<!-- ### Changes in Rate Limits

With the next release of Adobe Learning Manager, we're restructuring API rate limits for new accounts. For existing accounts, only the Admin APIs will be rate-limited. After 90 days (about 3 months), we will restructure rate limits for all APIs, but existing accounts will be whitelisted according to current usage. Existing accounts need to revisit their learner API usage. 

For new accounts, if they want to increase the rate limits, they must contact the Customer Success team of ALM. 

#### Which APIs will be rate limited 

For new accounts, all Admin, Learner, and Search APIs will have rate limits and burst enforced.  

The API burst rate or burst limit refers to the maximum number of requests allowed to be made to an API in a short burst within a limited timeframe. 

The following table lists the rate and burst limits for the APIs.

<table>
    <tr>
        <th>API</th>
        <th>Number of requests-RPM</th>
        <th>Number of requests-Burst</th>
    </tr>
    <tr>
        <td>Admin</td>
        <td>5</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Learner</td>
        <td>20</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Search</td>
        <td>50</td>
        <td>5</td>
    </tr>
</table>
-->

### Änderungen an den Versatzgrenzen

Aufgrund der hohen Anzahl von Datensätzen, die durch den Offsetwert abgerufen werden, und der Verlangsamung der Gesamtleistung erzwingen wir eine Beschränkung auf **500** Datensätze. In der nächsten Version gibt die **GET Users**-API für Administratoren und Teilnehmer maximal **500** Datensätze zurück.

Wenn Sie weitere Datensätze abrufen müssen, verwenden Sie die **GET Jobs**-API.

<!--### Exclude paths 

At present, Learning Manager APIs follow a graph data structure, which allows you to fetch data by traversing the API model through includes. Even though you could traverse an API up to seven levels, fetching the data using a single API call is computationally expensive. 

We recommend that all existing and new customers make small calls multiple times instead of one large call. This approach will prevent unwanted data from being loaded in the call. 

We want to enforce these restrictions on new accounts and maintain a whitelist of existing accounts.-->

#### Welche Pfade veraltet sind

Die folgenden Pfade sind veraltet:

* /learningObjects
   * Veraltete Pfade:
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Neue Pfade:
      * enrollment.loInstance.loResources
      * instances.loResources

* /learningObjects/{id}
   * Veralteter Pfad:
      * enrollment.instances.subLoInstances.learningObject
   * Neuer Pfad:
      * enrollment.instances.subLoInstances

* /enrollments
   * Veralteter Pfad:
      * loInstance.learningObject.enrollment
   * Neuer Pfad:
      * loInstance.learningObject

* /learningObjects/{id}
   * Veralteter Pfad:
      * instance.subLoInstances.learningObject.enrollment.loResourceGrades
   * Neuer Pfad:
      * instance.subLoInstances

<!--### Instance summary count changes 

Currently, in the LO summary endpoint, you fetch the number of all possible instances. For example, for a course, you can view the number of enrollments and waitlists in the response for **GET /learningObjects/{loId}/instances/{loInstanceId}/summary**. You can then view the completionCount and enrollmentCount in the response. If the course is a VC or classroom, you can also view its seat limit and waitlist limit. 

The process of retrieving the completion and enrollment counts is computationally expensive, therefore the calculation is done on a request basis. If the data is not present in the cache, the data is reloaded, which is computationally intensive. If there are many users enrolling in a course, the counts will be large, and effectively impacts CPU performance. 

In the next release of Adobe Learning Manager, in the LO Instance summary endpoint, the completionCount, enrollmentCount, seatLimit, and waitlistCount are cached. The cached information persists till there are changes in enrollments or unenrollments. For counts exceeding 1000 enrollments, we'll assume the estimated counts, and invalidate the results for all existing and new accounts.

>[!NOTE]
>
>For counts, such as, completionCount, enrollmentCount, seatLimit, and waitlistCount exceeding1000, it's advisable to interpret them as estimates rather than precise figures, as these will be retrieved from cache.-->

### Nach Name sortieren

In der nächsten Version von Adobe Learning Manager sind name und -name im Sortierfeld der folgenden APIs veraltet:

* GET /userGroups/{userGroupId}/users
* GET /users

>[!NOTE]
>
>Bei allen vorhandenen und neuen Konten ist die Sortierung nach Name und -name veraltet.


## API-Veraltungen in der Version November 2023 von Adobe Learning Manager

### Überschreiben-Flag

In der Adobe Learning Manager-Version vom November 2023 haben wir das Überschreibungs-Flag für die APIs eingestellt. Das Überschreiben-Flag ist kein Teil der öffentlichen API-Spezifikation und für Backend-Tests vorgesehen. Das Flag wird jetzt für Teilnehmer-APIs eingestellt. Das Flag ist jedoch weiterhin für Admin-APIs gültig.

Der Grund, warum wir das Flag für Teilnehmer-APIs verwerfen, ist, dass das Überschreibungsflag eine große Datenmenge über die Teilnehmer-APIs abgerufen hat.

In Zukunft wird die folgende Teilnehmer-API nicht mehr funktionieren, da sie das Überschreiben-Flag aufweist.

_/primeapi/v2/users?page[offset]=0&amp;page[limit]=10&amp;sort=id&amp;override=TRUE_

### API-Änderungen für kompetenzbasierte neue Empfehlungen

Adobe Learning Manager verbessert die Empfehlungen für Kunden- und Partnerkonten. Diese Verbesserung des Empfehlungsalgorithmus durch die Änderung des Ranglistenalgorithmus für Kurs, Lernpfad und Zertifizierung verbessert die Benutzererfahrung bei der Suche nach Inhalten.

Der Algorithmus lässt keine Empfehlungen auf Peer-Basis mehr zu. Die Änderung wirkt sich nicht auf die bestehenden Benutzer(innen) aus, aber die Option “Branchenspezifisch“ ist weiterhin vorhanden. Bei der Option “Benutzerdefiniert“ lässt Adobe-Lern-Manager keine benutzerdefinierte Peer-basierte Auswahl mehr zu.

Die Peer-Gruppe wird jetzt zu einem Konto, und die Teilnehmenden sehen eine Zeichenfolge, die die aktuellen Themen in der Gruppe anzeigt. Alle Empfehlungen sind erklärbar. Wenn Sie beispielsweise etwas zu einem Thema anzeigen, wird auf der Karte auf dem Streifen der Grund für den Kurs angezeigt.

### Änderungen am Bericht für Benachrichtigungen

In früheren Versionen von Adobe Learning Manager verfügte der Bericht zur Benachrichtigungsankündigung über keine Filter. Adobe Learning Manager hat alle Benachrichtigungen im Konto heruntergeladen.

In der Version vom November 2023 haben wir einen Datumsfilter hinzugefügt, mit dem Sie die Benachrichtigungen innerhalb eines bestimmten Zeitraums herunterladen können.  Sie können den Bericht jedoch nur für die letzten sechs Monate herunterladen.

### Abschaffung der hohen Versatzwerte im Endpunkt GET /users

Um die Systemleistung zu verbessern und die Ressourcennutzung effektiver zu verwalten, verfügt der Adobe über veraltete hohe Versatzwerte im Endpunkt GET /users für die Bereiche **ADMIN** und **LEARNER**. Es wird empfohlen, die **Jobs-API** zu verwenden, um die Datensätze mit einem Offsetwert abzurufen.


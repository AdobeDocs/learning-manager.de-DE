---
jcr-language: en_us
title: API-Veraltungen im Adobe Learning Manager
description: Wenn sich die APIs im Adobe Learning Manager weiterentwickeln, werden APIs regelmäßig neu organisiert oder aktualisiert. Wenn sich APIs weiterentwickeln, wird die alte API verworfen und schließlich entfernt. Diese Seite enthält Informationen, die Sie benötigen, wenn Sie von veralteten API-Versionen zu neueren und stabileren API-Versionen migrieren.
contentowner: saghosh
source-git-commit: 01cdcd816fe101af55adf0902f4e3660a1a098ce
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 21%

---


# API-Veraltungen und Änderungen im Adobe Learning Manager

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

Aufgrund der hohen Anzahl von Datensätzen, die durch den Offsetwert abgerufen werden, und der sich verschlechternden Gesamtleistung erzwingen wir eine Beschränkung der **500** Datensätze. In der nächsten Version für Admin und Teilnehmer wird das Dialogfeld &quot; **GET Users** API gibt maximal Folgendes zurück: **500** Datensätze.

Wenn Sie weitere Datensätze abrufen müssen, verwenden Sie den Katalog **GET Jobs** API.

Die Änderung der Verrechnungslimits gilt für alle Neukunden. Für Bestandskunden gilt die 90-Tage-Regel.

### Ausschließen von Pfaden

Derzeit folgen Learning Manager-APIs einer Diagrammdatenstruktur, mit der Sie Daten abrufen können, indem Sie das API-Modell durch Includes durchlaufen. Auch wenn Sie eine API auf bis zu sieben Ebenen durchlaufen könnten, ist das Abrufen der Daten mit einem einzigen API-Aufruf rechnerisch kostspielig.

Wir empfehlen allen bestehenden und neuen Kunden, mehrmals anstatt eines einzigen großen Anrufs kleine Anrufe zu tätigen. Dadurch wird verhindert, dass unerwünschte Daten in den Aufruf geladen werden.

Wir möchten diese Einschränkungen für neue Konten durchsetzen und eine Positivliste der bestehenden Konten führen.

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

### Änderungen an der Instanzzusammenfassungsanzahl

Derzeit wird im Endpunkt der LO-Zusammenfassung die Anzahl aller möglichen Instanzen abgerufen. Beispielsweise können Sie für einen Kurs die Anzahl der Registrierungen und Wartelisten in der Antwort für **GET /learningObjects/{loId}/instances/{loInstanceId}/summary**. Anschließend können Sie in der Antwort die Ergebnisse &quot;completeCount&quot; und &quot;enrollmentCount&quot; anzeigen. Wenn es sich bei dem Kurs um einen VC oder ein Klassenzimmer handelt, können Sie auch die Sitzplatzbeschränkung und die Wartelistenbeschränkung anzeigen.

Der Abruf der Abschlusses- und Registrierungszahlen ist rechnerisch aufwändig, sodass die Berechnung auf Anforderungsbasis erfolgt. Wenn die Daten nicht im Cache vorhanden sind, werden die Daten neu geladen, was rechenintensiv ist. Wenn sich viele Benutzer für einen Kurs registrieren, ist die Anzahl groß und wirkt sich effektiv auf die CPU-Leistung aus.

In der nächsten Version von Adobe Learning Manager werden im zusammenfassenden Endpunkt der LO-Instanz die Werte &quot;completeCount&quot;, &quot;enrollmentCount&quot;, &quot;seatLimit&quot; und &quot;waitlistCount&quot; zwischengespeichert. Die zwischengespeicherten Informationen bleiben erhalten, bis sich Registrierungen oder Aufhebung der Registrierung ändern. Bei einer Anzahl von mehr als 1000 Registrierungen übernehmen wir die geschätzte Anzahl und annullieren die Ergebnisse für alle bestehenden und neuen Konten.

>[!NOTE]
>
>Bei Zählern (z. B. completeCount, enrollmentCount, seatLimit und waitlistCount über 1000) sollten diese als Schätzungen und nicht als präzise Zahlen interpretiert werden, da diese aus dem Cache abgerufen werden.

### Nach Name sortieren

In der nächsten Version des Adobe-Lernmanagers werden name und -name im Sortierfeld der folgenden APIs veraltet sein:

* GET /userGroups/{userGroupId}/users
* GET /users

>[!NOTE]
>
>Bei allen vorhandenen und neuen Konten ist die Sortierung nach Name und -name veraltet.


## API-Veraltungen in der Version November 2023 von Adobe Learning Manager

### Überschreiben-Flag

In der Adobe Learning Manager-Version vom November 2023 haben wir das Überschreiben-Flag in den APIs eingestellt. Das Überschreiben-Flag ist kein Teil der öffentlichen API-Spezifikation und für Backend-Tests vorgesehen. Das Flag wird jetzt für Teilnehmer-APIs eingestellt. Das Flag ist jedoch weiterhin für Admin-APIs gültig.

Der Grund, warum wir das Flag für Teilnehmer-APIs verwerfen, ist, dass das Überschreibungsflag eine große Datenmenge über die Teilnehmer-APIs abgerufen hat.

In Zukunft wird die folgende Teilnehmer-API nicht mehr funktionieren, da sie das Überschreiben-Flag aufweist.

_/primeapi/v2/users?page[Offset]=0&amp;page[begrenzen]=10&amp;sort=id&amp;override=TRUE_

### API-Änderungen für kompetenzbasierte neue Empfehlungen

Adobe Learning Manager verbessert die Empfehlungen für Kunden- und Partnerkonten. Diese Verbesserung des Empfehlungsalgorithmus durch die Änderung des Ranglistenalgorithmus für Kurs, Lernpfad und Zertifizierung verbessert die Benutzererfahrung bei der Suche nach Inhalten.

Der Algorithmus lässt keine Empfehlungen auf Peer-Basis mehr zu. Die Änderung wirkt sich nicht auf die bestehenden Benutzer(innen) aus, aber die Option “Branchenspezifisch“ ist weiterhin vorhanden. Bei der Option “Benutzerdefiniert“ lässt Adobe-Lern-Manager keine benutzerdefinierte Peer-basierte Auswahl mehr zu.

Die Peer-Gruppe wird jetzt zu einem Konto, und die Teilnehmenden sehen eine Zeichenfolge, die die aktuellen Themen in der Gruppe anzeigt. Alle Empfehlungen sind erklärbar. Wenn Sie beispielsweise etwas zu einem Thema anzeigen, wird auf der Karte auf dem Streifen der Grund für den Kurs angezeigt.

### Änderungen am Bericht für Benachrichtigungen

In früheren Versionen des Adobe-Lernmanagers verfügte der Bericht &quot;Benachrichtigungsankündigung&quot; nicht über Filter. Adobe Learning Manager hat alle Benachrichtigungen im Konto heruntergeladen.

In der Version vom November 2023 haben wir einen Datumsfilter hinzugefügt, mit dem Sie die Benachrichtigungen innerhalb eines bestimmten Zeitraums herunterladen können.  Sie können den Bericht jedoch nur für die letzten sechs Monate herunterladen.
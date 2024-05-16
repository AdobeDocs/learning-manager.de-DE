---
title: Neue Funktionen in dieser Version
description: Erfahren Sie mehr über die neuen Funktionen und Verbesserungen in der Version November 2023 von Adobe Learning Manager.
exl-id: d670dc47-d57f-464a-bee8-064cc16e59f9
source-git-commit: eed6dd4d31a62d10a6b2901c48f14e3f4fe571d8
workflow-type: tm+mt
source-wordcount: '2373'
ht-degree: 70%

---

# Neue Funktionen in dieser Version

## Überarbeitete Benutzeroberfläche

Die Adobe Learning Manager-Benutzeroberfläche wurde einigen Aktualisierungen unterzogen, um ein saubereres und moderneres Erlebnis zu bieten. Die Landingpages für die Rollen “Administrator(in)“ und “Autor(in)“ wurden überarbeitet und die Designs der Benutzeroberfläche für alle Rollen aktualisiert. Es wurden jedoch keine Änderungen an der Position von Menüs, Schaltflächen oder Links vorgenommen, und Sie können diese genau dort finden, wo sie sich zuvor befunden haben.

Die Designaktualisierungen gelten automatisch für Konten, die das Standarddesign verwenden. Die Aktualisierungen des Designs der Benutzeroberfläche wirken sich nicht auf Konten aus, die Änderungen zur Verwendung eines benutzerdefinierten Designs vorgenommen haben. Solche Konten müssen zurück zum Standarddesign wechseln, um die neuen Designaktualisierungen zu erhalten.

![UI-Bild](assets/refreshed-ui.png)

### Über diese Änderung

**Änderungen in dieser Version**

Eine neue Vorlage in der Kopfzeile stellt automatisch Größe und Position des Logos ein, während das Seitenverhältnis des Logos beibehalten wird. Mit der Änderung soll die visuelle Attraktivität des Teilnehmererlebnisses verbessert werden.

Der Name der Organisation in der Kopfzeile wird für Teilnehmende auch automatisch auf 336 (Minimum) x 680 (Maximum) px geändert.

**Welche Größe wird für das Logo empfohlen?**

Die maximale Breite des Logos beträgt 210 px. Logos mit einer Breite von mehr als 210 px oder einer Höhe von mehr als 42 px werden auf 42 x 210 px skaliert.

Wenn die Logogröße die empfohlene Größe unterschreitet, wird das Logo unverändert hochgeladen und zentriert ausgerichtet.

**Welche Auswirkungen hat das?**

Längere Firmennamen werden zugeschnitten, und der Bereich wird mit einem Auslassungszeichen gefüllt.

**Was empfehlen wir?**

* Beim Ändern der Bildgröße wird das Seitenverhältnis beibehalten. Die empfohlene maximale Logogröße beträgt 42 px (vertikal) x 210 px (horizontal).
* Bei vielen Konten würde dies automatisch angewandt; Änderungen sind nicht erforderlich.

## Native Erweiterbarkeit

Richten Sie benutzerdefinierte Erfahrungen in der nativen Version von Adobe Learning Manager ein, sodass Sie für weniger komplizierte Fälle nicht Headless nutzen müssen. Sie können auch benutzerdefinierte Apps erstellen und sie an verschiedenen Punkten in der nativen Version der Workflows für Teilnehmende, Manager(innen), Administrator(inn)en, Autor(inn)en oder Kursleiter(inn)en platzieren.

Ein Teilnehmer kann eine benutzerdefinierte App oder eine Erweiterung verwenden, die ein Administrator erstellt hat.

Weitere Informationen finden Sie unter [Native Erweiterbarkeit](/help/migrated/administrators/feature-summary/native-extensibility.md).

## Quizerstellungswerkzeug

Sie können jetzt mit dem neuen Quizerstellungstool auf der Seite &quot;Inhaltsbibliothek&quot; Bewertungen im Learning Manager erstellen. Die erstellten Bewertungen werden Teil der Inhaltsbibliothek und können zu einem &quot;öffentlichen&quot; Ordner hinzugefügt werden, um die Wiederverwendbarkeit von Kursen zu gewährleisten.

Anzeigen [Quiz erstellen](/help/migrated/authors/feature-summary/content-library.md) Weitere Informationen.

## Berichten von Änderungen in dieser Version

### Änderungen am Registrierungsbericht für Arbeitshilfe

In früheren Versionen von Adobe Learning Manager verfügte der Bericht zur Registrierung der Arbeitshilfe nicht über Filter. Adobe Learning Manager hat alle Daten eines Kontos heruntergeladen.

In dieser Version haben wir eine Dropdown-Liste im Dialogfeld Bericht zu Arbeitshilfen hinzugefügt.

### Änderungen am Bericht zur Ankündigung von Benachrichtigungen

In früheren Versionen von Adobe Learning Manager verfügte der Bericht zur Benachrichtigungsankündigung über keine Filter. Adobe Learning Manager hat alle Benachrichtigungen im Konto heruntergeladen.

In dieser Version haben wir einen Datumsfilter hinzugefügt, mit dem Sie Benachrichtigungen innerhalb eines bestimmten Zeitraums herunterladen können.  Sie können den Bericht jedoch nur für die letzten sechs Monate herunterladen.

### Änderungen an den Kursüberprüfungsdaten im Registrierungsbericht

In dieser Version können Sie die Informationen zum erneuten Kursaufruf in einem Registrierungsbericht herunterladen, indem Sie eine Zeit angeben. Für Konten mit mehr als fünf Millionen Registrierungen ist der Downloadzeitraum auf sechs Monate begrenzt. Für alle anderen Konten beträgt der Zeitraum 15 Monate.

Sie können den Bericht von der Seite **[!UICONTROL Berichte]** > **[!UICONTROL Benutzerdefinierte Berichte]** > **[!UICONTROL Historische Berichte]** > **[!UICONTROL Kurszugriffsbericht]**.

### Änderungen am Teilnehmertranskript

In früheren Versionen von Adobe Learning Manager enthielt das Teilnehmertranskript die gelöschten Benutzer(innen), wenn ein benutzerdefinierter Administrator einen Benutzerbereich hatte. In dieser Version enthält das Teilnehmertranskript die gelöschten Benutzer(innen), wenn die/der benutzerdefinierte Administrator(in) entweder über den Benutzerbereich oder den Zugriff auf alle Benutzergruppen verfügt.

### Änderungen im Anwesenheitsbericht

Der Anwesenheitsbericht auf der Anwesenheitsseite von Kursen in der Admin-App und auf der Seite „Teilnehmer der Sitzung“ der Kursleiter-App wurde synchron heruntergeladen. In dieser Version wird dieser Bericht asynchron über eine Benachrichtigung heruntergeladen.

Weitere Informationen zu Berichten finden Sie unter [Berichte](/help/migrated/administrators/feature-summary/reports.md) in Adobe Learning Manager.

## Außerbetriebnahme des Inhalts-Marketplace

Die Kurse, die im importierten Inhalts-Marktplatzkatalog (Unternehmensschulung) abgelaufen sind, werden automatisch gelöscht, sobald sie ablaufen. Die Kurse werden eingestellt, wenn der Inhalt für die Außerbetriebnahme markiert wird. Bestehende registrierte Teilnehmende können sie innerhalb eines begrenzten Zeitraums nutzen. Danach werden sie gelöscht. Damit wird der Katalog bereinigt und Benutzer(inne)n werden keine abgelaufenen Kurse angezeigt.

## Neue kenntnisbasierte Empfehlungen

Adobe Learning Manager verbessert die Empfehlungen für Kunden- und Partnerkonten. Diese Verbesserung des Empfehlungsalgorithmus durch die Änderung des Ranglistenalgorithmus für Kurs, Lernpfad und Zertifizierung verbessert die Benutzererfahrung bei der Suche nach Inhalten.

Der Algorithmus lässt keine Empfehlungen auf Peer-Basis mehr zu. Die Änderung wirkt sich nicht auf die bestehenden Benutzer(innen) aus, aber die Option “Branchenspezifisch“ ist weiterhin vorhanden. Bei der Option “Benutzerdefiniert“ lässt Adobe-Lern-Manager keine benutzerdefinierte Peer-basierte Auswahl mehr zu.

Die Peer-Gruppe wird jetzt zu einem Konto, und die Teilnehmenden sehen eine Zeichenfolge, die die aktuellen Themen in der Gruppe anzeigt. Alle Empfehlungen sind erklärbar. Wenn Sie beispielsweise etwas zu einem Thema anzeigen, wird auf der Karte auf dem Streifen der Grund für den Kurs angezeigt.

## Verbesserungen am Arbeitsablauf für benutzerdefinierte Administrator(inn)en

Benutzerdefinierte Administrator(inn)en haben jetzt mehr Parität mit Administratorrollen in Bezug auf den Zugriff auf Berichte. Administrator(inn)en haben bessere Kontrolle beim Konfigurieren des Berichtszugriffs.

In Adobe Learning Manager stehen benutzerdefinierten Administrator(inn)en nur das Teilnehmertranskript und das Gamification-Transkript zur Verfügung. In dieser Version können benutzerdefinierte Administrator(inn)en auf alle benutzerdefinierten Berichte mit Ausnahme von xAPI- und E-Mail-Berichten zugreifen, die weiterhin nur für die/den Administrator(in) verfügbar sind. Der Zugriff auf alle Berichte hängt vom Katalog und dem Benutzerbereich ab, über den die/der benutzerdefinierte Administrator(in) verfügt. Nur wenige Berichte sind nur in vollem Umfang verfügbar. Sie sind:

<table>
    <tbody>
        <tr>
            <td>
    <p style="text-align: left;"><b>Bericht</b></p></td>
   <td>
    <p style="text-align: left;"><b>Verfügbar</b></p></td>
   <td>
    <p style="text-align: left;"><b>Umfang</b></p></td>
        </tr>
    <tr>
   <td>
    <p>Inhaltsprüfpfad</p></td>
   <td>
    <p>Ja</p></td>
   <td>
    <p>Vollständiger Katalog</p></td>
  </tr>
  <tr>
   <td>
    <p>Benutzerprüfpfad</p></td>
   <td>
    <p>Ja</p></td>
   <td>
    <p>Standardbenutzer(in)</p></td>
  </tr>
  <tr>
   <td>
    <p>Anmeldezugriff</p></td>
   <td>
    <p>Ja</p></td>
   <td>
    <p>Standardbenutzer(in)</p></td>
  </tr>
    </tbody>
</table>

**Neue schreibgeschützte Steuerelemente**

Auf der Seite &quot;Benutzerdefinierte Rollen&quot; haben wir die folgenden Schreibschutzoptionen hinzugefügt, damit Administratoren flexiblere Optionen für den benutzerdefinierten Administrator bereitstellen können: Der benutzerdefinierte Administrator verfügt jetzt über eine zusätzliche Schreibschutzberechtigung für Benutzer, E-Mail-Vorlagen und Lernpläne.

**Benutzer**:

Wenn Sie „Schreibgeschützt“ auswählen, kann die/der benutzerdefinierte Administrator(in) alle Benutzer(innen) anzeigen, aber keine Benutzerdaten bearbeiten, und ein Selbstregistrierungsportal für Benutzer(innen) erstellen.

**Lernpläne**:

Wenn Sie „Schreibgeschützt“ wählen, kann ein(e) benutzerdefinierte(r) Administrator(in) keinen Lernplan hinzufügen oder bearbeiten. Sie/er kann einen Lernplanbericht herunterladen und seine Details anzeigen. Aber sie/er kann die Kursdetails nicht ändern.

>[!NOTE]
>
>Lernpläne sind zusätzlich schreibgeschützt und bieten vollständige Kontrolle.

**E-Mail-Vorlagen**

Wenn Sie „Schreibgeschützt“ wählen, kann ein(e) benutzerdefinierte(r) Administrator(in) die E-Mail-Vorlagen anzeigen. Sie/er kann E-Mail-Vorlageneinstellungen nicht aktivieren oder deaktivieren, aber E-Mail-Zugriffsberichte herunterladen.

### Teilnehmertranskripte

Wenn die Benutzerberechtigung oder die Benutzergruppe &quot;Alle&quot; ausgewählt ist und der benutzerdefinierte Administrator versucht, Teilnehmertranskripte herunterzuladen, gibt die Option &quot;Gelöschte Teilnehmer einschließen&quot; alle gelöschten Teilnehmer im Bericht zurück.

### Berichte

Ein benutzerdefinierter Administrator kann entsprechend dem definierten Umfang auf die folgenden Berichte zugreifen:

<table>
    <tbody>
        <tr>
            <td>
    <p style="text-align: left;"><b>Bericht</b></p></td>
   <td>
    <p style="text-align: left;"><b>Verfügbar</b></p></td>
   <td>
    <p style="text-align: left;"><b>Umfang</b></p></td>
        </tr>
    <tr>
   <td>
    <p>Inhaltsprüfpfad</p></td>
   <td>
    <p>Ja</p></td>
   <td>
    <p>Vollständiger Katalog</p></td>
  </tr>
  <tr>
   <td>
    <p>Benutzerprüfpfad</p></td>
   <td>
    <p>Ja</p></td>
   <td>
    <p>Standardbenutzer(in)</p></td>
  </tr>
  <tr>
   <td>
    <p>Anmeldezugriff</p></td>
   <td>
    <p>Ja</p></td>
   <td>
    <p>Standardbenutzer(in)</p></td>
  </tr>
    </tbody>
</table>

<!--| Report | Available | Scope |
|--- |--- |
| Content Audit Trail | Yes | Full Catalog |
| User Audit Trail | Yes | Full User |
|Login Access | Yes | Full User |-->

## Verbesserte Connect-Integration

Kursleiter(innen) können ihre Sitzungserfahrung personalisieren, indem sie besondere Räume für Kursleiter(innen) auswählen. In dieser Version haben wir die folgenden Verbesserungen vorgenommen:

### Importieren von Transkripten

Sie können Sitzungstranskripte aus Connect importieren und die Transkripte analysieren. Teilnehmende erhalten nach der Aufzeichnung das Transkript, das sie später herunterladen können.

### Bearbeiten von Videos

Kursleiter können das Video bearbeiten und das Anwendererlebnis der Teilnehmer verbessern. Kursleiter(innen) sehen einen Link auf der Seite &quot;Sitzungsübersicht&quot;, über den sie zur Anmeldeseite von Adobe Connect gelangen. Nach der Anmeldung wird der/dem Kursleiter(in) der Aufzeichnungslink angezeigt. Wenn sie auf den Link klicken, werden sie zum Video weitergeleitet, das sie zuschneiden können.

## Dashboard-Berichte auf Benutzer mit Managerrolle beschränken

Administratoren können in Dashboard-Berichten nur nach Managern suchen.

## Beschränken veralteter Dashboard-Berichtsverarbeitung

Wenn ein Administrator versucht, einen Dashboard-Bericht zu zeichnen, und der Bericht zu lange dauert (mehr als 2,5 Minuten), zeigt Adobe Learning Manager die folgende Meldung an:

![Veraltetes Berichtsbild](assets/error-message.png)
*Fehlermeldung, wenn der Bericht zu lange dauert*

Berichte dieser Größenordnung können nicht auf der Benutzeroberfläche angezeigt werden, aber die/der Administrator(in) kann sie herunterladen.

## Migrationsunterstützung für Katalogbeschriftungen

Der Migrationsarbeitsablauf unterstützt jetzt Katalogbeschriftungen. Migrations-CSVs können verwendet werden, um Katalogbeschriftungs-Schlüssel und Katalogbeschriftungs-Werte zu importieren und sie Kursen, Lernpfaden, Zertifizierungen und Arbeitshilfen anzuhängen. Falls erforderlich, können mit dem Arbeitsablauf auch falsche Werte und Schlüssel gelöscht werden.

## API-Verbesserungen für die komplexe Kursfilterung

Erweiterte Filterung von Kursen nach Tags und Katalogbeschriftungen (mit einer Kombination aus &quot;UND&quot;- und &quot;ODER&quot;-Bedingungen) ist jetzt über Lern-Manager-APIs möglich.

## API-Änderungen in dieser Version

### Validierung in der Job-API

Wenn in dieser Version der Bericht zu Arbeitshilfen 10 Millionen überschreitet, die mithilfe der Job-API generiert wurden, erhält die Antwort die Meldung &quot;Der angeforderte Bericht enthält zu viele Daten, die generiert werden müssen, und Sie sollten die Filter für Arbeitshilfen anwenden!&quot;.

### Benachrichtigung über einen gelöschten Beitrag

Wenn in früheren Versionen von Adobe Learning Manager ein Kurs, eine Zertifizierung oder ein Lernplan gelöscht wurde und die entsprechende Benachrichtigung vorhanden ist, können Sie weiterhin auf den Kurs, die Zertifizierung oder den Lernplan zugreifen, indem Sie die entsprechende Benachrichtigung aufrufen.

In dieser Version stellen wir sicher, dass nicht mehr auf einen gelöschten Beitrag zugegriffen werden kann. Wenn Sie die ID in der Datei /posts/{id} API verfügbar ist und die ID für den Beitrag nicht mehr verfügbar ist, zeigt die API die Meldung &quot;Beitrag für die angegebene Ressource nicht gefunden&quot; an.

### Teilnehmer-API-Abschlussfrist

In früheren Versionen rief Adobe Learning Manager die Frist aus der Registrierungstabelle ab. In dieser Version berechnet Adobe Learning Manager die Frist aus der Kursinstanztabelle. Wenn die nicht verfügbar ist, wird auf die Registrierungstabelle zurückgegriffen.

### Überschreiben-Flag

In der November 2023-Version von Adobe Learning Manager stellen wir das Überschreiben-Flag in den APIs ein. Das Überschreiben-Flag ist kein Teil der öffentlichen API-Spezifikation und für Backend-Tests vorgesehen. Das Flag wird jetzt für Teilnehmer-APIs eingestellt. Das Flag ist jedoch weiterhin für Admin-APIs gültig.

Der Grund, warum wir das Flag für Teilnehmer-APIs verwerfen, ist, dass das Überschreibungsflag eine große Datenmenge über die Teilnehmer-APIs abgerufen hat.

In Zukunft wird die folgende Teilnehmer-API nicht mehr funktionieren, da sie das Überschreiben-Flag aufweist.

`https://captivateprime.adobe.com/primeapi/v2/users?page[offset]=0&page[limit]=10&sort=id&override=TRUE`

### Hervorheben von Ergebnissen

In der kommenden Version von Adobe Learning Manager beispielsweise in der API &quot;/search&quot; ändern wir den Standardwert für highlightResults in &quot;false&quot;.

Außerdem ändern wir die Standardeinstellung von &quot;snippetTypes&quot; in &quot;courseName&quot;. Dadurch werden die Kursnamen in der Suche nur hervorgehoben, wenn highlightResults auf True festgelegt ist.

### Neuer Ressourcentyp für Quiz

Die `instances.loResources.resources` Endpunkt wird zurückgegeben `ResourceContentType` mit Quiz.

## Hinweis zum Verwerfen

Am 30. November 2023 stellt LinkedIn Learning die Verwendung der HTTP-GET-Methode zum Abrufen eines OAuth-Tokens ein. Nach der Deaktivierung können Sie nur noch ein OAuth-Token mit der HTTP-POST generieren.
Adobe Learning Manager wird BlueJeans im Februar 2024 einstellen. Alle neuen Konten nach Februar 2024 werden den BlueJeans-Connector nicht enthalten.

## Versionshinweise

Weitere Informationen zu aktuellen und früheren Versionen der Learning Manager-Webanwendung und -Geräte-App finden Sie unter [Versionshinweise](release-note/release-notes.md).

## In dieser Version behobene Fehler

* Eine Miniaturansicht für einen Kurs, die eine Voraussetzung für einen Lernpfad oder einen anderen Kurs ist, wird nicht angezeigt, wenn ein(e) Teilnehmer(in) die Vorschauseite des Lernpfads oder Kurses öffnet.
* Wenn die Optionen „Kalender“, „Gamification“ und „Soziales Lernen“ nicht ausgewählt sind, wird die nächste Einstellung in der Teilnehmenden-Dashboard-Einstellung nicht beibehalten. Optionen wie “Empfohlen“ in Ihren Interessenbereichen und „Nach Katalog durchsuchen“ werden nicht als ausgewählt angezeigt, aber in der Vorschau angezeigt.
* Auch nachdem ein Teilnehmer einen VC-Kurs abgeschlossen hat, erhält er eine Erinnerungs-E-Mail, um den Kurs abzuschließen.
* Für Peer-Konten können Sie keine Dashboard-Berichte herunterladen.
* Das Löschen und Hinzufügen eines Checklistenmoduls in einem Kurs führt zu einem internen Fehler.
* Bei Vorlagen für Sitzungseinladungen enthält die E-Mail-ID des Absenders den Text captivatePrime anstelle von AdobeLearningManager.
* Wenn Sie für die Kurseffektivität die sekundäre Y-Achse verwenden, tritt beim Berichtsdownload mit einer Nullzeigerausnahme ein Fehler auf.
* Wenn Teilnehmenden eine benutzerdefinierte Administratorrolle zugewiesen ist, navigieren sie standardmäßig zum Profil “Benutzerdefinierter Administrator“. Wenn jedoch für das Konto eine Teilnehmenden-Weiterleitungs-URL festgelegt ist, wird die/der benutzerdefinierte Administrator(in) zu einem anderen Ziel geleitet und nicht zum Profil der benutzerdefinierten Administratorrolle.
* Der Gamification-Bereich funktioniert nicht wie erwartet, wenn disabled_sub_groups auf eine große Anzahl festgelegt ist.
* In einigen Fällen lösen gelöschte Benutzer eine Migration aus.
* Teilnehmende können keine LinkedIn-Kurse in der MS Teams-App abspielen.
* Die Registrierungs-API gibt die Registrierungen für einen Flex-Lernplan oder einen eingebetteten Lernplan nicht wie erwartet zurück.
* In der mobilen App werden die Namen eines Kurses, einer Zertifizierung oder eines Lernplans in Kleinbuchstaben angezeigt.
* Wenn in früheren Versionen von Adobe Learning Manager ein Kurs, eine Zertifizierung oder ein Lernplan gelöscht wurde und die entsprechende Benachrichtigung vorhanden ist, können Sie weiterhin auf den Kurs, die Zertifizierung oder den Lernplan zugreifen, indem Sie die entsprechende Benachrichtigung aufrufen. In dieser Version stellen wir sicher, dass nicht mehr auf einen gelöschten Beitrag zugegriffen werden kann. Wenn Sie die ID in der Datei /posts/{id} API verfügbar ist und die ID für den Beitrag nicht mehr verfügbar ist, zeigt die API die Meldung &quot;Beitrag für die angegebene Ressource nicht gefunden&quot; an.
* In der Teilnehmer-API wird das Abschlussfristfeld nicht in der Antwort der Registrierungs-API angezeigt.
* In der API zum Abrufen der Registrierung für Teilnehmende werden die Registrierungsdetails angezeigt, selbst wenn Sie eine falsche Instanz-ID angegeben haben.

## Bekannte Probleme in dieser Version

* Bei einer neuen Registrierung oder Aktualisierung einer Registrierung tritt ein Fehler auf, wenn sich ein Flex-Lernplan in einem anderen Flex-Lernplan befindet.
* Die Transkript-URL zeigt die Sitzungsaufzeichnungen in Adobe Connect-Sitzungen nicht an.
* Teilnehmende können ein Offline-Quiz in der mobilen App absolvieren, und es macht nichts aus, wenn sie nicht bestehen.

## Systemanforderungen

[Systemanforderungen für Learning Manager](system-requirements.md)

## Frühere Versionen von Adobe Learning Manager

* [Version Juli 2023](whats-new-2023-july.md)
* [Version April 2023](whats-new-2023-april.md)
* [Version November 2022](whats-new-2022-november.md)
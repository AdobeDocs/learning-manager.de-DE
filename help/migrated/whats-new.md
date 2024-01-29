---
title: Neue Funktionen in dieser Version
description: Erfahren Sie mehr über die neuen Funktionen und Verbesserungen im Adobe-Lernmanager
source-git-commit: 95ab7a13a7f3e9815785134bc1d1675c002ab64b
workflow-type: tm+mt
source-wordcount: '2372'
ht-degree: 0%

---

# Neue Funktionen in dieser Version

## Überarbeitete Benutzeroberfläche

Die Benutzeroberfläche des Adobe Learning Manager wurde einigen Aktualisierungen unterzogen, um ein saubereres und moderneres Erlebnis zu bieten. Die Zielseiten für die Rollen &quot;Administrator&quot; und &quot;Autor&quot; wurden überarbeitet und die Designs der Benutzeroberfläche wurden für alle Rollen aktualisiert. Es wurden jedoch keine Änderungen an der Position von Menüs, Schaltflächen oder Links vorgenommen, und Sie können diese genau dort finden, wo sie sich zuvor befunden haben.

Die Designaktualisierungen gelten automatisch für Konten, die das Standarddesign verwenden. Die Aktualisierungen des UI-Designs wirken sich nicht auf Konten aus, die Änderungen zur Verwendung eines benutzerdefinierten Designs vorgenommen haben. Solche Konten müssen zurück zum Standarddesign wechseln, um die neuen Designaktualisierungen zu erhalten.

![UI-Bild](assets/refreshed-ui.png)

*Überarbeitete Benutzeroberfläche von Adobe Learning Manager*

### Über diese Änderung

**Welche Änderungen gibt es in dieser Version?**

Es gibt eine neue Vorlage in der Kopfzeile, die die Größe des Logos automatisch auf eine feste Größe und Position anpasst, während das Seitenverhältnis des Logos beibehalten wird. Mit der Änderung soll die visuelle Attraktivität des Lernerlebnisses verbessert werden.

Der Name der Organisation in der Kopfzeile wird für Teilnehmer auch automatisch auf 336 (Minimum) x 680 (Maximum) px geändert.

**Welche Größe wird für das Logo empfohlen?**

Die maximale Breite des Logos beträgt 210 px. Logos mit einer Breite von mehr als 210 px oder einer Höhe von mehr als 42 px werden auf 42 x 210 px skaliert.

Wenn die Logogröße kleiner als die empfohlene Größe ist, wird das Logo unverändert hochgeladen und zentriert ausgerichtet.

**Welche Auswirkungen hat das?**

Längere Firmennamen werden zugeschnitten, und der Bereich wird mit einem Auslassungszeichen gefüllt.

**Was empfehlen wir?**

* Ändere die Bildgröße, ohne das Seitenverhältnis zu ändern. Die empfohlene maximale Logogröße beträgt 42 px (vertikal) x 210 px (horizontal).
* Bei vielen Konten würde dies automatisch gelten; Änderungen sind nicht erforderlich.

## Native Erweiterbarkeit.

Richten Sie benutzerdefinierte Erlebnisse in der nativen Version von Adobe Learning Manager ein, sodass Sie Headless nicht für weniger komplizierte Fälle verwenden können. Sie können auch benutzerdefinierte Apps erstellen und sie an verschiedenen Punkten in der nativen Version der Workflows für Teilnehmer, Manager, Administrator, Autor oder Kursleiter platzieren.

Ein Teilnehmer kann eine benutzerdefinierte App oder eine Erweiterung verwenden, die ein Administrator erstellt hat.

Anzeigen [Native Erweiterbarkeit.](/help/migrated/administrators/feature-summary/native-extensibility.md) Weitere Informationen.

## Quizerstellungswerkzeug

Sie können jetzt mit dem neuen Quizerstellungstool auf der Seite &quot;Inhaltsbibliothek&quot; Bewertungen im Learning Manager erstellen. Die erstellten Bewertungen werden Teil der Inhaltsbibliothek und können zu einem &quot;öffentlichen&quot; Ordner hinzugefügt werden, um die Wiederverwendbarkeit von Kursen zu gewährleisten.

Anzeigen [Quiz erstellen](/help/migrated/authors/feature-summary/content-library.md) Weitere Informationen.

## Berichte zu Änderungen in dieser Version erstellen

### Änderungen am Registrierungsbericht für Arbeitshilfe

In früheren Versionen des Adobe-Lernmanagers verfügte der Bericht zur Registrierung der Arbeitshilfe über keine Filter. Adobe Learning Manager hat alle Daten eines Kontos heruntergeladen.

In dieser Version haben wir eine Dropdown-Liste im Dialogfeld Bericht zu Arbeitshilfen hinzugefügt.

### Änderungen am Bericht zur Ankündigung von Benachrichtigungen

In früheren Versionen des Adobe-Lernmanagers verfügte der Bericht &quot;Benachrichtigungsankündigung&quot; nicht über Filter. Adobe Learning Manager hat alle Benachrichtigungen im Konto heruntergeladen.

In dieser Version haben wir einen Datumsfilter hinzugefügt, mit dem Sie Benachrichtigungen innerhalb eines bestimmten Zeitraums herunterladen können.  Sie können den Bericht jedoch nur für die letzten sechs Monate herunterladen.

### Änderungen an den Kursüberprüfungsdaten im Registrierungsbericht

In dieser Version können Sie die Kursbesuchsinformationen in einem Registrierungsbericht herunterladen, indem Sie eine Zeit angeben. Für Konten mit mehr als fünf Millionen Registrierungen ist der Downloadzeitraum auf sechs Monate begrenzt. Für alle anderen Konten beträgt der Zeitraum 15 Monate.

Sie können den Bericht von der Seite **[!UICONTROL Berichte]** > **[!UICONTROL Benutzerdefinierte Berichte]** > **[!UICONTROL Historische Berichte]** > **[!UICONTROL Kurszugriffsbericht]**.

### Änderungen am Teilnehmertranskript

In früheren Versionen des Adobe-Lernmanagers enthielt das Teilnehmertranskript die gelöschten Benutzer, wenn ein benutzerdefinierter Administrator einen Benutzerbereich hatte. In dieser Version enthält das Teilnehmertranskript die gelöschten Benutzer, wenn der benutzerdefinierte Administrator entweder über den Benutzerbereich oder den Zugriff auf alle Benutzergruppen verfügt.

### Änderungen im Anwesenheitsbericht

Der Anwesenheitsbericht auf der Anwesenheitsseite von Kursen in der Admin-App und auf der Seite der Sitzungsteilnehmer der Kursleiter-App wurde synchron heruntergeladen. In dieser Version wird dieser Bericht asynchron über eine Benachrichtigung heruntergeladen.

Weitere Informationen zu Berichten finden Sie unter [Berichte](/help/migrated/administrators/feature-summary/reports.md) im Adobe-Lernmanager.

## Außerbetriebnahme des Content Marketplace

Die Kurse, die im importierten Inhalts-Marktplatzkatalog (Unternehmensschulung) abgelaufen sind, werden automatisch gelöscht, sobald sie ablaufen. Die Kurse werden eingestellt, um eingestellt zu werden, wenn der Inhalt für die Stilllegung markiert wird. Bestehende registrierte Teilnehmer können sie innerhalb eines begrenzten Zeitraums nutzen. Danach werden sie gelöscht. Dadurch bleibt der Katalog sauber und es werden den Benutzern keine abgelaufenen Kurse angezeigt.

## Neue kompetenzbasierte Empfehlungen

Adobe Learning Manager verbessert die Empfehlungen für Kunden- und Partnerkonten. Diese Verbesserung des Empfehlungsalgorithmus durch die Änderung des Einstufungsalgorithmus für den Kurs, den Lernpfad und die Zertifizierung verbessert die Benutzererfahrung bei der Suche nach Inhalten.

Der Algorithmus lässt keine Peer-basierten Empfehlungen mehr zu. Die Änderung wirkt sich nicht auf die vorhandenen Benutzer aus, aber die Option &quot;Branchenspezifisch&quot; ist weiterhin vorhanden. Bei der Option &quot;Benutzerdefiniert&quot; lässt der Adobe-Lern-Manager eine benutzerdefinierte Peer-basierte Auswahl nicht mehr zu.

Die Peer-Gruppe wird jetzt zu einem Konto, und die Teilnehmer sehen eine Zeichenfolge, die die aktuellen Themen in der Gruppe anzeigt. Alle Empfehlungen sind erklärbar. Wenn Sie beispielsweise etwas zu einem Thema anzeigen, wird auf der Karte auf dem Streifen der Grund für den Kurs angezeigt.

## Verbesserungen am Arbeitsablauf für benutzerdefinierte Administratoren

Benutzerdefinierte Administratoren haben jetzt mehr Parität mit Administratorrollen in Bezug auf den Zugriff auf Berichte. Administratoren können den Berichtszugriff mit besserer Kontrolle konfigurieren.

Im Adobe-Lern-Manager stehen einem benutzerdefinierten Administrator nur das Lernaktranskript und das Gamification-Transkript zur Verfügung. In dieser Version kann ein benutzerdefinierter Administrator auf alle benutzerdefinierten Berichte mit Ausnahme von xAPI- und E-Mail-Berichten zugreifen, die weiterhin nur für den Administrator verfügbar sind. Der Zugriff auf alle Berichte hängt vom Katalog und dem Benutzerbereich ab, über den der benutzerdefinierte Administrator verfügt. Es gibt nur wenige Berichte, die nur in vollem Umfang verfügbar sind. Sie sind:

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
    <p>Vollbenutzer</p></td>
  </tr>
  <tr>
   <td>
    <p>Anmeldezugriff</p></td>
   <td>
    <p>Ja</p></td>
   <td>
    <p>Vollbenutzer</p></td>
  </tr>
    </tbody>
</table>

**Neue schreibgeschützte Steuerelemente**

Auf der Seite &quot;Benutzerdefinierte Rollen&quot; haben wir die folgenden Schreibschutzoptionen hinzugefügt, damit Administratoren flexiblere Optionen für den benutzerdefinierten Administrator bereitstellen können: Der benutzerdefinierte Administrator verfügt jetzt über eine zusätzliche Schreibschutzberechtigung für Benutzer, E-Mail-Vorlagen und Lernpläne.

**Benutzer**:

Wenn Sie Schreibgeschützt auswählen, kann der benutzerdefinierte Administrator alle Benutzer anzeigen, aber keine Benutzerdaten bearbeiten und ein Selbstregistrierungsportal für Benutzer erstellen.

**Lernpläne**:

Wenn Sie Schreibgeschützt wählen, kann ein benutzerdefinierter Administrator keinen Lernplan hinzufügen oder bearbeiten. Sie können einen Lernplanbericht herunterladen und seine Details anzeigen. Aber sie können die Kursdetails nicht ändern.

>[!NOTE]
>
>Lernpläne sind zusätzlich schreibgeschützt und bieten vollständige Kontrolle.

**E-Mail-Vorlagen**

Wenn Sie Schreibgeschützt auswählen, kann ein benutzerdefinierter Administrator die E-Mail-Vorlagen anzeigen. E-Mail-Vorlageneinstellungen können nicht aktiviert oder deaktiviert werden, aber E-Mail-Zugriffsberichte können heruntergeladen werden.

### Teilnehmertranskripte

Wenn die Benutzerberechtigung oder die Benutzergruppe &quot;Alle&quot; ausgewählt ist und der benutzerdefinierte Administrator versucht, Teilnehmertranskripte herunterzuladen, gibt die Option &quot;Gelöschte Teilnehmer einschließen&quot; alle gelöschten Teilnehmer im Bericht zurück.

### Berichte

Ein benutzerdefinierter Administrator kann entsprechend dem definierten Umfang auf die folgenden Berichte zugreifen:

| Bericht | Verfügbar | Umfang |
|--- |--- |
| Inhaltsprüfpfad | Ja | Vollständiger Katalog |
| Benutzerprüfpfad | Ja | Vollbenutzer |
| Anmeldezugriff | Ja | Vollbenutzer |

## Verbesserte Connect-Integration

Kursleiter können ihre Sitzungserfahrung personalisieren, indem sie lehrerspezifische Räume auswählen. In dieser Version haben wir die folgenden Verbesserungen vorgenommen:

### Transkripte importieren

Sie können Sitzungstranskripte aus Connect importieren und die Transkripte analysieren. Teilnehmer erhalten das Transkript nach der Aufzeichnung, das sie später herunterladen können.

### Bearbeiten von Videos

Kursleiter können das Video bearbeiten und das Anwendererlebnis der Teilnehmer verbessern. Kursleiter sehen einen Link auf der Seite &quot;Sitzungsübersicht&quot;, über den sie zur Anmeldeseite von Adobe Connect gelangen. Nach der Anmeldung wird dem Kursleiter der Aufzeichnungslink angezeigt. Wenn sie auf den Link klicken, werden sie zum Video weitergeleitet, wo sie zugeschnitten werden können.

## Dashboard-Berichte auf Benutzer mit Managerrolle beschränken

Administratoren können in Dashboard-Berichten nur nach Managern suchen.

## Veraltete Dashboard-Berichtsverarbeitung einschränken

Wenn ein Administrator versucht, einen Dashboard-Bericht zu zeichnen, und der Bericht zu lange dauert (mehr als 2,5 Minuten), zeigt Adobe Learning Manager die folgende Meldung an:

![Veraltetes Berichtsbild](assets/error-message.png)
*Fehlermeldung, wenn der Bericht zu lange dauert*

Berichte dieser Größenordnung können nicht auf der Benutzeroberfläche angezeigt werden, aber der Administrator kann sie herunterladen.

## Migrationsunterstützung für Katalogbeschriftungen

Der Migrationsarbeitsablauf unterstützt jetzt Katalogbeschriftungen. Migrations-CSVs können verwendet werden, um Katalogbeschriftungsschlüssel und Katalogbeschriftungswerte zu importieren und sie an Kurse, Lernpfade, Zertifizierungen und Arbeitshilfen anzuhängen. Der Workflow kann auch verwendet werden, um falsche Werte und Schlüssel zu löschen, falls erforderlich.

## API-Verbesserungen für die komplexe Kursfilterung

Erweiterte Filterung von Kursen nach Tags und Katalogbeschriftungen (mit einer Kombination aus &quot;UND&quot;- und &quot;ODER&quot;-Bedingungen) ist jetzt über Lern-Manager-APIs möglich.

## API-Änderungen in dieser Version

### Validierung in der Job-API

Wenn in dieser Version der Bericht zu Arbeitshilfen 10 Millionen überschreitet, die mithilfe der Job-API generiert wurden, erhält die Antwort die Meldung &quot;Der angeforderte Bericht enthält zu viele Daten, die generiert werden müssen, und Sie sollten die Filter für Arbeitshilfen anwenden!&quot;.

### Benachrichtigung über einen gelöschten Beitrag

Wenn in früheren Versionen von Adobe Learning Manager ein Kurs, eine Zertifizierung oder ein Lernplan gelöscht wurde und die entsprechende Benachrichtigung vorhanden ist, können Sie weiterhin auf den Kurs, die Zertifizierung oder den Lernplan zugreifen, indem Sie die entsprechende Benachrichtigung besuchen.

In dieser Version stellen wir sicher, dass nicht mehr auf einen gelöschten Beitrag zugegriffen werden kann. Wenn Sie die ID in der Datei /posts/{id} API verfügbar ist und die ID für den Beitrag nicht mehr verfügbar ist, zeigt die API die Meldung &quot;Beitrag für die angegebene Ressource nicht gefunden&quot; an.

### Frist für API-Abschluss für Teilnehmer

In früheren Versionen holte Adobe Learning Manager den Abgabetermin aus der Registrierungstabelle. In dieser Version berechnet der Adobe Learning Manager den Fristablauf aus der Kursinstanztabelle. Wenn der Termin nicht verfügbar ist, wird er auf die Registrierungstabelle zurückgesetzt.

### Kennzeichen überschreiben

In der Adobe Learning Manager-Version vom November 2023 stellen wir das Überschreiben-Flag in den APIs ein. Das override-Flag ist nicht Teil der öffentlichen API-Spezifikation und ist für Backend-Tests vorgesehen. Das Flag wird jetzt für Teilnehmer-APIs eingestellt. Das Flag ist jedoch weiterhin für Admin-APIs gültig.

Der Grund, warum wir das Flag für Teilnehmer-APIs verwerfen, ist, dass das Überschreibungsflag eine große Datenmenge über die Teilnehmer-APIs abgerufen hat.

In Zukunft wird die folgende Teilnehmer-API nicht mehr funktionieren, da sie das Überschreibungs-Flag aufweist.

`https://captivateprime.adobe.com/primeapi/v2/users?page[offset]=0&page[limit]=10&sort=id&override=TRUE`

### Ergebnisse hervorheben

In der kommenden Version von Adobe Learning Manager, beispielsweise in der API &quot;/search&quot;, ändern wir den Standardwert für highlightResults in &quot;false&quot;.

Außerdem ändern wir die Standardeinstellung von &quot;snippetTypes&quot; in &quot;courseName&quot;. Dadurch werden die Kursnamen in der Suche nur hervorgehoben, wenn highlightResults auf True festgelegt ist.

### Neuer Ressourcentyp für Quiz

Die `instances.loResources.resources` Endpunkt wird zurückgegeben `ResourceContentType` mit Quiz.

## Hinweis zur Aufhebung

Am 30. November 2023 stellt LinkedIn Learning die Verwendung der HTTP-GET-Methode zum Abrufen eines OAuth-Tokens ein. Nach der Deaktivierung können Sie nur noch ein OAuth-Token mit der HTTP-POST generieren.
Adobe Learning Manager wird BlueJeans im Februar 2024 einstellen. Alle neuen Konten nach Februar 2024 enthalten nicht den BlueJeans-Connector.

## Versionshinweise

Weitere Informationen zu aktuellen und früheren Versionen der Learning Manager-Webanwendung und -Geräte-App finden Sie unter [Versionshinweise](release-note/release-notes.md).

## In dieser Version behobene Fehler

* Eine Miniaturansicht für einen Kurs, die eine Voraussetzung für einen Lernpfad oder einen anderen Kurs ist, wird nicht angezeigt, wenn ein Teilnehmer die Vorschauseite des Lernpfads oder des Kurses öffnet.
* Wenn die Optionen Kalender, Gamification und Soziales Lernen nicht ausgewählt sind, wird die nächste Einstellung in der Teilnehmer-Dashboard-Einstellung nicht beibehalten. Optionen wie &quot;Empfohlen&quot; in den Interessenbereichen und &quot;Nach Katalog durchsuchen&quot; werden nicht als ausgewählt angezeigt, sondern in der Vorschau angezeigt.
* Auch nachdem ein Teilnehmer einen VC-Kurs abgeschlossen hat, erhält er eine Erinnerungs-E-Mail, um den Kurs abzuschließen.
* Bei Peer-Konten können Sie keine Dashboard-Berichte herunterladen.
* Das Löschen und Hinzufügen eines Checklistenmoduls in einem Kurs führt zu einem internen Fehler.
* Bei Vorlagen für Sitzungseinladungen enthält die E-Mail-ID des Absenders den Text captivatePrime anstelle von AdobeLearningManager.
* Wenn Sie die Kurseffektivität als sekundäre Y-Achse verwenden, schlägt der Berichtsdownload mit einer Nullzeigerausnahme fehl.
* Wenn einem Teilnehmer eine benutzerdefinierte Administratorrolle zugewiesen ist, navigieren er standardmäßig zum Profil &quot;Benutzerdefinierter Administrator&quot;. Wenn jedoch für das Konto eine Teilnehmerumleitungs-URL festgelegt ist, wird der benutzerdefinierte Administrator zu einem anderen Ziel geleitet und nicht zum Profil der benutzerdefinierten Administratorrolle.
* Der Gamification-Bereich funktioniert nicht wie erwartet, wenn disabled_sub_groups auf eine große Anzahl festgelegt ist.
* In einigen Fällen lösen gelöschte Benutzer eine Migration aus.
* Ein Teilnehmer kann keine LinkedIn-Kurse in der MS Teams-App abspielen.
* Die Registrierungs-API gibt die Registrierungen für einen Flex-Lernplan oder einen eingebetteten Lernplan nicht wie erwartet zurück.
* In der mobilen App werden die Namen eines Kurses, einer Zertifizierung oder eines Lernplans in Kleinbuchstaben angezeigt.
* Wenn in früheren Versionen von Adobe Learning Manager ein Kurs, eine Zertifizierung oder ein Lernplan gelöscht wurde und die entsprechende Benachrichtigung vorhanden ist, können Sie weiterhin auf den Kurs, die Zertifizierung oder den Lernplan zugreifen, indem Sie die entsprechende Benachrichtigung besuchen. In dieser Version stellen wir sicher, dass nicht mehr auf einen gelöschten Beitrag zugegriffen werden kann. Wenn Sie die ID in der Datei /posts/{id} API verfügbar ist und die ID für den Beitrag nicht mehr verfügbar ist, zeigt die API die Meldung &quot;Beitrag für die angegebene Ressource nicht gefunden&quot; an.
* In der Teilnehmer-API wird das Feld &quot;Abschlussdatum&quot; nicht in der Antwort der Registrierungs-API angezeigt.
* In der &quot;Get Enrollment API for Learners&quot; (Registrierungs-API für Teilnehmer abrufen) werden die Registrierungsdetails angezeigt, selbst wenn Sie eine falsche Instanz-ID angegeben haben.

## Bekannte Probleme in dieser Version

* Eine neue Registrierung oder Aktualisierung einer Registrierung schlägt fehl, wenn sich ein Flex-Lernplan in einem anderen Flex-Lernplan befindet.
* Die Transkript-URL zeigt die Sitzungsaufzeichnungen in Adobe Connect-Sitzungen nicht an.
* Ein Teilnehmer kann ein Offline-Quiz in der mobilen App absolvieren, auch wenn er es nicht besteht.

## Systemanforderungen

[Systemanforderungen für Learning Manager](system-requirements.md)

## Frühere Versionen von Adobe Learning Manager

<!--* [November 2023 release](whats-new-november-2023.md)-->
* [Version Juli 2023](whats-new-2023-july.md)
* [Version April 2023](whats-new-2023-april.md)

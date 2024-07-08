---
description: Weitere Informationen zu den neuen Funktionen und Verbesserungen im März 2024 release von Adobe Learning Manager
jcr-language: en_us
title: Zusammenfassung der neuen Funktionen
contentowner: jayakarr
exl-id: 603f1f1c-bf8d-4807-b9f7-b10ded19a91e
source-git-commit: c833d92533b7fbf5a87c980d8b5e088185d02ef5
workflow-type: tm+mt
source-wordcount: '3903'
ht-degree: 1%

---

# Zusammenfassung der neuen Funktionen {#new-features-summary}

Erfahrt mehr über die neuen Funktionen und Verbesserungen im März 2024 Release von Adobe Learning Manager.

Entdeckt einige der neuesten Funktionen von Adobe Learning Manager, z. B.:

1. Skills aus externen Quellen importieren
1. Unterstützung mehrerer Branding-Elemente
1. Modul zur Überprüfung der Checkliste für Aktivitäten
1. White-Label-App für Mobile Learning

>[!NOTE]
>
>In diesem [Webinar](https://learningmanager.adobe.com/app/learner?accountId=98632#/course/9212121) erfährst du mehr über die neuen Funktionen in dieser Version.


## Neue Funktionen in dieser Version {#whatsnewandchanged}

### Skills aus externen Quellen importieren

Importiere Skills von Content-Anbietern wie LinkedIn und Go1 mithilfe der jeweiligen Connectoren. Diese Verbesserung ist teil des Ziels, dass Learning Manager mit externen Skills Cloud- und Talent-Management-Systemen integriert werden kann. Die importierten Skills werden zu den admindefinierten Kompetenzen in Learning Manager hinzugefügt und stehen Autoren während des Workflows zur Kurserstellung zur Verfügung. Außerdem wurden die Funktionen für die Kompetenzsuche auf der plattformübergreifenden Plattform verbessert, um ein besseres Sucherlebnis zu bieten, wenn das Konto über umfangreiche Kenntnisse verfügt.

Mehr erfahren: Import-Skills[](administrators/feature-summary/import-skills-external-sources.md).

### Benutzerdefiniertes Branding

Sie können nun bestimmte UI-Elemente – Den Namen der Organisation, das Logo und das UI-Thema – basierend auf den im Konto verfügbaren Benutzergruppen anpassen. Ein Unternehmen mit mehreren Abteilungen kann beispielsweise ein benutzerdefiniertes Logo und ein BENUTZEROBERFLÄCHE-Thema einrichten, das für jede Abteilung angezeigt wird.

>[!NOTE]
>
>Diese Mehrfach-Branding-Funktion gilt nicht für die Ansicht des Administrators. Sie werden immer ein Branding auf Org-Ebene in ihrem Konto sehen. Dies liegt daran, dass dies eine Funktion für Teilnehmer ist, und Administratoren möchten dies möglicherweise nicht in ihrem Konto.

Weitere [Informationen findest du in mehreren branding-Funktionen](administrators/feature-summary/themes.md#multiple-branding) .


## Änderungen für Konten mit großem Anwenderstamm

### Seiten mit Kurs- oder Lernpfad für Administratoren

Wenn eine große Anzahl von Teilnehmern für den Kurs angemeldet ist, z. B. mehr als 50.000, wird die Liste der Teilnehmer nicht angezeigt. Sie können entweder in der Suchleiste &quot; *Suchlerner* &quot; nach einem Teilnehmer suchen oder oben in der **Suchleiste den Link &quot;Download** &quot; auswählen, um die Teilnehmerliste herunterzuladen.

### Seite &quot;Administrator– Teilnehmer&quot;

Bei der Suche nach anwendergebundenen Anwendern können Teilnehmer **** und **Exportoptionen** denselben Bericht herunterladen. Während du nach einer Anwendergruppe suchst, kannst du nun gefilterte Benutzer aus dieser Benutzergruppe herunterladen. Wenn du eine Benutzergruppe suchst,
die Liste der **Teilnehmer** herunterladen ändert sich in **der Download-Teilnehmerliste für die Anwendergruppe** . Die **Option &quot;Exportieren** &quot; lädt die gesamte Liste erneut herunter.

### Seite &quot;Admin- Users&quot;

#### Interne Benutzer

Wenn die Anzahl der Anwender beispielsweise 50.000 überschreitet, wird angezeigt, dass die Daten später für eine detailliertere Analyse heruntergeladen werden können. Die Suchleiste ist jetzt prominent und zeigt einen Benutzer im Format *Name, E-Mail an | 3D-Abo*.

>[!NOTE]
>
>Das 3D-Abo wird nur angezeigt, wenn das 3D-Abo für das Konto aktiviert ist.

#### Externe Benutzer

Für externe Benutzer gilt dasselbe Verhalten. Wenn die Anzahl der Benutzer groß ist, kannst du die Benutzer herunterladen und nach einer Suche im Format *Name, E-Mail | 3D-Abo*.

#### Seite zum Bereinigen von Anwendern

Auf der Seite &quot;Benutzer bereinigen&quot; haben wir für gelöschte Benutzer die Sortierfunktion zum **Gelöschten** Datum entfernt. Du kannst nur die UUIDs sortieren.

### Seiten der Admin-Instanz

#### Kurs- oder Lernpfad

Wenn die Anzahl der Anmeldungen groß ist, zeigt Adobe Learning Manager die Anzahl der Teilnehmer nicht an. Stattdessen gibt es ein Symbol, das du auswählen und die Anzahl der Teilnehmer anzeigen und zur Seite &quot;Teilnehmer&quot; navigieren kannst.

Die Anzahl der Teilnehmer wird als ungefährer Wert angezeigt. Wenn beispielsweise die Anzahl der Teilnehmer mehr als 50.000 ist, wird der Wert als 50K+ angezeigt.

### Seiten für Admin- L1/L3

Wenn die Anzahl der Kursanmeldungen groß ist, wird auf der L1-Feedback-Seite die Liste der Teilnehmer nicht angezeigt. Stattdessen kannst du die Liste der Benutzer exportieren, um später eine detailliertere Analyse durchzuführen.

Die Suche unterstützt die Vorausplanung, und die Ergebnisse sind auf die ausgewählte Instanz beschränkt.

#### Teilnahme- und Bewertungsseite

Auf der Seite wird bei der Suche nach einem Benutzer die Suche über alle verfügbaren Instanzen hinweg ausgeführt. Das Ergebnis ist jedoch für die ausgewählte Instanz.

Wenn du auf der Anwesenheitsseite nach einer Benutzergruppe suchst und die Anzahl der Benutzer unabhängig von der Anmeldung 10.000 Benutzergruppen überschreitet, kannst du nur Aktionen auf Massenebene durchführen. Sie können die Liste der Benutzer nicht anzeigen.

Wenn die Anzahl der Benutzer in der Benutzergruppe weniger als 10.000 beträgt, kannst du Aktionen auf Benutzerebene zusammen mit Aktionen auf Bulk-Ebene durchführen. In diesem Fall wird die Liste der Benutzer nicht deaktiviert.

### Seite &quot;Administratorzertifizierungen&quot;

Bei einer aktuellen Version von Adobe Learning Manager ist es bei einer großen Anzahl von Anwendern, die sich für eine Zertifizierung angemeldet haben, nicht möglich, die nicht abgerollten Teilnehmer anzuzeigen, da das **Dropdown-Menü &quot;Status** &quot; deaktiviert wurde.

Wenn die Anzahl der registrierten Anwender in dieser Version von Adobe Learning Manager groß ist, **werden im Dropdown-Menü &quot;Status** &quot; nur zwei Optionen angezeigt: **&quot;Registriert&quot;** und **&quot;Nicht abgerollt**&quot;. Die Option **&quot;Registriert** &quot; ist standardmäßig ausgewählt. Wenn du &quot;Nicht abgerollt&quot; (Unenrolled **) auswählst**, wird die Liste der nicht abgerollten Teilnehmer angezeigt.

#### Änderungen an Anwendergruppen

Wenn die Anzahl der Anwender in der Benutzergruppe kleiner als z. B. 50.000 ist, wird im **Dropdown-Menü &quot;Status** &quot; alle Optionen &quot;Zertifiziert&quot;, &quot;Zugewiesen&quot; und &quot;Ablaufdatum&quot; angezeigt.

Wenn die Anzahl der Benutzer in einer Anwendergruppe groß ist, werden im Dropdown-Menü &quot;Status **&quot; gemäß dem** neuen Design nur zwei Optionen angezeigt: **&quot;Enrolled**&quot; und **&quot;Unenrolled**&quot;.

### Vergleichstabelle

<table>
    <tbody>
        <tr>
            <td><b>Seite</b></td>
            <td><b>Vor der Änderung des Schwellenwerts</b></td>
            <td><b>Nach dem Ändern des Schwellenwerts</b></td>
        </tr>
        <tr>
            <td>Admin-Kursinstanz</td>
            <td>Instanzen werden wie folgt angezeigt:
            <ul>
                <li>Module</li>
                <li>Registrierte Teilnehmer</li>
                <li>Sitzungen</li>
                <li>Abzeichen</li>
                <li>L1-Feedback aktiviert</li>
                <li>Benachrichtigungswarnungen</li>
                <li>Gamification-Punkte</li>
                <li>QR-Code</li>
                <li>Erweiterung des Lernpfads</li>
            </ul>
            <td>
                <ul>
                    <li>Wenn die Anzahl der Anmeldungen den vordefinierten Schwellenwert überschreitet, wird die Anzahl der Anmeldungen von ALM nicht angezeigt. die Anzahl wird durch ein Symbol ersetzt. Wenn du darauf klickst, wird die tatsächliche Anzahl der Teilnehmer angezeigt und ein Link zur Seite "Teilnehmer" angezeigt.</li>
                    <li>Die Anzahl der Anmeldungen wird in einem ungefähren Format angezeigt. Wenn die Anzahl beispielsweise mehr als 50.000 beträgt, wird die Zählung auf Kursebene als 50K+ angezeigt.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Seite "Administrator– Teilnehmer"</td>
            <td>
                    <ul>
                        <li>Die Liste der Teilnehmer wird für jede Instanz angezeigt.</li>
                        <li>Du kannst einen Anwender oder eine Anwendergruppe durchsuchen, die an einem Kurs angemeldet sind.</li>
                        <li>Der exportierte Bericht umfasst keine Filter für die Anwendergruppe.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Die Auswahl der Instanz wird deaktiviert.</li>
                    <li>Die Teilnehmerliste kann nur in einem Fall heruntergeladen werden. Wenn du nach einer Benutzergruppe suchst und dann die Teilnehmerliste auswählst, werden diese Daten von der Anwendergruppe heruntergeladen.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Feedback-Seite für Admin L1/L3</td>
            <td>
                <p>Keine Änderung des vorhandenen Verhaltens</p>
            </td>
            <td>
                <ul>
                    <li>Die Auswahl der Instanz wird deaktiviert.</li>
                    <li>Wenn die Anmeldung für einen Kurs über 50 KB liegt, listet ALM die Teilnehmer nicht auf und zeigt nur die Suchleiste an. Wenn die Registrierung weniger als 50 KB beträgt, zeigt ALM sowohl die Teilnehmerliste als auch die Suchleiste an.</li>
                    <li>Das Angebot wird standardmäßig deaktiviert.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Seite "Teilnahme und Bewertung für Administratoren"</td>
            <td>
                <p>Keine Änderung des vorhandenen Verhaltens</p>
            </td>
            <td>
                <ul>
                    <li>Die Auswahl der Instanz wird bei der Suche nach einem Benutzer deaktiviert.</li>
                    <li>Wenn die Anzahl der Benutzer beispielsweise 50.000 überschreitet, wird eine zusätzliche Nachricht angezeigt, in der die Daten später für eine detailliertere Analyse heruntergeladen werden können. Die Suchleiste ist jetzt prominent und zeigt einen Benutzer im Format Name, E-Mail an | 3D-Abo.</li>
                    <li>Wenn die Anzahl der Benutzer in der Benutzergruppe unabhängig von der Anmeldung weniger als 10.000 beträgt, kannst du Aktionen auf Benutzerebene zusammen mit Aktionen auf Massenebene durchführen. In diesem Fall wird die Liste der Benutzer nicht deaktiviert.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Seite "Admin- L2 Quiz Score"</td>
            <td>
                    <ul>
                        <li>Auch die Benutzersuche ist implementiert.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Auch die Benutzersuche ist implementiert. Während der Typoshead auf LO-Ebene sucht, wird die Liste auf die derzeit ausgewählte Instanz gefiltert.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Seite für Administratoren (intern, extern)</td>
            <td>
                    <ul>
                        <li>Die E-Mail-ID wird bei der Suche nach einem Benutzer angezeigt.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Wenn die Anzahl der Anwender beispielsweise 50.000 überschreitet, wird eine zusätzliche Nachricht angezeigt, in der die Daten später für eine detailliertere Analyse heruntergeladen werden können. Die Suchleiste ist jetzt prominent und zeigt einen Benutzer im Format Name, E-Mail an | 3D-Abo.</li>
                    <li>Auf der Bereinigungsseite für gelöschte Benutzer haben wir die Sortierfunktion für **Datum gelöscht** entfernt. Du kannst nur die UUIDs sortieren.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Einreichung von Kursleitern</td>
            <td>
                    <ul>
                        <li>Paginierung der zu übermittelnden Module.</li>
                        <li>Als Kursleiter kannst du jetzt eingereichte Dateien von Teilnehmern nach Status filtern und die Prüfung beenden, die Einreichung ausstehend, bestanden und nicht bestanden. </li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Sie können nur Benutzer durchsuchen, nicht Benutzergruppen in dieser Instanz.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Auf die Vorschau als Teilnehmerseite zählen</td>
            <td>
                    <ul>
                        <li>Count umfasst die Daten aus der Anmeldung bei höheren Bestellungen.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Count schließt Daten von Anmeldungen höherer Bestellungen aus.</li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>

## Erweiterte Suchfunktionen

In dieser Version haben wir das Sucherlebnis verbessert. Die Suchergebnisse werden nicht nur basierend auf den Metadaten abgerufen, sondern auch auf der semantischen und inhaltsspezifischen Suche, um Ergebnisse basierend auf Präzision, Aktualität und relevantem Content zu erhalten.

Diese Veränderung spiegelt folgende Themen wider:

* Katalog und Meine Lernseite: Die Hover-Aktion zu Kurs, Lernpfad und Zertifizierung wurde entfernt.
* Das Erscheinungsbild der Suchleiste.
* Filter-Tags in der Lern-App hinzugefügt.

Um die Suchfunktionen zu aktivieren, wende dich an das CSAM-Team von Adobe Learning Manager.

## Änderungen in der Benutzeroberfläche {#ui-changes}

### Seite zur Kurserstellung

Während die Zuordnung der Kurse auf ein Kompetenzniveau erfolgt, ist die Liste der Fähigkeiten &quot;Search First&quot;. Mit anderen Worten: Suchfähigkeiten, und du siehst eine Liste der Fähigkeiten, die zum gesuchten Begriff passen.

### Benutzergruppen

#### Administrator: Teilnehmerseite

Bei der Suche nach anwendergebundenen Anwendern können Teilnehmer **** und **Exportoptionen** denselben Bericht herunterladen. Während du nach einer Anwendergruppe suchst, kannst du nun gefilterte Benutzer aus dieser Benutzergruppe herunterladen. Bei der Suche nach einer Benutzergruppe wird die Liste der **Teilnehmer** zum Herunterladen der Teilnehmerliste für die Anwendergruppe **geändert. Die** Option &quot;Exportieren **&quot; lädt** die gesamte Liste erneut herunter.

## Änderungen an Berichten

* Die Spalten &quot;Tag(s) und Kompetenz(en) im Schulungsbericht&quot; werden in &quot;Tag(s) und &quot;Skills&quot; geändert.
* Der Bericht [&quot;Gamification Audit Trail&quot;](administrators/feature-summary/reports.md#gamification-audit-trail) hinzugefügt.
* Wenn ein Konto mehr als 280000 Teilnehmer enthält, die einer Fertigkeit zugewiesen wurden, wird der Skill-Teilnehmerbericht als zipped csv heruntergeladen.
Wenn das Konto weniger als 250000 Teilnehmer hat, wird derselbe Bericht als CSV heruntergeladen.
Wähle **auf der Admin-Seite &quot;Administratorfähigkeiten** &quot; > **Skills** > **Skill** > **Teilnehmer** aus. Der Report wird als CSV heruntergeladen.
* Der [Bericht &quot;Session Summary&quot;](administrators/feature-summary/reports.md#session-summary-report) enthält zwei neue Spalten: Standortinformationen und Standortbereich.

## Änderungen an der Erstellung von Lernumgebungen

Basierend auf den [Administratoreinstellungen](administrators/feature-summary/classroom.md#classroom-settings) kannst [du als Autor Speicherorte](administrators/feature-summary/classroom.md#add-classroom-location) erstellen, ändern und löschen.

>[!NOTE]
>
>Autoren (in der Kurserstellungsseite) und Administratoren (auf der Instanzseite) erhalten beim Hinzufügen von Speicherorten und Katalogbeschriftungen eine automatisch befüllte Liste der Speicherorte bzw. Katalogbeschriftungen.

Als Administrator kannst du Einschränkungen für einen Autor zum Ändern oder Löschen eines Lernumgebungsstandorts durchsetzen. Weitere [Informationen findest du in den Lernumgebungen](administrators/feature-summary/classroom.md#classroom-settings) .

## Änderungen am flexiblen Lernpfad

Alle (alten und neuen) Konten beginnen, einschließlich Anmeldeschluss, Anmeldeschluss und Abrollfrist sowie &quot;Seat Limit&quot; in der Teilnehmer-App für einen flexiblen Lernpfad.
Teilnehmer können sich jetzt für den flexiblen Lernpfad anmelden, ohne eine Instanz des Kurses auszuwählen.

## Neuer Trigger für Lernpläne

Auf der Setup-Seite für den Lernplan wurde ein neuer Trigger hinzugefügt. Autoren und Administratoren können jetzt Aktionen auslösen, wenn ein Teilnehmer ein Modul eines Kurses nicht ausführt.

Weitere [Informationen findest du in den Lernplänen](administrators/feature-summary/learning-plans.md) .

## Neuer Bewerbungsstatus

Als Kursleiter kannst du jetzt eingereichte Dateien von Teilnehmern nach Status filtern und die Prüfung beenden, die Einreichung ausstehend, bestanden und nicht bestanden.

Weitere [Informationen findest du im Status](instructors/feature-summary/learners.md#filter-file-submissions) für Bewerbungen.

## Verbesserungen an der Checkliste

Im März 2024 release von Adobe Learning Manager wurden folgende Verbesserungen am Checklisten-Workflow vorgenommen:

### Nicht mehr zulässige Bearbeitung einer Checkliste

Wenn ein Autor eine Checkliste erstellt, kann er im Abschnitt &quot;Obligatorische Checkliste aktivieren&quot;**auswählen**. Auf diese Weise wird verhindert, dass ein Teilnehmer im Modul nicht an der Checkliste teilnimmt. Sie können nur fortfahren, wenn sie die Checkliste bestehen.

Die Prüfer der Checkliste, d. h. Lehrkräfte oder Manager, können dann den Status der Checkliste überprüfen. Prüfer können auch die Checkliste eines Teilnehmers außerhalb der Reihenfolge überprüfen.

### Überprüfung einer Checkliste

Wenn ein Autor eine Checkliste erstellt, kann er im Abschnitt &quot;Erneute Bewertung aktivieren&quot;**auswählen**. Auf diese Weise kann ein Manager oder Lehrer einen Teilnehmer neu bewerten, bis er die Checkliste bestanden hat.

Wenn das Modul obligatorisch ist, wird standardmäßig das Kontrollkästchen &quot;Neuauswertung&quot; aktiviert.

Ein Kursleiter oder Manager kann auch den Status einer Checkliste ändern, wenn die erneute Bewertung aktiviert ist.

Auf der Seite &quot;Checkliste&quot; kann ein Kursleiter die Anzahl der Teilnehmer im Status &quot;Ausstehend&quot; anzeigen. Als Kursleiter kannst du einen Teilnehmer bewerten und sie bestehen oder schlagen. Wenn sich ein Teilnehmer in einem misslungenen Status befindet, kannst du die Checkliste nur anzeigen, wenn die erneute Bewertung nicht aktiviert ist.

Das bedeutet, dass das **Kontrollkästchen Aktivieren** beim Erstellen der Checkliste im Abschnitt &quot;Neu bewerten&quot; nicht aktiviert wurde. Wenn dieses Kontrollkästchen aktiviert ist, siehst du auf der Seite &quot;Instructor Checkliste&quot; die Schaltfläche &quot;Ansicht/Auswerten neu bewerten&quot;.

Wenn du den Button auswählst, kannst du einen Teilnehmer erneut bewerten und sie als bestanden oder misslungen markieren.

>[!NOTE]
>
>Beide Funktionen – Neubewertung und Checkliste als obligatorisch – gelten nur für neu erstellte Module. Sobald ein Kurs veröffentlicht wurde, können diese nicht mehr ein- und ausgeschaltet werden.


Anzeigen [. Erstelle eine Checkliste](authors/feature-summary/courses.md#checklist-fail) für weitere Informationen.

## Sonstige Verbesserungen

### Session-bezogene E-Mail-Benachrichtigungen

In früheren Versionen von Adobe Learning Manager hat ein Teilnehmer keine Session-bezogenen E-Mails, aktualisierten Session-Details, Session-Einladungen und Session-Erinnerungen erhalten, wenn:

* Teilnehmer haben einen Kurs abgeschlossen,
* Einem Kurs werden neue Sessions hinzugefügt oder
* Bei vorhandenen Sessions gibt es Änderungen.

Im März 2024 release von Adobe Learning Manager wurden folgende Änderungen vorgenommen:

* Aktualisierte Session-Details und Session-Einladung (für Teilnehmer und Kursleiter)
   * Für zukünftige Sessions werden E-Mails mit **aktualisierten** Session-Details, **Session-Einladungen** für eingeschriebene Teilnehmer und aktuelle Kursleiter nicht mehr weiterentwickelt. Bei früheren Sitzungen bleiben E-Mails mit **aktualisierten** Session-Details und **Session-Einladungen** für eingeschriebene Teilnehmer und aktuelle Kursleiter erhalten.
* Erinnerungs-E-Mails (für Administratoren und Teilnehmer)
   * Für zukünftige Sessions werden nur **E-Mails mit Session-Erinnerung** gesendet.

>[!NOTE]
>
>Die E-Mails hängen nicht von der Session und dem Abschluss des Kurses ab.


### Änderungen an AEM Referenzseite

Auf einer AEM Reference-Site haben wir die Unterstützung für das Hinzufügen von Admin Refresh Token zu dem Teilnehmerzugriffstoken hinzugefügt.

### Einreichungen von Kursleitern ausblenden

Nachdem Teilnehmer ihre Dateien über den Workflow für die Einreichung von Dateien hochgeladen haben, wird die eingereichte URL nach einer vordefinierten Anzahl von Tagen ausgeblendet, wenn ein Kursleiter keine Maßnahmen (Genehmigen oder Ablehnen) an der Einreichung vornimmt. Wende dich an die CSAM-Teams von Adobe Learning Manager, um die Anzahl der Tage festzulegen oder zu ändern.

### Änderungen an Produktterminologien

Wir haben die Spalten *&quot;Instanz&quot;* und *&quot;Teilnehmer* &quot; zum Vokabular der Produktterminologie hinzugefügt.

### Änderungen an Mobile Apps

In dieser App-Version können Teilnehmer überfällige Kurserinnerungs-Erinnerungen planen und verwalten. Wenn du auf eine überfällige Erinnerungsbenachrichtigung klickst, kannst du auf die folgenden Optionen zugreifen:

* Abbrechen
* Zum Kurs
* Erinnere mich in 3 Tagen noch einmal.
* Erinnere mich in einer Woche noch einmal daran.

Auf Android: Wenn du auf die Push-Benachrichtigung klickst, kommst du zur **Kursübersicht** .
Auf iOS: Wenn du auf die Push-Benachrichtigung klickst, öffnest du die Startseite der App. Dies ist eine bekannte Einschränkung in iOS.

### Checklistenänderungen in der Teilnehmer-App in Salesforce

Wenn ein Teilnehmer eine Checkliste nicht erfüllt, kann er nicht zum nächsten Modul oder Kurs fortfahren. Wenn das Kontrollkästchen &quot;Obligatorische Checkliste&quot; aktiviert ist, kann der Teilnehmer einen Kurs nicht voran bringen, wenn er die Checkliste nicht erfüllt.

Wenn ein Teilnehmer eine Checkliste in der Salesforce-App nicht erfüllt, wird wie bei der Web-App eine Nachricht angezeigt und wird nicht vorankommen.

### Änderungen in Connect VC

In den aktuellen Versionen von Adobe Learning Manager wird ein Teilnehmer mit dem Vermerk &quot;Nicht teilnehmend **&quot; gekennzeichnet**, wenn er für eine Connect VC-Sitzung angemeldet ist, aber die Abschlusskriterien nicht erfüllt hat.

In dieser Version wird der Status &quot; **Noch nicht markiert&quot; geändert**.

### White-Labeling in Adobe Learning Manager

Die Adobe Learning Manager-App unterstützt jetzt die White-Label-Kennzeichnung. Das heißt, du kannst die App jetzt unter deinem eigenen Branding veröffentlichen.

Weitere Informationen findest du in der [Adobe Learning Manager-App](white-label.md) .

### Neue Spalte in Migrations-CSVs

In dieser Version gibt es eine neue, optionale Spalte uniqueLoId in den folgenden Migrations-CSVs.

* certification.csv
* course.csv
* learning_program.csv

>[!NOTE]
>
>Die **uniqueLoId-Spalte** ist optional.


Wenn du eine Migration durchführen, um einen vorhandenen Kurs oder einen Lernplan oder eine Zertifizierung zu aktualisieren, wird der Kurs oder der Lernplan oder die Zertifizierung mit den **uniqueLOIds** der Author-App hinzugefügt.

Bei der Migration müssen die **eindeutigenLOId-Werte** in den CSVs für kurs- oder Lernplan oder Zertifizierung aktualisiert werden, auch wenn es sich um eine optionale Spalte handelt.

Wenn die **UniqueLoId-Spalte** vor der Migration beim Aktualisieren des vorhandenen Kurses oder des Lernplans oder der Zertifizierung **mit uniqueLOId** s nicht hinzugefügt wird, werden die uniqueLOId-Werte **nach der** Migration mit NULL überschrieben.

>[!NOTE]
>
>Die Spalte **uniqueLoId** gilt nicht für die Job Aid CSV.


>[!IMPORTANT]
>
>Die Spaltenwerte müssen im gesamten Konto eindeutig sein. Sie können bei einem Kurs oder einer Zertifizierung nicht denselben Wert verwenden.

Lade die CSVs aus dem [Migrationshandbuch](integration-admin/feature-summary/migration-manual.md#csv-specifications-and-sample-csvs) herunter.


### App-Bewertung

Ein Teilnehmer kann sein Feedback zur Adobe Learning Manager-App übermitteln, um das Anwendererlebnis weiter zu verbessern. Wenn der Teilnehmer einen Stern oder mehr bewertet, wird ein Popup-Fenster angezeigt, das den Teilnehmer auffordert, die App im Play Store oder App Store zu bewerten.

### Bluejeans wurde im Februar 2024 eingestellt.

Wir möchten euch mitteilen, dass Bluejeans im Februar 2024 sein Lebensende (EOL) erreicht hat. Nach Februar 2024 erhält Bluejeans keine Updates und keinen Support mehr. Unsere CSAM- und Support-Teams unterstützen dich bei Fragen oder Anliegen, die du während dieser Übergangszeit hast.

Weitere [Informationen zur Konfiguration von Connectoren findest du in Adobe Learning Manager](integration-admin/feature-summary/connectors.md) .

### Änderungen am Anmeldezugriffsbericht

Der Login-Zugriffsbericht ist nur für die letzten fünf Quartale verfügbar. Wenn ein Integrations-Administrator den On-Demand-Download des einheitlichen Exports mit **Anmeldezugriff** aktiviert hat, wird adobe Learning Manager eine Fehlermeldung angezeigt. Auf andere Berichte hat dies jedoch keine Auswirkungen.

### ADFS-Änderungen

Die ADFS-Felder &quot;Mitarbeitertyp&quot; und &quot;Mitarbeiter-ID&quot; sind nun basierend auf den Zuordnungen in Adobe Learning Manager verfügbar.

## API-Änderungen in dieser Version

### Teilnehmer-APIs

In dieser Version haben wir API Unterstützung für Teilnehmer hinzugefügt, um das Branding-Logo und personalisierte Themen auf Der Ebene der Benutzergruppe anzuzeigen.

Die APIs /account und /user?include=account gibt vier Felder zurück, die speziell für das aktive Feld des Benutzers überschrieben werden, gehören logoUrl, logoStyling und themeData.

### Neue Attribute

Ein neues Attribut, isExpiredSubmission, in learningObjectResource, das zeigt, ob der Antrag in der Ressource abgelaufen ist oder nicht.

* GET/Account-API: Gibt das neue Attribut **zum Ablauf derUbmission Zurück** . Dabei ist X die festgelegte Anzahl von Tagen. Falls nicht festgelegt, wird &quot;0&quot; zurückgesendet.
* GET/LO-API mit Ressource enthält das neue Attribut **isExpiredSubmission**&quot; True oder False.
   * Stimmt, wenn die Bewerbung abgelaufen ist und &quot;submissionUrl&quot; nicht angezeigt wird.
   * Wenn &quot;False&quot;, ist die Bewerbung nicht abgelaufen und &quot;submissionUrl&quot; wird abgerufen.

### API Änderungen in der Checkliste

Ein Kurs kann aus mehreren Modulen bestehen, deren Checkliste eine Modulart ist. Dieses Checklistenmodul wird vom Kursleiter bewertet und kann basierend auf der Bewertung als &quot;Gescheitert&quot; oder &quot;Erfolg&quot; gekennzeichnet werden.

In beiden Fällen wird der Checklistenstatus jedoch mit &quot;Abgeschlossen&quot; gekennzeichnet, und auf diese Weise wird der Kurs mit &quot;Abgeschlossen&quot; gekennzeichnet.

In dieser Version enthält die LO-API den Parameter *isChecklistMandatory*. Wenn der Wert &quot;Wahr&quot; ist, ist die Checkliste obligatorisch.

### Unterstützung für mehrere Locales

Administratoren können den L1-Feedbackbericht in der Sprache ihrer Wahl herunterladen. L1-Feedback-Berichte für Power BI können jedoch noch nicht heruntergeladen werden. Verwende in der API-Anfrage den Parameter preferredLocale, um den Standort deiner Wahl anzugeben.

### Änderungen in der Übersicht über die Anzahl der Instanzen

Dies gilt für Konten mit mehr als 1000 Anmeldungen für einen Kurs im Klassenzimmer/VC.

Wenn die Zahl weniger als 1000 beträgt, werden die Cache-Werte ungültig, und die aktualisierten Werte werden in einer GET Summary API Call wie Anzahl der Anmeldung, Abschluss und seatVideo zurückgegeben.

Wenn das Konto für diese Funktion aktiviert ist und die Anzahl der Anmeldungen mehr als 1000 beträgt, werden die Werte aus dem Cache abgerufen.

### Veraltete Pfade

Derzeit folgen Learning Manager-APIs einer Diagrammdatenstruktur, mit der ihr Daten abrufen könnt, indem ihr das API Modells durch includes durchläuft. Auch wenn du eine API mit bis zu sieben Ebenen durchqueren kannst, ist das Abrufen der Daten mit einem einzigen API-Aufruf rechenintensiv.

Wir empfehlen allen Bestands- und Neukunden, mehrmals kleine Anrufe statt eines großen Anrufs abzurufen. Dieser Ansatz verhindert, dass unerwünschte Daten in den Anruf geladen werden.

#### Welche Pfade sind veraltet?

Die folgenden Pfade sind veraltet:

* /learningObjects
   * Veraltete Pfade:
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Vorhandene Pfade:
      * enrollment.loInstance
      * instances.loResources
* /learningObjects/{id}
   * Veralteter Pfad:
      * enrollment.instances.subLoInstances.learningObject
   * Vorhandener Pfad:
      * enrollment.instances.subLoInstances
* /Eintragungen
   * Veralteter Pfad:
      * loInstance.learningObject.enrollment
   * Neuer Weg:
      * loInstance.learningObject
* /learningObjects/{id}
   * Veralteter Pfad:
      * instance.subLoInstances.learningObject.enrollment.loResourceGrades
   * Neuer Weg:
      * instance.subLoInstances

### Anmeldezugriff und Prüfbericht zur Archivierung von Änderungen an Job-API

Mit dieser Version behält der Job-API den Anmeldezugriffsbericht bis zu fünf Quartale und den Prüfbericht der Anwender sechs Monate lang bei. Wenn du die Daten älter als diesen Zeitraum herunterladen möchtest, musst du den Archivparameter mit der Angabe von Quartal und Jahr übergeben. Referenziere die Nutzlast des Beispiels.

```
{
    "data": {
        "type": "job",
        "attributes": {
            "description": "description of your choice",
            "jobType": "generateLoginAccessReport",
            "payload": {
                "fromDate": "2023-04-01T18:30:00.000Z",
                "toDate": "2023-04-30T18:30:00.000Z",
                "archive": {
                    "quarter": "4",
                    "year": "2021"
                }
            }
        }
    }
}
```

Wenn du versuchst, den **Bericht &quot;Login Access** &quot; herunterzuladen, der über fünf Quartale hinausgeht, wird eine Fehlermeldung angezeigt. Eine ähnliche Fehlermeldung wird angezeigt, wenn du versuchst, den Bericht &quot;Anwenderprüfung **&quot; herunterzuladen, der**&#x200B;über sechs Monate hinausgeht.

### Veraltete APIs

Eine [kumulative Liste aller veralteten APIs im Produkt API-Deprecations in Adobe Learning Manager](api-deprecations-list.md) anzeigen.

## In diesem Update behobene Fehler {#bug-fixes}

* Wenn ein Teilnehmer an einem Kurs angemeldet ist und dann versucht, sich für einen anderen Kurs anzumelden, wird eine Warnmeldung angezeigt.
* Eine Benutzergruppe ist auch nach der Löschung in Search sichtbar.
* Wenn Anwender viele Teilnehmer-Protokolle mit einer großen Datenmenge auslösen, wird die Warteschlange für Teilnehmerprotokolle blockiert und eine neue Anforderung verhindert.
* Wenn ein Kind sein Elternkonto auffordert, einen Bericht weiterzugeben, kann das Elternkonto dies nicht tun.
* Die URLs aus einem Kurs und ein Lernpfad leiten zu falschen Speicherorten um.
* Ein Teilnehmer sieht sich die Kursinstanz eines anderen Kurses gelegentlich an, indem er auf den Kurs-Link auf der Katalogseite klickt.
* Die **Schaltfläche &quot;Abrollen** &quot; wird nicht wie erwartet nach der ersten Anmeldung angezeigt, sondern nach einer Aktualisierung.
* Sie können weder Inhalte noch Tests mit einem leeren Platz im Namen speichern.
* In von Managern genehmigten Kursen könnt ihr Teilnehmer erneut in eine Anwendergruppe einschreiben.
* Wenn du ein weiteres aktives Feld hinzufügen möchtest, wird in einigen Fällen die Fehlermeldung &quot;Aktive Felder konnten nicht gespeichert werden&quot;, angezeigt.
* Der Text überläuft im Namen eines Kurses innerhalb einer Kurskarte im Abschnitt Verwandte Kurse.
* Nach dem Wechsel einer Instanz und der Anmeldung eines Teilnehmers für die Instanz existieren die alten Instanzen weiterhin im Outlook-Kalender.
* Wenn ein Teilnehmer eines Peer-Kontos versucht, die Miniaturansicht eines Kurses auszuwählen, wird eine Fehlermeldung angezeigt.
* Wenn sich Teilnehmer für einen Kurs anmelden, erhalten sie mehrere Benachrichtigungen für die Anmeldung.
* Wenn ein Anwender den Namen der in einem Connector erstellten Kataloge manuell ändert, werden neue Kataloge erstellt und die Kurse in den falschen Katalogen veröffentlicht.
* Anwender, die inaktive Konten haben, erhalten immer noch Abo-E-Mails.

### bugfixes für API

* Die API GET/Benutzer ruft die Details eines Manager nicht ab.
* In einem Konto wurden Benutzer während einer geplanten Ausfallzeit über einen geplanten FTP-Anwenderimport erstellt.
* In der Mobile App oder im immersiven Modus wird nach dem Löschen oder Zurückziehen einer Kursinstanz und auswählen der nächsten aktiven Instanz statt &quot;Anmeldung&quot; die **Schaltfläche &quot;Interesse** registrieren&quot; angezeigt **.**
* Wenn ein Teilnehmer eines Peer-Kontos versucht, die Miniaturansicht eines Kurses mit dem Lernobjekt API auszuwählen, wird der Fehler 403 203 angezeigt.

## Systemanforderungen

Systemanforderungen für](system-requirements.md) Adobe Learning Manager anzeigen[.

## Frühere Versionen von Adobe Learning Manager

* [November 2023 release](whats-new-november-2023.md)
* [Release Juli 2023](whats-new-2023-july.md)

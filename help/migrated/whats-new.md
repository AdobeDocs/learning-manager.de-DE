---
description: Erfahren Sie mehr über die neuen Funktionen und Verbesserungen in der Version März 2024 von Adobe Learning Manager.
jcr-language: en_us
title: Zusammenfassung der neuen Funktionen
contentowner: jayakarr
exl-id: 603f1f1c-bf8d-4807-b9f7-b10ded19a91e
source-git-commit: 42d595e167663cb368e3597cfc4d9a49313ff46d
workflow-type: tm+mt
source-wordcount: '3661'
ht-degree: 1%

---

# Zusammenfassung der neuen Funktionen {#new-features-summary}

Informationen über die neuen Funktionen und Verbesserungen in Adobe Learning Manager

## Neue Funktionen in dieser Version {#whatsnewandchanged}

### Kenntnisse aus externen Quellen importieren

Importieren Sie Kenntnisse von Inhaltsanbietern wie LinkedIn und Go1 mithilfe der entsprechenden Connectors. Diese Verbesserung ist Teil des Ziels, Learning Manager in die Lage zu versetzen, sich in externe Skills Clouds und Talent Management Systeme zu integrieren. Die importierten Kenntnisse werden den vom Administrator definierten Kenntnissen im Lern-Manager hinzugefügt und stehen den Autoren während des Workflows zur Kurserstellung zur Verfügung. Darüber hinaus wurden Verbesserungen an der Funktionalität zur Kenntnissuche in der gesamten Plattform vorgenommen, um eine bessere Sucherfahrung zu bieten, wenn das Konto über eine große Anzahl von Kenntnissen verfügt.

Anzeigen [Kenntnisse importieren](administrators/feature-summary/import-skills-external-sources.md) , um mehr zu erfahren.

### Benutzerdefiniertes Branding

Sie können jetzt bestimmte Benutzeroberflächenelemente anpassen - den Organisationsnamen, das Logo und das UI-Design basierend auf den im Konto verfügbaren Benutzergruppen. Beispielsweise kann eine Organisation mit mehreren Abteilungen ein benutzerdefiniertes Logo und ein UI-Thema einrichten, die für jede Abteilung angezeigt werden.

>[!NOTE]
>
>Diese Funktion für mehrere Brandings gilt nicht für die Ansicht des Administrators. Das Branding auf Organisationsebene ist in jedem Account sichtbar. Dies liegt daran, dass dies eine Teilnehmerfunktion ist und die Administratoren diese möglicherweise nicht in ihrem Konto haben möchten.

Anzeigen [Mehrere benutzerdefinierte Brandings](administrators/feature-summary/themes.md#multiple-branding) für weitere Informationen.


## Änderungen für Konten mit großer Benutzerbasis

### Admin- Seiten Kurs- oder Lernpfad

Wenn sich viele Teilnehmer für den Kurs registriert haben, z. B. mehr als 50.000, wird die Liste der Teilnehmer nicht angezeigt. Sie können entweder im *Teilnehmer suchen* Suchleiste oder wählen Sie die Option **Herunterladen** oben in der Suchleiste, um die Liste der Teilnehmer herunterzuladen.

### Admin: Seite &quot;Teilnehmer&quot;

Wenn Sie nach einem Benutzer suchen, wird das Dialogfeld &quot; **Teilnehmer herunterladen** und **Exportieren** Optionen laden den gleichen Bericht herunter. In der Zwischenzeit können Sie beim Suchen nach einer Benutzergruppe jetzt gefilterte Benutzer aus dieser Benutzergruppe herunterladen. Wenn Sie eine Benutzergruppe suchen, wird das Dialogfeld &quot; **Teilnehmerliste herunterladen** Änderungen an **Teilnehmerliste für Benutzergruppe herunterladen** Die **Exportieren** lädt die gesamte Liste erneut herunter.

### Admin: Seite &quot;Benutzer&quot;

#### Interne Benutzer

Wenn die Anzahl der Benutzer z. B. 50.000 übersteigt, wird eine Meldung angezeigt, in der Sie die Daten herunterladen können, um später eine detailliertere Analyse durchzuführen. Die Suchleiste ist jetzt hervorgehoben und zeigt einen Benutzer im Format *Name, E-Mail | UUID*.

>[!NOTE]
>
>Die UUID wird nur angezeigt, wenn UUID für das Konto aktiviert ist.

#### Externe Benutzer

Für externe Benutzer gilt dasselbe Verhalten. Wenn die Anzahl der Benutzer groß ist, können Sie die Benutzer herunterladen und auch die Details eines Benutzers nach einer Suche im Format abrufen. *Name, E-Mail | UUID*.

#### Seite &quot;Benutzerbereinigung&quot;

Auf der Seite Benutzerbereinigung haben wir für gelöschte Benutzer die Sortierfunktion entfernt für **Löschdatum**. Sie können nur nach UUIDs sortieren.

### Admin- Instanzseiten

#### Kurs oder Lernpfad

Wenn die Anzahl der Registrierungen groß ist, zeigt der Adobe Learning Manager die Anzahl der Teilnehmer nicht an. Stattdessen wird ein Symbol angezeigt, das Sie auswählen können, die Anzahl der Teilnehmer anzeigen und zur Seite &quot;Teilnehmer&quot; navigieren können.

Die Anzahl der Teilnehmer wird als ungefährer Wert angezeigt. Wenn beispielsweise die Anzahl der Teilnehmer mehr als 50.000 beträgt, wird der Wert als 50.000+ angezeigt.

### Admin- L1/L3-Seiten

Wenn die Anzahl der Kursregistrierungen groß ist, wird auf der Seite L1-Feedback die Liste der Teilnehmer nicht angezeigt. Stattdessen können Sie die Benutzerliste exportieren, um später eine detailliertere Analyse durchzuführen.

Die Suche unterstützt Type-Ahead und die Ergebnisse sind auf die ausgewählte Instanz beschränkt.

#### Seite Anwesenheit und Punktzahl

Wenn Sie auf der Seite nach einem Benutzer suchen, wird die Suche in allen verfügbaren Instanzen ausgeführt. Das Ergebnis gilt jedoch für die ausgewählte Instanz.

Wenn Sie auf der Seite Anwesenheit nach einer Benutzergruppe suchen und die Anzahl der Benutzer in der Benutzergruppe 10.000 überschreitet, unabhängig von der Registrierung, können Sie nur Aktionen auf Massenebene ausführen. Sie können die Benutzerliste nicht anzeigen.

Wenn die Anzahl der Benutzer in der Benutzergruppe weniger als 10.000 beträgt, können Sie einzelne Aktionen auf Benutzerebene zusammen mit Aktionen auf Massenebene ausführen. In diesem Fall ist die Benutzerliste nicht deaktiviert.

### Seite &quot;Admin- Zertifizierungen&quot;

Wenn in den aktuellen Versionen des Adobe-Lernmanagers eine große Anzahl von Benutzern für eine Zertifizierung registriert ist, können Sie die nicht registrierten Teilnehmer nicht anzeigen, seit der **Status** &quot; deaktiviert ist.

In dieser Version des Adobe-Lernmanagers wird bei einer großen Anzahl von registrierten Benutzern das Dialogfeld &quot; **Status** Dropdown zeigt nur zwei Optionen an: **Registriert** und **Nicht registriert**. Die Option **Registriert** ist standardmäßig ausgewählt. Wenn Sie **Nicht registriert** wird die Liste der nicht registrierten Teilnehmer angezeigt.

#### Änderungen an Benutzergruppen

Wenn die Anzahl der Benutzer in einer Benutzergruppe weniger als z. B. 50.000 beträgt, wird das Dialogfeld **Status** &quot; werden alle Optionen angezeigt - &quot;Zertifiziert&quot;, &quot;Zugewiesen&quot; und &quot;Ablaufend&quot;.

Wenn die Anzahl der Benutzer in einer Benutzergruppe groß ist, wird das Dialogfeld &quot; **Status** Dropdown zeigt nur zwei Optionen an: **Registriert** und **Nicht registriert**, nach dem neuen Design.

### Vergleichstabelle

<table>
    <tbody>
        <tr>
            <td><b>Seite</b></td>
            <td><b>Vor der Schwellenwertänderung</b></td>
            <td><b>Nach Änderung des Schwellenwerts</b></td>
        </tr>
        <tr>
            <td>Admin- Kursinstanz</td>
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
                <li>Learning Path-Erweiterung</li>
            </ul>
            <td>
                <ul>
                    <li>Wenn die Anzahl der Registrierungen den vordefinierten Schwellenwert überschreitet, zeigt ALM die Anzahl nicht an. Die Anzahl wird durch ein Symbol ersetzt. Wenn darauf geklickt wird, wird die tatsächliche Anzahl der Teilnehmer und ein Link angezeigt, über den Sie zur Seite "Teilnehmer" gelangen.</li>
                    <li>Die Anzahl der Registrierungen wird in einem ungefähren Format angezeigt. Wenn die Anzahl beispielsweise mehr als 50.000 beträgt, wird die Anzahl auf Kursebene als 50K+ angezeigt.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Admin: Seite "Teilnehmer"</td>
            <td>
                    <ul>
                        <li>Die Liste der Teilnehmer wird für jede Instanz angezeigt.</li>
                        <li>Sie können einen Benutzer oder eine Benutzergruppe suchen, der bzw. die für einen Kurs registriert ist.</li>
                        <li>Der exportierte Bericht enthält keine Filter für Benutzergruppe.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Die Auswahl der Instanz ist deaktiviert.</li>
                    <li>Die Teilnehmerliste herunterladen lädt außerdem dieselben Daten herunter, mit Ausnahme einer Anfrage. Wenn Sie nach einer Benutzergruppe suchen und dann die Option "Teilnehmerliste herunterladen" auswählen, werden die Benutzergruppendaten heruntergeladen.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Admin-L1/L3-Feedback-Seite</td>
            <td>
                <p>Keine Änderung des bestehenden Verhaltens</p>
            </td>
            <td>
                <ul>
                    <li>Die Auswahl der Instanz ist deaktiviert.</li>
                    <li>Wenn die Registrierung für einen Kurs über 50 KB liegt, listet ALM die Teilnehmer nicht auf und zeigt nur die Suchleiste an. Wenn die Registrierung weniger als 50.000 beträgt, zeigt ALM sowohl die Teilnehmerliste als auch die Suchleiste an.</li>
                    <li>Das Auflisten ist standardmäßig deaktiviert.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Admin- Seite Anwesenheit und Punktzahl</td>
            <td>
                <p>Keine Änderung des bestehenden Verhaltens</p>
            </td>
            <td>
                <ul>
                    <li>Die Auswahl der Instanz ist beim Suchen eines Benutzers deaktiviert.</li>
                    <li>Wenn die Anzahl der Benutzer z. B. 50.000 übersteigt, wird eine zusätzliche Nachricht angezeigt, in der die Daten für eine detailliertere Analyse heruntergeladen werden. Die Suchleiste ist jetzt hervorgehoben und zeigt einen Benutzer im Format Name, E-Mail an. | UUID.</li>
                    <li>Wenn die Anzahl der Benutzer in der Benutzergruppe unabhängig von der Registrierung weniger als 10.000 beträgt, können Sie einzelne Aktionen auf Benutzerebene zusammen mit Aktionen auf Massenebene ausführen. In diesem Fall ist die Benutzerliste nicht deaktiviert.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Seite "Admin- L2 Quizpunktzahl"</td>
            <td>
                    <ul>
                        <li>Die Benutzersuche ist ebenfalls implementiert.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Die Benutzersuche ist ebenfalls implementiert. Während die Voraustippung auf LO-Ebene sucht, wird die Liste nach der aktuell ausgewählten Instanz gefiltert.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Admin- Seite "Benutzer" (intern, extern)</td>
            <td>
                    <ul>
                        <li>Die E-Mail-ID wird bei der Suche nach einem Benutzer angezeigt.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Wenn die Anzahl der Benutzer z. B. 50.000 übersteigt, wird eine zusätzliche Nachricht angezeigt, in der die Daten für eine detailliertere Analyse heruntergeladen werden. Die Suchleiste ist jetzt hervorgehoben und zeigt einen Benutzer im Format Name, E-Mail an. | UUID.</li>
                    <li>Auf der Seite Benutzerbereinigung haben wir für gelöschte Benutzer die Sortierfunktion zum **Datum gelöscht** entfernt. Sie können nur nach UUIDs sortieren.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Kursleiter - Einreichung</td>
            <td>
                    <ul>
                        <li>Paginierung der zu sendenden Module.</li>
                        <li>Als Kursleiter können Sie jetzt Dateiübermittlungen von Teilnehmern nach Status, beendeter Überprüfung, ausstehender Übermittlung, bestanden und fehlgeschlagen filtern. </li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Sie können nur nach Benutzern suchen, nicht nach Benutzergruppen in dieser Instanz.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Auf Vorschau als Teilnehmerseite zählen</td>
            <td>
                    <ul>
                        <li>Die Anzahl enthält die Daten aus der Registrierung mit höherer Reihenfolge.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Die Anzahl schließt Daten aus Registrierungen mit höherer Reihenfolge aus.</li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>

## Erweiterte Suchfunktionen

In dieser Version haben wir die Sucherfahrung verbessert. Die Suchergebnisse werden nicht nur anhand der Metadaten, sondern auch semantisch und inhaltlich abgerufen, um Ergebnisse auf der Grundlage von Genauigkeit, Aktualität und relevantem Inhalt abzuleiten.

Diese Änderung spiegelt Folgendes wider:
* Katalog und Meine Lernseite: Die Hover-Aktion auf Kurs, Lernpfad und Zertifizierung wurde entfernt.
* Das Erscheinungsbild der Suchleiste.
* In der Lern-App wurden Filter-Tags hinzugefügt.

Um die Suchfunktionen zu aktivieren, wenden Sie sich an das CSAM-Team des Adobe Learning Managers.

## Änderungen an Berichten

* Die Spalten &quot;Tag(s)&quot; und &quot;Kenntnisse(s)&quot; im Schulungsbericht wurden in &quot;Tag und Kenntnisse&quot; geändert.
* Bericht hinzugefügt [Gamification-Prüfprotokoll](administrators/feature-summary/reports.md#gamification-audit-trail).
* Wenn ein Konto mehr als 280000 Teilnehmer enthält, die Kenntnissen zugewiesen sind, wird der Bericht zu Kenntnissen und Teilnehmern als gezippte CSV-Datei heruntergeladen.
Wenn das Konto weniger als 250000 Teilnehmer hat, wird derselbe Bericht als CSV heruntergeladen.
Wählen Sie auf der Admin-Seite **Administrator** > **Kenntnisse** > **Kenntnisse** > **Teilnehmer**. Der Bericht wird als CSV heruntergeladen.
* Die [Sitzungsübersicht - Bericht](administrators/feature-summary/reports.md#session-summary-report) hat zwei neue Spalten: &quot;Standortinformationen&quot; und &quot;Standortbereich&quot;.

## Änderungen an der Erstellung von Klassenzimmern

Basierend auf [Administratoreinstellungen](administrators/feature-summary/classroom.md#classroom-settings)können Sie als Autor [Erstellen, Ändern und Löschen von Speicherorten](administrators/feature-summary/classroom.md#add-classroom-location).
>[!NOTE]
>
>Beim Hinzufügen von Speicherort- und Katalogbeschriftungen sehen Autoren (auf der Kurserstellungsseite) und Administratoren (auf der Instanzseite) eine automatisch ausgefüllte Liste von Speicherorten bzw. Katalogbeschriftungen.

Als Administrator können Sie Einschränkungen für einen Autor erzwingen, einen Speicherort für einen Klassenzimmer zu ändern oder zu löschen. Anzeigen [Einstellungen für Klassenzimmer](administrators/feature-summary/classroom.md#classroom-settings) für weitere Informationen.

## Änderungen am flexiblen Lernpfad

Alle Konten (alt und neu) in werden gestartet, einschließlich Registrierungsfrist, Registrierungsfrist für Aufhebung der Registrierung und Sitzplatzbeschränkung in der Teilnehmer-App für einen flexiblen Lernpfad.
Teilnehmer können sich jetzt für einen flexiblen Lernpfad registrieren, ohne eine Instanz des Kurses auszuwählen.

## Neuer Trigger für Lernpläne

Ein neuer Trigger wurde der Lernplan-Einrichtungsseite hinzugefügt. Autoren und Administratoren können jetzt Aktionen auslösen, wenn ein Teilnehmer ein Modul eines Kurses nicht besteht.

Anzeigen [Lernpläne](administrators/feature-summary/learning-plans.md) für weitere Informationen.

## Neuer Übermittlungsstatus

Als Kursleiter können Sie jetzt Dateiübermittlungen von Teilnehmern nach Status, beendeter Überprüfung, ausstehender Übermittlung, bestanden und fehlgeschlagen filtern.

Anzeigen [Übermittlungsstatus](instructors/feature-summary/learners.md#filter-file-submissions) für weitere Informationen.

## Verbesserungen der Checkliste

In der Version März 2024 von Adobe Learning Manager wurden folgende Verbesserungen am Arbeitsablauf für Checklisten vorgenommen:

### Fortschritt bei nicht bestandener Checkliste verhindern

Beim Erstellen einer Checkliste kann ein Autor **Aktivieren** im Abschnitt Obligatorische Checkliste . Dadurch wird verhindert, dass ein Teilnehmer das Modul fortsetzt, wenn er die Checkliste nicht besteht. Sie können nur fortfahren, wenn sie die Checkliste bestehen.

Die Prüflistenprüfer, d. h. Kursleiter oder Manager, können dann den Status der Prüfliste überprüfen. Reviewer können die Checkliste eines Teilnehmers auch ungeordnet durchsehen.

### Neubewertung einer Checkliste

Beim Erstellen einer Checkliste kann ein Autor **Aktivieren** im Abschnitt &quot;Neubewertung&quot;. Dadurch kann ein Manager oder Kursleiter einen Teilnehmer neu bewerten, bis er die Checkliste besteht.

Wenn das Modul obligatorisch ist, ist das Kontrollkästchen für die Neubewertung standardmäßig aktiviert.

Ein Kursleiter oder Manager kann auch den Status einer Checkliste von &quot;Nicht bestanden&quot; in &quot;Bestanden&quot; ändern, wenn die Neubewertung aktiviert ist.

Auf der Seite Checkliste kann ein Kursleiter die Anzahl der Teilnehmer mit dem Status &quot;Ausstehend&quot; anzeigen. Als Kursleiter können Sie einen Teilnehmer bewerten und ihn bestehen oder durchfallen lassen. Wenn ein Teilnehmer den Status &quot;Fehlgeschlagen&quot; aufweist, können Sie die Checkliste nur anzeigen, wenn die Neubewertung nicht aktiviert ist.

Dies bedeutet, dass die **Aktivieren** Das Kontrollkästchen wurde beim Erstellen der Checkliste im Abschnitt &quot;Neubewertung&quot; nicht aktiviert. Wenn dieses Kontrollkästchen aktiviert ist, wird die Schaltfläche &quot;Anzeigen/Erneut bewerten&quot; auf der Seite &quot;Kursleiter-Checkliste&quot; angezeigt.

Wenn Sie die Schaltfläche auswählen, können Sie einen Teilnehmer neu bewerten und ihn als bestanden oder als abgelehnt markieren.

>[!NOTE]
>
>Beide Funktionen - Neubewertung und Checkliste als obligatorisch festlegen - gelten nur für neu erstellte Module. Sobald ein Kurs veröffentlicht wurde, können diese nicht mehr aktiviert/deaktiviert werden.


Anzeigen [Erstellen einer Checkliste](authors/feature-summary/courses.md#checklist-fail) für weitere Informationen.

## Sonstige Verbesserungen

### Sitzungsbezogene E-Mail-Benachrichtigungen

In früheren Versionen des Adobe Learning Manager hat ein Teilnehmer keine sitzungsbezogenen E-Mails, Sitzungsdetails aktualisiert, Sitzungseinladung und Sitzungserinnerung erhalten, wenn:

* Teilnehmer haben einen Kurs abgeschlossen,
* Neue Sitzungen werden einem Kurs hinzugefügt oder
* Es gibt Änderungen an vorhandenen Sitzungen.

In der Version März 2024 von Adobe Learning Manager wurden folgende Änderungen vorgenommen:

* Sitzungsdetails aktualisiert und Sitzungseinladung (für Teilnehmer und Kursleiter)
   * Für zukünftige Sitzungen, E-Mails für **Sitzungsdetails aktualisiert**, **Einladung zur Sitzung** für registrierte Teilnehmer und aktuelle Kursleiter werden verworfen. Bei früheren Sitzungen wurden E-Mails für **Sitzungsdetails aktualisiert** und **Einladung zur Sitzung** für registrierte Teilnehmer und aktuelle Kursleiter bleiben unverändert.
* Erinnerungs-E-Mails (für Administrator und Teilnehmer)
   * Nur für zukünftige Sitzungen **Sitzungserinnerung** E-Mails werden versendet.

>[!NOTE]
>
>Die E-Mails hängen nicht von der Sitzung und dem Kursabschluss ab.


### AEM Änderungen am Referenzstandort

Auf einer AEM haben wir Unterstützung für das Hinzufügen eines Admin-Aktualisierungstokens zu einem Teilnehmerzugriffstoken hinzugefügt.

### Einreichungen von Kursleitern ausblenden

Wenn ein Kursleiter nach dem Hochladen seiner Dateien mithilfe des Arbeitsablaufs für die Dateiübermittlung keine Aktion (Genehmigen oder Ablehnen) für die Übermittlung ausführt, wird die Übermittlungs-URL nach einer vordefinierten Anzahl von Tagen aus der Ansicht ausgeblendet. Wenden Sie sich an die CSAM-Teams des Adobe Learning Manager, um die Anzahl der Tage festzulegen oder zu ändern.

### Änderungen an der Produktterminologie

Wir haben die Spalten hinzugefügt. *Instanz* und *Teilnehmer* in das Produktterminologie-Vokabular ein.

### Änderungen an mobilen Apps

In dieser Version der mobilen App können Teilnehmer überfällige Kurserinnerungen planen und verwalten. Wenn Sie auf eine Benachrichtigung bei einer überfälligen Erinnerung klicken, können Sie auf die folgenden Optionen zugreifen:

* Abbrechen
* Zum Kurs
* In 3 Tagen wieder erinnern
* Erinnere mich in einer Woche wieder.

Unter Android: Wenn Sie auf die Push-Benachrichtigung klicken, werden Sie zum **Kursübersicht** angezeigt.
Auf iOS: Durch Klicken auf die Push-Benachrichtigung werden Sie zur Startseite der App geleitet. Dies ist eine bekannte Einschränkung in iOS.

### Änderungen an der Checkliste in der Teilnehmer-App in Salesforce

Wenn ein Teilnehmer eine Checkliste nicht besteht, kann er nicht zum nächsten Modul oder Kurs übergehen. Wenn das Kontrollkästchen &quot;Obligatorische Checkliste&quot; aktiviert ist, kann der Teilnehmer einen Kurs nicht fortsetzen, wenn er die Checkliste nicht besteht.

Wenn ein Teilnehmer eine Checkliste für die Salesforce-App nicht abschließt, wird wie bei der Web-App eine Meldung angezeigt und der Vorgang wird nicht fortgesetzt.

### Änderungen in Connect VC

In aktuellen Versionen des Adobe-Lernmanagers wird ein Teilnehmer als **Nicht besucht** wenn sie für eine Connect VC-Sitzung registriert sind, aber die Abschlusskriterien nicht erfüllt haben.

In dieser Version ändert sich der Status in **Noch zu markieren**.

### Weiße Beschriftung im Adobe-Lernmanager

Die mobile Adobe Learning Manager-App unterstützt jetzt die Beschriftung auf weißem Hintergrund, d. h., Sie können die App jetzt unter Ihrem eigenen Branding veröffentlichen.

Ansicht Weiße Beschriftung in [Adobe Learning Manager-Mobilanwendung](white-label.md) für weitere Informationen.

### Neue Spalte in Migrations-CSVs

In dieser Version ist die neue, optionale Spalte &quot;uniqueLoId&quot; in den folgenden Migrations-CSVs enthalten.

* certification.csv
* course.csv
* learning_program.csv

Die Spalte &quot;uniqueLoId&quot; gilt nicht für die CSV-Datei &quot;Arbeitshilfe&quot;.

>[!IMPORTANT]
>
>Die Spaltenwerte müssen im Konto eindeutig sein. Sie können nicht denselben Wert für einen Kurs oder eine Zertifizierung verwenden.

Laden Sie die CSV-Dateien von der Seite [Migrationshandbuch](integration-admin/feature-summary/migration-manual.md#csv-specifications-and-sample-csvs).


### App-Bewertung

Ein Teilnehmer kann sein Feedback in der Adobe Learning Manager-App abgeben, um das App-Erlebnis weiter zu verbessern. Wenn der Teilnehmer die Bewertung vier Sterne oder mehr hat, wird ein Popup angezeigt, in dem der Teilnehmer aufgefordert wird, die App im Play Store oder auf App Store zu bewerten.

### Bluejeans hat im Februar 2024 das Ende seiner Lebensdauer erreicht.

Wir möchten Sie darüber informieren, dass Bluejeans am Februar 2024 sein Lebensende (EOL) erreicht hat. Nach Februar 2024 erhält Bluejeans keine Updates und keinen Support mehr. Unsere CSAM- und Support-Teams unterstützen Sie bei Fragen oder Bedenken, die Sie während dieser Übergangszeit haben.

Anzeigen [Connectors im Adobe Learning Manager](integration-admin/feature-summary/connectors.md) für weitere Informationen zum Konfigurieren von Konnektoren.

### Änderungen am Anmeldezugriffsbericht

Der Bericht über den Anmeldezugriff ist nur für die letzten fünf Quartale verfügbar. Wenn ein Integrations-Admin den On Demand-Download des einheitlichen Exports mit **Anmeldezugriff** aktiviert ist, zeigt der Adobe-Lernmanager eine Fehlermeldung an. Es gibt jedoch keine Auswirkungen auf andere Berichte.

### ADFS-Änderungen

Die Felder &quot;Mitarbeitertyp&quot; und &quot;Mitarbeiter-ID&quot; aus ADFS sind jetzt auf der Grundlage der Zuordnungen im Adobe Learning Manager verfügbar.

## API-Änderungen in dieser Version

### Teilnehmer-APIs

In dieser Version haben wir API-Unterstützung für Teilnehmer hinzugefügt, um das Branding-Logo und personalisierte Themen auf Benutzergruppenebene anzuzeigen.

Die APIs /account und /user?include=account geben vier Felder zurück, die speziell für das aktive Feld des Benutzers überschrieben wurden, das zu logoUrl, logoStyling und themeData gehört.

### Neue Attribute

Ein neues Attribut ist &quot;ExpiredSubmission&quot; in &quot;learningObjectResource&quot;, das anzeigt, ob die Übermittlung in der Ressource abgelaufen ist.

* GET /account API: Gibt neues Attribut zurück **expireSubmissionDuration** X, wobei X die eingestellte Anzahl der Tage ist. Wenn nicht festgelegt, wird 0 zurückgegeben.
* GET/LO-API mit Ressource enthält neues Attribut **isExpiredSubmission**&quot;True oder False.
   * True, wenn die Übermittlung abgelaufen ist und &quot;submissionUrl&quot; nicht angezeigt wird.
   * Wenn der Wert auf &quot;False&quot; gesetzt ist, ist die Übermittlung nicht abgelaufen und &quot;submissionUrl&quot; wird abgerufen.

### API-Änderungen in der Checkliste

Ein Kurs kann aus mehreren Modulen bestehen, von denen die Checkliste ein Modultyp ist. Dieses Checklistenmodul wird vom Kursleiter ausgewertet und kann basierend auf der Auswertung als &quot;Fehlgeschlagen&quot; oder &quot;Erfolg&quot; markiert werden.

In beiden Fällen wird der Status der Checkliste jedoch als Abgeschlossen und auf diese Weise als Abgeschlossen gekennzeichnet.

In dieser Version enthält die LO-API den Parameter *isChecklistObligatory*. Wenn der Wert &quot;True&quot; ist, ist die Checkliste obligatorisch.

### Unterstützung für mehrere Gebietsschemas

Ein Administrator kann jetzt den L1-Feedbackbericht in der Sprache seiner Wahl herunterladen. Sie können jedoch noch keine L1-Feedbackberichte für den Power BI herunterladen. Verwenden Sie in der API-Anforderung den Parameter &quot;preferLocale&quot;, um das gewünschte Gebietsschema anzugeben.

### Änderungen an der Zusammenfassung der Instanzenanzahl

Dies gilt für Konten, bei denen die Registrierungen für einen Klassenzimmer-/VC-Kurs mehr als 1000 betragen.

Wenn die Anzahl kleiner als 1000 ist, wird der Cache durch die Registrierungen ungültig und die aktualisierten Werte werden in einem API-Aufruf für die GET-Übersicht zurückgegeben, z. B. Anzahl der Registrierungen, Abschluss und seatLimit.

Wenn das Konto für diese Funktion aktiviert ist und die Anzahl der Registrierungen mehr als 1000 beträgt, werden die Werte aus dem Cache abgerufen.

### Veraltete Pfade

Derzeit folgen Learning Manager-APIs einer Diagrammdatenstruktur, mit der Sie Daten abrufen können, indem Sie das API-Modell durch Includes durchlaufen. Auch wenn Sie eine API auf bis zu sieben Ebenen durchlaufen könnten, ist das Abrufen der Daten mit einem einzigen API-Aufruf rechnerisch kostspielig.

Wir empfehlen allen bestehenden und neuen Kunden, mehrmals anstatt eines einzigen großen Anrufs kleine Anrufe zu tätigen. Dadurch wird verhindert, dass unerwünschte Daten in den Aufruf geladen werden.

#### Welche Pfade veraltet sind

Die folgenden Pfade sind veraltet:

* /learningObjects
   * Veraltete Pfade:
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Bestehende Pfade:
      * enrollment.loInstance
      * instances.loResources
* /learningObjects/{id}
   * Veralteter Pfad:
      * enrollment.instances.subLoInstances.learningObject
   * Vorhandener Pfad:
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

### Änderungen an der Archivierung des Anmeldezugriffs und Benutzerprüfungsberichts für die Job-API

Mit dieser Version wird der Anmeldezugriffsbericht für die Job-API bis zu fünf Quartale und der Benutzerprüfbericht sechs Monate lang gespeichert. Wenn Sie die Daten herunterladen möchten, die älter als dieser Zeitraum sind, müssen Sie den Archivparameter übergeben und Quartal und Jahr angeben. Siehe die Beispiel-Nutzlast.

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

Wenn Sie versuchen, die Datei **Anmeldezugriff** -Bericht, der über fünf Quartale hinausgeht, wird eine Fehlermeldung angezeigt. Eine ähnliche Fehlermeldung wird angezeigt, wenn Sie versuchen, die Datei **Benutzerüberwachung** Bericht, der mehr als sechs Monate dauert.

### Veraltete APIs

Anzeigen [API-Veraltungen im Adobe Learning Manager](api-deprecations-list.md) für eine kumulative Liste aller veralteten APIs im Produkt.

## In diesem Update behobene Fehler {#bug-fixes}

* Wenn ein Teilnehmer für einen Kurs registriert wird und dann versucht, sich für einen anderen Kurs zu registrieren, wird eine Warnmeldung angezeigt.
* Eine Benutzergruppe ist auch nach dem Löschen in der Suche sichtbar.
* Wenn Benutzer viele Teilnehmertranskripte mit einer großen Datenmenge auslösen, wird die Warteschlange für Teilnehmertranskripte blockiert und eine neue Anforderung wird verhindert.
* Wenn ein untergeordnetes Konto sein übergeordnetes Konto auffordert, einen Bericht freizugeben, ist das übergeordnete Konto nicht in der Lage, dies zu tun.
* Die URLs eines Kurses und eines Lernpfads werden an falsche Speicherorte umgeleitet.
* Ein Teilnehmer zeigt gelegentlich die Kursinstanz eines anderen Kurses an, wenn er auf den Kurslink auf der Katalogseite klickt.
* Die **Registrierung aufheben** wird nach der ersten Registrierung nicht wie erwartet angezeigt, aber die Schaltfläche wird nach einer Aktualisierung angezeigt.
* Sie können Inhalt oder ein Quiz, dessen Name einen Leerraum enthält, nicht speichern.
* Bei vom Manager genehmigten Kursen können Sie Teilnehmer in einer Benutzergruppe erneut registrieren.
* Wenn Sie versuchen, ein zusätzliches aktives Feld hinzuzufügen, wird in einigen Fällen die Fehlermeldung &quot;Aktive Felder konnten nicht gespeichert werden.&quot; angezeigt.
* Der Text im Namen eines Kurses innerhalb einer Kurskarte im Abschnitt &quot;Verwandte Kurse&quot; fließt über.
* Nachdem Sie eine Instanz gewechselt und einen Teilnehmer für die Instanz registriert haben, sind die alten Instanzen weiterhin im Outlook-Kalender vorhanden.
* Wenn ein Teilnehmer aus einem Peer-Konto versucht, die Miniaturansicht eines Kurses auszuwählen, wird eine Fehlermeldung angezeigt.
* Wenn Teilnehmer sich für einen Kurs registrieren, erhalten sie mehrere Benachrichtigungen zur Registrierung.
* Wenn ein Benutzer den Namen der in einem Connector erstellten Kataloge manuell ändert, werden neue Kataloge erstellt und die Kurse in den falschen Katalogen veröffentlicht.
* Benutzer mit inaktiven Konten erhalten weiterhin Abonnement-E-Mails.

### API-bezogene Fehlerbehebungen

* API-GET rufen die Details zu einem Manager nicht ab.
* In einem Konto wurden Benutzer während einer geplanten Ausfallzeit durch einen geplanten FTP-Benutzerimport erstellt.
* Wenn Sie in der mobilen App oder im immersiven Modus eine Kursinstanz löschen oder einstellen und die nächste aktive Instanz auswählen, wird das Dialogfeld &quot; **Interesse registrieren** wird anstelle von **Registrieren**.
* Wenn ein Teilnehmer aus einem Peer-Konto versucht, die Miniaturansicht eines Kurses mithilfe der Lernobjekt-API auszuwählen, wird der Fehler 403 Verboten angezeigt.

## Systemanforderungen

Anzeigen [Systemanforderungen für Adobe Learning Manager](system-requirements.md).

## Frühere Versionen von Adobe Learning Manager

* [Version November 2023](whats-new-november-2023.md)
* [Version Juli 2023](whats-new-2023-july.md)

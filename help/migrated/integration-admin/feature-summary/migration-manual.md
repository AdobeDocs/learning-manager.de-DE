---
description: Referenzhandbuch für Integrationsadministratoren zum Migrieren eines vorhandenen LMS in das Learning Manager-LMS.
jcr-language: en_us
title: Migrationshandbuch
exl-id: bfdd5cd8-dc5c-4de3-8970-6524fed042a8
source-git-commit: 0a5c51c6d56de2c9e2404ba6ddac5a82a62174a5
workflow-type: tm+mt
source-wordcount: '3614'
ht-degree: 73%

---

# Migrationshandbuch

Referenzhandbuch für Integrationsadministratoren zum Migrieren eines vorhandenen LMS in das Learning Manager-LMS

<!-- ## Overview {#overview} -->

## Anwendungsszenario {#usagescenario}

Im Allgemeinen verfügen große Unternehmen bereits über ein internes oder extern bereitgestelltes LMS. Ein LMS umfasst die Schulungsinhalte und -daten des Unternehmens. Wenn Sie als Unternehmen den Learning Manager erwerben, möchten Sie möglicherweise Ihre vorhandenen LMS-Inhalte und -Daten in den Learning Manager verschieben, damit Sie die Vorteile eines modernen und intuitiven LMS nutzen können, ohne ältere Daten Ihres Unternehmens zu verlieren.

Learning Manager bietet die erforderlichen Tools und Spezifikationen, mit denen der Integrationsadministrator des Unternehmens die Migrationsaufgaben einrichten und durchführen kann.

Von heute an können Administratoren des Unternehmens auf die Migrationsfunktion in Learning Manager zugreifen, indem sie sich an das Support-Team von Adobe wenden. Um die Migrationsfunktion in Ihrem Konto zu aktivieren, können Sie sich an das Adobe Learning Manager-Supportteam wenden.

## Migrationsvorgang {#apidescription}

In diesem Abschnitt werden die Voraussetzungen für die Migration, die wichtigsten Schritte des Migrationsvorgangs, Sprints, Spezifikationen und Schritte zur Daten- und Inhaltsmigration wie folgt erläutert:

### Voraussetzungen {#prerequisites}

Das Learning Manager-Team erwartet, dass folgende Aufgaben vor der Migration vom Integrationsadministrator des Unternehmens durchgeführt werden:

* Der Integrationsadministrator extrahiert die Daten und Inhalte des vorhandenen LMS und konvertiert sie in die von Learning Manager angegebenen Dateiformate.
* Der Import von Benutzern als Teil des Migrationsvorgangs wird von Learning Manager nicht unterstützt; es wird erwartet, dass diese vom Unternehmen mithilfe von Connectors importiert werden. Adobe System erwartet, dass diese Connectors vor dem Migrationsvorgang konfiguriert werden. Siehe [Hilfe zu Learning Manager-Connectors](connectors.md) für weitere Informationen.

In Learning Manager wird Administratoren empfohlen, den Migrationsvorgang in einem Testkonto auszuprobieren, bevor Daten und Inhalte zur Learning Manager-Produktionsumgebung migriert werden.

### Wichtige Schritte des Migrationsvorgangs {#keystepsofmigrationprocess}

Im Folgenden finden Sie wichtige Schritte für die Migration von Inhalten und Daten aus einem vorhandenen LMS zu Learning Manager:

1. Der Integrationsadministrator oder Partner ermittelt die Daten und -inhalte des bestehenden LMS, die migriert werden sollen.
1. Der Integrationsadministrator prüft die Tools und Spezifikationen, die Learning Manager zum Erfassen von Daten und Inhalten bereitstellt.
1. Der Integrationsadministrator schreibt einen Code oder führt entsprechende manuelle Aufgaben durch, um die Schulungsdaten und -inhalte basierend auf den Funktionen des älteren LMS zu exportieren.
1. Sobald die Schulungsdaten und -inhalte verfügbar sind, werden sie vom Integrationsadministrator analysiert und den entsprechenden Migrationsspezifikationen von Learning Manager zugeordnet.
1. Der Integrationsadministrator migriert die Daten und Inhalte mithilfe der vom Learning Manager bereitgestellten Tools in der folgenden Reihenfolge:

   1. Übertragen von Teilnehmenden zu Learning Manager
   1. Schulungsinhalte in Learning Manager übertragen und
   1. Übertragen von Schulungsdaten in Learning Manager

Das Learning Manager-LMS kann jetzt samt der alten Inhalte vom Unternehmen genutzt werden.

### Gültigkeitsbereich von Migrationsobjekten {#scopeofmigrationobjects}

Sie können Inhalte nur für die folgenden Lernobjekte migrieren:

* Modul
* Abzeichen
* Kurs
* Modulversion
* Kursinstanz
* Kursmodul
* Kenntnisse
* Kenntnisstand
* Kenntniskurs
* Zertifizierung
* Zertifizierungskurs
* Zertifizierung bestimmen
* Lernprogramm
* Lernprogrammkurs
* Lernprogramminstanz
* Lernprogrammkursinstanz
* Arbeitshilfe
* Version der Arbeitshilfe
* Kurs der Arbeitshilfe
* Von der Arbeitshilfe vermittelte Kenntnisse
* Registrierung
* Zertifizierungseinschreibung
* Lernprogrammeinschreibung
* Registrierung für Arbeitshilfe
* Benutzerkursbewertungen



### Wichtige Migrationskonzepte {#keyconceptsofmigration}

Einige der Schlüsselkonzepte des Lern-Manager-Migrationsprozesses werden im Folgenden kurz für Ihre Kurzanleitung erläutert:

**Migrationsprojekt**

Ein Migrationsprojekt in Learning Manager besteht aus mindestens einem Sprint. Ein Konto kann mehrere Migrationsprojekte umfassen. Der Migrationsvorgang in Learning Manager beginnt mit der Erstellung des Migrationsprojekts.

**Sprint**

Im Rahmen des Learning Manager-Migrationsvorgangs ist ein Sprint definiert als eine Reihe von Migrationselementen, die zur Migration aus einem bestehenden LMS ausgewählt wurden. Bei einem Migrationselement kann es sich um ein Kursmodul, Teilnehmerdatensätze oder eine Reihe von Kursen handeln. Ein Sprint kann mehrere Schulungsdatenelemente umfassen. Migrationsaufträge können in jedem Sprint durchgeführt werden.

**Sprint-Ausführungen**

Sprint-Ausführung bezeichnet das Starten einer Migrationsaufgabe. Sie können die Sprint-Ausführung jederzeit während des Vorgangs unterbrechen.

**Erneute Sprint-Ausführungen**

Sie können einen Migrations-Sprint nach Abschluss jederzeit erneut ausführen. Diese erneute Ausführung eines Sprints erfolgt, wenn Sie die Daten an ein Sprint-Element anhängen und dieses erneut in die Anwendung migrieren oder die Fehler in CSVs beheben möchten.

**CSV-Spezifikation**

Learning Manager bietet Ihnen eine Reihe von [CSV-Standardvorlagen](migration-manual.md#main-pars_header_140933605). Es empfiehlt sich, diese CSV-Spezifikationen vor Beginn des Migrationsvorgangs durchzugehen. Der Integrationsadministrator des Unternehmens kann die vorhandenen Datenformate analysieren und den entsprechenden vom Learning Manager bereitgestellten CSV-Vorlagenelementen zuordnen.

**Migrationsprojekt-Tags**

Adobe Systems empfiehlt, einige Suchbegriffe als Tags zu verwenden, um die Migrationsprojekte innerhalb von Learning Manager einfach wiederzufinden. Anhand dieser Tags können Sie Ihre Projekte in der Learning Manager-Anwendung jederzeit intern identifizieren.

**Modul ohne Inhalt**

Mit Learning Manager können Sie Module ohne Inhalt hochladen. Adobe Systems sieht es als Modul ohne Inhalt in Learning Manager an. In einem Szenario, bei dem Sie einige der älteren Daten von Ihrem vorhandenen LMS migrieren möchten, ohne dass Inhalte benötigt werden, können Sie die Datei module_version.csv ohne URL-Referenz hochladen.

## CSV-Spezifikationen und Beispiel-CSVs {#csv}

Im Folgenden finden Sie die CSV-Standardspezifikationen, die zur Verknüpfung mit Ihren vorhandenen LMS-Migrationsdaten verwendet werden können. Klicken Sie auf „CSV-Spezifikationen und Beispiel-CSVs“ („csv-templates“ und sample-csvs“) und laden Sie die ZIP-Dateien herunter. In der heruntergeladenen Datei „csv-specifications.zip“ sind sieben Excel-Dateien enthalten. Diese Excel-Dateien sind Spezifikationen mit Beschreibungen zum Ausfüllen von CSV-Dateien. Die entsprechenden CSV-Dateien sollten die Daten für jedes Feld im vordefinierten Format enthalten (wie in diesen XLSX-Dateien beschrieben).

<table border="1" cellspacing="0" cellpadding="0" width="100%">
 <tbody>
  <tr>
   <th>
    <p><b>Sl.no</b></p></th>
   <th>
    <p><b>Dateiname</b></p></th>
   <th>
    <p><b>Beschreibung des Inhalts</b></p></th>
   <th>
    <p>Hinweise</p></th>
  </tr>
  <tr>
   <td>
    <p>1</p></td>
   <td>
    <p>module.xlsx</p></td>
   <td>
    <p>Metadaten für module.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>2</p></td>
   <td>
    <p>badge.xlsx</p></td>
   <td>
    <p>Metadaten für badge.xlsx</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>3</p></td>
   <td>
    <p>course.xlsx</p></td>
   <td>
    <p>Metadaten für course.csv</p></td>
   <td>
    <p>Es empfiehlt sich, für einen bestimmten Kurs den Namen nur eines Autos zu verwenden, da mehrere Namen nach der Migration in der Anwendung nicht genau angezeigt werden. </p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>module_version.xlsx </p></td>
   <td>
    <p>Metadaten für module_version.csv</p></td>
   <td>
    <p>Achten Sie darauf, den URL-Pfad des Ordners für das Box-Konto anzugeben, in den Sie den Inhalt hochgeladen haben. </p></td>
  </tr>
  <tr>
   <td>
    <p>5</p></td>
   <td>
    <p>course_instance.xlsx</p></td>
   <td>
    <p>Metadaten für course_instance.csv </p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>6</p></td>
   <td>
    <p>session.xlsx</p></td>
   <td>
    <p>Metadaten für session.csv</p></td>
   <td>
    <p>Stellen Sie sicher, dass jeder Eintrag in der Sitzungs-CSV mindestens einem Klassenzimmer-/virtuellen Klassenzimmermodul zugeordnet ist</p></td>
  </tr>
  <tr>
   <td>
    <p>7</p></td>
   <td>
    <p>course_module.xlsx</p></td>
   <td>
    <p>Metadaten für course_module.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>8</p></td>
   <td>
    <p>skill.xlsx</p></td>
   <td>
    <p>Metadaten für skill.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>9</p></td>
   <td>
    <p>skill_level.xlsx</p></td>
   <td>
    <p>Metadaten für skill_level.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>10</p></td>
   <td>
    <p>skill_course.xlsx</p></td>
   <td>
    <p>Metadaten für skill_course.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>11</p></td>
   <td>
    <p>certification.xlsx</p></td>
   <td>
    <p>Metadaten für Certification.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>12</p></td>
   <td>
    <p>certification_course.xlsx</p></td>
   <td>
    <p>Metadaten für certification_course.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>13</p></td>
   <td>
    <p>certification_commit.xlsx</p></td>
   <td>
    <p>Metadaten für certification_commit.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>14</p></td>
   <td>
    <p>learning_program.xlsx</p></td>
   <td>
    <p>Metadaten für learning_program.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>15</p></td>
   <td>
    <p>learning_program_course.xls </p></td>
   <td>
    <p>Metadaten für learning_program_course.csv </p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>16</p></td>
   <td>
    <p>learning_program_instance.xlsx </p></td>
   <td>
    <p>Metadaten für learning_program_instance.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>17</p></td>
   <td>
    <p>learning_program_instance_course_instance.xlsx </p></td>
   <td>
    <p>Metadaten für learning_program_instance_course_instance.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>18</p></td>
   <td>
    <p>job_aid.xlsx</p></td>
   <td>
    <p>Metadaten für job_aid.csv</p></td>
   <td>
    <p>Für jede migrierte job_aid müssen eine oder mehrere job_aid-Versionen vorhanden sein.</p></td>
  </tr>
  <tr>
   <td>
    <p>19</p></td>
   <td>
    <p>Job_aid_version.xlsx</p></td>
   <td>
    <p>Metadaten für job_aid_version.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>20</p></td>
   <td>
    <p>job_aid_course.xlsx</p></td>
   <td>
    <p>Metadaten für job_aid_course.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>21</p></td>
   <td>
    <p>job_aid_skills.xlsx</p></td>
   <td>
    <p>Metadaten für job_aid_skills.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>22</p></td>
   <td>
    <p>enrollments.xlsx</p></td>
   <td>
    <p>Metadaten für enrollments.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>23</p></td>
   <td>
    <p>certification_enrollement.xlsx</p></td>
   <td>
    <p>Metadaten für certification_enrollement.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>24</p></td>
   <td>
    <p>learning_program_enrollment.xlsx</p></td>
   <td>
    <p>Metadaten für learning_program_enrollment.csv<br><br></p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>25</p></td>
   <td>
    <p>job_aid_enrollment.xlsx</p></td>
   <td>
    <p>Metadaten für job_aid_enrollment.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>26</p></td>
   <td>
    <p>user_course_grade.xlsx</p></td>
   <td>
    <p><br>
      Metadaten für user_course_grade.csv</p></td>
   <td>
    <p>Ebenso empfiehlt es sich, die erforderlichen Teilnehmer-Datensatzdaten in der CSV-Datei bereitzustellen, auch wenn sie nicht erforderlich sind. Selbst wenn die CSV-Datei für die Migration verarbeitet wird, kann die Learning Manager-Anwendung ohne diese Informationen möglicherweise keine Daten darstellen. In der Datei „sample-csvs.zip“ sind sieben CSV-Dateien mit einer ähnlichen Namenskonvention wie oben enthalten.</p></td>
  </tr>
 </tbody>
</table>

Learning Manager unterstützt nur Datums- und Zeitwerte im UTF-8- und 32-Bit-Format. Während der Migration werden möglicherweise Fehler angezeigt, wenn Sie in CSV-Dateien ein Datum außerhalb des zulässigen Bereichs angeben (z. B. 2038-07-17T08).:53:21.000Z oder 1980-04-17T08:13:25,322 Z.

* [sample-csvs.zip](assets/sample-csvs.zip)
* [csv_specifications.zip](assets/csv-specifications.zip)

Sie müssen die folgenden Abhängigkeiten für CSV-Dateien während des Imports berücksichtigen:

* „module_version.csv“ ist von „module.csv“ abhängig
* „course_instance.csv“ ist von „course.csv“ abhängig
* „course_module.csv“ ist von „course.csv“, „module.csv“ und „module_version.csv“ abhängig
* „course_instance.csv“ ist von „course.csv“ abhängig
* session.csv ist von „course.csv“ und „module.csv“ abhängig
* „enrollment.csv“ ist von „course.csv“ abhängig
* „user_course_grade.csv“ ist von „course.csv“ und „module.csv“ abhängig
* „skill_course.csv“ ist von „course.csv“ abhängig
* skill_level.csv skill.csv abhängig ist
* learning_program_instance.csv ist vom learning_program und learning_program_course.csv abhängig
* learning_program_course.csv learning_program.csv abhängig ist
* learning_program_enrollment.csv ist vom learning_program und learning_program_instance.csv abhängig
* learning_program_instance_course_instance.csv ist von learning_program.csv, learning_program_instance.csv und course_instance.csv abhängig
* certification_course.csv ist von certification.csv und von course.csv abhängig
* certification_commit.csv ist von certification.csv und certification_course.csv abhängig
* certification_enrollment.csv ist von certification.csv, certification_course.csv und certification_enrollment.csv abhängig

## Migrationsverfahren {#migrationprocedure}

Bevor Sie mit dem Migrationsverfahren beginnen, sollten Sie die folgenden Punkte beachten:

* Innerhalb eines Kontos kann jeweils nur ein Migrationsprojekt aktiv sein. Innerhalb eines Projekts kann jeweils nur ein Sprint aktiv sein.
* Wurde der Migrationsvorgang gestartet, kann die entsprechende Ausführung nicht mehr rückgängig gemacht werden. Sie können jedoch jede beliebige Daten- oder Inhaltsmigration mithilfe der Löschoption der jeweiligen Funktion in Learning Manager rückgängig machen.
* Sobald das Migrationsprojekt beginnt, erhält es den Status &quot;Unter Migration&quot;. Während der Migration kann sich nur der Integrationsadministrator bei Learning Manager anmelden.

### Erstellen von FTP- und Box-Konten {#creatingftpandboxaccounts}

Ihr Migrationsprojekt zu planen, ist sehr wichtig. Es wird empfohlen, Ihre Projekte in mehrere Teile zu teilen und deutlich anzugeben, was Sie in den einzelnen Teilen migrieren möchten. Es kann auch ratsam sein, eine Überprüfung nach jedem Teil durchzuführen, um sicher zu gehen, dass die Daten in diesem Teil migriert wurden, anstelle einer Gesamtüberprüfungsphase am Ende des Projekts. Bevor Sie die Teile als Teil Ihres Migrationsprojekts starten, müssen Sie Daten und Inhalts-CSV-Dateien auf FTP- und Box-Server hochladen. Wenn Sie keine Konten für benutzerdefiniertes FTP und Box haben, können Sie sie erstellen.

<!--**Create FTP account**-->

<!--Click **[!UICONTROL Request for CSV FTP folder]**. A pop-up dialog appears prompting you to enter your e-mail id. Go through online instructions and create an FTP account. As soon as you create your account, you can view your migration project and sprint project folders in FTP. 

A sample snapshot of project files and folder of FTP is shown below for your reference. -->

<!--![](assets/exavault-migration-upload-folders.png)-->

**Box-Konto erstellen**

Erstellen Sie den Upload-Ordner für Inhalte in einem ähnlichen Vorgang wie beim Erstellen des FTP-Ordners. Klicken Sie im linken Bereich auf „Migration“ und dann unten auf der daraufhin angezeigten Seite auf „Anfordern“ für einen Upload-Ordner für Inhalte.

Sie erhalten eine E-Mail von Box mit einem Link zum freigegebenen Ordner. Wenn Sie über kein Box-Konto verfügen, klicken Sie auf „Registrieren“ und erstellen Sie ein Konto. Anweisungen zur Anmeldung werden an die E-Mail-ID des Integrations-Admins gesendet.

**Hochladen von Daten (CSV-Dateien) auf FTP- oder Box-Ordner**

Bevor Sie ein Migrationsprojekt erstellen, müssen Sie als Voraussetzung ein FTP- oder Box-Konto erstellen. In dieser Phase können Sie also ein Migrationsprojekt und einen Sprint in der Learning Manager-Anwendung erstellen.  Siehe **Migrationsverfahren für Daten und Inhalte** auf dieser Seite, um ein Migrationsprojekt zu erstellen.

Klicken Sie im FTP- bzw. Box-Konto auf den Namen Ihres Projektordners und anschließend auf den Sprint-Namen. Innerhalb des Sprint-Ordners können Sie die CSV-Datendateien hochladen, die migriert werden sollen. Klicken Sie zum Hochladen oben auf dem FTP- oder Box-Server auf die Schaltfläche Dateien hochladen und legen Sie die CSV-Dateien ab. In der Abbildung unten sehen Sie ein Referenzbeispiel nach dem Hochladen auf FTP.

<!--![](assets/exavault-upload.png)-->

Sie können zum Learning Manager-Migrationsprojekt zurückkehren, indem Sie auf **[!UICONTROL Aktualisieren]** &quot; und zeigen Sie alle in Ihrem Migrations-Sprint aufgelisteten CSV-Datentypen an.

**Schulungsinhalte in Inhaltsordner hochladen**

Laden Sie die Schulungsinhalte von Ihrem vorhandenen LMS auf Ihr Box-Konto hoch. Wenn Sie bereits das Migrationsprojekt und den Sprint erstellt haben, füllt das Box-Konto das Migrationsprojekt und den Sprint-Namen aus. Sie können die Inhalte im selben Pfad hochladen. Siehe **Migrationsverfahren für Daten und Inhalte** auf dieser Seite, um ein Migrationsprojekt zu erstellen.

Sie können die Inhaltsdateien per Drag &amp; Drop verschieben oder auf **[!UICONTROL Hochladen]** klicken und die Dateien auf dem Desktop auswählen. Bei Inhalten mit sehr großen Dateigrößen kann es zu Verzögerungen beim Hochladen der Dateien kommen. Abhängig von der Größe der Datei ist die zum Hochladen der Dateien auf Ihr Box-Konto benötigte Zeit unterschiedlich.

In der Abbildung unten sehen Sie ein Referenzbeispiel mit einem Box-Konto nach dem Hochladen von Inhalten:

![](assets/box-account.png)

*Dateien im Box-Konto*

Nachdem die Dateien auf Ihr Box-Konto hochgeladen wurden, stellen Sie sicher, dass Sie den relativen Pfad dieser Box-Inhaltsdatei in der Datei „module_version.csv“ angeben. Dies ist ein obligatorischer Schritt für Sie, um den Pfad des Modulinhalts anzugeben.

Wenn Sie sich bei den FTP- und Box-Servern angemeldet und den Inhalt hochgeladen haben, werden die CSV-Speicherorte wie in der Abbildung unten dargestellt in Learning Manager angezeigt.

![](assets/after-setup.jpg)

*CSV-Speicherorte im Box-Konto*

## Migrationsverfahren für Daten und Inhalte {#dataandcontentmigrationprocedure}

Das Verfahren zur Migration der LMS-Daten und -Inhalte Ihres Unternehmens auf Learning Manager wird im Folgenden erläutert:

Prüfen Sie die Voraussetzungen für den Migrationsprozess, bevor Sie mit der Migration beginnen. Siehe [CSV-Spezifikationen und CSV-Musterdateien](migration-manual.md#main-pars_header_140933605) &quot; auf dieser Seite und bereiten Sie die CSVs für die Daten- und Inhaltsmigration vor.

1. Melden Sie sich bei der Learning Manager-Anwendung als Integrationsadministrator an und klicken Sie auf **[!UICONTROL Migration]** im linken Bereich.

   Daraufhin wird die Startseite für Migrationsprojekte angezeigt. Wenn Ihr Unternehmen bereits Migrationsprojekte erstellt hat, können Sie auf dieser Seite eine Liste mit allen Migrationsprojekten anzeigen.

1. Klicken Sie in der rechten oberen Ecke der Seite auf **[!UICONTROL Neu]**, um ein Migrationsprojekt zu erstellen. Alternativ können Sie auf der Seite auf den Link **[!UICONTROL Migrationsprojekt erstellen]** klicken, um ein Migrationsprojekt zu erstellen. Daraufhin wird die Seite zum Erstellen eines Migrationsprojekts angezeigt.

   Wenn Sie noch keinen FTP-Ordner erstellt haben, werden Sie aufgefordert, einen FTP-Ordner im Konto zu erstellen. Dies ist ein obligatorischer Schritt, bevor Sie mit dem Erstellen eines Migrationsprojekts beginnen.

   ![](assets/create-project.png)
   *FTP-Ordner erstellen*

   Geben Sie den Projektnamen, das Projekt-Tag, den Kurskatalog und eine Beschreibung für Ihr Migrationsprojekt an. Klicken Sie auf **[!UICONTROL Erstellen]**.

   Ihre Migrationsdatenelemente werden mithilfe dieses Migrationsprojekt-Tags identifiziert. Wenn Sie über keinen bestimmten Kurskatalog verfügen, wählen Sie den Standardkatalog in der Dropdown-Liste aus. Alle Kurse, die mithilfe eines Migrationsprojekts migriert werden, sind im Katalog enthalten, den Sie in dieser Phase ausgewählt haben. Wenn Sie keinen Katalog auswählen, sind alle migrierten Kurse Teil des Standardkatalogs.

1. Die Seite der Sprint-Konfiguration wird angezeigt (siehe nachfolgende Abbildung). Sie müssen einen Sprint als Teil Ihres Migrationsprojekts erstellen. Wählen Sie einen Sprint-Namen aus und geben Sie eine kurze Beschreibung des Sprints an. Sie können „Ja“ auswählen, wenn Sie Inhalte als Teil dieses Sprints migrieren möchten. Klicken **[!UICONTROL Weiter]**.

   ![](assets/users-modified-sprint.png)
   *Sprint-Migration*

   Aktivieren Sie das Kontrollkästchen mit dem Titel **Benutzer wurden seit der letzten Ausführung hinzugefügt oder geändert**, um die Liste der Benutzer mit der Learning Manager-Anwendung zu synchronisieren. Wenn Sie den Inhalt und die Daten in die Learning Manager-Anwendung migrieren, ist dies unter Umständen nicht erforderlich. Wenn zwischen Ihrer früheren Sprint-Migration und der neuesten Sprint-Migration jedoch eine Zeitspanne liegt, wird empfohlen, die Liste der Benutzer zu synchronisieren. Bei diesem Schritt kann die Learning Manager-Datenbank mit Ihren LMS-Benutzern synchronisiert werden.

   Dieser Synchronisierungsschritt wird empfohlen, wenn die Dateien „enrollment.csv“ und „user_course_grade.csv“ migriert werden. Bei diesem Schritt kann die Learning Manager-Datenbank mit Ihrer Migrationsdatenbank synchronisiert werden und es wird sichergestellt, dass alle Benutzer, deren Datensätze im Sprint migriert werden sollen, in der Migrationsdatenbank zur Verfügung stehen.

1. Sie können die Sprint-Migration mit Ihren hochgeladenen Daten und Inhalten beginnen. Klicken **[!UICONTROL Aktualisieren]** , bevor Sie den Sprint-Run starten, um die FTP- und Inhaltsordner mit der Learning Manager-Anwendung zu synchronisieren.

   ![](assets/sprint1-filesupload.png)
   *Sprint-Migration starten*

   Klicken **[!UICONTROL Start]** oben rechts auf der Seite. Sie können auf **[!UICONTROL Stopp]** während des Sprint-Migrationsvorgangs jederzeit ändern, um die Sprint-Migration abzubrechen.

   Der Migrationsstatus wird für die jeweiligen Sprint-Datenelemente und -Inhalte angezeigt. Überprüfen Sie die Anzahl der erfolgreichen und fehlgeschlagenen Elemente als Teil des Sprint-Laufs der Migration.

   Stellen Sie beim Hochladen von Modulinhalten sicher, dass der Pfad des Inhaltsordners in der Datei „module_version.csv“ angegeben wird. Wenn Sie diesen Schritt versäumen, stellen Sie möglicherweise Fehler während der Migration fest. Wenn Sie beispielsweise Inhalte von Modulen zum Selbststudium (z. B. Videos) hochladen, müssen Sie den relativen Box-URL-Pfad in der Datei „module_version.csv“ angeben. Für Inhalte des Aktivitätsmoduls können Sie den URL-Namen festlegen.

   In der Abbildung unten sehen Sie ein Referenzbeispiel für den Fortschrittsdialog. Sie können die Anzahl der für jedes Migrationsdatenelement verarbeiteten Datensätze zusammen mit dem Status der erfolgreichen und fehlgeschlagenen Elemente sehen. Klicken Sie auf „Fehlerdatensätze für die fehlgeschlagenen Elemente herunterladen“, um die Fehlerprotokolle herunterzuladen und anzuzeigen. Sie können die Probleme in der CSV-Datei beheben und diese erneut auf FTP hochladen.

   ![](assets/sample-sprint-progress-status.png)
   *Sprint-Fortschritt anzeigen*

   Klicken Sie im linken Bereich auf die Sprint-Liste, wenn Sie die Liste aller Sprints eines Migrationsprojekts anzeigen möchten. Sie können eine Liste aller Sprints, die Anzahl der für jeden Sprint ausgeführten Läufe, das Startdatum, die Dauer und den Abschlussstatus anzeigen, wie in der Abbildung unten dargestellt.

   ![](assets/sprint-list.png)
   *Liste der Sprints anzeigen*

1. Nachdem Sie die neuesten aktualisierten CSV-Dateien hochgeladen haben, können Sie in der oberen rechten Ecke der Seite auf „Wiederholen“ klicken. Bei der Wiederholung werden alle Datenelemente noch einmal verarbeitet und Elemente ignoriert, für die es keine Änderungen gibt. Sobald Sie mit der Migration von Datenelementen in einem Sprint zufrieden sind, können Sie die Sprint-Migration als abgeschlossen markieren, indem Sie auf die Schaltfläche oben auf der Seite klicken. Sie können einen neuen Sprint mit mehr Datenelementen zu einem späteren Zeitpunkt starten. Sobald ein Sprint als abgeschlossen markiert wurde, können Sie ihn nicht erneut wiederholen. Dementsprechend kann ein Migrationsprojekt eine beliebige Anzahl von Sprints umfassen. Sobald Sie mit dem Migrationsstatus aller Sprints zufrieden sind, können Sie das Migrationsprojekt als abgeschlossen markieren, indem Sie auf **Projekt als abgeschlossen markieren** auf der Seite mit der Sprint-Liste.

   Bevor Sie das Migrationsprojekt als abgeschlossen markieren, müssen Sie sicherstellen, dass alle Sprints des Projekts abgeschlossen sind. Nachdem Sie das Migrationsprojekt als abgeschlossen markiert haben, können Sie nicht zurückgehen und Sprints in diesem Projekt erstellen oder Änderungen an diesem Projekt vornehmen. Sie müssen ein weiteres Migrationsprojekt erstellen und ihm Sprints hinzufügen.

## Migrationsverifizierung {#registration}

Nachdem Sie die Lerndaten und -inhalte aus dem älteren LMS Ihres Unternehmens migriert haben, können Sie die importierten Daten und Inhalte mit verschiedenen Lernobjektfunktionen überprüfen. Sie können sich beispielsweise bei der Learning Manager-Anwendung als Administrator anmelden und die Verfügbarkeit der Daten und Inhalte von importierten Modulen und Kursen überprüfen.

## Nachrüsten in der Migration {#retrofittinginmigration}

Mit dieser Integrationsfunktion können Sie historische Daten für ein Lernobjekt von einem veralteten Learning Management-System auf einen aktiven Kurs nachrüsten, der in Learning Manager erstellt wird.

Im Folgenden finden Sie die CSV-Standardspezifikationen, die zur Verknüpfung mit Ihren vorhandenen LMS-Migrationsdaten verwendet werden können. Klicken Sie auf „CSV-Spezifikationen und Beispiel-CSVs“ („csv-templates“ und sample-csvs“) und laden Sie die ZIP-Dateien herunter. In der heruntergeladenen Datei „csv-specifications.zip“ sind vier Excel-Dateien enthalten. Diese Excel-Dateien sind Spezifikationen mit Beschreibungen zum Ausfüllen von CSV-Dateien. Die entsprechenden CSV-Dateien sollten die Daten für jedes Feld im vordefinierten Format enthalten (wie in diesen XLSX-Dateien beschrieben).

 1-enrollment.xlsx-enthält Beschreibungen von Metadaten, die für die retrofit_enrollment.csv-Datei erforderlich sind.

2-certification_enrollment.xlsx enthält Beschreibungen von Metadaten, die für die retrofit_certification_enrollment.csv-Datei erforderlich sind.

3-learning_program_enrollment.xlsx enthält Beschreibungen von Metadaten, die für die retrofit_learning_program_enrollment.csv-Datei erforderlich sind.

4-user_course_grades.xlsx enthält Beschreibungen von Metadaten, die für die retrofit_user_course_grades.csv-Datei erforderlich sind.
[csv-specifications.zip](assets/csv-specifications.zip)

>[!NOTE]
>
>Die UUID (Universally Unique ID) ist ebenfalls eine Spalte in der Migrations-CSV.


## Fehlerbehebung für Migrationsprobleme {#troubleshootingmigrationissues}

[Klicken Sie hier](../../kb/troubleshooting-migration.md), um mehr über die Problemumgehung/Lösung für die Probleme zu erfahren, mit denen die für die Integration zuständigen Administratoren bei der Migration von Daten und Inhalten aus Ihrem vorhandenen LMS in die Learning Manager-Anwendung konfrontiert sind.

## Tipps zur Benutzerverwaltung {#usermanagement}

Unter diesem Thema finden Sie einige Tipps zum besseren Verständnis dazu, wie Benutzer in Learning Manager berücksichtigt und verwaltet werden. Diese Konzepte unterstützen Sie beim Optimieren der Verwaltung von Benutzern, während der Verwendung von CSV-Import, Connectors und Migrationsfunktionen von Learning Manager.

## Learning Manager-IDs {#captivateprimeids}

In Learning Manager stehen zwei Arten von eindeutigen IDs für Benutzer zur Verfügung:

* E-Mail
* UUID (Universally Unique ID)

Learning Manager unterstützt UUID, um Unternehmen Flexibilität beim Steuern von Benutzerkonten zu bieten. Wenn Sie über UUID von Benutzern in einem Konto verfügen, können Sie als Administrator die E-Mail-IDs der Benutzer für dieses Konto ändern.

**Anwendungsszenario für UUID in einem Unternehmen**

Stellen Sie sich ein Szenario vor, in dem ein Mitarbeiter A sich als Vertragsnehmer dem Unternehmen Learning Manager anschließt. Während der Vertragslaufzeit stellt das Learning Manager-Unternehmen möglicherweise keine Unternehmens-E-Mail-ID wie A@example.com zur Verfügung, sondern berücksichtigt stattdessen das persönliche E-Mail-Konto des Mitarbeiters, z. B. A@gmail.com. Nach Abschluss von 6 Monaten Vertragslaufzeit, wenn derselbe Mitarbeiter A sich dem Learning Manager als Vollzeitmitarbeiter anschließt, möchte der Learning Manager seine E-Mail-ID in eine Unternehmens-E-Mail-ID ändern: A@example.com.

UUID-Zugriff auf das Benutzerkonto ist für den Learning Manager des Unternehmens im oben genannten Szenario hilfreich. Das Unternehmen mit dem Learning Manager kann die persönliche E-Mail-ID des Mitarbeiters A ganz einfach durch eine offizielle E-Mail-ID ersetzen. Die für dieses Konto relevanten Datensätze für den Mitarbeiter sind von dieser Änderung nicht betroffen.

## Identifikation einzelner Benutzer {#singleuseridentification}

Learning Manager identifiziert und speichert, wie ein einzelner Benutzer hinzugefügt wird: über Selbstregistrierung, CSV-Upload oder durch Hinzufügen eines einzelnen Benutzers über die Benutzeroberfläche oder mithilfe einer API.

* Wenn ein einzelner Benutzer über die Benutzeroberfläche (UI) oder über die API hinzugefügt wird, können Sie solche Einzelbenutzer über die Benutzeroberfläche (UI) oder die API löschen.
* Sie können einzelne Benutzer über CSV-Upload-Prozesse aktualisieren, aber Sie müssen dabei beachten, dass diese einzelnen Benutzer als CSV-Benutzer behandelt werden und die CSV-Arbeitsabläufe für solche Benutzer gelten.

## Zuweisen der Manager-Rolle {#assigningmanagerrole}

Sie können eine Manager-Rolle nicht jedem Benutzer in Learning Manager direkt zuweisen. Ein Benutzer X kann nur ein Learning Manager Manager werden, wenn Sie ein Manager-Attribut für einen beliebigen Benutzer (z. B. Y) in diesem Konto als X festlegen.

Szenario: X ist der Manager der Benutzer A, B und C; wenn X das Unternehmen verlässt, müssen Sie sicherstellen, dass das Manager-Attribut für A, B und C auf den neuen Manager festgelegt wird. Alternativ dazu können Sie auch das Manager-Attribut für diese Benutzer vorübergehend als ROOT festlegen und später dem neuen Namen des Managers zuweisen.

Weitere Informationen zu diesem Thema finden Sie in den folgenden Hilfeinhalten:

* [Häufig gestellte Fragen zum Hochladen von CSV](/help/migrated/administrators/add-users-in-bulk.md)
* [Funktions-Hilfe für das Hinzufügen von Benutzern](/help/migrated/administrators/feature-summary/add-users-user-groups.md)

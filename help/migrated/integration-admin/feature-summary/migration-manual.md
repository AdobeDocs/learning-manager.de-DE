---
description: Referenzhandbuch für Integrationsadministratoren zum Migrieren eines vorhandenen LMS in das Learning Manager-LMS
jcr-language: en_us
title: Migrationshandbuch
source-git-commit: 66dfaaaf723382eada39e2be29dfd49b795107a0
workflow-type: tm+mt
source-wordcount: '3705'
ht-degree: 0%

---



# Migrationshandbuch

Referenzhandbuch für Integrationsadministratoren zum Migrieren eines vorhandenen LMS in das Learning Manager-LMS

## Übersicht {#overview}

<table>
 <tbody>
  <tr>
   <td><img src="assets/migration.jpg"></td>
   <td>
    <p><a href="https://business.adobe.com/products/learning-manager/adobe-learning-manager.html">Adobe Learning Manager</a> ist eine in der Cloud gehostete, auf die Kursteilnehmer zugeschnittene Selfservice-Lösung für Learning Management. Mit dem Adobe können Unternehmen mit den bestehenden Lernmanagementsystemen (LMS) die Schulungsdaten und -inhalte ihres Unternehmens in die LMS-Anwendung für Learning Manager migrieren. </p></td>
  </tr>
 </tbody>
</table>

### Anwendungsszenario {#usagescenario}

Im Allgemeinen verfügen große Unternehmen über ein internes oder extern bereitgestelltes LMS. Ein LMS umfasst die Schulungsinhalte und -daten des Unternehmens. Wenn Sie als Unternehmen den Learning Manager erwerben, möchten Sie möglicherweise Ihre vorhandenen LMS-Inhalte und -Daten in den Learning Manager verschieben, damit Sie die Vorteile eines modernen und intuitiven LMS nutzen können, ohne ältere Daten Ihres Unternehmens zu verlieren.

Learning Manager bietet die erforderlichen Tools und Spezifikationen, mit denen der Integrationsadministrator des Unternehmens die Migrationsaufgaben einrichten und ausführen kann.

Von heute an können Administratoren des Unternehmens auf die Migrationsfunktion im Lern-Manager zugreifen, indem sie sich an das Adobe-Support-Team wenden. Um die Migrationsfunktion in Ihrem Konto zu aktivieren, können Sie sich an das Support-Team für den Adobe Learning Manager wenden.

## Migrationsvorgang {#apidescription}

In diesem Abschnitt werden die Voraussetzungen für die Migration, die wichtigsten Schritte des Migrationsvorgangs, Sprints, Spezifikationen und Schritte zur Daten- und Inhaltsmigration wie folgt erläutert:

### Voraussetzungen {#prerequisites}

Das Learning Manager-Team erwartet, dass die folgenden Aufgaben vor der Migration von den Integrationsadministratoren Ihres Unternehmens ausgeführt werden:

* Der Integrationsadministrator extrahiert Daten und Inhalte aus dem vorhandenen LMS und konvertiert sie in die von Learning Manager definierten Dateiformate.
* Learning Manager unterstützt nicht das Importieren von Benutzern als Teil des Migrationsprozesses und erwartet, dass die Organisation Benutzer mithilfe von Connectors importiert. Adobe Systems erwartet, dass diese Connectors vor dem Migrationsvorgang konfiguriert werden. Siehe [Hilfe zu Learning Manager-Connectors](connectors.md) für weitere Informationen.

Learning Manager empfiehlt Administratoren können den Migrationsprozess in einem Testkonto testen, bevor die Daten und Inhalte in die Learning Manager-Produktionsumgebung migriert werden.

### Wichtige Schritte des Migrationsvorgangs {#keystepsofmigrationprocess}

Im Folgenden finden Sie wichtige Schritte für die Migration von Inhalten und Daten aus einem vorhandenen LMS zu Learning Manager:

1. Der Integrationsadministrator oder Partner prüft die vorhandenen LMS-Daten und -Inhalte, die migriert werden müssen.
1. Der Integrationsadministrator prüft die Tools und Spezifikationen, die Learning Manager zum Erfassen von Daten und Inhalten bereitstellt.
1. Der Integrationsadministrator schreibt einen Code oder führt entsprechende manuelle Aufgaben durch, um die Schulungsdaten und -inhalte basierend auf den Funktionen des älteren LMS zu exportieren.
1. Sobald die Schulungsdaten und -inhalte verfügbar sind, werden sie vom Integrationsadministrator analysiert und den entsprechenden Migrationsspezifikationen des Learning Managers zugeordnet.
1. Der Integrationsadministrator migriert die Daten und Inhalte mithilfe der vom Learning Manager bereitgestellten Tools in der folgenden Reihenfolge:

   1. Teilnehmer auf Learning Manager übertragen
   1. Schulungsinhalte in Learning Manager übertragen und
   1. Übernehmen Sie zum Schluss die Schulungsdaten an den Learning Manager.

Das Learning Manager-LMS kann jetzt vom Unternehmen zusammen mit den alten Inhalten verwendet werden.

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
* Kenntnisskurs
* Zertifizierung
* Zertifizierungskurs
* Zertifizierung bestätigen
* Lernprogramm
* Lernprogrammkurs
* Lernprogramminstanz
* Lernprogrammkursinstanz
* Arbeitshilfe
* Version der Arbeitshilfe
* Kurs zur Arbeitshilfe
* Qualifikationen der Arbeitshilfe
* Registrierung
* Zertifizierungseinschreibung
* Lernprogrammeinschreibung
* Registrierung für Arbeitshilfe
* Benutzerkursbewertungen



### Wichtige Migrationskonzepte {#keyconceptsofmigration}

Einige der Schlüsselkonzepte des Lern-Manager-Migrationsprozesses werden im Folgenden kurz für Ihre Kurzanleitung erläutert:

**Migrationprojekt**

Im Lern-Manager besteht ein Migrationsprojekt aus einem oder mehreren Sprints. Sie können auch mehrere Migrationsprojekte für Ihr Konto haben. Ihr Migrationsprozess im Learning Manager beginnt mit dem Erstellen eines Migrationsprojekts.

**Sprint**

Ein Sprint definiert im LMS-Migrationsprozess des Learning Managers eine Reihe von Migrationselementen, die Sie für die Migration aus dem vorhandenen LMS ausgewählt haben. Bei einem Migrationselement kann es sich um ein Kursmodul, Teilnehmerdatensätze oder eine Reihe von Kursen handeln. Ein Sprint kann mehrere Lerndatenelemente umfassen. Migrationsaufträge können in jedem Sprint ausgeführt werden.

**Sprint-Ausführungen**

Sprint-Ausführung bezeichnet das Starten eines Migrationsauftrags für einen Sprint. Sie können die Sprint-Ausführung jederzeit während der Ausführung beenden.

**Erneute Sprint-Ausführungen**

Sie können einen Migrations-Sprint nach Abschluss jederzeit erneut ausführen. Diese erneute Ausführung eines Sprints erfolgt, wenn Sie die Daten an ein Sprint-Element anhängen und dieses erneut in die Anwendung migrieren oder die Fehler in CSVs korrigieren möchten.

**CSV-Spezifikation**

Learning Manager bietet Ihnen eine Reihe von [CSV-Standardspezifikationen](migration-manual.md#main-pars_header_140933605). Es empfiehlt sich, diese CSV-Spezifikationen vor Beginn des Migrationsvorgangs durchzugehen. Der Integrationsadministrator des Unternehmens kann die vorhandenen Datenformate analysieren und den entsprechenden vom Learning Manager bereitgestellten CSV-Vorlagenelementen zuordnen.

**Migrationsprojekt-Tags**

Adobe Systems empfiehlt, einige Schlüsselwörter als Tags zu verwenden, um Ihre Migrationsprojekte innerhalb der Learning Manager-Anwendung einfach zu identifizieren. Mit diesen Tags können Sie Ihre Projekte in der Learning Manager-Anwendung jederzeit intern identifizieren.

**Modul ohne Inhalt**

Mit dem Learning Manager können Sie ein Modul ohne Inhalt hochladen. Adobe Systems betrachtet es als ein Modul ohne Inhalt im Learning Manager. In einem Szenario, in dem Sie einige der älteren Daten von Ihrem vorhandenen LMS migrieren möchten, ohne dass Inhalte benötigt werden, können Sie die Datei &quot;module_version.csv&quot; ohne URL-Referenz hochladen.

## CSV-Spezifikationen und CSV-Musterdateien {#csv}

Im Folgenden finden Sie die CSV-Standardspezifikationen, die zur Verknüpfung mit Ihren vorhandenen LMS-Migrationsdaten verwendet werden können. Klicken Sie auf &quot;CSV-Spezifikationen und Beispiel-CSV&quot;, um ZIP-Dateien herunterzuladen. Die heruntergeladene Datei &quot;csv-specifications.zip&quot; enthält sieben Excel-Dateien. Diese Excel-Dateien sind Spezifikationen mit Beschreibungen zum Ausfüllen von CSV-Dateien. Die entsprechenden CSV-Dateien sollten die Daten für jedes Feld im vordefinierten Format enthalten, wie in diesen XLSX-Dateien erläutert.

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
    <p>Ebenso empfiehlt es sich, die erforderlichen Teilnehmer-Datensatzdaten in der CSV-Datei bereitzustellen, auch wenn sie nicht erforderlich sind. Selbst wenn die CSV-Datei für die Migration verarbeitet wird, kann die Learning Manager-Anwendung ohne diese Informationen möglicherweise keine Daten darstellen. In der Datei "sample-csvs.zip" sind sieben CSV-Dateien mit einer ähnlichen Namenskonvention wie oben enthalten.</p></td>
  </tr>
 </tbody>
</table>

Learning Manager unterstützt nur Datums- und Zeitwerte im UTF-8- und 32-Bit-Format. Während der Migration werden möglicherweise Fehler angezeigt, wenn Sie in CSV-Dateien ein Datum außerhalb des zulässigen Bereichs angeben (z. B. 2038-07-17T08).:53:21.000Z oder 1980-04-17T08:13:25,322 Z.
[sample-csvs.zip](assets/sample-csvs.zip) [csv_specifications.zip](assets/csv-specifications.zip)Sie müssen die folgenden Abhängigkeiten für CSV-Dateien während des Imports berücksichtigen:

* &quot;module_version.csv&quot; ist von &quot;module.csv&quot; abhängig
* &quot;course_instance.csv&quot; ist von &quot;course.csv&quot; abhängig
* &quot;course_module.csv&quot; ist von &quot;course.csv&quot;, &quot;module.csv&quot; und &quot;module_version.csv&quot; abhängig
* &quot;course_instance.csv&quot; ist von &quot;course.csv&quot; abhängig
* session.csv ist von &quot;course.csv&quot; und &quot;module.csv&quot; abhängig
* &quot;enrollment.csv&quot; ist von &quot;course.csv&quot; abhängig
* user_course_grade.csv ist von &quot;course.csv&quot; und &quot;module.csv&quot; abhängig
* skill_course.csv course.csv abhängig ist
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

* Es kann immer nur ein Migrationsprojekt in einem Konto aktiv sein. Innerhalb eines Projekts kann jeweils nur ein Sprint aktiv sein.
* Eine Ausführung, die sich bereits im Migrationsvorgang befindet, kann nicht rückgängig gemacht werden. Sie können jedoch jede beliebige Daten- oder Inhaltsmigration mithilfe der Löschoption in jeder Funktion des Learning Managers rückgängig machen.
* Sobald das Migrationsprojekt beginnt, erhält es den Status &quot;Unter Migration&quot;. Während der Migration kann sich nur der Integrationsadministrator beim Learning Manager anmelden.

### Erstellen von FTP- und Box-Konten {#creatingftpandboxaccounts}

Die Planung Ihres Migrationsprojekts ist sehr wichtig. Es wird empfohlen, dass Sie Ihre Projekte in mehrere Teile teilen und deutlich angeben, was Sie in jedem Teil migrieren möchten. Es kann sogar sinnvoll sein, nach jedem Teil eine Prüfung durchzuführen, um sicher zu gehen, dass die Daten in diesem Teil migriert wurden, anstatt eine Prüfung am Ende des Projekts durchzuführen. Bevor Sie den Sprint als Teil Ihres Migrationsprojekts starten, müssen Sie Daten- und Inhalts-CSV-Dateien auf FTP- bzw. Box-Server hochladen. Wenn Sie keine Konten für benutzerdefiniertes FTP und Box haben, können Sie sie erstellen.

**FTP-Konto erstellen**

Klicken **[!UICONTROL CSV-FTP-Ordner anfordern]**. Ein Popup-Dialogfeld wird angezeigt, in dem Sie zur Eingabe Ihrer E-Mail-ID aufgefordert werden. Lesen Sie die Online-Anweisungen und erstellen Sie ein FTP-Konto. Sobald Sie Ihr Konto erstellt haben, können Sie die Ordner für Ihre Migrations- und Sprint-Projekte auf FTP anzeigen.

In der Abbildung unten sehen Sie ein Referenzbeispiel für Projektdateien und FTP-Ordner.

<!--![](assets/exavault-migration-upload-folders.png)-->

**Box-Konto erstellen**

Erstellen Sie den Upload-Ordner für Inhalte in einem ähnlichen Vorgang wie beim Erstellen des FTP-Ordners. Klicken Sie im linken Bereich auf Migration und dann unten auf der angezeigten Seite auf Upload-Ordner für Inhalte anfordern .

Sie erhalten eine E-Mail von Box mit einem Link zum freigegebenen Ordner. Wenn Sie kein Box-Konto haben, klicken Sie auf Registrieren und erstellen Sie ein Konto. Anmeldeanweisungen werden an die E-Mail-ID des Integrationsadministrators gesendet.

**Hochladen von Daten (CSV-Dateien) auf FTP- oder Box-Ordner**

Bevor Sie ein Migrationsprojekt erstellen, müssen Sie als Voraussetzung ein FTP- oder Box-Konto erstellen. In dieser Phase können Sie also ein Migrationsprojekt und einen Sprint in der Learning Manager-Anwendung erstellen.  Siehe **Migrationsverfahren für Daten und Inhalte** auf dieser Seite, um ein Migrationsprojekt zu erstellen.

Klicken Sie im FTP- oder Box-Konto auf den Namen Ihres Projektordners und dann auf den Sprint-Namen. Innerhalb des Sprint-Ordners können Sie die CSV-Datendateien hochladen, die migriert werden sollen. Klicken Sie zum Hochladen oben auf dem FTP- oder Box-Server auf die Schaltfläche Dateien hochladen und legen Sie die CSV-Dateien ab. In der Abbildung unten sehen Sie ein Referenzbeispiel nach dem Hochladen auf FTP.

<!--![](assets/exavault-upload.png)-->

Sie können zum Learning Manager-Migrationsprojekt zurückkehren, indem Sie auf **[!UICONTROL Aktualisieren]** &quot; und zeigen Sie alle in Ihrem Migrations-Sprint aufgelisteten CSV-Datentypen an.

**Schulungsinhalte in Inhaltsordner hochladen**

Laden Sie die Schulungsinhalte Ihres vorhandenen LMS auf Ihr Box-Konto hoch. Wenn Sie das Migrationsprojekt und den Sprint bereits erstellt haben, füllt das Box-Konto das Migrationsprojekt und den Sprint-Namen aus. Sie können den Inhalt im selben Pfad hochladen. Siehe **Migrationsverfahren für Daten und Inhalte** auf dieser Seite, um ein Migrationsprojekt zu erstellen.

Sie können die Inhaltsdateien ziehen und ablegen oder auf **[!UICONTROL Hochladen]** und wählen Sie die Dateien auf Ihrem Desktop aus. Bei Inhalten mit sehr großen Dateigrößen kann es zu Verzögerungen beim Hochladen der Dateien kommen. Abhängig von der Größe der Datei ist die zum Hochladen der Dateien auf Ihr Box-Konto benötigte Zeit unterschiedlich.

In der Abbildung unten sehen Sie ein Referenzbeispiel mit einem Box-Konto nach dem Hochladen von Inhalten:

![](assets/box-account.png)

*Dateien im Box-Konto*

Nachdem die Dateien in Ihr Box-Konto hochgeladen wurden, stellen Sie sicher, dass Sie den relativen Pfad dieser Box-Inhaltsdatei in der Datei &quot;module_version.csv&quot; angeben. Dies ist ein obligatorischer Schritt für Sie, um den Pfad des Modulinhalts anzugeben.

Sobald Sie sich bei den FTP- und Box-Servern angemeldet und den Inhalt hochgeladen haben, werden die CSV-Speicherorte wie in der Momentaufnahme unten im Lern-Manager angezeigt.

![](assets/after-setup.jpg)

*CSV-Speicherorte im Box-Konto*

## Migrationsverfahren für Daten und Inhalte {#dataandcontentmigrationprocedure}

Das Verfahren zur Migration der LMS-Daten und -Inhalte Ihres Unternehmens auf Learning Manager wird im Folgenden erläutert:

Prüfen Sie die Voraussetzungen für den Migrationsprozess, bevor Sie mit der Migration beginnen. Siehe [CSV-Spezifikationen und CSV-Musterdateien](migration-manual.md#main-pars_header_140933605) &quot; auf dieser Seite und bereiten Sie die CSVs für die Daten- und Inhaltsmigration vor.

1. Melden Sie sich bei der Learning Manager-Anwendung als Integrationsadministrator an und klicken Sie auf **[!UICONTROL Migration]** im linken Bereich.

   Die Startseite für Migrationsprojekte wird angezeigt. Wenn Ihre Organisation bereits Migrationsprojekte erstellt hat, können Sie auf dieser Seite eine Liste aller Migrationsprojekte anzeigen.

1. Klicken **[!UICONTROL Neu]** in der oberen rechten Ecke der Seite, um ein Migrationsprojekt zu erstellen. Alternativ können Sie auf **[!UICONTROL Migrationsprojekt erstellen]** , um ein Migrationsprojekt zu erstellen. Daraufhin wird die Seite zum Erstellen eines Migrationsprojekts angezeigt.

   Wenn Sie noch keinen FTP-Ordner erstellt haben, werden Sie aufgefordert, einen FTP-Ordner im Konto zu erstellen. Dies ist ein obligatorischer Schritt, bevor Sie mit dem Erstellen eines Migrationsprojekts beginnen.

   ![](assets/create-project.png)
   *FTP-Ordner erstellen*

   Geben Sie den Projektnamen, das Projekt-Tag, den Kurskatalog und eine Beschreibung für Ihr Migrationsprojekt an. Klicken **[!UICONTROL Erstellen]**.

   Ihre Migrationsdatenelemente werden anhand dieses Migrationsprojekt-Tags identifiziert. Wenn Sie über keinen bestimmten Kurskatalog verfügen, wählen Sie den Standardkatalog in der Dropdown-Liste aus. Alle Kurse, die Sie mit einem Migrationsprojekt migrieren, werden in den Katalog aufgenommen, den Sie in dieser Phase auswählen. Wenn Sie keinen Katalog auswählen, sind alle migrierten Kurse Teil des Standardkatalogs.

1. Die Seite zur Sprint-Konfiguration wird angezeigt (siehe nachfolgende Abbildung). Sie müssen einen Sprint als Teil Ihres Migrationsprojekts erstellen. Wählen Sie einen Sprint-Namen aus und geben Sie eine kurze Beschreibung des Sprints an. Sie können &quot;Ja&quot; auswählen, wenn Sie Inhalte als Teil dieses Sprints migrieren möchten. Klicken **[!UICONTROL Weiter]**.

   ![](assets/users-modified-sprint.png)
   *Sprint-Migration*

   Aktivieren Sie das Kontrollkästchen mit dem Titel **Benutzer wurden seit der letzten Ausführung hinzugefügt oder geändert**, um die Liste der Benutzer mit der Learning Manager-Anwendung zu synchronisieren. Wenn Sie die Inhalte und Daten in die Learning Manager-Anwendung migrieren, ist dies möglicherweise nicht erforderlich. Wenn zwischen Ihrer früheren Sprint-Migration und der neuesten Sprint-Migration jedoch eine Zeitspanne liegt, wird empfohlen, die Liste der Benutzer zu synchronisieren. Bei diesem Schritt kann die Learning Manager-Datenbank mit Ihren LMS-Benutzern synchronisiert werden.

   Dieser Synchronisierungsschritt wird empfohlen, wenn die Dateien &quot;enrollment.csv&quot; und &quot;user_course_grade.csv&quot; migriert werden. Mit diesem Schritt kann die Lern-Manager-Datenbank mit Ihrer Migrationsdatenbank synchronisiert werden und es wird sichergestellt, dass alle Benutzer, deren Datensätze im Sprint migriert werden sollen, in der Migrationsdatenbank verfügbar sind.

1. Sie können die Sprint-Migration mit Ihren hochgeladenen Daten und Inhalten starten. Klicken **[!UICONTROL Aktualisieren]** , bevor Sie den Sprint-Run starten, um die FTP- und Inhaltsordner mit der Learning Manager-Anwendung zu synchronisieren.

   ![](assets/sprint1-filesupload.png)
   *Sprint-Migration starten*

   Klicken **[!UICONTROL Start]** oben rechts auf der Seite. Sie können auf **[!UICONTROL Stopp]** während des Sprint-Migrationsvorgangs jederzeit ändern, um die Sprint-Migration abzubrechen.

   Der Migrationsstatus wird für alle Sprint-Datenelemente und -Inhalte angezeigt. Überprüfen Sie die Anzahl der erfolgreichen und fehlgeschlagenen Elemente als Teil des Sprint-Laufs der Migration.

   Wenn Sie Modulinhalte hochladen, stellen Sie sicher, dass der Pfad des Inhaltsordners in der Datei &quot;module_version.csv&quot; angegeben wird. Wenn Sie diesen Schritt versäumen, können während der Migration Fehler auftreten. Wenn Sie beispielsweise Inhalte von Modulen zum Selbststudium (z. B. Videos) hochladen, müssen Sie den relativen Box-URL-Pfad in der Datei &quot;module_version.csv&quot; angeben. Für Inhalte des Aktivitätsmoduls können Sie den URL-Namen angeben.

   In der Abbildung unten sehen Sie ein Referenzbeispiel für den Fortschrittsdialog. Wie in der Momentaufnahme gezeigt, können Sie die Anzahl der für jedes Migrationsdatenelement verarbeiteten Datensätze zusammen mit dem Status der erfolgreichen und fehlgeschlagenen Elemente anzeigen. Klicken Sie auf Fehlerdatensätze für die fehlgeschlagenen Elemente herunterladen , um die Fehlerprotokolle herunterzuladen und anzuzeigen. Sie können die Probleme in der CSV-Datei beheben und sie erneut auf FTP hochladen.

   ![](assets/sample-sprint-progress-status.png)
   *Sprint-Fortschritt anzeigen*

   Klicken Sie auf die Sprint-Liste im linken Bereich, wenn Sie die Liste aller Sprints eines Migrationsprojekts anzeigen möchten. Sie können eine Liste aller Sprints, die Anzahl der für jeden Sprint ausgeführten Läufe, das Startdatum, die Dauer und den Abschlussstatus anzeigen, wie in der Abbildung unten dargestellt.

   ![](assets/sprint-list.png)
   *Liste der Sprints anzeigen*

1. Nachdem Sie die neuesten aktualisierten CSV-Dateien hochgeladen haben, können Sie in der oberen rechten Ecke der Seite auf &quot;Wiederholen&quot; klicken. Bei der Wiederholung werden alle Datenelemente noch einmal verarbeitet und Elemente ignoriert, für die keine Änderungen vorgenommen wurden. Sobald Sie mit der Migration von Datenelementen in einem Sprint zufrieden sind, können Sie die Sprint-Migration als abgeschlossen markieren, indem Sie auf die Schaltfläche oben auf der Seite klicken. Sie können einen neuen Sprint mit mehr Datenelementen zu einem späteren Zeitpunkt starten. Sobald ein Sprint als abgeschlossen markiert wurde, können Sie ihn nicht erneut ausführen. Entsprechend können Sie in einem Migrationsprojekt eine beliebige Anzahl von Sprints verwenden. Sobald Sie mit dem Migrationsstatus aller Sprints zufrieden sind, können Sie das Migrationsprojekt als abgeschlossen markieren, indem Sie auf **Projekt als abgeschlossen markieren** auf der Seite mit der Sprint-Liste.

   Bevor Sie das Migrationsprojekt als abgeschlossen markieren, müssen Sie sicherstellen, dass alle Sprints des Projekts abgeschlossen sind. Nachdem Sie das Migrationsprojekt als abgeschlossen markiert haben, können Sie nicht zurückgehen und Sprints in diesem Projekt erstellen oder Änderungen an diesem Projekt vornehmen. Sie müssen ein weiteres Migrationsprojekt erstellen und ihm Sprints hinzufügen.

## Migrationsverifizierung {#registration}

Nachdem Sie die Lerndaten und -inhalte aus dem älteren LMS Ihres Unternehmens migriert haben, können Sie die importierten Daten und Inhalte mit verschiedenen Lernobjektfunktionen überprüfen. Sie können sich beispielsweise bei der Learning Manager-Anwendung als Administrator anmelden und die Verfügbarkeit von Daten und Inhalten aus importierten Modulen und Kursen überprüfen.

## Nachrüsten in der Migration {#retrofittinginmigration}

Mit dieser Integrationsfunktion können Sie historische Daten für ein Lernobjekt von einem veralteten Learning Management-System auf einen aktiven Kurs nachrüsten, der in Learning Manager erstellt wird.

Im Folgenden finden Sie die CSV-Standardspezifikationen, die zur Verknüpfung mit Ihren vorhandenen LMS-Migrationsdaten verwendet werden können. Klicken Sie auf &quot;CSV-Spezifikationen und Beispiel-CSV&quot;, um ZIP-Dateien herunterzuladen. Die heruntergeladene Datei &quot;csv-specifications.zip&quot; enthält vier Excel-Dateien. Diese Excel-Dateien sind Spezifikationen mit Beschreibungen zum Ausfüllen von CSV-Dateien. Die entsprechenden CSV-Dateien sollten die Daten für jedes Feld im vordefinierten Format enthalten, wie in diesen XLSX-Dateien erläutert.

1-enrollment.xlsx enthält Beschreibungen von Metadaten, die für die retrofit_enrollment.csv-Datei erforderlich sind.

2-certification_enrollment.xlsx enthält Beschreibungen von Metadaten, die für die retrofit_certification_enrollment.csv-Datei erforderlich sind.

3-learning_program_enrollment.xlsx enthält Beschreibungen von Metadaten, die für die retrofit_learning_program_enrollment.csv-Datei erforderlich sind.

4-user_course_grades.xlsx enthält Beschreibungen von Metadaten, die für die retrofit_user_course_grades.csv-Datei erforderlich sind.
[csv-specifications.zip](assets/csv-specifications.zip)

## Fehlerbehebung bei Migrationsproblemen {#troubleshootingmigrationissues}

[Hier klicken](../../kb/troubleshooting-migration.md) Erfahren Sie mehr über die Problemumgehung/Lösung für die Probleme, mit denen die für die Integration zuständigen Administratoren bei der Migration von Daten und Inhalten aus ihrem vorhandenen LMS in die Learning Manager-Anwendung konfrontiert sind.

## Tipps zur Benutzerverwaltung {#usermanagement}

In diesem Thema finden Sie einige Tipps, mit denen Sie verstehen, wie Benutzer im Lern-Manager berücksichtigt und verwaltet werden. Mit diesen Konzepten können Sie Benutzer besser verwalten, während Sie den CSV-Import, Connectors und Migrationsfunktionen von Learning Manager verwenden.

## Learning Manager-IDs {#captivateprimeids}

Learning Manager bietet zwei Arten von eindeutigen IDs für Benutzer:

* E-Mail
* UUID (Universally Unique ID)

Learning Manager unterstützt UUID, um Unternehmen Flexibilität bei der Steuerung von Benutzerkonten zu bieten. Wenn Sie über UUID von Benutzern in einem Konto verfügen, können Sie als Administrator die E-Mail-IDs der Benutzer für dieses Konto ändern.

**Anwendungsszenario für UUID in einem Unternehmen**

Stellen Sie sich ein Szenario vor, in dem ein Mitarbeiter A sich als Vertragsnehmer dem Unternehmen Learning Manager anschließt. Während der Vertragslaufzeit stellt das Learning Manager-Unternehmen möglicherweise keine Unternehmens-E-Mail-ID wie A@example.com zur Verfügung, sondern berücksichtigt stattdessen das persönliche E-Mail-Konto des Mitarbeiters, z. B. A@gmail.com. Nach Abschluss von 6 Monaten Vertragslaufzeit, wenn derselbe Mitarbeiter A sich dem Learning Manager als Vollzeitmitarbeiter anschließt, möchte der Learning Manager seine E-Mail-ID in eine Unternehmens-E-Mail-ID ändern: A@example.com.

UUID-Zugriff auf das Benutzerkonto ist für den Learning Manager des Unternehmens im oben genannten Szenario hilfreich. Das Unternehmen mit dem Learning Manager kann die persönliche E-Mail-ID des Mitarbeiters A ganz einfach durch eine offizielle E-Mail-ID ersetzen. Die für dieses Konto relevanten Datensätze für den Mitarbeiter sind von dieser Änderung nicht betroffen.

## Identifikation einzelner Benutzer {#singleuseridentification}

Der Lern-Manager identifiziert und speichert, wie ein einzelner Benutzer hinzugefügt wird: über Selbstregistrierung, CSV-Upload oder durch Hinzufügen eines einzelnen Benutzers über die Benutzeroberfläche oder mithilfe einer API.

* Wenn ein einzelner Benutzer über die Benutzeroberfläche (UI) oder über die API hinzugefügt wird, können Sie solche Einzelbenutzer über die Benutzeroberfläche (UI) oder die API löschen.
* Sie können einzelne Benutzer über CSV-Upload-Prozesse aktualisieren, aber Sie müssen beachten, dass diese einzelnen Benutzer als CSV-Benutzer behandelt werden und die CSV-Workflows für diese Benutzer gelten.

## Manager-Rolle zuweisen {#assigningmanagerrole}

Sie können eine Manager-Rolle nicht jedem Benutzer im Lern-Manager direkt zuweisen. Ein Benutzer X kann nur ein Learning Manager Manager werden, wenn Sie ein Manager-Attribut für einen beliebigen Benutzer (z. B. Y) in diesem Konto als X festlegen.

In einem Szenario, in dem X der Manager der Benutzer A, B und C ist, müssen Sie sicherstellen, dass das Manager-Attribut für A, B und C auf den neuen Manager festgelegt wird, wenn X das Unternehmen verlässt. Alternativ können Sie auch das Manager-Attribut dieser Benutzer vorübergehend als ROOT festlegen und später dem neuen Namen des Managers zuweisen.

Weitere Informationen zu diesem Thema finden Sie in den folgenden Hilfeinhalten:

* [Häufig gestellte Fragen zum Hochladen von CSV](/help/migrated/administrators/add-users-in-bulk.md)
* [Funktions-Hilfe für das Hinzufügen von Benutzern](/help/migrated/administrators/feature-summary/add-users-user-groups.md)


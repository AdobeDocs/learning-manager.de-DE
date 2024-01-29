---
description: Dieses Dokument enthält grundlegende Tipps zur Fehlerbehebung, um einige der typischen Probleme zu lösen, die bei der Migration von Daten und Inhalten aus einem vorhandenen LMS in den Learning Manager auftreten können.
jcr-language: en_us
title: Fehlerbehebung bei Migrationsproblemen
contentowner: jayakarr
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 0%

---



# Fehlerbehebung bei Migrationsproblemen

Dieses Dokument enthält grundlegende Tipps zur Fehlerbehebung, um einige der typischen Probleme zu lösen, die bei der Migration von Daten und Inhalten aus einem vorhandenen LMS in den Learning Manager auftreten können.

## Allgemeine Migrationsprobleme {#genericmigrationissues}

### Anmeldung beim FTP-Ordner oder Inhaltsordner nicht möglich {#unabletologintoftpfolderorcontentfolder}

Stellen Sie sicher, dass Ihre Konten in den FTP- und Box-Diensten erstellt wurden. Wenn Sie ein Migrationsprojekt erstellen, fordern Sie die Einrichtung dieser beiden Dienste an. Sobald Sie die Dienste erstellt haben, erhalten Sie E-Mails von Exavault und Box zum Zurücksetzen oder Einrichten der Kennwörter. Wenn Sie sich nicht an die Kennwörter erinnern, können Sie sie zurücksetzen, indem Sie die Exavault- und Box-Websites besuchen.

### Aufträge werden auch nach dem Klicken auf die Schaltfläche &quot;Aktualisieren&quot; nicht wiedergegeben {#jobsarenotreflectedevenafterclickingrefreshbutton}

* Stellen Sie sicher, dass die CSV-Dateien in den richtigen Ordner in ExaVault FTP hochgeladen werden. Die Pfadstruktur sollte wie folgt lauten:

`code Account>Project>Sprint location`

* Stellen Sie sicher, dass die Dateinamen von CSV-Dateien den Namen der CSV-Spezifikation entsprechen:

   * course.csv
   * course_instance.csv
   * course_module.csv
   * enrollment.csv
   * module.csv
   * module_version.csv
   * user_course_grade.csv

### Für Aufträge mit Fehlerdatensätzen werden Fehler angezeigt {#failuresareshownforjobswitherrorrecords}

1. Herunterladen der Fehlerprotokolle durch Klicken auf **Fehlerdatensätze herunterladen** Glied
1. Korrigieren Sie die ursprünglichen CSVs basierend auf den gemeldeten Fehlern, und
1. Führen Sie den Sprint mit den geänderten CSVs erneut aus.

Es empfiehlt sich, geänderte CSVs in einem neuen Sprint auszuführen, wenn die Anzahl der Änderungen im Vergleich zur Gesamtzahl der Datensätze geringer ist.

### Anmeldung bei der Learning Manager-Anwendung auch nach Beenden der Sprint-Migration nicht möglich {#unabletologintocaptivateprimeapplicationevenafterstoppingthesprintmigration}

Es kann 10-15 Minuten dauern, ein Konto zu entsperren, sobald ein Sprint-Run beendet oder abgeschlossen ist. Versuchen Sie, nach 15 Minuten auf die Anwendung zuzugreifen.

### Einige der Migrationsaufträge zeigen den Status &quot;In Bearbeitung&quot; an, selbst wenn &quot;Stopp&quot; ausgelöst wird. {#someofthemigrationjobsdisplayinprogressstatusevenafterstopistriggered}

Es kann 10 bis 15 Minuten dauern, bis alle Aufträge beendet sind, sobald sie den Status &quot;In Bearbeitung&quot; aufweisen. Überprüfen Sie den Status nach 10 Minuten erneut.

### Sprint kann nicht erstellt werden, da die Schaltfläche deaktiviert ist {#unabletocreateasprintasthebuttonisdisabled}

Stellen Sie sicher, dass der aktuelle Sprint als abgeschlossen markiert ist, bevor Sie einen Sprint erstellen. Klicken **[!UICONTROL Mark Sprint abgeschlossen]** , um eine Sprint-Migration abzuschließen.

### Ein Migrationsprojekt kann nicht als abgeschlossen markiert werden, da die Schaltfläche deaktiviert ist {#unabletomarkamigrationprojectascompleteasthebuttonisdisabled}

Stellen Sie sicher, dass der aktuelle Sprint als abgeschlossen markiert ist, bevor Sie den Abschluss des Migrationsprojekts markieren. Klicken **[!UICONTROL Mark Sprint abgeschlossen]** , um eine Sprint-Migration abzuschließen.

## CSV-Probleme {#csvissues}

### Die Dateimigration von module_version.csv schlägt fehl und der Inhalt wird noch nicht migriert. {#moduleversioncsvfilemigrationisfailingandcontentisnotmigratedyet}

Stellen Sie sicher, dass der Inhalt im Inhaltsordner verfügbar ist (Box-Konto unter dem angegebenen Migrationsprojekt, Sprint-Pfad). Stellen Sie außerdem sicher, dass Sie die Option **Ja** für **Werden Sie Inhalte für diesen Sprint migrieren?** Frage auf der Seite zum Erstellen des Sprints.

Wenn Sie die Auswahl vergessen haben **Ja**, und fahren Sie weiter in diesem Sprint, dann müssen Sie warten, bis Sie diesen Sprint abgeschlossen. Erstellen Sie einen weiteren Sprint und klicken Sie auf **[!UICONTROL Ja]**.

### enrollment.csv- oder user_course_grade.csv-Datensätze schlagen fehl mit der Fehlermeldung &quot;Keine gültige Learning Manager-ID&quot;. {#enrollmentcsvorusercoursegradecsvrecordsfailwithanerrormessagenotavalidprimeid}

Stellen Sie sicher, dass die E-Mail-ID, die als Teil der Felder &quot;userId&quot; und &quot;assignedByUserID&quot; bereitgestellt wird, zu gültigen Lern-Manager-Benutzern gehört. Wenn nicht, fügen Sie den Benutzer hinzu, erstellen Sie einen neuen Sprint mit **Benutzer synchronisieren** ausgewählt ist. Wenn der Benutzer nicht Teil der Organisation ist, fügen Sie den Benutzer als gelöschten Benutzer im Lern-Manager hinzu, indem Sie die CSV-Spezifikation für Benutzer hinzufügen verwenden. In der Abbildung unten sehen Sie ein Referenzbeispiel mit einer CSV-Spezifikation zum Hinzufügen gelöschter Benutzer.

[Users.csv](assets/users.zip) Siehe **CSV-Spezifikationen und CSV-Musterdateien** Abschnitt in [Migrationshandbuch](../integration-admin/feature-summary/migration-manual.md) , um alle CSV-Spezifikationen und Beispiel-CSV-Dateien herunterzuladen.

### Kurse werden leer oder falsche Module werden für einen migrierten Kurs abgespielt {#coursesappearblankorincorrectmodulesplayforamigratedcourse}

Stellen Sie sicher, dass **moduleOrderInCourse** Schlüsselwert für einen Kurs beginnt mit **0** und ist in fortlaufender Reihenfolge. Die Reihenfolge in Bezug auf courseModuleType sollte PRETEST, TESTOUT, CONTENT lauten.

Stellen Sie außerdem sicher, dass die beiden Versionen von Aktivität, Klassenzimmer und VC nicht mit dem vorhandenen Kurs verknüpft sind.

### Erhalten einer Nachricht als &quot;Das Modul ist bereits mit einem vorhandenen Kurs verknüpft&quot; {#receivingamessageasmoduleisalreadylinkedwithanexistingcourse}

Learning Manager ermöglicht das Verknüpfen des Aktivitäts-/VC-/Klassenzimmermoduls mit nur einem Kurs nicht. Stellen Sie sicher, dass das Modul nicht mit anderen Kursen verknüpft ist.

### Alle Kurse zeigen die neueste Version der Activity/VC/Classroom-Module an, obwohl die Kurse mit verschiedenen Modulversionen verknüpft sind {#allthecoursesshowthelatestversionofactivityvcclassroommoduleseventhoughthecoursesarelinkedwithdifferentmoduleversions}

Die Versionierung von Aktivitäts-, Klassenzimmer- und virtuellen Klassenzimmermodulen wird in Learning Manager nicht unterstützt. Wenn Sie Versionen über die Datei &quot;moduleVersion.csv&quot; bereitstellen, wird die vorhandene Datei aktualisiert, anstatt eine neue Version zu erstellen.

### Die gewünschte Dauer wird für ein migriertes Aktivitäts-/VC-/Klassenzimmermodul nicht angezeigt {#desireddurationdoesnotappearforamigratedactivityvcclassroommodule}

Die gewünschte Dauer ist kein gültiger Eintrag für das Aktivitäts-/VC-/Klassenzimmermodul.

### Hyperlink-URL wird in Learning Manager nicht geöffnet {#hyperlinkurldoesntopenupincaptivateprime}

Stellen Sie sicher, dass die angegebenen Links mit &quot;http://&#39;&quot; oder &quot;https://&#39;&quot; als Präfix angegeben sind.

### moduleVersion-Migration schlägt fehl mit dem Fehler &quot;Datei nicht gefunden&quot; {#moduleversionmigrationfailswithfilenotfounderrors}

Stellen Sie sicher, dass die referenzierte Datei im Inhaltsordner vorhanden ist und erfolgreich migriert wird.

### moduleVersion-Migration schlägt mit einer Fehlermeldung fehl: &quot;Ein interner Fehler ist aufgetreten - für Modul : x und moduleVersion : y&quot; {#moduleversionmigrationfailswithanerrormessageasaninternalerrorhasoccurredformodulexandmoduleversiony}

Führen Sie den Sprint erneut aus, um das Problem zu beheben.

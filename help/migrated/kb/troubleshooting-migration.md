---
description: Dieses Dokument enthält grundlegende Tipps zur Fehlerbehebung, um einige Probleme zu lösen, die bei der Migration von Daten und Inhalten aus einem vorhandenen LMS zu Learning Manager auftreten.
jcr-language: en_us
title: Fehlerbehebung bei häufigen Migrationsproblemen
contentowner: jayakarr
exl-id: b9f17644-f237-4701-86e9-8496db941920
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 43%

---

# Fehlerbehebung bei häufigen Migrationsproblemen

Dieses Dokument enthält grundlegende Tipps zur Fehlerbehebung, um einige Probleme zu lösen, die bei der Migration von Daten und Inhalten aus einem vorhandenen LMS zu Learning Manager auftreten.

## Generische Migrationsprobleme {#genericmigrationissues}

### Keine Verbindung zum FTP-Ordner oder Inhaltsordner {#unabletologintoftpfolderorcontentfolder}

Stellen Sie sicher, dass Ihre Konten in den FTP- und Box-Diensten erstellt wurden. Wenn Sie ein Migrationsprojekt erstellen, wollen Sie diese beiden Dienste einrichten. Nachdem Sie die Dienste erstellen, erhalten Sie eine E-Mail von Exavault und Box, um die Kennwörter zurückzusetzen oder einzurichten. Wenn Sie sich nicht an die Kennwörter erinnern, können Sie sie zurücksetzen, indem Sie die Exavault- und Box-Websites besuchen.

### Aufträge werden nicht reflektiert, selbst nach dem Klicken auf die Schaltfläche „Aktualisieren“ {#jobsarenotreflectedevenafterclickingrefreshbutton}

* Stellen Sie sicher, dass die CSV-Dateien in den korrekten Ordner in Exavault FTP hochgeladen werden. Die Pfadstruktur sollte wie folgt lauten:

`code Account>Project>Sprint location`

* Stellen Sie sicher, dass die Dateinamen von CSV-Dateien mit den CSV-Spezifikationsnamen übereinstimmen:

   * course.csv
   * course_instance.csv
   * course_module.csv
   * enrollment.csv
   * module.csv
   * module_version.csv
   * user_course_grade.csv

### Fehler werden für Aufträge mit Fehlerdatensätzen angezeigt {#failuresareshownforjobswitherrorrecords}

1. Laden Sie die Fehlerprotokolle herunter, indem Sie auf den Link **Fehlerprotokolle herunterladen** klicken
1. Korrigieren Sie die ursprüngliche CSVs, basierend auf den gemeldeten Fehlern
1. Führen Sie den Sprint mit den geänderten CSVs erneut aus.

Es empfiehlt sich, geänderte CSVs in einem neuen Sprint auszuführen, wenn die Anzahl der Änderungen im Vergleich zur Gesamtzahl der Datensätze geringer ist.

### Anmeldung bei der Learning Manager-Anwendung auch nach dem Beenden der Sprint-Migration nicht möglich {#unabletologintocaptivateprimeapplicationevenafterstoppingthesprintmigration}

Es kann 10-15 Minuten dauern, um ein Konto zu entsperren, nachdem eine Sprint-Durchführung angehalten oder beendet wurde. Versuchen Sie, nach 15 Minuten auf die Anwendung zuzugreifen.

### Einige der Migrationsaufträge zeigen den Status &quot;In Bearbeitung&quot; an, selbst wenn &quot;Stopp&quot; ausgelöst wird. {#someofthemigrationjobsdisplayinprogressstatusevenafterstopistriggered}

Es kann 10 bis 15 Minuten dauern, bis alle Aufträge beendet sind, sobald sie den Status &quot;In Bearbeitung&quot; aufweisen. Überprüfen Sie den Status nach 10 Minuten erneut.

### Sprint konnte nicht erstellt werden da die Schaltfläche deaktiviert ist {#unabletocreateasprintasthebuttonisdisabled}

Stellen Sie sicher, dass der aktuelle Sprint als abgeschlossen markiert ist, bevor Sie einen Sprint erstellen. Klicken Sie oben auf der Seite auf **[!UICONTROL Sprint als abgeschlossen markieren]**, um eine Sprint-Migration abzuschließen.

### Migrationsprojekte können nicht als „abgeschlossen“ markiert werden, da die Schaltfläche deaktiviert ist {#unabletomarkamigrationprojectascompleteasthebuttonisdisabled}

Stellen Sie sicher, dass der aktuelle Sprint als abgeschlossen markiert ist, bevor Sie den Abschluss des Migrationsprojekts markieren. Klicken Sie oben auf der Seite auf **[!UICONTROL Sprint als abgeschlossen markieren]**, um eine Sprint-Migration abzuschließen.

## CSV-Probleme {#csvissues}

### module_version.csv-Dateimigration schlägt fehl und Inhalt ist noch nicht migriert {#moduleversioncsvfilemigrationisfailingandcontentisnotmigratedyet}

Stellen Sie sicher, dass der Inhalt im Inhaltsordner verfügbar ist (Box-Konto unter dem angegebenen Migrationsprojekt, Sprint-Pfad). Stellen Sie außerdem sicher, dass Sie die Option **Ja** für **Möchten Sie Inhalte für diesen Sprint migrieren?**-Frage auf der Seite zum Erstellen des Sprints.

Wenn Sie vergessen, **Ja** zu wählen und weiter diesen Sprint verwenden, müssen Sie warten, bis Sie diesen Sprint abgeschlossen haben. Erstellen Sie einen weiteren Sprint und klicken Sie auf **[!UICONTROL Ja]**.

### enrollment.csv- oder user_course_grade.csv-Datensätze schlagen fehl mit der Fehlermeldung &quot;Keine gültige Learning Manager-ID&quot;. {#enrollmentcsvorusercoursegradecsvrecordsfailwithanerrormessagenotavalidprimeid}

Stellen Sie sicher, dass die E-Mail-ID, die im Rahmen der Felder „userId“ und „assignedByUserID“ bereitgestellt wird, zu gültigen Learning Manager-Benutzern gehören. Wenn dies nicht der Fall ist, fügen Sie den Benutzer hinzu, erstellen Sie einen neuen Sprint mit der Option **Benutzer synchronisieren**. Wenn der Benutzer nicht Teil der Organisation ist, fügen Sie den Benutzer als gelöschten Benutzer im Lern-Manager hinzu, indem Sie die CSV-Spezifikation für Benutzer hinzufügen verwenden. In der Abbildung unten sehen Sie ein Referenzbeispiel mit einer CSV-Spezifikation zum Hinzufügen gelöschter Benutzer.

[Benutzer.csv](assets/users.zip) Lesen Sie im Abschnitt [CSV-Spezifikationen und Beispiel-CSVs **im** Migrationshandbuch](../integration-admin/feature-summary/migration-manual.md) den vollständigen Satz von CSV-Spezifikationen und Beispiel-CSV-Dateien, um diese herunterzuladen.

### Kurse werden leer oder falsche Module werden für einen migrierten Kurs abgespielt {#coursesappearblankorincorrectmodulesplayforamigratedcourse}

Stellen Sie sicher, dass der Schlüsselwert **moduleOrderInCourse** für einen Kurs mit **0** beginnt und in fortlaufender Reihenfolge vorliegt. Die Reihenfolge in Bezug auf courseModuleType sollte PRETEST, TESTOUT, CONTENT lauten.

Stellen Sie außerdem sicher, dass die beiden Versionen von Aktivität, Klassenzimmer und VC nicht mit dem vorhandenen Kurs verknüpft sind.

### Erhalten einer Nachricht als &quot;Das Modul ist bereits mit einem vorhandenen Kurs verknüpft&quot; {#receivingamessageasmoduleisalreadylinkedwithanexistingcourse}

Learning Manager lässt keine Verknüpfungen des Moduls für Aktivität/VC/Klassenzimmer mit mehr als einem Kurs zu. Stellen Sie sicher, dass das Modul nicht mit anderen Kursen verknüpft ist.

### Alle Kurse zeigen die neueste Version von von Aktivitäts-/VC-/Klassenzimmer-Modul an, obwohl die Kurse mit verschiedenen Modulversionen verknüpft sind {#allthecoursesshowthelatestversionofactivityvcclassroommoduleseventhoughthecoursesarelinkedwithdifferentmoduleversions}

Die Versionierung der Module für Aktivität, Klassenzimmer und virtuelle Klassenzimmer wird in Learning Manager nicht unterstützt. Wenn Sie Versionen über die Datei &quot;moduleVersion.csv&quot; bereitstellen, wird die vorhandene Datei aktualisiert, anstatt eine neue Version zu erstellen.

### Die gewünschte Dauer wird für ein migriertes Aktivitäts-/VC-/Klassenzimmermodul nicht angezeigt {#desireddurationdoesnotappearforamigratedactivityvcclassroommodule}

Die gewünschte Dauer ist kein gültiger Eintrag für das Aktivitäts-/VC-/Klassenzimmermodul.

### Hyperlink-URL wird in Learning Manager nicht geöffnet {#hyperlinkurldoesntopenupincaptivateprime}

Stellen Sie sicher, dass die angegebenen Links mit &quot;http://&#39;&quot; oder &quot;https://&#39;&quot; als Präfix angegeben sind.

### moduleVersion-Migration schlägt fehl mit dem Fehler &quot;Datei nicht gefunden&quot; {#moduleversionmigrationfailswithfilenotfounderrors}

Stellen Sie sicher, dass die referenzierte Datei im Inhaltsordner vorhanden ist und erfolgreich migriert wird.

### moduleVersion-Migration schlägt mit einer Fehlermeldung fehl: &quot;Ein interner Fehler ist aufgetreten - für Modul : x und moduleVersion : y&quot; {#moduleversionmigrationfailswithanerrormessageasaninternalerrorhasoccurredformodulexandmoduleversiony}

Führen Sie den Sprint erneut aus, um das Problem zu beheben.

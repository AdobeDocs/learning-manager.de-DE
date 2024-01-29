---
jcr-language: en_us
title: Gleichzeitiges Hinzufügen mehrerer Benutzer
description: Erfahren Sie, wie Sie mehrere Benutzer gleichzeitig hinzufügen.
contentowner: saghosh
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---



# Gleichzeitiges Hinzufügen mehrerer Benutzer

Ja, Sie können mehrere Benutzer gleichzeitig hinzufügen, indem Sie die folgenden Schritte ausführen:

1. Klicken **[!UICONTROL Benutzer]** im linken Bereich bei der Administratoranmeldung und klicken Sie dann auf **[!UICONTROL Hinzufügen]** > **[!UICONTROL CSV hochladen]**. Ein Popup-Dialogfeld wird angezeigt.

1. Sie können mehrere Benutzer mithilfe einer CSV-Datei hinzufügen. Klicken **[!UICONTROL Importieren]** und wählen Sie die CSV-Datei auf Ihrem Computer aus bzw. öffnen Sie sie.

1. Nachdem Sie die Datei importiert haben, ordnen Sie den Inhalt der CSV-Datei den Anwendungsbezeichnungen zu, wenn Sie die CSV-Datei zum ersten Mal hochladen.

   Für alle nachfolgenden Uploads werden die vorherigen Einstellungen für Beschriftungen berücksichtigt. Klicken **[!UICONTROL Speichern]** nach Abschluss der Datenzuordnung und klicken Sie auf **[!UICONTROL Hinzufügen]** , um die zugeordnete CSV-Datei hochzuladen.

1. Klicken **[!UICONTROL Speichern]** nach Abschluss der Datenzuordnung und klicken Sie auf **[!UICONTROL Hinzufügen]** , um die zugeordnete CSV-Datei hochzuladen.

## CSV-Upload mit obligatorischen Feldern {#csvuploadwithmandatoryfields}

Es ist nicht zwingend erforderlich, das Profil des Benutzers und die E-Mail-ID des Managers zur CSV hinzuzufügen. Der Benutzername und die E-Mail-ID des Benutzers sind die einzigen obligatorischen Felder.

In diesem Fall wird der Administrator Ihres Unternehmens standardmäßig als Manager für Benutzer behandelt. Standardmäßig wird der Mitarbeiter als Benutzerprofil betrachtet.

**Beispiel-CSV**

Beispiel-CSV für Learning Manager ist unten mit Pflichtfeldern verfügbar.
[Sample-CSV-name-email.zip](assets/sample-csv-name-email.zip)

## CSV-Upload mit allen Feldern {#csvuploadwithallthefields}

Bevor Sie die E-Mail-ID des Managers für einen Mitarbeiter hinzufügen, stellen Sie sicher, dass der Manager zuerst als Mitarbeiter in der CSV-Datei hinzugefügt wird. Verweisen Sie z. B. in der Momentaufnahme unten auf den Namen des Mitarbeiters, Howard Walters:

![](assets/csv-example.png)

*CSV-Vorlage für Upload*

Außerdem können Administratoren eines Unternehmens sich selbst als Mitarbeiter hinzufügen und die E-Mail-ID ihres Managers als Stamm erwähnen.

**Beispiel-CSV**

Die Beispiel-CSV für den Learning Manager ist unten mit allen Feldern verfügbar.
[learning-manager-sample-csv.zip](assets/learning-manager-sample-csv.zip).

Siehe  [CSV-Upload verwenden](/help/migrated/administrators/feature-summary/add-users-user-groups.md) Weitere Informationen finden Sie in der Hilfe.

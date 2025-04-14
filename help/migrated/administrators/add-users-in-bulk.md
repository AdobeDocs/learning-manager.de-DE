---
jcr-language: en_us
title: Gleichzeitiges Hinzufügen mehrerer Benutzer
description: Erfahren Sie, wie Sie mehrere Benutzer gleichzeitig hinzufügen.
contentowner: saghosh
exl-id: c3309ce5-8764-452e-82d5-5637c23c661b
source-git-commit: a28ac8f57710c118ca4ad02872fd100c6f24beac
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 23%

---

# Gleichzeitiges Hinzufügen mehrerer Benutzer

In dieser Schulung erfahren Sie, wie Sie mehrere Benutzer gleichzeitig über eine CSV-Datei hinzufügen.

[![Schaltfläche](feature-summary/assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/7555555)

Wenn Sie die Schulung nicht starten können, schreiben Sie an <almacademy@adobe.com>.

## Mehrere Benutzer hinzufügen

Sie können mehrere Benutzer gleichzeitig hinzufügen, indem Sie die folgenden Schritte ausführen:

1. Klicken Sie auf **[!UICONTROL Benutzer]** im linken Bereich in der Administratoranmeldung und klicken Sie dann auf **[!UICONTROL Hinzufügen]** > **[!UICONTROL CSV hochladen]**. Ein Popup-Fenster wird angezeigt.

1. Mithilfe einer CSV-Datei können Sie mehrere Benutzer gleichzeitig hinzufügen. Klicken Sie auf **[!UICONTROL Importieren]** und wählen/öffnen Sie die CSV-Datei von Ihrem Computer aus.

1. Nachdem Sie die Datei importiert haben, müssen Sie den Inhalt der CSV-Datei den Anwendungsbezeichnungen zuordnen, wenn Sie die CSV-Datei zum ersten Mal hochladen.

   Bei allen nachfolgenden Uploads werden die vorherigen Einstellungen für die Beschriftungen beachtet. Klicken Sie auf **[!UICONTROL Speichern]**, nachdem Sie die Datenzuordnung abgeschlossen haben, und klicken Sie auf **[!UICONTROL Hinzufügen]**, um die zugeordnete CSV-Datei hochzuladen.

1. Klicken Sie auf **[!UICONTROL Speichern]**, nachdem Sie die Datenzuordnung abgeschlossen haben, und klicken Sie auf **[!UICONTROL Hinzufügen]**, um die zugeordnete CSV-Datei hochzuladen.

## CSV-Upload mit Pflichtfeldern {#csvuploadwithmandatoryfields}

Es ist nicht zwingend erforderlich, das Profil des Benutzers und die E-Mail-ID des Managers zur CSV hinzuzufügen. Der Benutzername und die E-Mail-ID des Benutzers sind die einzigen obligatorischen Felder.

In diesem Fall wird der Administrator Ihres Unternehmens standardmäßig als Manager für Benutzer behandelt. Standardmäßig wird der Mitarbeiter als Benutzerprofil betrachtet.

>[!NOTE]
>
>Um neue Benutzer hinzuzufügen, erstellen Sie eine neue CSV-Datei mit ihren Details und laden Sie sie hoch. Das Aktualisieren und erneute Hochladen einer vorhandenen CSV-Datei wird nicht unterstützt.

**Beispiel-CSV**

Beispiel-CSV für Learning Manager ist unten mit Pflichtfeldern verfügbar.
[Beispiel-CSV-Name-email.zip](assets/sample-csv-name-email.zip)

## CSV-Upload mit allen Feldern {#csvuploadwithallthefields}

Bevor Sie die E-Mail-ID des Managers für einen Mitarbeiter hinzufügen, stellen Sie sicher, dass der Manager zuerst als Mitarbeiter in der CSV-Datei hinzugefügt wird. In der Momentaufnehme unten sehen Sie beispielsweise den Namen Howard Walters:

![](assets/csv-example.png)

*CSV-Vorlage für Upload*

Außerdem können Administratoren eines Unternehmens sich selbst als Mitarbeiter hinzufügen und die E-Mail-ID ihres Managers als Stamm erwähnen.

**Beispiel-CSV**

Die Beispiel-CSV für den Learning Manager ist unten mit allen Feldern verfügbar.
[learning-manager-sample-csv.zip](assets/learning-manager-sample-csv.zip).

Weitere Informationen finden Sie unter [Verwenden des CSV-Uploads](/help/migrated/administrators/feature-summary/add-users-user-groups.md).

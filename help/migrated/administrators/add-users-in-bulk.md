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

In dieser Schulung erfahren Sie, wie Sie Benutzer in großen Mengen über eine CSV-Datei hinzufügen.

[![Knopf](feature-summary/assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/7555555)

Wenn Sie das Training nicht starten können, schreiben Sie an <almacademy@adobe.com>.

## So fügen Sie mehrere Benutzer hinzu

Sie können mehrere Benutzer gleichzeitig hinzufügen, indem Sie die folgenden Schritte ausführen:

1. Klicken Sie **[!UICONTROL im linken Bereich der Administratoranmeldung auf Benutzer]** , und klicken Sie dann auf **[!UICONTROL Hinzufügen]** > **[!UICONTROL Hochladen einer CSV-Datei]**. Ein Popup-Fenster wird angezeigt.

1. Mithilfe einer CSV-Datei können Sie mehrere Benutzer gleichzeitig hinzufügen. Klicken Sie auf **[!UICONTROL Importieren]** und wählen Sie die .csv Datei von Ihrem Computer aus.

1. Nachdem Sie die Datei importiert haben, müssen Sie den Inhalt der CSV-Datei den Anwendungsbezeichnungen zuordnen, wenn Sie die CSV-Datei zum ersten Mal hochladen.

   Bei allen nachfolgenden Uploads werden die vorherigen Einstellungen für die Beschriftungen beachtet. Klicken Sie nach **[!UICONTROL Abschluss der Datenzuordnung auf Speichern]** und dann auf **[!UICONTROL Hinzufügen]** , um die zugeordnete .csv Datei hochzuladen.

1. Klicken Sie nach **[!UICONTROL Abschluss der Datenzuordnung auf Speichern]** und dann auf **[!UICONTROL Hinzufügen]** , um die zugeordnete .csv Datei hochzuladen.

## CSV-Upload mit Pflichtfeldern {#csvuploadwithmandatoryfields}

Es ist nicht zwingend erforderlich, das Benutzerprofil und die E-Mail-ID des Managers in der CSV-Datei hinzuzufügen. Der Benutzername und die E-Mail-ID des Benutzers sind die einzigen Pflichtfelder.

In diesem Fall wird der Administrator Ihres Unternehmens standardmäßig als Manager für Benutzer behandelt. Standardmäßig wird &quot;Mitarbeiter&quot; als Benutzerprofil betrachtet.

>[!NOTE]
>
>Um neue Benutzer hinzuzufügen, erstellen Sie eine neue CSV-Datei mit ihren Details und laden Sie sie hoch. Das Aktualisieren und erneute Hochladen einer vorhandenen CSV-Datei wird nicht unterstützt.

**Beispiel-CSV**

Die Learning Manager-Beispiel-CSV-Datei ist unten mit Pflichtfeldern verfügbar.
[Sample-CSV-name-email.zip](assets/sample-csv-name-email.zip)

## CSV-Upload mit allen Feldern {#csvuploadwithallthefields}

Bevor Sie die E-Mail-ID des Managers für einen Mitarbeiter einfügen, stellen Sie sicher, dass der Manager zuerst als Mitarbeiter in CSV hinzugefügt wird. In der Momentaufnehme unten sehen Sie beispielsweise den Namen Howard Walters:

![](assets/csv-example.png)

*CSV-Vorlage zum Hochladen*

Außerdem können Administratoren einer Organisation sich selbst als Mitarbeiter hinzufügen und die E-Mail-ID ihres Managers als root angeben.

**Beispiel-CSV**

Die Learning Manager-Beispiel-CSV-Datei ist unten mit allen Feldern verfügbar.
[learning-manager-sample-csv.zip](assets/learning-manager-sample-csv.zip).

Weitere Informationen finden Sie unter  [Verwenden der CSV-Upload-Funktion](/help/migrated/administrators/feature-summary/add-users-user-groups.md) .

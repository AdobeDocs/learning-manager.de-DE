---
jcr-language: en_us
title: Gleichzeitiges Hinzufügen mehrerer Benutzer
description: Erfahren Sie, wie Sie mehrere Benutzer gleichzeitig hinzufügen.
contentowner: saghosh
exl-id: c3309ce5-8764-452e-82d5-5637c23c661b
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 37%
---
# Gleichzeitiges Hinzufügen mehrerer Benutzer

>[!INFO]
>
>In dieser Schulung erfahren Sie, wie Sie Benutzer gesammelt über eine CSV-Datei hinzufügen.<br><br>[![Schaltfläche](feature-summary/assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/7555555)</br></br>

Wenn Sie die Schulung nicht starten können, schreiben Sie an <almacademy@adobe.com>.

## Mehrere Benutzer hinzufügen

Sie können mehrere Benutzer gleichzeitig hinzufügen, indem Sie die folgenden Schritte ausführen:

1. Klicken Sie auf **[!UICONTROL Benutzer]** im linken Bereich in der Administratoranmeldung und klicken Sie dann auf **[!UICONTROL Hinzufügen]** > **[!UICONTROL CSV hochladen]**. Ein Popup-Fenster wird angezeigt.

1. Mithilfe einer CSV-Datei können Sie mehrere Benutzer gleichzeitig hinzufügen. Klicken Sie auf **[!UICONTROL Importieren]** und wählen/öffnen Sie die CSV-Datei von Ihrem Computer aus.

1. Nachdem Sie die Datei importiert haben, müssen Sie den Inhalt der CSV-Datei den Anwendungsbezeichnungen zuordnen, wenn Sie die CSV-Datei zum ersten Mal hochladen.

   Bei allen nachfolgenden Uploads werden die vorherigen Einstellungen für die Beschriftungen beachtet. Nachdem Sie die Datenzuordnung abgeschlossen haben, klicken Sie auf **[!UICONTROL Speichern]** und auf **[!UICONTROL Hinzufügen]**, um die zugeordnete CSV-Datei hochzuladen.

1. Nachdem Sie die Datenzuordnung abgeschlossen haben, klicken Sie auf **[!UICONTROL Speichern]** und auf **[!UICONTROL Hinzufügen]**, um die zugeordnete CSV-Datei hochzuladen.

## CSV-Upload mit Pflichtfeldern {#csvuploadwithmandatoryfields}

Es ist nicht zwingend erforderlich, das Profil des Benutzers und die E-Mail-ID des Managers zur CSV hinzuzufügen. Der Benutzername und die E-Mail-ID des Benutzers sind die einzigen obligatorischen Felder.

In diesem Fall wird der Administrator Ihres Unternehmens standardmäßig als Manager für Benutzer behandelt. Standardmäßig wird der Mitarbeiter als Benutzerprofil betrachtet.

>[!NOTE]
>
>Um neue Benutzer hinzuzufügen, erstellen Sie eine neue CSV-Datei mit ihren Details und laden Sie sie hoch. Das Aktualisieren und erneute Hochladen einer vorhandenen CSV-Datei wird nicht unterstützt.

**Beispiel-CSV**

Learning Manager-Beispiel-CSV ist mit den Pflichtfeldern unten verfügbar.
[Beispiel-CSV-Name-email.zip](assets/sample-csv-name-email.zip)

## CSV-Upload mit allen Feldern {#csvuploadwithallthefields}

Bevor Sie die E-Mail-ID des Managers für einen Mitarbeiter hinzufügen, stellen Sie sicher, dass der Manager zuerst als Mitarbeiter in der CSV-Datei hinzugefügt wird. In der Momentaufnehme unten sehen Sie beispielsweise den Namen Howard Walters:

![](assets/csv-example.png)

*CSV-Vorlage für Upload*

Außerdem können Administratoren eines Unternehmens **sich selbst** als Mitarbeiter hinzufügen und die E-Mail-ID ihres Managers als Stamm erwähnen.

**Beispiel-CSV**

Learning Manager-Beispiel-CSV ist mit allen Feldern unten verfügbar.
[learning-manager-sample-csv.zip](assets/learning-manager-sample-csv.zip).

Weitere Informationen finden Sie unter [Verwenden des CSV-Uploads](/help/migrated/administrators/feature-summary/add-users-user-groups.md).

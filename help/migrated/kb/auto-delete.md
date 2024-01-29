---
jcr-language: en_us
title: Benutzer wird automatisch im Lern-Manager gelöscht
description: Ein Benutzer wird aus dem Lern-Manager gelöscht, der Administrator hat jedoch nie eine solche Aktion ausgeführt.
contentowner: nluke
source-git-commit: 66dfaaaf723382eada39e2be29dfd49b795107a0
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---



# Benutzer wird automatisch im Lern-Manager gelöscht {#user-gets-auto-deleted-in-learning-manager}

## Problem

Ein Benutzer wird aus dem Lern-Manager gelöscht, der Administrator hat jedoch nie eine solche Aktion ausgeführt.

## Ursache

Im Adobe Learning Manager gibt es eine Option, mit der Sie einen Benutzer löschen können, wenn er sich für eine bestimmte Zeit nicht im System angemeldet hat.

## Wie kann ich die Einstellung ändern/anwenden?

### Für interne Teilnehmer

1. Melden Sie sich als **Administrator**.
1. Unter **Konfigurieren** auf **Einstellungen** > **Allgemein**.
1. Auf der Seite &quot;Allgemeine Einstellungen&quot; finden Sie die Option **Interne Benutzer automatisch löschen**.
1. Klicken **[!UICONTROL Bearbeiten]** , um die Anzahl der Tage in das Feld einzugeben, um einen Teilnehmer automatisch zu löschen, wenn er nicht auf das System zugegriffen hat.

   ![](assets/cp-autodelete-internal.png)

   *Anzahl der Tage bearbeiten*

>[!NOTE]
>
>   Lassen Sie das Feld leer, wenn Sie Benutzer nicht automatisch löschen möchten.


1. Klicken **[!UICONTROL Speichern]** , um die vorgenommenen Einstellungen beizubehalten.

### Für externe Teilnehmer:

1. Melden Sie sich als **Administrator**.
1. Unter **Verwalten** auf **[!UICONTROL Benutzer]** > **[!UICONTROL Extern]**.
1. Klicken Sie auf den Namen eines externen Benutzers, auf den die Einstellung angewendet werden soll.

   Dadurch wird das Fenster &quot; **Externes Registrierungsprofil bearbeiten** &quot; anzuzeigen.

1. Klicken **[!UICONTROL Erweiterte Einstellungen]** in der linken unteren Ecke.

   ![](assets/cp-autodelete-external.png)

   *Wählen Sie die Option Erweiterte Einstellungen .*

1. Im Dialogfeld &quot; **Anmeldeanforderung** die Anzahl der Tage ein, nach denen Teilnehmer automatisch gelöscht werden, wenn sie nicht auf das System zugegriffen haben.
1. Klicken **[!UICONTROL Speichern]** , um die vorgenommenen Einstellungen beizubehalten.

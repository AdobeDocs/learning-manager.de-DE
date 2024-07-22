---
jcr-language: en_us
title: Benutzer wird automatisch in Learning Manager gelöscht
description: Ein Benutzer wird aus Learning Manager gelöscht, der Administrator hat jedoch nie eine solche Aktion ausgeführt.
contentowner: nluke
exl-id: 9e293da3-bcbf-4798-b391-aef53ef8d946
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 61%

---

# Benutzer wird automatisch in Learning Manager gelöscht {#user-gets-auto-deleted-in-learning-manager}

## Problem

Ein Benutzer wird aus Learning Manager gelöscht, der Administrator hat jedoch nie eine solche Aktion ausgeführt.

## Ursache

In Adobe Learning Manager gibt es eine Option, mit der Sie Benutzer löschen können, wenn diese sich für eine bestimmte Zeit nicht im System angemeldet haben.

## Wie kann ich die Einstellung ändern/anwenden?

### Für interne Teilnehmer

1. Melden Sie sich als ein **Administrator** an.
1. Klicken Sie unter **Konfigurieren** auf **Einstellungen** > **Allgemein**.
1. Auf der Seite „Allgemeine Einstellungen“ finden Sie die Option **Interne Benutzer automatisch löschen**.
1. Klicken Sie auf **[!UICONTROL Bearbeiten]**, um die Anzahl der Tage in das Feld einzugeben, nach denen Teilnehmer automatisch gelöscht werden, wenn sie nicht auf das System zugegriffen haben.

   ![](assets/cp-autodelete-internal.png)

   *Anzahl der Tage bearbeiten*

>[!NOTE]
>
>   Lassen Sie das Feld leer, wenn Sie Benutzer nicht automatisch löschen möchten.


1. Klicken Sie auf **[!UICONTROL Speichern]**, um die vorgenommenen Einstellungen beizubehalten.

### Für externe Teilnehmer:

1. Melden Sie sich als ein **Administrator** an.
1. Klicken Sie unter **Verwalten** auf **[!UICONTROL Benutzer]** > **[!UICONTROL Extern]**.
1. Klicken Sie auf den Namen eines externen Benutzers, auf den die Einstellung angewendet werden soll.

   Dadurch wird das Fenster **Externes Registrierungsprofil bearbeiten** geöffnet.

1. Klicken Sie auf **[!UICONTROL Erweiterte Einstellungen]** in der unteren linken Ecke.

   ![](assets/cp-autodelete-external.png)

   *Wählen Sie die Option Erweiterte Einstellungen* aus.

1. Geben Sie im Feld **Anmeldeanforderung** die Anzahl der Tage ein, nach denen Teilnehmer automatisch gelöscht werden, wenn sie nicht auf das System zugegriffen haben.
1. Klicken Sie auf **[!UICONTROL Speichern]**, um die vorgenommenen Einstellungen beizubehalten.

---
jcr-language: en_us
title: Kalender kann nicht angezeigt werden
description: Wenn ein Administrator versucht, das Ablaufdatum eines externen Registrierungsprofils zu bearbeiten, und auf den Kalender klickt, um das Ablaufdatum zu bearbeiten, wird der Kalender nicht angezeigt.
contentowner: saghosh
exl-id: 1b7e5594-714a-4a1d-9b8f-d481c1b48cb5
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 88%

---

# Kalender kann nicht angezeigt werden

## Problem

Sie können den Kalender nicht anzeigen lassen, während Sie das Ablaufdatum eines externen Profils bearbeiten.

## Beschreibung

Wenn ein Administrator versucht, das Ablaufdatum eines externen Registrierungsprofils zu bearbeiten, und auf den Kalender klickt, um das Ablaufdatum zu bearbeiten, wird der Kalender nicht angezeigt.

## Ursache

Das Problem tritt aus folgenden Gründen auf:

* Der Zoomfaktor des Browsers beträgt mehr als 100 %.
* Die Skalierung und das Layout in den Anzeigeeinstellungen beträgt mehr als 100 %.

## Auflösung

### Browser

1. Starten Sie den Browser.
1. Melden Sie sich bei Adobe Learning Manager an.
1. Klicken Sie in der Adressleiste auf das Zoomsymbol.
1. Klicken Sie auf **[!UICONTROL Zurücksetzen]**.
1. Ändern Sie das Ablaufdatum des Registrierungsprofils.

### Anzeigeeinstellungen

1. Klicken Sie auf **[!UICONTROL Start]** > **[!UICONTROL Einstellungen]** > **[!UICONTROL System]**.
1. Klicken Sie auf **[!UICONTROL Anzeige]**.
1. Verwenden Sie unter dem Abschnitt **[!UICONTROL Skalierung und Anordnung]** die Dropdownliste. Ändern Sie die Einstellungen zu 100 %.

   ![](assets/scale-layout.png)

   *Anzeigeeinstellungen ändern*

1. Starten Sie den Computer neu.

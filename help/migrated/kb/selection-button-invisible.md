---
jcr-language: en_us
title: Auswahlschaltflächen werden im Lern-Manager nicht angezeigt
description: Aufgrund fehlender Optionsfelder kann ein Administrator keine Rollen zuweisen oder entfernen, keine Willkommens-E-Mail senden oder Benutzer löschen.
contentowner: nluke
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---



# Auswahlschaltflächen werden im Lern-Manager nicht angezeigt

## Problem

Aufgrund fehlender Optionsfelder kann ein Administrator Folgendes nicht ausführen (keine vollständige Liste):

* Rollen zuweisen oder entfernen.
* Begrüßungs-E-Mail senden
* Löschen Sie einen Benutzer.

## Ursache

Das Problem tritt aufgrund falscher Designs im Konto auf.

![](assets/radio-buttons.png)

*Optionsfelder nicht sichtbar*

## Auflösung

Laden Sie die Designs neu und korrigieren Sie das Erscheinungsbild der Optionsfelder. Führen Sie die folgenden Schritte aus:

1. Klicken Sie als Administrator auf **[!UICONTROL Branding]**.
1. Im Dialogfeld &quot; **Designs** klicken Sie auf **[!UICONTROL Bearbeiten].**
1. Wählen Sie ein beliebiges Design aus und speichern Sie die Änderungen.

   ![](assets/set-themes.png)

   *Beliebiges Design auswählen*

1. Wechseln Sie zum vorherigen Design zurück und speichern Sie die Änderungen.
1. Melden Sie sich vom Adobe-Lernmanager ab und melden Sie sich erneut an.

---
jcr-language: en_us
title: Eine Kenntnis kann nach Abschluss eines Kurses nicht abgerufen werden
description: Ein Teilnehmer erhält auch nach Abschluss eines Kurses keinen Kenntnisnachweis. Die Qualifikationen, die diesem Kurs zugewiesen sind, bleiben für den Teilnehmer als In Bearbeitung erhalten.
contentowner: nluke
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 52%

---



# Eine Kenntnis kann nach Abschluss eines Kurses nicht abgerufen werden

## Problem

Ein Teilnehmer erhält auch nach Abschluss eines Kurses keinen Kenntnisnachweis. Die Kenntnisse, die diesem Kurs zugewiesen sind, bleiben erhalten als **In Bearbeitung** für den Teilnehmer auswählen.

## Ursache

Dieses Problem tritt auf, wenn das **Erforderliche Credits** um diese Fähigkeit zu erreichen, ist größer als die **Verdiente Credits** vom Teilnehmer nach Abschluss des Kurses ändern.

## Lösung

Aktuelle überprüfen **Qualifikationsnachweise** und **Punkt** erforderliche Informationen, um die Kenntnisse zu erwerben. Führen Sie die unten genannten Schritte aus:

1. Generieren Sie für den Teilnehmer einen Bericht **Teilnehmertranskript**.
1. Klicken Sie beim Generieren des Teilnehmertranskripts auf **[!UICONTROL Erweiterte Optionen]** und aktivieren Sie die Option **[!UICONTROL Qualifikationsdaten und Zusammenfassungsblätter einschließen]**.

   ![](assets/advanced-options.png)

   *Wählen Sie die Option Qualifikationsdaten und Zusammenfassungsblätter einschließen.*

1. Öffnen Sie den heruntergeladenen Teilnehmertranskriptbericht.
1. Navigieren Sie zur Seite **[!UICONTROL Kenntnistranskript]**. Hier können Sie die **[!UICONTROL Erforderliche Credits]** und **[!UICONTROL Verdiente Credits]** durch den Teilnehmer ändern.

   Im folgenden Beispiel sind zum Erlangen des Kenntnisnachweises für einen Kurs 50 Credits erforderlich. Der Teilnehmer hat jedoch nur einen Credit erzielt.

   ![](assets/skill-transcript.png)

   *Erforderliche Credits anzeigen*

1. Um Credits zu überprüfen, die bestimmten Kenntnissen zugewiesen sind, melden Sie sich als Administrator an und navigieren Sie zur Registerkarte **Kenntnisse**, wie unten gezeigt:

   ![](assets/skill.png)

   *Registerkarte &quot;Kenntnisse starten&quot;*

1. Um die Anzahl der einem Kurs zugewiesenen Credits zu überprüfen, melden Sie sich als Autor an und öffnen Sie den Kurs. Klicken **[!UICONTROL Einstellungen]** > **Kurskenntnisse** wie folgt:

   ![](assets/course-skills.png)

   *Kurskenntnisse anzeigen*

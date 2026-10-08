---
jcr-language: en_us
title: Dateiübermittlungen können nicht in Adobe Learning Manager angezeigt werden
description: Kursleiter können keine Dateien anzeigen, die die Teilnehmer im Modul für Übermittlungsaktivitäten hochgeladen haben.
contentowner: nluke
exl-id: b4a0af25-14ae-46f1-9afd-0bf2aace7fe2
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 59%
---
# Dateiübermittlungen können nicht in Adobe Learning Manager angezeigt werden

## Ein Problem

Ein Ausbilder kann die von einem Teilnehmer hochgeladenen Dateien nicht anzeigen.

## Beschreibung

Ausbilder können keine Dateien anzeigen, die Teilnehmer im **Einreichungsaktivitätsmodul** hochgeladen haben.

Beispielsweise hatte sich ein Teilnehmer für eine Instanz mit dem Namen **Testinstanz** eines Kurses angemeldet, wie unten gezeigt:

![](assets/test-instance.png)

*Instanz anzeigen*

Der Teilnehmer öffnet dann den Kurs und lädt eine Datei im Aktivitätsmodul hoch.

Wenn der Ausbilder versucht, die Übermittlung zu genehmigen, kann der Ausbilder dies nicht tun.

![](assets/activity.png)

*Datei im Aktivitätsmodul hochladen*

## Ursache

Wenn es in der Kursinstanz keinen Kursleiter gibt, bei dem sich der Teilnehmer registriert hat, wird das Problem angezeigt.

## Lösung

Um zu überprüfen, ob der Kursinstanz ein Ausbilder hinzugefügt wurde, führen Sie die folgenden Schritte aus:

1. Navigieren Sie zu den Kurseinstellungen.
1. Klicken Sie im Abschnitt **Verwalten** auf **[!UICONTROL Instanzen].**.
1. Klicken Sie in der Instanz, in der sich der Teilnehmer registriert hat, auf **[!UICONTROL Sitzungen]**.

   ![](assets/check-instructor.png)

   *Sitzungen in der Instanz auswählen*

   Dieser Sitzung ist kein Kursleiter zugewiesen.

1. Klicken Sie auf **[!UICONTROL Bearbeiten]**. Fügen Sie den Kursleiter hinzu, der die Dateiübermittlung genehmigt.

   ![](assets/assign-instructor.png)

   *Kursleiter hinzufügen*
1. Speichern Sie die Änderungen.

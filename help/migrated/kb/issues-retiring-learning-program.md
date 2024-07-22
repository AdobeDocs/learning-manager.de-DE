---
jcr-language: en_us
title: Probleme beim Einstellen eines Lernprogramms
description: Probleme beim Einstellen eines Lernprogramms in Adobe Learning Manager
contentowner: nluke
exl-id: 706cafe3-2650-4837-9dee-e381a4a711f9
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 55%

---

# Probleme mit dem Einstellen eines Lernprogramms

## Problem

Ein Lernprogramm wird automatisch eingestellt.

## Ursache

Es gibt Situationen, in denen ein Lernprogramm eingestellt wurde, ohne dass ein Administrator/Autor das Lernprogramm explizit eingestellt hat.

Dieses Problem tritt auf, weil ein Lernprogramm eine Sammlung von Kursen ist. Die Schulungen mit höherer Reihenfolge werden eingestellt, wenn einer der darin enthaltenen Kurse eine eingestellte Instanz enthält oder die Kursinstanz eingestellt wird.

## Auflösung

Um den Kurs zu überprüfen, der eine eingestellte Instanz enthält, führen Sie die folgenden Schritte aus:

1. Melden Sie sich als Administrator an und starten Sie das entsprechende Lernprogramm.

1. Klicken Sie auf **[!UICONTROL Instanzen]** > **CKurse**. Auf der Seite werden alle Kurse aufgeführt, die Teil dieses Lernprogramms sind. Sie können den Kurs sehen, der eine eingestellte Instanz enthält.

   ![](assets/retired-instance.png)

   *Liste aller Kurse anzeigen*

1. Nachdem Sie die Kursinstanz gefunden haben, die eingestellt wurde, klicken Sie auf **[!UICONTROL Kurse]** > **[!UICONTROL Kurs öffnen]**.

1. Klicken Sie auf **[!UICONTROL Instanzen]**. Klicken Sie in der eingestellten Instanz auf **[!UICONTROL Bearbeiten]** und ändern Sie dann das Abschlussdatum in ein zukünftiges Datum, zu dem die Instanz eingestellt werden soll.

   ![](assets/completion-date.png)

   *Das Abschlussdatum eines Kurses bearbeiten*

1. Klicken Sie nach Abschluss auf das Dropdown-Menü, wie in der Abbildung unten gezeigt. Klicken Sie dann auf **[!UICONTROL Instanz erneut öffnen]**.

   ![](assets/re-open-instance.png)

   *Instanz eines Kurses erneut öffnen*

1. Besuchen Sie das entsprechende Lernprogramm. Klicken Sie auf **[!UICONTROL Instanzen]** und führen Sie den vorherigen Schritt aus, um die Instanz des Lernprogramms erneut zu öffnen.

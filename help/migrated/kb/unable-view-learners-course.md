---
jcr-language: en_us
title: Teilnehmer in einem Kurs können nicht angezeigt werden
description: Auf der Registerkarte "Teilnehmer" eines Kurses werden keine Teilnehmer angezeigt, die im Adobe-Lernmanager registriert sind. Wenn Sie jedoch einen Bericht generieren, können Sie die registrierten Teilnehmer im Bericht anzeigen.
contentowner: saghosh
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---



# Teilnehmer in einem Kurs können nicht angezeigt werden

## Problem

Sie können die Teilnehmer, die für einen Kurs registriert sind, nicht anzeigen.

## Beschreibung

Auf der Registerkarte &quot;Teilnehmer&quot; eines Kurses werden keine registrierten Teilnehmer angezeigt. Wenn Sie jedoch einen Bericht generieren, können Sie die registrierten Teilnehmer im Bericht anzeigen.

![](assets/no-learners.png)

*Kein Teilnehmer angezeigt*

## Ursache

Wenn sich ein Teilnehmer über ein höheres Lernobjekt (Lernprogramm oder Zertifizierung) registriert hat, wird der Teilnehmer auf der Registerkarte &quot;Teilnehmer&quot; des höheren Lernobjekts angezeigt. Der Teilnehmer kann nicht auf der Registerkarte &quot;Teilnehmer&quot; des Kurses gesucht werden.

**Wie kann ich sehen, bei welchem höheren Lernobjekt der Teilnehmer registriert ist?**

Sie können diese Informationen im Teilnehmertranskriptbericht überprüfen. Um ein Teilnehmertranskript zu generieren, führen Sie die folgenden Schritte aus:

1. Melden Sie sich als Administrator an.
1. Klicken **[!UICONTROL Berichte]** > **[!UICONTROL Benutzerdefinierte Berichte]** > **[!UICONTROL Excel-Berichte]** > **[!UICONTROL Teilnehmertranskript]**.

1. Geben Sie den Namen des **[!UICONTROL Teilnehmer]** und geben Sie den Befehl **[!UICONTROL Datum]** Bereich.
1. Erweitern Sie den Abschnitt **[!UICONTROL Erweiterte Optionen]** und wählen Sie die Option **[!UICONTROL Modulebeneninformationen aktivieren]**.
1. Klicken **[!UICONTROL Generieren]**.

   Im Teilnehmertranskript können Sie sehen, bei welchem höheren Lernobjekt der Teilnehmer registriert ist.

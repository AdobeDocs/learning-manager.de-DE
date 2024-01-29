---
jcr-language: en_us
title: Das automatische Popup mit L1-Feedback wird nicht angezeigt
description: So beheben Sie den Fehler "Automatisches Popup mit L1-Feedback wird nicht angezeigt"
contentowner: saghosh
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---



# Das automatische Popup mit L1-Feedback wird nicht angezeigt

## Problem

Das automatische Popup mit L1-Feedback wird nach Abschluss des Kurses für einen Teilnehmer nicht angezeigt.

## Ursache

Manchmal kann es vorkommen, dass ein Teilnehmer das L1-Feedback nach Abschluss eines bestimmten Kurses nicht erhält oder eine Nachricht erhält, wie unten gezeigt:

![](assets/l1-feedback.png)

*L1-Feedback kann nicht empfangen werden*

Dies kann aus folgenden Gründen passieren:

1. Das Feedback ist nicht für die Anzeige nach Kursabschluss festgelegt.
1. Erinnerungen sind deaktiviert.
1. Eine Erinnerung wird planmäßig nach einer bestimmten Zeit angezeigt.

## Auflösung

1. Stellen Sie sicher, dass die Option &quot;Fragebogen sofort nach Kursabschluss anzeigen&quot; in **Kurs** > **Instanzen** > **L1-Feedback**.
   <!--![](assets/l1-feedback.png)-->
1. Navigieren Sie als Administrator zu **Einstellungen > Feedback**. Überprüfen Sie, wann die Erinnerung geplant ist. Falls es für geplant ist **Nach dem Kurs** Abschluss ändern Sie die Option in **Auf Kurs** Fertigstellung.
1. Aktivieren Sie die folgenden E-Mail-Vorlagen: **E-Mail-Vorlagen > Erinnerungen und Updates > Teilnehmer-Feedback für Kurs anfordern**. Falls die Option deaktiviert ist, aktivieren Sie sie und testen Sie sie dann.
1. Wenn die oben genannten Schritte nicht funktionieren, löschen Sie die Erinnerung in **Admin > Einstellungen > Feedback**. Erstellen Sie eine für &quot;Bei Abschluss des Kurses&quot; und legen Sie die Wiederholung entsprechend den Anforderungen fest.

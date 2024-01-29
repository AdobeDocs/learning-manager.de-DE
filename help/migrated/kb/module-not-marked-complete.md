---
jcr-language: en_us
title: Das Modul wird nach Kursabschluss im Adobe-Lernmanager als unvollständig markiert
description: Auch nachdem ein Teilnehmer einen Kurs im Adobe-Lernmanager abgeschlossen hat, wird das Modul als unvollständig markiert.
contentowner: nluke
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---



# Das Modul wird nach Kursabschluss im Adobe-Lernmanager als unvollständig markiert

## Problem

Auch nachdem ein Teilnehmer einen Kurs im Adobe-Lernmanager abgeschlossen hat, wird das Modul als unvollständig markiert.

## Ursache

SCORM 2004 definiert die Erfolgs- und Abschlusskriterien und sendet die Anweisungen für beide separat.

Angenommen, es ist ein Inhaltssatz mit einer **Abschlusskriterien** von 100 % Folienansichten und **Erfolgskriterien** als &quot;Quiz ist bestanden&quot; festgelegt.

Ein Teilnehmer schließt den Kurs ab, schlägt aber beim Quiz fehl. In diesem Fall ist der Fortschritt 100 %, aber das Modul wird als unvollständig markiert, da der Teilnehmer die **Erfolgskriterien**.

## Lösung

Das Problem hängt mit der Berichterstellung zusammen **Voreinstellungen** für das Projekt festgelegt. Der Autor muss die Kriterien für Abschluss und Erfolg des Kurses überprüfen.

Wenn Änderungen erforderlich sind, kann der Autor dies mit einem Werkzeug zum Erstellen von Inhalten tun, z. B. Adobe Captivate Classic. Der Autor kann das Modul dann entsprechend aktualisieren.

![](assets/scorm.png)

*Captivate Classic-Reporting-Voreinstellungen anzeigen*

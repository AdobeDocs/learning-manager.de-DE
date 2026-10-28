---
description: Erfahren Sie, wie die Webhooks für den Abschluss von Go1-Kursen dazu beitragen, dass Adobe Learning Manager Kursabschlüsse erfasst, selbst wenn die Teilnehmer den Browser früh schließen
jcr-language: en_us
title: Go1-Abschlussverfolgung mit webhooks
exl-id: 25c9c401-905f-4408-89ac-ac630a45a0c7
source-git-commit: aaea92d190b8ab22ce9f08c309faf5caa0b58a69
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%
---

# Go1-Abschlussverfolgung mit webhooks

## Übersicht

Adobe Learning Manager unterstützt jetzt die webhook-basierte Vervollständigungsverfolgung für Go1-Inhalte. Diese Verbesserung verbessert die Zuverlässigkeit der Kursabschlusssynchronisierung zwischen Go1 und Learning Manager. Abschlussereignisse werden auch dann erfasst, wenn Teilnehmer den Kurs-Player direkt nach Abschluss eines Kurses verlassen.

Go1 verwendet Webhooks, um Benachrichtigungen zum Kursabschluss an den Learning Manager zu senden, wenn ein Teilnehmer einen Go1-Kurs abschließt. Learning Manager empfängt und verarbeitet diese Abschlussereignisse unabhängig von der Browsersitzung des Teilnehmers.

Go1 versucht auch die Webhook-Bereitstellung erneut, bis Learning Manager den Eingang des Abschlussereignisses bestätigt. Dadurch können versäumte oder unvollständige Lerndatensätze verhindert werden.

## Problem, das durch diese Verbesserung gelöst wird

Zuvor war die Abschlussverfolgung auf die Kommunikation zwischen dem Go1-Player und dem Lernmanager angewiesen, während die Browsersitzung des Teilnehmers aktiv blieb. Wenn ein Teilnehmer das Browser-Fenster schloss oder wegnavigierte, bevor der Abschlussstatus vollständig verarbeitet wurde, könnte der Abschlussdatensatz verloren gehen.

Das Ergebnis:

* Kursabschlüsse werden möglicherweise nicht in den Teilnehmertranskripten angezeigt.
* Administratoren können Abweichungen zwischen tatsächlichen und aufgezeichneten Abschlüssen feststellen.
* Verpasste Abschlussereignisse konnten nicht automatisch wiederhergestellt werden.

## Ereignis-Workflow

1. Ein Teilnehmer startet und schließt einen Go1-Kurs ab.
1. Go1 zeichnet den Abschluss auf.
1. Go1 sendet ein Webhook zum Abschluss an den Lern-Manager.
1. Learning Manager validiert und akzeptiert das Abschlussereignis.
1. Learning Manager aktualisiert den Abschlussstatus des Teilnehmers.
1. Wenn Learning Manager das Ereignis nicht bestätigt, versucht Go1 die Bereitstellung automatisch erneut.

## Häufige Fragen

**Ist für diese Änderung eine Administratorkonfiguration erforderlich**

Nein, für diese Änderung ist keine Administratorkonfiguration erforderlich.

**Sind vorhandene Go1-Kurse betroffen**

Nein, bestehende Go1-Kurse sind davon nicht betroffen. Die Verbesserung verbessert die Abschlusssynchronisierung für Go1-Inhalte.

**Was passiert, wenn ein Teilnehmer den Browser früh schließt**

Go1 sendet den Abschluss-Webhook unabhängig von der Browsersitzung des Teilnehmers. Auch wenn der Teilnehmer den Kursplayer verlässt, versucht Go1 die Bereitstellung erneut, bis Learning Manager das Abschlussereignis bestätigt.

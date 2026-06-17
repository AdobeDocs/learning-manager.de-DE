---
jcr-language: en_us
title: Berichtsgenerator
description: Einführung in Report Builder
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---


# Report Builder in Adobe Learning Manager

Erstellen und laden Sie benutzerdefinierte Berichte mit den Spalten, Filtern und Daten herunter, die Sie auswählen, ohne ein Werkzeug zur Nachbearbeitung verwenden zu müssen.

Der Report Builder von Adobe Learning Manager bietet Administratoren eine Self-Service-Arbeitsfläche für Berichte, auf der sie genau die Berichte erstellen können, die sie benötigen. Anstatt einen festen Bericht herunterzuladen und in einem Tabellenkalkulationstool neu zu gestalten, wählen Sie die gewünschten Spalten aus, wenden Filter an und laden eine saubere Ausgabe herunter.

## Warum wurde Report Builder eingeführt?

Bestehende Berichte in Adobe Learning Manager wurden behoben. Jeder Bericht verfügt über eine festgelegte Liste von Spalten, die Sie nicht ändern können, und die Filteroptionen sind eingeschränkt. Administratoren, die eine benutzerdefinierte Ausgabe benötigten, mussten mehrere Berichte herunterladen, in Excel daran teilnehmen, Filter manuell anwenden und den Prozess jede Woche oder jeden Monat wiederholen.

Report Builder entfernt diesen Zyklus. Sie konfigurieren einen Bericht einmal, speichern ihn und laden neue Daten herunter, wann immer Sie sie benötigen. Umformungen sind nicht erforderlich.

Drei spezifische Probleme, die Report Builder löst:

* **Behobene Spalten:** Vorhandene Berichte enthalten viele Spalten, die Sie möglicherweise nicht benötigen, und schließen diejenigen aus, die Sie verwenden. Mit Report Builder können Sie nur die Felder auswählen, die für Ihren Anwendungsfall relevant sind.
* **Eingeschränkte Filterung:** Sie können jetzt nach jedem unterstützten Feld filtern. Beispiel: Registrierungsdatum, Abschlussdatum, aktive Felder und Katalogbeschriftungen, nicht nur Status.
* **Inkonsistente Datenquellen:** Vorhandene Berichte können von der Benutzeroberfläche, der Job-API oder den Connectors abgerufen werden, was je nach Zeitpunkt leicht unterschiedliche Daten zurückgeben kann. Da der Report Builder aus einer einzigen, konsistenten Datenquelle abgerufen wird, spiegelt jeder Download dieselben zugrunde liegenden Daten wider.

## Einbindung von Report Builder in vorhandene Berichte

Der Report Builder ersetzt nicht die bestehenden festen Berichte in Adobe Learning Manager. Beide Varianten sind verfügbar. Verwenden Sie vorhandene Berichte für Standardausgaben, auf die Sie sich bereits verlassen. Verwenden Sie Report Builder, wenn Sie benutzerdefinierte Spalten, bestimmte Filter oder Daten benötigen, die derzeit nachbearbeitet werden müssen.

## Wo finde ich Report Builder?

Report Builder ist auf der Administrator-Startseite verfügbar. Wählen Sie **Berichte** und anschließend **Report Builder** aus. Es werden zwei Registerkarten angezeigt: **Vorlagen** und **Berichte**.
8![](assets/report-builder-001.png)

## Wer kann Report Builder verwenden?

Administratoren haben Zugriff auf den Report Builder.

>[!NOTE]
>
>Report Builder muss für Konten aktiviert werden. Wenden Sie sich an Ihr Adobe-Kontoteam oder Ihren CSM, wenn Sie es nicht in Ihrer Administratoransicht sehen.

## Best Practices

* Beginnen Sie mit einer Vorlage, wenn Sie noch nicht mit Report Builder vertraut sind. Vorlagen sind für die gängigsten Anwendungsfälle vorgefertigt und funktionieren sofort.
* Speichern Sie jeden konfigurierten Bericht vor dem Herunterladen. Gespeicherte Berichte können später ohne Neukonfiguration erneut heruntergeladen werden.

---
jcr-language: en_us
title: Einschränkungen des Report Builders in Adobe Learning Manager
description: Erfahren Sie, welcher Report Builder in dieser Version nicht unterstützt wird, damit Sie Ihren Berichtsansatz entsprechend planen können.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# Einschränkungen des Report Builders in Adobe Learning Manager

Report Builder deckt eine Vielzahl benutzerdefinierter Berichtsanforderungen ab, aber einige Berichtstypen, Datensätze und Konfigurationen werden in dieser Version nicht unterstützt. In diesem Abschnitt werden bekannte Einschränkungen aufgeführt und Problemumgehungen vorgeschlagen, sofern verfügbar.

## Wiederkehrende Zertifizierungen

Bestimmte Abfragen mit wiederkehrenden Zertifizierungen funktionieren in dieser Version im Report Builder nicht ordnungsgemäß. Wenn Ihr Bericht sich wiederholende Zertifizierungszyklen umfasst, z. B. die Verfolgung der erneuten Registrierung oder der erneuten Fertigstellung über mehrere Zertifizierungszeiträume, verwenden Sie stattdessen die bestehenden Zertifizierungsberichte in Adobe Learning Manager.

## Nicht unterstützte Datensätze und Berichtstypen

Folgende Funktionen stehen in dieser Version nicht im Report Builder zur Verfügung:

* **Geschäftsergebnisdaten**: Report Builder unterstützt keine BYOD-Integrationen (Bring Your Own Data). Berichte, die externe Geschäftsdaten mit LMS-Daten kombinieren, werden nicht unterstützt.
* **Audit-Berichte**: Systemprüfprotokolle und Administratoraktivitätsprotokolle können nicht in Report Builder erstellt werden. Verwenden Sie für diese Daten die vorhandenen Audit-Berichte in der Administratoransicht.
* **Inkrementelle Berichte**: Report Builder erstellt jedes Mal vollständige Snapshot-Berichte. Inkrementelle Berichte, die nur Datensätze zurückgeben, die seit dem letzten Download geändert wurden, werden nicht unterstützt. Verwenden Sie für inkrementelle Daten die Job-API.

## Einschränkungen durch Trend-Berichte

### Nur eine Datumsspalte pro Trendbericht

Ein einziger Trendbericht kann nur nach einer datumsbasierten Spalte gruppiert werden. Sie können nicht zwei verschiedene datumsbasierte Trends im selben Bericht kombinieren.

Sie können beispielsweise Folgendes erstellen:

* Ein Bericht, der **Registrierungen nach Monat** anzeigt (gruppiert nach Registrierungsdatum)
* Ein separater Bericht, der **Abschlüsse nach Monat** anzeigt (gruppiert nach Abschlussdatum)

Sie können keinen einzelnen Bericht erstellen, der sowohl den Registrierungsmonat als auch den Abschlussmonat als separate Trendspalten anzeigt. Erstellen Sie zwei separate Berichte, und analysieren Sie die beiden Berichte nebeneinander.

### Trends spiegeln aktuelle Daten wider, keine historischen Schnappschüsse

Trendberichte im Report Builder basieren auf aktuellen Point-in-Time-Daten, nicht auf historischen Snapshots. Der Bericht spiegelt den Status der heute vorhandenen Datensätze wider, die über die Datumsfelder verteilt sind.

Dies bedeutet:

* Ein Teilnehmer, der sich im Januar registriert, aber später die Registrierung aufgehoben hat, wird möglicherweise nicht im Registrierungstrend im Januar angezeigt
* Eine Benutzergruppe, die neu organisiert wurde, wird ihre historische Mitgliedschaft in den letzten Monaten nicht widerspiegeln
* Gelöschte Datensätze werden möglicherweise nicht im Trend für den Zeitraum angezeigt, in dem sie aktiv waren.

Verwenden Sie Trendberichte für die Richtungsanalyse. Verwenden Sie für präzise historische Datensätze oder Auditzwecke die vorhandenen festen Berichte oder Job-API-Exporte.

---
jcr-language: en_us
title: Anwenden von Gruppen nach und Aggregationen im Report Builder
description: Fassen Sie Adobe Learning Manager-Berichtsdaten anhand eines ausgewählten Felds zusammen, und berechnen Sie Zählungen, Summen und Prozentwerte für gruppierte Zeilen.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---


# Anwenden von Gruppen nach und Aggregationen im Report Builder

Mithilfe von Gruppierung und Aggregation können Sie zusammenfassende Berichte erstellen, z. B. Gesamtabschlüsse pro Kursleiter, Anzahl der Registrierungen pro Katalog oder Prozentsatz der Konformität nach Region.

## Verwendung von group by

Verwenden Sie group by , wenn Sie eine Zeile pro Kategorie anstelle einer Zeile pro Datensatz verwenden möchten. Beispiel:

* Eine Zeile pro Kursleiter, die angibt, wie viele Sitzungen sie unterrichtet haben
* Eine Zeile pro Katalog, die die Gesamtzahl der Registrierungen anzeigt
* Eine Zeile pro Benutzergruppe, die den Prozentsatz der Konformität anzeigt

Wenn Sie einzelne Teilnehmerdatensätze oder einzelne Registrierungszeilen anzeigen möchten, wenden Sie &quot;Gruppieren nach&quot; nicht an.

Wenn Sie group by auf eine Spalte anwenden, muss auf jede zweite Spalte im Bericht eine Aggregatfunktion angewendet werden. Sie können keinen unformatierten Feldwert neben einer gruppierten Spalte anzeigen - nur einen berechneten Wert (Anzahl, Summe, Durchschnitt usw.).

Wenn Sie beispielsweise nach **Kursleitername** gruppieren, können Sie keine einzelnen **Sitzungsname**-Werte daneben anzeigen. Stattdessen wenden Sie **Anzahl** auf das Feld **Sitzungs-ID** an, um anzuzeigen, wie viele Sitzungen jeder Kursleiter unterrichtet hat.

## Anwenden von Gruppen nach und Aggregationen

In diesem Beispiel vergleichen Sie den Registrierungsfortschritt aller Teilnehmer. In diesem Bericht erfahren Sie, wie verschiedene Manager den Registrierungsfortschritt und den Abschluss überwachen.

### Spalten auswählen

1. Starten Sie **Report Builder**, und wählen Sie **Bericht erstellen** aus.
2. Geben Sie den Namen und die Beschreibung des Berichts ein:
a. **Name:** Fortschritt der Registrierung bei Benutzern vergleichen
b. **Beschreibung:** Dieser Bericht gruppiert Teilnehmer nach Manager und berechnet zusammenfassende Metriken wie die Gesamtzahl der Teilnehmer, den durchschnittlichen Fortschritt und die Anzahl der Abschlüsse für den Registrierungsstatus=ABGESCHLOSSEN
3. Wählen Sie die folgenden Spalten aus: `<dataset>:<column name>`
a. Benutzer-\Managername
b. Benutzer\Name
c. Registrierung\Status
d. Registrierung\Fortschritt in Prozent
e. Lernobjekt-/Abschlussanzahl

### &quot;Nach Spalten gruppieren&quot; auswählen

1. Wählen Sie die folgenden Spalten im Abschnitt **Gruppe nach** aus:
a. Registrierung\Status
b. Benutzer-\Managername
   ![](assets/image020.jpg)
2. Wählen Sie **Anwenden**.

### Auswählen zu aggregierender Spalten

Die aggregierten Funktionen fassen die Registrierungsleistung der Teilnehmer nach Manager und Registrierungsstatus zusammen und zeigen die Anzahl der Teilnehmer, die durchschnittliche Anzahl der Schulungsfortschritte und die durchschnittliche Anzahl der Lernobjektabschlüsse in gruppierten Schulungsdatensätzen an.

1. Wählen Sie **Count Distinct** für Benutzer\Name aus.
2. Wählen Sie **Durchschnitt** für Registrierung\Fortschritt in Prozent.
3. Wählen Sie **Durchschnitt** für Lernobjekt-/Abschlussanzahl aus.
   ![](assets/image021.png)

### Filter anwenden

Wenden Sie Filter an, um nur abgeschlossene Registrierungen einzubeziehen und Datensätze mit fehlenden Managernamen auszuschließen, um sicherzustellen, dass der Bericht gültige Teilnehmerdaten analysiert, um einen genauen Schulungsfortschritt und Abschlusseinblicke zu erhalten.

1. Wenden Sie einen Filter an, wobei _Registrierungsstatus_ gleich _Abgeschlossen_ ist.
2. Wenden Sie einen zweiten Filter an, wobei &quot;_User-Manager Name_&quot; nicht leer ist.
3. Kombinieren Sie beide Filter mit der UND-Bedingung, um nur gültige abgeschlossene Teilnehmerdatensätze einzuschließen.

### Bericht speichern und herunterladen

Wählen Sie **Bericht speichern** aus, und wählen Sie **Aktionen** > **Download** aus, um den Bericht herunterzuladen. Sie erhalten eine Benachrichtigung, dass Sie den Bericht im CSV-Format herunterladen können, sobald er verfügbar ist.

Die CSV-Datei enthält eine verwaltungsmäßige Zusammenfassung der abgeschlossenen Teilnehmerregistrierungen und des Schulungsfortschritts. Jede Zeile stellt einen Manager dar und enthält die Anzahl der Teilnehmer, den Registrierungsstatus, den durchschnittlichen Fortschritt in Prozent und die durchschnittliche Anzahl der Abschlüsse.

Insgesamt vergleicht der Bericht den Abschluss von Schulungen und die Lernaktivität zwischen Managern und hebt die Unterschiede bei der Interaktion der Teilnehmer und die Anzahl der abgeschlossenen Lernobjekte hervor.

---
jcr-language: en_us
title: Berichtsspalten in Report Builder sortieren
description: Wenden Sie eine ein- oder mehrspaltige Sortierung in Adobe Learning Manager Report Builder an, um die Zeilenreihenfolge Ihrer heruntergeladenen Berichte zu steuern.
contentowner: mmanuel
source-git-commit: 8823a5481bc3b34266f7ec36a8f3c26cb923e1ce
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---


# Berichtsspalten in Report Builder sortieren

## Übersicht

Die Sortierung bestimmt die Reihenfolge der Zeilen in der heruntergeladenen Berichtsdatei. Wenden Sie die Sortierung an, wann immer eine konsistente Ausgabe wichtig ist.

## Sortierung hinzufügen

In diesem Beispiel finden Sie heraus, welche Kurse die höchsten Abschlüsse haben.

1. Starten Sie den Report Builder, und wählen Sie **Bericht erstellen**.
2. Geben Sie den Namen und die Beschreibung des Berichts ein.
3. Wählen Sie die folgenden Spalten aus: <dataset>:<column name>

   * Lernobjekt - Lernobjektname
   * Lernobjekt - Status des Lernobjekts
   * Lernobjekt - Abschlussanzahl

4. Wählen Sie im Abschnitt Sortieren die Option **Sortierung hinzufügen**.
5. Wählen Sie **Lernobjekt - Anzahl der Abschlüsse**.
6. Wählen Sie eine Sortierreihenfolge aus: **Aufsteigend** oder **Absteigend**

   ![](assets/report-builder-0034.png)

7. Wählen Sie **Hinzufügen** aus.
8. Wählen Sie **Bericht speichern** aus, und wählen Sie **Aktionen** > **Download** aus, um den Bericht herunterzuladen.

Der heruntergeladene Bericht listet alle Datensätze auf, sortiert nach der Anzahl der Kursabschlüsse.

## Mehrspaltige Sortierung hinzufügen

In diesem Beispiel generieren Sie einen Bericht, um die Performance managerübergreifend zu messen.

So sortieren Sie nach mehreren Spalten:

1. Starten Sie den Report Builder, und wählen Sie **Bericht erstellen**.
2. Geben Sie den Namen und die Beschreibung des Berichts ein.
3. Wählen Sie die folgenden Spalten aus: <dataset>:<column name>

   * Benutzer - Name
   * Benutzer - Name des Managers
   * Modultranskript - Status
   * Modultranskript - Fortschritt in Prozent

4. Fügen Sie die folgenden Aggregate hinzu:

   * Nach Benutzername gruppieren
   * Unterschiedlichen Benutzernamen zählen
   * Count If=COMPLETED Module Transkript - Status
   * Durchschnittliches Modultranskript - Fortschritt in Prozent

   ![](assets/report-builder-0035.png)

5. Fügen Sie im Abschnitt Sortieren die folgende mehrspaltige Sortierung hinzu:

   * <span class="mark">Modultranskript - Status: Absteigend</span>
   * Benutzer - Name des Managers: aufsteigend

   ![](assets/report-builder-0036.png)

6. Wählen Sie **Bericht speichern** aus, und wählen Sie **Aktionen** > **Download** aus, um den Bericht herunterzuladen.

Der heruntergeladene Bericht enthält eine Zusammenfassung der Leistung des Managers, in der die Anzahl der Teilnehmer, die statusbasierte Anzahl der Registrierungen und der durchschnittliche Fortschritt in Prozent angezeigt werden. Er hebt die Teilnahmequoten und den Schulungsfortschritt in den verschiedenen Managergruppen hervor.

---
jcr-language: en_us
title: Berichtsspalten in Report Builder sortieren
description: Wenden Sie eine ein- oder mehrspaltige Sortierung in Adobe Learning Manager Report Builder an, um die Zeilenreihenfolge Ihrer heruntergeladenen Berichte zu steuern.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---


# Berichtsspalten in Report Builder sortieren

Die Sortierung bestimmt die Reihenfolge der Zeilen in der heruntergeladenen Berichtsdatei\. Wenden Sie die Sortierung an, wann immer eine konsistente Ausgabe wichtig ist.

## Sortierung hinzufügen

In diesem Beispiel finden Sie heraus, welche Kurse die höchsten Abschlüsse haben.

1. Starten Sie den Report Builder, und wählen Sie **Bericht erstellen**.
2. Geben Sie den Namen und die Beschreibung des Berichts ein.
3. Wählen Sie die folgenden Spalten aus: `<dataset>:<column name>`
a. Lernobjekt - Lernobjektname
b. Lernobjekt - Status des Lernobjekts
c. Lernobjekt - Abschlussanzahl
4. Wählen Sie im Abschnitt Sortieren die Option **Sortierung hinzufügen**.
5. Wählen Sie **Lernobjekt - Anzahl der Abschlüsse**.
6. Wählen Sie eine Sortierreihenfolge **Aufsteigend** oder **Absteigend**.
   ![](assets/image032.jpg)
7. Wählen Sie **Hinzufügen** aus.
8. Wählen Sie **Bericht speichern** aus, und wählen Sie **Aktionen** > **Download** aus, um den Bericht herunterzuladen.

Der heruntergeladene Bericht listet alle Datensätze auf, sortiert nach der Anzahl der Kursabschlüsse.

## Mehrspaltige Sortierung hinzufügen

In diesem Beispiel generieren Sie einen Bericht, um die Performance managerübergreifend zu messen.

So sortieren Sie nach mehreren Spalten:

1. Starten Sie **Report Builder**, und wählen Sie **Bericht erstellen** aus.
2. Geben Sie den Namen und die Beschreibung des Berichts ein.
3. Wählen Sie die folgenden Spalten aus: `<dataset>:<column name>`
a. Benutzer - Name
b. Benutzer - Name des Managers
c. Modultranskript - Status
d. Modultranskript - Fortschritt in Prozent
4. Fügen Sie die folgenden Aggregate hinzu:
a. Gruppe nach Benutzer - Name des Managers
b. Unterschiedlicher Benutzer zählen - Name
c. Anzahl If=COMPLETED Module Transkript - Status
d. Durchschnittliches Modultranskript - Fortschritt in Prozent
   ![](assets/image033.png)
5. Fügen Sie im Abschnitt **Sortieren** die folgende mehrspaltige Sortierung hinzu:
a. Modultranskript - Status: absteigend
b. Benutzer - Name des Managers: aufsteigend
   ![](assets/image034.jpg)
6. Wählen Sie Bericht speichern und dann Aktionen > Herunterladen , um den Bericht herunterzuladen.

Der heruntergeladene Bericht enthält eine Zusammenfassung der Leistung des Managers, in der die Anzahl der Teilnehmer, die statusbasierte Anzahl der Registrierungen und der durchschnittliche Fortschritt in Prozent angezeigt werden. Er hebt die Teilnahmequoten und den Schulungsfortschritt in den verschiedenen Managergruppen hervor.

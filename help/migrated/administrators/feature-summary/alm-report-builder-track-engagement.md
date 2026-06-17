---
jcr-language: en_us
title: Interaktion in der Report Builder nach Benutzergruppe verfolgen
description: Erstellen Sie einen Bericht in Adobe Learning Manager Report Builder, der die Gesamtzeit für die Registrierung und Registrierung pro Benutzergruppe nach Monat gruppiert enthält.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---


# Interaktion in der Report Builder nach Benutzergruppe verfolgen

Dieser Bericht hilft Schulungsleitern und L&amp;D-Administratoren zu ermitteln, welche Benutzergruppen am aktivsten sind und wie sich die Interaktion Monat für Monat entwickelt. Es verwendet die **Active Field User Group**- und **Enrollment**-Datensätze mit Gruppen-nach- und Aggregatfunktionen, um eine Zusammenfassungszeile pro Benutzergruppe und Monat zu erstellen.

## Bericht &quot;Interaktion nach Benutzergruppe&quot; erstellen

1. Starten Sie **Report Builder**, und wählen Sie **Bericht erstellen** aus.
2. Geben Sie einen Namen ein, z. B. _Engagement nach Benutzergruppe MoM_.
3. Erweitern Sie im Bereich **Spalten** auswählen die **Benutzergruppe für aktives Feld**, und wählen Sie **+** neben **Benutzergruppenname** aus. Die Spalte wird im Bereich **Ausgewählte Spalten** angezeigt.
4. Erweitern Sie **Registrierung** und wählen Sie **+** neben **Registrierungsdatum** aus.
5. Wählen Sie **+** neben **Verbrauchte Zeit**. Wählen Sie das Symbol **Bearbeiten** (Bleistift) aus, und geben Sie den Alias _Aufgewandte Gesamtzeit_ ein.
6. Erweitern Sie **Lernobjekt**, und wählen Sie **+** neben **Anzahl der Registrierungsbenutzer** aus. Wählen Sie das Bearbeitungssymbol aus und geben Sie den Alias _Registrierungen insgesamt_ ein.
7. Wählen Sie **Gruppieren nach: Wählen Sie oben im Bereich** Ausgewählte Spalten **die Option** aus.
8. Wählen Sie **Registrierung - Registrierungsdatum** und legen Sie die Granularität auf **Monat** fest. Wählen Sie **Benutzergruppe für aktives Feld - Benutzergruppenname**. Beide werden als Tags angezeigt: **Registrierung - Registrierungsdatum (Monat)** und **Benutzergruppe für aktives Feld - Benutzergruppenname**.
9. Wählen Sie in der Zeile **Registrierung - Zeitaufwand** die Option **Aggregieren nach** und anschließend **Summe**.
10. Wählen Sie in der Zeile **Lernobjekt - Anzahl der Registrierungsbenutzer** die Option **Aggregieren nach** und anschließend **Anzahl** aus.
   ![](assets/image038.jpg)
11. Wählen Sie **Filter hinzufügen**. Wählen Sie **Registrierung - Registrierungsdatum** und wählen Sie einen relativen Bereich wie **Letzte 3 Monate** aus, oder geben Sie einen bestimmten Datumsbereich ein.
12. Wählen Sie **+ Sortierung hinzufügen**. Sortieren nach **Registrierung - Registrierungsdatum** aufsteigend, dann eine sekundäre Sortierung am **Gesamtdauer** absteigend.
13. Wählen Sie **Bericht speichern** aus, und wählen Sie **Aktionen** > **Download** aus, um den Bericht herunterzuladen.

Der Bericht enthält eine Zeile pro Benutzergruppe und Monat und zeigt die gesamte aufgewendete Zeit und die Gesamtzahl der Registrierungen für diesen Zeitraum an.


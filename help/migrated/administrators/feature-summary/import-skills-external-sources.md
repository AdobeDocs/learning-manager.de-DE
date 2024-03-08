---
jcr-language: en_us
title: Kenntnisse aus externen Quellen importieren
description: Importieren Sie Kenntnisse von Inhaltsanbietern wie LinkedIn und Go1 mithilfe der entsprechenden Connectors.  Die importierten Kenntnisse werden den vom Administrator definierten Kenntnissen im Lern-Manager hinzugefügt und stehen den Autoren während des Workflows zur Kurserstellung zur Verfügung.
contentowner: saghosh
exl-id: 3bcd8fc6-16e4-4f66-a5c6-15b3d606f0c2
source-git-commit: b6228ff242d9fe483de8ea31d7a40935405bda90
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Kenntnisse aus externen Quellen importieren

Importieren Sie Kenntnisse von Inhaltsanbietern wie LinkedIn und Go1 mithilfe der entsprechenden Connectors. Diese Verbesserung ist Teil des Ziels, Learning Manager in die Lage zu versetzen, sich in externe Skills Clouds und Talent Management Systeme zu integrieren. Die importierten Kenntnisse werden den vom Administrator definierten Kenntnissen im Lern-Manager hinzugefügt und stehen den Autoren während des Workflows zur Kurserstellung zur Verfügung. Darüber hinaus wurden Verbesserungen an der Funktionalität zur Kenntnissuche in der gesamten Plattform vorgenommen, um eine bessere Sucherfahrung zu bieten, wenn das Konto über eine große Anzahl von Kenntnissen verfügt.

## Kenntnisimport konfigurieren

Führen Sie die Schritte im Verfahren aus, um den Kenntnisimport in das Konto zu aktivieren.

1. Wählen Sie in der Admin-App **Einstellungen** im linken Bereich.
1. Auswählen **Allgemein**.
1. Im Dialogfeld &quot; **Import von Kenntnissen** Abschnitt, wählen Sie **Aktivieren**. Wenn aktiviert, können Sie eine externe Quelle für den Import auswählen **Kenntnisse**. Die Kenntnisse für vorhandene Lernressourcen werden während der ersten Ausführung einmal in das Kompetenz-Repository importiert. Bei allen nachfolgenden Importen von Lernressourcen werden die Kenntnisse nur für neu importierte Elemente in das Kenntnisrepository importiert.
1. Wählen Sie einen Inhaltsanbieter aus der Dropdown-Liste aus.

Als Administrator können Sie nur eine Qualifikation als Quelle importieren.

### Standardkenntnisstufe

Die standardmäßige Kenntnisstufe ist eins und &quot;Credits&quot; ist 10, nachdem die Kenntnisse migriert wurden. Ein späterer Administrator kann das Guthaben ändern.

Sie können den Namen der Kenntnisse, die Beschreibung und die Stufen externer Kenntnisse nicht bearbeiten. Sie können jedoch Domänen und Abzeichen hinzufügen und Credits bearbeiten.

#### Berichte

Die Spalte **Source** mit Werten: Intern, LinkedIn Learning, Go1, was die Quelle des Kenntnisimports angibt.

Die kürzlich hinzugefügten Kenntnisse werden ganz oben auf der Liste stehen.

Auf der Seite mit den Kurseinstellungen wird die Spalte **Zugewiesen von** mit Werten wie &quot;Intern&quot; und &quot;Inhaltsanbieter&quot;.


## Integration Admin-Arbeitsablauf

Der Integrations-Admin lädt die CSVs (Kenntnisse, Kenntnisstufen und Kurs) hoch und migriert dann die Kurse in das Konto. Nachdem der Administrator beispielsweise LinkedIn Learning ausgewählt hat, kann der Integrationsadministrator eine Aktivität planen, bei der sowohl Kenntnisse als auch Ebenen in den Adobe-Lernmanager importiert werden.

## Kenntnisse exportieren

Als Administrator:

1. Auswählen **Kenntnisse** im linken Bereich.
1. Wählen Sie die Quelle für Kenntnisse aus. Sie können die Kurse, Arbeitshilfen, registrierten Teilnehmer und Kursleiter des Kurses anzeigen.

### Kenntnisse bearbeiten

Wählen Sie Kenntnisse aus. Im Dialogfeld &quot; **Kenntnisse bearbeiten** können Sie den Namen und die Beschreibung der Kenntnisse nicht bearbeiten. Sie können jedoch Kenntnisdomänen und ein Abzeichen für Kenntnisse hinzufügen.

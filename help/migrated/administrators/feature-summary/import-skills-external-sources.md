---
jcr-language: en_us
title: Kenntnisse aus externen Quellen importieren
description: Importieren Sie Kenntnisse von Inhaltsanbietern wie LinkedIn und Go1 mithilfe der entsprechenden Connectors.  Die importierten Kenntnisse werden den vom Administrator definierten Kenntnissen im Lern-Manager hinzugefügt und stehen den Autoren während des Workflows zur Kurserstellung zur Verfügung.
contentowner: saghosh
exl-id: 3bcd8fc6-16e4-4f66-a5c6-15b3d606f0c2
source-git-commit: 260b413b7bb739dc57504df57a6bd2d6a35df161
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Kenntnisse aus externen Quellen importieren

Importieren Sie Kenntnisse von Inhaltsanbietern wie LinkedIn und Go1 mithilfe der entsprechenden Connectors. Diese Verbesserung ist Teil des Ziels, Learning Manager in die Lage zu versetzen, sich in externe Skills Clouds und Talent Management Systeme zu integrieren. Die importierten Kenntnisse werden den vom Administrator definierten Kenntnissen im Lern-Manager hinzugefügt und stehen den Autoren während des Workflows zur Kurserstellung zur Verfügung. Darüber hinaus wurden Verbesserungen an der Funktionalität zur Kenntnissuche in der gesamten Plattform vorgenommen, um eine bessere Sucherfahrung zu bieten, wenn das Konto über eine große Anzahl von Kenntnissen verfügt.

## Kenntnisimport konfigurieren

Führen Sie die Schritte im Verfahren aus, um den Kenntnisimport in das Konto zu aktivieren.

1. Wählen Sie in der Admin-App im linken Fensterbereich **Einstellungen**.
1. Wählen Sie **Allgemein** aus.
1. Wählen Sie im Abschnitt **Qualifikationsimport** die Option **Aktivieren** aus. Wenn diese Option aktiviert ist, können Sie eine externe Quelle auswählen, um Kenntnisse zu importieren. Nach der Aktivierung werden die Kenntnisse für alle nachfolgenden Importe von Lernressourcen in das Kenntnisrepository für neu importierte Elemente importiert. Die Kenntnisse für vorhandene Lernressourcen können einmal in das Kompetenz-Repository importiert werden. Wenden Sie sich an Ihren CSM, um diesen ersten Lauf auszuführen.
1. Wählen Sie einen Inhaltsanbieter aus der Dropdown-Liste aus.

Als Administrator können Sie Kenntnisse nur aus einer Kenntnisquelle importieren.

### Standardkenntnisstufe

Die standardmäßige Kenntnisstufe ist eins und &quot;Credits&quot; ist 10, nachdem die Kenntnisse migriert wurden. Ein späterer Administrator kann das Guthaben ändern.

Sie können den Namen der Kenntnisse, die Beschreibung und die Stufen externer Kenntnisse nicht bearbeiten. Sie können jedoch Domänen und Abzeichen hinzufügen und Credits bearbeiten.

### Standardkurskenntnisse und Credits

Nachdem Sie Kenntnisse importiert haben, werden sie den Lernressourcen hinzugefügt, die aus der Quelle importiert wurden, die als Kenntnisquelle ausgewählt wurde. Wenn Ihre Kenntnisquelle beispielsweise &quot;LinkedIn Learning&quot; war, verfügen alle aus LinkedIn Learning importierten Lernressourcen über die Kenntnisse, die darin bereitgestellt werden. Beim Import in Lernressourcen weist jede Lernressource einen Standardwert von 10 Credits auf.

#### Berichte

Die Spalte &quot;**Quelle**&quot; mit den Werten &quot;Intern&quot;, &quot;LinkedIn Learning&quot;, &quot;Go1&quot;, die die Quelle des Kenntnisimports angibt.

Die kürzlich hinzugefügten Kenntnisse werden ganz oben auf der Liste stehen.

Auf der Seite mit den Kurseinstellungen wird die Spalte &quot;**Assigned by**&quot; mit den Werten &quot;Internal&quot; (Intern) und &quot;Content Provider&quot; (Inhaltsanbieter) angezeigt.


## Integration Admin-Arbeitsablauf

Der Integrations-Admin lädt die CSVs (Kenntnisse, Kenntnisstufen und Kurs) hoch und migriert dann die Kurse in das Konto. Nachdem der Administrator beispielsweise &quot;LinkedIn Learning&quot; ausgewählt hat, kann der Integrationsadministrator eine Aktivität planen, bei der sowohl Kenntnisse als auch Ebenen in Adobe Learning Manager importiert werden.

## Kenntnisse exportieren

Als Administrator:

1. Wählen Sie im linken Teilfenster **Kenntnisse** aus.
1. Wählen Sie die Quelle für Kenntnisse aus. Sie können die Kurse, Arbeitshilfen, registrierten Teilnehmer und Kursleiter des Kurses anzeigen.

### Kenntnisse bearbeiten

Wählen Sie Kenntnisse aus. Im Popup **Kenntnisse bearbeiten** können Sie den Namen und die Beschreibung der Kenntnisse nicht bearbeiten. Sie können jedoch Kenntnisdomänen und ein Abzeichen für Kenntnisse hinzufügen.

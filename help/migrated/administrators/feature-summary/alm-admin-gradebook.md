---
description: Alles über das Aktivieren des Gradebooks und dessen Sichtbarkeit für Autoren und Teilnehmer
jcr-language: en_us
title: Schulungsbuch für Administratoren
source-git-commit: 971576b95ab0f75b9d28a7f3d1d62440927925f7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 1%

---


# Gradebook-Sichtbarkeit für Ihr Konto aktivieren

## Übersicht

Bevor Autoren den Teilnehmern in einem Kurs das Schulungsbuch anzeigen können, muss ein Administrator die Einstellung für die Anzeige des Schulungsbuchs auf Kontoebene aktivieren. Diese Einstellung fungiert als Hauptschalter: Wenn sie deaktiviert ist, können die Teilnehmer das Schulungsbuch in keinem Kurs sehen, unabhängig davon, wie einzelne Kurse konfiguriert sind.

## Was diese Einstellung steuert

Die Einstellung **Gradebook Visibility** in **Einstellungen** > **Allgemein** bestimmt, ob Autoren das Gradebook Teilnehmern auf Kursebene zur Verfügung stellen dürfen.

| Festlegen des Status | Effekt |
| --- | --- |
| Aktiviert | Autoren können die Sichtbarkeit von Schulungsunterlagen pro Kurs mithilfe der Option **Schulungsbuch für Teilnehmer anzeigen** im Kurseditor steuern. Teilnehmer sehen die Registerkarte **Gradebook** in Kursen, in denen der Autor sie aktiviert hat. |
| Deaktiviert | Die Teilnehmer können das Schulungsbuch in keinem Kurs sehen. Wenn sie deaktiviert ist, verfügt die Kurskonfiguration nicht über die Einstellung, um den Teilnehmern das Schulungsbuch anzuzeigen. |


Dies bedeutet, dass die Einstellung auf Kontoebene und die Einstellung auf Kursebene zusammenwirken. Beide müssen aktiviert sein, damit ein Teilnehmer das Schulungsbuch sehen kann.

## Gradebook-Sichtbarkeit aktivieren

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.
2. Wählen Sie in der linken Navigation **Einstellungen**.
3. Wählen Sie **Allgemein** aus.
4. Scrollen Sie zum Abschnitt **Gradebook Visibility**.
5. Aktivieren Sie das Kontrollkästchen **Gradebook-Ansicht für Teilnehmer aktivieren**.

   ![](assets/gradebook-admin-1.png)

Autoren können jetzt die Gradebook-Sichtbarkeit pro Kurs konfigurieren.

## Auswirkungen auf die Workflows von Autoren

Wenn diese Einstellung auf Kontoebene aktiviert ist, ist der Schalter **Kursbuch für Teilnehmer anzeigen** im Kurseditor verfügbar. Autoren verwenden diesen Schalter, um pro Kurs zu entscheiden, ob Teilnehmer die Registerkarte **Gradebook** sehen können.

Wenn diese Einstellung auf Kontoebene deaktiviert ist:

* Der Schalter **Schulungsbuch für Teilnehmer anzeigen** im Kurseditor wird möglicherweise weiterhin angezeigt, aber jede Konfiguration auf Kursebene wird überschrieben. Teilnehmer sehen das Schulungsbuch nicht.
* Notenbuchbewertungen und gewichtete Berechnungen werden für Administratorberichtszwecke weiterhin im Hintergrund ausgeführt.
* Administratoren und benutzerdefinierte Administratoren können weiterhin Teilnehmertranskripte mit Schulbuchdaten herunterladen.

>[!NOTE]
>
>Wenn Sie diese Einstellung auf Kontoebene deaktivieren, werden keine Gradebook-Konfigurationen oder -Punktzahlen gelöscht. Wenn Sie sie wieder aktivieren, werden alle zuvor konfigurierten Schulungsbucheinstellungen auf Kursebene sofort wiederhergestellt.

## Wie die beiden Einstellungen interagieren

| Einstellungen auf Kontoebene | Einstellung auf Kursebene | Was der Teilnehmer sieht |
| --- | --- | --- |
| Aktiviert | Schulungskalender für Teilnehmer anzeigen: **Am** | Registerkarte **Gradebook** im Kurs-Player sichtbar |
| Aktiviert | Schulungskalender für Teilnehmer anzeigen: **Aus** | Registerkarte &quot;Kein Schulungsbuch&quot; nur intern berechnete Punktzahl |

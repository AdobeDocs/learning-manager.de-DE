---
description: Alles über das Aktivieren des Gradebooks und dessen Sichtbarkeit für Autoren und Teilnehmer
jcr-language: en_us
title: Schulungsbuch für Administratoren
source-git-commit: 2f1a64abe8be62bfc23da052232d6ceb1202ebad
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---


# Gradebook-Sichtbarkeit für Ihr Konto aktivieren

## Übersicht

Bevor Autoren den Teilnehmern in einem Kurs das Schulungsbuch anzeigen können, muss ein Administrator die Einstellung für die Anzeige des Schulungsbuchs auf Kontoebene aktivieren. Diese Einstellung fungiert als Hauptschalter: Wenn sie deaktiviert ist, können die Teilnehmer das Schulungsbuch in keinem Kurs sehen, unabhängig davon, wie einzelne Kurse konfiguriert sind.

## Was diese Einstellung steuert

Die Einstellung **Gradebook Visibility** in **Einstellungen** > **Allgemein** bestimmt, ob Autoren das Gradebook Teilnehmern auf Kursebene zur Verfügung stellen dürfen.

Weitere Informationen finden Sie unter [Gradebook Visibility](/help/migrated/administrators/feature-summary/settings/basic-settings.md#gradebookvisibility).

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

## Anzeigen und Berichten von Notenbuchbewertungen

Administratoren in Adobe Learning Manager können gewichtete Notizbuchergebnisse für alle registrierten Teilnehmer in einem Kurs anzeigen, die Leistung der einzelnen Teilnehmer nach Modul anzeigen, ein gefiltertes Teilnehmertranskript herunterladen und die Konfigurationsänderungen des Notizbuchs im Bericht &quot;Inhaltsprüfpfad&quot; verfolgen.

## Schulungskalender für einen Kurs anzeigen

Wenn das Notizbuch für einen Kurs aktiviert ist, wird in der linken Navigation unter **Berichte** ein neuer Abschnitt **L2 Feedback - Notizbuch** angezeigt, wenn Sie den Kurs öffnen.

* Melden Sie sich bei Adobe Learning Manager als Administrator an.
* Wählen Sie in der linken Navigation **Kurse** aus und öffnen Sie den Kurs, den Sie überprüfen möchten.
* Wählen Sie in der Kursnavigation unter **Berichte** die Option **L2 Feedback - Schulungsbuch**. Die Seite **Gradebook für aktives Feedback** wird geöffnet.

  ![](assets/image_0013.png)

Es zeigt:

1. Die Kriterien für das Bestehen des Kurses (erforderliche Mindestmodule und minimale Gesamtpunktzahl)
2. Eine Filterzeile, um Teilnehmer nach Stufe anzuzeigen: **Übergeben**, **Fehlgeschlagen** oder **Abschluss ausstehend**
3. Die Formel für die Gesamtpunktzahl: Gesamtpunktzahl = ÷ (Punktzahl erreicht Höchstpunktzahl) × Gewicht für jedes Modul
4. Eine Teilnehmerliste, die die **Gesamtpunktzahl des Teilnehmers** und seine Punktzahl für jedes bewertete Modul anzeigt
5. Dropdown-Liste mit Instanzen, um zwischen Kursinstanzen zu wechseln, wenn ein Kurs mehrere Instanzen hat

Teilnehmer, die noch keine bewerteten Module ausprobiert haben, zeigen in den Punktzahlspalten Bindestriche an. Module, die keine Bewertung, PDF, Video, Audio und Ähnliches unterstützen, werden nicht als Bewertungsspalten angezeigt.

## Anzeigen der Punktzahlen eines einzelnen Teilnehmers

Wählen Sie im **Gradebook für aktives Feedback** den Namen eines Teilnehmers aus.

![](assets/image_0014.png)

In der Ansicht &quot;Einzelner Teilnehmer&quot; wird Folgendes angezeigt:

1. Name, E-Mail-Adresse und Status des Teilnehmers (**Abschluss ausstehend**, **Bestanden** oder **Nicht bestanden**)
2. Die Gesamtpunktzahl und die Anzahl der erforderlichen Module, die der Teilnehmer abgeschlossen hat
3. Eine Modultabelle, die Folgendes zeigt: Modulname, Typ, ob erforderlich, Status, Gewichtung, erreichte Punktzahl und Beitrag zum Aggregat

Die Modultabelle enthält alle bewertbaren und nicht bewertbaren Module. Bewertungsmodule zeigen ihre Punktzahl und ihren Beitrag an. Nicht bewertbare Module zeigen Bindestriche in den Spalten &quot;Punktzahl&quot; und &quot;Beitrag&quot;.

## Bewertungsmodule

Das Bewertungsverhalten für Administratoren und Kursleiter bleibt gegenüber dem aktuellen Arbeitsablauf unverändert:

* **SCORM-, AICC-, xAPI- und native Quizmodule** werden automatisch bewertet, wenn der zugrunde liegende Inhalt eine Punktzahl meldet.
* **Klassenzimmersitzungen, virtuelle Klassenzimmersitzungen und Aktivitätsmodule** werden von Kursleitern oder Administratoren auf der Seite **Anwesenheit und Punktzahl** bewertet.

## Teilnehmertranskript für einen Kurs herunterladen

Sie können ein in diesen Kurs gefiltertes Teilnehmertranskript auf eine der beiden folgenden Arten direkt von der Schulbuchseite herunterladen:

* Wählen Sie im **Gradebook für aktives Feedback** in der oberen rechten Ecke der Seite die Option **Teilnehmertranskript herunterladen**.
* Wählen Sie auf der Startseite des Administrators **Berichte** und anschließend **Benutzerdefinierte Berichte** aus. Wählen Sie **Teilnehmertranskripte** aus der Liste der verfügbaren Berichte aus.

>[!NOTE]
>
>Beim Teilnehmertranskript (CSV-Bericht und Jobs-API) wird die Gewichtung als Spalte hinzugefügt, wenn das Schulungsbuch auf Kursebene aktiviert ist.


## Inhaltsprüfpfadereignisse

Der Inhaltsprüfpfad erfasst zwei gradebook-spezifische Konfigurationsereignisse:

| **Ereignis** | **Wenn sie angezeigt wird** |
|-----------|---------------------|
| **Gradebook aktualisiert** | Wenn ein Autor ein Schulungsbuch für einen Kurs aktiviert oder deaktiviert |
| **Modulgewicht aktualisiert** | Wenn ein Autor den Gewichtungsprozentsatz für ein Modul ändert |

Weitere Informationen finden Sie unter Melden von Änderungen in der Version .

Verwenden Sie diese Einträge, um zu verfolgen, wer die Gradebook-Konfiguration und wann geändert hat, insbesondere in Umgebungen, in denen mehrere Autoren am selben Kurs zusammenarbeiten.

## Fehlerbehebung

**Der Abschnitt L2 Feedback - Gradebook wird in der Kursnavigation nicht angezeigt**

Das Schulungsbuch muss vom Kursautor aktiviert werden, wenn er den Kurs erstellt. Vergewissern Sie sich, dass der Autor das Schulungsbuch für die Kurserstellung aktiviert hat. Wenn der Kurs erstellt wurde, bevor das Schulungsbuch verfügbar war, kann er nicht rückwirkend hinzugefügt werden. Eine neue Kursversion ist erforderlich.

**Die Gesamtpunktzahl eines Teilnehmers ist trotz abgeschlossener Module 0**

Vergewissern Sie sich, dass dem Kurs mindestens ein bewertbares Modul mit einem zugewiesenen Gewichtungswert zugeordnet ist. Wenn alle vom Teilnehmer abgeschlossenen Module nicht bewertbar sind (PDF, Video, Audio), wird keine Gesamtpunktzahl berechnet. Bestätigen Sie außerdem, dass die bewerteten Module noch nicht den Status &quot;**Ausstehende Überprüfung**&quot; aufweisen. Unbewertete Module werden aus der Aggregation ausgeschlossen, bis ein Kursleiter eine Punktzahl eingibt.

**Die Gewichtungsspalte fehlt im heruntergeladenen Teilnehmertranskript**

Diese Spalte wird nur angezeigt, wenn das Notenbuch aktiviert ist und in mindestens einem Modul ein Gewichtungswert gespeichert ist. Bestätigen Sie, dass der Autor das Notenbuch aktiviert und die Gewichtungswerte auf insgesamt 100 % gespeichert hat.

**Ein Teilnehmer hat alle erforderlichen Module abgeschlossen, zeigt jedoch &quot;Abschluss ausstehend&quot; an**

Ein oder mehrere Module warten möglicherweise noch auf eine Punktzahl von einem Kursleiter oder Administrator (**Status &quot;Überprüfung ausstehend&quot;**). Der Kurs kann erst abgeschlossen werden, wenn in allen erforderlichen Modulen sowohl ein Abschluss als auch eine Punktzahl aufgezeichnet wurden. Geben Sie die ausstehende Punktzahl aus **Anwesenheit und Punktzahl** ein, um den ausstehenden Status zu löschen.

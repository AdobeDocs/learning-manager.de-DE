---
description: Dieses Dokument fasst die Berichterstellungsänderungen im August 2026 in Adobe Learning Manager zusammen. Es deckt neue und aktualisierte Spalten im Teilnehmertranskript, in der Schulung, der Registrierung, der Warteliste, der Anwesenheit, der Inhaltsüberwachung und in Benutzerberichten ab. Außerdem werden das adaptive Kursverhalten, die Bewertung in Schulungsunterlagen, externe Lerndatensätze, KI-Bonitätsberichte der Generationen, die Verfolgung von Stammzertifizierungen, die Zeitstempelstandardisierung und API-Autor-Updates erläutert.
jcr-language: en_us
title: Meldungsänderungen in der Version August 2026 von Adobe Learning Manager
source-git-commit: 5c32d300f6e66e154a5c993a0d9701254ac8b4ce
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 2%

---


# Meldungsänderungen in der Version August 2026 von Adobe Learning Manager

Die Adobe Learning Manager-Version vom August 2026 bietet Berichtsverbesserungen für das gesamte Schulungsmaterial, das externe Lernen, die Nutzung von KI-Krediten der Generation und vieles mehr. In diesem Artikel werden die neuen Spalten, Berichte und Verhaltensänderungen zusammengefasst, die Administratoren in dieser Version zur Verfügung stehen.

## Was hat sich verändert

Die Berichterstattungsaktualisierungen erstrecken sich auf acht Funktionsbereiche: Notizbuchbewertung, externes Lernen, inkrementelle Benutzerexporte, Verwendung von KI-Guthaben der Generation, Verfolgung der Stammzertifizierungen und Ausrichtung der Webhook-Zeitstempel. Die Änderungen wirken sich am stärksten auf die folgenden Berichte aus:

- Teilnehmertranskript (LT)
- Schulungsbericht
- Registrierungsbericht
- Wartelistenbericht
- Inhaltsprüfungsbericht

Die meisten Aktualisierungen führen neue Spalten ein. Einige führten neue Berichtstypen ein. Einige haben die Modellierung oder Formatierung vorhandener Daten geändert.

<!--
## Adaptive course reporting changes

### Training report

Three new columns in the Training report support adaptive course behavior.

| **Column**               | **Description**                                          | **Supported Values**                                                   |
|--------------------------|----------------------------------------------------------|------------------------------------------------------------------------|
| Adaptive Learning Object | Identifies whether a course is adaptive                  | true (adaptive), false (non-adaptive)                                  |
| Visibility User Groups   | Lists user groups that can view each module              | One or more user group names (for example, All Learners, UG-Australia) |
| Mandatory                | Indicates whether a module is mandatory for a user group | User group names for which the module is mandatory; blank = optional   |

You can combine **Visibility User Groups** and **Mandatory** to interpret adaptive completion rules directly in the report. For example, a module may be visible to **All Learners** but mandatory only for the **Administrator group**.


### Learner Transcript

A new **Previous Completions** column captures historical completion data when adaptive logic triggers recompletion.

| **Sub-field**         | **Description**                         |
|-----------------------|-----------------------------------------|
| completionRefreshDate | Timestamp when the completion was reset |
| completedDate         | Previous completion timestamp           |
| progressAtRefresh     | Learner progress before reset           |
| gradeAtRefresh        | Learner score at the time of reset      |

The Learner Transcript now supports multiple completion cycles. When a recompletion event occurs, for example, due to course updates or new mandatory modules, the previous completion moves to the **Previous Completions** column. The current completion remains in the standard transcript fields.

### Enrollment report

A new **Waitlisted** column indicates whether a learner is waitlisted in any module within a course.

| **Value** | **Meaning**                                             |
|-----------|---------------------------------------------------------|
| true      | The learner is waitlisted in one or more modules        |
| false     | Learner has confirmed enrollment in all visible modules |

### Waitlist report

Two new columns and an enhanced status-detail support module enable waitlist tracking at the module level.

| **Column**      | **Description**                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Module**      | Name of the module (classroom or virtual classroom session) where the learner is waitlisted. Appears after the Instance Status column. |
| **Module ID**   | Identifier of the module where the learner is waitlisted. Appears after the Module column.                                             |
| **Embedded In** | The learning path name and ID of any learning path that contains this course. Blank if the course is not part of a learning path.      |

The Waitlist report has shifted from a course-level model to a module session–level model. A learner can now be enrolled in some modules and waitlisted in others. The report also supports waitlist tracking within Flex learning paths, where seat limits are enforced at the module level.

### LP Enrollment report

The Learning Path Enrollment report also receives a new **Remarks** column. When a learner is in a waitlisted state on any classroom or virtual classroom session within the courses that make up the learning path, the Remarks column shows **Waitlisted**. When all sessions are confirmed, the column is blank.

### Attendance report

The **Learner status** column now distinguishes between confirmed and waitlisted learners.

| **Value**  | **Meaning**                            |
|------------|----------------------------------------|
| Confirmed  | The learner has an allocated seat      |
| Waitlisted | The learner is pending seat allocation |

-->

## Berichterstellungsänderungen im Gradebook

### Teilnehmertranskript

Eine neue Spalte **Gewicht** stellt den Beitrag jedes bewertbaren Moduls zum Gesamtkursergebnis dar.

| **Wert** | **Beschreibung** |
|----------------------------------------------|------------------------------------------------------|
| Numerischer Prozentsatz (z. B. 20, 30, 50) | Beitrag des Moduls zum Kursergebnis |
| Leer | Modul ist nicht bewertbar (z. B. PDF oder Videos) |

### Inhaltsprüfungsbericht

Zwei neue Ereignisse erfassen Änderungen an der Konfiguration der Schulungsunterlagen.

| **Ereignis** | **Wird ausgelöst, wenn** | **Erfasste Daten** |
|-----------------------|-----------------------------------------------------------------|----------------------------------------------------------|
| Notenbuch aktualisiert | Schulungsunterlagen werden auf Kursebene aktiviert, deaktiviert oder geändert | Änderung des Gradientenbuchstatus; Konfigurationsaktualisierungen für die Bewertung |
| Modulgewichtung aktualisiert | Das einem Modul zugewiesene Gewicht wird geändert | Modulkennung; aktualisierter Gewichtungswert |

Das Teilnehmertranskript spiegelt die neueste Gewichtung wider. Der Inhaltsprüfungsbericht verfolgt historische Änderungen. Zusammen geben sie Ihnen ein vollständiges Bild der aktuellen Bewertungslogik und ihrer Entwicklung.

## Änderungen an externen Lern-Berichten

### Teilnehmertranskript

Drei neue Spalten werden hinzugefügt, um externe Lerndatensätze zu unterstützen.

| **Spalte** | **Beschreibung** |
|------------------------|-----------------------------------------------------------------------------------------------------|
| Name des externen Lernprogramms | Name der externen Lernaktivität, die vom Teilnehmer gesendet wurde |
| Benutzerdefinierte Felder | Eine Spalte pro benutzerdefiniertem Feld, das für externes Lernen konfiguriert ist (Text, numerisch, Kontrollkästchen oder Dropdown) |
| Abschlusskommentar | Anmerkungen des Managers, die während der Genehmigung oder Ablehnung eingegeben wurden |

**Hinweis:** Im Teilnehmertranskript (Teilnehmer-Self-Service-Ansicht) unterscheidet sich die Spaltenplatzierung vom Admin-Teilnehmertranskript:

- **Der Name für externes Lernen** wird unmittelbar nach der vorhandenen Spalte **Modul** hinzugefügt.

- **Der Abschlusskommentar** wird unmittelbar nach der vorhandenen Spalte **Anmerkungen des Reviewers** hinzugefügt.

- Spalten für benutzerdefinierte Felder (eine pro konfiguriertes benutzerdefiniertes Feld) werden am Ende des Transkripts angehängt.

Im Admin-Teilnehmertranskript werden alle neuen Spalten, einschließlich Name des externen Lernprogramms und Abschlusskommentar, am Ende angehängt, gefolgt von benutzerdefinierten Feldspalten.

### Spalte &quot;Typ&quot; im Teilnehmertranskript

Externe Lerneinträge werden jetzt neben vorhandenen Lernobjekten (Kursen, Lernpfaden, Zertifizierungen) in Administrator LT angezeigt. Die Spalte **Type** enthält eine neue externe Lernklassifizierung für eine einfache Filterung.

Externe Lerndaten fließen sowohl in das Teilnehmertranskript als auch in die Admin LT. Kernfelder wie Abschlussdatum, Status und Punktzahl werden vorhandenen Spalten zugeordnet. Benutzerdefinierte Felder werden als zusätzliche Spalten angehängt.

## Inkrementelle Änderungen an Benutzerberichten

Mit einem neuen inkrementellen Exportmodell können Sie nur Benutzer exportieren, deren Daten sich in einem bestimmten Zeitfenster geändert haben, anstatt jedes Mal vollständige Datenexporte zu generieren.

| **Exportmodus** | **Verhalten** |
|--------------------|-----------------------------------------------------------------|
| Vollständiger Export | Gibt alle Benutzer im Konto zurück |
| Inkrementeller Export | Gibt nur Benutzer mit Änderungen innerhalb des angegebenen Datumsbereichs zurück. |

Um den inkrementellen Export zu verwenden, filtern Sie nach **von Datum** und **bis Datum**, um das Änderungsfenster zu definieren. Benutzerberichte werden jetzt mithilfe einer Datenplattform-Pipeline generiert und die Ausgabe wird in Blöcken zurückgegeben, um große Konten zu unterstützen.

## Generelle KI-Erstellung von Kreditauswertungen

Ein neues Credit-Dashboard und zwei Berichte geben Administratoren einen Einblick in den Kreditverbrauch der Generation AI.

### Credit-Dashboard

Das Dashboard zeigt die folgenden Metriken auf Kontoebene an.

| **Metrik** | **Beschreibung** |
|-------------------|---------------------------------------------------|
| Gekaufte Credits | Für das Konto bereitgestellte Credits insgesamt |
| Verwendete Credits | Über KI-gestützte Funktionen hinweg genutzte Credits |
| Verbleibende Credits | Nach Verbrauch verfügbare Credits |
| Nutzung pro Funktion | Kreditverbrauch geteilt nach KI-Funktion |

### Neue Berichte

| **Bericht** | **Beschreibung** |
|----------------------|---------------------------------------------------------------------------------------------|
| Bericht über die monatliche Nutzung | Fasst den Kreditverbrauch nach Monat, Funktion und genutzten Credits zusammen |
| Audit-Bericht | Stellt Details auf Benutzerebene bereit: Benutzer-ID, Funktionsname, verbrauchte Credits und Zeitstempel |

## Sonstige Verhaltensänderungen

### Stammzertifizierung: Stammtrainings-ID

Eine neue **Stammtrainings-ID**-Spalte wird am Ende des **Admin-Teilnehmertranskripts** und des **Teilnehmertranskripts** (Teilnehmer-Self-Service-Ansicht) hinzugefügt. Es erfasst den eindeutigen Bezeichner, der alle Wiederholungen einer Zertifizierung mit einer einzigen Stammentität verknüpft. Dies ermöglicht es, alle sich wiederholenden Instanzen einer Zertifizierung mit einer einzigen Stamm-ID für die Verfolgung und Filterung zu verknüpfen.

### Standardisierung von Webhook- und Teilnehmertranskriptzeitstempeln

Webhook-Zeitstempel sind jetzt an der Formatierung des Teilnehmertranskripts ausgerichtet. Für jedes Datums- und Zeitfeld im **Datenobjekt** einer Webhook-Payload ist jetzt der Sekundenwert auf 00 festgelegt, wodurch die Detailgenauigkeit auf Minutenebene mit den Teilnehmertranskriptberichten konsistent ist. Dadurch entfällt die Notwendigkeit, Zeitstempelformate zu normalisieren, wenn Webhook-Daten mit Teilnehmertranskriptdaten verglichen werden.

### Informationen zum Autor in der API-Antwort für freigegebene Kurse

Wenn ein Kurs von einem Adobe Learning Manager-Konto für ein anderes über die Katalogfreigabe freigegeben wird, gibt die Lernobjekt-Antwort (LO) der API jetzt nur die ursprünglichen Autorendetails aus dem Quellkonto zurück. Zuvor war der Administrator des akzeptierenden Kontos der Kursverfasser in der API-Antwort für sein Konto.

Diese Änderung betrifft nur Peer-Konten (Empfangskonten). Wenn Sie den LO-Detailendpunkt für einen freigegebenen Kurs in einem empfangenden Konto abfragen, gibt das Feld &quot;authorNames&quot; jetzt den ursprünglichen Autor aus dem Quellkonto wieder und nicht den Administrator des empfangenden Kontos.

Es gibt keine Änderungen daran, wie Autorendetails angezeigt werden, wenn Sie das LO im Quellkonto abfragen.

**Hinweis:** Wenn sich Ihre Integration bei freigegebenen Kursen auf das Feld &quot;authorNames&quot; in der LO-API-Antwort stützt, stellen Sie sicher, dass die aktualisierten Autorendaten keine Downstream-Logik beschädigen, die davon ausging, dass der Administratorname des empfangenden Kontos in diesem Feld angezeigt wird.

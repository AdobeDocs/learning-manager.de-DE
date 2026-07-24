---
description: Dieses Dokument fasst die Berichterstellungsänderungen im August 2026 in Adobe Learning Manager zusammen. Es deckt neue und aktualisierte Spalten im Teilnehmertranskript, in der Schulung, der Registrierung, der Warteliste, der Anwesenheit, der Inhaltsüberwachung und in Benutzerberichten ab. Außerdem werden das adaptive Kursverhalten, die Bewertung in Schulungsunterlagen, externe Lerndatensätze, KI-Bonitätsberichte der Generationen, die Verfolgung von Stammzertifizierungen, die Zeitstempelstandardisierung und API-Autor-Updates erläutert.
jcr-language: en_us
title: Meldungsänderungen in der Version August 2026 von Adobe Learning Manager
source-git-commit: 2d60f665d2e00c95edfc96360ee65fdae013c0cd
workflow-type: tm+mt
source-wordcount: '1434'
ht-degree: 2%

---


# Meldungsänderungen in der Version August 2026 von Adobe Learning Manager

Die Adobe Learning Manager-Version vom August 2026 bietet Berichterstellungsverbesserungen für adaptive Kurse, Schulungskurse, externes Lernen, Nutzung von KI-Krediten der Generation und mehr. In diesem Artikel werden die neuen Spalten, Berichte und Verhaltensänderungen zusammengefasst, die Administratoren in dieser Version zur Verfügung stehen.

## Was hat sich verändert

Die Berichterstattungsaktualisierungen erstrecken sich auf acht Funktionsbereiche: adaptives Kursverhalten, adaptive Warteliste, Notizbuchbewertung, externes Lernen, inkrementelle Benutzerexporte, Nutzung von KI-Guthaben der Generation, Verfolgung der Stammzertifizierung und Ausrichtung der Webhook-Zeitstempel. Die Änderungen wirken sich am stärksten auf die folgenden Berichte aus:

- Teilnehmertranskript (LT)
- Schulungsbericht
- Registrierungsbericht
- Wartelistenbericht
- Inhaltsprüfungsbericht

Die meisten Aktualisierungen führen neue Spalten ein. Einige führten neue Berichtstypen ein. Einige haben die Modellierung oder Formatierung vorhandener Daten geändert.

## Änderungen bei der adaptiven Kursberichterstattung

### Schulungsbericht

Drei neue Spalten im Schulungsbericht unterstützen das adaptive Kursverhalten.

| **Spalte** | **Beschreibung** | **Unterstützte Werte** |
|--------------------------|----------------------------------------------------------|------------------------------------------------------------------------|
| Adaptives Lernobjekt | Gibt an, ob ein Kurs adaptiv ist. | true (adaptiv), false (nicht adaptiv) |
| Sichtbarkeitsbenutzergruppen | Listet Benutzergruppen auf, die jedes Modul anzeigen können | Name einer oder mehrerer Benutzergruppen (z. B. &quot;Alle Teilnehmer&quot;, UG-Australien) |
| Obligatorisch | Gibt an, ob ein Modul für eine Benutzergruppe obligatorisch ist. | Benutzergruppennamen, für die das Modul obligatorisch ist; blank = optional |

Sie können **Sichtbarkeitsbenutzergruppen** und **Obligatorisch** kombinieren, um adaptive Abschlussregeln direkt im Bericht zu interpretieren. Beispielsweise kann ein Modul für **alle Teilnehmer** sichtbar sein, aber nur für die **Administratorgruppe** obligatorisch.

### Teilnehmertranskript

Eine neue Spalte **Vorherige Abschlüsse** erfasst historische Abschlussdaten, wenn die adaptive Logik eine Neuvervollständigung auslöst.

| **Unterfeld** | **Beschreibung** |
|-----------------------|-----------------------------------------|
| completeRefreshDate | Zeitstempel beim Zurücksetzen der Fertigstellung |
| completedDate | Zeitstempel für vorherigen Abschluss |
| progressAtRefresh | Teilnehmerfortschritt vor dem Zurücksetzen |
| gradeAtRefresh | Teilnehmerpunktzahl zum Zeitpunkt des Zurücksetzens |

Das Teilnehmertranskript unterstützt jetzt mehrere Abschlusszyklen. Wenn ein Ereignis für die Neuvervollständigung eintritt, z. B. aufgrund von Kursupdates oder neuen obligatorischen Modulen, wird der vorherige Abschluss in die Spalte **Vorherige Abschlüsse** verschoben. Die aktuelle Fertigstellung bleibt in den Standardtranskriptfeldern erhalten.

### Registrierungsbericht

Eine neue **Spalte auf Warteliste** zeigt an, ob ein Teilnehmer in einem Modul innerhalb eines Kurses auf die Warteliste gesetzt wird.

| **Wert** | **Bedeutung** |
|-----------|---------------------------------------------------------|
| korrekt | Der Teilnehmer wird in einem oder mehreren Modulen auf die Warteliste gesetzt |
| falsch | Teilnehmer hat die Registrierung für alle sichtbaren Module bestätigt |

### Wartelistenbericht

Zwei neue Spalten und ein erweitertes Status-Detail-Supportmodul ermöglichen die Wartelistenverfolgung auf Modulebene.

| **Spalte** | **Beschreibung** |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Modul** | Name des Moduls (Klassenzimmer oder virtuelle Klassenzimmersitzung), in dem der Teilnehmer auf der Warteliste steht. Wird nach der Spalte &quot;Instanzstatus&quot; angezeigt. |
| **Modul-ID** | Kennung des Moduls, in dem der Teilnehmer auf der Warteliste steht. Wird nach der Spalte &quot;Modul&quot; angezeigt. |
| **Eingebettet in** | Der Name des Lernpfads und die ID jedes Lernpfads, der diesen Kurs enthält. Leer, wenn der Kurs nicht Teil eines Lernpfads ist. |

Der Bericht &quot;Warteliste&quot; wurde von einem Modell auf Kursebene zu einem Modell auf Modulsitzungsebene verschoben. Ein Teilnehmer kann jetzt in einigen Modulen registriert werden und in anderen auf die Warteliste gesetzt werden. Der Bericht unterstützt auch die Wartelistenverfolgung in Flex-Lernpfaden, bei denen Sitzplatzbeschränkungen auf Modulebene erzwungen werden.

### LP-Registrierungsbericht

Der Bericht zur Lernpfadregistrierung erhält auch eine neue **Anmerkungen**-Spalte. Wenn ein Teilnehmer in einer beliebigen Klassenzimmer- oder virtuellen Klassenzimmersitzung in den Kursen, die den Lernpfad bilden, auf die Warteliste gesetzt ist, wird in der Spalte &quot;Anmerkungen&quot; **Warteliste** angezeigt. Wenn alle Sitzungen bestätigt wurden, ist die Spalte leer.

### Anwesenheitsbericht

In der Spalte **Teilnehmerstatus** wird jetzt zwischen bestätigten und auf die Warteliste gesetzten Teilnehmern unterschieden.

| **Wert** | **Bedeutung** |
|------------|----------------------------------------|
| Bestätigt | Dem Teilnehmer ist eine Lizenz zugewiesen. |
| Auf Warteliste | Der Teilnehmer hat noch keine Lizenz zugewiesen |

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

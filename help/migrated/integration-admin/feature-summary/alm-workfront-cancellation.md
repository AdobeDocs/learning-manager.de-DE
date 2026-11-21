---
description: Erfahren Sie, wie Sie ILT- und VILT-Sitzungen in Adobe Learning Manager abbrechen und reaktivieren, indem Sie den Sitzungsstatus in den Workfront-Migrationsdaten festlegen.
jcr-language: en_us
title: ALM Workfront-Kündigung
exl-id: 01500cf2-6e39-4ac3-84e2-823a5215f6cf
source-git-commit: 90b45cb128b74ecb33a89bf42ef4d6e960101ff0
workflow-type: tm+mt
source-wordcount: '2112'
ht-degree: 1%
---

# ALM-Workfront-Abbruch-/Aktualisierungsauslöser

## Übersicht

Adobe Learning Manager (Learning Manager) kann jetzt Sitzungen mit Kursleiter und virtuellen Kursleitern (ILT/VILT) basierend auf den in Workfront vorgenommenen Änderungen abbrechen und wieder aktivieren. Wenn Ihr Unternehmen Sessions in Workfront plant und sie über die Migration von Workfront zu Learning Manager in den Learning Manager einbindet, können Sie den Status jeder Session in den Migrationsdaten auf &quot;Aktiv&quot; oder &quot;Abgebrochen&quot; setzen. Der Lern-Manager wendet die Änderung dann so an, als hätte ein Administrator die Sitzung auf der Benutzeroberfläche abgebrochen.

Das Abbrechen einer Sitzung durch Migration verhält sich genauso wie das Abbrechen über die Lern-Manager-Benutzeroberfläche. Der eine absichtliche Unterschied ist die Reaktivierung, die in [Eine abgebrochene Sitzung erneut aktivieren](#reactivate-a-cancelled-session) beschrieben wird.

### Die Anforderung

Aktualisierungen einer Sitzung, z. B. Datum und Uhrzeit, Kursleiter, Standort oder Link und Kapazität, fließen bereits von Workfront über die Migration zum Learning Manager. Stornierungen sind nicht erfolgt. Wenn eine Sitzung in Workfront abgebrochen wurde, hatte der Learning Manager keine Möglichkeit, dies zu erfahren, was die folgenden Probleme verursachte:

* Die Teilnehmer blieben für eine Sitzung registriert, die nicht mehr lief, was zu Verwirrung und No-Shows führte.
* Administratoren mussten den Abbruch manuell im Lern-Manager wiederholen.
* Workfront und Learning Manager sind nicht mehr synchron, was Workfront als Quelle der Wahrheit für die Terminplanung untergraben hat.

### Funktionsweise

1. Ein Bereitstellungsmanager bricht eine Sitzung in Workfront ab.
1. Die Sitzungszeile in den Migrationsdaten enthält die neue Spalte für den Sitzungsstatus, die auf &quot;Abgebrochen&quot; festgelegt ist.
1. Ein Systemadministrator führt die Migration über die API aus.
1. Der Lern-Manager markiert die entsprechende Sitzung als abgebrochen und sendet die gleichen Benachrichtigungen, die ein Abbruch von der Benutzeroberfläche sendet.

>[!NOTE]
>
>Diese Funktion erweitert den vorhandenen Migrationsprozess, anstatt einen zweiten Echtzeit-Integrationspfad hinzuzufügen.

### Durchgängiger Arbeitsablauf

Das folgende Diagramm zeigt, wie eine Sitzungszeile von Workfront in den Lernmanager wechselt.

![Flussdiagramm, das eine Workfront-Sitzungszeile anzeigt, die durch die Migration zum Erstellen, Aktualisieren oder Abbrechen der entsprechenden Sitzung navigiert](assets/alm-workfront-cancellation-visual1.png "Arbeitsablauf für den Sitzungsstatus des Workfront-zu-Learning-Managers")

## Anwendungsszenarien

Die folgenden Rollen sind an einer Absage beteiligt, die in Workfront beginnt.

### Rollen

| Rolle | Beschreibung |
|---|---|
| Zustellungsmanager | Plant und verwaltet den Schulungskalender in Workfront, einschließlich der Absage von Sitzungen. Bereitstellungsmanager verwenden nicht die Lern-Manager-Benutzeroberfläche. Die Migration ist der einzige Pfad, über den die Kündigung den Learning Manager erreicht. |
| Systemadministrator | Führt die Migration über die API aus. Diese Rolle betreibt die Workfront-to-Learning-Manager-Pipeline und ist vom Bereitstellungsmanager und vom Learning Manager-Administrator getrennt. |
| Administration | Verwaltet Kurs- und Sitzungsdaten in der Learning Manager-Benutzeroberfläche. Administratoren müssen Sitzungen nicht mehr manuell abbrechen, nachdem sie über eine Änderung in Workfront informiert wurden. |
| Autor | Verantwortlich für den Kurs- und Sitzungsinhalt in der Learning Manager-Benutzeroberfläche. |
| Der Kursleiter | Ist Sessions zugewiesen. Kursleiter sehen den richtigen Sitzungsstatus und werden benachrichtigt, wenn eine von ihnen instruierte Sitzung abgebrochen wird. |
| Teilnehmer | Ist für eine Sitzung über den Lern-Manager registriert. Teilnehmer werden umgehend benachrichtigt, wenn ihre Sitzung abgebrochen wird. |

### Häufige Szenarien

| Szenario | Aktionen. | Ergebnis |
|---|---|---|
| Eine Sitzung wird in Workfront abgebrochen, z. B. weil eine Ressource nicht verfügbar ist oder ein Anbieter ein Problem hat. | Setzen Sie den Sitzungsstatus in der Migrationszeile für die Sitzung auf Abgebrochen und führen Sie die Migration aus. | Die Sitzung wird im Lern-Manager abgebrochen und die betroffenen Personen werden benachrichtigt. |
| Die Details einer aktiven Sitzung ändern sich in Workfront. | Schließen Sie die geänderten Werte in die Migrationszeile ein. Setzen Sie den Sitzungsstatus auf Aktiv oder lassen Sie ihn leer. | Die Sitzung wird aktualisiert. Learning Manager sendet eine sitzungsaktualisierte E-Mail. |
| Eine abgebrochene Sitzung wird in Workfront wieder hergestellt. | Setzen Sie den Sitzungsstatus in der Migrationszeile auf Aktiv und führen Sie die Migration aus. | Die Sitzung wird aktiv und kann geändert und wieder abgebrochen werden. |
| Aktualisierte Details werden für eine abgebrochene Sitzung gesendet, ohne den Status auf &quot;Aktiv&quot; festzulegen. | Der Benutzer muss keine Aktion ausführen. | Die Sitzung wird abgebrochen, die Zeile gibt einen Validierungsfehler zurück und es werden keine Details geändert. |
| Eine Migrationszeile enthält keinen Sitzungsstatus. | Lassen Sie die Spalte leer oder lassen Sie sie weg. | Der aktuelle Status der Sitzung im Lern-Manager bleibt unverändert. |

## Wichtigste Funktionen

* **Spalte für den Sitzungsstatus.** Das Migrationsschema enthält ein optionales Feld für den Sitzungsstatus, das &quot;Aktiv&quot; und &quot;Abgebrochen&quot; unterstützt.
* **Abbruch durch Migration.** Wenn eine Zeile den Status Abgebrochen aufweist, wird die entsprechende Sitzung im Lern-Manager abgebrochen. Learning Manager verwendet denselben übereinstimmenden Schlüssel, den die Migration bereits zum Erstellen und Aktualisieren von Sitzungen verwendet.
* **Keine manuelle Arbeit im Lern-Manager.** Administratoren müssen die Sitzung nicht erneut auf der Benutzeroberfläche abbrechen.
* **Das gleiche Verhalten wie beim Abbrechen in der Benutzeroberfläche.** Die Handhabung von Registrierungen, die Sichtbarkeit für Teilnehmer, die Berichterstellung, der Audit-Verlauf und Benachrichtigungen stimmen mit einem Abbruch über die Benutzeroberfläche überein.
* **Reaktivierung.** Sie können eine abgebrochene Sitzung wieder auf &quot;Aktiv&quot; zurücksetzen, indem Sie den Status explizit in den Migrationsdaten festlegen.
* **Schutz für abgebrochene Sitzungen.** Die Migration ändert die Details einer abgebrochenen Sitzung nicht, es sei denn, die Zeile legt den Status explizit auf Aktiv fest.
* **Abwärtskompatibilität.** Die Spalte &quot;Status&quot; ist optional, sodass vorhandene Migrationsdateien weiterhin ohne Änderungen funktionieren.
* **Benachrichtigungen abschließen.** Teilnehmer, Kursleiter, Administratoren, Autoren und Manager erhalten von der Benutzeroberfläche die gleichen E-Mails für die Kündigung wie für eine Kündigung.

## Sitzungsstatus

Jede Sitzung im Learning Manager befindet sich in einem von zwei Status.

| Status | Bedeutung |
|---|---|
| Aktiv | Der Standardstatus. Die Sitzung ist live, und die Teilnehmer können sich anmelden und daran teilnehmen. |
| Abgebrochen | Die Sitzung wird abgebrochen. Registrierte Teilnehmer, Administratoren, Autoren und Manager werden benachrichtigt, sobald sie über die Benutzeroberfläche eine Kündigung erhalten. |

### Regeln für den Übergang von Staaten zur Migration

Die folgende Tabelle zeigt, was passiert, wenn eine Migrationszeile verarbeitet wird. Der Lern-Manager identifiziert die Sitzung mithilfe des entsprechenden Schlüssels, den die Migration bereits für das Erstellen und Aktualisieren verwendet.

| Aktueller Status im Lern-Manager | Sitzungsstatus in der Migrationszeile | Ergebnis |
|---|---|---|
| Sitzung ist nicht vorhanden | Aktiv oder leer | Die Sitzung wird als aktiv erstellt. |
| Aktiv | Aktiv oder leer | Die Sitzung bleibt aktiv. Geänderte Werte in der Zeile werden angewendet. |
| Aktiv | Abgebrochen | Die Sitzung wird abgebrochen und Benachrichtigungen werden gesendet. |
| Abgebrochen | Abgebrochen | Die Zeile wird übersprungen. Eine abgebrochene Sitzung kann nicht erneut abgebrochen werden. |
| Abgebrochen | Aktiv | Die Sitzung wird wieder aktiviert. Geänderte Werte in der Zeile werden angewendet. |
| Abgebrochen | Leer | Die Sitzung wird abgebrochen. Wenn die Zeile Werte geändert hat, wird ein Validierungsfehler zurückgegeben, und es werden keine Details geändert. |

### Regeln für die Spalte &quot;Sitzungsstatus&quot;

* Die Spalte ist in jeder Zeile optional.
* Wenn die Spalte leer ist, wird die Sitzung auf &quot;Aktiv&quot; aktualisiert.
* Eine Sitzung wird nur dann durch Migration wieder aktiv, wenn in der Spalte explizit &quot;Aktiv&quot; steht.

Verwenden Sie einen der folgenden Werte in der Spalte &quot;Sitzungsstatus&quot;:

* `state = Active`
* `state = Cancelled`

>[!NOTE]
>
>Die genaue Spaltenüberschrift und die akzeptierten Werte werden bestätigt. Verwenden Sie die Namen, die in Ihrer Migrationsdokumentation angegeben sind.

## Updates für abgebrochene Sitzungen

Sie können die Details einer abgebrochenen Sitzung nicht durch Migration aktualisieren. Wenn eine Zeile für eine abgebrochene Sitzung geänderte Werte enthält und den Status nicht auf &quot;Aktiv&quot; setzt, gibt der Lern-Manager einen Validierungsfehler zurück, lässt die Sitzung abgebrochen und wendet die geänderten Details weder an noch speichert er sie. Der Lern-Manager sendet keine sitzungsaktualisierte E-Mail für den Versuch.

### Abbrechen einer Sitzung mithilfe der Migration

Gehen Sie wie folgt vor, wenn eine Sitzung in Workfront abgebrochen wurde und die Änderung im Learning Manager widergespiegelt werden soll.

**Vorbereitung**

* Die Sitzung ist bereits im Lern-Manager vorhanden und wird durch die Migration von Workfront zum Lern-Manager importiert.
* Sie kennen den entsprechenden Schlüssel, den Ihre Migration zur Identifizierung der Sitzung verwendet.

1. Abbrechen der Sitzung in **Workfront**.
1. Suchen Sie in der CSV-Sitzungsdatei, die Sie für die Migration verwenden, die Zeile für die Sitzung. Stellen Sie sicher, dass der Schlüssel mit dem Schlüssel übereinstimmt, der beim Erstellen der Sitzung verwendet wurde.
1. Geben Sie in der Spalte Sitzungsstatus **Abgebrochen** ein.
1. Führen Sie die Migration über die API aus.
1. Überprüfen Sie im Lern-Manager, ob die Sitzung abgebrochen wird.

Der Lern-Manager markiert die Sitzung als abgebrochen, behandelt die registrierten Teilnehmer wie einen Abbruch über die Benutzeroberfläche und sendet die Abbruchbenachrichtigungen. In der Lern-Manager-Benutzeroberfläche ist keine Aktion erforderlich.

>[!NOTE]
>
>Wenn die Sitzung bereits abgebrochen wurde, überspringt der Lern-Manager die Zeile.

### Aktualisieren einer aktiven Sitzung

Bei einer aktiven Sitzung bleibt das vorhandene Migrationsaktualisierungsverhalten verfügbar. Setzen Sie den Sitzungsstatus auf &quot;Aktiv&quot; oder lassen Sie ihn leer und fügen Sie die geänderten Werte in die Zeile ein. Über die Migrationspipeline können Sie weiterhin Details wie Datum und Uhrzeit, Kursleiter, Standort oder Link und Kapazität aktualisieren.

Mit &quot;Aktiv&quot; bleibt das vorhandene Erstellungs- und Aktualisierungsverhalten erhalten. Durch Abbrechen wird derselbe Sitzungsabbruch ausgelöst, den die Benutzeroberfläche über die CSV-Sitzungsmigration bereitstellt.

### Abgebrochene Sitzung erneut aktivieren

Eine abgebrochene Sitzung kehrt nur dann in den aktiven Status zurück, wenn Sie den Status explizit auf Aktiv setzen. Sie können eine Sitzung durch Migration oder durch Bearbeiten in der Benutzeroberfläche erneut aktivieren.

1. Suchen Sie in der CSV-Sitzungsdatei die Zeile für die abgebrochene Sitzung. Stellen Sie sicher, dass der Schlüssel mit dem Schlüssel übereinstimmt, der beim Erstellen der Sitzung verwendet wurde.
1. Geben Sie in der Spalte &quot;Sitzungsstatus&quot; Aktiv ein.
1. (Optional) Aktualisieren Sie alle anderen Werte in der Zeile, die Sie ändern möchten, z. B. Datum und Uhrzeit, Kursleiter, Standort, Link oder Kapazität.
1. Führen Sie die Migration über die API aus.

Die Sitzung wird aktiv und die Details können geändert werden. Eine Sitzung, die durch Migration oder über die Benutzeroberfläche erneut aktiviert wird, kann über beide Pfade wieder abgebrochen werden.

>[!IMPORTANT]
>
>Wenn Sie aktualisierte Sitzungsdetails für eine abgebrochene Sitzung senden, ohne den Status auf &quot;Aktiv&quot; festzulegen, bleibt die Sitzung abgebrochen und die Zeile gibt einen Validierungsfehler zurück.

## Benachrichtigungen

Learning Manager sendet jede E-Mail, die zum Abbruch gesendet wird, von der Benutzeroberfläche, wenn eine Sitzung durch Migration abgebrochen wird. Die Empfängerabdeckung wird nicht verringert, und der Inhalt verwendet dieselbe Vorlage, sodass die Empfänger nicht wissen, wie die Kündigung gestartet wurde.

Die Empfänger, je nach Anwendung auf die Sitzung, sind wie folgt:

| Empfänger | Benachrichtigung |
|---|---|
| Teilnehmer | Teilnehmer, die für die Sitzung registriert sind, werden darüber informiert, dass die Sitzung abgebrochen wird. |
| Kursleiter | Kursleiter, die der Sitzung zugewiesen sind, werden über die Kündigung informiert. |
| Manager | Manager erhalten die Stornierungsbenachrichtigung. |

### E-Mails für abgebrochene Sitzungen

Eine abgebrochene Sitzung generiert keine sitzungsaktualisierten E-Mails. Während eine Sitzung abgebrochen wird, lösen Änderungen an Datum und Uhrzeit, Kursleiter, Standort oder Link und Kapazität nicht die sitzungsaktualisierte E-Mail aus. Für eine abgebrochene Sitzung gelten nur Abbruch- und Reaktivierungsbenachrichtigungen.

## Überlegungen und Einschränkungen

* Da die Funktion die Migration verwendet, wird eine in Workfront vorgenommene Kündigung beim Learning Manager vorgenommen, wenn die Migration ausgeführt wird. Webhook-basierte Abbruch in Echtzeit wird nicht unterstützt.
* Die Migration kann die Details einer abgebrochenen Sitzung nicht ändern. Um sie zu ändern, legen Sie zunächst den Status auf &quot;Aktiv&quot; fest.
* Die Spalte mit dem Sitzungsstatus ist optional. Zeilen, die es auslassen, ändern nie den Status einer Sitzung.
* Die Funktion erweitert die vorhandene Migrationsintegration. Es wird kein zweiter Echtzeit-Integrationspfad hinzugefügt.
* Der Migrationszeitplan bzw. -auslöser hängt von der Symbolleiste ab, die Ihre Organisation verwendet, um ihn auszuführen. In diesem Leitfaden wird kein fester Zeitplan definiert.
* Bereitstellungsmanager arbeiten nur in Workfront. Sie benötigen keinen Zugriff auf die Lern-Manager-Benutzeroberfläche, um eine Sitzung abzubrechen.

## Erfolgsmaßnahmen

| Messwert | Target |
|---|---|
| Stornierungen, die Administratoren oder der Kundendienst manuell replizieren | Wird innerhalb eines vollständigen Release-Zyklus nach dem Start auf 0 reduziert. |
| Absagen von Workfront im Lern-Manager | 100 % der Stornierungsereignisse werden innerhalb eines Migrationszyklus verarbeitet. |
| Benachrichtigungsparität zwischen der Benutzeroberfläche und Migrationsstornierungen | 0 Lücken bei der Empfängerabdeckung (Administratoren, Autoren, Manager und Teilnehmer) und 0 unnötige Update-E-Mails für abgebrochene Sitzungen. |

## Fehlerbehebung

| Problem | Erwartete oder mögliche Ursache | Aktion |
|---|---|---|
| Eine Sitzung bleibt aktiv, nachdem sie in Workfront abgebrochen wurde. | Die Migration hat den Abbruch noch nicht verarbeitet, oder die Migrationszeile wies nicht den expliziten Status &quot;Abgebrochen&quot; auf. | Überprüfen Sie die Migrationseingabe und das Verarbeitungsergebnis. |
| Die Details einer abgebrochenen Sitzung ändern sich nicht. | Erwartetes Verhalten, während die Sitzung abgebrochen wird. | Aktivieren Sie die Sitzung erneut, indem Sie den Status auf &quot;Aktiv&quot; setzen, und wenden Sie dann die Änderungen an. |
| Es wird keine E-Mail mit aktualisierter Sitzung für eine abgebrochene Sitzung gesendet. | Erwartetes Verhalten. Normale Update-E-Mails werden bei abgebrochenen Sitzungen unterdrückt. | Verwenden Sie statt eines Updates nur mit Details den Lebenszyklus der Kündigung und Reaktivierung. |
| Eine Stornierungszeile wird übersprungen. | Die entsprechende Sitzung im Learning Manager wurde bereits abgebrochen. | Eine weitere Kündigung ist nicht erforderlich. Aktivieren Sie die Sitzung zuerst erneut, wenn sie wieder aktiv sein muss. |
| Ein Empfänger hat dieselbe Stornierungs-E-Mail erhalten wie bei einem Abbruch der Benutzeroberfläche. | Erwartetes Verhalten. Migrationsabbruch ist auf die Benutzeroberfläche abgestimmt. | Es ist keine Aktion erforderlich. |
| Das Verhalten ist unklar, wenn der Sitzungsstatus leer ist. | Die Quellanforderungen widersprechen bei der Behandlung des leeren Zustands. | Bestätigen Sie das Freigabeverhalten, bevor Sie sich bei einem Übergang auf einen leeren Status verlassen. |

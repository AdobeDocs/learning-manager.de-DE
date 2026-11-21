---
description: Erfahren Sie, wie Sie die Mehrfacheinschreibung für adaptive Kurse aktivieren, Sitzplatzbeschränkungen und Wartelisten verwalten und Registrierungsregeln für Lernpfade verstehen.
jcr-language: en_us
title: Mehrere Registrierungen für adaptive Kurse
exl-id: e2a52964-fe9d-4a71-a020-68201f75f9f0
hide: true
source-git-commit: e056f1a655efd7c999856e2b54b28e676e67afc6
workflow-type: tm+mt
source-wordcount: '1231'
ht-degree: 0%
---

# Mehrere Registrierungen für adaptive Kurse

## Übersicht

Mit einer Mehrfachregistrierung kann sich ein Teilnehmer gleichzeitig in mehr als einer Instanz desselben Kurses registrieren. In Adobe Learning Manager können Sie jetzt die Mehrfacheinschreibung für adaptive Kurse aktivieren.

## Informationen zur Mehrfacheinschreibung in einem adaptiven Kurs

In einem adaptiven Kurs werden jedem Teilnehmer nur die Module angezeigt, die seinen Benutzergruppen entsprechen. Wenn die Mehrfacheinschreibung aktiviert ist, kann ein Teilnehmer mehrere Instanzen dieses Kurses nehmen, z. B. Sitzungen in verschiedenen Monaten.

Adaptive Kurse verfolgen Wartelisten auf Modulebene, nicht auf Instanzebene. Ein Teilnehmer kann an einigen Modulen gerade bearbeitet werden und gleichzeitig auf anderen auf der Warteliste stehen. Ein Kurs hat beispielsweise zwei Instanzen und jede Instanz hat eine Sitzplatzbeschränkung von einer. Der erste Teilnehmer registriert sich für beide Instanzen und belegt beide Plätze. Ein zweiter Teilnehmer, der sich in beiden Instanzen registriert, wird in beiden auf die Warteliste gesetzt.

## Aktivieren Sie die Mehrfacheinschreibung für einen adaptiven Kurs

1. Melden Sie sich bei Adobe Learning Manager als Autor an.
2. Wählen Sie in der linken Navigation **Kurse** aus. Öffnen Sie einen adaptiven Kurs oder erstellen Sie einen.
3. Fügen Sie die Module hinzu. Wählen Sie für jedes Inhaltsmodul **Regeln hinzufügen**, um die Benutzergruppen festzulegen, die es sehen können, sowie die Benutzergruppen, für die es obligatorisch ist.
4. Wählen Sie **Speichern**. Die Option zur Mehrfacheinschreibung wird verfügbar.
5. Aktivieren Sie den Schalter **Mehrfacheinschreibung**.
6. Erstellen Sie die Instanzen, die Sie benötigen. Legen Sie die Lizenzbeschränkungen für Klassenzimmer- und virtuelle Klassenzimmersitzungen fest.
7. Wählen Sie **Publish** aus.

Teilnehmer können sich jetzt für mehr als eine Instanz des Kurses registrieren.

## Sitzlimit und Wartelistenverhalten

Adaptive Kurse erzwingen Sitzungsbeschränkungen für jedes Klassenzimmer oder jede virtuelle Klassenzimmersitzung. Ein Teilnehmer wird sofort registriert und nur in den vollständigen Sitzungen auf die Warteliste gesetzt. Der Teilnehmer kann alle anderen Module sofort starten.

| Bedingung | Ergebnis |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Alle sichtbaren Sitzungen verfügen über verfügbare Lizenzen | Der Teilnehmer wird mit vollem Zugriff auf alle Module registriert. |
| Mindestens eine sichtbare Sitzung ist voll | Der Teilnehmer ist registriert und wird nur in den vollständigen Sitzungen auf die Warteliste gesetzt. |
| Sie fügen einem Kurs mit registrierten Teilnehmern eine obligatorische Sitzung ohne Lizenzen hinzu | Der Teilnehmer wird in der neuen Sitzung auf die Warteliste gesetzt. Bestehender Fortschritt und Zugang bleiben unberührt. |
| Eine Änderung der Benutzergruppe entfernt eine Sitzung aus den sichtbaren Modulen des Teilnehmers | Adobe Learning Manager gibt die Lizenz sofort frei. |
| Ein Teilnehmer wechselt zu einer anderen Instanz | Abgeschlossene Module bleiben abgeschlossen. Lizenzen werden nur für sichtbare Module verwendet, die der Teilnehmer nicht abgeschlossen hat. |

## Anmelde- und Abschlussregeln für adaptive Lernpfade

Autoren können in Adobe Learning Manager jetzt adaptive Kurse zu adaptiven Lernpfaden hinzufügen. Für Registrierung, Warteliste und Abschluss gelten Regeln, die die von Ihren Autoren konfigurierten Abschnittseinstellungen und Kurseinstellungen kombinieren.

### Wie ein adaptiver Lernpfad einen Teilnehmer auswertet

Adobe Learning Manager bewertet die Sichtbarkeit auf Abschnitts- und Kursebene. Die Abschnittsregel bestimmt, ob ein Teilnehmer einen Abschnitt und die adaptiven Kurse darin sieht. Die Modulregeln in jedem adaptiven Kurs entscheiden dann, ob der Teilnehmer für den Kurs registriert ist.

Die Teilnehmer werden automatisch registriert, wenn es eine Kursänderung in Bezug auf den adaptiven Kurs in Adaptive LP gibt. Gleichzeitig erhalten die Teilnehmer Benachrichtigungen und E-Mails zur automatischen Registrierung.

### Regeln für die Registrierungsbewertung

Wenn Sie einen Teilnehmer für einen adaptiven Lernpfad registrieren, überprüft Adobe Learning Manager den Pfad in dieser Reihenfolge:

| Bestellung | Überprüfen | Ergebnis |
|-----------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 | Abschnittssichtbarkeit | Adobe Learning Manager überprüft einen Kurs nur dann auf Registrierung, wenn sein Abschnitt für den Teilnehmer sichtbar ist. |
| 2 | Kursberechtigung | Wenn der Kurs kein obligatorisches Modul für den Teilnehmer hat, ist der Teilnehmer nicht für den Kurs registriert. Der Kurs zählt nicht zum Abschluss des Lernpfads. |
| 3 | Abschnitte ohne förderfähigen Kurs | Wenn ein Abschnitt nur adaptive Kurse enthält und der Teilnehmer für keinen dieser Kurse berechtigt ist, überspringt Adobe Learning Manager den Abschnitt. |
| 4 | Lernpfadregistrierung | Wenn keiner der obligatorischen Abschnitte auf den Teilnehmer zutrifft, ist der Teilnehmer nicht für den Lernpfad registriert. |

Wenn der Teilnehmer bereits bei einer Instanz des Kurses registriert ist, die zur Lernpfadinstanz gehört, verwendet Adobe Learning Manager diese Registrierung.

Nach der Registrierung gelten die folgenden Regeln:

* Ein Teilnehmer, der einen Kurs aufgrund der Sichtbarkeit übersprungen hat, kann automatisch registriert werden, wenn der adaptive Kurs sichtbar ist, da sich die Sichtbarkeit/obligatorische Regel später ändert.
* Eine Änderung der Benutzergruppe oder eine Kursänderung kann die Registrierung eines Teilnehmers für einen adaptiven Kurs aufheben. Wenn kein obligatorischer Inhalt im Pfad verbleibt, wird die Registrierung des Teilnehmers für den Pfad aufgehoben.
* Bei Abschnittsänderungen erhält der Teilnehmer keine Benachrichtigung oder E-Mail zur automatischen Registrierung. Einfach beim erneuten Laden der Seite kann der Teilnehmer die Änderungen sehen.

### Wartelistenverhalten in adaptiven Lernpfaden

Die Warteliste funktioniert auf Sitzungsebene, nicht auf Instanzebene. Dies gilt auch für adaptive Kurse in Lernpfaden.

| Szenario | Verhalten |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Kein adaptiver Kurs im Pfad verfügt über ein Klassenzimmer oder ein virtuelles Klassenzimmermodul | Keine Warteliste. |
| Ein adaptiver Kurs verfügt über ein Klassenzimmer- oder virtuelles Klassenzimmermodul. Es wird keine Instanz ausgewählt. | Der Kurs verwendet standardmäßig **Keine Instanz**. Der Teilnehmer kann sich in jeder Instanz registrieren und wird nur in vollen Sitzungen auf die Warteliste gesetzt. |
| Eine Instanz wird vor der Registrierung ausgewählt | Der Teilnehmer ist für diese Instanz registriert und wird nur bei vollständigen Sitzungen auf die Warteliste gesetzt. |

Um Teilnehmer auf der Warteliste zu verwalten, öffnen Sie den adaptiven Kurs und wählen Sie die Registerkarte **Teilnehmer** > **Warteliste** aus. Bei einem adaptiven Kurs in einem flexiblen Lernpfad und einem adaptiven Lernpfad werden Teilnehmer auf der Warteliste nur auf der Registerkarte **Warteliste** des Kurses und nicht unter dem Lernpfad angezeigt.

### Abschluss aktualisieren und Rollback-Verhalten

Adobe Learning Manager widerruft die Vervollständigung nicht automatisch, wenn sich Benutzergruppen oder Regeln ändern. Ein abgeschlossener Teilnehmer bleibt abgeschlossen, bis Sie den Abschluss aktualisieren.

* Führen Sie **Abschluss aktualisieren** auf dem Lernpfad aus. Sie können einen adaptiven Kurs für Teilnehmer, die ihn durch den Pfad führen, nicht selbst aktualisieren.

* Jeder adaptive Kurs wird zuerst basierend auf den aktuellen obligatorischen Modulen des Teilnehmers neu berechnet. Der Lernpfad wird dann basierend auf den aktuellen obligatorischen Abschnitten und den aktualisierten Kursstatus neu berechnet.

* Wenn der Kurs oder Pfad nicht mehr abgeschlossen ist, ändert sich der Status des Teilnehmers in &quot;Wird ausgeführt&quot;. Der ursprüngliche Abschluss bleibt im Teilnehmertranskript als historischer Datensatz erhalten.

* Ein Abschluss-Rollback findet die adaptiven Kurse, deren Module sich aufgrund einer Änderung der Benutzergruppe oder einer erneuten Veröffentlichung geändert haben. Diese Kurse und dann der Lernpfad werden neu berechnet. Der Auftragsstatus zeigt **Success** an, wenn das Rollback abgeschlossen ist.

Die Warteliste wird auf Modulebene verfolgt. Ein Teilnehmer kann in einer vollständigen Sitzung in mehr als einer Instanz auf die Warteliste gesetzt werden. Ein Kurs hat z. B. zwei Instanzen mit einer Sitzplatzbeschränkung von jeweils einer. Der erste Teilnehmer registriert sich für beide Instanzen und belegt beide Plätze. Ein zweiter Teilnehmer, der sich für beide Instanzen registriert, wird auf der Registerkarte **Warteliste** jeder Instanz angezeigt.

### Lizenzen zu Teilnehmern auf Warteliste zuweisen

Wenn ein Teilnehmer die Registrierung widerruft, ein Autor eine Lizenzbeschränkung erhöht oder ein Teilnehmer die Instanzen wechselt, löscht Adobe Learning Manager die Warteliste in der Reihenfolge des Registrierungsdatums. Sie können Lizenzen auch manuell zuweisen.

1. Öffnen Sie den adaptiven Kurs.
2. Wählen Sie die Registerkarte **Teilnehmer** > **Warteliste** aus.
3. Aktivieren Sie das Kontrollkästchen neben jedem Teilnehmer, dem Sie Lizenzen zuweisen möchten.
4. Wählen Sie **Lizenzen zuordnen**.

Adobe Learning Manager löscht jeden ausgewählten Teilnehmer aus der Warteliste in allen auf der Warteliste stehenden Sitzungen gleichzeitig, nicht nur in der angezeigten Sitzung. Das System geht davon aus, dass Sie den Platz für den Teilnehmer eingerichtet haben.

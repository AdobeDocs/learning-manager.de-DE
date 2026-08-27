---
title: Erstellen und Verwalten von Arbeitsgruppensitzungen im Live Hub
description: Hier erfahren Sie, wie Kursleiter Arbeitsräume in einer Live-Hub-Sitzung erstellen, konfigurieren, starten, überwachen und verwalten, einschließlich KI-generierter Raumzusammenfassungen und Berichte.
source-git-commit: 0da79f36c305889cb70831f7791fddbd1f470da0
workflow-type: tm+mt
source-wordcount: '1387'
ht-degree: 0%

---


# Arbeitsgruppensitzungen erstellen und verwalten

Die Kursleiter können eine Live-Hub-Sitzung in kleinere, interaktive Gruppen aufteilen, um Aktivitäten zu konzentrieren und Diskussionen zu führen. Sie können Arbeitsräume erstellen, Teilnehmer automatisch oder manuell zuweisen, Aktivitätsanweisungen festlegen und die Dauer der Sitzung steuern. Während eine Arbeitsgruppensitzung aktiv ist, können Sie Räume mit KI-generierten Zusammenfassungen überwachen, einem Raum beitreten, um Ihren Bildschirm freizugeben oder zu chatten, und die Sitzung verlängern.

Dieses Handbuch führt Sie durch alle Arbeitsgruppenraum-Aktionen, die den Kursleitern zur Verfügung stehen, von der Erstellung eines Raums bis zur Überprüfung des Sitzungsberichts.

## Arbeitsgruppensitzung erstellen

Breakout-Sessions teilen ein virtuelles Klassenzimmer in kleinere, interaktive Gruppen auf. Führen Sie die folgenden Schritte aus, um eines zu erstellen.

So erstellen Sie eine Arbeitsgruppensitzung:

1. Wählen Sie in der Steuerungsleiste ![Breakout-Icon](./assets/breakout-icon.svg) aus.

   ![Arbeitsgruppensitzungs-Bereich auswählen](assets/select-breakout-sessions-panel.png)
   *Live-Hub-Schnittstelle, die das Arbeitsgruppenfenster anzeigt.*

1. Wählen Sie **Arbeitsgruppensitzung einrichten**.

Der Bereich Arbeitsgruppen wird geöffnet. Von hier aus können Sie Arbeitsräume konfigurieren, Teilnehmer zuweisen und Arbeitsgruppensitzungseinstellungen verwalten.

>[!NOTE]
>Wenn die Arbeitsgruppensitzung nicht gestartet wird, finden Sie im [Leitfaden zur Fehlerbehebung für Live Hub](../kb/troubleshooting-guide-for-live-hub.md#breakout-session-issues) eine Liste der häufigsten Fehlermeldungen und deren Behebung.

## Entwerfen einer Arbeitsgruppensitzung

Konfigurieren Sie vor dem Starten einer Arbeitsgruppensitzung Räume, weisen Sie Teilnehmer zu, und definieren Sie die Aktivitätsdetails mithilfe des Bedienfelds **Arbeitsgruppen**. Die richtige Konfiguration hilft dabei, die Teilnehmer richtig zu platzieren und das Ziel jeder Breakout-Aktivität zu verstehen.

So entwerfen Sie eine Arbeitsgruppensitzung:

1. Wählen Sie in der Steuerungsleiste ![Breakout-Icon](./assets/breakout-icon.svg) aus. 2 <br>Der Bereich Arbeitsgruppen wird geöffnet.

   ![Arbeitsgruppenfenster öffnen](assets/open-breakouts-panel.png)
   *Arbeitsgruppenfenster mit den Optionen zum Konfigurieren der Arbeitsgruppenräume.*

1. Konfigurieren Sie die Arbeitsräume mithilfe der folgenden Optionen:

| **Option** | **Beschreibung** |
|----|----|
| Bearbeitungssymbol | Wählen Sie das Bearbeitungssymbol aus, um die Arbeitsgruppensitzung umzubenennen. |
| **Räume** | Legen Sie die Anzahl der Arbeitsräume mithilfe der Steuerelemente zum Erhöhen oder Verringern fest. Das Maximum beträgt **10** Räume. |
| **Dauer** | Legen Sie fest, wie lange die Arbeitsgruppensitzung ausgeführt wird. Die Mindestdauer beträgt **5 Minuten** und die Höchstdauer beträgt **60 Minuten**. |
| **Teilnehmer zuweisen** | Wählen Sie **Automatische Zuweisung** aus, um Teilnehmer automatisch Räumen zuzuweisen. Sie können einen Teilnehmer auch per Drag &amp; Drop in einen anderen Raum verschieben. |
| **Einzeln für Räume festlegen** | Passen Sie die Anweisungen für jeden Arbeitsraum separat an. |
| **Anweisungen** | Beschreiben Sie die Aktivität und skizzieren Sie das erwartete Ergebnis für die Arbeitsgruppensitzung. |
| **Raumzuordnungen anzeigen** | Zeigen Sie vor Beginn der Sitzung an, wie die Teilnehmer auf die Arbeitsräume verteilt werden. |
| **Arbeitsgruppen starten** | Starten Sie die Arbeitsgruppensitzung und verschieben Sie die Teilnehmer in die ihnen zugewiesenen Räume. |
| Symbol verwerfen | Verwerfen Sie die aktuelle Arbeitsgruppenkonfiguration, ohne die Änderungen zu speichern. |

1. Wählen Sie **Speichern** aus. <br> Die Arbeitsgruppensitzung wird im Bereich &quot;**Arbeitsgruppen**&quot; mit einem **Neu**-Tag angezeigt.

## Starten einer Arbeitsgruppensitzung

Sobald die Arbeitsgruppensitzung konfiguriert und gespeichert wurde, wird sie im Bereich **Arbeitsgruppen** angezeigt. Starten Sie die Sitzung, um Teilnehmer in die ihnen zugewiesenen Räume zu verschieben.

So starten Sie eine Arbeitsgruppensitzung:

1. Öffnen Sie den Bereich **Arbeitsgruppen**.

1. Navigieren Sie zur Arbeitsgruppensitzung mit dem Tag **Neu**.

1. Wählen Sie **Arbeitsgruppen starten**. <br> In einer Benachrichtigung wird **Starten in 5 Sekunden angezeigt**. Teilnehmer werden dann in die ihnen zugewiesenen Arbeitsräume verschoben, wenn die konfigurierte Einrichtung angewendet wird.

   ![Arbeitsgruppensitzung starten](assets/start-breakout-session.png)
   *Wählen Sie &quot;Arbeitsgruppen starten&quot; aus, um die Arbeitsgruppensitzung zu starten.*

## Arbeitsgruppensitzungen verwalten

Nachdem Sie eine Arbeitsgruppensitzung gespeichert haben, wird sie im Bereich **Arbeitsgruppen** angezeigt. Jede gespeicherte Sitzung zeigt ihren Status (**Neu** oder **Geschlossen**), die Anzahl der Räume und die Dauer an. Über dieses Bedienfeld können Sie eine Sitzung nach Bedarf bearbeiten, duplizieren oder löschen.

### Bearbeiten einer Arbeitsgruppensitzung

Verwenden Sie diese Option, um eine vorhandene Arbeitsgruppenkonfiguration zu aktualisieren. Die Bearbeitung ist für Sitzungen mit dem Status **Neu** verfügbar.

Bearbeiten einer Arbeitsgruppensitzung:

1. Öffnen Sie den Bereich **Arbeitsgruppen**.

1. Navigieren Sie zu der Arbeitsgruppensitzung, die Sie ändern möchten.

1. Wählen Sie das Bearbeitungssymbol (Bleistift) für die Sitzung aus.

   ![Symbol für Arbeitsgruppensitzungen bearbeiten](assets/edit-breakout-session-icon.png)
   *Wählen Sie das Symbol &quot;Bearbeiten&quot; (Bleistift), um die Konfiguration der Arbeitsgruppensitzung zu aktualisieren.*

1. Aktualisieren Sie die Konfiguration nach Bedarf, z. B. die Anzahl der Räume, die Dauer oder die Anweisungen.

1. Wählen Sie **Speichern**.

### Duplizieren einer Arbeitsgruppensitzung

Sie können eine vorhandene Arbeitsgruppeneinrichtung wiederverwenden, indem Sie eine zuvor erstellte Sitzung duplizieren.

So duplizieren Sie eine Sitzung:

1. Öffnen Sie den Bereich **Arbeitsgruppen**.

1. Navigieren Sie zu der Arbeitsgruppensitzung, die Sie duplizieren möchten.

1. Wählen Sie die weiteren Optionen (**...**) Symbol auf der Sitzung.

   ![Menü für doppelte Arbeitsgruppensitzungen](assets/duplicate-breakout-session-menu.png)
   *Im Menü &quot;Weitere Optionen&quot; werden doppelte Aktionen angezeigt.*

1. Wählen Sie **Duplicate**.

Eine neue Sitzung wird mit derselben Raumkonfiguration, denselben Teilnehmerzuweisungen, denselben Anweisungen und derselben Dauer erstellt. Der kopierte Arbeitsraum wird oben im Bereich mit dem Status **Neu** und einem Namen wie **Arbeitsgruppensitzung 1 (Kopie)** angezeigt.

### Löschen einer Arbeitsgruppensitzung

Verwenden Sie diese Option, um eine nicht mehr benötigte Arbeitsgruppensitzung zu entfernen.

So löschen Sie eine Arbeitsgruppensitzung:

1. Öffnen Sie den Bereich **Arbeitsgruppen**.

1. Navigieren Sie zur gespeicherten Arbeitsgruppensitzung.

1. Wählen Sie die weiteren Optionen (**...**) Symbol auf der Sitzung.

1. Wählen Sie **Löschen** aus. <br> Ein Bestätigungs-Popup-Fenster wird angezeigt.

   ![Breakout-Bestätigung löschen](assets/delete-breakout-confirmation.png)
   *Wählen Sie im Bestätigungs-Popup-Fenster Löschen aus, um eine Arbeitsgruppensitzung zu löschen.*

1. Wählen Sie **Löschen** aus.

## Aktivitäten in einer aktiven Arbeitsgruppensitzung verwalten

Während einer aktiven Arbeitsgruppensitzung können Kursleiter die Raumaktivität überwachen, mit den Teilnehmern kommunizieren und mit den Teilnehmern zusammenarbeiten, indem sie einzelnen Arbeitsräumen beitreten. Die meisten Tools für Zusammenarbeit, die in der Hauptsitzung verfügbar sind, z. B. Chat, Bildschirmfreigabe und Whiteboard, sind auch in Arbeitsräumen verfügbar und funktionieren auf die gleiche Weise.

### Anzeigen KI-generierter Zusammenfassungen von Arbeitsräumen

Die Kursleiter können in jedem Arbeitsraum KI-generierte Zusammenfassungen der Diskussionen anzeigen, um die Gespräche der Teilnehmer zu überwachen, die Ausrichtung auf die Aktivität zu bewerten und zu entscheiden, wann sie einem Raum beitreten möchten. Die Zusammenfassungen werden während der gesamten Sitzung automatisch aktualisiert, wenn Diskussionen stattfinden.

>[!NOTE]
>
>Ein Arbeitsraum muss mindestens 60 Sekunden lang diskutiert werden, bevor eine Zusammenfassung generiert werden kann. Bei weniger aktiven Zimmern wird im Fenster &quot;Zimmer prüfen&quot; keine Zusammenfassung angezeigt.

So zeigen Sie Zusammenfassungen an:

1. Navigieren Sie zu dem Raum, den Sie überprüfen möchten.

1. Wählen Sie **Raum** überprüfen. <br> Ein Popupfenster **Raum überprüfen** mit der Zusammenfassung des Raums wird angezeigt.

   ![Übersicht über die Arbeitsraum-KI](assets/breakout-room-ai-summary.png)
   *Das Popup-Fenster &quot;Raum überprüfen&quot; zeigt die Zusammenfassung des Raums an.*

1. (Optional) Wählen Sie einen anderen Raum aus. Die Zusammenfassung wird aktualisiert, um Details für den ausgewählten Raum anzuzeigen.

### Verwenden von Tools für die Zusammenarbeit in Arbeitsräumen

Nachdem die Kursleiter einem Arbeitsraum beigetreten sind, können sie die gleichen Tools für die Zusammenarbeit verwenden, die in der Hauptsitzung verfügbar sind, um die Teilnehmer zu leiten und mit ihnen zu interagieren. Sie haben folgende Möglichkeiten:

* Chatten Sie mit Teilnehmern, um Fragen zu beantworten und Diskussionen zu ermöglichen. Weitere Informationen finden Sie unter [Über das Chatfenster](./about-the-chat-panel.md).

* Präsentieren Sie Ihren Bildschirm oder Ihre Präsentationen, um Konzepte zu erläutern oder Aufgaben zu demonstrieren. Weitere Informationen finden Sie unter [Über die Bildschirmfreigabe](./about-the-screen-sharing.md).

* Arbeiten Sie mit dem Whiteboard zusammen, um Brainstorming, Anmerkungen und interaktive Aktivitäten zu ermöglichen. Weitere Informationen finden Sie unter [Info zum Whiteboard](./about-the-whiteboard.md).

![Arbeitsraum-Chat-Bereich](assets/breakout-room-chat-panel.png "Arbeitsgruppensitzungsschnittstelle zeigt den Chat-Bereich im Arbeitsgruppenraum an.")

## Beenden einer Arbeitsgruppensitzung

Sie können die Arbeitsgruppensitzung jederzeit beenden.

1. Navigieren Sie zum Bereich **Arbeitsgruppen**.

1. Wählen Sie **Arbeitsgruppen beenden** in der aktiven Arbeitsgruppensitzung. 2 <br>Alle Teilnehmer werden wieder in den Hauptraum verschoben und die Arbeitsgruppensitzung wird für alle Teilnehmer beendet.

   ![Arbeitsgruppensitzung beenden](assets/end-breakout-session.png)
   *Arbeitsgruppensitzung 2 mit Optionen zum Beenden der Arbeitsgruppensitzung.*

## Anzeigen eines Arbeitsgruppensitzungsberichts

Nachdem die Arbeitsgruppensitzung beendet ist, können Sie auf den Bericht der Arbeitsgruppensitzung zugreifen, um die Sitzungsaktivität und die Teilnahme zu überprüfen. Der Bericht enthält die Teilnehmerdetails, eine allgemeine und raumspezifische Zusammenfassung der Arbeitsgruppendiskussionen, Anweisungen für die Teilnehmer sowie eine Übersicht über die Sitzungsdauer und das Engagement.

>[!NOTE]
>
>Für Arbeitsräume mit weniger als 60 Sekunden Gesprächszeit ist keine Zusammenfassung im Bericht enthalten.

So zeigen Sie einen Arbeitsgruppensitzungsbericht an:

1. Navigieren Sie zur geschlossenen Arbeitsgruppensitzung im Bereich **Arbeitsgruppen**.

1. **Berichte anzeigen** auswählen. <br> Das Popupfenster &quot;Arbeitsgruppenbericht&quot; wird mit der Sitzungszusammenfassung geöffnet.

   ![Bericht über Arbeitsgruppensitzungen](assets/breakout-session-report.png)
   *Popup-Fenster für Arbeitsgruppenberichte, in dem der Arbeitsgruppenraumbericht angezeigt wird.*

1. Führen Sie einen der folgenden Schritte aus:
   * Wählen Sie **Alle Räume** aus, um die **Gesamtübersicht** für die Arbeitsgruppensitzung anzuzeigen.
   * Wählen Sie eine Raumregisterkarte aus, um die Zusammenfassung für diesen Raum anzuzeigen.

Alle Erkenntnisse zu Arbeitsgruppensitzungen sind auch im **Sitzungs-Dashboard** verfügbar, in dem Sie Zusammenfassungen überprüfen, die Teilnahme analysieren und die Sitzungsergebnisse nach der Sitzung verfolgen können. Weitere Informationen finden Sie unter [Komponenten des Sitzungs-Dashboards](./components-of-the-session-dashboard.md).

## Erweitern einer Arbeitsgruppensitzung

Wenn mehr Zeit erforderlich ist, können Sie die Arbeitsgruppensitzung verlängern, während sie aktiv ist, indem Sie **Zeit um 2 Minuten verlängern** in den Arbeitsgruppensteuerelementen auswählen, um die Sitzungsdauer zu erhöhen. Sie können die Sitzung während jeder Arbeitsgruppensitzung bis zu zweimal verlängern. Die aktualisierte Dauer wird sofort angewendet, sodass Teilnehmer ihre Aktivitäten ohne Unterbrechung fortsetzen können.

---
title: Live Hub (Beta) in Adobe Learning Manager aktivieren
description: Erfahren Sie, wie Administratoren den Live Hub für ein Konto aktivieren, ihn als Standardanbieter für virtuelle Klassenzimmer festlegen und KI-gestützte Live Hub-Assistenten aktivieren.
source-git-commit: 552ecc22af6d59d80bda48a05ed8b950a500ee0a
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---


# Live Hub (Beta) in Adobe Learning Manager aktivieren

Administratoren können den Live Hub für ein Adobe Learning Manager-Konto aktivieren und KI-gestützte Assistenten konfigurieren, die Kursleiter während Live-Sitzungen unterstützen. Nachdem der Live Hub aktiviert wurde, können Autoren virtuelle Live Hub-Schulungstools verwenden, um virtuelle Klassenzimmermodule für Kurse zu erstellen und zu verwalten.

So aktivieren Sie den Live Hub:

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.

1. Wählen Sie im linken Navigationsbereich **AI in Learning**.

   ![KI in Learning Nav](assets/ai-in-learning-nav.png)
   *Wählen Sie KI im Lernprogramm aus, um den Live-Hub zu aktivieren.*

1. Wählen Sie **Live Hub** aus. <br> Die Seite **Live Hub** wird geöffnet.

   ![Seite mit Einstellungen für Live-Hub](assets/live-hub-settings-page.png)
   *In den Einstellungen für den Live-Hub wird die Option zum Aktivieren des Live-Hub in ALM angezeigt.*

1. Umschalten auf **Live Hub für dieses Konto aktivieren**. <br> Das Dialogfeld &quot;**Live Hub als Standard festlegen**&quot; wird angezeigt.

   ![Standarddialogfeld für Live-Hub festlegen](assets/set-live-hub-default-dialog.png)
   *Wählen Sie im Popup-Fenster &quot;Als Standard festlegen&quot; aus.*

1. Wählen Sie eine der folgenden Optionen aus:

   1. **Als Standard festgelegt**: Macht Live Hub zum Standard-Anbieter für virtuelle Klassenzimmer. Der Live-Hub ist vorab ausgewählt, wenn Autoren ein Modul für ein virtuelles Klassenzimmer für einen Kurs erstellen.

   1. **Nicht jetzt**: Schließt das Dialogfeld, ohne den Standardanbieter für virtuelle Klassenzimmer zu ändern. Sie können diese Einstellung später auf der Seite &quot;Live-Hub&quot; aktivieren.

1. Aktivieren Sie **KI im Live Hub**, um KI-gestützte Assistenten in Live-Sitzungen verfügbar zu machen.

   ![KI im Live-Hub aktivieren](assets/enable-ai-in-live-hub.png)
   *Aktivieren Sie KI im Live Hub, um die Live Hub-Agents zu aktivieren.*

1. Aktivieren Sie die Assistenten über die Live Hub-Agenten:

   1. **Umfrageassistent**: Generiert Umfragen aus dem Kursinhalt und dem Transkript der Live-Sitzung und erstellt so Eisbrecher oder Wissensüberprüfungen, die mit einem Klick überprüft und gestartet werden können. Weitere Informationen finden Sie unter [Erstellen und Starten einer Umfrage](../../getting-started-with-live-hub/create-and-launch-a-poll.md#create-a-poll-using-ai).

   1. **Fragen und Antworten-Assistent**: Erkennt Teilnehmer-Fragen im Session-Chat und entwirft Antworten auf den hochgeladenen Inhalt und das Session-Transkript, die die Kursleiter überprüfen, verfeinern und freigeben können. Weitere Informationen finden Sie unter [Verwenden des Chat-Bereichs als Kursleiter](../../getting-started-with-live-hub/use-the-chat-panel-as-an-instructor.md#draft-replies-to-participant-questions-with-ai).

   1. **Arbeitsgruppenüberwachungsassistent**: Liest die Protokolle jedes Arbeitsraums gegen das Ziel des Kursleiters durch, stellt alle paar Minuten eine Statuskarte bereit und liefert Zusammenfassungen der Diskussionen pro Raum sowie eine einzelne, raumübergreifende Synthese von Themen, Entscheidungen und Lücken für einen sofortigen Rückblick. Weitere Informationen finden Sie unter [Erstellen und Verwalten von Arbeitsgruppensitzungen](../../getting-started-with-live-hub/create-and-manage-breakout-rooms.md#view-ai-generated-summaries-of-breakout-rooms).

   1. **Themengenerator für Aufzeichnungen**: Segmentiert Sessionaufzeichnungen automatisch in benannte Themen mit Zeitstempeln und strukturierten Notizen, sodass ein Teilnehmer direkt zu den benötigten Informationen gelangen oder aus den Notizen lernen kann, ohne die vollständige Aufzeichnung ansehen zu müssen. Weitere Informationen finden Sie unter [Grundlagen von Aufzeichnungen und Transkripten](../../getting-started-with-live-hub/record-a-session.md#generate-topics-in-recording).

   1. **Assistent für die Kursleitersuche**: empfiehlt den Kursleitern eine Sitzung, bei der Fähigkeiten, Verfügbarkeit, Nutzung, bevorzugte Unterrichtszeiten und andere Kriterien gegeneinander abgewogen werden. Weitere Informationen finden Sie unter [Livehub-Sitzung erstellen](../../getting-started-with-live-hub/create-a-live-hub-session.md#add-instructors-using-instructor-finder).

>[!NOTE]
>
> KI-Assistenten können nur konfiguriert werden, wenn KI im Live Hub aktiviert ist. Kursleiter können Assistenten deaktivieren, wenn sie eine Sitzung vorbereiten, aber sie können keinen Assistenten aktivieren, der von einem Administrator deaktiviert wurde.

Weitere Informationen finden Sie unter [Erste Schritte mit Live Hub](../../getting-started-with-live-hub/getting-started-live-hub.md).
---
title: Erstellen Sie einen Kurs mit "Abgesicherter Prüfungsbrowser"
description: Erstellen Sie ein Quiz im Modus "Sichere Prüfung Browser" und fügen Sie es als Modul zum Selbststudium in Adobe Learning Manager zu einem Kurs hinzu, um eine eingeschränkte Lernumgebung bereitzustellen.
source-git-commit: 8f23f95cd81e5b64932281c990d27be0c390850b
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%
---

# Erstellen Sie einen Kurs mit &quot;Abgesicherter Prüfungsbrowser&quot;

Autoren können Quizze zu Kursen hinzufügen, die einen sicheren Prüfungsbrowser erfordern, um eine sichere, eingeschränkte Bewertungsumgebung bereitzustellen. Der abgesicherte Prüfungsbrowser gilt nur für einzelne native Adobe Learning Manager-Quiz und schränkt den Zugriff auf andere Module im Kurs nicht ein.

Bevor Sie das Quiz einem Kurs hinzufügen, vergewissern Sie sich, dass der sichere Prüfungsbrowser für das Quiz aktiviert ist. Wenn der Kurs andere Bereitstellungstypen umfasst, z. B. Module für virtuelle Klassenzimmer, funktionieren diese Module weiterhin unabhängig von den Anforderungen des sicheren Prüfungsbrowsers.

In diesem Artikel wird erläutert, wie Sie einem Kurs ein Quiz mit aktiviertem abgesichertem Prüfungsbrowser hinzufügen und seine Einstellungen für den Kurs konfigurieren.

## Quiz im Modus &quot;Sichere Prüfung im Browser&quot; erstellen

Im abgesicherten Prüfungsbrowser-Modus wird festgelegt, ob Teilnehmer den abgesicherten Prüfungsbrowser verwenden sollen, um das Quiz zu absolvieren. Die Option wird nur angezeigt, nachdem ein Administrator die Integration des sicheren Prüfungsbrowsers für das Konto aktiviert hat. Weitere Informationen finden Sie unter **Abgesicherten Prüfungsbrowser aktivieren**.

So erstellen Sie ein Quiz im abgesicherten Prüfungsbrowser:

1. Melden Sie sich bei der ALM als Autor an.
1. Wählen Sie **Inhalt erstellen** aus.

   Die Seite **Inhaltsbibliothek** wird angezeigt.

1. Wählen Sie **Hinzufügen** > **Quiz**.

   Die Seite **Quiz erstellen** wird geöffnet.

1. Geben Sie einen Namen für das Quiz in das Feld **Name** ein.
1. (Optional) Geben Sie eine Beschreibung für das Quiz in das Feld &quot;Beschreibung&quot; ein.
1. Wählen Sie **Quizfrage hinzufügen** und fügen Sie die **Kriterien für das Bestehen** hinzu.
1. Aktivieren Sie den **Modus für den sicheren Prüfungsbrowser**. Die Option **Autor darf anpassen, während Kurserstellung** angezeigt wird.

   ![Einstellung des Modus für den sicheren Prüfungsbrowser auf der Seite &quot;Quiz erstellen&quot;](assets/quiz-safe-exam-browser-mode-setting.png "Einstellung des Modus für den sicheren Prüfungsbrowser auf der Seite &quot;Quiz erstellen&quot;")

1. (Optional) Aktivieren Sie **Autor darf während der Kurserstellung anpassen**.

   Die Option &quot;Sicherer Prüfungsbrowser&quot; wird angezeigt, wenn Sie den Kurscode konfigurieren.

   >[!NOTE]
   >
   > Wenn der Administrator diese Option aktiviert, können Sie die Anforderung des sicheren Prüfungsbrowsers (SEB) für ein Kursquiz-Modul aktivieren oder deaktivieren. Wenn der Administrator diese Option deaktiviert, wird SEB für das Quiz obligatorisch, und Sie können diese Anforderung nicht ändern. Weitere Informationen finden Sie unter [Integration des abgesicherten Prüfungsbrowsers aktivieren](../../administrators/feature-summary/safe-exam-browser.md#enable-safe-exam-browser-integration).

1. Wählen Sie **Publish** aus.

## Hinzufügen eines Quiz mit aktiviertem Browser für die sichere Prüfung zu einem Kurs

Fügen Sie das Quiz als Modul zum Selbststudium hinzu, für das ein sicherer Prüfungsbrowser erforderlich ist. Stellen Sie vor Beginn sicher, dass das Quiz mit aktiviertem sicheren Prüfungsbrowser veröffentlicht wird. Weitere Informationen finden Sie unter Einen Prüfungsbrowser aktivieren.

Hinzufügen des Quiz zu einem Kurs:

1. Wählen Sie **Kurs erstellen** aus, und geben Sie den Kursnamen und die Beschreibung ein.
1. Wählen Sie **Module hinzufügen** auf der Seite **Module** aus.

   Das Popupmenü &quot;Module&quot; wird angezeigt.

1. Wählen Sie **Selbststudium**. Das Dialogfeld &quot;**Modul zum Selbststudium**&quot; wird geöffnet.

   Dialogfeld &quot;![Modul zum Selbststudium&quot; mit den verfügbaren Quizmodulen](assets/self-paced-module-dialog-quiz-selection.png "Dialogfeld &quot;Modul zum Selbststudium&quot; mit den verfügbaren Quizmodulen")

1. Aktivieren Sie das Kontrollkästchen neben dem Quiz im Browser für sichere Prüfungen, das Sie erstellt haben.
1. Wählen Sie **Hinzufügen** aus. Das Quiz wird dem Kurs als Modul zum Selbststudium hinzugefügt.
1. (Optional) Um dem Kurs einen anderen Bereitstellungstyp hinzuzufügen, wählen Sie **Weitere Bereitstellungstypen hinzufügen** und konfigurieren Sie das erforderliche Modul.
1. Wählen Sie **Speichern** > **Publish**.

   Der Kurs enthält jetzt eine Bewertung, bei der die Teilnehmer den sicheren Prüfungsbrowser verwenden müssen.

Zeigen Sie [Quiz im abgesicherten Prüfungsbrowser starten](../../learners/feature-summary/launch-safe-exam-browser.md) an, um zu erfahren, wie Teilnehmer mit dem abgesicherten Prüfungsbrowser auf Quiz zugreifen und sie absolvieren können.

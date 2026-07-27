---
description: Der Learning Path-Agent in Adobe Learning Manager ist ein KI-gestützter Assistent, der einen benutzerdefinierten, sequenziellen Lernplan basierend auf Ihren Zielen, Ihrem Hintergrund und der verfügbaren Zeit erstellt.
jcr-language: en_us
title: Learning Path Agent (Beta) in Adobe Learning Manager
source-git-commit: d61e81b0df6a6043b938c65adaabecb5699c2ce9
workflow-type: tm+mt
source-wordcount: '1956'
ht-degree: 0%

---


# Was ist ein Learning Path Agent?

Ein Learning Path Agent erstellt einen strukturierten Lernpfad mithilfe des AI-Assistenten. Im Gegensatz zu Standardlernpfaden, die von Ihrem Administrator zugewiesen werden, werden solche Lernpfade durch eine geführte Konversation generiert. Sie beschreiben Ihr Ziel und der Agent erstellt einen Pfad, der zu Ihren Lernanforderungen passt.

Der Support-Mitarbeiter bezieht zunächst Inhalte aus dem internen Kurskatalog Ihrer Organisation und priorisiert Kurse, die genehmigt sind und für Ihr Team relevant sind. Wenn Ihr Administrator Inhalte von Drittanbietern aktiviert hat, kann der Agent auch Kurse von verbundenen externen Anbietern einbeziehen, um Lücken in der Abdeckung zu schließen. Sie werden für die Kurse innerhalb Ihres gespeicherten Pfads immer automatisch registriert, sodass Sie sofort mit dem Lernen beginnen können.

Personalisierte Lernpfade wurden für zwei Hauptanwendungsfälle entwickelt:

- **Gezielte Kompetenzentwicklung**: Wenn Sie ein bestimmtes Geschäftsergebnis erzielen oder schnell ein Leistungsziel erreichen müssen, z. B. die Vorbereitung auf eine neue Verantwortung oder den Abschluss einer Qualifikationslücke, die in einer Überprüfung identifiziert wurde.
- **Aufbau umfangreicher Expertise**: Wenn Sie in einem bestimmten Bereich, einer Technologie oder einem Fachgebiet über einen längeren Zeitraum vom Anfänger zum Experten wechseln möchten.

## Funktionsweise des konversationsbasierten Ansatzes

Der Agent trifft Sie, wo Sie sind. Sie beginnen, indem Sie beschreiben, was Sie lernen möchten, in einfacher Sprache, so viel oder so wenig Details, wie Sie haben. Der Support-Mitarbeiter stellt dann Anschlussfragen, um Ihre Rolle, Ihre spezifischen Herausforderungen und den Zeitaufwand für das Lernen pro Woche zu verstehen.

Anhand Ihrer Antworten identifiziert der Support-Mitarbeiter 3 bis 5 Lernthemen mit vorgeschlagenen Kompetenzstufen. Sie können diese Themen überprüfen, Änderungen anfordern oder bestätigen, bevor der Agent nach entsprechenden Kursen sucht. Der Agent generiert dann einen benannten Lernpfad, der jeden Kurs, seine Beschreibung, Dauer und Modulanzahl anzeigt. Du kannst den Pfad weiter anpassen, bevor du ihn speicherst.

Wenn Sie den Pfad speichern, werden Sie automatisch für alle Kurse registriert. Der Pfad wird auf Ihrer Startseite im Abschnitt _Personalisierte Lernpfade_ angezeigt und kann jetzt beginnen.

### Inhaltsquellen und Kursauswahl

Der Support-Mitarbeiter wählt Kurse basierend auf der Relevanz für das angegebene Ziel, Ihrem aktuellen Kenntnisstand, der gesamten verfügbaren Zeit und der Aktualisierung des Inhalts aus. Wenn der Agent für ein bestimmtes Thema im verfügbaren Katalog keine passenden Kurse findet, teilt er Ihnen dies mit und schlägt vor, sich an Ihren Administrator zu wenden, um zusätzliche Inhalte für diesen Bereich anzufordern.

### Personalisierte Lernpfade auf der Startseite

Alle gespeicherten personalisierten Lernpfade werden in der Leiste _Personalisierte Lernpfade_ auf Ihrer Startseite angezeigt. Jede Karte zeigt den Pfadnamen, die Anzahl der Kurse und eine _Weiter_-Schaltfläche an, um an der Stelle fortzufahren, an der Sie aufgehört haben.

### Freigeben eines Lernpfads

Nachdem Sie einen personalisierten Lernpfad gespeichert haben, können Sie ihn für Kollegen freigeben. Bei der Freigabe wird ihnen ein Link oder eine E-Mail-Einladung gesendet. Wenn ein Kollege einen gemeinsamen Pfad öffnet, kann er sich mit einer einzigen Aktion registrieren. Das Freigeben ist nützlich, wenn mehrere Personen in Ihrem Team ähnliche Lernziele haben und Sie möchten, dass sie demselben strukturierten Plan folgen.

### Best Practices

- Beschreiben Sie Ihr Lernziel so genau wie möglich, wenn Sie die Unterhaltung beginnen. Je mehr Kontext der Agent hat, desto relevanter ist Ihr Pfad.
- Gebt vorab eure Zeit an, damit der generierte Pfad zu eurem tatsächlichen Zeitplan passt. Der Agent versteht natürliche Sprache: &quot;zwei Abende pro Woche&quot; oder &quot;30 Minuten pro Tag&quot; sind beide gültig.
- Überprüfen Sie die vorgeschlagenen Themen, bevor Sie den Agenten bitten, Kurse zu generieren. Das Bestätigen oder Anpassen von Themen in dieser Phase spart Zeit, verglichen mit dem anschließenden Überarbeiten der Kursliste.
- Wenn ein Thema keine übereinstimmenden Inhalte enthält, notieren Sie es und wenden Sie sich an Ihren Administrator, um anzufordern, dass dem Katalog relevante Kurse hinzugefügt werden.

## Konfigurieren Sie den Agenten für den personalisierten Lernpfad

Der Agent für einen personalisierten Lernpfad ist in Adobe Learning Manager standardmäßig aktiviert, wenn Sie die Option &quot;AI-Assistent&quot; in den Einstellungen aktivieren.

>[!NOTE]
>
> Die Inhaltssichtbarkeit entspricht Ihren vorhandenen Katalogzugriffsregeln. Teilnehmer können Kurse nur aus Katalogen anzeigen und empfangen, auf die sie bereits Zugriff haben.\ Der Agent für den personalisierten Lernpfad umgeht keine Katalogbeschränkungen.

Innerhalb jeder Quelle ordnet der Agent die Kurse nach Relevanz für das Ziel des Teilnehmers und danach, wie gut die Kursebene mit den angegebenen Kenntnissen des Teilnehmers übereinstimmt.

Wenn für ein Thema im Katalog keine entsprechenden Kurse verfügbar sind, benachrichtigt der Agent den Teilnehmer und schlägt vor, sich an einen Administrator zu wenden, um Inhalte für diesen Bereich anzufordern.

<!-- 
### Monitor credit usage

The Personalized Learning Path agent consumes AI credits each time a learner generates a path. To monitor and manage usage:

1. In the left navigation of the administrator's home page, select **Billing**.
2. Select the **AI Credits** tab. The **Learning Path** agent appears as a line item in the features list.
3. Review current usage and adjust the credit allocation or usage limit as needed.

>[!CAUTION]
>
>If the credit limit for the Learning Path agent is reached, learners receive an in-app message that the agent is unavailable and are directed to contact an administrator. Increase the allocation to restore access. 
-->

## Erstellen eines personalisierten Lernpfads mit dem Teilnehmer-KI-Assistenten

Verwenden Sie den Teilnehmer-KI-Assistenten in Adobe Learning Manager, um einen personalisierten Lernpfad zu generieren, der zu Ihrem Ziel, Ihrem Hintergrund und der verfügbaren Zeit passt. Speichere es dann in deinem Profil, um sofort mit dem Lernen zu beginnen.

### Öffnen Sie den Teilnehmer-KI-Assistenten und starten Sie eine Konversation.

1. Wählen Sie auf der Startseite **AI Assistant** aus.
2. Geben Sie Ihr Lernziel in das Textfeld ein. Sei so genau wie möglich. Beispiel:
   - *Ich bin Softwareentwickler und möchte mit dem Cursor einen AI-Agenten erstellen.*
   - *Ich wurde gerade zu einer Managerrolle befördert und möchte lernen, wie mit schwierigen Unterhaltungen umgegangen wird.*
   - *Ich möchte die Finanzmodellierung als Analyst beherrschen.*
     ![](assets/ai-assistant.png)

3. Wählen Sie optional _+ Neuer Chat_ aus, um eine neue Unterhaltung zu starten, wenn vorherige Sitzungen geöffnet sind.

Hinweise:

- Optional können Sie ein Dokument mit dem Symbol _Papierclip_ anhängen, z. B. einen Lebenslauf, eine Manager-Feedback-E-Mail oder eine Projektbeschreibung. Der Agent verwendet das Dokument, um mehr Kontext zu Ihrem Lernziel und Ihrem Hintergrund zu erhalten.
- Wählen Sie _Senden_ aus.

### Ziel und Hintergrund beschreiben.

Der Agent antwortet mit einer Nachricht, in der er dein Ziel bestätigt, und bittet um zusätzlichen Kontext, um deinen Pfad anzupassen. In der Regel werden folgende Fragen gestellt:

- _Ihre aktuelle Rolle und Ihr Hintergrund_, was Sie bereits wissen, wie lange Sie in Ihrer Rolle tätig sind oder über eine relevante Erfahrung verfügen.
- _Ihre spezifischen Herausforderungen oder Szenarien_ die Situationen in der realen Welt, in denen Sie dieses Lernen benötigen, um es sofort zu lösen.
- _Ihre Zeitverpflichtung_ gibt die Anzahl der Stunden pro Woche an, die Sie realistischerweise für das Lernen verwenden können.

![](assets/goal-background.png)

Sie müssen nicht jede Frage beantworten. Die einzige Eingabe, die erforderlich ist, ist Ihr Lernziel oder Ihre Herausforderung. Der Support-Mitarbeiter wird mit dem von Ihnen angegebenen Kontext fortfahren.

>[!TIP]
>
>Der Agent versteht natürliche Zeitausdrücke. Sie können sagen &quot;zwei Abende pro Woche&quot;, &quot;etwa 30 Minuten pro Tag&quot; oder &quot;ein paar Stunden am Wochenende&quot;, und der Agent konvertiert es in wöchentliche Stunden, um es zu schätzen und bestätigt es mit Ihnen.

Geben Sie Ihre Antwort ein und wählen Sie _Senden_.

![](assets/time-commitment.png)

Setzen Sie die Unterhaltung fort, bis der Agent Ihre vorgeschlagenen Themen präsentiert.

![](assets/suggested-topics.png)

### Überprüfen der vorgeschlagenen Themen

Nachdem der Agent genügend Kontext gesammelt hat, präsentiert er eine Liste von 3 bis 5 Lernthemen mit jeweils einem Titel, einer kurzen Beschreibung und einem vorgeschlagenen Kenntnisstand.

1. Lesen Sie die Themenliste sorgfältig durch. Der Agent wählt die Kenntnisstufen basierend auf dem, was Sie freigegeben haben, aber Sie können Änderungen anfordern.
2. Um ein Thema anzupassen, um beispielsweise die Kenntnisstufe zu ändern oder ein Thema zu tauschen, geben Sie Ihr Feedback im Chat ein. Zum Beispiel habe ich bereits Kenntnisse über das erste Thema. Können Sie das auf &quot;Mittel&quot; setzen?
3. Wenn Sie mit den Themen wie vorgeschlagen zufrieden sind, bestätigen Sie sie, indem Sie im Chat antworten oder die vorgeschlagene Bestätigungsaufforderung auswählen, falls eines angezeigt wird.

### Lernpfad überprüfen

Der Agent durchsucht den verfügbaren Katalog und erstellt einen benannten Lernpfad. Der Pfad zeigt Folgendes an:

- Der Pfadname und die geschätzte Gesamtdauer
- Titel, Beschreibung, Dauer und Modulanzahl jedes Kurses
- Ein Hinweis, wenn für einige Themen keine übereinstimmenden Inhalte verfügbar waren

Wenn einige Themen keinen übereinstimmenden Inhalt haben:

Der Support-Mitarbeiter informiert Sie darüber, dass er keine Kurse für diese spezifischen Themen finden konnte, und schlägt vor, sich an Ihren Administrator zu wenden, um Inhalte für diese Bereiche anzufordern. Der Pfad wird weiterhin für die Themen generiert, in denen Kurse gefunden wurden.

<!-- - Review the path. If you want to change something, for example, remove a course, adjust the scope, or explore different topics. Type your request in the chat\. For example, Can you remove the first course and replace it with something shorter? -->
Wenn Sie mit dem Pfad zufrieden sind, bitten Sie den Agenten, ihn zu speichern, indem Sie den Lernpfad speichern eingeben.

![](assets/create-lp.png)

### Speichern und Zugriff auf Ihren Lernpfad

Wenn Sie den Pfad speichern, bestätigt der Agent den Speichervorgang und registriert Sie automatisch für alle Kurse innerhalb des Pfads.

Zugriff auf Ihren Pfad:

- Wählen Sie in der Bestätigungsmeldung _Gehe zum Lernpfad_, um ihn sofort zu öffnen, oder
- Sie können ihn jederzeit im Streifen _Personalisierte Lernpfade_ auf Ihrer Startseite finden.

### Freigeben Ihres Lernpfads

Über die Pfadübersichtsseite können Sie Ihren gespeicherten Pfad für Kollegen freigeben.

1. Öffnen Sie den gespeicherten Pfad aus dem Streifen _Personalisierte Lernpfade_ auf Ihrer Startseite.
2. Wählen Sie _Freigeben_ aus.
3. Geben Sie den generierten Link frei oder geben Sie E-Mail-Adressen ein, um eine direkte Einladung zu senden.

Ein Kollege, der den freigegebenen Link erhält, kann sich mit einer einzigen Aktion für den Pfad registrieren.

## Best Practices

- Erstellt einen Kontext zu eurer Rolle und euren aktuellen Herausforderungen. Je genauer Sie sind, desto relevanter ist die Kursauswahl.
- Erwähnen Sie Ihren wöchentlichen Zeitaufwand in natürlicher Sprache. Der Agent bestätigt seine Interpretation, bevor er den Pfad generiert.
- Überprüfen Sie die vorgeschlagenen Themen, bevor Sie nach der Pfadgenerierung fragen. Das Anpassen von Themen in dieser Phase ist schneller als das nachträgliche Überarbeiten der Kursliste\.
- Wenn der generierte Pfad Kurse enthält, die Sie bereits abgeschlossen haben, teilen Sie dies dem Support-Mitarbeiter mit. Es kann Alternativen vorschlagen.

## Häufige Fragen

_Wo finde ich meine gespeicherten personalisierten Lernpfade?_

Alle Ihre gespeicherten Pfade werden in der Leiste _Personalisierte Lernpfade_ auf Ihrer Startseite angezeigt. Jede Karte zeigt den Pfadnamen und die Schaltfläche _Weiter_ an. Sie können von dort aus auch einen beliebigen Pfad öffnen, um die vollständige Kursliste und Ihren Fortschritt anzuzeigen.

_Wie viele personalisierte Lernpfade kann ich speichern?_

Der Streifen _Personalisierte Lernpfade_ auf Ihrer Startseite zeigt maximal 10 Pfade an.

_Welche Informationen muss ich angeben, um einen relevanten Lernpfad zu erhalten?_

Beschreiben Sie mindestens Ihr Lernziel oder die spezifische Herausforderung, die Sie angehen möchten. Je mehr Kontext Sie angeben, desto besser ist der Pfad\. Zu den nützlichen Informationen gehören Ihre aktuelle Rolle, die Dauer, über die Sie diese Rolle bereits ausgeübt haben, alle relevanten Vorkenntnisse und die Anzahl der Stunden pro Woche, die Sie sich realistischerweise für das Lernen wünschen.

_Was passiert, wenn der Agent keine passenden Kurse für meine Themen finden kann?_

Der Agent teilt Ihnen direkt in der Unterhaltung mit, dass er keine passenden Kurse für eines oder mehrere Ihrer Themen finden konnte. Der Pfad wird nur mit den Themen generiert, in denen Kurse verfügbar waren.

Wenn der Agent für keines Ihrer Themen Kurse finden kann, wird er Sie darüber informieren, dass er keinen Pfad für dieses Ziel erstellen kann. Wenden Sie sich in jedem Fall an Ihren Lernadministrator und teilen Sie ihm mit, welche Themen keinen Inhalt hatten. Sie können dem Katalog relevante Kurse hinzufügen, damit zukünftige Pfadanfragen abgedeckt werden.

<!-- 
_How does the agent decide which courses to include?_

The agent prioritizes your organization's internal course catalog above external sources. It selects courses based on relevance to your stated goal, whether the course level matches your proficiency, how recently the content was published or updated, and quality signals such as ratings and completion rates\. Your administrator controls which content sources are available. 
-->

_Kann ich die Themen in meinem Lernpfad anpassen?_

Ja. Während der Unterhaltung können Sie den Agenten bitten, Themen hinzuzufügen, zu entfernen oder zu ändern, bevor der Pfad generiert wird. Der Agent aktualisiert die Themenliste und generiert den entsprechenden Pfad neu.

_Kann ich die einzelnen Kurse in einem generierten Pfad ändern?_

Anzahl Sobald der Agent einen Pfad generiert hat, wird die Kursauswahl behoben. Sie können einzelne Kurse nicht austauschen, entfernen oder ersetzen. Was der Agent empfiehlt, ist, was der Pfad enthält.

Wenn sich die vorgeschlagenen Kurse nicht richtig anfühlen, empfiehlt es sich, zurückzugehen und Ihre Themen vor dem Generieren anzupassen. Der Support-Mitarbeiter wählt Kurse basierend auf den von Ihnen bestätigten Themen aus. Wenn Sie also den Themenbereich oder die Kompetenzstufe ändern, erhalten Sie einen anderen Kurssatz.

_Warum stellt der Agent weiterhin Anschlussfragen?_

Der Support-Mitarbeiter benötigt ausreichende Klarheit über Ihr Lernziel, um relevante Themen zu identifizieren. Wenn deine ursprüngliche Botschaft umfassend war, z. B. &quot;Ich möchte Marketing lernen&quot;, werden Fragen gestellt, um den Umfang einzugrenzen. Wenn Sie spezifischere Details zu Ihrer Rolle, den Herausforderungen, mit denen Sie konfrontiert sind, und den Möglichkeiten, die Sie nach dem Lernen nutzen möchten, angeben, kann der Agent schneller zur Themengenerierung wechseln.
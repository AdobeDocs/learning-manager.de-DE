---
description: Der AI Assistant (Beta) für Teilnehmer ist eine Gen-AI-gestützte Chat-Ergänzung in Adobe Learning Manager, die Teilnehmern hilft, schnelle, präzise Antworten auf ihre zugewiesenen Lerninhalte zu erhalten. Mithilfe von Anfragen in natürlicher Sprache können Teilnehmer zielgerichtete Antworten mit klaren Zitaten sofort abrufen. So ist es ganz einfach, die richtigen Informationen zu finden, die Quellen zu verifizieren und effizient zu lernen, ohne den gesamten Kurs durchsuchen zu müssen.
jcr-language: en_us
title: AI Assistant für Teilnehmer in Adobe Learning Manager
exl-id: 8203488d-74a6-4463-9383-76d16cabccfa
source-git-commit: 64765bdd9f364267f7c7f5d23a03cc576b875be3
workflow-type: tm+mt
source-wordcount: '2008'
ht-degree: 0%

---

# KI-Assistent für Teilnehmende

Mit dem AI Assistant (Beta) für Teilnehmer können sie schnell Antworten auf die zugewiesenen Lerninhalte finden, ohne sich durch ganze Kurse bewegen zu müssen. Sie können Fragen in verständlicher Sprache stellen und erhalten präzise, zielgerichtete Antworten mit Quell-Links zu den relevanten Kursinhalten.

>[!IMPORTANT]
>
>Der AI Assistant für Teilnehmer ist derzeit als Betafunktion verfügbar. Funktionen, unterstützte Szenarien und Einschränkungen können sich mit der Weiterentwicklung der Funktion ändern.


## Was ist der KI-Assistent für Teilnehmer?

Der AI Assistant ist ein Gen-KI-gestützter Chat-Begleiter in Adobe Learning Manager, der schnelle, präzise Antworten auf Teilnehmerfragen bietet, indem er die vertrauenswürdigen Lerninhalte nutzt, die ihm in Adobe Learning Manager zur Verfügung stehen. Es enthält auch Zitate, sodass die Teilnehmer immer wissen, aus welcher Quelle die Informationen stammen.

### Wichtigste Funktionen des AI Assistant

1. Intelligente Fragenantworten
   * Gespräche mit einer und mehreren Gängen
   * Natürliches Sprachverständnis auf Englisch
   * Antworten auf Kurse, Zertifizierungen, Lernpfade und Arbeitshilfen
   * Intelligente Klärung von Fragen bei mehrdeutigen Abfragen
   * Unterstützt von Azure Open AI LLM-Funktionen zum Generieren von Antworten
2. Inhaltsquellen und Zitate
   * Ruft Antworten aus verfügbaren Ressourcen ab, die in unterstützten Katalogen vorhanden sind.
   * Bietet Zitaten direkte Verknüpfungen zu Quellmaterialien
   * Unterstützt alle ALM-Inhaltsformate statisch und interaktiv: PDF, DOCX, PPTX, XLSX, Audio (mp3, wav, m4a), Video (mp4, mov, wmv), HTML, SCORM 2004, SCORM 1.2
3. Benutzererfahrung
   * Seitenbedienfeld, über alle Teilnehmerseiten zugänglich
   * Responsive Design zur Anpassung an den Inhaltsbereich
   * Der Chat-Verlauf wird in einer Browsersitzung verwaltet
   * Bei neuer Anmeldung oder Seitenaktualisierung ungefähren
   * Lehrer- oder Tutorenton: freundlich, klar und pädagogisch fundiert
4. Administratorsteuerelemente
   * Funktion auf Kontoebene aktivieren oder deaktivieren
   * Steuern des Zugriffs durch Benutzergruppen
   * Auswählen, welche Kataloge für KI-Antworten eingeschlossen werden sollen
   * Annahme der Nutzungsbedingungen gemäß den Richtlinien von Adobe AI

## Welche Inhaltstypen unterstützt der KI-Assistent?

Der KI-Assistent ruft Informationen aus den Lerninhalten ab, die Ihnen zugewiesen sind, darunter:

* **Dokumente:** PDF, Word, PowerPoint, Excel, HTML
* **Medien:** Audio (mp3, wav, m4a), Video (mp4, mov, wmv)
* **Interaktiver Inhalt:** SCORM 1.2, SCORM 2004
* **Lernobjekttypen:** Kurse, Lernpfade, Zertifizierungen, Arbeitshilfen

Adobe transkribiert Lerninhalte sicher mithilfe von vertrauenswürdigen Verarbeitungs-Services von Drittanbietern, die in der privaten VPC-Umgebung von Adobe gehostet werden.

### Einschränkungen bei Katalogen und Inhaltsquellen

Der Teilnehmer-KI-Assistent verwendet nur Inhalte aus **internen Katalogen** die von Administratoren explizit konfiguriert werden.

Die folgenden Inhaltsquellen werden in **aktuellen Version** nicht unterstützt):

* Freigegebene Kataloge
* Acquired Catalogs
* Externe Kataloge
* Standardkataloge
* Drittanbieter-Inhaltsbibliotheken (z. B. LinkedIn Learning oder Go1)

Wenn ein Teilnehmer keinen Zugriff auf einen Kurs oder eine Arbeitshilfe hat, zeigt der KI-Assistent keine Informationen aus diesem Inhalt an, und die Zitat-Links sind nicht verfügbar.

## Anwendungsfälle des KI-Assistenten

### Technischer Teilnehmer

Sarah ist Vertriebsingenieurin und lernt Grafikkarten kennen. Sie muss schnell die technischen Spezifikationen und Vorteile verstehen, um Kundenfragen zuverlässig beantworten zu können.

Die KI-Assistentin unterstützt Sarah bei folgenden Aufgaben:

* Klare, technische Erklärung der komplexen GPU-Architektur
* Vertiefen Sie das Verständnis für die verschiedenen Grafikkarten und ihre Unterschiede
* Erläuterung von Beispielen, damit Sarah Funktionen mit Anwendungsfällen aus der realen Welt in Beziehung setzen kann

### Support

Marcus ist Supportspezialist bei einer Partnerfirma. Er braucht schnelle Antworten auf seine Fragen zu Produktfunktionen, um Kunden zu helfen, ohne zu Entwicklungs-Teams zu eskalieren.

Der KI-Assistent unterstützt Marcus bei folgenden Aufgaben:

* Relevante Support-Inhalte für häufig gestellte Kundenanfragen finden
* Klärende Fragen stellen, wenn die erste Antwort nicht spezifisch genug ist
* Finden von Empfehlungen für verwandte Fehlerbehebungskurse, um seine Kenntnisse zu verbessern

### Onboarding neuer Mitarbeiter

Jennifer ist gerade dem Unternehmen beigetreten und wird von der Menge an Schulungsmaterial überwältigt. Sie benötigt eine Möglichkeit, bestimmte Informationen zu finden, ohne den gesamten Kurs zu überprüfen.

Die KI-Assistentin unterstützt Jennifer bei folgenden Aufgaben:

* Abrufen einer schrittweisen Anleitung zum Einreichen von Spesenabrechnungen
* Ermitteln von Kursen zu Unternehmensrichtlinien, ohne den gesamten Katalog durchsuchen zu müssen
* Sie wird zum entsprechenden Abschnitt eines Kurses geleitet, ohne stundenlanges Video zu sehen

## Wie nutzt der AI Assistant Inhalte?

Der KI-Assistent hilft Ihnen dabei, während des Lernens schnell präzise Antworten zu finden. Damit Sie sie effektiv einsetzen können, sollten Sie wissen, welche Inhalte die Assistenzkraft verwendet, welche Inhalte sie nicht verwendet und wie sie Antworten generiert.

### Welche Inhalte nutzt der AI Assistant?

Der AI Assistant beantwortet Fragen ausschließlich mit den vom Kontoadministrator aktivierten Lerninhalten. Der Inhalt des Katalogs wird indiziert.

Der AI Assistant analysiert Ihre zugewiesenen Lerninhalte, um zielgerichtete und kontextbezogene Antworten zu generieren.

* Jede Antwort enthält Zitate, die auf den ursprünglichen Quellinhalt verweisen.
* Sie können eine Erwähnung auswählen, um direkt zum entsprechenden Kurs, Modul oder Dokument zu navigieren.
* Zitate helfen Ihnen dabei, Informationen zu verifizieren und bei Bedarf zusätzlichen Kontext zu erkunden.

### Streaming-Antworten

Eine Streaming-Antwort bedeutet, dass der AI Assistant die Antwort während der Generierung progressiv bereitstellt, sodass Benutzer sofort mit dem Lesen der Antwort beginnen können, ohne darauf warten zu müssen, dass die gesamte Antwort vollständig geladen ist.

### Zitate und Quellentransparenz

Jede Antwort des AI Assistant umfasst Zitate, die direkt mit dem ursprünglichen Kurs, Modul oder Lernobjekt verknüpft sind. Mit Zitaten können Sie:

* Wählen Sie eine Inline-Zitatnummer aus, um zum exakt referenzierten Abschnitt zu springen.
* Öffnen Sie die vollständige Quellliste, indem Sie unten in der Antwort Quellen anzeigen auswählen.
* Informationen überprüfen und zusätzlichen Kontext aus der maßgeblichen Quelle erkunden

>[!IMPORTANT]
>
>Der AI-Assistent bietet Antworten auf Basis von Inhalten, die vom Administrator aktiviert wurden. Wenn ein Benutzer jedoch keinen Zugriff auf ein referenziertes Element hat, wird ihm beim Öffnen die Meldung &quot;Nicht unterstützt&quot; angezeigt.


## Integrierte Eingabeaufforderungen

Der AI Assistant umfasst integrierte Eingabeaufforderungen, die Teilnehmern den schnellen Einstieg in häufige Fragen und Szenarien erleichtern. Diese Anweisungen leiten die Teilnehmer dazu, wie sie mit dem Assistenten interagieren, und zeigen die Arten von Fragen an, die sie stellen können.

![Integrierte Eingabeaufforderungen vom Teilnehmerassistenten bereitgestellt](assets/built-in-prompt-new.png)

Integrierte Eingabeaufforderungen können pro Konto angepasst werden. Unternehmen können sie an ihre Lernziele, Teilnehmerrollen, Terminologie oder spezifische Anwendungsfälle anpassen. Administratoren können mit ihrem Customer Success Manager (CSM) integrierte Eingabeaufforderungen konfigurieren oder aktualisieren.

Die Eingabeaufforderung wird auf Kontoebene verwaltet und kann in der aktuellen Version nicht direkt in der Adobe Learning Manager-Benutzeroberfläche konfiguriert werden.

## Administrator-Setup - Aktivieren des AI-Assistenten für Teilnehmer

![KI-fähiger Teilnehmerassistent](assets/learner-ai-assistant-new.png)

Administratoren wählen aus, welche Benutzergruppen und internen Kataloge auf die AI Assistant-Funktion zugreifen können. Sie sollten sicherstellen, dass die zugewiesenen Kataloge nur die Lerninhalte enthalten, die für die Anzeige durch AI-Antworten und Zitate geeignet sind, und dass diese Kataloge &quot;Standard&quot;, &quot;Intern&quot;, &quot;Nicht freigegeben&quot;, &quot;Erworben&quot; oder &quot;Extern&quot; sind.

Stellen Sie vor dem Konfigurieren des KI-Assistenten sicher, dass Sie über Administratorberechtigungen verfügen und ermittelt haben, welche Benutzergruppen und Kataloge Zugriff auf die Funktion haben sollen.

### Konfigurieren des Zugriffs auf den KI-Assistenten

So aktivieren Sie den Teilnehmer-KI-Assistenten:

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.

2. Wählen **auf** Startseite die Option „Einstellungen“ aus.
   ![Administratorkonsole mit der Option „Einstellungen“ im linken Bereich](assets/settings-menu.png)

3. Wählen Sie **Teilnehmer-KI-Assistent (Beta** aus dem Menü **Einstellungen** aus.
   ![Die Administratorkonsole zeigt die Option „Teilnehmer-KI-Assistent“ im linken Bereich an](assets/learner-assistant-ai-beta.png)

4. Wählen Sie den Umschalter aus, um den **Teilnehmer-KI-Assistenten (Beta) zu**.
   ![Die Administratorkonsole zeigt den für den Teilnehmer-KI-Assistenten aktivierten Umschalter an](assets/learner-assistant-toggle.png)

5. Wählen Sie eine oder mehrere Benutzergruppen aus der Option **Berechtigte**) aus.

6. Wählen **Speichern**, um die Benutzergruppeneinstellungen anzuwenden.

7. Wählen Sie einen oder mehrere Kataloge aus der Option **Geeignete Kataloge** aus.

8. Wählen **Speichern**, um die Katalogeinstellungen anzuwenden.

>[!IMPORTANT]
>
>Der KI-Assistent unterstützt nur interne Kataloge. Wenn ein freigegebener, erworbener, externer oder anderer nicht interner Katalog ausgewählt ist, wird sein Inhalt vom KI-Assistenten nicht angezeigt, selbst wenn der Katalog in der Liste Mögliche Kataloge aufgeführt ist.

## Teilnehmerleitfaden - Starten des KI-Assistenten

### Starten des KI-Assistenten

So starten Sie den KI-Assistenten:

1. Melden Sie sich bei Adobe Learning Manager als Teilnehmer an.

2. Wählen **auf der Startseite**&#x200B;Ask AI Assistant) aus.
   ![Auf der Teilnehmer-Startseite wird Ask AI Assistant angezeigt, um das Bedienfeld Learner AI Assistant auszuwählen und zu öffnen](assets/ask-ai-assistant.png)

3. Wenn der Bildschirm **Teilnehmer-KI** angezeigt wird, wählen Sie **Erste Schritte**.
   ![Wählen Sie Erste Schritte aus, um den Teilnehmer-Assistenten zu starten](assets/get-started-learner-assistant.png)

>[!NOTE]
>
>Beim erstmaligen Starten des KI-Assistenten müssen Sie vor dessen Verwendung Ihr Einverständnis einholen. Das Zustimmungsdialogfeld wird nur während dieses ersten Starts angezeigt. Für alle nachfolgenden Starts werden Sie direkt zum AI Assistant weitergeleitet, wo Sie Ihre Eingabeaufforderungen eingeben können.

&#x200B;4. Geben Sie die Eingabeaufforderung in das Textfeld ein.

![Eingabeaufforderung im Teilnehmerassistenten eingeben](assets/type-prompt-new.png)

5.Drücken Sie **Enter**, um eine Antwort zu erhalten. Prüft eure Antworten, Quellen und Empfehlungen.

Sie haben folgende Möglichkeiten:

* Wählen Sie die Zitatnummer inline aus, um zum exakt referenzierten Abschnitt zu springen.
* Öffnen Sie die vollständige Liste der Quellen, indem Sie unten in der Antwort **Quellen anzeigen** auswählen.

![Quellen in der Antwort anzeigen](assets/show-sources-latest.png)

Der AI Assistant enthält Zitate mit allen Antworten, um zu zeigen, woher die Informationen stammen. Jede Erwähnung wird direkt mit dem ursprünglichen Kurs, Modul oder Lernobjekt verknüpft, mit dem die Antwort generiert wurde.

Sie können ein beliebiges Zitat auswählen, um die Kursseite im Adobe Learning Manager zu öffnen und den gesamten Inhalt im Kontext zu überprüfen. Zitate helfen Ihnen dabei, Informationen zu verifizieren, zusätzliche Details zu erkunden und weiterhin von der maßgeblichen Quelle zu lernen.

## Zugriff auf den AI Assistant über die Suche

Sie können den AI-Assistenten auch direkt über die Suchleiste starten. Geben Sie Ihre Frage in das Suchfeld ein und wählen Sie dann **AI-Assistenten fragen** aus den Optionen aus, die angezeigt werden, um Antworten von Ihren zugewiesenen Lerninhalten zu erhalten. Die zugewiesenen Lerninhalte.

![Zugriff auf den Teilnehmerassistenten über die Suchleiste](assets/learner-assistant-search-new.png)


## Feedback zu den Antworten des Teilnehmer-KI-Assistenten geben

Ihr Feedback zu den vom Teilnehmer-KI-Assistenten (Beta) generierten Antworten trägt dazu bei, die Genauigkeit, Relevanz und die Gesamtleistung zu verbessern.

### Antwort mögen oder ablehnen

* Wählen Sie **Minimieren**, wählen Sie aus, was Ihnen in der Antwort hilfreich war, fügen Sie optional Kommentare hinzu, und wählen Sie dann **Senden** aus.

![&quot;Miniaturen nach oben&quot; auswählen, um eine Antwort zu unterstützen](assets/la-feedback.png)

* Wählen Sie **Minimieren**, wählen Sie den Grund aus, aus dem die Antwort nicht hilfreich war, fügen Sie Kommentare hinzu, und wählen Sie dann **Senden** aus.

## Neuen Chat im AI Assistant starten

Das Starten eines neuen Chats ermöglicht es dem Benutzer, eine neue Unterhaltung zu beginnen, wobei der vorherige Kontext gelöscht wird, sodass sich der Assistent auf das neue Thema konzentrieren kann, ohne auf vorherige Interaktionen zu verweisen. Dies ist wichtig, wenn Themen gewechselt oder Antworten gesucht werden, die nicht mit früheren Fragen in Zusammenhang stehen.

Löscht das aktuelle Gespräch und beginnt jederzeit einen neuen Chat.

Wählen **Neuer Chat** im Bildschirm des KI-Assistenten aus und klicken Sie dann auf **Ja**.

![Starten Sie einen neuen Chat im Teilnehmer-Assistenten](assets/start-new-chat.png)

Der KI-Assistent bietet Lernenden schnelle, kontextuelle Antworten, unterstützt mehrere Inhaltstypen und bietet Inline-Zitate für Transparenz. Administratoren können den Zugriff steuern und sicherstellen, dass der KI-Assistent auf die organisatorischen Anforderungen zugeschnitten ist und das Lernerlebnis verbessert.


## Fehlerbehebung

>[!NOTE]
>
>Warten Sie nach der Konfiguration eines neuen Katalogs 4-5 Stunden, bis der Inhalt indiziert und für Antworten des KI-Assistenten verfügbar ist.

### Szenario 1: Kein Zugriff auf Inhalte

Problem: Der Teilnehmer hat Zugriff auf den Teilnehmer-Assistenten, erhält jedoch Antworten von „Ich habe keine Antwort auf diese Frage“.

**Mögliche Ursachen**

* Die Kataloge der Teilnehmer sind bei der Konfiguration des KI-Assistenten nicht enthalten
* Der mit der Frage in Zusammenhang stehende Inhalt ist nicht in ausgewählten Katalogen enthalten oder die Kataloge sind leer.
* Teilnehmer hat keine Sichtbarkeit für relevante Inhalte

**Lösung**

* Überprüfen des Katalogzugriffs des Teilnehmers
* Überprüfen, welche Kataloge in den Einstellungen des Teilnehmer-Assistenten aktiviert sind
* Sicherstellen, dass relevante Inhalte in diesen Katalogen vorhanden sind
* Warten Sie einige Stunden nach dem Hinzufügen neuer Inhalte, damit sie indiziert werden können

### Szenario 2: Irrelevante oder schlechte Antworten

**Problem**: Der KI-Assistent liefert Antworten, die nicht mit der Frage übereinstimmen oder von schlechter Qualität sind.

**Mögliche Ursachen**

* Die Frage ist zu weit gefasst oder mehrdeutig
* Relevante Inhalte haben schlechte Metadaten (Beschreibungen, Tags)
* Die Inhaltsstruktur erschwert die Extraktion von Informationen

**Lösung**

* Ermutigen Sie Teilnehmer, spezifischere Fragen zu stellen
* Überprüfen und verbessern Sie Kursbeschreibungen und Metadaten
* Sicherstellen, dass Inhalte klare Überschriften und Strukturen aufweisen
* Detaillierten Nutzungsbericht lesen, um Muster zu identifizieren
* Erwägen Sie die Erstellung von Arbeitshilfen für häufig gestellte Fragen.

### Szenario 3: Fragen außerhalb des Anwendungsbereichs

**Problem**: Der Teilnehmer stellt Fragen, die nichts mit Schulungsinhalten zu tun haben.

**Beispiele**:

* Allgemeine Wissensfragen (&#39;Wer ist der Präsident?&#39;)
* Persönliche Meinungen (&#39;Was halten Sie von X?&#39;)
* Unangemessene Inhalte

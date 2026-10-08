---
description: Erfahren Sie, wie Sie realistische, messbare Rollenspiele für Virtual Coach entwerfen, die Personas, Szenarien, Bewertungskriterien und eine Szenarienbibliothek abdecken.
jcr-language: en_us
title: Entwerfen eines Rollenspiels
exl-id: a9eb5303-df1f-4f1d-9e21-0cf3eff5f199
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '4120'
ht-degree: 2%
---

*Ein Designleitfaden für das Erstellen von Virtual Coach-Rollenspielen in Adobe Learning Manager*

# Entwerfen eines Rollenspiels

## Einführung

Virtual Coach ist eine Adobe Learning Manager-Funktion, mit der Teilnehmer realistische Unterhaltungen am Arbeitsplatz mit KI-gestützten Personas üben und personalisiertes Coaching-Feedback erhalten können. Im Gegensatz zu herkömmlichen Bewertungen, die den Wissensrückruf messen, bewertet Virtual Coach, wie effektiv die Teilnehmer Wissen, Kommunikationstechniken, Problemlösungskompetenzen und Entscheidungsfindung in simulierten realen Situationen anwenden.

Die Qualität eines Rollenspiels beeinflusst direkt die Lernerfahrung des Teilnehmers. Ein gut gestaltetes Rollenspiel fühlt sich authentisch an, fordert die Lernenden heraus, kritisch zu denken, stellt realistische Hindernisse dar und misst aussagekräftige Verhaltensweisen. Schlecht gestaltete Rollenspiele wirken oft skriptorientiert, generisch und losgelöst von der Realität am Arbeitsplatz.

Dieses Handbuch bietet einen Rahmen für das Entwerfen wirkungsvoller Rollenspiele, Best Practices für das Authoring, eine Bibliothek mit anpassungsfähigen Beispielen und eine Zuordnung von jedem Entwurfskonzept zum tatsächlichen Feld, das Sie in Virtual Coach konfigurieren.

## Für wen ist dieser Leitfaden?

Dieses Handbuch wurde für Kursautoren und Entwickler von Lernprogrammen geschrieben, die vor dem Öffnen des Autorenbildschirms ein Rollenspiel für den virtuellen Coach planen. Es ist auch für L&amp;D-Stakeholder gedacht, die Rollenspielinhalte überprüfen oder genehmigen, da sich die Gold Standard-Vorlage und die Checkliste vor der Veröffentlichung als Review-Rubrik verdoppeln.

Dieser Leitfaden gilt für das Konversationsdesign: die Kriterien für Szenario, Person, Ziel und Bewertung, die bestimmen, ob ein Rollenspiel realistisch wirkt und die richtigen Dinge misst.

## Die Anatomie von Rollenspielen verstehen

Jedes erfolgreiche Rollenspiel baut auf vier grundlegenden Elementen auf:

1. Szenario
2. Persona
3. Gesprächsziel
4. Auswertungskriterien

Zusammen bestimmen diese Elemente die Qualität des Lernerlebnisses und den Wert des Coaching-Feedbacks.

### Szenario: Warum findet diese Unterhaltung statt?

Das Szenario legt den Geschäftskontext fest. Er erklärt:

* Warum die Teilnehmer sich treffen
* Welches Geschäftsereignis hat die Diskussion ausgelöst?
* Was geschah vor dem Gespräch?
* Worum geht es?
* Warum die Diskussion wichtig ist

Ohne ein überzeugendes Szenario führt die KI zu einem Gespräch, aber möglicherweise mangelt es ihr an Tiefe, Realismus und Dringlichkeit.

**Zu stellende Fragen**

Beantworten Sie vor dem Schreiben des Szenarios Folgendes:

* Warum reden diese Leute?
* Was ist passiert, das diese Unterhaltung ausgelöst hat?
* Ist dies die erste Interaktion oder ein Follow-up?
* Über welches Geschäftsproblem wird diskutiert?
* Was passiert, wenn die Unterhaltung nicht erfolgreich ist?

**Beispiel**

**Schwaches Szenario.** Der Kunde möchte mehr über Adobe Learning Manager erfahren.

**Starkes Szenario.** Ein Director of Learning hat einem Discovery-Call zugestimmt, nachdem er an einem Webinar zur Weiterbildung von Mitarbeitern teilgenommen hat. Der aktuelle LMS-Vertrag des Unternehmens läuft in neun Monaten ab, und die Leitung hat das L&amp;D-Team angewiesen, alternative Lösungen zu evaluieren, bevor ein Budgetantrag gestellt wird.

Das zweite Beispiel bietet Kontext, Dringlichkeit, Relevanz für die Entscheidungsfindung und realistische geschäftliche Faktoren.

**Best Practices**

Definieren Sie die Beziehungsphase. Geben Sie an, wo sich die Teilnehmer auf der Reise befinden, z. B.: Erster Ermittlungsaufruf, Besprechung zur Produktbewertung, Geschäftsbesprechung mit Führungskräften, Verlängerungsverhandlung, Eskalationsdiskussion, Trainingssitzung für Führungskräfte oder Besprechung zu Leistungsfeedback.

Einschließen eines auslösenden Ereignisses, z. B.: Initiative zum Austausch von LMS, fehlgeschlagene Prüfungen, rückläufige Akzeptanz, Produktausfall, organisatorische Umstrukturierung, versäumte Umsatzziele oder Einführung strategischer KI.

Folgen einführen. Gute Rollenspiele beinhalten Risiken, z. B.: Budgetverlust, Compliance-Fehler, Kundenfluktuation, Mitarbeiterabwanderung, verzögerte Implementierung oder Überprüfung durch Führungskräfte.

### Die Persona: Mit wem spricht der Lernende?

Personen fördern den Realismus. Eine Person sollte sich wie ein echter Stakeholder fühlen, nicht wie ein fiktionaler Charakter. Effektive Personas umfassen: Rolle, Zuständigkeiten, Ziele, Prioritäten, Anliegen, Zwänge, Kommunikationsstil und Persönlichkeit.

**Zu stellende Fragen**

* Für welche Ergebnisse sind sie verantwortlich?
* Welche Bedenken beeinflussen ihre Entscheidungen?
* Wie kommunizieren sie in der Regel?
* Welche Einwände werden sie voraussichtlich erheben?

**Beispiel**

**Schwäche Persönlichkeit.** Learning Manager ist an LMS-Plattformen interessiert.

**Starke Persönlichkeit:**

* Rolle: Vice President, Learning and Talent Development
* Persönlichkeit: Analytisch und skeptisch
* Aktuelle Zuständigkeiten: überwacht Lernprogramme für 20 000 Mitarbeiter; meldet der Führungsebene Lernaktivitätsmetriken; Verwaltung von LMS-Modernisierungsinitiativen
* Derzeitiger Druck: Haushaltskürzungen; Prüfung der Einhaltung der Vorschriften in sechs Monaten; Forderung von Führungskräften nach besserer Berichterstattung
* Wichtigste Anliegen: Komplexität der Migration; Übernahme durch die Nutzer; Kostenbegründung; Exekutivsponsoring

**Best Practices**

Geben Sie Persönlichkeiten Bedenken. Die meisten Personen sollten drei bis fünf Anliegen haben. Diese Bedenken werden zur natürlichen Quelle von Einwänden und herausfordernden Gesprächen.

Füge emotionalen Kontext hinzu. Menschen treten selten emotional neutral in Gespräche ein, zum Beispiel: frustriert, skeptisch, gestresst, defensiv, neugierig oder optimistisch.

Definieren des Kommunikationsstils (zum Beispiel: direkt, analytisch, beziehungsorientiert, reserviert, durchsetzungsstark oder herausfordernd.

### Das Gesprächsziel: Was sollte der Teilnehmer erreichen?

Das Ziel definiert Erfolg. Einer der häufigsten Fehler ist, sich auf Themen statt auf Ergebnisse zu konzentrieren.

**Schlechtes Ziel.** Onboarding - Diskussion

**Besseres Ziel.** Ermittelt die Onboarding-Herausforderungen, und holt die Zustimmung der Führungskräfte zur Einführung eines Pilotprogramms ein.

**Best Practices**

Konzentrieren Sie sich auf die Ergebnisse, z. B. Sichern Sie ein Follow-up-Meeting, beheben Sie eine Beschwerde, erhalten Sie Unterstützung durch die Interessengruppen, erhalten Sie eine Genehmigung durch die Führungskräfte, erstellen Sie einen Plan zur Leistungsverbesserung oder erzielen Sie eine Vereinbarung für ein Pilotprojekt.

Messbare Erfolge definieren. Am Ende der Unterhaltung sollte klar sein, ob der Teilnehmer erfolgreich war.

### Bewertungskriterien: Wie wird der Erfolg gemessen?

Bewertungskriterien definieren, was die KI bewerten soll. Die wirksamsten Kriterien konzentrieren sich auf beobachtbare Verhaltensweisen.

**Gute Bewertungskriterien**

* Offene Fragen
* Bestätigtes Verständnis
* Zusammenfassende Bedenken
* Geschäftliche Vorteile.
* Erwiderte Einwände
* Etablierung der nächsten Schritte

**Schlechte Bewertungskriterien**

* Klang zuversichtlich
* Erschien professionell
* War überzeugend
* Führungspräsenz gezeigt

Diese sind subjektiv und schwer konsistent zu bewerten.

**Best Practices**

Wertet Verhaltensmuster aus, nicht Persönlichkeitsmerkmale. Fragen: &quot;Welche spezifischen Aktionen sollten im Konversationstranskript angezeigt werden?&quot; Wenn das Verhalten gehört oder beobachtet werden kann, ist es wahrscheinlich ein gutes Bewertungskriterium.

Bewertungskategorien beschränken. Die meisten Rollenspiele schneiden mit drei bis sechs Bewertungsbereichen, klaren Beschreibungen und messbaren Verhaltensweisen am besten ab.

## Realistische Dialoge gestalten.

### Spannung erzeugen.

Zu den besten Rollenspielen gehören Hindernisse.

| **Funktion** | **Beispielspannung** |
|---|---|
| Verkauf | Der Kunde hinterfragt den ROI. |
| Kundenreferenzen. | Der Kunde ist der Ansicht, dass Adoption keine Priorität mehr ist. |
| Führung | Der Mitarbeiter ist mit dem Feedback nicht einverstanden. |
| Änderungsmanagement | Die Stakeholder befürchten, die Kontrolle über die Entscheidungsfindung zu verlieren. |

Ohne Spannungen werden Gespräche oft zu einfach und unrealistisch.

### Konkurrierende Prioritäten setzen.

Echte Interessengruppen konzentrieren sich selten auf ein einziges Thema. Ein VP of Learning kann sich gleichzeitig um Kosten, Compliance, Anwenderakzeptanz, Implementierungszeitpläne und Berichte für Führungskräfte kümmern. Konkurrierende Prioritäten führen zu umfassenderen Gesprächen und besseren Coaching-Möglichkeiten.

### Dialogfeld &quot;Erstellen&quot;, keine Interviews

Der virtuelle Coach sollte eine echte Konversation anstatt einer Checkliste mit Fragen simulieren. Die Teilnehmer sollten ermutigt werden, Probleme zu erforschen, zu klären, zu trainieren, zu verhandeln, zu beeinflussen und zu lösen.

## Reifegradmodell

Rollenspiele entwickeln sich im Allgemeinen über fünf Reifegrade hinweg, von einem generischen Einzelfragenaustausch bis hin zu einer vollständig adaptiven Simulation mit mehreren Stakeholdern. Verwenden Sie dieses Modell, um zu planen, wie sich ein Rollenspiel entwickeln soll, wenn die Teilnehmer vom Onboarding zum Meistersein übergehen, anstatt zu versuchen, die Komplexität der Stufe 5 beim ersten Versuch zu verfassen.

### Ebene 1: Grundlegende Rollenspiele {#level-1-basic-role-play}

**Szenario.** Discovery Call bei einem potenziellen Kunden.

**Persona.** Interessent.

**Ziel.** Voraussetzungen verstehen.

**Auswertungskriterien**

* Fragen stellen
* Bedürfnisse verstehen
* Lösung empfehlen

*Diese Ebene aktiviert die KI-Interaktion, fühlt sich jedoch häufig als generisch an.*

### Ebene 2: Kontextabhängiges Rollenspiel {#level-2-context-driven-role-play}

**Szenario.** Ein Interessent hat an einem Webinar teilgenommen und einen Discovery Call angefordert.

**Persona.** Learning Manager bei der Bewertung von Schulungslösungen.

**Ziel.** Herausforderungen bei Schulungen.

**Auswertungskriterien**

* Erkennung
* Problemidentifizierung
* Zusammenfassung
* Nächste Stufe: Ausrichtung

### Ebene 3: Auf Unternehmen fokussiertes Rollenspiel {#level-3-business-focused-role-play}

**Szenario.** Ein Unternehmen plant, sein LMS aufgrund eines bevorstehenden Vertragsablaufs zu ersetzen.

**Persona.** Director of Learning überwacht die Modernisierung der Plattform.

**Ziel.** Versteht die geschäftlichen Anforderungen und sichert euch eine Demonstration.

**Auswertungskriterien**

* Ermittlungseffektivität
* Stakeholder-Zuordnung
* Schmerzpunkterkennung
* Umgang mit Einwänden

### Ebene 4: Rollenspiel mit mehreren Stakeholdern {#level-4-multi-stakeholder-role-play}

**Szenario.** Eine Initiative zur digitalen Transformation des Lernens erfordert die Zustimmung des Finanzwesens, der IT und des Unternehmens-Sponsors, bevor sie fortgesetzt werden kann. Jeder Stakeholder hat dabei eine andere Priorität.

**Persona.** Drei Personen in einer Session, jede mit einer bestimmten Rolle, Persönlichkeit und einem bestimmten Anliegen (z. B. ein CFO mit Fokus auf Kosten, eine IT-Director mit Fokus auf Sicherheit und ein Business Sponsor mit Fokus auf Zeitplan) - konfiguriert als persönliches Rollenspiel mit bis zu vier Personen.

**Ziel.** Passen Sie die Botschaft für jeden Stakeholder im selben Gespräch an und sorgen Sie dafür, dass alle Stakeholder die gleiche Meinung haben, nicht nur der stimmhafteste.

**Auswertungskriterien**

* Anpassung von Nachrichten an alle Beteiligten
* Individuelle Behandlung von Einwänden pro Person
* Synthese und Abstimmung zwischen konkurrierenden Prioritäten
* Engagement für den nächsten Schritt bei jedem Beteiligten

*Diese Stufe führt die Komplexität des Beispiels für Führungskräfte weiter unten in diesem Leitfaden ein. Die meisten Teilnehmer sollten Stufe 3 beherrschen, bevor sie Stufe 4 ausprobieren.*

### Ebene 5: Anpassungsfähiges Rollenspiel mit hohem Einsatz {#level-5-adaptive-high-stakes-role-play}

**Szenario.** Eine strategische Initiative liegt bereits hinter dem Zeitplan zurück und hat das Budget überschritten, und die Geduld und Skepsis der Person nehmen sichtbar zu, wenn der Teilnehmer seine größte Sorge nicht früh im Gespräch anspricht.

**Persona.** Ein leitender Stakeholder, dessen Ton und Widerstandsniveau die Mitte der Konversation basierend auf der Leistung des Teilnehmers verschieben - um zum Beispiel kooperativer zu werden, sobald ein bestimmtes Problem gelöst ist, oder skeptischer, wenn Einwände umgelenkt anstatt angegangen werden.

**Ziel.** Wiederherstellung des Vertrauens der Stakeholder und Sicherstellung des Engagements trotz einer anfänglich gegensätzlichen Ausgangsposition.

**Auswertungskriterien**

* Adaptive Behandlung von Einwänden
* Deeskalation unter Druck
* Erholung von einer schlechten Eröffnung
* Verhandlung und Abschluss auf Führungsebene

*Dies ist die Ebene mit der höchsten Komplexität: die KI basiert auf einer Person, die mit einem starken Bedenken-Timing konfiguriert ist (&quot;wenn es dazu kommt&quot;). Daher ändert sich der Ton der KI wirklich basierend auf dem, was der Teilnehmer sagt, anstatt einem festen Skript zu folgen. Reservieren Sie diese Stufe für Grundsteinbewertungen, nicht für frühes Üben.*

## Enterprise-Szenarienbibliothek

Das nachfolgende Beispiel für die Aktivierung des Vertriebs ist die voll funktionsfähige Referenz für diese Bibliothek. Jedes Feld, das die Gold Standard-Vorlage aufruft, wird ausgefüllt, einschließlich gewichteter Bewertungskriterien, Make-or-Break-Markierungen, Öffnungszeilen und Einwänden. Die übrigen Beispiele folgen der gleichen Struktur, sodass sie gleichermaßen anpassungsbereit sind. keine absichtlich abgekürzt werden.

### Verkaufsunterstützung: Evaluierung des Enterprise-LMS

**Szenario.** Eine globale Fertigungsorganisation mit mehr als 40.000 Mitarbeitern bewertet LMS-Anbieter, da ihr aktueller Plattformvertrag innerhalb von neun Monaten ausläuft. Der Teilnehmer ist ein Account Executive, der das erste formelle Discovery-Gespräch führt, nachdem er den Interessenten auf einer Branchenkonferenz getroffen hat. Die Organisation ist in 25 Ländern tätig und verwendet derzeit fünf voneinander getrennte Lernsysteme.

**Persona**

| **Feld** | **Details** |
|---|---|
| Name | Sarah Thompson |
| Rolle | Vice President, Learning and Talent Development |
| Systemeigenschaft | skeptisch |
| Kommunikationsstil (Hintergrundnuance) | analytisch und direkt; verlangt Beweise, bevor sie einer Forderung vertrauen. |
| Prioritäten | Konsolidierung von Lernsystemen Verbesserung der Compliance-Berichterstattung; Verringerung des Verwaltungsaufwands; Akzeptanz der Teilnehmer steigern |
| Druck | die Einhaltung der Vorschriften wird in sechs Monaten überprüft; Initiative zur Modernisierung der Geschäftsführung; Budget für vorherige Migration überschritten |

**Persönliche Bedenken**

* Komplexität der Migration - wird angezeigt, wenn der Teilnehmer Implementierungszeitpläne beschreibt. Gut genug: Der Teilnehmer skizziert einen stufenweisen Migrationsansatz mit benannten Meilensteinen.
* Akzeptanz durch Benutzer - wird angezeigt, wenn der Teilnehmer über das Rollout diskutiert. Gut genug: der Teilnehmer verweist auf einen Änderungsmanagement- oder Schulungsplan für Endbenutzer.
* Executive-Sponsoring - kommt kurz vor dem Ende des Gesprächs. Gut genug: der Teilnehmer identifiziert, wer sonst noch an der Entscheidung beteiligt sein muss.
* Verborgene Implementierungskosten - tauchen bei der Preisgestaltung auf. Gut genug: der Teilnehmer reagiert proaktiv auf die Gesamtbetriebskosten und nicht nur auf den Lizenzpreis.

**Ziel.** Der Teilnehmer muss geschäftliche Herausforderungen erkennen, Bewertungskriterien verstehen, Stakeholder identifizieren, den Zeitplan und die Dringlichkeit analysieren und eine sichere Vereinbarung für eine Demonstration treffen.

**AI Trainer Opener.** *Sie stehen kurz vor einem Discovery Call bei einem VP of Learning, der LMS-Anbieter vor einer Vertragsverlängerung evaluiert. Ihr Ziel ist es, eine Nachfolgedemo zu sichern.*

**AI Persona Opener.** *Vielen Dank, dass Sie nach der Konferenz weiterverfolgt haben. Ich habe ungefähr zwanzig Minuten - ich bin ehrlich, wir haben bereits viele Versprechungen von Anbietern gehört, also lassen Sie uns auf die Einzelheiten eingehen.*

**Bewertungskriterien (abzudeckende Themen)**

| **Thema** | **Gewicht** | **Erstellen oder Unterbrechen** |
|---|---|---|
| Ermittlungsfragen | 25% | Nein |
| Untersuchung der geschäftlichen Auswirkungen | 20% | Nein |
| Identifizierung der Beteiligten | 20% | Nein |
| Erfolgsmetrik-Identifizierung | 15% | Nein |
| Nächste Stufe: Ausrichtung | 20% | Ja |

**Typische Einwände**

* &quot;Wir haben von jedem LMS-Anbieter ähnliche Versprechungen gehört.&quot;
* &quot;Unsere größte Sorge ist das Migrationsrisiko.&quot;
* &quot;Wir sind nicht davon überzeugt, dass eine andere Plattform die Akzeptanz verbessern wird.&quot;

**Erfolgsstatus.** Der Teilnehmer stellt eine Nachdemonstration sicher und versteht den Kaufprozess des Unternehmens.

### Kundenreferenzen: Executive Review zur Wiederaufnahme der Zulassung

**Szenario.** Die Plattformnutzung ist in den beiden vorangegangenen Quartalen um 40 % zurückgegangen. Executive-Sponsoren stellen den ROI in Frage und die Verlängerungsgespräche beginnen in vier Monaten. Teilnehmer ist ein Customer Success Manager, der eine vierteljährliche Geschäftsüberprüfung durchführt.

**Persona**

| **Feld** | **Details** |
|---|---|
| Name | Michael Adams |
| Rolle | Director of HR Technology. |
| Systemeigenschaft | Beziehungsorientiert |
| Kommunikationsstil (Hintergrundnuance) | Zusammenarbeit, aber frustriert; möchte gemeinsam an einer Korrektur arbeiten, hat aber nicht mehr die Geduld mit dem aktuellen Verlauf. |
| Prioritäten | Verbesserung der Mitarbeiterbindung; Erhöhung der Beteiligung der Manager; Geschäftlichen Nutzen nachweisen |
| Druck | Haushaltskürzungen; Neue CHRO-Erwartungen; Verstärkte Überprüfung der Verlängerung |

**Persönliche Bedenken**

* Eine geringe Akzeptanz wird zu Beginn der Überprüfung angezeigt. Gut genug: der Teilnehmer erkennt den Rückgang direkt an, anstatt mit positiven Metriken zu führen.
* Mangelnde Transparenz für Führungskräfte - wird immer wieder angezeigt, wenn über Berichte gesprochen wird. Gut genug: der Teilnehmer schlägt ein spezielles Dashboard oder einen spezifischen Bericht für die Führungsebene vor.
* Unzureichende Berichterstellung - kommt mit Sichtbarkeit. Gut genug: Der Teilnehmer verpflichtet sich zu einer konkreten Meldeschwankung.
* Konkurrierende Prioritäten - wird vorgeschlagen, wenn die nächsten Schritte vorgeschlagen werden. Gut genug: Der Teilnehmer schlägt einen ersten Schritt mit geringem Aufwand anstelle eines großen Programms vor.

**Ziel.** Diagnose von Adoptionsherausforderungen und Festlegung einer Recovery-Strategie mit klaren Zuständigkeiten und Zeitvorgaben.

**AI Trainer Opener.** *Sie sind im Begriff, eine vierteljährliche Geschäftsüberprüfung mit einem Kunden zu leiten, dessen Plattformnutzung stark zurückgegangen ist. Ihr Ziel ist es, mit einem vereinbarten Wiederherstellungsplan abzuschließen.*

**AI Persona Opener.** *Ich bin direkt - die Nutzung ist um 40 % gesunken, und mein CHRO fragt mich, warum wir für eine Plattform bezahlen, die niemand nutzt. Ich brauche heute mehr als nur Beruhigung.*

**Bewertungskriterien (abzudeckende Themen)**

| **Thema** | **Gewicht** | **Erstellen oder Unterbrechen** |
|---|---|---|
| Effektivität der geschäftlichen Überprüfung | 20% | Nein |
| Ursachenanalyse | 25% | Nein |
| Bewertung des Änderungsmanagements | 20% | Nein |
| Erfolgsplanung | 20% | Nein |
| Ausrichtung der Exekutive | 15% | Ja |

**Typische Einwände**

* &quot;Warum sollte ich glauben, dass dieses Quartal anders sein wird?&quot;
* &quot;Mein Team hat keine Zeit für eine weitere Initiative.&quot;
* &quot;Ich brauche etwas, was ich meinem CHRO zeigen kann, nicht nur einen Plan.&quot;

**Erfolgsstatus.** Beide Parteien einigen sich auf Maßnahmen, Rechenschaftspflicht, Zeitpläne und messbare Ergebnisse.

### Führungskräfteentwicklung: Management der unzureichenden Performance

**Szenario.** Ein Manager muss die abnehmende Leistung eines leitenden Mitarbeiters ansprechen, der kürzlich Fristen versäumt, Kundenbeschwerden erhalten und mit der Zusammenarbeit im Team zu kämpfen hatte. Der Mitarbeiter war zuvor ein Vorreiter.

**Persona**

| **Feld** | **Details** |
|---|---|
| Name | David Lewis |
| Rolle | Senior Project Manager |
| Systemeigenschaft | selbstüberzeugt |
| Kommunikationsstil (Hintergrundnuance) | zuversichtlich und defensiv; zurück, anstatt sofort Feedback zu akzeptieren. |
| Prioritäten | Protect seinen beruflichen Ruf; Das Vertrauen seines Managers wiedergewinnen. |
| Druck | Erhöhung der Arbeitsbelastung; persönlicher Stress Bedenken hinsichtlich der Laufbahnentwicklung |

**Persönliche Bedenken**

* Unklare Erwartungen - kommen früh. Gut genug: Der Manager gibt Böden Feedback zu bestimmten, vorher kommunizierten Erwartungen.
* Unangemessene Arbeitsbelastung - entsteht mitten in der Konversation. Gut genug: Der Manager erkennt die Arbeitslast als einen Faktor an, ohne die versäumten Fristen zu entschuldigen.
* Feedback-Fairness - kommt zur Sprache, wenn Performance-Beispiele angesprochen werden. Gut genug: der Manager nennt konkrete, faktische Beispiele und keine allgemeinen Eindrücke.

**Ziel.** Vermitteln Sie Vereinbarungen und Vereinbarungen im Zusammenhang mit einem Plan zur Leistungsverbesserung.

**AI Trainer Opener.** *Sie sind im Begriff, eine Feedback-Unterhaltung mit einem zuvor starken Darsteller zu führen, dessen aktuelle Arbeit verrutscht ist. Ihr Ziel ist die Vereinbarung eines bestimmten Verbesserungsplans.*

**AI Persona Opener.** *Ich weiß, warum wir reden, und ehrlich gesagt, ich denke nicht, dass es fair ist. Die Arbeitslast aller Mitarbeiter ist gestiegen, nicht nur meine.*

**Bewertungskriterien (abzudeckende Themen)**

| **Thema** | **Gewicht** | **Erstellen oder Unterbrechen** |
|---|---|---|
| Faktenbasiertes Feedback | 25% | Nein |
| Aktives Zuhören | 20% | Nein |
| Empathie | 15% | Nein |
| Rechenschaftspflicht | 20% | Nein |
| Erstellung eines Aktionsplans | 20% | Ja |

**Typische Einwände**

* &quot;Kein anderer hätte mit dieser Arbeitslast umgehen können.&quot;
* &quot;Ich wusste nicht, dass sich die Erwartungen geändert hatten.&quot;
* &quot;Bei anderen fehlen auch die Fristen.&quot;

**Erfolgsstatus.** Der Mitarbeiter stimmt den messbaren Leistungserwartungen und Folgemaßnahmen zu.

### Änderungsmanagement: Transformation von Unternehmensprozessen

**Szenario.** Das Unternehmen entwickelt eine neue Beschaffungsplattform, die Genehmigungsprozesse und -aufgaben ändert. Mehrere Geschäftseinheiten haben sich bereits dagegen ausgesprochen. Der Teilnehmer ist ein Change Manager-Meeting mit einem wichtigen Stakeholder.

**Persona**

| **Feld** | **Details** |
|---|---|
| Name | Jennifer Kim |
| Rolle | Regionale Maßnahmen Director |
| Systemeigenschaft | skeptisch |
| Kommunikationsstil (Hintergrundnuance) | direkt und skeptisch; geht davon aus, dass das Rollout mehr Arbeit schafft, als es spart, bis das Gegenteil bewiesen ist. |
| Prioritäten | Aufrechterhaltung der Produktivität; Erfüllung vierteljährlicher Ziele Unterbrechungen minimieren |
| Druck | Ressourcenmangel; Umstrukturierung von Unternehmen; Prüfung durch die Exekutive |

**Persönliche Bedenken**

* Zusätzliche Arbeitslast, die sofort entsteht. Gut genug: der Teilnehmer anerkennt, dass die kurzfristige Arbeitslast ehrlich zunimmt, anstatt sie zu minimieren.
* Die Auswirkungen auf die Produktivität werden bei der Diskussion von Zeitplänen angezeigt. Gut genug: Der Teilnehmer bietet eine realistische Übergangszeitleiste, keine optimistische.
* Widerstand der Mitarbeiter - Gesprächsthema ist die Mitte. Gut genug: die Teilnehmer schlägt einen spezifischen Kommunikations- oder Schulungsplan für ihr Team vor.
* Der Verlust der Autonomie kommt fast zum Schluss. Gut genug: die Teilnehmerin klärt, welche Entscheidungsbefugnis ihr Team im Rahmen des neuen Prozesses behält.

**Ziel.** Sorgt für Vertrauen in den Rollout und sichert euch die Unterstützung der Beteiligten.

**AI Trainer Opener.** *Sie sind im Begriff, sich mit einem Regionaldirektor zu treffen, dessen Team von einem neuen Beschaffungsprozess erheblich betroffen sein wird. Ihr Ziel ist es, ihre Unterstützung für den Rollout zu sichern.*

**AI Persona Opener.** *Bevor Sie loslegen - ich weiß bereits, dass dies mein Team verlangsamen wird. Überzeugen Sie mich, dass ich mich irre.*

**Bewertungskriterien (abzudeckende Themen)**

| **Thema** | **Gewicht** | **Erstellen oder Unterbrechen** |
|---|---|---|
| Empathie | 20% | Nein |
| Kommunikation mit Geschäftsideen | 20% | Nein |
| Umgang mit Einwänden | 25% | Nein |
| Bewertung der Änderungsbereitschaft | 15% | Nein |
| Aufbau von Verpflichtungen | 20% | Ja |

**Typische Einwände**

* &quot;Dadurch wird mein Team langsamer, wir werden nicht schneller.&quot;
* &quot;Wir wurden nicht konsultiert, bevor das entschieden wurde.&quot;
* &quot;Mein Team hat in diesem Quartal bereits zu viel auf dem Teller.&quot;

**Erfolgsstatus.** Die Interessenträger verpflichten sich, die Umsetzungsmaßnahmen zu unterstützen.

### Technischer Support: Kritischer Compliance-Ausfall

**Szenario.** Eine Gesundheitsorganisation kann drei Wochen vor einer externen Prüfung nicht auf eine obligatorische Compliance-Schulung zugreifen. Mehr als 8.000 Beschäftigte sind betroffen. Der Teilnehmer ist ein Supportingenieur, der eine kritische Eskalation verarbeitet.

**Persona**

| **Feld** | **Details** |
|---|---|
| Name | Rebecca Sutton |
| Rolle | Lernobjektadministrator |
| Systemeigenschaft | selbstüberzeugt |
| Kommunikationsstil (Hintergrundnuance) | betonte und dringende Notwendigkeit; will einen Zeitplan und einen Plan, nicht nur Beruhigung. |
| Prioritäten | Wiederherstellung des Zugriffs vor Ablauf der Prüfungsfrist; Protect des Unternehmens vor regulatorischen Risiken |
| Druck | Prüftermin; Eskalation der Geschäftsführung; Regulierungsrisiko |

**Persönliche Bedenken**

* Audit-Fehler - wird sofort angezeigt. Gut genug: Der Teilnehmer gibt eine konkrete geschätzte Lösungszeit an, keine vage Rückversicherung.
* Unterbrechungen für Mitarbeiter - wird bei der Abstimmung des Umfangs angezeigt. Gut genug: Der Teilnehmer erkennt die Größe an (8.000 Mitarbeiter) und schlägt eine Zwischenlösung vor, falls vorhanden.
* Transparenz für Führungskräfte - am Ende. Gut genug: Die Teilnehmerin sagt ihrem Führungsteam eine bestimmte Aktualisierungskadenz zu.

**Ziel.** Diagnostizieren Sie das Problem und stellen Sie das Vertrauen in den Lösungsprozess her.

**AI Trainer Opener.** *Sie sind im Begriff, eine kritische Eskalation von einem Kunden zu verarbeiten, der vor einer externen Prüfung nicht auf obligatorische Compliance-Schulungen zugreifen kann. Ihr Ziel ist es, einen glaubwürdigen Lösungsplan zu erstellen.*

**AI Persona Opener.** *Ich muss dies heute beheben, nicht irgendwann. Wir haben eine Prüfung in drei Wochen und achttausend Menschen ausgesperrt. Was ist der Plan?*

**Bewertungskriterien (abzudeckende Themen)**

| **Thema** | **Gewicht** | **Erstellen oder Unterbrechen** |
|---|---|---|
| Empathie | 15% | Nein |
| Fehlerbehebung | 25% | Nein |
| Klare Kommunikation | 20% | Nein |
| Erwartungsmanagement | 20% | Nein |
| Lösungsplanung | 20% | Ja |

**Typische Einwände**

* &quot;Du scheinst nicht zu verstehen, wie ernst das ist.&quot;
* &quot;Gestern wurde mir gesagt, dass das schon repariert werden würde.&quot;
* &quot;Ich muss meiner Führung jetzt etwas Konkretes mitteilen.&quot;

**Erfolgsstatus.** Der Kunde versteht den Aktionsplan und fühlt sich unterstützt.

### Einführung von KI: Rollout-Strategie für KI von Führungskräften

**Szenario.** Die Organisation prüft derzeit einen KI-Assistenten für Unternehmen, der in mehreren Abteilungen eingesetzt werden kann. Führungskräfte unterstützen die Untersuchung der Opportunity, sind aber nach wie vor besorgt über Governance, Sicherheit, Compliance und Adoption. Teilnehmer ist ein AI-Programm-Manager, der den Vorschlag einem Vizepräsidenten der Abteilung vorlegt.

**Persona**

| **Feld** | **Details** |
|---|---|
| Name | Robert Chen |
| Rolle | Vice President of Operations |
| Systemeigenschaft | Neutral |
| Kommunikationsstil (Hintergrundnuance) | Strategisch und risikoorientiert; Er wägt den Vorschlag nach seinen Vorzügen ab, anstatt emotional zu reagieren, aber er wird nicht vorankommen, ohne jedes größere Risiko einzugehen. |
| Prioritäten | Steigerung der Produktivität; Senkung der Betriebskosten; Protect-Kundendaten Compliance gewährleisten |
| Druck | Wettbewerbsdruck; Sichtbarkeit von KI auf Board-Ebene Bestehende Technologieschulden |

**Persönliche Bedenken**

* Halluzinationen - kommt auf, wenn Genauigkeit diskutiert wird. Gut genug: Der Teilnehmer beschreibt eine spezifische Sicherheitsmaßnahme, wie z. B. die Überprüfung risikoreicher Produkte durch den Menschen.
* Sicherheitsrisiken werden bei der Behandlung von Daten berücksichtigt. Gut genug: Der Teilnehmer verweist auf Data-Governance-Kontrollen, nicht nur &quot;es ist sicher&quot;.
* Missbrauch durch Mitarbeiter - leicht verständlich. Gut genug: Der Teilnehmer beschreibt eine Richtlinie oder einen Schulungsplan für eine zulässige Verwendung.
* Die ROI-Unsicherheit kommt dem Ende nahe. Gut genug: der Teilnehmer schlägt ein messbares Pilotprojekt mit definierten Erfolgsmetriken vor.

**Ziel.** Probleme lösen, Mehrwert demonstrieren und Sponsoring für ein Pilotprogramm erhalten.

**AI Trainer Opener.** *Sie sind im Begriff, einem VP of Operations einen Rollout für Unternehmens-KI vorzulegen, der die Erkundung von KI unterstützt, aber echte Governance-Bedenken hat. Ihr Ziel ist es, das Sponsoring für einen Piloten zu sichern.*

**AI Persona Opener.** *Ich bin prinzipiell nicht dagegen, aber ich habe genug AI-Schlagzeilen gesehen, um die Risiken zu kennen. Führt mich durch die Details, wie wir es vermeiden können, einer von ihnen zu werden.*

**Bewertungskriterien (abzudeckende Themen)**

| **Thema** | **Gewicht** | **Erstellen oder Unterbrechen** |
|---|---|---|
| Abstimmung des Unternehmenswerts | 20% | Nein |
| Governance-Kommunikation | 25% | Ja |
| Risikomanagement | 20% | Nein |
| Umgang mit Einwänden | 15% | Nein |
| Einfluss der Geschäftsleitung | 20% | Nein |

**Typische Einwände**

* &quot;Woher wissen wir, dass sich mit einer Lösung nicht alles vor einem Kunden erfindet?&quot;
* &quot;Was passiert mit unseren Daten, wenn sie im Modell sind?&quot;
* &quot;Wir wurden schon früher von unerprobter Technologie verbrannt.&quot;

**Erfolgsstatus.** Die Stakeholder verpflichten sich, ein Pilotprojekt zu finanzieren und Erfolgsmetriken festzulegen.

### Führungskräfte (mehrere Personen): Überprüfung durch den Lenkungsausschuss

**Szenario.** Eine strategische Initiative zur digitalen Transformation ist nicht mehr zeitgemäß und hat auch das Budget überschritten. Der Teilnehmer ist der Programmmanager, der einem vierköpfigen Lenkungsausschuss einen Sanierungsplan vorlegt, von dem jeder den Plan mit einer anderen Priorität bewertet.

**Personas (bis zu vier, einzeln konfiguriert)**

| **Persona** | **Rolle** | **Systemeigenschaft** | **Fokus/Priorität** |
|---|---|---|---|
| CFO | Finanzvorstand | skeptisch | Investitionsrenditen und Haushaltsrisiken. Fordert Rechtfertigung für weitere Ausgaben. |
| CIO | Chief Information Officer | selbstüberzeugt | Risiken bei Architektur, Sicherheit und Implementierung. Stellt technische Annahmen direkt in Frage. |
| Unternehmenssponsor | VP, die Initiative unterstützender Geschäftsbereich | Beziehungsorientiert | Geschäftsergebnisse und Zeitpläne. Kümmert sich um die Beziehung zum Programm-Team so viel wie die Zahlen. |
| Lead im Einkauf | Director der Kreditorenverwaltung | Neutral | Lieferantenleistung und vertragliche Verpflichtungen. Bewertet den Plan anhand der dokumentierten Vorteile. |

**Persönliche Bedenken (ein repräsentatives Anliegen pro Person)**

* CFO — Anhaltende Budgetbegründung. Kommt zuerst. Gut genug: der Teilnehmer bindet den Wiederherstellungsplan an eine bestimmte, quantifizierte Rendite.
* CIO — Technische Machbarkeit des überarbeiteten Zeitplans. Wird angezeigt, wenn der Plan vorgelegt wird. Gut genug: der Teilnehmer benennt die spezifischen technischen Risiken, die eingestellt werden, nicht nur den Zeitplan.
* Business Sponsor - Ob die ursprünglich versprochenen Geschäftsergebnisse noch erreichbar sind. Mitten im Gespräch. Gut genug: der Teilnehmer die ursprünglichen Ergebnisverpflichtungen erneut bestätigt oder explizit überarbeitet.
* Procurement Lead - Verantwortlichkeit des Anbieters für die Verzögerung. Kommt gegen Ende. Gut genug: Der Teilnehmer stellt klar, welche Vertrags- oder Leistungsänderungen in Zukunft auf den Anbieter angewendet werden.

**Ziel.** Sichere Genehmigung einer überarbeiteten Implementierungsstrategie durch alle vier Beteiligten, nicht nur durch den lautstärksten.

**AI Trainer Opener.** *Sie sind im Begriff, einem vierköpfigen Lenkungsausschuss einen Sanierungsplan für eine Initiative vorzulegen, die hinter dem Zeitplan und über dem Budget liegt. Ihr Ziel ist die einstimmige Genehmigung des überarbeiteten Plans.*

**CFO-Öffner.** *Bevor wir in den Plan einsteigen — erinnern Sie den Raum daran, wie viel wir bisher ausgegeben haben und warum wir diese überarbeitete Zahl glauben sollten.*

**Bewertungskriterien (abzudeckende Themen)**

| **Thema** | **Gewicht** | **Erstellen oder Unterbrechen** |
|---|---|---|
| Kommunikation mit Führungskräften | 20% | Nein |
| Risikokommunikation | 20% | Nein |
| Behandlung von Stakeholder-spezifischen Einwänden | 25% | Nein |
| Entscheidungsfindung über konkurrierende Prioritäten hinweg | 20% | Nein |
| Einstimmige Verpflichtung für den nächsten Schritt | 15% | Ja |

**Typische Einwände**

* &quot;Wir haben das Budget bereits einmal überschritten - warum sollte dieser überarbeitete Plan anders sein?&quot; CFO)
* &quot;Das Integrationsrisiko, das wir im 2. Quartal gekennzeichnet haben, ist im Zeitplan immer noch nicht berücksichtigt.&quot; (CIO)
* &quot;Ich muss wissen, dass die ursprünglichen Geschäftsergebnisse immer noch auf dem Tisch liegen.&quot; (Unternehmenssponsor)
* &quot;Wenn der Anbieter diese Verzögerung verursacht hat, was ändert sich dann am Vertrag?&quot; (Procurement Lead)

**Erfolgsstatus.** Der Lenkungsausschuss billigt den überarbeiteten Plan und einigt sich auf die nächsten Schritte - wobei jede der vier Personen ausdrücklich ihre Zustimmung erteilt, nicht nur die lauteste Person im Raum.

## Gold-Standard-Rollenspielvorlage

Bei jedem Rollenspiel sollte Folgendes eindeutig beantwortet werden, wobei das Feld &quot;Virtueller Coach&quot; verwendet werden sollte, um Folgendes zu erreichen:

| **Diese Vorlage fragt** | **Konfiguration in** |
|---|---|
| Szenario — warum reden diese Leute? | Gesprächskontext |
| Geschäftskontext: Welches Ereignis hat die Konversation ausgelöst? | Gesprächskontext |
| Persona - mit wem spricht der Lernende? | Persona Background Information |
| Prioritäten und Zwänge - welche Ergebnisse und Zwänge beeinflussen die Person? | Persona Background Information |
| Sorgen - welche Sorgen oder Herausforderungen prägen ihre Entscheidungen? | Persönliche Bedenken |
| Ziel: Was sollte der Teilnehmer erreichen? | Kontext des Endes der Unterhaltung, reflektiert in abzudeckenden Themen |
| Häufige Einwände - welcher Widerstand sollte während der Unterhaltung entstehen? | In persönliche Anliegen eingegliedert |
| Zeilen öffnen - wer spricht als Erster, und wie? | AI Trainer Opener + AI Persona Opener |
| Bewertungskriterien: Welche beobachtbaren Verhaltensweisen definieren den Erfolg? | Themen, die abgedeckt werden sollen (mit Stärke und Erstellen oder Unterbrechen) |
| Erfolgsstatus - was sollte stimmen, wenn die Unterhaltung endet? | Wird in Ihren höchstgewichteten Themen widergespiegelt |

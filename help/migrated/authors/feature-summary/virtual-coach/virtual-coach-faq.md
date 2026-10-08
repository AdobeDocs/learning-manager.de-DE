---
description: Hier finden Sie Antworten auf häufige Fragen zu Authoring, Lizenzierung, Sicherheit, Datenschutz, Punktzahl und dem Lernerlebnis für Teilnehmer
jcr-language: en_us
title: Häufige Fragen zum virtuellen Coach
exl-id: b8955b04-4655-413a-b570-a05b1f76285c
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '1904'
ht-degree: 0%
---

# Häufige Fragen zum virtuellen Coach

## Authoring

Hier erhalten Sie Antworten auf häufige Fragen zum Erstellen, Konfigurieren und Beheben von Fehlern beim Rollenspiel eines virtuellen Coaches.

1. **Warum erreichte mein Rollenspiel den Wert Null, obwohl ich die meisten Themen behandelt habe?**
Überprüfen Sie, ob für eines Ihrer Themen **Make oder Break** aktiviert ist. Wenn ein Teilnehmer während der Unterhaltung überhaupt nicht auf ein &quot;Erstellen&quot;- oder &quot;Unterbrechen&quot;-Thema eingeht, ist der Endwert der Simulation 0, unabhängig davon, wie gut er an allem anderen gearbeitet hat. Reservieren Sie Make oder Break für ein oder zwei wirklich nicht verhandelbare Themen, um dies bei einem vernünftigen Versuch zu vermeiden. Die vollständige Einrichtung finden Sie unter [Erstellen und Veröffentlichen eines virtuellen Coach-Rollenspiels](/help/migrated/authors/feature-summary/virtual-coach/create-publish-virtual-coach-role-play.md).

2. **Wie viele Personas kann ein Rollenspiel für mehrere Personen enthalten?**
Bis zu vier Personas in einem einzelnen Szenario, jede individuell mit ihrer eigenen **Rolle**, **Persönlichkeit** und **Persona Concerns** konfiguriert. Verwenden Sie diese Option, wenn ein Teilnehmer mehr als einen Stakeholder in derselben Konversation navigieren muss, z. B. einen Verkaufsgesprächskomitee oder einen Vorstandsbericht.

3. **Wie wähle ich zwischen Sprache, Chat und Video für ein Rollenspiel aus?**
Dies hängt vom ausgewählten Personentyp ab. **Systempersonas** unterstützen entweder **Sprache und Video** (ein animierter Avatar mit einer gesprochenen Stimme) oder nur **Stimme**. **Benutzerdefinierte Personas** unterstützen Sprachinteraktionen, und Sie können **Video Avatar** separat für Personas aktivieren, die den Sprach- und Videomodus unterstützen. Wählen Sie &quot;Sprache und Video&quot; für die realistischste Simulation aus oder &quot;Nur Sprache&quot; für Szenarien, in denen kein visueller Avatar erforderlich ist, wie z. B. telefonbasiertes Training.

4. **Wie schreibe ich eine gute Eingabeaufforderung für den KI-Co-create-Assistenten?**
Geben Sie eine kurze Beschreibung ein, in der das Szenario beschrieben wird, z. B. `Handling price objections in enterprise sales` oder `Pitching our new product to a buying committee`. Der KI-Assistent stellt dann Anschlussfragen, um Sie beim Aufbau der Themen &quot;Übersicht&quot;, &quot;KI-Persona&quot; und &quot;Evaluierung&quot; zu unterstützen. Gebt so viel Kontext wie möglich über die Situation, die Rolle und Sorgen der Person und wie ihr den Erfolg messen möchtet vor - mehr Details in eurer ursprünglichen Beschreibung bedeutet weniger Hin und Her im Chat. Eine Vorlage mit umfassenderen Eingabeaufforderungen finden Sie unter [Materials für ein Virtual Coach-Rollenspiel sammeln](/help/migrated/authors/feature-summary/virtual-coach/gather-materials-for-virtual-coach-role-play.md).

5. **Kann ich ein Rollenspiel nach der Veröffentlichung bearbeiten?**
Ja. Änderungen an persönlichen Einstellungen, Themen und anderen Konfigurationen werden sofort für alle unveröffentlichten Rollenspiele wirksam. Wenn ein Rollenspiel bereits veröffentlicht und den Teilnehmern zugewiesen wurde, veröffentlichen Sie es erneut, nachdem Sie Änderungen vorgenommen haben, damit die Teilnehmer die neueste Version sehen.

Allgemeine Fragen zu Produkten, Lizenzen und Administratoren finden Sie in den [Häufig gestellte Fragen zu Adobe Learning Manager Virtual Coach](/help/migrated/authors/feature-summary/virtual-coach/virtual-coach-faq.md).

## Schulung und Compliance

1. **Wie schützt Virtual Coach die Daten von Kunden und Teilnehmern?**
Kundendaten werden mit AES-256-Verschlüsselung gespeichert, bei der Übertragung mit TLS 1.3+ geschützt und logisch durch eindeutige Kundentrennungen getrennt, um die Isolation zwischen Kundenumgebungen zu gewährleisten. Diese Kontrollen werden durch jährliche Penetrationstests von Drittanbietern validiert.

2. **Wo werden Virtual Coach-Daten gespeichert und verarbeitet?**
Kundendaten werden in EU-Rechenzentren gespeichert, um die Anpassung an die europäischen Datenschutzanforderungen zu unterstützen.

3. **Wie lange bewahrt Virtual Coach Kunden- und Teilnehmerdaten auf, und können sie gelöscht werden?**
Sitzungsdaten können für die Dauer der Servicevereinbarung aufbewahrt werden, und Kunden können unternehmensspezifische Aufbewahrungsrichtlinien konfigurieren. Einzelne Benutzer können ihre eigenen Aufzeichnungen löschen, Administratoren können Massenlöschungen durchführen und Daten können vor dem Löschen exportiert werden. Auch automatische Löschmechanismen und Audit-Protokollierung werden unterstützt.

4. **Wird vom Kunden hochgeladener Inhalt für andere Zwecke als zum Generieren des Rollenspiels verwendet, z. B. für KI-Schulungen oder Produktverbesserungen?**
Nein, Kundendaten werden nicht für KI-Schulungen verwendet.

5. **Wie nutzt Virtual Coach KI, und welche Sicherheitsvorkehrungen gelten für KI-generierte Antworten?**
Der virtuelle Coach nutzt generative KI, um interaktive Rollenspielerlebnisse zu erstellen. Es wurden mehrere Sicherheitsmechanismen eingeführt, darunter Azure OpenAI-Inhaltsfilter für Kategorien wie Gewalt, Hassreden, sexuelle Inhalte und Selbstverletzung. Soforthilfe-Leitplanken; und kontextbezogene Steuerelemente, die den Schwerpunkt der KI auf den Nutzungsszenarien für Lernen und Entwicklung halten. Auch KI-Sicherheitstests werden durchgeführt, und Sicherheitsvorkehrungen wie die sicherheitsbasierte Prompt-Transformation und das Verhalten &quot;Klarheit - dann ablehnen&quot; werden für sensible Anfragen verwendet. Darüber hinaus erfordern vertragliche Verpflichtungen die Offenlegung von AI-erzeugten Produkten und die Einhaltung der geltenden AI-Vorschriften.

6. **Welche Datenschutz- und Compliance-Standards unterstützt Virtual Coach?**
Virtual Coach unterstützt DSGVO-bezogenen Datenschutz, konfigurierbare Aufbewahrungskontrollen, Audit-Protokollierung, Funktionen zum Löschen von Benutzern und EU-basiertes Daten-Hosting. Die vertragliche Vereinbarung erfordert auch die Einhaltung geltender Gesetze und Vorschriften, einschließlich des EU AI Act und des California AI Transparency Act (SB-942).

7. **Wem gehören Inhalte, die in den virtuellen Coach hochgeladen wurden, und die Inhalte, die während einer Sitzung generiert wurden?**
Der Kunde besitzt die Inhalte, die in Virtual Coach hochgeladen wurden, sowie die Inhalte, die während einer Sitzung generiert wurden.

8. **Wo befinden sich Virtual Coach-Daten in Adobe Learning Manager oder beim Virtual Coach-Dienstanbieter?**
Rollenspieldaten werden in der Cloud-Infrastruktur des Virtual Coach-Dienstleisters gespeichert und in EU-Rechenzentren gehostet.

## Produkt

1. **Wie wird Virtual Coach für einen bestehenden Adobe Learning Manager-Kunden aktiviert?**
Siehe [Virtuellen Coach aktivieren](/help/migrated/administrators/feature-summary/virtual-coach/manage-virtual-coach-usage-billing.md#activatevirtualcoach)

2. **Wie lange ist die Virtual Coach-Aktivierung gültig und wie wird sie erneuert?**
Die Aktivierung von Virtual Coach in Adobe Learning Manager gilt für die Dauer Ihres Add-on-Abonnementvertrags. Es ist nicht automatisch unbefristet. Stattdessen richtet sich die Gültigkeit nach Ihrem Abonnementzeitraum.

   **Verlängerung:** Um den virtuellen Coach nach Ablauf des Vertragszeitraums weiterhin verwenden zu können, müssen Sie Ihr Abonnement verlängern. Zum Zeitpunkt des Kaufs stellt Adobe einen Aktivierungsschlüssel zur Verfügung, den der Kontoadministrator verwendet, um Virtual Coach im Bereich &quot;Abrechnung&quot; zu aktivieren. Wenn du deinen Vertrag verlängerst, erhältst du Anweisungen und bei Bedarf einen neuen Aktivierungsschlüssel, damit es zu keinen Unterbrechungen beim Zugriff kommt.

   Monatliche MAU-Credits (Active User) werden ebenfalls für jede Vertragslaufzeit zugeordnet. Nicht genutzte Credits verfallen am Ende des Vertrags. Sie werden nicht in eine erneuerte oder neue Periode übertragen. Ihre Aktivierung dauert so lange, wie Ihr kostenpflichtiges Virtual Coach-Abonnement aktiv ist, und die Verlängerung erfolgt durch Verlängerung Ihres Abonnements, das über Ihr Adobe-Konto verwaltet wird.

3. **Was passiert mit hochgeladenen Quelldokumenten und generierten Sitzungsdaten, nachdem eine Rollenvorgabe erstellt oder abgeschlossen wurde?**
Hochgeladene Quelldokumente können zum Erstellen und Konfigurieren von Rollenspielszenarien, Personas und Bewertungskriterien verwendet werden. Nachdem die Teilnehmer ein Rollenspiel abgeschlossen haben, generiert der virtuelle Coach Bewertungsergebnisse, Punktzahlen, Coaching-Feedback und Abschlussinformationen, um Lern- und Berichtsaktivitäten zu unterstützen. Mit Rollenspielen verknüpfte Daten bleiben gemäß den geltenden Content Lifecycle- und Aufbewahrungs-Policies verfügbar.

4. **Können Teilnehmer ein Rollenspiel erneut versuchen?**
Ja. Teilnehmer können eine Rollenspielsitzung mehrmals wiederholen, um ihre Fähigkeiten zu üben, Coaching-Feedback anzuwenden und ihre Leistung zu verbessern. Nach Abschluss eines Rollenspiels können die Teilnehmer ihr Feedback einsehen und einen weiteren Versuch starten, ihre Kenntnisse weiterzuentwickeln.

## Allgemein

1. **Was ist Virtual Coach?**
Virtual Coach ist eine KI-gestützte Rollenspiel- und Coaching-Funktion, die in Adobe Learning Manager integriert ist. So können Teilnehmer mit einer KI-Person, die in Echtzeit intelligent reagiert, reale Gespräche führen und anschließend einen sofortigen Leistungsbericht erhalten, der ihre Kommentare und ihre Art der Äußerung abdeckt. Eine ausführliche Erläuterung finden Sie unter [Was ist ein virtueller Coach?](/help/migrated/authors/feature-summary/virtual-coach/what-virtual-coach-is.md).

2. **Wer nutzt den virtuellen Coach?**
Unternehmen nutzen Virtual Coach, um Vertriebsmitarbeiter, Kundendienstteams, Callcenter-Mitarbeiter, Manager und Führungskräfte, Neueinstellungen, Partner und Mitarbeiter darin zu schulen, neue Produkte oder Prozesse zu erlernen. Der virtuelle Coach ist für alle Teilnehmer, Autoren und Administratoren in einem Adobe Learning Manager-Konto verfügbar, in dem er aktiviert wurde. Teilnehmer können auf Rollenspielsitzungen zugreifen und diese abschließen, Autoren erstellen und veröffentlichen Rollenspielszenarien und Administratoren verwalten Credits und zeigen Berichte an.

3. **Verwendet Virtual Coach automatisch meine vorhandenen Adobe Learning Manager-Inhalte?**
Anzahl Die Autoren müssen Referenz-Materialien wie Playbooks, Sales Decks, Transkripte und Bewertungsmatrizen oder eine schriftliche Aufforderung für jedes von ihnen erstellte Rollenspiel bereitstellen. Der virtuelle Coach verwendet diese hochgeladenen Materialien und persönlichen Definitionen, um die Konversation zu fördern. Es nutzt nicht automatisch Inhalte, die bereits in Ihrer Inhaltsbibliothek oder in Kursen vorhanden sind. Informationen zur Vorbereitung finden Sie unter [Materialien für ein Virtual Coach-Rollenspiel sammeln](/help/migrated/authors/feature-summary/virtual-coach/gather-materials-for-virtual-coach-role-play.md).

4. **Welche Arten von Rollenspielen sind verfügbar?**
Der virtuelle Coach unterstützt drei Domänen: Vertriebsförderung, Führungskräfteentwicklung und Kompetenzbewertung. Autoren wählen aus vorgefertigten Vorlagen, die Szenarien abdecken, wie B2B-Discovery-Aufrufe, Cold Calls, die Behandlung von Einwänden, schwieriges Feedback und die Deeskalation von Kundenbeschwerden. Autoren können mit dem KI-Assistenten auch benutzerdefinierte Szenarien von Grund auf neu erstellen. Siehe [Erstellen und Veröffentlichen eines virtuellen Coach-Rollenspiels](/help/migrated/authors/feature-summary/virtual-coach/create-publish-virtual-coach-role-play.md).

5. **Welche Sprachen unterstützt Virtual Coach?**
Virtual Coach ist in neun Sprachen sowohl für die Benutzeroberfläche als auch für Simulationsinhalte verfügbar: Deutsch (Deutschland), Spanisch (LATAM), Spanisch (Spanien), Französisch (Frankreich), Italienisch (Italien), Portugiesisch (Portugal), Portugiesisch (Brasilien), Niederländisch (Niederlande) und Englisch.

6. **Wie wird Virtual Coach lizenziert und in Rechnung gestellt?**
Virtual Coach ist als Add-on-Abonnement für Adobe Learning Manager verfügbar. Die Nutzung wird in monatlich aktiven Benutzern (MAUs) gemessen. Ein MAU-Kredit wird verbraucht, wenn ein Teilnehmer einen Kurs in einem Kalendermonat startet; Für weitere Sitzungen desselben Teilnehmers in diesem Monat werden keine zusätzlichen Credits verbraucht. Nicht genutzte Credits verfallen am Ende des Jahresvertrags. Siehe [Nutzung und Abrechnung des virtuellen Coaches verwalten](/help/migrated/administrators/feature-summary/virtual-coach/manage-virtual-coach-usage-billing.md).

7. **Wie wird die Punktzahl eines Teilnehmers berechnet?**
Jede Sitzung erstellt eine Wissensbewertung und eine Stilbewertung. Die Wissensbewertung gibt an, ob der Teilnehmer die erforderlichen Themen behandelt und richtige Informationen bereitgestellt hat. Die Punktzahl für &quot;Stil&quot; gibt an, wie der Teilnehmer kommuniziert hat, einschließlich Tempo, Klarheit, Füllwörter, Stärke von Sätzen und Stimmenergie. Autoren legen die Gewichtung jeder Komponente bei der Konfiguration des Szenarios fest. Eine allgemeine Konfiguration ist 70 % Wissen und 30 % Stil. Siehe [Verstehen Ihres Virtual Coach-Leistungsberichts](/help/migrated/learners/feature-summary/virtual-coach/understand-virtual-coach-performance-report.md).

8. **Können Teilnehmer ihren Leistungsbericht herunterladen?**
Ja. Zusätzlich zur Anzeige des Berichts auf dem Bildschirm können die Teilnehmer ihn als PDF herunterladen, um ihn für ihre eigenen Unterlagen aufzubewahren oder mit einem Manager zu teilen.

9. **Kann ein Teilnehmer ein Rollenspiel erneut versuchen?**
Ja. Teilnehmer können ein Rollenspiel so oft versuchen, wie sie wollen. Jeder Versuch ist eine neue, unabhängige Sitzung und generiert einen neuen Leistungsbericht. Nur die erste Sitzung in einem Kalendermonat verbraucht einen MAU-Kredit.

10. **Können Teilnehmer ihre Sitzungen zur menschlichen Überprüfung einreichen?**
Anzahl

11. **Ist Virtual Coach auf Mobilgeräten verfügbar?**
Virtual Coach wird auf dem Adobe Learning Manager-Desktop und im mobilen Web sowie über APIs unterstützt. Sie ist in der aktuellen Version nicht in der mobilen Adobe Learning Manager-App (iOS/Android) verfügbar.

12. **Werden Teilnehmerdaten zur Schulung der KI verwendet?**
Anzahl Der virtuelle Coach wird in einer DSGVO-konformen Infrastruktur gehostet und es werden keine persönlichen Teilnehmerdaten zum Trainieren von KI-Modellen verwendet.

13. **Was ist der Unterschied zwischen einer Arbeitshilfe und einem Kursmodul für Virtual Coach?**
Eine Arbeitshilfe ist eine eigenständige On-Demand-Ressource, auf die Teilnehmer jederzeit direkt aus dem Katalog zugreifen können, ohne sich für einen Kurs zu registrieren. Auf ein Kursmodul wird als Teil einer strukturierten Kurssequenz mit Registrierung, Abschlussverfolgung und formaler Bewertung zugegriffen. Das gleiche Rollenspiel kann als Arbeitshilfe veröffentlicht und mehreren Kursen gleichzeitig hinzugefügt werden. Siehe [Hinzufügen eines virtuellen Coach-Rollenspiels zu einem Kurs](/help/migrated/authors/feature-summary/virtual-coach/add-virtual-coach-role-play-to-course.md).

14. **Wie sollten wir Virtual Coach verpacken, wenn wir einen neuen Prozess oder ein neues Produkt bereitstellen?**
Verpacken Sie die Rollenspiele in einem Kurs oder auf einer Lernreise neben den entsprechenden Schulungsinhalten und verteilen Sie den Kurslink per E-Mail oder über andere Mitteilungen zum Change-Management. Der virtuelle Coach eignet sich am besten für die letzte Meile des Trainings - den Checkpoint direkt nach Abschluss des zugehörigen Inhalts durch die Teilnehmer, wo sie nachweisen, dass sie ihn anwenden können, anstatt als eigenständige Aktivität.

15. **Wird Virtual Coach auf Headless- oder API-Implementierungen unterstützt?**
Öffentliche APIs zum Abrufen von Kursen und Arbeitshilfen rufen auch virtuelle Coach-Kurse und Arbeitshilfen ab. Der `jobAidType`-Filter ist zum Abrufen von virtuellen Coach-Arbeitshilfen speziell verfügbar. Virtual Coach-Inhalte werden im Headless-Player unterstützt, und Kurse und Arbeitshilfen, die Virtual Coach enthalten, funktionieren im Fluidic Player.

Antworten auf häufig gestellte Fragen zum Erstellen und Konfigurieren von Rollenspielen finden Sie auf dieser Seite.

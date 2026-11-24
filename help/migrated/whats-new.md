---
description: Erfahren Sie mehr über die neuen Funktionen in der Version Dezember 2026 von Adobe Learning Manager, einschließlich Report Builder Charts und Virtual Coach.
jcr-language: en_us
title: Neue Funktionen in der Adobe Learning Manager-Version Dezember 2026
exl-id: da46f186-3ff3-422a-af49-31c7405fd584
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: b05fc0d33acf0b594a64f3ad4aa9a5c8e570ab30
workflow-type: tm+mt
source-wordcount: '4748'
ht-degree: 2%
---

>[!IMPORTANT]
>
>**Haftungsausschluss**
>
>Beta-Funktionen können Mängel enthalten und werden &quot;wie besehen&quot; ohne jegliche Gewährleistung bereitgestellt. Adobe hat das alleinige Ermessen, ob Betafunktionen allgemein verfügbar gemacht werden sollen. Adobe ist nicht verpflichtet, die Beta-Funktionen zu verwalten, zu korrigieren, zu aktualisieren, zu ändern, zu ändern oder auf andere Weise (über Adobe Support Services oder auf andere Weise) zu unterstützen. Sollte eine Beta-Funktion allgemein verfügbar werden, kann sie zusätzlichen Nutzungsbedingungen einschließlich ggf. anfallender Gebühren unterliegen. Beta-Funktionen können sich ohne vorherige Ankündigung ändern, einschließlich der Kündigung. Kunden wird empfohlen, mit Vorsicht vorzugehen und sich in keiner Weise auf die ununterbrochene oder fehlerfreie Funktion oder Leistung der Betafunktionen zu verlassen. Dementsprechend erfolgt jede Nutzung der Beta-Funktionen auf eigenes Risiko des Kunden. Die Produktfunktionen und die zugehörige Dokumentation können sich mit der Weiterentwicklung der Funktion ändern. Diese Dokumentation spiegelt die aktuelle Beta-Erfahrung wider und sollte nicht als endgültige oder vollständige Produktdokumentation betrachtet werden.

# Neue Funktionen in der Adobe Learning Manager-Version Dezember 2026

Die neue Version von Adobe Learning Manager enthält eine Reihe neuer Funktionen und Verbesserungen, mit denen die Plattform optimiert und ihre Funktionen erweitert werden sollen. Diese Updates vereinfachen alltägliche Workflows, verbessern die Organisation und Bereitstellung von Lerninhalten und machen das Gesamterlebnis konsistenter und intuitiver.

## Report Builder- und Dashboards

Adobe Learning Manager unterstützt jetzt Diagramme und Dashboards im Report Builder, sodass Administratoren Berichtsdaten direkt auf der Plattform visualisieren können. Administratoren können Diagramme aus Berichtsspalten erstellen, wobei in jedem Diagramm Aggregation und Filterungen verfügbar sind.

Report Builder unterstützt die folgenden Diagrammtypen:

* Große Zahl
* Liniendiagramm
* Balkendiagramm
* Kreisdiagramm
* Pivot-Tabelle

Ein Berichts-Dashboard enthält Diagramme, die aus einem einzigen Bericht erstellt wurden. Ein benutzerdefiniertes Dashboard kombiniert Diagramme aus mehreren Berichten, z. B. Registrierungs- und Benutzerdaten, und unterstützt bis zu 20 Widgets. Diagramme, die zu einem Bericht gehören, werden freigegeben, wenn Sie den Bericht freigeben. Dadurch können Administratoren aktuelle Berichtsdaten in einer Ansicht verwalten, anstatt Berichte erneut auszuführen. In Diagrammen werden bis zu 10.000 Datenpunkte angezeigt, in Pivot-Tabellen bis zu 100 Zeilen und 100 Spalten. Wenn ein Diagramm einen Grenzwert überschreitet, wenden Sie Filter an, um die Ergebnisse einzugrenzen. Dashboards können noch nicht exportiert werden.

[Weitere Informationen](/help/migrated/administrators/feature-summary/report-builder-visualization.md)

## Insights Agent-Berichte im Report Builder

Administratoren können jetzt mit den Antworten auf den Insights Agent im Report Builder weiterarbeiten. Wenn der Insights Agent eine Frage beantwortet, ordnet der Report Builder die gleiche Abfrage in einem Parallelschritt seinen eigenen Feldern zu. Administratoren können den Bericht öffnen, überprüfen, bearbeiten und speichern. Dort können Sie die gleichen Report Builder-Funktionen wie für andere Berichte verwenden, z. B. Abonnements.

Wenn ein Teil einer Frage nicht mit Report Buildern ausgedrückt werden kann, wird dieser Teil im Bericht als Lücke aufgelistet. Wenn das fehlende Teil von zentraler Bedeutung für die Frage ist, wird der Bericht nicht angeboten. Komplexe Abfragen können zu geringeren Ergebnissen führen. Überprüfen Sie daher jeden Bericht, bevor Sie sich darauf verlassen.

[Weitere Informationen](/help/migrated/administrators/feature-summary/insights-agent.md#create-report-insights-agent)

## Integration mit Adobe Experience Manager Assets

Adobe Learning Manager ist jetzt mit Adobe Experience Manager Assets integriert, sodass Autoren direkt aus einem zentralen Repository auf genehmigte Lerninhalte und Bild-Assets zugreifen und diese verwenden können. Dadurch wird der manuelle Download- und Upload-Schritt zwischen dem Team, das die Assets im Digital Asset Manager (DAM) verwaltet, und dem Team, das Kurse in Adobe Learning Manager erstellt, entfernt.

Änderungen:

* **Zugriff auf genehmigte Assets:** Autoren können Assets aus Experience Manager Assets durchsuchen und auswählen, ohne Adobe Learning Manager zu verlassen. Kurse verwenden daher aktuelle, genehmigte Dateien anstatt lokaler Kopien, die veraltet sein können.
* **Kurs-Assets auf dem neuesten Stand halten:** Wenn sich ein Asset im DAM ändert, kann die Aktualisierung automatisch in die Kurse fließen, wobei Inhalte konsistent bleiben, wenn Assets überarbeitet werden.
* **Der Zugriff folgt bestehenden Berechtigungen:** Autoren sehen nur die Assets, auf die sie bereits Zugriff haben, in Experience Manager Assets. Beim Durchsuchen in Adobe Learning Manager werden daher dieselben Berechtigungen wie für das DAM selbst berücksichtigt.

Das Ergebnis ist ein einzelner, gesteuerter Pfad vom Asset zum Teilnehmer, mit weniger manueller Arbeit und weniger Versionskonflikten.

[Weitere Informationen](/help/migrated/integration-admin/feature-summary/aem-assets-integration.md)

## Verbesserungen bei der Dateiübermittlung

Dateiübermittlungsmodule unterstützen jetzt Teamübermittlungen und strukturbasierte Evaluierung. Eine neue Einstellung steuert auch, ob die Genehmigung des Kursleiters für Einreichungen erforderlich ist.

### Teameinreichungen

Kursleiter können jetzt Teams für Dateiübermittlungen erstellen. Jedes Team sendet eine Datei für das gesamte Team. Der Kursleiter bewertet die Einreichung einmal, und das Ergebnis gilt für jedes Mitglied. Es gibt zwei Möglichkeiten für Teamformulare: Kursleiter erstellen sie manuell oder ein geplanter Prozess erstellt sie vor dem Startdatum der Instanz basierend auf den Mitgliedern pro Team oder der Anzahl der Teams.

Die Kursleiter verwalten die Teams auf einer neuen Seite **Teamverwaltung** und überprüfen die Arbeit auf einer Seite für Teameinreichungen. Kursleiter können auch die Einreichung einer genehmigten Einreichung aufheben, um das Team zu entsperren, wenn Änderungen erforderlich sind, z. B. wenn ein Team-Mitglied das Team verlässt. Ein Team fasst bis zu 100 Mitglieder. Teilnehmer können ihr Team, ihre Mitglieder und das Bewertungsergebnis einsehen. Team-Module können nach Veröffentlichung eines Kurses nicht mehr hinzugefügt oder gelöscht werden.

[Weitere Informationen](/help/migrated/learners/feature-summary/submit-assignment-as-team.md)

### Rubrikbasierte Bewertungen (Evaluierungsplan)

Autoren können jetzt eine als Evaluierungsplan bezeichnete Rubrik für Dateiübermittlungsmodule definieren. Eine Rubrik unterstützt objektive Fragen mit bewerteten Optionen und subjektive Fragen mit schriftlicher Prüfung.

Autoren können auch die folgenden Einstellungen konfigurieren:

* Gibt an, ob Teilnehmer die regelbasierten Bewertungsfragen anzeigen, bevor sie das Dokument einreichen
* Ob die Punktzahl eine Gesamtpunktzahl oder eine Punktzahl für jedes Kriterium ist

Jede Frage kann als erforderlich markiert und so konfiguriert werden, dass Reviewerbemerkungen zugelassen werden. Eine abteilungsbasierte Bewertung umfasst bis zu 100 Fragen, und die Autoren geben die Fragen für jedes Gebietsschema separat ein. Nach der Veröffentlichung eines Kurses kann sich nur der Fragentext ändern.

[Weitere Informationen](/help/migrated/administrators/feature-summary/team-submissions-and-rubrics.md)

### Kursleitergenehmigung oder automatische Vervollständigung

Autoren können jetzt auswählen, ob Dateiübermittlungen eine Genehmigung des Kursleiters erfordern oder automatisch abgeschlossen werden. Diese Einstellung ist unabhängig vom Evaluierungsplan.

## Model Context Protocol Server für Teilnehmerassistenten

Mit ALM können Teilnehmer über einen Model Context Protocol (MCP)-Server auf Lernprogramme in den Tools zugreifen, die sie bereits verwenden. Teilnehmer können von überall auf den Learning Manager zugreifen, einschließlich ChatGPT, Claude und benutzerdefinierte Agenten. Konfigurieren Sie den Server in der Integrations-Admin-App, um Administratoren Zugriff auf sechs Kernwerkzeuge für Teilnehmer zu gewähren. Dazu gehören zwei Tools für den Teilnehmerassistenten: Antwort: Agent und personalisierter Lernpfad.

Der Server bietet die folgenden Funktionen:

* Suchen
* Registrierungen auflisten
* Lernobjekt abrufen
* Benutzerprofil abrufen
* Frage zu Lerninhalten beantworten
* Personalisierter Lernpfad

Administratoren können jede Tool-Beschreibung bearbeiten, um organisationsspezifische Beispiele hinzuzufügen. Clients lesen die Autorisierungsdetails aus den Server-Metadaten, daher benötigt das Setup nur eine Client-ID und ein Client-Secret.

[Weitere Informationen](/help/migrated/integration-admin/feature-summary/configure-alm-mcp-server.md)

## Personalisierte Bearbeitung von Lernpfaden und Branding-Streifen

* Teilnehmer können vorgeschlagene Themen oder Kurse jetzt in einem einzigen Schritt entfernen, zusätzlich zu der vorhandenen Option, um Themen- und Kurslisten über Chat zu verfeinern.
* Administratoren können jetzt den Streifen &quot;Personalisierte Lernpfade&quot; auf der Teilnehmer-Startseite über die Branding-Seite neu positionieren.

[Weitere Informationen](/help/migrated/administrators/feature-summary/customize-learner-homepage.md#add-reorder-homepage-strips)

## Üben Sie Ihre Fähigkeiten mit Rollenspielen im virtuellen Coach

Adobe Learning Manager bietet jetzt Virtual Coach, eine KI-gestützte Rollenspiel- und Coaching-Lösung, mit der Teilnehmer realistische Unterhaltungen am Arbeitsplatz üben können, bevor sie sich ihnen bei der Arbeit stellen. Beispiele hierfür sind Einwände im Zusammenhang mit Verkäufen, Kundeneskalationen und Leistungsüberprüfungen.

Autoren erstellen Szenarien aus ihren eigenen Referenzszenarien mithilfe von Vorlagen oder einem AI-Assistenten, und die Teilnehmer sprechen mit einer KI-Person, die sich in Echtzeit an ihre Material anpasst. Nach jeder Sitzung erhalten die Teilnehmer eine sofortige Punktzahl und erhalten Coaching-Feedback zu Wissen und Kommunikationsstil, gemessen anhand der vom Autor definierten Kriterien.

Virtual Coach unterstützt neun Sprachen und kann als eigenständige Arbeitshilfe verwendet oder in einen Kurs eingebettet werden.

[Weitere Informationen](/help/migrated/authors/feature-summary/virtual-coach/what-virtual-coach-is.md)

## Zitate von Lernpfaden im Teilnehmerassistenten

In den Antworten des Teilnehmer-Assistenten wird jetzt der Lernpfad zitiert, der einen Quellkurs enthält, zusammen mit dem Kurs selbst. Teilnehmer öffnen entweder die Kursübersicht oder die Lernpfadseite über das Zitat. Antworten auf eine Arbeitshilfe enthalten einen Download-Link. Dies hilft Teilnehmern, die Schulung zu finden, die ihre Frage beantwortet.

[Weitere Informationen](/help/migrated/learners/feature-summary/learner-ai-assistant.md#learning-path-citations)

## AI Assistant-Konfigurationen

Der Administrator Assistant bietet zwei Agenten an: Insights Agent und Knowledge Agent. Sie können einzeln konfiguriert werden. Der Teilnehmer-Assistent bietet drei Agenten: Knowledge Agent, Answer Agent und Learning Path Agent. Sie können zusammen mit der Katalogkonfiguration konfiguriert werden.

[Weitere Informationen](/help/migrated/learners/feature-summary/learner-ai-assistant.md#configure-la-agents)

## Webhooks für Kursleiter-Bearbeitungen bei Lernobjektinstanzen

Der Webhook zur Änderung der Lernobjektinstanz wird jetzt zusätzlich zu den Änderungen an Administratoren und Autoren auch ausgelöst, wenn ein Kursleiter eine Sitzung im virtuellen Klassenzimmer bearbeitet. Änderungen wie Sitzungszeiten, Veranstaltungsort und Registrierungslimit lösen sie aus. Headless-Kunden können dann Sitzungsdetails über die öffentliche API abrufen und Aktualisierungen an Teilnehmer weitergeben.

[Weitere Informationen](/help/migrated/integration-admin/feature-summary/webhook-instructor-edits.md)

## Mehrere registrierte Kurse im Compliance-Widget

Das Kompatibilitäts-Widget listet jetzt jede Instanz eines Kurses mit mehreren Registrierungen auf, den ein Teilnehmer abschließen muss. In jedem Eintrag wird der Instanzname angezeigt. Wenn eine Instanz über einen Abgabetermin verfügt, wird jede Instanz ohne Abgabetermin ausgeblendet. Der Registrierungsendpunkt der öffentlichen API unterstützt dasselbe Verhalten über einen optionalen Parameter.

[Weitere Informationen](/help/migrated/api-changes-dec-2026.md#api-multienrolled-instances-lc-widget)

## Einladungen zu Sitzungen im virtuellen Klassenzimmer erneut senden

Administratoren mit Kursbearbeitungsberechtigung können jetzt eine Sitzungseinladung von der Instanzseite aus erneut senden. Wählen Sie **Erneut senden**, suchen Sie nach dem Teilnehmer, und senden Sie den Kurs. Diese Option ist für aktuelle und zukünftige Sitzungen vom Typ &quot;Virtuelles Klassenzimmer&quot; verfügbar. Bei Teilnehmern in mehreren Instanzen wird die Einladung nur zur ausgewählten Instanz gesendet. Teilnehmer, die nicht für die Sitzung registriert sind, werden mit einer Warnung übersprungen.

[Weitere Informationen](/help/migrated/instructors/feature-summary/resend-session-invite.md)

## Automatische Anwesenheit aus Adobe Connect-Aufnahmeansichten

Adobe Learning Manager markiert jetzt die Anwesenheit, wenn ein Teilnehmer die Aufzeichnung einer verpassten virtuellen Klassenzimmersitzung abspielt. Bei einer geplanten Integration werden Viewer-Daten aus Adobe Connect abgerufen und die Wiedergabezeit mit den für das Konto festgelegten Abschlusskriterien verglichen. Administratoren legen den Zeitplan in der Integrationsadministrator-App fest. Adobe Learning Manager berücksichtigt bei der Bestimmung der Anwesenheit nur die tatsächliche Anzeigezeit, sodass das Überspringen einer Aufzeichnung nicht auf die Abschlusskriterien angerechnet wird.

[Weitere Informationen](/help/migrated/integration-admin/feature-summary/track-attendance-through-adobe-connect.md)

## Email Builder für Kurse und Instanzen

Mit Email Builder in Adobe Learning Manager können Administratoren und Autoren Vorlagen für die Kommunikation mit Teilnehmern im Branding erstellen. In der ALM-Version vom Dezember 2026 ist das vollständige E-Mail-Builder-Erlebnis für E-Mails auf Kurs- und Instanzebene verfügbar. Autoren können diese E-Mails anpassen, während sie die Layouts und Formatierungen übernehmen, die Administratoren definieren.

Mit Email Builder könnt ihr:

* Wiederverwendbare E-Mail-Layouts erstellen
* Branding-Elemente Ihrer Organisation anwenden
* Banner und Signaturen anpassen
* Definieren von Standardschriften und -farben
* Standardisieren Sie die Kommunikation über Kurse und Lernprogramme hinweg.

Administratoren erstellen kontoweite E-Mail-Vorlagen und -Layouts. Autoren passen E-Mails auf Kurs- und Instanzebene an, ohne die Vorlagen von Grund auf neu erstellen zu müssen.

Die Einstellungen für Banner und Signatur wurden verschoben. Früher wurden diese Einstellungen auf einer separaten Registerkarte **Einstellungen** angezeigt. Diese Registerkarte wurde entfernt, und **Banner** und **Signatur** werden jetzt in **Globales Layout** angezeigt.

Mit Email Builder können Sie E-Mail-Titel mit der Variable &quot;Titel&quot; hinzufügen.

### Funktionsweise der Hierarchie von Email Builder

Email Builder verwendet eine Hierarchie. Jede Ebene erbt von der übergeordneten Ebene und ermöglicht die lokale Anpassung.

| **Ebene** | **Bereitgestellte Funktionen** | **Wer passt es an** |
|----|----|----|
| Account-Layout | Branding, Schriften, Farben sowie Kopf- und Fußzeilenstruktur | Administratoren |
| Kontovorlage | Globales Styling von E-Mails, gemeinsame Messaging-Komponenten und gemeinsames Branding | Administratoren |
| Kursvorlage | Kursspezifische E-Mails wie Registrierungsmeldungen, Kurserinnerungen, Abschluss-E-Mails und Sitzungsbenachrichtigungen | Autoren |
| Instanzvorlage | Die höchste Anpassungsstufe, z. B. kohorten-, sitzungs- oder regionsspezifische Meldungen | Autoren |

Alle Kurse können von Kontovorlagen erben. Kurs-E-Mails übernehmen das Layout des Unternehmens und ermöglichen die Anpassung von Inhalten.

### Layout-Vererbung

Eine Vorlage wird mit dem nächstgelegenen verfügbaren Layout verknüpft. Eine Vorlage auf Instanzebene wird mit einem vorhandenen Layout auf Instanzebene verknüpft. Wenn keine vorhanden ist, wird die Vorlage mit dem nächstgelegenen übergeordneten Layout verknüpft. Sie können sehen, von welcher Ebene ein Layout kommt.

Wenn eine Vorlage mit einem Layout verknüpft ist:

* Das Branding fließt automatisch in die Vorlage ein
* Autoren aktualisieren nur den Inhalt
* Die Duplizierung wird für alle Nachrichten verringert.

Sie können die Verknüpfung einer Vorlage zum Layout aufheben. Nachdem Sie die Verknüpfung einer Vorlage aufgehoben haben:

* Die Vorlage behält ihr bestehendes Design bei
* Zukünftige Layoutaktualisierungen wirken sich nicht auf die Vorlage aus
* Die Vorlage kann unabhängig voneinander bearbeitet werden.

Die Vererbung des Layouts hängt von den verfügbaren übergeordneten Layouts ab. Wenn beide vorhanden sind, überschreiben E-Mails auf Instanzebene die Vorlagen auf Kursebene.

### So teilen Administratoren und Autoren die Arbeit

Administratoren erstellen ein Account-Layout, erstellen eine Account-Vorlage und veröffentlichen das Branding. Autoren übernehmen dann das Layout, passen die Kurs-E-Mail an, speichern die Vorlage und veröffentlichen den Kurs. Autoren verwenden Vorlagen auf Instanzebene, wenn Kohorten unterschiedliche Nachrichten benötigen, die sie über Kursinstanzen verwalten.

### Verfügbarkeit von Email Builder für Kurs- und Instanz-E-Mails

Wenn Email Builder bereits für Ihr Konto aktiviert ist, erhalten Sie die neuen Änderungen automatisch und müssen keine Maßnahmen ergreifen. Bestehende E-Mail-Funktionen funktionieren weiterhin unabhängig von den Migrationsaktivitäten von Email Builder.

[Weitere Informationen](/help/migrated/authors/feature-summary/customize-course-instance-emails.md)

## Benutzerdefinierte Teilnehmerattribute in der Interoperabilität von Lernwerkzeugen

Adobe Learning Manager liest jetzt benutzerdefinierte Teilnehmerattribute über den optionalen Endpunkt der Namen- und Rollenbereitstellungsdienste der Interoperabilität von Lernwerkzeugen. Sie werden auch von der Startanforderung gelesen. Attribute wie Land oder Stadt werden in gruppierbaren Profilfeldern gespeichert. Startparameter erfordern ein Präfix, damit Adobe Learning Manager sie erkennt. Einige Lernsysteme, z. B. Moodle, unterstützen diesen Endpunkt nicht.

[Weitere Informationen](/help/migrated/integration-admin/feature-summary/lti-support-for-nrps.md)

## Diskussions-Dashboard - Kursleiterbenachrichtigungen

Headless-Kunden können Kursleitern und Kohortenmanagern jetzt einen Überblick über die Diskussions-Dashboard-Aktivität senden. Mithilfe der API fügen Sie Abonnenten zu einem Board hinzu. Sie erhalten neue Beiträge, Kommentare und Antworten in einem von Ihnen festgelegten Intervall in einer einzigen E-Mail. Likes und Abneigungen sind nicht enthalten. Sie aktivieren die Funktion über die API.

[Weitere Informationen](/help/migrated/discussion-board-instructor-notifications.md)

## Relevanz-Ranking in der Admin-Katalogsuche

Die Katalogsuche in der Admin-Ansicht bewertet die Ergebnisse jetzt nach Relevanz, wobei sie den gleichen Suchdienst wie Teilnehmer und die Admin-Suche an einer anderen Stelle verwendet. Eine exakte Übereinstimmung, z. B. ein Katalogname mit einem bestimmten Datum, wird zuerst angezeigt, gefolgt von Teilübereinstimmungen. Die Vorschlagsliste folgt während der Eingabe derselben Reihenfolge.

[Weitere Informationen](/help/migrated/administrators/feature-summary/catalogs.md#search-catalogs)

## Synchronisierung des Sitzungsabbruchs über Adobe Workfront

In Adobe Workfront abgebrochene Sessions werden während des Migrationsvorgangs ohne manuelle Schritte an Adobe Learning Manager übertragen. Die Migration fügt eine optionale **Statusspalte** hinzu, die **Aktiv** oder **Abgebrochen** akzeptiert. Bei einem leeren Wert bleibt die Sitzung unverändert. Eine durch Migration vorgenommene Absage verhält sich wie eine Absage in der Lern-Manager-Oberfläche. Teilnehmer, Kursleiter, Administratoren, Autoren und Manager erhalten die gleichen Kündigungs-E-Mails.

Für abgebrochene Sitzungen gelten zwei Verhaltensweisen:

* Die Migration wendet keine Detailänderungen auf eine abgebrochene Sitzung an und gibt einen Validierungsfehler für diese Zeilen zurück.
* Wenn Sie den Status auf &quot;Aktiv&quot; setzen, wird die Sitzung erneut aktiviert. Anschließend können Sie die Details aktualisieren oder die Sitzung erneut abbrechen.

Die Sitzungsaktualisierungen funktionieren weiterhin wie zuvor.

[Weitere Informationen](/help/migrated/integration-admin/feature-summary/alm-workfront-cancellation.md)

## Zeichenbeschränkung für Vornamen

Adobe Learning Manager akzeptiert jetzt Vornamen mit bis zu 255 Zeichen, ab 63. Dies gilt für Benutzer, die über den CSV-Import in der Benutzeroberfläche und bei der Selbstregistrierung hinzugefügt wurden, sodass die Benutzersynchronisierung von anderen Systemen in langen Namen nicht mehr fehlschlägt.

Dies ist besonders hilfreich, wenn Sie Benutzer von einem externen System migrieren oder die Benutzererstellung automatisieren.

Ab der Version vom Dezember 2026 akzeptiert das Feld Vorname bis zu 255 Zeichen. Frühere Versionen akzeptierten maximal 63 Zeichen.

>[!NOTE]
>
>Das Limit gilt für alle Benutzer in Ihrem Konto, unabhängig von ihrer Rolle. Bestehende Benutzer und ihre Namen sind von dieser Änderung nicht betroffen.

Sie können lange Namen eingeben, wenn Sie Benutzer wie folgt hinzufügen oder bearbeiten:

* Hinzufügen eines einzelnen Benutzers in der Administratoroberfläche
* Vorhandenen Benutzer bearbeiten
* Benutzer mit einer CSV-Datei importieren
* Benutzer durch Selbstregistrierung registrieren
* Benutzer hinzufügen

Lange Namen können breiter sein als der in einigen Teilen der Benutzeroberfläche verfügbare Platz. Damit das Layout lesbar bleibt, verkürzt Adobe Learning Manager lange Namen in den folgenden kompakten Bereichen:

* Tabellenzellen
* Dropdown-Listenelemente
* Suchergebnisse

Um den vollständigen Namen anzuzeigen, bewegen Sie den Mauszeiger über den verkürzten Namen.

[Weitere Informationen](/help/migrated/deployment-guide/user-setup.md#character-limit-username)

## Abzeicheninformationen für Kurse und Lernpfade

Wenn Autoren einen Kurs oder Lernpfad hinzufügen, werden in einem Fenster vorhandene Kurse und Lernpfade mit Abzeichen aufgelistet. Das Fenster zeigt den Namen, den Typ (Kurs oder Lernpfad), den Veröffentlichungsstatus und das Kursformat an, z. B. Selbststudium, Virtuell, Klassenzimmer oder Gemischt.

[Weitere Informationen](/help/migrated/authors/feature-summary/create-learning-path.md)

## Verbesserungen, die nicht angemeldet sind

Learning Manager ermöglicht jetzt einen kontrollierten Zugriff auf Lerninhalte, ohne dass sich Benutzer anmelden müssen. Administratoren können angeben, welche Kataloge öffentlich sind, während Autoren bestimmen können, welche Kurse und Module ohne Konto verfügbar sind. Öffentliche Inhalte werden als durchsuchbare, KI-lesbare Seiten veröffentlicht, sodass die Akademie über Suchmaschinen-Engine und KI-Assistenten wie Claude und ChatGPT auffindbar ist. Die anonyme Nutzung wird pro Besucher verfolgt und getrennt von der angemeldeten Nutzung gemeldet.

### Inhaltsnutzung ohne Anmeldung

Besucher Ihrer öffentlichen Akademie können jetzt ausgewählte Inhalte direkt von der Kursübersichtsseite aus abspielen, ohne dass ein Konto, eine E-Mail oder ein Formular erforderlich sind.

* **Nicht angemeldeten Zugriff aktivieren oder deaktivieren:** Administratoren können die nicht angemeldete Inhaltsnutzung für das gesamte Konto aktivieren oder deaktivieren.
* **Stellen Sie Kurse oder Module ohne Anmeldung zur Verfügung:** Autoren können einen ganzen Kurs ohne Anmeldung zur Verfügung stellen oder nur bestimmte Module öffnen, z. B. ein kostenloses Einführungsmodul, bevor Sie erweiterte Inhalte durchsuchen.
* **Einstellungen aus Kursen erben:** Lernpfade und Zertifizierungen folgen den Einstellungen der darin enthaltenen Kurse, ohne dass eine zusätzliche Einrichtung erforderlich ist.
* **Inhalt anzeigen, ohne sich anzumelden:** Nicht authentifizierte Teilnehmer können verfügbare, nicht angemeldete Inhalte anzeigen, ohne sich bei ihrem Konto anzumelden.
* **Nur Inhalte zum Selbststudium:** Lizenzinhalte von Drittanbietern und erworbene Kataloginhalte können ohne Anmeldung nicht verfügbar gemacht werden.
* **Berichte über anonymen Verbrauch:** Es kann ein Bericht über monatlichen nicht angemeldeten Verbrauch erstellt werden.
* **Aktivieren Sie nicht angemeldete Lerninhalte plattformübergreifend:** Die Nutzung nicht angemeldeter Inhalte wird auf nativen Adobe Learning Manager im Web und auf Mobilgeräten, auf Headless-Bereitstellungen und auf Adobe Experience Manager Sites-Widget-basierten Akademien unterstützt.

### Öffentliche Kataloge auswählen

Administratoren können jetzt die spezifischen Kataloge auswählen, die in der öffentlichen Akademie angezeigt werden. Nur diese Kataloge können von anonymen Besuchern durchsucht und von Suchmaschinen-Engine und KI-Assistenten indiziert werden. Testkurse oder interne Inhalte bleiben also privat.
 

### In Suchmaschinen-Engine und KI-Assistenten finden (Beta)

Adobe Learning Manager kann jetzt Ihre öffentliche Akademie über Suchmaschinen-Engine wie Google und KI-Assistenten wie ChatGPT, Claude und Gemini auffindbar machen. Ihre Kurse können dann in Suchergebnissen und AI-generierten Antworten angezeigt werden, die Ihrer Akademie zugeordnet sind.

* Mithilfe von Steuerelementen auf Kontoebene können Administratoren entscheiden, ob Crawler auf die öffentliche Akademie zugreifen können und ob ihre Inhalte indiziert werden können.
* Jede Akademie erhält eine eigene Sitemap und robots.txt, die automatisch aus den Katalogen generiert werden, die Sie veröffentlicht haben.
* Für Crawler sind Seiten vorab gerendert, sodass KI-Assistenten, die kein JavaScript ausführen, diese weiterhin lesen können.
* Crawler sehen nur, worauf ein Besucher zugreifen kann. Geschützte Inhalte werden nie gelegt.
* Meta-Titel, Beschreibung und strukturierte Daten: Adobe Learning Manager generiert sie basierend auf den Lernmetadaten automatisch für jeden Kurs, jeden Lernpfad und jede Zertifizierung.

>[!NOTE]
>
>Die KI- und Sucherkennung auf nativem Adobe Learning Manager erfordert eine benutzerdefinierte Domäne. Headless-Bereitstellungen müssen Teile des Setups in ihrer eigenen Umgebung implementieren.

>[!NOTE]
>
>Die Dokumentation für diese Funktion wird in Kürze verfügbar sein.

## Kurs einstellen, ohne einen Lernpfad unzugänglich zu machen

Ein eingestellter Kurs oder ein verschachtelter Lernpfad wird aus dem übergeordneten Lernobjekt entfernt, das für neue Registrierungen geöffnet bleibt. Durch das Einstellen eines Kurses wird der Lernpfad nicht mehr unzugänglich.

[Weitere Informationen](/help/migrated/administrators/feature-summary/settings/basic-settings.md#retiral-impact-ho-lo)

## URL für nicht angemeldete Seite für Selbstregistrierungsprofile

Mit Selbstregistrierungsprofilen können externe Benutzer, z. B. Partner oder Mitglieder mehrerer Organisationen, ihre eigenen Adobe Learning Manager-Konten erstellen. Jedes Profil kann jetzt über eine eigene, nicht angemeldete Menü-URL verfügen, die in Experience Builder integriert ist und freigegeben werden kann.

Wenn Benutzer **Registrieren** auf einer Seite auswählen, die über diese URL erreicht wird, werden sie dem Profil hinzugefügt, zu dem die URL gehört. Dadurch werden Benutzer aus verschiedenen Organisationen, z. B. separaten Agenturen oder Partnerunternehmen, in separaten Profilen gespeichert.

[Weitere Informationen](/help/migrated/administrators/feature-summary/experience-builder/non-logged-in-menu-url-self-registration.md)

## Änderungen an Spaltenüberschriften in heruntergeladenen Berichten

Der Report Builder enthält jetzt den Datasetnamen in den Standardspaltenüberschriften der heruntergeladenen Berichte. Der Name aus dem Lernobjektdataset wird daher als **Lernobjekt - Name** anstelle von **Name** angezeigt. Bei aggregierten Spalten enthält die Überschrift auch die Funktion, z. B. &quot;**Anzahl der Lernobjekte - ID**&quot;. Wenn Sie einen benutzerdefinierten Namen in das Feld **Alias** einer Spalte eingeben, wird dieser Alias als Überschrift verwendet und bleibt unverändert.

Nach dem Upgrade werden in vorhandenen Berichten ohne benutzerdefinierte Aliase die aktualisierten Überschriften angezeigt, während Berichtsdaten, Filter und Zeitpläne davon nicht betroffen sind. Wenn Ihre Skripte, Kalkulationstabellen, Business Intelligence-Dashboards oder Integrationen Spalten nach Überschrift referenzieren, aktualisieren Sie sie auf die neuen Namen oder legen Sie einen benutzerdefinierten Alias fest, um eine bestimmte Überschrift beizubehalten.

## Live-Hub

Live Hub ist jetzt allgemein für Ultimate -Kunden verfügbar und bleibt für Prime -Kunden in der Beta-Version.

[Weitere Informationen](./administrators/feature-summary/billing-management.md#view-live-hub-usage)

## Mehrsprachige Unterstützung für Untertitel im Live Hub

Untertitel im Live-Hub wurden verbessert, um zusätzliche Sprachen zu unterstützen. Kursleiter können jetzt die Untertitelsprache in **Raumeinstellungen** basierend auf der Sprache auswählen, die während der Sitzung gesprochen wird.

Untertitel werden automatisch in der ausgewählten Sprache generiert und in einem eigenen Fenster angezeigt, das ständig aktualisiert wird, wenn der Kursleiter spricht. Alle Teilnehmer zeigen Untertitel in der vom Kursleiter ausgewählten Sprache an.

Diese Verbesserung verbessert die Barrierefreiheit für Teilnehmer in verschiedenen Sprachen und hilft ihnen, Live-Sitzungen effektiver zu verfolgen.

[Weitere Informationen](./getting-started-with-live-hub/closed-captions-in-live-hub.md)

## Lokalisierte Live-Hub-Oberfläche und Aufzeichnungsgerät

Die Live Hub-Oberfläche wird jetzt in der Sprache angezeigt, die für die Lern-Manager-Benutzeroberfläche ausgewählt wurde. Beschriftungen und Überschriften während der Sitzung, einschließlich Chat, Teilnehmer, Umfragen, Arbeitsräume und Einstellungen, werden in der vom Benutzer gewählten Sprache angezeigt. Live Hub unterstützt die gleichen 18 Benutzeroberflächensprachen wie Learning Manager, einschließlich Englisch. Der Aufnahme-Player ist ebenfalls lokalisiert, sodass Elemente wie Umfragen in der Kurssprache angezeigt werden. Bei einer Aufnahme eines Deutschkurses wird die Player-Benutzeroberfläche beispielsweise auf Deutsch angezeigt.

Auf diese Weise erhalten globale Teilnehmer ein einheitliches Erlebnis auf der gesamten Plattform und in Sitzungsaufzeichnungen.

## Live-Hub-Sitzungen mit bis zu 5000 Teilnehmern

Der Live Hub unterstützt jetzt umfangreiche Sitzungen mit bis zu 5000 Teilnehmern, sodass Organisationen große Schulungssitzungen durchführen können. Autoren können eine Kapazität von 5000 Teilnehmern auswählen, wenn sie einem Kurs ein Modul für virtuelle Klassenzimmer hinzufügen. Der Live Hub konfiguriert den Raum automatisch basierend auf der Zielgruppengröße und wendet bestimmte Interaktionsbeschränkungen an.

In großen Sitzungen gelten die folgenden Funktionen und Verhaltensweisen:

* Der Zugriff auf die Kamera, die Bildschirmfreigabe und die Whiteboard-Funktionen sind auf Kursleiter beschränkt.
* Arbeitsräume sind nicht verfügbar.
* Große Mengen an gleichzeitigen Chatnachrichten, Reaktionen und Fragen werden in gestaffelten Stapeln bereitgestellt.
* Andere Interaktionen und Funktionen wie Umfragen, Tests, Aufzeichnung und Anwesenheitsverfolgung funktionieren wie in regulären Sitzungen.

Auf diese Weise können Unternehmen große Schulungssitzungen auf derselben Plattform mit einem Raum durchführen, der an die erwartete Zielgruppengröße angepasst werden kann.

[Weitere Informationen](./getting-started-with-live-hub/create-a-live-hub-session.md#create-large-session)

## Kanäle

Kanäle sind jetzt in der Regel für alle Kunden verfügbar.

[Weitere Informationen](./administrators/feature-summary/create-channels.md)

## Gruppenregistrierungsreservierung und Verwaltung von Wartelisten

Gruppenregistrierungsreservierung und Verwaltung von Wartelisten geben Autoren eine genauere Kontrolle darüber, wer sich für Klassenzimmer- und virtuelle Klassenzimmerkurse anmelden kann. Autoren können bestimmten Benutzergruppen Lizenzen zuweisen und separate Daten für die Öffnung der Registrierung für diese Gruppen und für alle anderen Teilnehmer festlegen. Sie können auch die automatische Warteliste-Promotion mit einem Stichtag aktivieren, sodass ein verfügbarer Platz zum nächsten berechtigten Teilnehmer geht. Wenn alle Lizenzen reserviert werden, wird ein Kurs auf die ausgewählten Gruppen beschränkt.

[Weitere Informationen](./authors/feature-summary/courses.md#configure-enrollment-window-and-seat-allocation-for-a-classroom-course)

## Unterstützung für mehrere Zoom-Verbindungen

Adobe Learning Manager unterstützt jetzt mehrere Zoom-Verbindungen innerhalb eines einzigen Kontos, sodass Organisationen virtuelle Klassenzimmersitzungen über verschiedene Zoom-Konten hinweg verwalten können.

Integrationsadministratoren können mehrere Zoom-Verbindungen konfigurieren und sie bestimmten Rollen oder Benutzergruppen zuweisen. Beim Erstellen oder Bearbeiten einer Kurssitzung können Autoren aus den für sie verfügbaren Zoom-Verbindungen auswählen, wobei jede Sitzung eine Verbindung verwendet.

Diese Verbesserung bietet mehr Flexibilität für Organisationen, die mehrere Zoom-Konten verwenden, insbesondere in den folgenden Fällen:

* **Abteilungsspezifische Schulung**: Verwalten separater Zoom-Konten für verschiedene Abteilungen oder Teams innerhalb desselben Learning Manager-Kontos.
* **Partner- und externe Schulung**: Weisen Sie bestimmten Partnern oder Benutzergruppen spezielle Zoom-Verbindungen zu, um deren Schulungssitzungen zu unterstützen.
* **Überwachter Zugriff**: Schränken Sie die Verfügbarkeit von Zoom-Verbindungen basierend auf Rollen oder Benutzergruppen ein, um sicherzustellen, dass Autoren nur die Verbindungen auswählen können, die ihnen zugewiesen sind.
* **Vereinfachte Verbindungsverwaltung**: Ermöglichen Sie Integrationsadministratoren die zentrale Verwaltung mehrerer Zoom-Verbindungen, ohne bestehende Sitzungen zu beeinträchtigen.

[Weitere Informationen](./integration-admin/feature-summary/zoom-connector.md)

## Integration des sicheren Prüfungsbrowsers für Tests

Adobe Learning Manager ist jetzt mit dem sicheren Prüfungsbrowser für native Tests integriert und bietet eine sichere, kontrollierte Umgebung für die Durchführung von Tests. Administratoren können die Integration auf Kontoebene aktivieren und eine Konfigurationsdatei (.seb) für den sicheren Prüfungsbrowser hochladen, um die Bewertungseinschränkungen zu definieren. Die Autoren können dann auswählen, für welche einzelnen Tests ein sicherer Prüfungsbrowser erforderlich ist.

Wenn Teilnehmer ein Quiz absolvieren, für das ein sicherer Prüfungsbrowser erforderlich ist, werden sie aufgefordert, den Browser zu starten. Dadurch wird der Zugriff auf andere Browser und Anwendungen für die Dauer der Prüfung gemäß den vom Administrator definierten Einschränkungen blockiert. Teilnehmer, die es nicht installiert haben, werden aufgefordert, es herunterzuladen.

**Hilfreich:**

* **Zertifizierungsbewertungen:** Führen Sie Tests durch, bei denen die Einschränkung des Zugriffs auf externe Ressourcen wichtig ist.
* **Compliance-Schulung:** Support-gesteuerte Bewertungen für obligatorische Schulungen und behördliche Anforderungen.
* **Bewertungen mit hohem Einsatz:** Verringern Sie die Möglichkeiten für den Zugriff auf nicht autorisierte Anwendungen oder Ressourcen während wichtiger Bewertungen.
* **Flexible Bewertungsverwaltung:** Ermöglichen Sie Autoren, den sicheren Prüfungsbrowser nur für Tests zu benötigen, für die zusätzliche Einschränkungen erforderlich sind.

[Weitere Informationen](/help/migrated/administrators/feature-summary/safe-exam-browser.md)

## Fehlerbehebungen für die Barrierefreiheit im Live Hub

Verbesserungen der Barrierefreiheit im Live Hub verbessern die Benutzerfreundlichkeit von Hilfstechnologien und der Tastaturnavigation.

* **Bildschirmleseprogramme**: Steuerelemente und Inhalte werden jetzt mit NVDA, JAWS, VoiceOver und TalkBack korrekt angekündigt.
* **Tastaturnavigation**: Jedes interaktive Element ist in einer logischen Registerkartenreihenfolge mit einer sichtbaren Fokusanzeige erreichbar, der Fokus wird nicht mehr eingefangen und ein Link zum Überspringen der Navigation ist verfügbar.
* **Untertitel**: Live-Sitzungen zeigen Untertitel in Echtzeit an, Aufzeichnungen unterstützen das Hochladen und Umschalten von Untertiteln, und der Umschalter für Untertitel kann über die Tastatur bedient werden.
* **Farbkontrast**: Text- und UI-Komponenten erfüllen jetzt die erforderlichen Kontrastverhältnisse und es ist ein Design mit hohem Kontrast verfügbar.
* **Zoom und Reflow**: Inhalt und Funktionalität bleiben bei einer Browservergrößerung von 200 % erhalten und der Live-Hub funktioniert mit Bildschirmlupen.

## API-Änderungen in der Adobe Learning Manager-Version Dezember 2026

### Reihenfolge von Lesezeichen-APIs und Behandlung eingestellter Inhalte

Teilnehmer können Schulungen mit einem Lesezeichen versehen, um sie später erneut aufzurufen. Bisher haben Lesezeichen-APIs gespeicherte Schulungen in keiner bestimmten Reihenfolge zurückgegeben, sodass Headless-Integrationen nicht zuerst die zuletzt gespeicherten Schulungen anzeigen konnten. Lesezeichen für eingestellte Lernobjekte blieben ebenfalls in der Liste und führten zu Fehlern &quot;Seite nicht gefunden&quot;.

Dieses Update behebt beide Probleme:

* Lesezeichen werden jetzt zuerst zurückgegeben.
* Lesezeichen für eingestellte Lernobjekte werden nicht mehr zurückgegeben.

Es werden keine neuen Endpunkte, Parameter oder Antwortattribute hinzugefügt, sodass bestehende Integrationen ohne Änderungen weiterarbeiten können.

[Weitere Informationen](/help/migrated/api-changes-dec-2026.md#bookmark-api-ordering-retired-content)

### APIs für Diskussionsforum-Kursleiterbenachrichtigungen

Diese Version enthält neue APIs, die Benachrichtigungen von Diskussions-Dashboard-Kursleitern unterstützen. Verwenden Sie sie, um Kursleiter und Kohortenmanager für Diskussionsforen zu abonnieren und zu steuern, welche Aktivität in ihren Auswahl-E-Mails angezeigt wird.

[Weitere Informationen](/help/migrated/api-changes-dec-2026.md#api-discussion-board-instructors)

### API-Unterstützung für Instanzen mit mehreren Registrierungen in der Teilnehmer-App

Die API für Registrierungen unterstützt jetzt Instanzen mit mehreren Registrierungen in der Teilnehmer-App. Fügen Sie den optionalen `includeMultiInstanceEnrollments=true`-Parameter zu `GET /enrollments` hinzu, um sie einzuschließen. Der Standardwert ist `false`. Vorhandene Integrationen, einschließlich Headless-Implementierungen, funktionieren also unverändert.

[Weitere Informationen](/help/migrated/api-changes-dec-2026.md#api-multienrolled-instances-lc-widget)

### Letztes Zugriffsdatum für die Lernpfadregistrierung

Sie können jetzt benutzerdefinierte Metadaten, wie z. B. das Datum des letzten Zugriffs, in einer Lernpfadregistrierung speichern und sie über die API festlegen und lesen. Auf diese Weise können Sie den zeitgebundenen Zugriff auf die von Ihnen zugewiesenen Lernpfade verfolgen.

* Legen Sie die Metadaten für eine vorhandene Registrierung fest oder wenn Sie einen Teilnehmer mithilfe eines Admin-Tokens registrieren.
* Lesen Sie es mit einem Administrator- oder Teilnehmer-Token.

Die Metadaten dienen deinem eigenen Tracking. Der Zugriff wird nicht gesteuert und nicht auf die Kurse im Pfad angewendet.

[Weitere Informationen](/help/migrated/api-changes-dec-2026.md#api-last-access-date-lp-enrollment)

### Job-API-Jobtyp für Report Builder-Exporte

Die Job-API verfügt über einen neuen Auftragstyp (`generateCustomReport`), der jeden gespeicherten Bericht exportiert, wenn Sie die Report Builder-ID übergeben. Mit dem neuen L2-Quizdatensatz können Sie Quizdaten auf Fragenebene in einem Bericht über mehrere Kurse hinweg exportieren und wiederkehrende Exporte automatisieren.

Vorhandene Auftragstypen, einschließlich `generateQuizReport`, bleiben unverändert.

[Weitere Informationen](/help/migrated/api-changes-dec-2026.md#api-job-report-builder-exports)

### APIs für die Zoom-Verbindung

Verwenden Sie diese APIs zum Anzeigen und Verwalten von Zoom-Verbindungen in Adobe Learning Manager. Verwenden Sie sie, um vorhandene Zoom-Verbindungen abzurufen, Zoom-Anmeldeinformationen zu speichern, Verbindungen zu erstellen oder zu aktualisieren und Zugriffsberechtigungen für Benutzergruppen und benutzerdefinierte Rollen zu verwalten.

**API-Sequenz**

Verwenden Sie die APIs in dieser Sequenz:

| **Schritt** | **API** | **Zweck** | **Authentifizierung** |
|------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------|-----------------------------------------------------|
| 1 | `POST /ctr/authcred/uuid/20012    ` | Speichern Sie die Zoom-Anmeldedaten. | Integrations-Admin-Sitzung |
| 2 | `POST /ctr/app/esconnect  ` | Erstellen Sie eine Zoom-Verbindung oder aktualisieren Sie eine vorhandene. | Integrations-Admin-Sitzung |
| 3 | `PUT /ctr/xtsa/{connectionId}/access` | Legen Sie die Benutzergruppen und benutzerdefinierten Rollen fest, die die Verbindung verwenden können. | Integrations-Admin-Sitzung |

**Authentifizierung und Berechtigungen**

Diese APIs verwenden die sitzungsbasierte Authentifizierung und erfordern, dass sich der Benutzer als Integrations-Admin bei Adobe Learning Manager anmeldet.

[Weitere Infos](./api-changes-dec-2026.md#apis-to-create-and-manage-the-zoom-connector)

---
description: Erfahren Sie mehr über die neuen Funktionen und Verbesserungen in der Version April 2026 von Adobe Learning Manager, einschließlich API- und Webhooks-Änderungen
jcr-language: en_us
title: Neue Funktionen in Adobe Learning Manager Version August 2026
exl-id: da46f186-3ff3-422a-af49-31c7405fd584
source-git-commit: 558b239bd393c175384e6559559929d4d21ee131
workflow-type: tm+mt
source-wordcount: '2747'
ht-degree: 0%

---

# Neue Funktionen in der Version August 2026 von Adobe Learning Manager

>[!IMPORTANT]
>
>Die in diesem Artikel beschriebenen Funktionen sind als Teil der Betaversion verfügbar. Adobe Learning Manager Beta-Funktionen werden zu Evaluierungszwecken bereitgestellt und können vor der allgemeinen Verfügbarkeitsversion geändert, eingeschränkt oder entfernt werden. Funktionsnamen, Verhalten und Konfigurationsoptionen können sich jederzeit ohne Vorankündigung ändern.


## Adaptive Kurse

Mit adaptiven Kursen können Sie eine personalisierte Schulung bereitstellen, indem Sie basierend auf den Benutzergruppen, zu denen die Teilnehmer gehören, steuern, welche Module die einzelnen Teilnehmer sehen und welche erforderlich sind. Ein einzelner Kurs stellt der richtigen Person automatisch die richtigen Inhalte dynamisch zur Verfügung.

Autoren konfigurieren jedes Modul mit **Optional** und **Obligatorisch** für Benutzergruppenregeln. Teilnehmer in verschiedenen Benutzergruppen können völlig unterschiedliche Sätze von Modulen abschließen und dennoch denselben Kurs absolvieren. Sitzplatzbeschränkungen für Klassenzimmer- und virtuelle Klassenzimmersitzungen werden jetzt auf Modulebene erzwungen, sodass ein Teilnehmer sich für einen Kurs anmelden kann, während er nur auf eine bestimmte Sitzung wartet. Weitere Informationen finden Sie unter [Adaptive Kurse - Autor](/help/migrated/authors/feature-summary/adaptive-course-author.md).

Wichtigste Funktionen:

* Sichtbarkeit auf Modulebene und Abschlussregeln pro Benutzergruppe
* ODER-Zusammenführungslogik: Wenn eine Gruppe ein Modul als obligatorisch definiert, ist es für diesen Teilnehmer obligatorisch.
* Warteliste auf Modulebene für Sitzungen im Schulungsraum und virtuellen Schulungsraum
* Der Abschluss der Aktualisierung wird ausgelöst, wenn sich das Profil eines Teilnehmers ändert
* Unterstützung für Lernpfade und Zertifizierungen mit dokumentierten Einschränkungen für wiederkehrende Zertifizierungen

Weitere Informationen zu adaptiven Kursen.

## Leistungsübersicht

Ein Schulungsbuch in Adobe Learning Manager fügt Kursen gewichtete Punktzahl hinzu, sodass Autoren jedem bewerteten Modul einen Beitragsprozentsatz zuweisen und eine zusammengefasste Mindestpunktzahl für den Kursabschluss festlegen können. Teilnehmer können ihre Noten während des Kurses verfolgen, und Administratoren können die Endergebnisse anzeigen und relevante Transkripte herunterladen.

### Was ist ein Notenbuch?

Ein mit einem Schulungsbuch kompatibler Kurs berechnet die Endpunktzahl jedes Teilnehmers, indem er einzelne Modulpunktzahlen entsprechend dem Gewichtungsprozentsatz kombiniert, der jedem Modul zugewiesen ist. Dies ist ein präzises, gewichtetes Maß für die Leistung und keine einfache Summe von Punktzahlen oder einer Pass-/Fail-Marke, die allein auf der Fertigstellung basiert.

Gradebook unterstützt zwei Abschlussmodelle:

* **Nur erforderliche Module**: Der Kurs wird abgeschlossen, wenn alle obligatorischen Module abgeschlossen sind. Notenbuchbewertungen werden weiterhin berechnet und sind sichtbar, aber die Gesamtpunktzahl trägt nicht zum Bestehen der Kriterien bei.

* **Erforderliche Module plus Aggregatwert**: Der Teilnehmer muss sowohl alle erforderlichen Module abschließen als auch eine Gesamtpunktzahl bei oder über dem Mindestwert zum Bestehen der Prüfung erreichen. Beide Bedingungen müssen erfüllt sein, um eine Mindestnote zu erreichen.

### Berechnung der Kurswerte

Für jedes bewertete Modul beträgt der Beitrag zum Gesamtwert des Kurses:

(Punktzahl erreicht ÷ Höchstpunktzahl) × Gewicht % = Modulanteil

Die Gesamtkursbewertung ist die Summe aller Modulbeiträge. Gewichtungsprozentsätze für alle bewertbaren Module müssen bis zu genau 100 betragen. Die Gradientenbuchanordnung kann erst gespeichert werden, wenn diese Bedingung erfüllt ist.

Die Gesamtkursbewertung ist die Summe aller Modulbeiträge. Gewichtungsprozentsätze für alle bewertbaren Module müssen bis zu genau 100 betragen. Die Gradientenbuchanordnung kann erst gespeichert werden, wenn diese Bedingung erfüllt ist.

Die Bewertungsskala muss nicht modulübergreifend konsistent sein. Eine Klassenzimmersitzung, die von 100 bewertet wird, und ein SCORM-Modul, das von 10 bewertet wird, können im selben Schulungsbuch zusammengeführt werden. Die Formel normalisiert jeden Beitrag, bevor die Gewichtung angewendet wird.

**Bewertungsfähige und nicht bewertbare Module**

Nur Module, die eine Bewertung erstellen, können gewichtet werden. Zu den Modultypen mit Bewertung gehören:

* SCORM-, AICC- und xAPI-Inhalte mit aktivierter Bewertung
* Captivate von Inhaltspaketen
* Native Quizze in Adobe Learning Manager
* Sitzungen mit Klassenzimmern und virtuellen Klassenzimmern, in denen der Kursleiter oder Administrator eine Punktzahl eingibt
* Aktivitätsmodule, die von einem Kursleiter oder Administrator bewertet wurden

Nicht bewertbare Modultypen, PDF-Dateien, Videodateien, Audiodateien, PowerPoint-Präsentationen, Word-Dokumente, Excel-Dateien und HTML-Inhalte können nicht mit einem Gewichtungsprozentsatz versehen werden und tragen nicht zur Gesamtpunktzahl bei. Diese Module sind möglicherweise noch für den Kursabschluss erforderlich. Wenn die Option Module einschließen, die keinen Beitrag zur Endnote leisten aktiviert ist, werden sie im Notenbuch ohne Gewichtungswert angezeigt.

Weitere Informationen finden Sie unter [Gradebook für Autoren](/help/migrated/authors/feature-summary/alm-author-gradebook.md).

## Hierarchische Inhaltsordner

Die Inhaltsbibliothek unterstützt jetzt bis zu drei Ebenen der Hierarchie privater Ordner. Administratoren erstellen die Ordnerstruktur und steuern, welche benutzerdefinierten Rollen auf welche Ordner der Ebene 1 zugreifen können. Der Zugriff kaskadiert automatisch auf alle Unterordner innerhalb eines Ordners der Ebene 1.

Autoren können Inhalte zwischen Ordnern kopieren und verschieben, die Inhaltsbibliothek nach Ordnern filtern und die Hierarchie durchsuchen, wenn sie einem Kurs Module hinzufügen.

Wichtigste Funktionen:

* Bis zu drei Verschachtelungsebenen (maximal 25 Unterordner pro übergeordnetem Element)
* Rollenbasierter Zugriff, nur zugewiesen auf Stufe 1
* Der Inhalt kann ohne Duplizierung in mehreren Ordnern angezeigt werden
* Öffentliche Ordner und private Ordnerstruktur schließen sich gegenseitig aus
* Ordnererlebnis bei der Auswahl von Modulen bei der Kurserstellung

Weitere Informationen zu Funktionen auf Administratorebene finden Sie unter [Ordner für hierarchische Inhalte](/help/migrated/administrators/feature-summary/settings/advanced-settings.md#content-folder). Weitere Informationen zu Funktionen auf Autorenebene finden Sie unter [Ordner für hierarchische Inhalte](/help/migrated/authors/feature-summary/content-library.md#add-content-to-a-folder).

## Live-Hub

Der Live Hub ist ein KI-gestütztes virtuelles Schulungserlebnis in Adobe Learning Manager, mit dem Unternehmen ansprechende und wirkungsvolle Live-Lernerlebnisse bereitstellen können. Mit intelligenten Funktionen wie KI-gestützten Umfragen, Breakout-Room-Orchestrierung, dauerhaften Lernumgebungen und KI-gestützter Unterstützung steigert Live Hub die Produktivität der Kursleiter und reduziert gleichzeitig die Komplexität der Sitzungsbereitstellung.

Wichtigste Highlights:

* Verbessern Sie das Live-Lernen mit einem nativen Adobe Learning Manager-Erlebnis, das die Lernqualität und die Lernergebnisse verbessert.
* Stellen Sie Ihren Kursleitern einen KI-gestützten Co-Moderator zur Verfügung, der die Interaktion durch intelligente Umfragen, Fragen-und-Antworten-Support und Erkenntnisse aus den Breakout-Räumen fördert.
* Helfen Sie Ihren Teilnehmern, mit KI-generierten Zusammenfassungen und nach Themen durchsuchbaren Sitzungsaufzeichnungen mehr aus jeder Sitzung zu erhalten.
* Mit Interaktionsanalysen, die über die Anwesenheit hinausgehen und echte Lernbeteiligung ermöglichen, messen Sie, worauf es ankommt.
* Unterstützen Sie Ihre Autoren bei der Verwendung des KI-gestützten Instructor Finder, um den richtigen Kursleiter nach Kompetenzen, Verfügbarkeit, bevorzugten Zeiten, Zeitzone und aktueller Nutzung abzugleichen.

## Komponentenbasierte E-Mail-Vorlage

Mit einem modernen WYSIWYG-Komponenten-Editor können Unternehmen jetzt E-Mail-Benachrichtigungen für Unternehmensanforderungen in Adobe Learning Manager erstellen. Administratoren können ein globales Layout einmal erstellen, mit einer wiederverwendbaren Kopf- und Fußzeile und Markenelementen, und es auf alle E-Mail-Vorlagen auf Kontoebene anwenden. Einzelne Vorlagen können dann auf Kurs- oder Instanzebene angepasst werden, wobei das übergeordnete Layout standardmäßig übernommen und nur bei Bedarf überschrieben wird.

Wichtigste Funktionen:

* WYSIWYG-Editor mit einer Bibliothek wiederverwendbarer Komponenten (Text, Bild, Schaltfläche, Trennlinie, Kopfzeile, Fußzeile)
* Variable Unterstützung: dynamische Felder wie den Namen des Teilnehmers, den Kursnamen und das Fälligkeitsdatum einfügen
* Verknüpfte und nicht verknüpfte Vorlagenhierarchie: Änderungen an einer verknüpften Vorlage werden auf alle untergeordneten Vorlagen übertragen. Nicht verknüpfte Vorlagen können unabhängig bearbeitet werden
* Unterstützung mehrsprachiger Vorlagen
* Vor der Veröffentlichung Vorschau anzeigen und testen - senden
* Abwärtskompatibilität: Bestehende E-Mail-Vorlagen funktionieren weiterhin

Weitere Informationen finden Sie unter [Komponentenbasierter E-Mail-Generator](/help/migrated/administrators/feature-summary/email-builder.md)

## Unterstützung für externes Lernen

Teilnehmer können jetzt plattformunabhängige Schulungen wie Zertifizierungen, Workshops, Konferenzen und externe Kurse direkt über ihr Teilnehmer-Dashboard zur Genehmigung durch den Manager einreichen. Genehmigte Einreichungen werden im Teilnehmertranskript angezeigt.

Wichtigste Funktionen:

* Konfigurierbares Einreichungsformular mit Standard- und benutzerdefinierten Feldern
* Manager-Workflow für Überprüfung und Genehmigung mit Kommentarunterstützung
* Genehmigte Einreichungen werden im Teilnehmertranskript mit vollständigen Metadaten angezeigt
* Der Administrator kann obligatorische Felder einschließlich benutzerdefinierter Felder konfigurieren.
* Neue Spalten in Admin- und Teilnehmertranskripten: Externer Lernname, Abschlusskommentar, benutzerdefinierte Feldspalten
* API-Unterstützung: fünf neue Endpunkte mit Teilnehmerbereich für das Erstellen, Abrufen und Aktualisieren von Einreichungen

Weitere Informationen auf Administratorebene finden Sie unter [Unterstützung für externes Lernen](/help/migrated/administrators/feature-summary/settings/basic-settings.md). Weitere Informationen auf Managerebene finden Sie unter [Unterstützung für externes Lernen](/help/migrated/managers/feature-summary/review-external-learning-requests.md). Weitere Informationen auf Teilnehmerebene finden Sie unter [Unterstützung für externes Lernen](/help/migrated/learners/feature-summary/submit-external-learning.md).

## KI-Funktionen

### KI-Assistent für Teilnehmende

Der AI-Assistent für Teilnehmer unterstützt jetzt vier neue Funktionen zusätzlich zum Beantworten von Fragen aus zugewiesenen Lerninhalten:

* **Kurszusammenfassungen**: mit dem Befehl / ein Katalogelement auswählen und eine Zusammenfassung generieren, ohne den Kurs zu öffnen
* **Lernobjektvergleich**: mit dem Befehl / bis zu zwei Lernobjekte auswählen und den Assistenten bitten, diese zu vergleichen
* **Antworten von Adobe Experience League**: Der Assistent bezieht jetzt Antworten auf Gewusst-wie-Fragen aus der Hilfedokumentation zu Adobe Learning Manager
* **Inhaltsabfragen von Drittanbietern**: Der Inhalt des Go1- und LinkedIn-Lernkatalogs kann abgefragt werden (nur Metadaten; nur Englisch; Die Aufnahme dauert 1-2 Stunden, nachdem der Katalog hinzugefügt wurde)

Weitere Informationen finden Sie unter [AI-Assistent für Teilnehmer](/help/migrated/learners/feature-summary/learner-ai-assistant.md).

### Learning Path-Agent

Teilnehmer können jetzt eine geführte Konversation mit dem AI-Assistenten führen, um einen benutzerdefinierten, sequenzierten Lernpfad basierend auf ihren Zielen, ihrem Hintergrund und der verfügbaren Zeit zu erstellen. Der Lernpfad wird automatisch erstellt und der Teilnehmer wird registriert.

Wichtigste Funktionen:

* Multiturn-Unterhaltungen führen den Teilnehmer durch Themenauswahl, Kursüberprüfung und Pfadbestätigung
* Bis zu fünf vorgeschlagene Lernthemen pro Unterhaltung
* Kursauswahl aus zugewiesenen Katalogen
* Maximal 10 personalisierte Lernpfade auf der Teilnehmer-Startseite
* Abgeschlossene Pfade können für Kollegen freigegeben werden

Weitere Informationen finden Sie unter [AI-Assistent für Teilnehmer](/help/migrated/learners/feature-summary/learning-path-agent.md).

### Agent für Einblicke

Der Insights Agent unterstützt Administratoren bei der Analyse von Lerndaten durch Abfragen in natürlicher Sprache. Stellen Sie Fragen zu Anmelde-Trends, Abschlussraten, Interaktionen mit Teilnehmern und Qualifikationslücken. Der Agent generiert Berichte und Visualisierungen als Reaktion.

Weitere Informationen finden Sie unter [Insights Agent](/help/migrated/administrators/feature-summary/insights-agent.md)

### Gen AI Credits

Adobe Learning Manager integriert KI-gestützte Funktionen, die über ein kreditbasiertes System verwaltet werden, das mit Agent Orchestrator-Lizenzen verknüpft ist. Bei diesem System müssen Administratoren Funktionen aktivieren, Kreditlimits festlegen und die Nutzung über die Abrechnungsseite überwachen. Die Verknüpfung des Adobe Learning Manager-Kontos mit einer Adobe Admin Console-Organisation mit einer aktiven Agent Orchestrator-Lizenz ist für die Aktivierung der Funktionen von Gen AI unerlässlich.

Weitere Informationen finden Sie unter [KI-Credits der Generation](/help/migrated/administrators/feature-summary/billing-management.md#genaicredits).

## Kanäle

Kanäle bieten eine zentralisierte Möglichkeit zum Organisieren, Veröffentlichen und Entdecken von Videoinhalten aus Web- und Confluence-Seiten. Administratoren können Kanäle erstellen und verwalten, indem sie unterstützte Webseiten oder Confluence-Seiten verbinden, Kanaleinstellungen konfigurieren, die Sichtbarkeit steuern und Inhalte aus der Quelle synchronisieren. Teilnehmer können verfügbare Kanäle durchsuchen, interessante Kanäle abonnieren und kuratierte Videoinhalte von einem einzigen Ort aus ansehen.

Weitere Informationen finden Sie unter [Kanäle erstellen](/help/migrated/administrators/feature-summary/create-channels.md).

## Berichtsgenerator

Report Builder bietet Administratoren ein flexibles Self-Service-Reporting-Tool, das über die in anderen Adobe Learning Manager verfügbaren festen Berichtstypen hinausgeht. Anstatt auf vordefinierte Berichtsstrukturen beschränkt zu sein, können Administratoren Felder aus mehreren Datensätzen, wie Benutzer, Benutzergruppen, Kurse und Lernpfade, Module, Transkript, Kataloge und mehr, zu einem einzigen benutzerdefinierten Bericht zusammenführen, der auf die spezifischen Datenanforderungen ihres Unternehmens zugeschnitten ist.

Berichte werden einmal erstellt und zur wiederholten Verwendung gespeichert. Es ist nicht erforderlich, Filter neu zu erstellen, Gruppierungen erneut anzuwenden oder Datensätze bei jedem Download erneut zu verknüpfen. Gespeicherte Berichte können nach Bedarf heruntergeladen, an andere Administratoren weitergegeben oder mit einem Abonnement eingerichtet werden, sodass Empfänger in regelmäßigen Abständen automatisch aktualisierte Berichte erhalten.

Weitere Informationen finden Sie unter [Report Builder](/help/migrated/administrators/feature-summary/alm-report-builder.md).

## Benutzerdefinierte Rollenänderungen

Benutzerdefinierte Administratoren können jetzt erweiterte Benutzerverwaltungsfunktionen über die erweiterte Berechtigungsebene unter Benutzer in einer benutzerdefinierten Rollendefinition erhalten.

Es stehen zwei Zugriffsebenen zur Verfügung:

| Zugriffsebene | Mögliche Aktionen des benutzerdefinierten Administrators |
|---|---|
| **Schreibgeschützt** | Alle benutzerdefinierten Rollen anzeigen, Protokolle importieren und Benutzer löschen Bericht über benutzerdefinierte Rollen herunterladen |
| **Vollständige Kontrolle** | Alle schreibgeschützten Funktionen plus: benutzerdefinierte Rollen erstellen, bearbeiten, löschen und zuweisen; Importieren von Benutzern über CSV gelöschte Benutzer bereinigen |

Weitere Informationen zu benutzerdefinierten Rollenänderungen. Weitere Informationen finden Sie unter [Was die erweiterte Benutzerberechtigung freigibt](/help/migrated/administrators/feature-summary/custom-role.md#whatadvanceduserpermissionunlocks)

## LTI-Deep-Linking

Integrationsadministratoren können jetzt LTI Deep Linking für LTI-Tool-Konfigurationen aktivieren, sodass Kursautoren Adobe Learning Manager-Kurse direkt über ein externes LMS durchsuchen und einbetten können, ohne die Kurs-URLs manuell zu kopieren.

Nach der Aktivierung wird den Autoren in der Konfiguration der externen LMS-Aktivität die Schaltfläche **Inhalt auswählen** angezeigt. Sie können genehmigte Kataloge durchsuchen, Kurse auswählen und die Auswahl bestätigen - wobei alle Felder automatisch ausgefüllt werden.

Weitere Informationen finden Sie unter [LTI-Deep Links](/help/migrated/integration-admin/feature-summary/lti-deep-links.md).

## Standorte für Klassenzimmer

Standorte für Klassenzimmer unterstützen jetzt ein strukturiertes **Standortformat für vier Felder**, einschließlich Land, Bundesland/Provinz/Region, Stadt und Ortsname, wodurch die Verwaltung und Organisation von Schulungsstandorten in verschiedenen Regionen vereinfacht wird. Das Update enthält eine einmalige Migration vom älteren Einzelfeldformat und fügt mehrsprachige Unterstützung für die Felder **Name des Speicherorts** und **Rauminformationen** hinzu, wodurch lokalisierte Klassenzimmerdetails für Teilnehmer aktiviert werden.

Weitere Informationen finden Sie unter [Standorte für Klassenzimmer](/help/migrated/administrators/feature-summary/classroom.md).

## Demnächst verfügbar: Adobe Learning Manager Content Composer

Adobe Learning Manager Content Composer ist ein anstehendes KI-Kurs-Authoring-Tool in Adobe Learning Manager, mit dem Sie in kürzester Zeit einen Kurs erstellen können, der für die Veröffentlichung bereit ist.

## Melden von Änderungen in der Version

Erfahren Sie mehr über die [Berichterstellungsänderungen in der Version August 2026 von Adobe Learning Manager](/help/migrated/reporting-changes-august-2026.md).

## API-Änderungen in der Version

Erfahren Sie mehr über die [API-Änderungen in der Version August 2026 von Adobe Learning Manager](/help/migrated/api-changes-august-2026.md).

## Weitere Verbesserungen in der Version

| Verbesserungen | Beschreibung |
|---|---|
| **MQA: Neueste vs. höchste Punktzahl** | Bei Modulen mit mehreren Versuchen können Autoren jetzt auswählen, ob die Punktzahl für den neuesten oder höchsten Versuch im Teilnehmertranskript aufgezeichnet und in Gradebook-Berechnungen verwendet wird. Latest war die vorhandene Standardeinstellung und bleibt es auch, wenn die Einstellung nicht konfiguriert ist. Weitere Informationen finden Sie unter [Gradebook für Autoren](/help/migrated/authors/feature-summary/alm-author-gradebook.md#configurescoresettingsmultipleattempts). |
| **Inhaltsvorschau in der Inhaltsbibliothek** | Autoren können jetzt eine Vorschau der hochgeladenen Inhaltsdateien direkt in der Inhaltsbibliothek anzeigen, bevor sie sie zu Kursen hinzufügen. Weitere Informationen finden Sie unter [Inhaltsbibliothek in der Vorschau anzeigen](/help/migrated/authors/feature-summary/content-library.md#previewcontentlibrary). |
| **Inkrementeller Benutzerbericht** | Ein neuer API-basierter Benutzerbericht gibt nur Benutzer zurück, die seit der letzten Anforderung erstellt oder geändert wurden. Dadurch wird die Datenübertragung für große Konten mithilfe automatisierter Workflows für die Benutzersynchronisation reduziert. Weitere Informationen finden Sie unter [Inkrementeller Benutzerbericht](/help/migrated/incremental-user-report.md). |
| **11 neue Sprachen im Fluidic Player** | Der Fluidic Player unterstützt jetzt 11 zusätzliche Sprachen, einschließlich Rechts-nach-Links-Skriptunterstützung (RTL). Weitere Informationen finden Sie unter [Fluidic Player](/help/migrated/learners/feature-summary/fluidic-player.md). |
| **LTI-Modulmigration** | Vorhandene LTI 1.1-Module können jetzt mit dem Migrations-Tool auf LTI 1.3 migriert werden. Weitere Informationen finden Sie unter [LTI-Migration von Modulen](/help/migrated/integration-admin/feature-summary/migration-manual.md#migrationofltimodules). |
| **E-Mail-Generator: Unterstützung für Rich-Text-Editor** | E-Mail-Vorlagen in Adobe Learning Manager unterstützen jetzt Rich-Text-Formatierung, Anhänge und benutzerdefinierte Automatisierungen. Weitere Informationen finden Sie unter [Email Builder](/help/migrated/administrators/feature-summary/email-builder.md). |
| **E-Mail-Generator: Vorschaufunktion** | Sie können die E-Mail-Komposition überprüfen, um zu sehen, wie sie am Ende des Empfängers aussieht, indem Sie die Option Vorschau verwenden. Weitere Informationen finden Sie unter [Email Builder](/help/migrated/administrators/feature-summary/email-builder.md). |
| **Standardisierung des Webhook-Zeitstempels** | Für alle Datums- und Zeitfelder im `data`-Objekt der Webhook-Payloads sind jetzt Sekunden auf `00` festgelegt, sodass die Genauigkeit der Minutenebene mit den Teilnehmertranskriptberichten übereinstimmt. |
| **Verbesserungen der Verbindung** | Connector-Updates für Azure Data Lake Storage (ADLS) Dauerhafte Raumnamenunterstützung für wiederkehrende virtuelle Klassenzimmersitzungen; Anwesenheitsverfolgung in der Aufnahmeansicht. |
| **Verbesserungen der Player-Leistung** | Der Fluidic Course Player wurde für schnellere Ladezeiten und sanftere Übergänge zwischen den Modulen optimiert. |
| **Auswirkungswarnung vor dem Aussetzen von Kursen/LPs** | Administratoren sehen jetzt eine Warnung, in der alle aktiven Registrierungen und abhängigen Lernpfade aufgelistet werden, bevor ein Kurs oder Lernpfad eingestellt werden kann. |
| **CR/VC-Modul: Erwartete Dauer** | Autoren können jetzt die erwartete Dauer für Klassenzimmer- und virtuelle Klassenzimmermodule separat von der geplanten Sitzungszeit festlegen. Dieser Wert wird in Berichten und Kursinformationen zu Teilnehmern angezeigt. |
| **Bestätigung vor der Bearbeitung erworbener Kurse** | Administratoren in Peer-Konten sehen jetzt ein Bestätigungsdialogfeld, bevor sie einen Kurs bearbeiten, der über die Katalogfreigabe erworben wurde, um unbeabsichtigte Änderungen an freigegebenen Inhalten zu verhindern. |
| **Sitzungs-URL mit Instanz-ID** | Die URLs zum Starten von Sitzungen für Microsoft Teams-, Adobe Connect- und Zoom-Sitzungen enthalten jetzt die Instanz-ID, sodass Teilnehmer an die richtige Sitzung weitergeleitet werden, wenn mehrere Instanzen vorhanden sind. |
| **Warnung für Ankündigungen mit großen Zielgruppen** | Beim Senden einer Ad-hoc-Ankündigungs-E-Mail an mehr als einen konfigurierbaren Schwellenwert für Empfänger sehen Administratoren jetzt vor dem Senden eine Volumenwarnung. |
| **E-Mail-Vorlagen: Konto-URL für externe Teilnehmer** | Vorlagen für E-Mail-Benachrichtigungen können jetzt eine separate Konto-URL speziell für externe Teilnehmer enthalten, über die sie an das richtige Anmeldeerlebnis weitergeleitet werden. |
| **AEM Sites** | Es gibt jetzt nur eine **Schaltfläche** in **Ihrem Profil** > Ihre Interessensbereiche, um Ihre Voreinstellungen für Produkte und Rollen und Kenntnisse zu bearbeiten. Dies ist auch Teil des nativen Lern-Managers. |
| **AEM Sites** | Früher gab es zwei **Bearbeiten**-Schaltflächen, aber jetzt ist die **Bearbeiten**-Schaltfläche eine konsolidierte Schaltfläche, um Ihre Voreinstellungen für Produkte und Rollen und Kenntnisse zu ändern. |
| **Zeitzone** | Ein neues Suchfeld wurde direkt unter dem Feld Zeitzone in den Profileinstellungen des angemeldeten Benutzers hinzugefügt. Das Suchfeld kann verwendet werden, um direkt nach einer Zeitzone zu suchen, anstatt durch die gesamte Liste der verfügbaren Zeitzonen zu scrollen. Wenn Sie die vorhandene Zeitzone ändern möchten, wählen Sie eine neue Zeitzone aus und klicken Sie auf Speichern. Die neue Zeitzone wird gespeichert. Die Schaltfläche Speichern wird nur angezeigt, wenn Sie eine Zeitzone auswählen. |

## Systemanforderungen

[Systemanforderungen für Adobe Learning Manager anzeigen](/help/migrated/system-requirements.md).

## Versionshinweise

Lesen Sie die [Versionshinweise](/help/migrated/release-note/release-notes.md) für die neuesten Versionsupdates.

## Frühere Versionen von Adobe Learning Manager

* [Adobe Learning Manager Version April 2026](/help/migrated/whats-new-april-2026.md)
* [Adobe Learning Manager Version Oktober 2025](/help/migrated/whats-new-october-2025.md)

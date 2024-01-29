---
title: Neue Funktionen in dieser Version (November 2022)
description: Erfahren Sie mehr über die neuen Funktionen und Verbesserungen im Adobe-Lernmanager
hidefromtoc: true
source-git-commit: 1da0911a4d0c2ae5cb01bbb2b7955675b0dfcdde
workflow-type: tm+mt
source-wordcount: '1994'
ht-degree: 0%

---

# Neue Funktionen in dieser Version (November 2022)

<!--
IN-PROGRESS

<https://helpx.adobe.com/learning-manager/whats-new-nov-2022.html>
-->

## Konfiguration mehrerer SSO

Adobe Learning Manager unterstützt derzeit eine Anmeldemethode für interne und eine Anmeldemethode für externe Benutzer. Dies führt zu Einschränkungen in Fällen, in denen Kunden ihre Mitarbeiter und ihre eigenen Kunden und Vertriebspartner im gleichen Konto haben.

Mit der Absicht, mehrere Arten von Benutzergruppen zu unterstützen, die sich bei der Plattform anmelden, unterstützt Adobe Learning Manager jetzt mehrere Anmeldemethoden über mehrere SSO-Konfigurationen sowohl für interne als auch für externe Benutzer.

Weitere Informationen finden Sie unter [Mehrere SSO-Anmeldungen](/help/migrated/administrators/feature-summary/multiple-sso-logins.md).

## Unterstützung für nicht angemeldete Funktionen

Das native Portal des Adobe Learning Managers unterstützt jetzt nicht angemeldete Zugriffe auf ein Schulungsportal.

Die Teilnehmer können sich jetzt auf der Schulungsseite informieren und darauf zugreifen, verschiedene verfügbare Kurse und Inhalte auschecken und sich anmelden, um die Kurse zu nutzen.

Diese Funktion erleichtert die Erstellung eines kundenseitigen Lernportals, in dem Teilnehmer verschiedene Kurse durchsuchen können, ohne sich zunächst anmelden zu müssen.

Weitere Informationen finden Sie unter [Nicht angemeldete Benutzer für Teilnehmer](/help/migrated/administrators/feature-summary/non-logged-in-experience-learners.md).

## Verbesserungen der Schulungsübersichtsseite

Auf der Seite Schulungsübersicht wird jetzt eine aktualisierte Benutzeroberfläche angezeigt, sodass die Teilnehmer während der Bearbeitung eines Kurses über ein verbessertes Benutzererlebnis verfügen.

Weitere Verbesserungen:

* Versehen Sie eine Schulung mit einem Lesezeichen.
* Empfehlung verwandter Kurse.
* Lernpfadinformationen für Kurse und Lernpfade.
* Klickbare Autorennamen.
* Breadcrumbs für einfachere Navigation.

## Verbesserungen der Schulungsübersichtsseite

Auf der Seite Schulungsübersicht wird jetzt eine aktualisierte Benutzeroberfläche angezeigt, sodass die Teilnehmer während der Bearbeitung eines Kurses über ein verbessertes Benutzererlebnis verfügen.

Weitere Verbesserungen:

* Versehen Sie eine Schulung mit einem Lesezeichen.
* Empfehlung verwandter Kurse.
* Lernpfadinformationen für Kurse und Lernpfade.
* Klickbare Autorennamen.
* Breadcrumbs für einfachere Navigation.

## Autorenprofilseite

Auf der Seite mit dem Autorenprofil werden alle Schulungen angezeigt, die von einem bestimmten Autor erstellt werden.

Teilnehmer können autorenspezifische Informationen und alle vom Autor erstellten Schulungen leicht finden.

## Mit Lesezeichen versehene Schulungen

Teilnehmer können Schulungen speichern (über die Schaltfläche &quot;Speichern&quot;) oder ein Lesezeichen dafür über die Kurskachel oder die Übersichtsseite einfügen. Alle mit einem Lesezeichen versehenen Kurse sind auf der Teilnehmer-Startseite verfügbar.

## Player-Anpassung

In dieser Version können Sie den Fluidic Player an die Branding-Anforderungen eines Kurses anpassen.

Sie können verschiedene Player-Einstellungen und -Optionen je nach Inhaltsanforderung ein- und ausblenden und Teilnehmern basierend auf dem Inhaltstyp die Kontrolle gewähren. Sie können diese Änderung sowohl auf native als auch auf Headless-Implementierungen anwenden.

Folgende Optionen können geändert werden:

* Umschalten des Inhaltsverzeichnisses
* Hinweise
* Sprache
* Geschwindigkeit
* Beschriftung
* Lautstärke
* Steuerelemente für die Wiedergabe

## Identitätswechsel des Teilnehmers und Managers

Administratoren können eine Sitzung starten, für die sie die Identität eines beliebigen Benutzers in ihrem Konto in der Teilnehmer- und Managerrolle übernehmen können.

Weitere Informationen finden Sie unter [Identitätswechsel des Teilnehmers und Managers](/help/migrated/administrators/feature-summary/impersonation-learner-manager.md).

## Weitere Verbesserungen

### Überwachungsprotokoll von E-Mails

Administratoren können jetzt über einen Bericht zum E-Mail-Prüfprotokoll auf alle vom System gesendeten E-Mail-Protokolle zugreifen.

Dieses Protokoll erfasst alle Daten in Bezug auf E-Mails, die in den letzten 30 Tagen gesendet wurden, und wird täglich aktualisiert. Darüber hinaus enthält der Bericht Informationen wie den Status der zugestellten Datei, den Absender, den Empfänger, den Betreff und Inhaltsmetadaten.

Laden Sie den Bericht unter Berichte > Benutzerdefinierte Berichte > Excel-Berichte > E-Mail-Bericht herunter. Eine Benachrichtigung wird angezeigt, über die Sie den Bericht herunterladen können.

Dieser Bericht enthält die folgenden Felder:

* Trigger-Zeit für E-Mails (UTC TimeZone)
* Zeit des letzten Ereignisstatus (UTC-Zeitzone)
* Lieferstatus
* Empfänger-E-Mail
* Benutzer-ID des Absenders
* Email Subject
* Entitätstyp
* Name der Entität
* Entitäts-ID

### Benachrichtigung der Teilnehmer auf Warteliste

Wenn ein Autor eine neue Instanz hinzufügt, kann der Autor eine E-Mail auslösen, um Teilnehmer auf der Warteliste über andere Instanzen zu benachrichtigen. Die Teilnehmer erhalten eine E-Mail der Änderung.

### E-Mail-Vorlagen auf Instanzebene

Sie können E-Mails für jede Instanz einer Schulung anpassen.

Überall dort, wo der Autor oder Administrator eine neue Instanz hinzufügen kann, kann die Vorlage für eine einzelne Instanz bearbeitet werden.

Wenn ein Kurs beispielsweise unterschiedliche Zielgruppentypen hat, können Sie die E-Mail-Vorlage entsprechend ändern.

![E-Mail-Vorlagen](assets/email-template.png)

Die Priorität der Vorlage ist unten aufgeführt:

1. Vorlage auf Instanzebene
2. Vorlage für Schulungsstufen
3. Vorlage auf Kontoebene

### Kursleiterkommentare beim Annehmen von Einreichungen

Kursleiter können jetzt Kommentare hinzufügen, während sie die von den Teilnehmern eingereichten Beiträge akzeptieren. Der Teilnehmer erhält eine E-Mail-Benachrichtigung und eine In-App-Benachrichtigung (sofern aktiviert), sobald die Einreichung vom Kursleiter genehmigt wurde. Die übermittlungsbezogenen Kommentare sind in den Teilnehmertranskripten sowohl für den Administrator als auch für die Teilnehmer vorhanden.

### Verbesserte Suchfunktionen

Der aktuelle Suchverlauf eines Teilnehmers wird angezeigt, damit er alle früheren Suchvorgänge anzeigen kann.

Die Suchergebnisse sind jetzt konsistent über das gesamte formelle und informelle Lernen (soziales Lernen) hinweg. Die Ergebnisse umfassen Schulungen, soziales Lernen und Matches auf dem Marktplatz für Inhalte.

Die Suche ist fokussierter und zielgerichteter, wo Sie die Suchergebnisse an drei Stellen anzeigen können: formales Lernen, soziales Lernen und Inhalts-Marketplace.

![Recherche](assets/search-image.png)

#### Ausdrucksgesteuerte Suche

In dieser Version von Adobe Learning Manager haben wir die Typeahead-Suche durch die Phrasenbasierte Suche ersetzt.

#### Zuletzt verwendete Suchvorgänge

Ein Teilnehmer kann seine zuletzt durchgeführten Suchvorgänge nur in der aktuellen Sitzung anzeigen.

### Katalog für kostenlose Kurse für Content Marketplace

Auf dem Inhalts-Marketplace für Teilnehmer steht jetzt ein Satz von kuratierten, hochwertigen, kostenlosen Katalogen mit 50 kostenlosen Kursen sofort zur Verfügung.

### Unterstützung für die indonesische Sprache

Bahasa Indonesia wurde jetzt als Benutzeroberflächensprache in den Teilnehmer- und Manager-Apps hinzugefügt.

### Pflichtfeld &quot;Autor&quot;

Beim Erstellen eines Kurses ist das Feld &quot;Autor&quot; obligatorisch.

### Änderungen am Content Marketplace

* Neu erstellte Testkonten listen einen neuen Katalog für 50 kostenlose Kurse im Inhalts-Marketplace auf, die für Benutzer verfügbar sind.
* Ein Teilnehmer kann jetzt die Anzahl der Suchergebnisse sehen und eingebettete Links verknüpfen, um zum Inhalts-Marketplace weitergeleitet zu werden.

### Immersive Änderungen für Mobilgeräte

In dieser Version können immersive mobile Webbenutzer die unten aufgeführten Aufgaben ausführen:

* Erstellen - Abstimmungsposten
* Beitrag bearbeiten - alle Typen, RTE
* E-Commerce-Workflow.
* Vorschau eines Moduls: Teilnehmer verfügen über die Modulvorschau-Funktion in der immersiven Mobilanwendung. Diese Änderung ermöglicht es Teilnehmern, vor der Registrierung für einen Kurs eine Vorschau des Moduls anzuzeigen.
* Kopieren Sie eine URL.
* Löschen Sie ein Board.

### Änderungen am Zoom-Connector

Der JWT-App-Typ wird im Juni 2023 veraltet sein. Es wird empfohlen, dass Sie Server-zu-Server-OAuth- oder OAuth-Apps erstellen, um die Funktionalität einer JWT-App in Ihrem Konto zu ersetzen.

### Bericht für Gamification

In dieser Version erhalten Sie Zugriff auf einen Bericht, der verschiedene Kurse anzeigt, in denen Gamification aktiviert wurde.

### Sprachvoreinstellung über CSV importieren

Beim Importieren einer CSV-Datei enthält die CSV-Datei die Felder &quot;Interface Language&quot;, &quot;Content Language&quot; und &quot;Time Zone&quot;.

Der Administrator kann auch den Bericht exportieren, der die gleichen Felder wie oben enthält.

* Benutzeroberflächensprache
* Inhaltssprache
* Zeitzone

Neben Administratoren kann ein benutzerdefinierter Administrator diesen Bericht auch exportieren.

![Sprachenbericht](assets/language-report.png)

#### Auswirkungen auf die Lokalisierung

* Die Spaltennamen können nicht lokalisiert werden und müssen unverändert sein (Schnittstellensprache, Inhaltssprache, Zeitzone).
* Bei den Gebietsschemacodes wird nicht zwischen Groß- und Kleinschreibung unterschieden.
* Obwohl es keine Einschränkung für die Angabe des Ländercodes gibt, können Sie nur den Sprachcode angeben. Zum Beispiel sind sowohl &quot;it_IT&quot; als auch &quot;it&quot; gültig.
* Wenn der Bericht aufgrund eines falschen Gebietsschemacodes Diskrepanzen enthält, wird die CSV-Verarbeitung wie gewohnt fortgesetzt und wirkt sich nicht auf die anderen Datensätze in der CSV-Datei aus. Die Gebietsschemaeinstellung des Benutzers mit einem falschen Gebietsschema wird nicht aktualisiert. Der Rest der Daten wird aktualisiert.

## API-Änderungen und Verbesserungen

### VC-Anschlüsse

Wenn eine Administrator-E-Mail-ID zum Konfigurieren des VC-Connectors verwendet wird, muss dieser bestimmte Administrator über die Berechtigung für Folgendes verfügen:

* Erstellen eines Meetings
* Aktualisieren eines Meetings
* Anwesenheitsbericht wird abgerufen

Beim Erstellen oder Aktualisieren des VC-Meetings müssen die Kursleiter das Meeting innerhalb von 30 Minuten nach der geplanten Endzeit des Meetings BEENDEN.

### Lesezeichen

Die folgenden APIs werden hinzugefügt, um einen Kurs auf der Seite Schulungsübersicht mit einem Lesezeichen zu versehen:

* Alle Lesezeichen abrufen: `primeapi/v2/bookmarks`
* Erstellen eines Lesezeichens: `primeapi/v2/learningObjects/{id}/bookmark`
* Lesezeichen löschen: `primeapi/v2/learningObjects/{id}/bookmark`

### Unterstützung von Metadaten und Inhalten mit mehreren Gebietsschemas durch Migration

Für alle Arten von Schulungen, die auf der Plattform unterstützt werden (Kurse, Lernpfade, Module, Zertifizierungen und Arbeitshilfen), kann die Migration mehrerer Sprachen jetzt über CSV-Dateien unterstützt werden, wobei zusätzliche Spalten für zusätzliche Sprachen verwendet werden.

#### Voraussetzungen

Erstellen Sie das Migrationsprojekt als Integrations-Admin und geben Sie dann die migrationProjectId für das ALM-Support-Team frei, damit das Flag &quot;Multi-Locale&quot; vom Backend aus aktiviert werden kann.

#### Gültigkeitsbereich von Migrationsobjekten mit mehreren Gebietsschemas

* Modul
* Kurs
* Modulversion
* Zertifizierung
* Lernprogramm
* Arbeitshilfe
* Version der Arbeitshilfe

#### CSV-Spezifikation

Der Adobe Learning Manager bietet Ihnen eine Reihe von CSV-Standardspezifikationen für die Migration, die für mehrere Gebietsschemas aktiviert ist. Es empfiehlt sich, diese CSV-Spezifikationen vor Beginn des Migrationsvorgangs durchzugehen. Der Integrationsadministrator Ihres Unternehmens kann die vorhandenen Datenformate analysieren und den entsprechenden vom Learning Manager bereitgestellten CSV-Vorlagenelementen zuordnen.

#### Änderungen mit Unterstützung mehrerer Gebietsschemas

* Die Spalte &quot;module_version&quot; wird in &quot;module_version.csv&quot; und &quot;course_module.csv&quot; nicht unterstützt.
* Die Version &quot;module_version&quot; kann nicht im selben Run aktualisiert werden (in demselben Run kann das Modul nicht mit zwei Versionen mit demselben Modul migriert werden).
* Die Aktualisierung von Inhalten oder Metadaten wird als Modulversionsupdate von module_version.csv betrachtet.
* Das Update &quot;Job_Aid_Version&quot; kann nicht über job_aid_version.csv unterstützt werden

### Authentifizierungstoken und Cookies widerrufen

Eine Headless-LMS-Anwendung erhält bei der ersten Anmeldung das refresh_token . Anschließend wird das refresh_token zum Generieren des access_token für seine Clientanwendungen zum Durchführen von API-Aufrufen verwendet. In ähnlicher Weise verwendet die Inhaltswiedergabe den OAuth-Endpunkt zum Generieren von Cookies für die Verwaltung der Wiedergabe, die mehrere Inhaltsdateien und API-Aufrufe umfasst, die von diesen Dateien mithilfe von Cookies aufgerufen werden. Das Cookie, das von oauth generiert wird, hat die gleiche Gültigkeit wie das access_token, die sieben Tage beträgt. Sobald das Cookie generiert ist, gibt es keine Möglichkeit, es anders als bei der typischen Abmeldung von Webanwendungen zu löschen. Das OAuth-Cookie und das Webanwendungs-Cookie sind zwei unterschiedliche Cookies, die einander nicht kennen.

Zum Löschen des Cookies haben wir einen neuen Endpunkt eingeführt, der &quot;refresh_token&quot;, &quot;cookie&quot; und &quot;cookie&quot; sowie das Aktualisierungstoken widerruft.

**Details**

**Endpunkt**

`POST oauth/o/revoke`

**Abfrageparameter**

* `cookie=true|false` - weist darauf hin, dass Cookie widerrufen werden muss
* `refresh_token=true|false` - zeigt an, dass die Aktualisierung

**Textkörper anfordern**

Body erforderlich für das Widerrufen von refresh_token oder (refresh_token und Cookie)

```
{
      "client_id": <>,
      "client_secret": <>,
      "refresh_token": <>
}
Body required for revoking oauth cookie only
{
      "access_token": <>
}
```

### APIs veröffentlicht

In dieser Version haben wir einige APIs veröffentlicht.

| API | Typ | Beschreibung |
|---|---|---|
| /social/search | GET | In Social Media suchen. |
| /Ankündigungen | GET | Rufen Sie detaillierte Informationen zur Ankündigung auf dem Mastertitel ab, der dem Teilnehmer zugewiesen ist. |
| /Ankündigungen/`{id}` | GET | Rufen Sie detaillierte Informationen zur Ankündigung auf dem Mastertitel ab, der dem Teilnehmer zugewiesen ist. |
| /learningObjects/`{id}`/loResources/{loResourcesId} | GET | Laden Sie die URL der Datei für loResource vom Typ &#39;Aktivität&#39; hoch, wenn die Dateiübermittlung erforderlich ist. |
| /jobAid/`{jobAidId}`/jobAidDownloaded | GET | Bericht zum Herunterladen der Arbeitshilfe festlegen |
| /bulkimport/startrun | POST | Führen Sie den Massenimport aus. |
| /bulkimport/cansync | GET | Synchronisierung des Massenimport. |
| /search | GET | DELETEMEBOB |
| /uploadInfo | GET | Informationen zu Inhaltsaktualisierungen abrufen. |
| /uploadSigner | GET | Unterschrift des To_Sign-Inhalts einholen |
| /avatar | POST | Aktualisiert das Avatarbild des Teilnehmers mit einem neuen Bild. |
| /avatar | DELETE | Löscht das Avatarbild des Teilnehmers. |

### Salesforce-App

Die **Höhere Reihenfolgen-LO ignorieren** muss in der Salesforce-App aktiviert sein, damit alle Kurse, Lernprogramme und Zertifikate gleichzeitig angezeigt werden können.

### APIs zur Player-Anpassung

In dieser Version haben wir APIs bereitgestellt, um einen Player anzupassen. Sie haben folgende Möglichkeiten:

* Starten oder laden Sie den Player.
* Navigieren Sie zu einem bestimmten Modul.
* Inhaltsverzeichnis ein-/ausschalten.
* Ändern Sie die Sprache.
* Schließen Sie den Player.
* Sie können die Wiedergabe, Pause, Vorwärts- oder Rückwärtswiedergabe, die Suche, die Lautstärke oder die Geschwindigkeit ändern.
* Vom Player ausgegebene Ereignisse erfassen.

### Anzeigen der Wartelistenposition eines Teilnehmers

Die GET /enrollments/{id}/waitlistPosition API ruft unter der LO-API die Wartelistenposition eines Benutzers für eine angegebene Registrierung ab.

### Abschlussdatum Einreichung in externen Zertifizierungen

Die /primeapi/v2/learningObjects/certification:xxxxx-API verfügt über das Attribut &quot;completeDateSameAsApprovalDate&quot;, um anzugeben, dass für das Zertifikat &quot;Abschlussdatum der Zertifizierung&quot; für den Teilnehmer aktiviert ist oder nicht, zusammen mit dem Flag &quot;true/false&quot;.

### LO-Vorschaudaten abrufen

Die GET /preview/learningObjects/{id} API wird hinzugefügt, um Vorschauinformationen zu einem Lernobjekt abzurufen.

### Externe Benutzer innerhalb von Profilen verschieben

Die `PUT primeapi/v2/externalProfiles/{currentep}/users/{userid}?` hilft, einen Benutzer zu einem anderen externen Profil zu verschieben, indem eine neue externalProfile-ID angegeben wird.

### Benutzer zu externen Profilen hinzufügen

Die `POST /externalProfiles/{id}/users` fügt externe Benutzer dem externen Profil hinzu.

## Versionshinweise

Weitere Informationen zu aktuellen und früheren Versionen der Learning Manager-Webanwendung und -Geräte-App finden Sie unter [Versionshinweise](/help/migrated/release-note/release-notes.md).

## Fehlerbehebungen

Um die Fehler anzuzeigen, die in diesem Update behoben wurden, lesen Sie die [Liste der behobenen Fehler](release-note/release-notes.md#bugs-fixed-in-this-release).

## Systemanforderungen

[Systemanforderungen für Learning Manager](/help/migrated/system-requirements.md)

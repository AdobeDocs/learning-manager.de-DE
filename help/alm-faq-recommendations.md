---
title: Lebenszyklus des Administratorkontos für Adobe Learning Manager
description: Dieses Dokument enthält einen umfassenden Überblick über die Sicherheitskontoverwaltung, Konfiguration und Compliance-Funktionen von Adobe Learning Manager (ALM), die den FedRAMP-Empfehlungen entsprechen.
jcr-language: en-us
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '1706'
ht-degree: 0%
---

# Adobe Learning Manager-Sicherheitsempfehlungen

## Welche sicherheitsrelevanten Einstellungen können nur von benutzerdefinierten Administratoren oder Integrationsadministratoren in Adobe Learning Manager verwendet werden und welche Auswirkungen haben sie auf die Sicherheit?

Die beiden privilegierten Kontotypen von Adobe Learning Manager - &quot;Benutzerdefinierter Administrator&quot; und &quot;Integrationsadministrator&quot; - verfügen jeweils über eine definierte Reihe sicherheitsrelevanter Einstellungen mit dokumentierten Auswirkungen.

### Benutzerdefinierter Administrator: was sie bedienen können:

* Benutzerdefinierte Rollen werden vom vollständigen Administrator unter ALM-Admin > Benutzer > Benutzerdefinierte Rollen konfiguriert. Einem benutzerdefinierten Administrator kann Zugriff auf eine oder mehrere dieser Berechtigungskategorien gewährt werden: Kontoberechtigungen (Ankündigungen, Gamification, Kenntnisse, Benutzerverwaltung), Funktionsberechtigungen (Kataloge, Berichte, Tags) und Lernobjektberechtigungen (Kurse, Zertifizierungen, Lernpfade).
* &quot;Umfang&quot; ist die sicherheitsempfindlichste Einstellung: Eine benutzerdefinierte Rolle kann auf bestimmte Benutzergruppen und/oder bestimmte Kataloge beschränkt werden. Ohne Bereichseinschränkungen hat eine benutzerdefinierte Rolle plattformweiten Zugriff auf die zugewiesenen Funktionen, sodass sie der Stellfläche eines vollständigen Administrators entspricht.
* Wenn einer benutzerdefinierten Rolle unter &quot;Kontoberechtigungen&quot; der Zugriff auf Einstellungen gewährt wird, kann dieser benutzerdefinierte Administrator Anmeldemethoden, Benachrichtigungseinstellungen und Konfigurationen auf Kontoebene ändern. Dies ist eine Berechtigung mit hoher Auswirkung, die nur mit expliziter geschäftlicher Begründung gewährt werden sollte.
* Ein benutzerdefinierter Administrator mit Einstellungszugriff, der auch über Entitätszugriff für Benutzer verfügt, kann sich selbst die vollständige Administratorrolle zuweisen und effektiv zur vollständigen Administratorsteuerung eskalieren.

### Integrationsadministrator: was sie bedienen können:

* Integrationsadministratoren verwalten OAuth 2.0-Anwendungsregistrierungen unter Integrationsadministrator > Anwendungen > Registrieren. Sie wählen einen von sechs OAuth-Geltungsbereichen aus, die vom Lese-/Schreibzugriff für Teilnehmer bis hin zum Lese-/Schreibzugriff für die Administratorrolle reichen. Der Lese-/Schreibbereich des Administrators gewährt der registrierten Anwendung dieselben Berechtigungen wie einem vollständigen Administrator über die API.
* Die für die Integration zuständigen Administratoren konfigurieren FTP, SFTP, Salesforce, Workday und andere Verbindungen, mit denen Benutzerdatensätze, Rollenzuweisungen und Kursabschlüsse importiert und Plattformdaten in externe Systeme exportiert werden.
* OAuth-Geltungsbereich für registrierte Anwendungen: Mindestumfang. Gewähren Sie niemals Lese-/Schreibzugriff für die Administratorrolle, es sei denn, dies ist unbedingt erforderlich.
* Integrationsadministratoren konfigurieren WebHooks, die ALM-Ereignisdaten in Echtzeit (Registrierungen, Abschlüsse, Rollenänderungen) an externe URLs übertragen. Ein beschädigter oder falsch konfigurierter Webhook-Endpunkt ist ein Datenexfiltrationsrisiko.
* Integrationsadministratoren können LTI-Integrationen konfigurieren. Nach der Aktivierung kann LTI nicht mehr deaktiviert werden. Gelegt LTI-Anmeldedaten erlauben nicht autorisierten Zugriff auf Kursinhalte von externen LMS-Plattformen.


## Welche Sicherheitsstandards werden für Verwaltungs- und privilegierte Konten der obersten Ebene in Adobe Learning Manager empfohlen und wo werden sie konfiguriert?

### Standardwerte für Administratorkonten auf oberster Ebene (bei der ersten Bereitstellung konfiguriert):

* Anmeldemethode für interne Benutzer: Single Sign-on (SSO) über SAML 2.0: konfiguriert unter ALM-Admin > Einstellungen > Anmeldemethoden. Verwenden Sie Adobe ID nicht für Mitarbeiter oder Administratoren.
* Zweistufige Verifizierung (2FA): Für alle Benutzer erzwingen: konfiguriert unter Adobe Admin Console > Einstellungen > Datenschutz und Sicherheit > Authentifizierungseinstellungen.
* Max. Sitzungsdauer: 8 Stunden (oder pro Organisationsrichtlinie): konfiguriert unter Adobe Admin Console > Einstellungen > Datenschutz und Sicherheit > Erweiterte Einstellungen.
* Max. Leerlaufzeit: 30 Minuten (oder pro Organisationsrichtlinie): am selben Ort wie oben.
* Automatisches Löschen inaktiver Benutzer: Aktiviert mit einer unternehmensdefinierten Aufbewahrungsfrist (z. B. 90 Tage Inaktivität): ALM-Admin > Einstellungen > Allgemein.
* Ablauf des externen Benutzerprofils: Setzen Sie dies bei der Erstellung auf jedes externe Profil - ALM-Admin > Benutzer > Extern. Keine unbestimmten externen Profile.
* IP-Zugriffsbeschränkungen: Sofern möglich, auf genehmigte IP-Bereiche beschränken - Admin Console > Einstellungen > Erweiterte Einstellungen.

### Standardwerte für benutzerdefinierte Administratorrollen (konfiguriert beim Erstellen jeder Rolle):

* OAuth-Geltungsbereich für registrierte Anwendungen: Mindestumfang. Gewähren Sie niemals Lese-/Schreibzugriff für die Administratorrolle, es sei denn, dies ist unbedingt erforderlich.
* Benutzerdefinierter Rollenbereich: auf bestimmte Benutzergruppen und bestimmte Kataloge beschränken. Erstellen Sie keine benutzerdefinierten Rollen mit dem Bereich &quot;Alle Benutzer&quot; und &quot;Alle Kataloge&quot;, es sei denn, die Funktion erfordert dies.
* Einstellungszugriff in benutzerdefinierten Rollen: nicht gewähren, es sei denn, die spezifische Funktion erfordert dies angesichts des Risikos einer Berechtigungsausweitung.

### Standardwerte für den Integrationsadministrator:

* API-OAuth-Geltungsbereich: den restriktivsten Bereich auswählen, der die Anforderungen der Integration erfüllt. Gewähren Sie dem Administrator keine Lese-/Schreibrechte für Anwendungen, die nur Lesezugriff auf Teilnehmer benötigen.
* Verbindung-Anmeldedaten, LTI-Anmeldedaten und Webhook-URLs: Vertrauliche Daten - niemals per E-Mail weitergeben oder an die Quellcodeverwaltung binden.

## Bietet Adobe Learning Manager Administratoren die Möglichkeit, die aktuellen Kontoeinstellungen mit den empfohlenen sicheren Standardwerten zu vergleichen?

Adobe Learning Manager verfügt über kein eigenes Vergleichs-Dashboard, in dem automatisch die aktuellen Einstellungen neben den empfohlenen sicheren Standardwerten angezeigt werden. Mit drei Plattformfunktionen können Administratoren jedoch aktuelle Konfigurationen manuell oder programmgesteuert überprüfen und vergleichen.

### Benutzerdefinierter Rollenbericht - aktuelle privilegierte Rollenzuweisungen:

Navigieren Sie in ALM zu Admin > Benutzer > Benutzerdefinierte Rollen und klicken Sie auf Herunterladen (oben rechts), um eine CSV-Datei mit allen benutzerdefinierten Rollen, ihren Berechtigungssätzen und ihren Bereichszuweisungen zu exportieren.

### ALM REST API - Abruf der programmgesteuerten Konfiguration:

* Der Endpunkt GET /account gibt Konfigurationsdaten auf Kontoebene im JSON-Format zurück, auf die über den OAuth-Bereich der Administratorrolle zugegriffen werden kann. Kunden können diesen Endpunkt programmgesteuert aufrufen.
* Der Endpunkt GET /users (mit include=role filter) gibt die aktuellen Rollenzuweisungen für alle Benutzer zurück, wodurch eine automatische Erkennung unerwarteter Rollenzuweisungen ermöglicht wird. Verwenden Sie die Jobs-API für Massenexporte von Benutzern.

## Können Administratoren aktuelle sicherheitsrelevante Einstellungen und Konfigurationen aus Adobe Learning Manager in einem maschinenlesbaren Format exportieren?

Adobe Learning Manager unterstützt den Export sicherheitsrelevanter Konfigurationsdaten über verschiedene Mechanismen. Kein einzelner Export erzeugt einen vollständigen Snapshot aller Sicherheitseinstellungen auf einmal, aber die folgenden Exporte decken gemeinsam den gesamten Bereich der sicherheitsrelevanten Daten ab.

### Admin Console-Audit-Protokoll - CSV-Export aller Authentifizierungs- und Rollenänderungen:

* Navigieren Sie in der Adobe Admin Console zu **Auswertung > Protokolle > Überwachungsprotokoll**, wenden Sie nach Bedarf Filter an und klicken Sie auf **CSV exportieren**.
* Die exportierte CSV-Datei zeichnet alle administrativen Aktionen auf, einschließlich: 2Änderungen an der Durchsetzung von Zugriffsrechten, Änderungen an Sitzungslimits, Zuweisungen und Entfernen von Administratorrollen, Löschen von Benutzern und Änderungen an Produktberechtigungen - alles mit Zeitstempeln und Schauspieleridentität.
* Die Daten werden 90 Tage lang aufbewahrt. Unternehmensbenutzer können Protokolle über alle Global Admin Consolen hinweg exportieren.

### ALM REST API - JSON-Export der aktuellen Rollenzuweisungen und Kontokonfiguration:

* `GET /account` — gibt Einstellungen auf Kontoebene in JSON zurück, einschließlich Konfigurationsdaten für aktive Anmeldungen und Metadaten für Konten.
* `GET /users?include=role` — gibt alle Benutzer mit ihren aktuell zugewiesenen Rollen in JSON zurück.
* `GET /userGroups` — gibt alle Benutzergruppen und deren Mitgliedschaft zurück, die für die Überwachung des benutzerdefinierten Rollenbereichs relevant sind.
* Alle API-Antworten sind JSON (`vnd.api+json`). Die Authentifizierung verwendet OAuth 2.0 mit dem Lese-/Schreibbereich der Administratorrolle.

### CSV-Export benutzerdefinierter Rollen - aktuelle Definitionen privilegierter Rollen:

* ALM-Administrator > Benutzer > Benutzerdefinierte Rollen > Download exportiert eine CSV-Datei aller benutzerdefinierten Rollendefinitionen, ihrer Berechtigungskategorien und Bereichszuweisungen.
* Dieser Export kann als maschinenlesbarer Snapshot der aktuellen privilegierten Kontokonfiguration verwendet werden.

### Jobs-API - Daten für mehrere Benutzer und Rollen:

* Die ALM Jobs-API unterstützt die bedarfsgesteuerte Generierung von Benutzerberichten (einschließlich Rollenzuweisungen) im CSV-Format. Diese können von externen Compliance- oder SIEM-Tools geplant und genutzt werden.

Weitere Informationen finden Sie im [Handbuch für Anwendungsentwickler für Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual).

## Bietet Adobe Learning Manager eine API, über die sicherheitsrelevante Einstellungen programmgesteuert angezeigt und angepasst werden können?

Adobe Learning Manager bietet eine vollständige REST-API v2, die die programmgesteuerte Anzeige und Anpassung sicherheitsrelevanter Einstellungen mithilfe der OAuth 2.0-Authentifizierung ermöglicht. Im Folgenden sind die spezifischen API-Funktionen aufgeführt, die für die Sicherheitseinstellungen relevant sind:

### Authentifizierung und Umfang

* Anwendungen werden vom Integrationsadministrator unter **Integrationsadministrator > Anwendungen > Register** registriert. OAuth 2.0 Client-ID und Geheimnis werden pro Anwendung ausgegeben.
* Es sind sechs Scopes verfügbar. Für die Verwaltung der Sicherheitseinstellungen ist Zugriff auf die **Administratorrolle mit Lese-/Schreibzugriff** erforderlich. Dadurch erhält die Anwendung über die API den gleichen Zugriff wie ein vollständiger Administrator.
* Zugriffstoken werden über den standardmäßigen OAuth-Autorisierungscode oder den Clientanmeldeinformationen-Fluss abgerufen.\
  **Basis-URL:**\
  `https://learningmanager.adobe.com/primeapi/v2/`

### Benutzer- und Rollenverwaltung über API

* `GET /users` — alle Benutzer und ihre aktuellen Rollen abrufen
* `POST /users` — Programmgesteuertes Bereitstellen neuer Benutzer
* `PATCH /users/{id}` — Benutzerattribute einschließlich Rollenzuweisungen aktualisieren
* `DELETE /users/{id}` — Deaktivieren eines Benutzerkontos
* `POST /users/{id}/purge` - Benutzer und alle zugehörigen Datensätze endgültig bereinigen

### Abrufen der Kontokonfiguration

* `GET /account` — gibt die Konfiguration auf Kontoebene zurück, einschließlich der Kontoeinstellungsdaten im JSON-Format, einschließlich der folgenden Felder:
  * `complianceLabelDefaultID`
  * `showComplianceLabel`
  * `custom_injections`

### Adobe User Management API (Admin Console Layer)

* Die Adobe User Management API (UMAPI) bietet programmatischen Zugriff auf Admin Console-Vorgänge:
  * Benutzerbereitstellung
  * Zuweisung von Produktberechtigungen
  * Systemadministrator-Rollenzuweisung auf Organisationsebene
* UMAPI ist von der ALM REST API getrennt und wird auf Adobe-Organisationsebene ausgeführt. Verwenden Sie sie zum Automatisieren von Rollenzuweisungen für die Admin Console und zur Benutzerbereitstellung.

## Veröffentlicht Adobe Learning Manager seine Sicherheitsrichtlinien für die Konfiguration - die empfohlenen Standardeinstellungen - in einem maschinenlesbaren Format wie OSCAL, JSON oder YAML?

Adobe Learning Manager veröffentlicht sein Secure Configuration Guide derzeit nicht in einem maschinenlesbaren Format.

## Ist das Handbuch zur sicheren Konfiguration von Adobe Learning Manager öffentlich zugänglich, ohne dass eine Anmeldung oder ein besonderer Zugriff erforderlich sind?

Ja. Das Handbuch zur sicheren Konfiguration von Adobe Learning Manager ist auf Adobe Experience League öffentlich zugänglich. Es ist kein Konto, keine Anmeldung oder Lizenz erforderlich, um darauf zuzugreifen.

Was ist öffentlich zugänglich?

* FRR-RSC-01: Handbuch für sichere Administration: umfassende Lebenszyklusberatung für Administratorkonten der obersten Ebene.
* FRR-RSC-02: Administrative Sicherheitseinstellungen und Auswirkungen - alle sicherheitsrelevanten Einstellungen, ihre Auswirkungen und empfohlene Standardwerte.

## Bietet Adobe Learning Manager Versionierung und einen Versionsverlauf, anhand dessen Behörden Änderungen an sicherheitsrelevanten Einstellungen und empfohlenen Standardeinstellungen im Zeitverlauf verfolgen können?

Adobe Learning Manager verwaltet einen öffentlich zugänglichen, detaillierten Versionsverlauf für jedes Produktupdate. Sicherheitsrelevante Änderungen an Administratoreinstellungen, Authentifizierungsfunktionen, API-Endpunkten und Rollenverwaltungsfunktionen sind in jeder Version dokumentiert.

### ALM-Versionshinweise - Nummeriert, kumulativer Änderungsverlauf

* Adobe veröffentlicht nummerierte Versionshinweise für jedes Adobe Learning Manager-Update (z. B. *Update 100*, *Update 99*).
* Diese werden auf **Experience League** und folgendem Dokument veröffentlicht:
  * Neue Funktionen
  * Änderungen an vorhandenen Einstellungen
  * Hinzufügen und Entfernen von APIs
  * Connector-Änderungen
  * Veraltete Funktionen
* Jede Versionshinweise enthält einen dedizierten Abschnitt für **API-Änderungen**, in dem Folgendes aufgelistet wird:
  * Neue Endpunkte
  * Geänderte Antwortfelder
  * Abschreibungen
  * Diese sind direkt relevant für sicherheitsrelevante Konfigurationsmöglichkeiten.

### Seite &quot;Was ist neu?&quot; - Funktionsübersichten pro Version

* Jede Hauptversion verfügt über eine dedizierte **-Seite &quot;Neuerungen&quot;**, auf der neue sicherheitsrelevante Funktionen mit Kontext dokumentiert werden.
* Beispiele für dokumentierte sicherheitsbezogene Updates:
  * Änderungen an der Behandlung benutzerdefinierter Rollenberechtigungen
  * Sichtbarkeit von durch CSV erstellten Berechtigungen für benutzerdefinierte Rollen
  * Änderungen an der API-Ratenbegrenzung

### Liste der API-Veraltungen - Autorisierende Aufzeichnung entfernter API-Funktionen

* Adobe verwaltet eine dedizierte Seite **API-Veraltungen**, auf der alle veralteten und entfernten ALM-API-Endpunkte aufgelistet werden, einschließlich der Release-Version, in der jede Veraltungen aufgetreten sind.
* Beispiele für sicherheitsrelevante Ausnahmen:
  * Änderungen am Sortier- und Überschreibungsverhalten des `GET /users`-Endpunkts
  * Benachrichtigung, Anforderungen für Berichtsdatumsfilter


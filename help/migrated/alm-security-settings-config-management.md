---
title: Adobe Learning Manager - Sicherheitseinstellungen und Konfigurationsverwaltung
description: In diesem Dokument werden die administrativen Kontotypen, sicherheitsbezogenen Einstellungen, empfohlenen sicheren Standardwerte, API-Funktionen, Exportfunktionen, Konfigurationsvergleichsmethoden, Veröffentlichungspraktiken und der Versionsverlauf von Adobe Learning Manager beschrieben. Er enthält ausführliche Anleitungen zur Funktionsweise privilegierter Konten, zu deren Auswirkungen auf die Sicherheit und zur Unterstützung der Konfigurationsverwaltung in der gesamten Plattform.
jcr-language: en-us
exl-id: a2e34104-c417-407f-af85-9f3f4b2a9fcb
source-git-commit: 77fddea1c5458485124b8f14d387a69c5ecd11a7
workflow-type: tm+mt
source-wordcount: '1945'
ht-degree: 0%

---

# Sicherheitseinstellungen und Konfigurationsverwaltung

Dieser Leitfaden enthält detaillierte Antworten auf FedRAMP-Empfehlungen (FRR-RSC-03 bis FRR-RSC-08) für Adobe Learning Manager (ALM). Es werden Best Practices zur Sicherheit, empfohlene sichere Standardwerte und Tools für die Überwachung, den Export und die Verwaltung privilegierter Kontoeinstellungen beschrieben. Das Dokument wurde für Administratoren und Compliance-Teams entwickelt, um eine sichere Konfiguration und Verwaltung von ALM-Konten zu gewährleisten.

Außerdem werden die Bereiche hervorgehoben, in denen ALM die FedRAMP-Standards erfüllt oder teilweise erfüllt. Außerdem werden Verweise auf unterstützende Dokumentation und auf Ressourcen, die in Adobe Experience League verfügbar sind, angezeigt.

+++Welche sicherheitsrelevanten Einstellungen können nur von benutzerdefinierten Administratoren oder Integrationsadministratoren in Adobe Learning Manager verwendet werden und welche Auswirkungen haben sie auf die Sicherheit?

Die beiden privilegierten Kontotypen von Adobe Learning Manager: Benutzerdefinierter Administrator und Integrationsadministrator. Jedes verfügt über einen definierten Satz sicherheitsrelevanter Einstellungen mit dokumentierten Auswirkungen.

**Benutzerdefinierter Administrator - was er ausführen kann**:

* Benutzerdefinierte Rollen werden vom vollständigen Administrator unter ALM-Admin > Benutzer > Benutzerdefinierte Rollen konfiguriert. Einem benutzerdefinierten Administrator kann Zugriff auf eine oder mehrere dieser Berechtigungskategorien gewährt werden: Kontoberechtigungen (Ankündigungen, Gamification, Kenntnisse, Benutzerverwaltung), Funktionsberechtigungen (Kataloge, Berichte, Tags) und Lernobjektberechtigungen (Kurse, Zertifizierungen, Lernpfade).
* &quot;Umfang&quot; ist die sicherheitsempfindlichste Einstellung: Eine benutzerdefinierte Rolle kann auf bestimmte Benutzergruppen und/oder bestimmte Kataloge beschränkt werden. Ohne Bereichseinschränkungen hat eine benutzerdefinierte Rolle plattformweiten Zugriff auf die zugewiesenen Funktionen, sodass sie der Stellfläche eines vollständigen Administrators entspricht.
* Wenn einer benutzerdefinierten Rolle unter &quot;Kontoberechtigungen&quot; der Zugriff auf Einstellungen gewährt wird, kann dieser benutzerdefinierte Administrator Anmeldemethoden, Benachrichtigungseinstellungen und Konfigurationen auf Kontoebene ändern. Dies ist eine Berechtigung mit hoher Auswirkung, die nur mit expliziter geschäftlicher Begründung gewährt werden sollte.

**Integrationsadministrator — was er ausführen kann**:

* Integrationsadministratoren verwalten OAuth 2.0-Anwendungsregistrierungen unter Integrationsadministrator > Anwendungen > Registrieren. Sie wählen einen von sechs OAuth-Geltungsbereichen aus, die vom Lese-/Schreibzugriff für Teilnehmer bis hin zum Lese-/Schreibzugriff für die Administratorrolle reichen. Der Lese-/Schreibbereich des Administrators gewährt der registrierten Anwendung dieselben Berechtigungen wie einem vollständigen Administrator über die API.
* Der für die Integration zuständige Administrator konfiguriert FTP-, SFTP-, Salesforce-, Workday- und andere Connectors, die Benutzerdatensätze, Rollenzuweisungen und Kursabschlüsse importieren und Plattformdaten in externe Systeme exportieren.
* Integrationsadministratoren konfigurieren WebHooks, die ALM-Ereignisdaten in Echtzeit (Registrierungen, Abschlüsse, Rollenänderungen) an externe URLs übertragen. Ein beschädigter oder falsch konfigurierter Webhook-Endpunkt ist ein Datenexfiltrationsrisiko.
* Integrationsadministratoren können LTI-Integrationen konfigurieren. Nach der Aktivierung kann LTI nicht mehr deaktiviert werden.

**Verweise**:

* [Benutzerdefinierte Rollen | ADOBE LEARNING MANAGER](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role)
* [Verwalten benutzerdefinierter Rollen über CSV | ADOBE LEARNING MANAGER](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/configure-role-csv-files)
* [Handbuch für Anwendungsentwickler \| Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual)
* [Adobe Learning Manager Connectors](/help/migrated/integration-admin/feature-summary/connectors.md)

+++

+++Welche Sicherheitsstandards werden für Verwaltungs- und privilegierte Konten der obersten Ebene in Adobe Learning Manager empfohlen und wo werden sie konfiguriert?

Für Adobe Learning Manager-Dokumente spezifische empfohlene sichere Standardeinstellungen sowohl für die Administratorrolle als auch für privilegierte Kontotypen.

* **Standardwerte für das Administratorkonto auf oberster Ebene (bei der ersten Bereitstellung konfiguriert)**:

* Anmeldemethode für interne Benutzer: Single Sign-on (SSO) über SAML 2.0: konfiguriert unter ALM-Admin > Einstellungen > Anmeldemethoden. Verwenden Sie Adobe ID nicht für Mitarbeiter oder Administratoren.
* Zweistufige Verifizierung (2FA): Für alle Benutzer erzwingen: konfiguriert unter Adobe Admin Console > Einstellungen > Datenschutz und Sicherheit > Authentifizierungseinstellungen.
* Max. Sitzungsdauer: 8 Stunden (oder pro Organisationsrichtlinie): konfiguriert unter Adobe Admin Console > Einstellungen > Datenschutz und Sicherheit > Erweiterte Einstellungen.
* Max. Leerlaufzeit: 30 Minuten (oder pro Organisationsrichtlinie): am selben Ort wie oben.
* Automatisches Löschen inaktiver Benutzer: Aktiviert mit einer unternehmensdefinierten Aufbewahrungsfrist (z. B. 90 Tage Inaktivität): ALM-Admin > Einstellungen > Allgemein.
* Ablauf des externen Benutzerprofils: Bei der Erstellung auf jedes externe Profil festlegen: ALM-Administrator > Benutzer > Extern. Keine unbestimmten externen Profile.
* IP-Zugriffsbeschränkungen: Sofern möglich, auf genehmigte IP-Bereiche beschränken: Admin Console > Einstellungen > Erweiterte Einstellungen.

**Standardwerte für benutzerdefinierte Administratorrollen (konfiguriert beim Erstellen jeder Rolle)**:

* OAuth-Geltungsbereich für registrierte Anwendungen: Mindestumfang. Gewähren Sie niemals Lese-/Schreibzugriff für die Administratorrolle, es sei denn, dies ist unbedingt erforderlich.
* Benutzerdefinierter Rollenbereich: auf bestimmte Benutzergruppen und bestimmte Kataloge beschränken. Erstellen Sie keine benutzerdefinierten Rollen mit dem Bereich &quot;Alle Benutzer&quot; und &quot;Alle Kataloge&quot;, es sei denn, die Funktion erfordert dies.
* Einstellungszugriff in benutzerdefinierten Rollen: nicht gewähren, es sei denn, die spezifische Funktion erfordert dies angesichts des Risikos einer Berechtigungsausweitung.

**Standardwerte für Integrationsadministrator**:

* API-OAuth-Geltungsbereich: den restriktivsten Bereich auswählen, der die Anforderungen der Integration erfüllt. Gewähren Sie dem Administrator keine Lese-/Schreibrechte für Anwendungen, die nur Lesezugriff auf Teilnehmer benötigen.
* Connector-Anmeldedaten, LTI-Anmeldedaten und Webhook-URLs: Vertrauliche Daten - niemals per E-Mail weitergeben oder an die Quellcodeverwaltung binden.

**Verweise**:

* [Einstellungen | ADOBE LEARNING MANAGER](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role)
* [Sichere Benutzerauthentifizierung und Kennwörter | ADOBE ADMIN CONSOLE](https://helpx.adobe.com/enterprise/using/authentication-settings.html)
* [Benutzerdefinierte Rollen | ADOBE LEARNING MANAGER](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role)

+++

+++Bietet Adobe Learning Manager Administratoren die Möglichkeit, die aktuellen Kontoeinstellungen mit den empfohlenen sicheren Standardwerten zu vergleichen?

Adobe Learning Manager verfügt über kein eigenes Vergleichs-Dashboard, in dem automatisch die aktuellen Einstellungen neben den empfohlenen sicheren Standardwerten angezeigt werden.

**Bericht über benutzerdefinierte Rollen: Aktuelle privilegierte Rollenzuweisungen**:

* Navigieren Sie in ALM zu Admin > Benutzer > Benutzerdefinierte Rollen und klicken Sie auf Herunterladen (oben rechts), um eine CSV-Datei mit allen benutzerdefinierten Rollen, ihren Berechtigungssätzen und ihren Bereichszuweisungen zu exportieren.
* Vergleichen Sie diesen Export mit den empfohlenen Standardeinstellungen in FRR-RSC-02, Abschnitt 8. Insbesondere wird geprüft, ob eine benutzerdefinierte Rolle über Zugriff auf Einstellungen, den Bereich &quot;Alle Benutzer&quot; oder den Bereich &quot;Alle Kataloge&quot; verfügt, ohne dass eine dokumentierte Begründung vorliegt.

**ALM REST-API: Abruf der programmatischen Konfiguration**:

* Der Endpunkt GET /account gibt Konfigurationsdaten auf Kontoebene im JSON-Format zurück, auf die über den OAuth-Bereich der Administratorrolle zugegriffen werden kann. Kunden können diesen Endpunkt programmgesteuert aufrufen und die Antwort anhand einer Baseline vergleichen, die von den empfohlenen Standardwerten in FRR-RSC-02, Abschnitt 8, abgeleitet wird.
* Der Endpunkt GET /users (mit include=role filter) gibt die aktuellen Rollenzuweisungen für alle Benutzer zurück, wodurch eine automatische Erkennung unerwarteter Rollenzuweisungen ermöglicht wird.

>[!NOTE]
>
>Adobe Learning Manager bietet keine systemeigene Vergleichsbenutzeroberfläche. Kunden, die eine automatische Überprüfung der Konfigurationskonformität benötigen, sollten die ALM REST API in ihr bestehendes Tool integrieren.

**Referenz**

* [Handbuch für Anwendungsentwickler | ADOBE LEARNING MANAGER](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual)

+++

+++Können Administratoren aktuelle sicherheitsrelevante Einstellungen und Konfigurationen aus Adobe Learning Manager in einem maschinenlesbaren Format exportieren?

Adobe Learning Manager unterstützt den Export sicherheitsrelevanter Konfigurationsdaten über verschiedene Mechanismen. Kein einzelner Export erzeugt einen vollständigen Snapshot aller Sicherheitseinstellungen auf einmal, aber die folgenden Exporte decken gemeinsam den gesamten Bereich der sicherheitsrelevanten Daten ab.

**ALM REST-API: JSON-Export der aktuellen Rollenzuweisungen und der Kontokonfiguration**:

* GET /account: gibt Einstellungen auf Kontoebene in JSON zurück, einschließlich aktiver Anmeldekonfigurationsdaten und Kontometadaten.
* GET /users?include=role: gibt alle Benutzer mit ihren aktuell zugewiesenen Rollen in JSON zurück.
* GET /userGroups — gibt alle Benutzergruppen und deren Mitgliedschaft zurück, die für die Überwachung des benutzerdefinierten Rollenbereichs relevant sind.
* Alle API-Antworten sind JSON (vnd.api+json). Die Authentifizierung verwendet OAuth 2.0 mit dem Lese-/Schreibbereich der Administratorrolle.

**CSV-Export für benutzerdefinierte Rollen: Aktuelle Definitionen privilegierter Rollen**:

* ALM-Administrator > Benutzer > Benutzerdefinierte Rollen > Download exportiert eine CSV-Datei aller benutzerdefinierten Rollendefinitionen, ihrer Berechtigungskategorien und Bereichszuweisungen.
* Dieser Export kann als maschinenlesbarer Snapshot der aktuellen privilegierten Kontokonfiguration verwendet werden.
**

**Jobs-API: Massenbenutzer- und Rollendaten**:

* Die ALM Jobs-API unterstützt die bedarfsgesteuerte Generierung von Benutzerberichten (einschließlich Rollenzuweisungen) im CSV-Format. Diese können von externen Compliance- oder SIEM-Tools geplant und genutzt werden.

**Referenz**

* [Handbuch für Anwendungsentwickler | ADOBE LEARNING MANAGER](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual)

+++

+++Bietet Adobe Learning Manager eine API, über die sicherheitsrelevante Einstellungen programmgesteuert angezeigt und angepasst werden können?

Adobe Learning Manager bietet eine vollständige REST-API v2, die die programmgesteuerte Anzeige und Anpassung sicherheitsrelevanter Einstellungen mithilfe der OAuth 2.0-Authentifizierung ermöglicht. Im Folgenden sind die spezifischen API-Funktionen aufgeführt, die für die Sicherheitseinstellungen relevant sind:

**Authentifizierung und Umfang**:

* Anwendungen werden vom Integrationsadministrator unter Integrationsadministrator > Anwendungen > Registrieren registriert. OAuth 2.0 Client-ID und Geheimnis werden pro Anwendung ausgegeben.
* Es sind sechs Scopes verfügbar. Für die Verwaltung der Sicherheitseinstellungen ist Lese-/Schreibzugriff auf die Administratorrolle erforderlich. Dadurch erhält die Anwendung über die API den gleichen Zugriff wie ein vollständiger Administrator.
* Zugriffstoken werden über den standardmäßigen OAuth-Autorisierungscode oder den Clientanmeldeinformationen-Fluss abgerufen. Basis-URL: https://learningmanager.adobe.com/primeapi/v2/

**Benutzer- und Rollenverwaltung über API**:

* GET /users: alle Benutzer und ihre aktuellen Rollen abrufen
* POST /Benutzer: programmgesteuertes Bereitstellen neuer Benutzer
* PATCH /users/{id}: Benutzerattribute einschließlich Rollenzuweisungen aktualisieren
* DELETE /users/{id}: Benutzerkonto deaktivieren
* POST /users/{id}/purge: Benutzer und alle zugehörigen Datensätze endgültig bereinigen

Abrufen der Kontokonfiguration:

* GET /account: Gibt die Konfiguration auf Kontoebene zurück, einschließlich der Kontoeinstellungsdaten im JSON-Format, einschließlich der Felder complianceLabelDefaultID, showComplianceLabel und custom_jections.

+++

+++Veröffentlicht Adobe Learning Manager seine sicheren Konfigurationsleitfäden in einem maschinenlesbaren Format wie OSCAL, JSON oder YAML?

Adobe Learning Manager veröffentlicht sein Secure Configuration Guide derzeit nicht in einem maschinenlesbaren Format. Die Anleitung in [FRR-RSC-01](/help/migrated/alm-administrative-lifecycle.md) und [FRR-RSC-02](/help/migrated/alm-secure-administration-guide.md) wird als vom Menschen lesbare Dokumentation auf Adobe Experience League in HTML- und herunterladbaren Dokumentformaten veröffentlicht.

Es gibt keine öffentlich verfügbare OSCAL-Komponentendefinition, YAML-Grundlinie oder JSON-Richtliniendatei, die die empfohlenen sicheren Standardwerte für Adobe Learning Manager codiert.

Kunden, die einen automatisierten Vergleich der aktuellen Einstellungen mit empfohlenen Grundlinien benötigen, sollten die [ALM REST API](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual) verwenden, um aktuelle Konfigurationsdaten im JSON-Format abzurufen.

+++

+++Ist das Handbuch zur sicheren Konfiguration von Adobe Learning Manager öffentlich zugänglich, ohne dass eine Anmeldung oder ein besonderer Zugriff erforderlich sind?

**Was ist öffentlich verfügbar**:

* [FRR-RSC-01: Handbuch für sichere Administration](/help/migrated/alm-administrative-lifecycle.md): umfassende Anleitung zum Lebenszyklus von übergeordneten Administratorkonten.
* [FRR-RSC-02: Verwaltungssicherheitseinstellungen und Auswirkungen](/help/migrated/alm-secure-administration-guide.md): alle sicherheitsrelevanten Einstellungen, ihre Auswirkungen und empfohlenen Standardeinstellungen.
* FRR-RSC-03-10 (dieses Dokument) — Fragen und Antworten zu allen acht FedRAMP-Empfehlungen SOLLTEN berücksichtigt werden.

+++

+++Bietet Adobe Learning Manager Versionierung und einen Versionsverlauf, anhand dessen Behörden Änderungen an sicherheitsrelevanten Einstellungen und empfohlenen Standardeinstellungen im Zeitverlauf verfolgen können?

Adobe Learning Manager verwaltet einen öffentlich zugänglichen, detaillierten Versionsverlauf für jedes Produktupdate. Sicherheitsrelevante Änderungen an Administratoreinstellungen, Authentifizierungsfunktionen, API-Endpunkten und Rollenverwaltungsfunktionen sind in jeder Version dokumentiert.

**ALM-Versionshinweise: nummerierter, kumulativer Änderungsverlauf**:

* Adobe veröffentlicht nummerierte Versionshinweise für jedes Adobe Learning Manager-Update (z. B. Update 100, Update 99). Diese werden auf dem Experience League veröffentlicht und dokumentieren alle neuen Funktionen, Änderungen an bestehenden Einstellungen, API-Ergänzungen und -Entfernungen, Connector-Änderungen und veraltete Funktionen.
* Jede Versionshinweise enthält einen speziellen Abschnitt für API-Änderungen, in dem neue Endpunkte, geänderte Antwortfelder und Veraltungen aufgelistet werden, die direkt für sicherheitsrelevante Konfigurationsfunktionen relevant sind.

**Neue Seiten: Funktionsübersichten pro Version**:

* Jede Hauptversion verfügt über eine spezielle Seite &quot;Neue Funktionen&quot;, auf der neue sicherheitsrelevante Funktionen kontextbezogen dokumentiert werden. Die Versionshinweise enthalten beispielsweise Änderungen an der Berechtigungsbehandlung für benutzerdefinierte Rollen, an der Sichtbarkeit von Berechtigungen, die mit CSV erstellt wurden, für benutzerdefinierte Rollen und an Änderungen zur API-Ratenbegrenzung.

Liste der **API-Veraltungen: Autorisierender Datensatz der entfernten API-Funktionen** s:

* Adobe verwaltet eine dedizierte API-Seite mit den veralteten und entfernten ALM-API-Endpunkten mit der Release-Version, in der die jeweilige Veraltungen aufgetreten sind.

**Verweise**:

* [Versionshinweise zu Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/introduction/release-notes)
* [Neue Funktionen in Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/introduction/whats-new-july-2024)
* [API-Veraltungen in Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/introduction/api-deprecations-list)

+++

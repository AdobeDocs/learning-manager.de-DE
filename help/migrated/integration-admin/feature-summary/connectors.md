---
description: Überblick über jeden ALM-unterstützten Connector
jcr-language: en_us
title: Überblick über ALM-unterstützte Connectors
contentowner: mmanuel
source-git-commit: fc9bf565de2f9491c793654645d2f2400ca49697
workflow-type: tm+mt
source-wordcount: '1415'
ht-degree: 6%

---


# Adobe Learning Manager-Connectors

## Einführung

Adobe Learning Manager (ALM) bietet eine umfassende Suite an Connectors, die eine nahtlose Integration mit Anwendungen von Drittanbietern und Unternehmenssystemen ermöglichen. Diese Connectors dienen als Brücken zwischen Ihrem Lernmanagementsystem und externen Plattformen und erleichtern die automatisierte Datensynchronisierung, Benutzerverwaltung, den Import von Inhalten und den Export von Lerndatensätzen.

Dieses Dokument dient als vollständiger Leitfaden zum Verständnis und zur Auswahl der geeigneten Connectors für das Lernökosystem Ihres Unternehmens. Ganz gleich, ob ihr HR-Systeme, E-Commerce-Plattformen, virtuelle Meeting-Tools oder Business-Intelligence-Lösungen integrieren möchtet.

Eine vollständige Liste der von Adobe Learning Manager unterstützten Connectors finden Sie unter Artikel von Connectors, die direkt unter diesem Artikel im Inhaltsverzeichnis auf der linken Seite verschachtelt sind.

>[!NOTE]
>
>Diese Funktion ist teilweise in FedRAMP-autorisierten Umgebungen verfügbar. Weitere Informationen finden Sie unter [Verfügbarkeit von Funktionen in FedRAMP-Umgebungen](/help/migrated/feature-availability-in-fedramp-authorized-environment.md).

>[!NOTE]
>
>Mit der Adobe Learning Manager-Version vom November 2022 hat Zoom die [JWT-Authentifizierung bis Juni 2023 veraltet](https://developers.zoom.us/docs/internal-apps/s2s-oauth/). Dementsprechend funktioniert der Zoom-Connector mit JWT noch bis zum erwähnten Datum, aber wir empfehlen Benutzern die Erstellung einer Server-zu-Server-OAuth-App, um die Funktionalität in ihrem Konto zu ersetzen. Alle neuen Verbindungen haben standardmäßig eine Zoom-OAuth-Authentifizierung.

## Connector-Kategorien

Adobe Learning Manager-Connectors können je nach Hauptzweck und Integrationsfunktionen in mehrere Funktionskategorien unterteilt werden:

| Kategorie | Zweck | Beispiel-Connectors |
|---------|--------|-------------------|
| Datenübertragung | Dateibasierter Datenaustausch und Massenvorgänge | FTP, Benutzerdefiniertes FTP, Box |
| Virtuelles Klassenzimmer | Integration von Live-Schulungen und Meetings | Microsoft Teams, Zoom, Adobe Connect |
| Unternehmenssysteme | Integration von HR- und Geschäftssystemen | Workday, Salesforce, ADFS |
| Content-Plattformen | Integration externer Lerninhalte | LinkedIn Learning, Harvard ManageMentor, getAbstract |
| Analytics und BI | Reporting und Datenvisualisierung. | Power BI, Zugriff auf Schulungsdaten |
| Authentifizierung | Identitäts-Management und Sicherheit. | ADFS (SSO-Funktionen) |
| E-Commerce und Marketing. | Integration von Vertrieb und Marketing | Adobe Commerce, Marketo Engage |

## Connectors für Datenübertragung und Dateiverwaltung

Diese Connectors ermöglichen den automatisierten Datenaustausch über Dateiübertragungsprotokolle und ermöglichen Massenvorgänge und die Kommunikation zwischen Systemen.

### Adobe Learning Manager FTP-Connector

Mit dem FTP-Connector können Unternehmen die Datensynchronisierung zwischen Adobe Learning Manager und externen Systemen mithilfe des weit verbreiteten File Transfer Protocol automatisieren. Dieser Connector unterstützt sichere Varianten, einschließlich SFTP (SSH File Transfer Protocol) und FTPS (FTP Secure) für verbesserte Sicherheit.

#### Wichtigste Funktionen:

- Hochladen und Herunterladen von Dateien zwischen Adobe Learning Manager und Remote-Servern
- Automatisierter Datenaustausch für Benutzerinformationen und Schulungsunterlagen.
- Unterstützung für sichere Dateiübertragungsprotokolle (SFTP, FTPS).
- Stapelverarbeitung großer Datensätze.

Weitere Informationen finden Sie unter [FTP-Connector](/help/migrated/integration-admin/feature-summary/ftp-connector.md).

### Benutzerdefinierter FTP-Connector

Der benutzerdefinierte FTP-Connector bietet anspruchsvollere Dateiübertragungsfunktionen und unterstützt strukturierte Datenformate und den Austausch von xAPI-Anweisungen. Dieser Connector wurde für Unternehmen entwickelt, die eine detailliertere Kontrolle über ihre Datenaustauschprozesse benötigen.

#### Wichtigste Funktionen:

- Importieren und exportieren Sie Benutzerdaten über strukturierte CSV-Dateien.
- Behandeln Sie Lerndatensätze und xAPI-Anweisungen.
- Automatisierte Dateiverarbeitung aus angegebenen FTP-Ordnern.
- Verbesserte Sicherheitsfunktionen für die Übertragung vertraulicher Daten.

Weitere Informationen finden Sie unter [Benutzerdefinierter FTP-Connector](/help/migrated/integration-admin/feature-summary/custom-ftp-connector.md).

### Box-Connector

Der Box-Connector nutzt die Cloud-Speicherplattform von Box, um eine nahtlose Datensynchronisierung zwischen externen Systemen und Adobe Learning Manager zu erleichtern. Dieser Connector ist besonders für Organisationen nützlich, die Box bereits für die Dateiverwaltung verwenden.

#### Wichtigste Funktionen:

- Cloud-basierte Speicherung und Synchronisation von Dateien.
- Automatisierte Verarbeitung von CSV-Daten.
- Integration mit vorhandenen Box-Workflows.
- Echtzeit-Datenaktualisierungen aus angegebenen Ordnern.

## Connectors für virtuelle Klassenzimmer und Meetings

Diese Connectoren integrieren Adobe Learning Manager mit beliebten Videokonferenz- und virtuellen Meetingplattformen und ermöglichen die nahtlose Bereitstellung von Live-Schulungssitzungen.

Weitere Informationen finden Sie unter [Box-Connector](/help/migrated/integration-admin/feature-summary/box-connector.md).

### Microsoft Teams-Connector

Der Microsoft Teams-Connector verwandelt Adobe Learning Manager in eine umfassende Lösung für virtuelle Klassenzimmer, indem er direkt in die Meetingfunktionen von Teams integriert wird. Dieser Connector ist für Unternehmen, die das Microsoft 365-Ökosystem verwenden, unerlässlich.

#### Wichtigste Funktionen:

- Planen Sie Sitzungen im virtuellen Klassenzimmer direkt über Adobe Learning Manager.
- Automatisches Erstellen und Verwalten von Teams-Meetings.
- Nahtloser Teilnehmerzugriff ohne separate Meetinglinks.

Weitere Informationen finden Sie unter [MS Teams-Connector](/help/migrated/integration-admin/feature-summary/install-microsoft-teams-connector.md).

### Zoom-Connector

Der Zoom-Connector ermöglicht es Unternehmen, die robusten Videokonferenzfunktionen von Zoom direkt in ihrer Adobe Learning Manager-Umgebung zu nutzen und so ein nahtloses Erlebnis sowohl für Kursleiter als auch für Teilnehmer bereitzustellen.

#### Wichtigste Funktionen:

- Terminierter direkter Zoom von Meetings über Adobe Learning Manager.
- Automatisierte Erstellung und Verteilung von Meeting-Links.
- Anwesenheitsüberwachung in Echtzeit.
- Integration von Aufnahmemanagement und Wiedergabe.
- Unterstützung für Breakout-Räume für interaktive Sitzungen.

Weitere Informationen finden Sie unter [Zoom-Connector](/help/migrated/integration-admin/feature-summary/zoom-connector.md).

### Adobe Connect Connector

Der Adobe Connect-Connector bietet eine enge Integration mit der eigenen virtuellen Klassenzimmerplattform der Adobe und erweiterte Funktionen für interaktive Online-Lernerlebnisse.

#### Wichtigste Funktionen:

- Erweiterte interaktive Funktionen (Umfragen, Tests, Breakout-Sessions).
- Hochwertige Tools für Bildschirmfreigabe und Präsentation.
- Umfassende Aufzeichnung und Wiedergabe von Sessions.
- Für Mobilgeräte optimierte virtuelle Lernumgebungen.

Weitere Informationen finden Sie unter [Adobe Connect-Connector](/help/migrated/integration-admin/feature-summary/adobe-connect-connector.md).

## Enterprise-Systemintegrations-Connectors

Diese Connectoren ermöglichen die Integration von Adobe Learning Manager in wichtige Unternehmenssysteme und erleichtern die automatisierte Benutzerverwaltung und Datensynchronisierung in der Organisation.

### Workday Connector

Der Workday-Connector stellt eine nahtlose Brücke zwischen Ihrem HR-System und der Lernmanagementplattform dar und stellt sicher, dass Mitarbeiterdatensätze, Organisationsstrukturen und Rollenzuweisungen über beide Systeme hinweg synchronisiert bleiben.

#### Wichtigste Funktionen:

- Automatisierte Benutzerbereitstellung von Workday.
- Datensynchronisierung in Echtzeit für Mitarbeiter.
- Zuordnung der Organisationshierarchie.
- Rollenbasierte Lernzuweisungsautomatisierung.

Weitere Informationen finden Sie unter [Workday-Connector](/help/migrated/integration-admin/feature-summary/workday-connector.md).

### Salesforce-Connector

Der Salesforce-Connector ermöglicht es Unternehmen, ihr System für das Customer Relationship Management in Lerninitiativen zu integrieren und so Möglichkeiten für Vertriebsschulungen, Kundenschulungen und Leistungsüberwachung zu schaffen.

#### Wichtigste Funktionen:

- Automatischer Benutzerimport aus Salesforce.
- Benutzerdefinierte Datenfeldzuordnung.
- Export von Lerndatensätzen nach Salesforce.
- Verkäufer-Performance-Korrelation mit Schulungsabschluss.
- Schulungsprogramm-Management für Kunden.

Weitere Informationen finden Sie unter [Salesforce-Connector](/help/migrated/integration-admin/feature-summary/salesforce-connector.md).

### ADFS-Connector (Active Directory-Verbunddienste)

Mit dem ADFS-Connector können Organisationen Authentifizierung und Autorisierung auf Unternehmensniveau implementieren, sodass Benutzer mit ihren bestehenden Active Directory-Anmeldeinformationen auf Adobe Learning Manager zugreifen können.

#### Wichtigste Funktionen:

- Implementierung von Single Sign-on (SSO)
- Enterprise Security Compliance.
- Nahtlose Benutzerauthentifizierung

Weitere Informationen finden Sie unter [ADFS-Connector](/help/migrated/integration-admin/feature-summary/adfs-connector.md).

## Connectoren für Content- und Lernplattformen

Diese Connectors erweitern Ihren Lernkatalog durch die Integration externer Inhaltsbibliotheken und spezieller Lernplattformen.

### LinkedIn Learning-Connector

Der LinkedIn Learning-Connector bietet Zugriff auf die umfangreiche LinkedIn-Bibliothek an Kursen zur beruflichen Entwicklung, sodass Unternehmen ihre interne Schulung mit branchenführenden externen Inhalten ergänzen können.

#### Wichtigste Funktionen:

- Zugriff auf den vollständigen Kurskatalog von LinkedIn Learning.
- Automatisierte Kurserkennung und -import.
- Fortschrittsverfolgung für Teilnehmer in Adobe Learning Manager.

Weitere Informationen finden Sie unter [LinkedIn-Connector](/help/migrated/integration-admin/feature-summary/linkedin-learning-connector.md).

### Harvard ManageMentor-Connector

Der Harvard ManageMentor-Connector bietet erstklassige Inhalte für Führungs- und Managementschulungen direkt in Ihre Adobe Learning Manager-Umgebung und ermöglicht den Zugriff auf die renommierten Bildungsressourcen der Harvard Business School.

#### Wichtigste Funktionen:

- Premium-Zugriff auf Inhalte der Harvard Business School.
- Module zur Entwicklung von Management und Führung.
- Nahtloser Import und Organisation von Inhalten.

Weitere Informationen finden Sie unter [Harvard ManageMentor-Connector](/help/migrated/integration-admin/feature-summary/harvard-managementor-connector.md).

### getAbstract-Connector

Der getAbstract-Connector bietet Zugang zu prägnanten Geschäftsbuchzusammenfassungen und professionellen Einblicken, sodass Organisationen kontinuierliches Lernen durch verdauliche Inhaltsformate anbieten können.

#### Wichtigste Funktionen:

- Zugriff auf Zusammenfassungen und Einblicke in Geschäftsbücher.
- Verfolgung von Nutzungsdaten und Reporting.
- Datensatz-Erstellung mit automatischem Abschluss.

Weitere Informationen finden Sie unter [getAbstract-Connector](/help/migrated/integration-admin/feature-summary/getabstract-connector.md).

## Business-Intelligence- und Analyse-Connectors

Diese Connectors ermöglichen erweiterte Reporting-, Datenvisualisierungs- und Business-Intelligence-Funktionen, indem Lerndaten mit externen Analyseplattformen integriert werden.

### Power BI-Connector

Der Power BI-Connector verwandelt Ihre Lerndaten in verwertbare Geschäftsinformationen, indem Lernmetriken automatisch mit der leistungsstarken Business-Intelligence-Plattform von Microsoft synchronisiert werden.

#### Wichtigste Funktionen:

- Datensynchronisierung beim Lernen in Echtzeit.
- Benutzerdefinierte Dashboard-Erstellung und -Verwaltung.
- Erweiterte Datenvisualisierung und Reporting.
- Integration von Teilnehmertranskripten und Kenntnisberichten.

Weitere Informationen finden Sie unter [Power BI-Connector](/help/migrated/integration-admin/feature-summary/power-bi-connector.md).

### Connector für Schulungsdatenzugriff

Der Connector für den Zugriff auf Schulungsdaten ermöglicht Unternehmen die Erstellung benutzerdefinierter Lernschnittstellen und Headless-Lernerlebnisse, indem er API-Zugriff auf Schulungsdaten und Kursinformationen bietet.

**Wichtige Funktionen:**

- Öffentlicher API-Zugriff auf Kurs- und Lernpfaddaten.
- Unterstützung für die Entwicklung benutzerdefinierter Benutzeroberflächen.
- Headless-Lernerlebniserstellung.
- Erweiterte Such- und Filterfunktionen.

Weitere Informationen finden Sie unter [Schulungsdatenzugriffsconnector](/help/migrated/integration-admin/feature-summary/training-data-access-connector.md).

## E-Commerce- und Marketing-Connectoren

Diese Connectoren ermöglichen die Monetarisierung von Lerninhalten und die Integration mit Marketing-Automatisierungsplattformen.

### Adobe Commerce-Connector

Der Adobe Commerce-Connector verwandelt Adobe Learning Manager in eine umfassende E-Commerce-Plattform, mit der Organisationen Kurse, Zertifizierungen und Schulungsprogramme über ein vollständig integriertes E-Commerce-Erlebnis verkaufen können.

**Wichtige Funktionen:**

- Nahtlose Integration von E-Commerce-Plattformen.
- Kurskatalog und Preismanagement.
- Automatisierte Zahlungsverarbeitung und Registrierung.

Weitere Informationen finden Sie unter [Adobe Commerce-Connector](/help/migrated/integration-admin/feature-summary/adobe-commerce-connector.md).

### Marketo Engage-Connector

Der Marketo Engage-Connector schafft leistungsstarke Synergien zwischen Lernaktivitäten und Marketingkampagnen, sodass Unternehmen Bildungsinteraktionen zur Lead-Nurturing und Kundenentwicklung nutzen können.

#### Wichtigste Funktionen:

- Automatisierte Lead-Erstellung und -Aktualisierung.
- Tracking der Lernaktivitäten für Marketing-Erkenntnisse.
- Auslöser für Kursregistrierungs- und Abschlussereignisse.

Weitere Informationen finden Sie unter [Marketo Engage-Connector](/help/migrated/integration-admin/feature-summary/marketo-engage-connector.md).

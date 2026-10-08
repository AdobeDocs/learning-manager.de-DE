---
description: Überblick über die einzelnen ALM-unterstützten Verbindungen
jcr-language: en_us
title: Überblick über Verbindungen in Adobe Learning Manager
contentowner: mmanuel
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 6%
---

# Adobe Learning Manager Verbindungen

## Einführung

Adobe Learning Manager (ALM) bietet ein umfassendes Paket an Verbindungen, die eine nahtlose Integration mit Anwendungen von Drittanbietern und Unternehmenssystemen ermöglichen. Diese Verbindungen dienen als Brücken zwischen Ihrem Lernmanagementsystem und externen Plattformen und erleichtern die automatisierte Datensynchronisierung, Benutzerverwaltung, den Import von Inhalten und den Export von Lerndatensätzen.

Dieses Dokument dient als vollständiger Leitfaden zum Verständnis und zur Auswahl der geeigneten Verbindungen für das Lernökosystem Ihres Unternehmens. Ganz gleich, ob ihr HR-Systeme, E-Commerce-Plattformen, virtuelle Meeting-Tools oder Business-Intelligence-Lösungen integrieren möchtet.

Eine vollständige Liste der von Adobe Learning Manager unterstützten Verbindungen finden Sie unter Artikel von Verbindungen, die direkt unter diesem Artikel im Inhaltsverzeichnis auf der linken Seite verschachtelt sind.

>[!NOTE]
>
>Diese Funktion ist teilweise in FedRAMP-autorisierten Umgebungen verfügbar. Weitere Informationen finden Sie unter [Verfügbarkeit von Funktionen in FedRAMP-Umgebungen](/help/migrated/feature-availability-in-fedramp-authorized-environment.md).

>[!NOTE]
>
>Mit der Adobe Learning Manager-Version vom November 2022 hat Zoom die [JWT-Authentifizierung bis Juni 2023 veraltet](https://developers.zoom.us/docs/internal-apps/s2s-oauth/). Dementsprechend funktioniert der Zoom-Connector mit JWT noch bis zum erwähnten Datum, aber wir empfehlen Benutzern die Erstellung einer Server-zu-Server-OAuth-App, um die Funktionalität in ihrem Konto zu ersetzen. Alle neuen Verbindungen haben standardmäßig eine Zoom-OAuth-Authentifizierung.

## Verbindungen

Adobe Learning Manager-Verbindungen können je nach Hauptzweck und Integrationsmöglichkeiten in mehrere Funktionskategorien unterteilt werden:

| Kategorie | Zweck | Beispiel-Verbindungen |
|---------|--------|-------------------|
| Datenübertragung | Dateibasierter Datenaustausch und Massenvorgänge | FTP, Benutzerdefiniertes FTP, Box |
| Virtuelles Klassenzimmer | Integration von Live-Schulungen und Meetings | Microsoft Teams, Zoom, Adobe Connect |
| Unternehmenssysteme | Integration von HR- und Geschäftssystemen | Workday, Salesforce, ADFS |
| Content-Plattformen | Integration externer Lerninhalte | LinkedIn Learning, Harvard ManageMentor, getAbstract |
| Analytics und BI | Reporting und Datenvisualisierung. | Power BI, Zugriff auf Schulungsdaten |
| Authentifizierung | Identitäts-Management und Sicherheit. | ADFS (SSO-Funktionen) |
| E-Commerce und Marketing. | Integration von Vertrieb und Marketing | Adobe Commerce, Marketo Engage |

## Verbindungen bei der Datenübertragung und Dateiverwaltung

Diese Verbindungen erleichtern den automatisierten Datenaustausch über Dateiübertragungsprotokolle und ermöglichen Massenvorgänge und die Kommunikation zwischen Systemen.

### Adobe Learning Manager FTP-Verbindung

Mit der FTP-Verbindung können Unternehmen die Datensynchronisierung zwischen Adobe Learning Manager und externen Systemen mithilfe des weit verbreiteten Dateiübertragungsprotokolls automatisieren. Diese Verbindung unterstützt sichere Varianten, einschließlich SFTP (SSH File Transfer Protocol) und FTPS (FTP Secure) für verbesserte Sicherheit.

#### Wichtigste Funktionen:

- Hochladen und Herunterladen von Dateien zwischen Adobe Learning Manager und Remote-Servern
- Automatisierter Datenaustausch für Benutzerinformationen und Schulungsunterlagen.
- Unterstützung für sichere Dateiübertragungsprotokolle (SFTP, FTPS).
- Stapelverarbeitung großer Datensätze.

Weitere Informationen finden Sie unter [FTP-Verbindung](/help/migrated/integration-admin/feature-summary/ftp-connector.md).

### Benutzerdefinierte FTP-Verbindung

Die Custom FTP-Verbindung bietet anspruchsvollere Dateiübertragungsfunktionen und unterstützt strukturierte Datenformate sowie den Austausch von xAPI-Anweisungen. Diese Verbindung wurde für Unternehmen entwickelt, die eine detailliertere Kontrolle über ihre Datenaustauschprozesse benötigen.

#### Wichtigste Funktionen:

- Importieren und exportieren Sie Benutzerdaten über strukturierte CSV-Dateien.
- Behandeln Sie Lerndatensätze und xAPI-Anweisungen.
- Automatisierte Dateiverarbeitung aus angegebenen FTP-Ordnern.
- Verbesserte Sicherheitsfunktionen für die Übertragung vertraulicher Daten.

Weitere Informationen finden Sie unter [Benutzerdefinierte FTP-Verbindung](/help/migrated/integration-admin/feature-summary/custom-ftp-connector.md).

### Box-Connector

Die Box-Verbindung nutzt die Cloud-Speicherplattform von Box, um eine nahtlose Datensynchronisierung zwischen externen Systemen und Adobe Learning Manager zu ermöglichen. Diese Verbindung ist besonders für Unternehmen hilfreich, die Box bereits für die Dateiverwaltung verwenden.

#### Wichtigste Funktionen:

- Cloud-basierte Speicherung und Synchronisation von Dateien.
- Automatisierte Verarbeitung von CSV-Daten.
- Integration mit vorhandenen Box-Workflows.
- Echtzeit-Datenaktualisierungen aus angegebenen Ordnern.

Weitere Informationen finden Sie unter [Box-Connector](/help/migrated/integration-admin/feature-summary/box-connector.md).

## Verbindungen für virtuelle Klassenzimmer und Meetings

Diese Verbindungen integrieren Adobe Learning Manager mit beliebten Videokonferenzen und virtuellen Meetingplattformen und ermöglichen die nahtlose Bereitstellung von Live-Schulungssitzungen.

### Microsoft Teams-Connector

Die Microsoft Teams-Verbindung transformieren Adobe Learning Manager in eine umfassende Lösung für virtuelle Klassenzimmer, indem sie direkt in die Meetingfunktionen von Teams integriert wird. Diese Verbindung ist für Unternehmen, die das Microsoft 365-Ökosystem verwenden, unerlässlich.

#### Wichtigste Funktionen:

- Planen Sie Sitzungen im virtuellen Klassenzimmer direkt über Adobe Learning Manager.
- Automatisches Erstellen und Verwalten von Teams-Meetings.
- Nahtloser Teilnehmerzugriff ohne separate Meetinglinks.

Weitere Informationen finden Sie unter [MS Teams-Verbindung](/help/migrated/integration-admin/feature-summary/install-microsoft-teams-connector.md).

### Zoom-Verbindung

Die Zoom-Verbindung ermöglicht es Unternehmen, die leistungsstarken Videokonferenzfunktionen von Zoom direkt in ihrer Adobe Learning Manager-Umgebung zu nutzen und so sowohl den Kursleitern als auch den Teilnehmern ein nahtloses Erlebnis zu bieten.

#### Wichtigste Funktionen:

- Terminierter direkter Zoom von Meetings über Adobe Learning Manager.
- Automatisierte Erstellung und Verteilung von Meeting-Links.
- Anwesenheitsüberwachung in Echtzeit.
- Integration von Aufnahmemanagement und Wiedergabe.
- Unterstützung für Breakout-Räume für interaktive Sitzungen.

Weitere Informationen finden Sie unter [Zoom-Verbindung](/help/migrated/integration-admin/feature-summary/zoom-connector.md).

### Adobe Connect Verbindung

Die Adobe Connect-Verbindung bietet eine enge Integration mit der eigenen virtuellen Klassenzimmerplattform von Adobe und bietet erweiterte Funktionen für interaktive Online-Lernerlebnisse.

#### Wichtigste Funktionen:

- Erweiterte interaktive Funktionen (Umfragen, Tests, Breakout-Sessions).
- Hochwertige Tools für Bildschirmfreigabe und Präsentation.
- Umfassende Aufzeichnung und Wiedergabe von Sessions.
- Für Mobilgeräte optimierte virtuelle Lernumgebungen.

Weitere Informationen finden Sie unter [Adobe Connect-Verbindung](/help/migrated/integration-admin/feature-summary/adobe-connect-connector.md).

## Verbindungen der Enterprise-Systemintegration

Mit diesen Verbindungen kann Adobe Learning Manager in die wichtigsten Unternehmenssysteme integriert werden, was die automatisierte Benutzerverwaltung und Datensynchronisierung in der Organisation erleichtert.

### Workday Connector

Mit der Workday-Verbindung wird eine nahtlose Verbindung zwischen Ihrem HR-System und der Lernmanagementplattform hergestellt, sodass sichergestellt ist, dass Mitarbeiterdatensätze, Organisationsstrukturen und Rollenzuweisungen über beide Systeme hinweg synchronisiert bleiben.

#### Wichtigste Funktionen:

- Automatisierte Benutzerbereitstellung von Workday.
- Datensynchronisierung in Echtzeit für Mitarbeiter.
- Zuordnung der Organisationshierarchie.
- Rollenbasierte Lernzuweisungsautomatisierung.

Weitere Informationen finden Sie unter [Workday-Verbindung](/help/migrated/integration-admin/feature-summary/workday-connector.md).

### Salesforce-Connector

Mit der Salesforce-Verbindung können Unternehmen ihr System für das Customer Relationship Management in Lerninitiativen integrieren und so Möglichkeiten für Vertriebsschulungen, Kundenschulungen und Leistungsüberwachung schaffen.

#### Wichtigste Funktionen:

- Automatischer Benutzerimport aus Salesforce.
- Benutzerdefinierte Datenfeldzuordnung.
- Export von Lerndatensätzen nach Salesforce.
- Verkäufer-Performance-Korrelation mit Schulungsabschluss.
- Schulungsprogramm-Management für Kunden.

Weitere Informationen finden Sie unter [Salesforce-Verbindung](/help/migrated/integration-admin/feature-summary/salesforce-connector.md).

### ADFS-Verbindung (Active Directory-Verbunddienste)

Mit der ADFS-Verbindung können Organisationen Authentifizierung und Autorisierung auf Unternehmensniveau implementieren, sodass Benutzer mit ihren bestehenden Active Directory-Anmeldeinformationen auf Adobe Learning Manager zugreifen können.

#### Wichtigste Funktionen:

- Implementierung von Single Sign-on (SSO)
- Enterprise Security Compliance.
- Nahtlose Benutzerauthentifizierung
- Automatischer Benutzerimport
- Möglichkeit zur Terminierung
- Filtermöglichkeiten

Weitere Informationen finden Sie unter [ADFS-Verbindung](/help/migrated/integration-admin/feature-summary/adfs-connector.md).

## Verbindungen der Inhalts- und Lernplattform

Diese Verbindungen erweitern Ihren Lernkatalog durch die Integration externer Inhaltsbibliotheken und spezieller Lernplattformen.

### LinkedIn Learning-Connector

Die LinkedIn Learning-Verbindung bietet Zugriff auf die umfangreiche LinkedIn-Bibliothek mit Kursen zur beruflichen Entwicklung, die es Unternehmen ermöglicht, ihre interne Schulung mit branchenführenden externen Inhalten zu ergänzen.

#### Wichtigste Funktionen:

- Zugriff auf den vollständigen Kurskatalog von LinkedIn Learning.
- Automatisierte Kurserkennung und -import.
- Fortschrittsverfolgung für Teilnehmer in Adobe Learning Manager.

Weitere Informationen finden Sie unter [LinkedIn-Verbindung](/help/migrated/integration-admin/feature-summary/linkedin-learning-connector.md).

### Harvard ManageMentor-Connector

Die Harvard ManageMentor-Verbindung bringt erstklassige Inhalte für Führungs- und Managementschulungen direkt in Ihre Adobe Learning Manager-Umgebung und bietet Zugriff auf die renommierten Schulungsressourcen der Harvard Business School.

#### Wichtigste Funktionen:

- Premium-Zugriff auf Inhalte der Harvard Business School.
- Module zur Entwicklung von Management und Führung.
- Nahtloser Import und Organisation von Inhalten.

Weitere Informationen finden Sie unter [Harvard ManageMentor-Verbindung](/help/migrated/integration-admin/feature-summary/harvard-managementor-connector.md).

### getAbstract-Verbindung

Die getAbstract-Verbindung bietet Zugang zu prägnanten Geschäftsbuchzusammenfassungen und professionellen Einblicken, sodass Unternehmen durch verdauliche Inhaltsformate kontinuierliches Lernen anbieten können.

#### Wichtigste Funktionen:

- Zugriff auf Zusammenfassungen und Einblicke in Geschäftsbücher.
- Verfolgung von Nutzungsdaten und Reporting.
- Datensatz-Erstellung mit automatischem Abschluss.

Weitere Informationen finden Sie unter [getAbstract-Verbindung](/help/migrated/integration-admin/feature-summary/getabstract-connector.md).

## Business-Intelligence- und Analyse-Verbindungen

Diese Verbindungen ermöglichen erweiterte Reporting-, Datenvisualisierungs- und Business-Intelligence-Funktionen, indem Lerndaten mit externen Analyseplattformen integriert werden.

### Power BI-Connector

Die Power BI-Verbindung transformieren Ihre Lerndaten in verwertbare Geschäftsinformationen, indem Lernmetriken automatisch mit der leistungsstarken Business-Intelligence-Plattform von Microsoft synchronisiert werden.

#### Wichtigste Funktionen:

- Datensynchronisierung beim Lernen in Echtzeit.
- Benutzerdefinierte Dashboard-Erstellung und -Verwaltung.
- Erweiterte Datenvisualisierung und Reporting.
- Integration von Teilnehmertranskripten und Kenntnisberichten.

Weitere Informationen finden Sie unter [Power BI-Connector](/help/migrated/integration-admin/feature-summary/power-bi-connector.md).

### Connector für Schulungsdatenzugriff

Mit der Verbindung &quot;Zugriff auf Schulungsdaten&quot; können Unternehmen benutzerdefinierte Lernschnittstellen und Headless-Lernerlebnisse erstellen, indem sie API-Zugriff auf Schulungsdaten und Kursinformationen gewähren.

**Wichtige Funktionen:**

- Öffentlicher API-Zugriff auf Kurs- und Lernpfaddaten.
- Unterstützung für die Entwicklung benutzerdefinierter Benutzeroberflächen.
- Headless-Lernerlebniserstellung.
- Erweiterte Suche und Filterung.

Weitere Informationen finden Sie unter [Verbindung für den Zugriff auf Schulungsdaten](/help/migrated/integration-admin/feature-summary/training-data-access-connector.md).

## E-Commerce- und Marketing-Verbindungen

Diese Verbindungen ermöglichen die Monetarisierung von Lerninhalten und die Integration mit Marketing-Automatisierungsplattformen.

### Adobe Commerce-Connector

Die Adobe Commerce-Verbindung transformieren Adobe Learning Manager in eine umfassende E-Commerce-Plattform, mit der Organisationen Kurse, Zertifizierungen und Schulungsprogramme über ein vollständig integriertes E-Commerce-Erlebnis verkaufen können.

**Wichtige Funktionen:**

- Nahtlose Integration von E-Commerce-Plattformen.
- Kurskatalog und Preismanagement.
- Automatisierte Zahlungsverarbeitung und Registrierung.

Weitere Informationen finden Sie unter [Adobe Commerce-Verbindung](/help/migrated/integration-admin/feature-summary/adobe-commerce-connector.md).

### Marketo Engage-Connector

Die Marketo Engage-Verbindung schafft leistungsstarke Synergien zwischen Lernaktivitäten und Marketing-Kampagnen und versetzt Unternehmen in die Lage, pädagogisches Engagement für Lead-Nurturing und Kundenentwicklung zu nutzen.

#### Wichtigste Funktionen:

- Automatisierte Lead-Erstellung und -Aktualisierung.
- Tracking der Lernaktivitäten für Marketing-Erkenntnisse.
- Auslöser für Kursregistrierungs- und Abschlussereignisse.

Weitere Informationen finden Sie unter [Marketo Engage Verbindung](/help/migrated/integration-admin/feature-summary/marketo-engage-connector.md).

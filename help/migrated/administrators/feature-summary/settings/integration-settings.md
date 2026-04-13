---
description: Erfahre mehr darüber, wie die Integrationseinstellungen Adobe Learning Manager mit Drittanbieterlösungen verbinden.
jcr-language: en_us
title: Integrationseinstellungen in Adobe Learning Manager
source-git-commit: 03123dcd8d9066cdfcb0fe97e61acb3df625a23e
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 4%

---


# Integrationseinstellungen in Adobe Learning Manager

## Anmeldemethoden

Adobe Learning Manager bietet verschiedene Anmeldemethoden, um den sicheren und flexiblen Zugriff für interne und externe Benutzer zu gewährleisten. Administratoren können diese Anmeldemethoden entsprechend den Anforderungen der Organisation konfigurieren.

Folgende Anmeldemethoden stehen zur Verfügung:

* Adobe Learning Manager: ID
* Adobe ID
* Single Sign-On

### Interne Benutzer

Im Abschnitt &quot;Interne Benutzer&quot; können Sie Anmeldeoptionen speziell für interne Benutzer konfigurieren. Interne Benutzer können entweder über die Adobe ID oder über Single Sign-on (SSO) auf das Konto zugreifen.

**Adobe ID:**

* Interne Benutzer können sich mit ihren Adobe ID-Anmeldeinformationen anmelden.
* Geeignet für Organisationen, die bereits Adobe-Dienste verwenden.

**Single Sign-On (SSO):**

* Ermöglicht es SSO für interne Benutzer, den Identitätsanbieter (IdP) der Organisation zu verwenden.
* Unterstützung der SAML 2.0-basierten Authentifizierung für eine nahtlose Anmeldung.

Um SSO-Anmeldungen für interne Benutzer zuzulassen, wählen Sie Mehrere Single Sign-on (SSO) für die Anmeldung aktivieren aus und beginnen Sie mit der Konfiguration von SSO.

Das aktive **[!UICONTROL SSO-Feld]** in Adobe Learning Manager wird zum Zuordnen von SSO-Konfigurationen (Single Sign-On) zu bestimmten Benutzerattributen oder Gruppen verwendet. Sie können dieses Feld so konfigurieren, dass mehrere SSO-Setups für interne Benutzer basierend auf ihrer Organisation, ihrem Standort oder anderen Kriterien aktiviert werden.

### Externe Teilnehmer

Im Bereich &quot;Externe Benutzer&quot; in Adobe Learning Manager können Sie externe Teilnehmer verwalten, z. B. Partner oder Agenturen, die eingeschränkten Zugriff auf das Adobe Learning Manager-Konto benötigen. Dieser Abschnitt enthält Tools zum Erstellen von Registrierungsprofilen, zum Verwalten externer Benutzergruppen und zum Konfigurieren von Einstellungen, die für externe Teilnehmer spezifisch sind.

Externe Benutzer können sich wie folgt anmelden:

* Adobe ID: Externe Benutzer können sich mit ihren Adobe ID-Anmeldeinformationen anmelden.
* Single Sign-On (SSO): Externe Benutzer können sich über SSO anmelden, wenn dies vom Administrator konfiguriert wurde.
* Adobe Learning Manager-ID: Externe Benutzer können einen Learning Manager-Benutzernamen und ein Kennwort erstellen, um auf die Plattform zuzugreifen.

**Wichtigste Punkte:**

* Sie können eine oder mehrere Anmeldemethoden für externe Benutzer aktivieren.
* Wenn die Adobe Learning Manager-ID aktiviert ist, müssen externe Benutzer ihre eigenen Anmeldeinformationen erstellen.
* SSO kann je nach organisatorischen Anforderungen für externe Benutzer konfiguriert werden.

### SSO-Konfiguration in Adobe Learning Manager

Adobe Learning Manager unterstützt Single Sign-on (SSO), damit Benutzer sich einmal authentifizieren und Zugriff auf mehrere Anwendungen erhalten. Administratoren können SSO für interne und externe Benutzer mithilfe von SAML 2.0-basierten Anbietern konfigurieren.

Weitere Informationen finden Sie unter [SSO-Anmeldungen in Adobe Learning Manager](/help/migrated/administrators/feature-summary/multiple-sso-logins.md).

>[!NOTE]
>
>* Einem Konto können bis zu 20 SSO-Konfigurationen hinzugefügt werden.
>* Wenden Sie sich an den Adobe-Support, um Unterstützung für SSO-Anbieter mit SAML 2.0 zu erhalten.

## Datenquellen

Datenquellen ermöglichen es Ihnen oder Integrationsadministratoren, externe Systeme zum Importieren und Synchronisieren von Benutzer- und Lerndaten zu integrieren. Diese Funktion stellt eine nahtlose Datenverwaltung und Synchronisierung mit Systemen wie HRMS, Salesforce, FTP und anderen sicher.

**Beispiele für Datenquellentypen**

* **FTP-Connectors**: FTP-basierte Datenquellen ermöglichen es Organisationen, Benutzerdatendateien über sichere Dateiübertragungsprotokolle direkt in Adobe Learning Manager hochzuladen. Diese Verbindungen sind besonders für den Batch-Import von Benutzerinformationen, Kursregistrierungen und anderen Massendatenvorgängen nützlich.
* **Integrationen von Drittanbietern**: Adobe Learning Manager unterstützt die Integration mit verschiedenen Unternehmenssystemen über vorkonfigurierte Connectoren. Diese Integrationen können HR-Management-Systeme, Plattformen für Customer Relationship Management und andere Lernmanagement-Systeme umfassen.
*** Salesforce-Integration**: Der Salesforce-Connector ermöglicht die direkte Synchronisation von Benutzerdaten, Kursinformationen und Lerndatensätzen zwischen Salesforce und Adobe Learning Manager.

Weitere Informationen finden Sie unter [Connectors in Adobe Learning Manager](/help/migrated/integration-admin/feature-summary/connectors.md).

## Peer-Konten

Über Peer-Konten in Adobe Learning Manager können Sie erworbene Lizenzen freigeben und Berichte über zugeordnete Konten hinweg anzeigen. Diese Funktion ist nützlich für Organisationen, die zusammenarbeiten oder Ressourcen zwischen verschiedenen Konten austauschen müssen.

Weitere Informationen finden Sie unter [Peer-Konten](/help/migrated/administrators/feature-summary/peer-account.md) in Adobe Learning Manager.






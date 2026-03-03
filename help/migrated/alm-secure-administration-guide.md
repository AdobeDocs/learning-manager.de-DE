---
title: Adobe Learning Manager - sicherer Administrationshandbuch
description: Dieser Leitfaden beschreibt Sicherheitseinstellungen, -rollen und bewährte Verfahren für die Verwaltung der administrativen Sicherheit und der Zugriffskontrolle in Adobe Learning Manager, um Compliance und Sicherheit zu gewährleisten.
jcr-language: en-us
exl-id: 67dd9334-9718-4b2a-841e-5d8bd5c42714
source-git-commit: 5682c45a4e5789a3eede53faf7cb257cd9685759
workflow-type: tm+mt
source-wordcount: '2354'
ht-degree: 0%

---

# Administrative Sicherheitseinstellungen und Auswirkungen auf die Sicherheit

## Administratorrollen mit Auswirkungen auf die Sicherheit

Adobe Learning Manager verwendet ein rollenbasiertes Zugriffssteuerungsmodell (RBAC). In der folgenden Tabelle sind die FedRAMP-Kontoebenen den ALM-Rollen zugeordnet, auf die in diesem Dokument verwiesen wird:

| FedRAMP-Begriff | ALM-Rolle | Sicherheitsrelevanz |
|-------------|---------|------------------|
| Administratorkonto der obersten Ebene | Administrator | Umfassende Kontrolle auf Kontoebene. Exklusiver Zugriff auf alle in diesem Dokument beschriebenen sicherheitsrelevanten Einstellungen. Dies ist die Rolle, auf die in diesem Leitfaden Bezug genommen wird, wenn der Begriff &quot;oberstes Verwaltungskonto&quot; verwendet wird. |
| Berechtigtes Konto (Umfang) | Benutzerdefinierter Administrator | Delegierter administrativer Zugriff, der sich auf bestimmte Funktionen, Benutzergruppen oder Kataloge erstreckt. Zugriff auf Sicherheitseinstellungen auf Kontoebene nur möglich, wenn dies explizit gewährt wurde. |
| Privilegiertes Konto (Integration) | Integrationsadministrator | Verwaltet Integrationen, API-Registrierungen und Connector-Konfigurationen. Erhöhte Rechte für die Integrationsverwaltung. Andere Sicherheitseinstellungen auf Kontoebene können nicht geändert werden. |

>[!NOTE]
>
>Nur Benutzer, denen diese Rollen explizit zugewiesen wurden, können administrative oder sicherheitsrelevante Einstellungen ändern. Sofern nicht anders angegeben, können ausschließlich Administratoren auf die in den Abschnitten 3-7 dokumentierten Einstellungen zugreifen.

## Anmelde- und Authentifizierungseinstellungen

Die Anmelde- und Authentifizierungseinstellungen steuern, wie alle Benutzer - einschließlich Administratoren - auf die ALM-Plattform zugreifen. Diese Einstellungen werden ausschließlich von der Administratorrolle konfiguriert und haben direkte und erhebliche Auswirkungen auf die Sicherheitslage des gesamten Kontos.

### Konfiguration der Anmeldemethode

**Speicherort:** ALM-Administrator > Einstellungen > Anmeldemethoden

Der Administrator steuert die Authentifizierungsmethode, die für alle internen und externen Benutzer verwendet wird. Folgende Optionen stehen zur Auswahl:

- **Adobe ID:** Benutzer authentifizieren sich über ihr persönliches Adobe-Konto. Von Adobe verwaltet, nicht vom Unternehmen.
- **Single Sign-On (SSO) über SAML 2.0:** Benutzer authentifizieren sich über den Identitätsanbieter (IdP) der Organisation. Die Organisation verfügt über die vollständige Kontrolle über Authentifizierung, MFA und Sitzungsrichtlinie.
- **Learning Manager-ID:** Nur für externe Benutzer verfügbar. Benutzer erstellen einen plattformspezifischen Benutzernamen und ein plattformspezifisches Kennwort.
- **Mehrere SSO-Konfigurationen:** Es können bis zu 20 SSO-Konfigurationen hinzugefügt werden, um verschiedene Benutzergruppen, Standorte oder Unternehmensbereiche zu unterstützen.

| Anmeldemethode | Sicherheitsauswirkungen | Empfehlung |
|-------------|---------------------|----------------|
| **Adobe ID** | Die Organisation hat keine Kontrolle über Kennwortrichtlinien, MFA oder die Kontowiederherstellung. Ein kompromittiertes persönliches Adobe-Konto gewährt Zugriff auf die ALM-Plattform. | **NICHT EMPFOHLEN** für administrative oder interne Benutzer. Verwenden Sie diese Option nur, wenn SSO nicht verfügbar ist. |
| **SSO (SAML 2.0 / Federated ID)** | Die Authentifizierung wird vollständig vom IdP der Organisation gesteuert. MFA, Sitzungszeitüberschreitungen und Richtlinien für bedingten Zugriff werden auf IdP-Ebene erzwungen. Sofortiger Widerruf bei Benutzerabreise. | **EMPFOHLEN** für alle internen Benutzer und Administratoren. Bietet die höchste Stufe der Organisationssteuerung. |
| **Learning Manager-ID** | Benutzer verwalten Kennwörter außerhalb der Identitätsinfrastruktur der Organisation selbst. MFA kann nicht über ALM erzwungen werden. Die Kennwortsicherheit hängt vom Benutzerverhalten ab. | Gilt nur für externe Benutzer. Nicht geeignet für Mitarbeiter oder Administratoren. |

>[!CAUTION]
>
>Wenn die Anmeldemethode für interne Benutzer auf Adobe ID festgelegt ist, verliert das Unternehmen die Möglichkeit, eine Multi-Faktor-Authentifizierung durchzusetzen, die Komplexität des Kennworts zu steuern oder den Zugriff sofort zu widerrufen, wenn ein Benutzer das Programm verlässt. Dies erhöht das Risiko eines unberechtigten Zugriffs erheblich.

Weitere Informationen finden Sie unter [Benutzerdefinierte Rollen](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role).

### Multi-Factor Authentication (MFA)

**Speicherort:** Adobe Admin Console > Einstellungen > Datenschutz und Sicherheit > Authentifizierungseinstellungen

Die MFA-Erzwingung für **Adobe ID**- und **Enterprise ID**-Benutzer wird vom **Systemadministrator** in der Adobe Admin Console konfiguriert, nicht in der ALM-Anwendung selbst.  Für **Federated ID-/SSO**-Benutzer wird die MFA beim Identitätsanbieter der Organisation erzwungen.

- **Erzwungene 2FA:** Benutzer können die zweistufige Verifizierung nicht deaktivieren. Bietet zuverlässigen Schutz vor Diebstahl und Phishing.
- **Optionale 2FA:** Benutzer wählen aus, ob die 2-Schritte-Bestätigung aktiviert werden soll. Deutlich schwächere Sicherheitslage.
- **MFA nicht konfiguriert:** Der Zugriff wird nur durch Kennwörter geschützt. Hohes Risiko, insbesondere für die Buchführung der Verwaltung.

>[!IMPORTANT]
>
>Bei Verwaltungskonten ohne MFA ist das Risiko eines unbefugten Zugriffs deutlich höher. Eine beschädigte Administratorberechtigung ohne MFA gewährt die vollständige Kontokontrolle, einschließlich der Möglichkeit, alle Sicherheitseinstellungen zu ändern.

### Sitzungslebensdauer und Leerlaufzeitüberschreitung

**Speicherort:** Adobe Admin Console > Einstellungen > Datenschutz und Sicherheit > Erweiterte Einstellungen

Der **Systemadministrator** konfiguriert die maximale Lebensdauer der aktiven Sitzung und das Zeitlimit für die Leerlaufsitzung für das Unternehmen. Diese Einstellungen gelten für alle Benutzer, einschließlich Administratoren.

- **Max. Sitzungsdauer:** Erzwingt eine erneute Authentifizierung nach einem definierten Zeitraum, unabhängig von der Aktivität. Beschränkt das Zeitfenster für den Fall, dass eine Sitzung gefährdet ist.
- **Max. Leerlaufzeit:** Beendet Sitzungen, die für einen definierten Zeitraum inaktiv waren. Schützt vor unbeaufsichtigten authentifizierten Sitzungen auf freigegebenen oder entsperrten Geräten.

## Einstellungen für Rollenzuweisung und Berechtigungsbereich

Die Einstellungen für die Rollenzuweisung und den Berechtigungsbereich bestimmen, wer in ALM über Administratorzugriff verfügt und was er tun kann. Diese gehören zu den am stärksten betroffenen Sicherheitseinstellungen in der Plattform. Nur die Administratorrolle kann Administratorrollen erstellen, zuweisen, ändern oder widerrufen.

### Zuweisung von Administratorrollen

**Speicherort:** ALM-Administrator > Benutzer > Intern > Aktionen > Rolle zuweisen/Rolle entfernen

Der **Administrator** kann die folgenden Rollen erteilen oder widerrufen:

- **Administrator:** Vollständiger Zugriff auf Kontoebene
- **Autor:** Zugriff auf die Inhaltserstellung
- **Benutzerdefinierter Administrator:** administrativer Zugriff (siehe Abschnitt 4.2)
- **Integrationsadministrator:** Integration und API-Zugriff (siehe Abschnitt 7)

| Einstellung / Aktion | Sicherheitsauswirkungen | Empfohlene Vorgehensweisen |
|---|---|---|
| **Administratorrolle wird gewährt** | Vollständige Kontrolle über Konten. Ein Benutzer mit dieser Rolle kann alle Einstellungen in diesem Dokument ändern, einschließlich der Neukonfiguration der Authentifizierung und des Widerrufens des Zugriffs anderer Administratoren. | Weisen Sie nur einer Mindestanzahl von Benutzern mit einer bestätigten Geschäftsanforderung zu. Führen Sie eine dokumentierte Liste aller Inhaber von Administratorrollen. |
| **Fehler beim Widerrufen von Rollen bei der Abreise** | Abgegangene Benutzer behalten den Zugriff auf administrative Funktionen. Risiko von unbefugtem Zugriff, Datenexfiltration oder Sabotage. | Entfernen Sie Rollen sofort, wenn sich die Beschäftigungs- oder Verwaltungsaufgaben eines Benutzers ändern. Durchführen regelmäßiger Zugriffsüberprüfungen |
| **Übermäßige Zuweisung allgemeiner Rollen** | Ein umfassender administrativer Zugriff erhöht die potenziellen Auswirkungen eines beschädigten Kontos und verringert die Rechenschaftspflicht für Verwaltungsaktionen. | Wendet den Grundsatz der geringsten Privilegien an. Bevorzugen Sie Rollen mit Umfang (z. B. &quot;Benutzerdefinierter Administrator&quot;), wo möglich. |

### Konfiguration benutzerdefinierter Administratorrollen

**Speicherort:** ALM-Administrator > Benutzer > Benutzerdefinierte Rollen > Rolle erstellen

Wenden Sie den Grundsatz der **geringsten Berechtigung** an. Verwenden Sie **Benutzerdefinierte Administratorrollen**, um bestimmte Funktionen zu delegieren (siehe Abschnitt 4.2).

Der **Administrator** kann benutzerdefinierte Rollen erstellen, die eine definierte Teilmenge von Administratorberechtigungen gewähren. Benutzerdefinierte Rollen können auf bestimmte Benutzergruppen, Kataloge oder Funktionssätze beschränkt werden, wodurch die Reichweite delegierten Administratorzugriffs eingeschränkt wird.

**Verfügbare Berechtigungskategorien:**

- **Kontoberechtigungen:** Zugriff auf systemweite Konfigurationen wie Ankündigungen, Gamification, Kenntnisse und Benutzerverwaltung.
- **Funktionsberechtigungen (Kern):** Zugriff auf Kataloge, Berichte und Tags.
- **Funktionsberechtigungen (Lernobjekte):** Zugriff auf Kurse, Zertifizierungen, Lernpfade und Arbeitshilfen.
- **Umfang:** Beschränken Sie die Rolle auf bestimmte Benutzergruppen und/oder Kataloge.

| Konfigurationsentscheidung | Sicherheitsauswirkungen | Empfohlene Vorgehensweisen |
|---|---|---|
| **Erstellen einer übermäßig breiten benutzerdefinierten Rolle** | Eine benutzerdefinierte Rolle mit überhöhten Berechtigungen bietet gegenüber der vollständigen Administratorrolle nur einen geringen Sicherheitsvorteil und erhöht den Explosionsradius eines beschädigten Kontos. | Der Umfang benutzerdefinierter Rollen entspricht dem Mindestsatz an Berechtigungen, die für die jeweilige Funktion erforderlich sind. Bevorzugen Sie katalogspezifische und Benutzergruppenspezifische Rollen. |
| **Einstellungszugriff auf einen benutzerdefinierten Administrator gewähren** | Benutzerdefinierte Administratoren mit Zugriff auf Einstellungen können Anmeldemethoden, Benachrichtigungseinstellungen und andere Konfigurationen auf Kontoebene ändern. | Gewähren Sie Einstellungen nur dann Zugriff auf benutzerdefinierte Rollen, wenn dies explizit erforderlich ist. Überprüfen Sie regelmäßig, welche benutzerdefinierten Rollen über diese Berechtigung verfügen. |
| **Benutzerdefinierte Rollenzuweisungen werden nicht überwacht** | Nicht dokumentierte oder nicht überprüfte benutzerdefinierte Rollen können sich im Laufe der Zeit ansammeln und zu neuen Berechtigungen führen. | Laden Sie regelmäßig den Bericht zu benutzerdefinierten Rollen (**Benutzer > Benutzerdefinierte Rollen > Download**) herunter, und überprüfen Sie alle aktiven benutzerdefinierten Rollenzuweisungen. |

## Einstellungen für Benutzerbereitstellung und Zugriffsverwaltung

Einstellungen für die Benutzerbereitstellung steuern, wie Benutzer zur Plattform hinzugefügt werden, wie lange sie aktiv bleiben und wann ihre Daten entfernt werden. Diese Einstellungen werden ausschließlich von der Administratorrolle konfiguriert und haben direkte Auswirkungen auf die Sicherheit der Datenexposition und die Zugriffskontrolle.

| Einstellung | Standort | Sicherheitsauswirkungen | Empfohlene Standardeinstellung |
|---|---|---|---|
| **Automatisches Löschen eines inaktiven Benutzers** | ALM-Administrator > Einstellungen > Allgemein | Ohne automatische Löschung werden inaktive Konten kumuliert. Ruhende Konten sind ein häufiges Ziel für nicht autorisierten Zugriff, da sie möglicherweise nicht überwacht werden. | Aktivieren. Legen Sie einen Aufbewahrungszeitraum fest, der an die Unternehmensrichtlinie angepasst ist (z. B. 90 Tage Inaktivität). |
| **Ablauf des externen Benutzerprofils** | ALM-Administrator > Benutzer > Extern > Profil hinzufügen | Externe Benutzerprofile ohne Ablaufdatum bleiben unbegrenzt zugänglich. Partner oder Auftragnehmer, die keinen Zugriff mehr benötigen, behalten einen aktiven Einstiegspunkt. | Legen Sie ein Ablaufdatum für jedes externe Benutzerprofil zur Erstellungszeit fest. |
| **Steuerelemente für die Selbstregistrierung** | ALM-Administrator > Benutzer > Intern > Hinzufügen > Selbstregistrierung | Über einen Link zur Selbstregistrierung kann jeder Benutzer mit der URL ein Teilnehmerkonto erstellen. Wenn sie nicht verwaltet wird, kann dies dazu führen, dass nicht autorisierte oder unerwartete Benutzer Zugriff auf die Plattform erhalten. | Generieren Sie Links zur Selbstregistrierung nur, wenn dies erforderlich ist. Deaktivieren oder widerrufen Sie nicht verwendete Links umgehend. |
| **Anhalten/Fortsetzen des externen Profils** | ALM-Administrator > Benutzer > Extern > Aktionen > Anhalten | Wenn Sie ein externes Profil anhalten, können sich neue Benutzer nicht registrieren, haben aber keine Auswirkungen auf bereits registrierte Benutzer. Wenn inaktive externe Profile nicht angehalten werden, kann dies zu unbeabsichtigten Registrierungen führen. | Halten Sie externe Profile an, wenn die Registrierung nicht mehr erforderlich ist. Löschen Sie Profile, die dauerhaft inaktiv sind. |
| **Benutzer löschen und bereinigen** | ALM-Administrator > Benutzer > Intern > Aktionen > Löschen/Benutzerbereinigung > Bereinigen | Gelöschte Benutzer werden deaktiviert, ihre Daten werden jedoch beibehalten. Beim Bereinigen werden alle Benutzerdaten dauerhaft entfernt. Wenn veraltete Benutzer nicht bereinigt werden, werden möglicherweise sensible Lerndatensätze und personenbezogene Daten über den erforderlichen Aufbewahrungszeitraum hinaus aufbewahrt. | Bereinigung von Benutzerdatensätzen im Einklang mit Datenaufbewahrungs- und Datenschutzrichtlinien des Unternehmens Das Bereinigen ist unumkehrbar. |

>[!IMPORTANT]
>
>Das Bereinigen ist dauerhaft und unumkehrbar. Alle Lerndatensätze, Registrierungsdaten und Benutzerinformationen werden gelöscht. Wenn ein bereinigter Benutzer in Connector-Konfigurationen referenziert wird, werden diese Connectors deaktiviert. Bestätigen Sie die Auswahl sorgfältig, bevor Sie eine Bereinigung durchführen.

## Reporting- und Datenzugriffseinstellungen

Reporting- und Datenzugriffseinstellungen legen fest, welche Benutzer Plattformdaten anzeigen, generieren und exportieren können. Fehlkonfigurationen dieser Einstellungen können dazu führen, dass vertrauliche persönliche, organisatorische oder Compliance-bezogene Informationen angezeigt werden.

| Einstellung | Standort | Sicherheitsauswirkungen | Empfohlene Standardeinstellung |
|---|---|---|---|
| **Berichtszugriff auf benutzerdefinierte Rollen wird gewährt** | ALM-Administrator > Benutzer > Benutzerdefinierte Rollen > Funktionsberechtigungen > Berichte | Berichte können personenbezogene Informationen (PII), Kursabschlussdaten, Bewertungsergebnisse und den Fortschritt der Teilnehmer enthalten. Der Zugriff auf Berichtsfunktionen sollte auf Benutzer mit nachgewiesenen Geschäftsanforderungen beschränkt sein. | Gewähren Sie dem Bericht nur Zugriff auf Rollen mit einem bestimmten, dokumentierten Bedarf. Schreibgeschützter Zugriff, wenn kein Schreibzugriff erforderlich ist. |
| **Vollständige Kontrolle und schreibgeschützter Berichtsbereich** | ALM-Administrator > Benutzer > Benutzerdefinierte Rollen > Kontoübersichtsbericht | Vollständige Kontrolle über den Kontoübersichtsbericht gewährt dem benutzerdefinierten Administrator Transparenz über alle Benutzergruppen und Kataloge, unabhängig vom Rollenbereich. Dadurch können Daten verfügbar gemacht werden, die außerhalb des vorgesehenen Bereichs einer Administratorrolle mit Umfang liegen. | Vollständige Kontrolle über den Kontoübersichtsbericht gewähren: Dies gilt nur für Rollen, für die eine Transparenz der Berichterstattung in der gesamten Organisation erforderlich ist. |
| **xAPI- und E-Mail-Berichtszugriff** | ALM-Administrator > Benutzer > Benutzerdefinierte Rollen | xAPI-Berichte und E-Mail-Berichte sind nur für die vollständige Administratorrolle verfügbar. Diese Berichte können detaillierte Verhaltens- und Kommunikationsdaten enthalten. Der Zugriff ist durch den Entwurf eingeschränkt. | Versuchen Sie nicht, den Zugriff auf xAPI- oder E-Mail-Berichte über benutzerdefinierte Rollen zu delegieren. Diese sind nur als Administrator konzipiert. |
| **Benutzerdaten exportiert** | ALM-Administrator > Benutzer > Intern > Benutzerdaten exportieren | Die Funktion Benutzerdaten exportieren generiert eine herunterladbare Datei, die alle internen Benutzerdatensätze enthält. Diese Daten müssen im Einklang mit den Sicherheits- und Datenschutzrichtlinien des Unternehmens behandelt werden. | Beschränkung der Exportkapazität auf autorisiertes Personal. Behandeln Sie exportierte Daten als vertraulich. Speichern oder übertragen Sie sie nicht außerhalb genehmigter Systeme. |

## Einstellungen für Integration und API-Zugriff

Die Einstellungen für Integration und API-Zugriff steuern die Verbindung externer Systeme mit Adobe Learning Manager. Diese Einstellungen erweitern den Zugriff über die ALM-Benutzeroberfläche hinaus und können, wenn sie falsch konfiguriert sind, Plattformdaten und -funktionen für nicht autorisierte Systeme verfügbar machen.  Die Integrationseinstellungen werden von der Rolle &quot;Integrationsadministrator&quot; verwaltet. Die vollständige Administratorrolle behält die Möglichkeit, registrierte Anwendungen zu überprüfen, zu genehmigen und zu widerrufen.

| Einstellung | Standort | Sicherheitsauswirkungen | Empfohlene Standardeinstellung |
|---|---|---|---|
| **API-Anwendungsregistrierung** | Integrationsadministrator > Anwendungen > Registrieren | Durch die Registrierung einer Anwendung werden OAuth 2.0-Anmeldeinformationen (Client-ID und Geheimnis) erstellt, mit denen auf ALM-Daten und -Funktionen programmgesteuert zugegriffen werden kann. Übermäßig breite OAuth-Geltungsbereiche (z. B. Lese-/Schreibzugriff für die Admin-Rolle) gewähren vollständigen administrativen API-Zugriff. | Gewähren Sie die mindestens erforderlichen OAuth-Geltungsbereiche. Überprüfen und widerrufen Sie regelmäßig ungenutzte oder veraltete Anwendungsregistrierungen. Clientanmeldeinformationen als vertrauliche Geheimnisse behandeln. |
| **OAuth-Anwendungsbereich** | Integrations-Admin > Anwendungen > Registrieren > Geltungsbereiche | Die verfügbaren OAuth-Geltungsbereiche reichen vom Lese-/Schreibzugriff für Teilnehmer bis hin zum Lese-/Schreibzugriff für Administratoren. Mit der Lese-/Schreibberechtigung für die Administratorrolle kann eine Anwendung alle Daten ändern, die ein Administrator ändern kann, einschließlich Benutzerrollen und Sicherheitseinstellungen. | Verwenden Sie den restriktivsten OAuth-Bereich, der die Anforderungen der Integration erfüllt. Gewähren Sie niemals Lese-/Schreibzugriff für die Administratorrolle, es sei denn, dies ist unbedingt erforderlich. |
| **Connector-Konfiguration (FTP, Salesforce, HRIS usw.)** | Integrations-Admin > Connectors | Connectors ermöglichen den automatischen Import und Export von Benutzerdaten, Kenntnissen und Kursabschlüssen. Fehlkonfigurierte Connectors können falsche Benutzerdaten importieren, unbeabsichtigte Rollen zuweisen oder vertrauliche Daten an nicht autorisierte Ziele exportieren. | Überprüfen Sie alle aktiven Connector-Konfigurationen regelmäßig. Sicherstellen, dass Datenquellen und -ziele autorisiert sind Deaktivieren Sie Connectors, die nicht mehr verwendet werden. |
| **Webhook-Konfiguration** | Integrationsadministrator > Webhooks | Webhooks senden Echtzeit-ALM-Ereignisdaten (Registrierungen, Abschlüsse, Benutzeränderungen) an eine angegebene externe URL. Ein falsch konfigurierter oder kompromittierter Webhook-Endpunkt kann zu Datenexfiltration oder Offenlegung sensibler Teilnehmerereignisse führen. | Registrieren Sie nur verifizierte, von der Organisation genehmigte Webhook-URLs. Überprüfen Sie regelmäßig die aktiven Webhook-Konfigurationen. Entfernen Sie inaktive oder nicht erkannte webhooks sofort. |
| **LTI-Integrationskonfiguration** | Integrationsadministrator > LTI-Integrationen | Die LTI-Integration ermöglicht es ALM, als LTI-Anbieter oder -Verbraucher zu agieren, wodurch externe LMS-Plattformen auf ALM-Kurse zugreifen können. Nach der Aktivierung kann LTI nicht mehr deaktiviert werden. Verfügbare LTI-Anmeldedaten können einen nicht autorisierten Zugriff auf Kursinhalte ermöglichen. | Aktivieren Sie LTI nur, wenn eine bestätigte Integrationsanforderung vorhanden ist. LTI-Anmeldeinformationen als vertraulich behandeln. Geben Sie die Anmeldeinformationen nur für autorisierte LMS-Administratoren frei. |

## Administratorkonfigurationsaufgaben und gemeinsame Verantwortung

Die Verwaltungseinstellungen in Adobe Learning Manager können von Kunden konfiguriert werden und sind Teil der vom Kunden verwalteten Sicherheitskontrollen im Rahmen des Modells der gemeinsamen Verantwortung des Adobe.

| Adobe-Zuständigkeiten | Verantwortung des Kunden |
|---|---|
| Sicherer Betrieb der ALM-Plattform und der zugrunde liegenden Infrastruktur. | Konfiguration aller Administratorrollen und Berechtigungen. |
| Durchsetzung des rollenbasierten Zugriffssteuerungsmodells (RBAC). | Auswählen und Erzwingen geeigneter Anmeldemethoden und MFA. |

Weitere Informationen zu den Sicherheitspraktiken von Adobe Learning Manager finden Sie unter:

**Referenz:** [Überblick über die Sicherheit von Adobe Learning Manager (PDF)](https://experienceleague.adobe.com/docs/learning-manager/assets/alm-security-whitepaper-2024.pdf)

## Dokumentenverwaltung

Dieses Dokument kann regelmäßig aktualisiert werden, um Änderungen an der Funktionalität von Adobe Learning Manager oder an den Sicherheitsrichtlinien Rechnung zu tragen. Die Version und das Datum der letzten Aktualisierung werden in den Dokument-Metadaten und im FedRAMP-Autorisierungspaket beibehalten. Kunden sollten die öffentlich verfügbare Version auf Adobe Experience League nutzen, um sicherzustellen, dass sie die neuesten Anleitungen verwenden.

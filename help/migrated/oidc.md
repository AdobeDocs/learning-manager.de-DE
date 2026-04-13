---
description: Erfahren Sie mehr über die OIDC-Anmeldemethode
jcr-language: en_us
title: Anmelden bei Adobe Learning Manager mit OpenID Connect
source-git-commit: 7c430e3fbb2716455310f2130d73af10ce2e56c7
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---


# Anmelden bei Adobe Learning Manager mit OpenID Connect (OIDC)

Erfahren Sie, wie die OpenID Connect-Anmeldung in Adobe Learning Manager für Teilnehmer, Autoren und Administratoren funktioniert. In diesem Artikel wird die Erfahrung behandelt, nicht die Implementierung.

## OpenID Connect-Anmeldung

OpenID Connect (OIDC) ist eine gängige Anmeldemethode, die auf Webstandards basiert. Viele Unternehmen verwenden einen Identitätsanbieter (z. B. Okta, Google Workspace oder Microsoft Entra ID) für Mitarbeiter und Partner.

Wenn Ihr Unternehmen OIDC für Adobe Learning Manager aktiviert:

* Sie melden sich mit der üblichen Anmeldeseite Ihrer Organisation an und nicht mit einem Kennwort, das nur für Adobe Learning Manager gilt, es sei denn, Ihre Organisation wählt etwas Anderes aus.
* Nachdem Sie sich authentifiziert haben, erhält Adobe Learning Manager die Informationen, die Ihr Unternehmen zulässt (z. B. Ihre E-Mail- und Profilattribute), und öffnet die richtige Erfahrung für Sie: Teilnehmer, Autor, Administrator oder andere Rollen, die Ihr Konto unterstützt.

OIDC ist eine Alternative zu anderen Anmeldeoptionen, die Ihr Konto möglicherweise anbietet, z. B. Adobe ID oder SAML-basiertes Single Sign-on (SSO). Ihr Administrator bestimmt, welche Methoden verfügbar sind.

## Gründe, warum Organisationen sich für OpenID Connect entscheiden

Unternehmen entscheiden sich häufig für OIDC aus folgenden Gründen:

* Benutzer können dieselbe Unternehmens- oder Cloud-Identität wie für andere Anwendungen nutzen.
* Kennwortrichtlinien, Multi-Faktor-Authentifizierung und Kontolebenszyklus werden im Identitätsanbieter verwaltet, der mit anderen Enterprise-Anwendungen konsistent ist.
* OIDC folgt aus Benutzer- und IT-Perspektive ähnlichen Mustern wie andere moderne Anmelde-Flows, ohne dass der mit einigen SAML-reinen Setups verbundene stärkere Dokumentaustausch erforderlich ist.

Ihre Erfahrung bleibt unverändert: Gehen Sie zum Learning Manager, melden Sie sich an, wo Ihr Unternehmen es Ihnen sagt, und landen Sie in der App.

## Was Sie sehen, wenn Sie sich anmelden

### Adobe Learning Manager öffnen

Sie können Folgendes verwenden:

* Die Haupt-Adobe Learning Manager-URL für Ihre Umgebung
* Eine von Ihrer Organisation konfigurierte benutzerdefinierte Domäne, falls zutreffend
* einen Link aus einer E-Mail, einer Einladung oder einer Seite zur Selbstregistrierung
* Ein Lesezeichen oder ein Deep-Link zu einem bestimmten Kurs, einer bestimmten Katalogseite oder einer bestimmten Ressource

Wenn Ihr Konto OIDC verwendet, wird Ihr Browser bei der Anmeldung in der Regel an den Identitätsanbieter Ihrer Organisation umgeleitet.

### Anmelden mit Ihrer Organisation

Geben Sie auf der Seite Ihres Identitätsanbieters Ihre Anmeldeinformationen ein und führen Sie alle zusätzlichen Schritte aus, die Ihre Organisation benötigt, z. B. die Multi-Faktor-Authentifizierung. Dieser Schritt erfolgt außerhalb des Anmeldeformulars von Adobe Learning Manager, wenn OIDC verwendet wird. Aus Ihrer Sicht ist es wie eine Anmeldung bei Ihrem Unternehmens- oder Bildungseinrichtungskonto. Möglicherweise werden in diesem Schritt keine technischen Begriffe wie *OIDC* oder *OAuth* angezeigt.

### Zurück zu Adobe Learning Manager

Nach erfolgreicher Anmeldung kehrt Ihr Browser zu Adobe Learning Manager zurück. Anschließend wird das Produkt:

* Erkennt Sie anhand der E-Mail- und Profilinformationen, die Ihr Identitätsanbieter gemäß den Einstellungen Ihrer Organisation freigibt.
* Wendet Ihre Berechtigungen in Adobe Learning Manager an (Teilnehmer, Autor, Administrator, Integrationsadministrator usw.)
* Öffnet die entsprechende App oder den entsprechenden Bereich (z. B. das Teilnehmererlebnis im Vergleich zu dem Erlebnis als Administrator oder Autor), entsprechend der Art und Weise, wie Adobe Learning Manager Ihrem Konto Rollen zuweist

Wenn etwas schief geht (z. B. wenn Ihr Konto nicht bereitgestellt wird oder Ihre Organisation den Zugriff blockiert), wird möglicherweise ein Fehler angezeigt oder Sie können nicht fortfahren. Wenden Sie sich an Ihr internes IT-Team oder an den Adobe Learning Manager-Administrator.

## Andere Anmeldeoptionen für OpenID Connect verwenden

Adobe Learning Manager kann mehrere Anmeldemethoden für ein Konto unterstützen (mehrere SSO-Optionen). Beispiel:

* Einige Benutzer melden sich mit Adobe ID an
* Andere verwenden SAML SSO
* Andere verwenden OIDC

Welche Optionen Ihnen angezeigt werden, hängt davon ab, wie Ihr Konto konfiguriert ist. Wenn Sie OIDC für Ihre Organisation aktivieren, werden andere Methoden nicht automatisch entfernt, es sei denn, Ihre Administratoren ändern diese Konfiguration.

## Unterstützte Funktionen und Szenarien

Die folgenden Verhaltensweisen werden unterstützt, wenn Ihr Unternehmen OIDC mit Adobe Learning Manager verwendet, was der Funktionsweise anderer Anmeldemethoden für Unternehmen entspricht.

### Tabelle 1. OIDC-Unterstützung in gängigen Szenarien

| Bereich | Was es für Sie bedeutet |
| --- | --- |
| Interne und externe Benutzer | Mitarbeiter und eingeladene externe Benutzer (z. B. Partner) können OIDC verwenden, wo dies von Ihrem Administrator aktiviert wird, einschließlich Flows, die über Links zur Selbstregistrierung beginnen, wenn Ihr Konto dafür eingerichtet ist. |
| Erstmaliger Zugriff | Wenn Sie laut Richtlinie zulässig sind, kann Ihre erste erfolgreiche OIDC-Anmeldung Ihren Benutzer in Adobe Learning Manager gemäß den Regeln Ihres Unternehmens erstellen oder verknüpfen, ähnlich wie bei anderen SSO-Optionen. |
| Profil und Attribute | Informationen wie E-Mail und andere Attribute können von Ihrem Identitätsanbieter im Laufe der Zeit aktualisiert werden, sodass Ihr Adobe Learning Manager-Profil innerhalb der von Ihrem Administrator konfigurierten Grenzen mit dem Verzeichnis Ihrer Organisation übereinstimmt. |
| Tiefe Links | Links, die auf eine bestimmte Seite oder Ressource im Lern-Manager verweisen (nicht nur auf die Startseite), werden unterstützt. Sie können nach der Anmeldung auf den gewünschten Inhalten landen, wenn die Einrichtung Ihrer Organisation dies zulässt. |
| Rückgabepfad | Nach der Authentifizierung können Sie zu der Stelle zurückkehren, an der Sie versucht haben, zu gelangen (z. B. dieselbe Kurs- oder Katalog-URL, von der Sie gestartet haben), anstatt immer auf einer allgemeinen Startseite zu landen. |
| Benutzerdefinierte Domäne | Wenn Ihr Unternehmen einen benutzerdefinierten Hostnamen für Adobe Learning Manager verwendet, wird die OIDC-Anmeldung auch in diesem Kontext unterstützt. |
| Mobile | Die Anmeldung auf Smartphones und Tablets über unterstützte Browser oder Benutzererlebnisse wird unterstützt. |
| Publish zu Adobe Learning Manager (Prime) | Workflows, bei denen Inhalte aus verbundenen Tools in Learning Manager veröffentlicht werden, werden weiterhin unterstützt, wenn Ihr Konto OIDC verwendet, was mit Ihrer Integrationseinrichtung konsistent ist. |
| Bezeichnerbasierte Anmeldung | Wenn Ihr Konto (abgesehen von E-Mails) für übereinstimmende Konten auf stabilen Kennungen beruht, werden diese Flows für OIDC entsprechend der Konfiguration Ihres Administrators unterstützt. |

Wenn ein bestimmter Workflow nicht funktioniert, kann die Ursache in den Einstellungen des Identitätsanbieters, der Kontobereitstellung oder der Adobe Learning Manager-Rollenzuweisung liegen. Ihr Administrator kann dies überprüfen.

## Funktionsweise von Rollen nach der Anmeldung

Adobe Learning Manager bestimmt, was Sie über die Rollen und Berechtigungen Ihres Kontos und nicht über das OIDC-Protokoll selbst tun können. OIDC stellt nur fest, wer Sie zur Zufriedenheit Ihres Identitätsanbieters sind und was Ihr Unternehmen mit Adobe Learning Manager teilt.

* Teilnehmer sehen in der Regel Schulungen, Kataloge und Lernpläne.
* Autoren können Inhalte erstellen oder verwalten.
* Administratoren verwalten Benutzer, Konfiguration und Berichte.

Wenn du in dem falschen Bereich landest oder keinen Zugriff auf die Datei erwartest, bitte deinen Adobe Learning Manager-Administrator, dein Profil- und Gruppenabonnement zu überprüfen.

## Fehlerbehebung für häufige Probleme

### Tabelle 2. Fehlerbehebung bei der OIDC-Anmeldung

| Problem | Was Sie ausprobieren sollten |
| --- | --- |
| Schleife oder leere Seite umleiten | Löschen Sie Cookies für Ihre Learning Manager-URL und Ihren Identitätsanbieter, probieren Sie einen anderen Browser oder ein privates Fenster aus. Wenn das Problem weiterhin besteht, wenden Sie sich an die IT-Abteilung. Es kann vorkommen, dass sich unternehmensinterne Proxys oder Sitzungsrichtlinien für Identitätsanbieter gegenseitig beeinflussen. |
| &quot;Zugriff verweigert&quot; oder ähnlich nach Anmeldung beim Identitätsanbieter | Ihr Identitätsanbieter hat Sie akzeptiert, aber Adobe Learning Manager hat möglicherweise keinen entsprechenden Benutzer, oder Ihrem Konto fehlt eine Lizenz oder Rolle. Wenden Sie sich an Ihren Adobe Learning Manager-Administrator. |
| Falsche Sprach- oder Profildetails | Die Attributzuordnung wird von Ihrer Organisation gesteuert. Fragen Sie Ihren Administrator, ob Verzeichnisattribute das Gebietsschema oder die Profilfelder steuern sollen. |
| Deep-Link hat die Startseite anstelle der Ressource geöffnet | Das Verhalten von &quot;Rückkehrpfad&quot; und &quot;Deep-Link&quot; kann davon abhängen, wie der Link freigegeben wurde und von Ihrer Sitzung. Versuchen Sie den Link nach einer vollständigen Anmeldung erneut oder fragen Sie Ihren Administrator, ob das Link-Format für externe Benutzer unterstützt wird. |

## Was Administratoren wissen sollten

Wenn Sie Adobe Learning Manager für Ihr Unternehmen konfigurieren, wird OIDC mit der Anwendungsregistrierung Ihres Identitätsanbieters eingerichtet: Client-IDs, Endpunkte für die Autorisierung, Token, Benutzerinformationen und der Umleitungs-URL, die Adobe Learning Manager für die Anmeldung verwendet. Diese Werte stammen aus der Dokumentation Ihres Identitätsanbieters. Die Einstellungen müssen zwischen Ihrem Identitätsanbieter und dem Learning Manager übereinstimmen, damit Benutzer eine reibungslose Umleitung und Rückkehr sehen.

Endbenutzer müssen diese Werte nicht verwalten. Sie benötigen nur die richtige Lern-Manager-URL (oder benutzerdefinierte Domäne) und gegebenenfalls Einladungs- oder Selbstregistrierungslinks von Ihrem Team.

## Zusammenfassung

* Mit OIDC können sich Benutzer über den Standardidentitätsanbieter ihres Unternehmens bei Adobe Learning Manager anmelden, mit einem vertrauten Umleitungs- und Rückkehrfluss.
* Nach der Anmeldung verwendet Adobe Learning Manager E-Mail-Adressen und freigegebene Attribute, um den Benutzer zu identifizieren und Rollen (Teilnehmer, Autor, Administrator usw.) anzuwenden.
* Je nach Kontokonfiguration werden Selbstregistrierung, mehrere SSO-Optionen, Attributaktualisierungen, erstmalige Benutzerbereitstellung, Deep Links, Rückkehrpfad, benutzerdefinierte Domänen, Mobilgeräte, Publish zu Adobe Learning Manager und bezeichnerbasierte Zuordnung unterstützt.
* Andere Anmeldemethoden (z. B. Adobe ID oder SAML) bleiben verfügbar, wenn Ihre Administratoren sie aktiviert lassen.

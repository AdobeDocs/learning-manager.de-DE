---
title: Lebenszyklus des Administratorkontos für Adobe Learning Manager
description: Dieses Dokument enthält umfassende Anleitungen zur sicheren Verwaltung von Administratorkonten auf höchster Ebene in Adobe Learning Manager (ALM), um die FedRAMP-Konformität und bewährte Sicherheitsverfahren zu erfüllen.
jcr-language: en-us
source-git-commit: db3ed4dc44da75b418e923999bdf3776bf81b11f
workflow-type: tm+mt
source-wordcount: '2122'
ht-degree: 0%

---


# Administrative Kontotypen in Adobe Learning Manager

## ALM-Rollenzuordnung

In Adobe Learning Manager ist das Administratorkonto der obersten Ebene die Administratorrolle. Dies ist die Rolle, auf die in diesem Leitfaden immer dann Bezug genommen wird, wenn der FedRAMP-Begriff &quot;oberstes Verwaltungskonto&quot; verwendet wird. Benutzerdefinierte Administratoren und Integrationsadministratoren werden als privilegierte Konten (mit Umfang) behandelt.

In der folgenden Tabelle sind die FedRAMP-Kontoebenen den spezifischen Rollen zugeordnet, die in Adobe Learning Manager verwendet werden:

| FedRAMP-Begriff | ALM-Rollenname | Beschreibung |
|--------------------------------------|----------------------------|-------------|
| Administratorkonto der obersten Ebene | Administrator | Rolle mit höchsten Rechten in ALM. Vollständige Kontrolle über Benutzer, Rollen, Lerninhalte, Berichte, Integrationen und alle Systemkonfigurationen. Direkte Zuordnung zur FedRAMP-Definition des übergeordneten Administratorkontos. |
| Berechtigtes Konto (Umfang) | Benutzerdefinierter Administrator | Eine definierte Teilmenge von Administratorberechtigungen, die sich auf bestimmte Funktionen beziehen (z. B. Berichterstellung, Katalogverwaltung). Umfassende Kontrolle auf Kontoebene ist nicht möglich. |
| Privilegiertes Konto (Integration) | Integrationsadministrator | Verwaltet Integrationen und API-basierten Zugriff zwischen ALM und externen Systemen. Erhöhte Rechte gelten nur für die Integrationsverwaltung. |


Adobe Learning Manager verwendet ein rollenbasiertes Zugriffssteuerungsmodell (RBAC) zur Verwaltung des administrativen Zugriffs. Administratorrollen werden nur von autorisierten Administratoren zugewiesen.

Weitere Informationen finden Sie unter [Benutzerdefinierte Rollen in Adobe Learning Manager](https://experienceleague.adobe.com/de/docs/learning-manager/using/admin/custom-role).

## Identitätstypen und empfohlene Authentifizierung

Adobe Admin Console unterstützt drei Identitätstypen für Administratorkonten. Die Auswahl des Identitätstyps hat direkte Auswirkungen auf die Sicherheit:

| Identitätstyp | Beschreibung | Sicherheitsempfehlung |
|---------------------------|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| Adobe ID (Personal ID) | Standardtyp; wird von Adobe verwaltet. Jeder kann sie erstellen. | NICHT EMPFOHLEN für Administratoren. Die Organisation hat keine Kontrolle über diesen Kontotyp. |
| Enterprise ID | Das Unternehmenskonto wird von einem Admin Console-Systemadministrator verwaltet. | Akzeptierbar, wenn Federated ID/SSO nicht verfügbar ist. 2FA erzwingen. |
| Federated ID (SSO) | Unternehmenseigentum; integriert mit SAML 2.0 SSO. Die Organisation kontrolliert die Authentifizierung vollständig. | EMPFOHLEN: Authentifiziert über den IdP der Organisation und unterstützt die MFA-Erzwingung auf der Ebene des Identitätsanbieters. |

Weitere Informationen finden Sie unter:

* [Identitätstyp](https://helpx.adobe.com/de/enterprise/using/admin-console.html)
* [Sichere Benutzerauthentifizierung und Kennwörter](https://helpx.adobe.com/de/enterprise/using/authentication-settings.html)

## Rollenzuweisung und Zugriffskontrolle

Der Zugriff auf Administratorkonten in Adobe Learning Manager wird durch die explizite [Rollenzuweisung](https://experienceleague.adobe.com/de/docs/learning-manager/using/admin/user-management/add-users-user-groups) durch einen bestehenden Administrator gesteuert. Zu den Hauptmerkmalen eines sicheren administrativen Zugriffs gehören:

* Administratorrollen werden nur von autorisierten Administratoren zugewiesen.
* Der Zugriff erfolgt rollenbasiert und kann entsprechend den zugewiesenen Berechtigungen erfolgen.
* Organisationen sind dafür verantwortlich, den administrativen Zugriff auf Benutzer mit einer legitimen geschäftlichen Notwendigkeit zu beschränken.

Adobe empfiehlt, dass Kunden den administrativen Zugriff regelmäßig überprüfen, um die Einhaltung des Grundsatzes der geringsten Privilegien sicherzustellen.

## Multi-Factor Authentication (MFA) erzwingen

Adobe empfiehlt Administratoren dringend, eine zweistufige Verifizierung (2FA) unternehmensweit durchzusetzen. MFA gilt für Nutzer von Enterprise ID und Adobe ID. Federated ID-Benutzer sollten MFA beim Identitätsanbieter ihrer Organisation erzwingen lassen.

So erzwingen Sie 2FA in der Adobe Admin Console:

1. Melden Sie sich bei der Adobe Admin Console an.
2. Navigieren Sie zu Einstellungen > Datenschutz und Sicherheit > Authentifizierungseinstellungen.
3. Aktivieren Sie die zweistufige Verifizierung und wählen Sie die Option Erzwingen , um zu verhindern, dass Benutzer sie deaktivieren.
4. Konfigurieren Sie optional IP-basierte Zugriffsbeschränkungen und erweiterte Sitzungseinstellungen (Max. Sitzungslebensdauer / Max. Leerlaufzeit).

>[!IMPORTANT]
>
>Adobe empfiehlt, 2FA zu erzwingen und nicht als Option für Anwender zu belassen. 2FA kann bis zu 24 Stunden dauern. Für Federated ID-Benutzer erzwingen Sie MFA bei Ihrem Identitätsanbieter.

Weitere Informationen finden Sie unter [Sichere Benutzerauthentifizierung](https://helpx.adobe.com/de/enterprise/using/authentication-settings.html).


## Als Administrator anmelden

ALM [Administratoren](https://experienceleague.adobe.com/de/docs/learning-manager/using/get-started/getting-started-admin) melden sich direkt bei der ALM-Plattform an, indem sie Organisationsanmeldeinformationen verwenden, die über die Admin Console verwaltet werden.

### Administratorrolle zuweisen

Innerhalb der ALM-Plattform konfigurieren Administratoren den administrativen Zugriff, indem sie Rollen erstellen und verwalten, Benutzern Berechtigungen zuweisen und den Berechtigungsbereich basierend auf den operativen Verantwortlichkeiten definieren.

So weisen Sie die Administratorrolle in ALM zu:

1. Melden Sie sich bei Adobe Learning Manager als bestehender Administrator an.
2. Navigieren Sie zu Benutzer > Intern.
3. Suchen Sie nach dem Zielbenutzer oder wählen Sie ihn aus.
4. Wählen Sie Aktionen > Rolle zuweisen > Als Administrator festlegen.

Mit benutzerdefinierten Administratorrollen können Kunden Verwaltungsaufgaben delegieren und gleichzeitig die zentrale Kontrolle über Berechtigungen auf Kontoebene behalten. Benutzerdefinierte Administratoren können auf bestimmte Benutzergruppen oder Kataloge beschränkt werden.

Weitere Informationen finden Sie unter [Benutzer und Benutzergruppen hinzufügen](https://experienceleague.adobe.com/de/docs/learning-manager/using/admin/user-management/add-users-user-groups).

## Anmeldemethoden und SSO konfigurieren

ALM-Administratoren steuern die Anmeldemethoden, die allen Benutzern über Einstellungen > Anmeldemethoden zur Verfügung stehen. Dabei handelt es sich um eine kritische sicherheitsrelevante Konfiguration:

* **Interne Benutzer**: Legen Sie den Anmeldemodus auf Adobe ID oder Single Sign-On (SSO) fest. SSO über SAML 2.0 wird dringend empfohlen.
* **Externe Benutzer**: Legen Sie den Anmeldemodus auf Adobe ID, SSO oder die Learning Manager-ID fest. Richten Sie die ausgewählte Methode mit der Sicherheitsrichtlinie Ihrer Organisation aus.

Adobe empfiehlt, Federated ID/SAML 2.0 SSO als Anmeldemethode für alle internen Benutzer zu verwenden. Dies stellt sicher, dass die Authentifizierung vollständig vom Identitätsanbieter Ihrer Organisation kontrolliert wird, sodass eine zentralisierte MFA-Durchsetzung und sofortiger Kontowiderruf beim Abgang des Benutzers möglich sind.

Weitere Informationen finden Sie unter [Einstellungen](https://experienceleague.adobe.com/de/docs/learning-manager/using/admin/settings).

## Empfohlene sichere Standardwerte bei der Bereitstellung

Wenn ein ALM-Konto zum ersten Mal bereitgestellt wird, empfiehlt Adobe, die folgenden Standardeinstellungen zu überprüfen, bevor ein administrativer Benutzerzugriff gewährt wird:

| Einstellung | Empfohlene sichere Standardeinstellung | Zu konfigurierende Elemente |
|------------------------------|------------------------------------------------------------------|-------------------------------------------------|
| Anmeldemethode — interne Benutzer | Single Sign-on (SSO)/Federated ID | ALM > Einstellungen > Anmeldemethoden |
| Zweistufige Verifizierung (2FA) | Erzwungen (für keinen Benutzer optional) | Admin Console > Einstellungen > Datenschutz und Sicherheit |
| Max. Sitzungsdauer | 8 Stunden oder pro Unternehmensrichtlinie | Admin Console > Einstellungen > Erweiterte Einstellungen |
| Max. Leerlaufzeit | 30 Minuten oder pro Organisationsrichtlinie | Admin Console > Einstellungen > Erweiterte Einstellungen |
| Umfang der Administratorrolle | Geringste Privilegien; nach Möglichkeit benutzerdefinierte Administratorrollen verwenden | ALM > Benutzer > Benutzerdefinierte Rollen |
| Ablaufdatum des externen Benutzers | Festlegen eines Ablaufdatums für jedes externe Benutzerprofil | ALM > Benutzer > Extern |

### Checkliste für die Ersteinrichtung für neue Administratoren

Wenn Sie ein neues Administratorkonto der obersten Ebene bereitstellen, führen Sie die folgenden Schritte aus, bevor Sie den operativen Zugriff gewähren:

* Bestätigen Sie, dass der Identitätstyp &quot;Enterprise ID&quot; oder &quot;Federated ID&quot; ist - nicht &quot;Personal Adobe ID&quot;.
* Erzwingen Sie 2FA auf der Ebene der Admin Console (Einstellungen > Authentifizierungseinstellungen).
* Konfigurieren Sie SSO/Federated ID, wenn diese Option nicht bereits aktiviert ist.
* Legen Sie die maximale Sitzungslebensdauer und die maximale Leerlaufzeit unter &quot;Admin Console&quot; > &quot;Einstellungen&quot; > &quot;Erweiterte Einstellungen&quot; fest.
* Administratorrollen begrenzen: Weisen Sie nur die Berechtigungen zu, die für die Verantwortlichkeiten des Benutzers erforderlich sind.
* Vergewissern Sie sich, dass das Administratorkonto mit einer Unternehmens-E-Mail-Adresse verknüpft ist, die von Ihrem IT-Team gesteuert wird.
* Dokumentieren Sie das Konto im Register für den privilegierten Zugriff Ihrer Organisation.

## Betrieb der Verwaltungskonten

### Alltägliche Verwaltungsaufgaben

Verwaltungskonten werden zur Ausführung täglicher operativer Aufgaben verwendet, darunter:

* **Lebenszyklusverwaltung für Benutzer**: Erstellen von Benutzern, Aktualisieren von Profilen und Durchführen von Rollenänderungen.
* **Learning Content Management**: Verwalten von Kursen, Lernprogrammen, Zertifizierungen und Katalogen.
* **Berichte und Analysen**: Generieren und Überprüfen von Berichten über den Teilnehmerfortschritt und die Plattformnutzung.
* **Integrationen und Systemkonfiguration**: Verwalten von Konnektoren, API-basiertem Zugriff und Einstellungen auf Systemebene.

Beim Ausführen von Verwaltungsaktionen müssen Administratoren die internen Zugriffskontroll- und Änderungsverwaltungsrichtlinien ihrer Organisation befolgen.

Siehe [Häufig gestellte Fragen für Adobe Learning Manager-Administratoren](https://experienceleague.adobe.com/de/docs/learning-manager/using/faq/frequently-asked-questions-for-administrators)


### Rollenhierarchie und Delegierung

Adobe Admin Console verwendet eine hierarchische Administratorstruktur. Systemadministratoren können Verantwortlichkeiten an Rollen mit niedrigeren Berechtigungen delegieren, um die Angriffsfläche des Administratorkontos auf der obersten Ebene zu verringern:

* Produktadministrator: Verwaltet den Zugriff auf bestimmte Adobe-Produkte (z. B. Adobe Learning Manager).
* Produktprofil-Administrator: Verwaltet die Benutzermitgliedschaft in bestimmten Produktprofilen.
* Benutzergruppen-Admin: Verwaltet die Mitgliedschaft in Benutzergruppen.
* Benutzerdefinierter ALM-Administrator: Umfangreicher Administrator in ALM mit konfigurierbaren Berechtigungen für jeden Katalog und jede Benutzergruppe.

### Kontinuierliche Governance-Praktiken

Die folgenden Praktiken sollten von Organisationen befolgt werden, die fortlaufend ALM-Administratorkonten betreiben:

* **Überprüfung des regelmäßigen Zugriffs**: Überprüfen Sie regelmäßig die Liste der Systemadministratoren in der Admin Console (&quot;Benutzer&quot; > &quot;Administratoren&quot;) und der ALM-Administratoren (&quot;Benutzer&quot; > &quot;Intern&quot;), um sicherzustellen, dass nur die aktuellen, autorisierten Mitarbeiter über diese Rollen verfügen.
* **Überwachungsprotokollüberwachung**: Das Überwachungsprotokoll der Admin Console zeichnet alle von Administratoren vorgenommenen Änderungen auf. Systemadministratoren sind vollständig sichtbar. Prüfen Sie das Protokoll regelmäßig auf nicht autorisierte Änderungen.
* **Mindest ständiger Zugriff**: Verwenden Sie keine Administratorkonten der obersten Ebene für Routineaufgaben. Vollständigen Administratorzugriff für Aufgaben reservieren, die dies erfordern.
* **Sitzungssicherheit**: Konfigurieren Sie die maximale Sitzungslebensdauer und die maximale Leerlaufzeit in &quot;Admin Console&quot; > &quot;Einstellungen&quot; > &quot;Erweiterte Einstellungen&quot;, um die Belastung durch unbeaufsichtigte Sitzungen zu begrenzen.

Weitere Informationen finden Sie unter [Übersicht über die Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html).

### Verwalten von Benutzerkonten unter Administratorsteuerung

ALM-Administratoren verwalten interne und externe Benutzerkonten. Zu den sicherheitsrelevanten Operationen gehören:

* Automatisches Löschen von Benutzern: In den Einstellungen können Administratoren konfigurieren, dass inaktive interne Benutzer nach einer festgelegten Anzahl von Tagen automatisch gelöscht werden. So wird das Risiko ruhender Konten verringert.
* Ablauf der Laufzeit für externe Benutzer: Administratoren legen ein Ablaufdatum beim Erstellen externer Benutzerprofile fest. Abgelaufene Konten werden automatisch in einen inaktiven Status verschoben.
* Löschen von Benutzern: Administratoren können Benutzer manuell über &quot;Benutzer&quot; > &quot;Intern&quot; > &quot;Aktionen&quot; > &quot;Benutzer löschen&quot; löschen.
* Benutzerbereinigung: Nach dem Löschen können Administratoren Benutzerdatensätze endgültig bereinigen, um Datenaufbewahrungsrichtlinien einzuhalten und unberechtigten Zugriff auf veraltete Benutzerdaten zu verhindern.

Weitere Informationen finden Sie unter:

* [Benutzer und Benutzergruppen hinzufügen](https://experienceleague.adobe.com/de/docs/learning-manager/using/admin/user-management/add-users-user-groups)
* [Benutzer bereinigen](https://experienceleague.adobe.com/de/docs/learning-manager/using/admin/purge-users)

## Entlastung der Verwaltungskonten

Der Administratorzugriff muss entfernt werden, wenn er nicht mehr erforderlich ist. Die Stilllegungsverwaltungskonten können Folgendes umfassen:

* Widerrufen von Administratorrollen für Benutzer.
* Verringern von Berechtigungen, wenn kein vollständiger Administratorzugriff mehr erforderlich ist.
* Entfernen von Benutzern aus dem System, falls erforderlich.

Regelmäßige Überprüfungen und das Entfernen unnötiger administrativer Zugriffsrechte tragen dazu bei, dass der Zugriff mit den geringsten Rechten erhalten bleibt.

### Systemadministratorrechte entfernen (Admin Console)

Wenn ein Systemadministrator die Organisation verlässt oder die Rollen ändert, müssen die Berechtigungen umgehend widerrufen werden:

1. Melden Sie sich bei der Adobe Admin Console als Systemadministrator an.
2. Navigieren Sie zu Benutzer > Administratoren.
3. Wählen Sie den Administrator aus, der entfernt werden soll.
4. Klicken Sie auf das Symbol Weitere Optionen (...) > Administrator bearbeiten und entfernen Sie dann die Systemadministratorrolle — ODER wählen Sie Benutzer entfernen aus , um den Benutzer vollständig aus der Organisation zu entfernen.
5. Wenn der Administrator andere Rollen innehatte (Produktadministrator, Supportadministrator usw.), widerrufen Sie diese ebenfalls.

>[!IMPORTANT]
>
>Wenn der scheidende Administrator der Vertragseigentümer für das Unternehmen ist, muss die Rolle des Vertragseigentümers auf eine andere Person übertragen werden, bevor sie entfernt werden kann. Wenden Sie sich bei Bedarf an den Adobe-Support.

Weitere Informationen finden Sie unter:

* [Erstellen, Aktualisieren oder Entfernen von Benutzerkonten auf der Admin Console](https://helpx.adobe.com/de/enterprise/using/manage-users-individually.html)
* [So verlassen Sie Ihr Unternehmenskonto](https://helpx.adobe.com/de/enterprise/using/leave-organization.html)

### Entfernen der ALM-Administratorrolle

So widerrufen Sie den ALM-Administratorzugriff, ohne das Benutzerkonto zu löschen (z. B. wenn die Person Teilnehmer bleibt):

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.
2. Navigieren Sie zu Benutzer > Intern.
3. Suchen Sie nach dem Benutzer und wählen Sie ihn aus.
4. Wählen Sie Aktionen > Rolle entfernen > Administrator entfernen.

Der Benutzer kehrt zur Teilnehmerrolle zurück. Ihr Lernverlauf und ihre Kursanmeldungen bleiben erhalten.

Weitere Informationen finden Sie unter [Benutzer und Benutzergruppen hinzufügen](https://experienceleague.adobe.com/de/docs/learning-manager/using/admin/user-management/add-users-user-groups).

### Benutzer löschen und bereinigen

Wenn ein Benutzer die Organisation vollständig verlässt und sein Konto von der Plattform entfernt werden sollte:

* Löschen Sie den Benutzer: Benutzer > Intern > wählen Sie Benutzer > Aktionen > Benutzer löschen. Dadurch wird das Konto deaktiviert und der aktive Zugriff wird entfernt.
* Benutzer bereinigen: Gehen Sie nach dem Löschen zu Benutzer > Benutzerbereinigung , wählen Sie den Löschmonat aus, wählen Sie den Benutzer aus und wählen Sie Aktionen > Benutzer bereinigen. Durch das Bereinigen werden alle Benutzerdatensätze dauerhaft entfernt.

Weitere Informationen finden Sie unter [Benutzer bereinigen](https://experienceleague.adobe.com/de/docs/learning-manager/using/admin/purge-users).


## Sicherheit und geteilte Verantwortung.

Adobe Learning Manager arbeitet mit einem Modell der geteilten Verantwortung:

* Adobe ist für die Sicherung der zugrunde liegenden ALM-Plattform und -Infrastruktur verantwortlich.
* Die Kunden sind für die Verwaltung des administrativen Zugriffs, der Rollenzuweisungen und der Lebenszyklusaktivitäten der Benutzer innerhalb ihres ALM-Kontos verantwortlich.

Weitere Informationen zu den Sicherheitsmethoden von Adobe Learning Manager finden Sie unter [Adobe Learning Manager-Sicherheitsübersicht (PDF)](https://experienceleague.adobe.com/docs/learning-manager/assets/alm-security-whitepaper-2024.pdf?lang=de).

## Dokumentenverwaltung

Dieses Dokument kann regelmäßig aktualisiert werden, um Änderungen an den Funktionen von Adobe Learning Manager oder an den Best Practices für Administratoren zu berücksichtigen. Die Version und das Datum der letzten Aktualisierung werden in den Dokument-Metadaten und im FedRAMP-Autorisierungspaket beibehalten. Kunden sollten die öffentlich verfügbare Version auf Adobe Experience League nutzen, um sicherzustellen, dass sie die neuesten Anleitungen verwenden.

## Verbesserte Abdeckung der Sicherheitsfunktionen

### SCG-ENH-CMP

Adobe verwaltet dokumentierte Prozesse für Komponenteninventar, -eigentum und -lebenszyklusmanagement, um eine kontrollierte Konfiguration und Compliance über alle Systemkomponenten hinweg zu gewährleisten.

### SCG-ENH-API

Adobe erzwingt standardisierte API-Sicherheitskontrollen, einschließlich Authentifizierung, Autorisierung und Überwachung, unterstützt durch dokumentierte Governance- und Plattformsicherungen.

### SCG-ENH-MRG

Adobe wendet formale Änderungs- und Zusammenführungsverwaltungsprozesse an, einschließlich Überprüfungs- und Genehmigungskontrollen, um die Systemintegrität zu wahren und das Bereitstellungsrisiko zu verringern.

### SCG-ENH-VRH

Adobe folgt einem definierten Prozess zur Verwaltung und Behebung von Sicherheitslücken, der die Identifikation, Priorisierung, Verfolgung und rechtzeitige Lösung umfasst.

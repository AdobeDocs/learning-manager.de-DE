---
description: Dieses Dokument bietet einen empfohlenen Ansatz für Unternehmen zum Einrichten und Konfigurieren des Adobe Learning Manager. Das Learning Manager-Team schlägt einen stufenweisen Ansatz für die ersten Schritte mit der Anwendung vor. Es ist nicht zwingend erforderlich, alle Phasen in einer bestimmten Reihenfolge zu befolgen.
jcr-language: en_us
title: Empfohlene Vorgehensweisen zum Einrichten von Learning Manager
contentowner: jayakarr
preview: true
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3387'
ht-degree: 0%

---



# Empfohlene Vorgehensweisen zum Einrichten von Learning Manager

Dieses Dokument bietet einen empfohlenen Ansatz für Unternehmen zum Einrichten und Konfigurieren des Adobe Learning Manager. Das Learning Manager-Team schlägt einen stufenweisen Ansatz für die ersten Schritte mit der Anwendung vor. Es ist nicht zwingend erforderlich, alle Phasen in einer bestimmten Reihenfolge zu befolgen.

Diese Phasen können durch drei verschiedene Rollen von einer oder mehreren Personen basierend auf Ihrer Organisationseinrichtung durchgeführt werden. Die drei Rollen lauten wie folgt:

1. **IT-Administrator** - Der IT-Administrator führt aktivierungs- oder integrationsbezogene Aktivitäten für die Learning Manager-Anwendung in einem Unternehmen durch. Der IT-Administrator kann auch einzelne/mehrere Benutzer hinzufügen und die Rolle eines Integrationsadministrators ausführen.
1. **Autor** - Der Autor erstellt Lerninhalte, die für die Lernanforderungen des Unternehmens erforderlich sind. Der Autor von Schulungs- oder Lerninhalten in Ihrem Unternehmen kann mit dem Erstellen der grundlegenden Inhalte beginnen, die für die Learning Manager-Anwendung erforderlich sind.
1. **Learning Manager-Administrator** - Der Learning Manager-Anwendungsadministrator führt Konfigurations- und Einrichtungsaktivitäten durch. In einigen Unternehmen kann der IT-Administrator auch als Administrator der Learning Manager-Anwendung fungieren.

Sie können die unten stehende Infografik durchgehen, um sich einen Überblick über die Phasen und die zugehörigen Aufgaben zu verschaffen.

![](assets/learning-manager-getting-started.jpg)

In dieser Phase wird davon ausgegangen, dass Ihr Unternehmen bereits den Lizenzschlüssel erhalten hat und Sie das Learning Manager-Konto aktiviert haben. Wie in der Infografik erwähnt, werden die drei Spuren wie folgt erläutert:

## Phase 1 - Technische Einrichtung (IT-Administrator) {#phase1technicalsetupitadministrator}

In Track 1 kann der IT-Administrator Ihres Unternehmens zur Rolle des Integrationsadministrators in der Learning Manager-Anwendung wechseln und einige Aktivierungs- und Integrationsvorgänge wie folgt ausführen:

### Aktive Felder aktivieren/hinzufügen (Learning Manager-Administrator) {#enableaddactivefieldscaptivateprimeadministrator}

Zusätzlich zu den aktiven Feldern, die von den Benutzern während der Registrierung bereitgestellt werden, kann der Administrator weitere aktive Felder hinzufügen. Der Administrator kann auch die Benutzerfelder aktivieren/deaktivieren. Die Werte für diese aktiven Felder werden aus den Metadaten aus verschiedenen Datenquellen generiert, die Benutzerkonten zugeordnet sind. Siehe [Hilfe zu aktiven Feldern](feature-summary/add-users-user-groups.md#active-fields) für weitere Informationen.

### Single Sign-on (SSO) {#singlesignonsso}

Sie können über Adobe ID oder Single Sign-on auf die Learning Manager-Anwendung zugreifen. Die einmalige Anmeldung (SSO) ist ein Verfahren, mit dem ein Benutzer sich einmal authentifizieren kann und mehrmals auf mehrere Anwendungen zugreifen kann. Diese Konfiguration ist für das Unternehmen nicht obligatorisch. Wenn Ihre Organisation über einen SAML 2.0-basierten SSO-Anbieter verfügt, können Sie diesen zum Konfigurieren der Learning Manager-Anwendung verwenden. Die Konfiguration ist auf Organisationsebene und für die Learning Manager-Anwendung erforderlich. Wenn Sie SSO verwenden möchten, wenden Sie sich an den Adobe-Support , um Konfigurationsanweisungen zu erhalten. Siehe [Hilfe zu Einstellungen](feature-summary/settings.md) für weitere Informationen.

### Massenimport von Benutzern {#bulkimportofusers}

Wenn Sie in Ihrer Organisation eine große Anzahl von Benutzern haben, können Sie alle Benutzer gleichzeitig mithilfe einer CSV-Datei in die Learning Manager-Anwendung importieren. Bevor Sie diese Aufgabe ausführen, empfehlen wir Ihnen, die Benutzerliste aus der HR-Anwendung Ihres Unternehmens im CSV-Format zu exportieren. Auch wenn Sie die Benutzer in dieser Phase nicht als Massenimport importieren, können Sie sich mit dem CSV-Format vertraut machen. Um mit dem Importvorgang in Learning Manager zu beginnen, laden Sie die CSV-Datei hoch und ordnen Sie die Anwendungsdatenfelder den CSV-Spalten Ihrer Organisation zu. Siehe [Hilfe zum Massenimport](add-users-in-bulk.md) für weitere Informationen.

### Integration des FTP-Connectors {#ftpconnectorintegration}

Wenn Sie ständig Mitarbeiter in Ihrer Organisation hinzufügen oder entfernen müssen, können Sie den Massenimport von Benutzern über den FTP-Connector automatisieren. Sie müssen zunächst eine Verbindung herstellen. Anschließend können Sie eine CSV-Datei hochladen und die Attribute der CSV-Datei den entsprechenden Feldern des Lern-Managers zuordnen. Sie können den automatischen Importvorgang planen und ihn bei Bedarf synchronisieren. Siehe [Hilfe zum FTP-Connector](../integration-admin/feature-summary/connectors.md#ftpconnector) für weitere Informationen.

### Integration des Salesforce-Connectors {#salesforceconnectorintegration}

Wenn Sie über ein Salesforce-Konto in Ihrer Organisation verfügen, können Sie den Prozess des Imports aller Benutzer aus Salesforce in die Learning Manager-Anwendung automatisieren. Wenn Sie diese Funktion verwenden möchten, können Sie den Salesforce-Connector verwenden, um Learning Manager mit dem Salesforce-Konto zu integrieren und die Datensynchronisierung zu automatisieren. Nutzen Sie die automatische Zeitplanung, um den automatischen Benutzerimport regelmäßig durchzuführen. Sie können die Synchronisierung auch täglich durchführen. Siehe [Hilfe zum Salesforce-Connector](../integration-admin/feature-summary/connectors.md#sfconnector) für weitere Informationen.

### Integration mit Adobe Connect {#adobeconnectintegration}

Wenn Sie Adobe Connect in Ihrem Unternehmen verwenden, können Sie es mit der Adobe Learning Manager-Anwendung integrieren, um Teilnehmern eine nahtlose Benutzererfahrung zu bieten. Durch die Integration können die Teilnehmer mit einem einzigen Klick auf eine virtuelle Lernumgebung direkt in der Learning Manager-Anwendung zugreifen, ohne sich erneut bei Adobe Connect anmelden zu müssen. Mit dieser Funktion können die Teilnehmer auch die aufgezeichneten virtuellen Klassenzimmersitzungen in der Learning Manager-Anwendung nutzen. Um die Integration durchzuführen, müssen Sie zuerst die Einstellungen integrieren. Verwendung **Einstellungen > Adobe Connect > Jetzt konfigurieren** , um eine Connect-URL und Anmeldedaten anzugeben und die Integration durchzuführen. Siehe [Hilfe zur Adobe Connect-Integration](feature-summary/adobeconnect-integration.md) für weitere Informationen.

### Registrierung der Salesforce-App {#salesforceappregistration}

Ihre Teilnehmer in Unternehmen können nahtlose Erfahrungen mit dem Zugriff auf die Learning Manager-App direkt innerhalb ihrer Salesforce-Konten sammeln. Teilnehmer können über die Salesforce-Anwendung auf ihre zugewiesenen Lerninhalte wie Kurse, Lernprogramme und Arbeitshilfen zugreifen. Benutzer können auch über die Learning Manager-App in Salesforce auf Benachrichtigungen und Ankündigungen zugreifen. Um diese Funktion verwenden zu können, müssen Sie die Salesforce-App in der Learning Manager-Anwendung registrieren. Siehe [Hilfe zur Salesforce-App](../integration-admin/feature-summary/sfdc-app.md) , um mehr über die Installations- und Nutzungsanweisungen zu erfahren.

## Phase 2 - Standortkonfiguration (Learning Manager-Administrator) {#phase2siteconfigurationcaptivateprimeadministrator}

Der Administrator der Lern-Manager-Anwendung in Ihrem Unternehmen muss einige Funktionen konfigurieren oder einrichten, bevor Sie mit deren Implementierung für die Teilnehmer beginnen.

### Branding {#branding}

Eine Organisation kann das Firmenlogo in der Learning Manager-Anwendung anzeigen, ihre eigene Domäne in der URL haben, den Namen der Organisation anzeigen und Farbschemata anzeigen, die der Marke einer Organisation entsprechen. Mit Learning Manager können Organisationen all diese Funktionen nutzen. Wenn Sie die Einstellungen anpassen und Ihr eigenes Branding verwenden möchten, klicken Sie im linken Bereich auf den Abschnitt &quot;Branding&quot;. Klicken Sie neben all diesen Optionen auf &quot;Bearbeiten&quot; und nehmen Sie die gewünschten Anpassungen vor. Siehe [Hilfe zu Branding und Designs](feature-summary/themes.md) für weitere Informationen.

### Benutzer/Benutzergruppen hinzufügen {#addusersusergroups}

Da die Teilnehmer die primären Benutzer Ihrer Lerninhalte sind, ist das Hinzufügen von Benutzern zum Learning Management-System der primäre Schritt. Fügen Sie Benutzer zur Learning Manager-Anwendung hinzu und weisen Sie ihnen Rollen zu. Sie haben folgende Möglichkeiten, Benutzer hinzuzufügen:

#### Benutzer hinzufügen (intern) {#addusersinternal}

* **Als Einzelbenutzer** - Durch das Hinzufügen einzelner Benutzer zur Learning Manager-Anwendung können Sie einige Benutzer ausprobieren, bevor Sie sie gesammelt hinzufügen. Diese Option ist außerdem nützlich, wenn Sie nach dem Massenimport von Benutzern mehr einzelne Benutzer nach Bedarf hinzufügen möchten.
* **Selbstregistrierung** - Mit dieser Option können Administratoren ihren Mitarbeitern die Möglichkeit geben, sich bei Learning Manager zu registrieren.
* **Massenimport** (mit CSV-Upload) - Mit dieser Option können Sie Benutzer gesammelt in die Learning Manager-Anwendung importieren. Als Voraussetzung müssen Sie die Liste der Benutzer im CSV-Format bereit halten, bevor Sie diese Funktion verwenden.

#### Benutzer hinzufügen (externe Profile) {#addusersexternalprofiles}

* Durch externe Registrierung: Mit dieser Option können Sie externe Abteilungsmitglieder oder externe Mitarbeiter Ihrer Organisation für die Anwendung registrieren.

#### Benutzergruppen hinzufügen {#addusergroups}

Die Lern-Manager-Anwendung generiert Standardbenutzergruppen basierend auf ähnlichen Attributen. Zusätzlich zu den Standardgruppen können Sie benutzerdefinierte Benutzergruppen basierend auf Parametern wie Bezeichnung, Speicherort generieren, sodass Sie diese Gruppen unter anderem in Gamification und Berichten verwenden können. Siehe [Hilfe zum Hinzufügen von Benutzern](feature-summary/add-users-user-groups.md) für weitere Informationen.

### Rollen zuweisen {#assignroles}

Nachdem die Benutzer dem Lern-Manager hinzugefügt wurden, kann der Administrator den Benutzern die Rollen &quot;Autor&quot;, &quot;Administrator&quot; oder &quot;Integrations-Admin&quot; gemäß den Anforderungen des Unternehmens zuweisen. Um Benutzern Rollen zuzuweisen, können Sie bei der Administratoranmeldung auf **[!UICONTROL Benutzer]**  Aktivieren Sie im linken Bereich das Kontrollkästchen für die einzelnen Benutzernamen und klicken Sie auf **[!UICONTROL Aktionen]** , um die Rolle auszuwählen, die Sie zuweisen möchten. Managerrollen werden Benutzern vom Adobe-Lern-Manager zugewiesen, basierend auf den Rollen/Berechtigungen, die von Ihrem Unternehmen in der CSV-Datei angegeben wurden. Sie können die Rollen von Benutzern als Manager auch ändern, indem Sie den Arbeitsablauf Benutzer bearbeiten verwenden. Siehe [Hilfe zum Hinzufügen von Benutzern](feature-summary/add-users-user-groups.md) für weitere Informationen.

### Benachrichtigungsvorlagen {#notificationtemplates}

Benachrichtigungen können für Benutzer in einem Learning Management-System nützlich sein, um ihren Status zu kennen oder über die Ereignisse/Aktivitäten informiert zu werden. Beim Erstellen von Kursen, beim Konfigurieren der Funktionen oder beim Nutzen von Kursen durchlaufen Benutzer mehrere Ereignisse, die Benachrichtigungen an Teilnehmer, ihre Manager, Administratoren oder Autoren auslösen. Learning Manager stellt verschiedene E-Mail-Benachrichtigungsvorlagen in der Anwendung bereit. Als Administrator können Sie sie gemäß den Anforderungen Ihrer Organisation anpassen. Um E-Mail-Benachrichtigungen zu erstellen, wählen Sie **E-Mail-Vorlagen** im linken Bereich und klicken Sie auf den Vorlagennamen. Siehe [Hilfe zu E-Mail-Vorlagen](feature-summary/email-templates.md) für weitere Informationen

**E-Mail-Benachrichtigungen deaktivieren (empfohlen)**

Standardmäßig sind die Benachrichtigungen in der Learning Manager-Anwendung aktiviert. Sie können Benachrichtigungen in dieser Phase deaktivieren, wenn Sie Ihre Mitarbeiter nicht über das Unternehmen informieren möchten.

### Abzeichen {#badges}

Abzeichen sind ein Leistungsnachweis, den sich Ihr Mitarbeiter nach Abschluss eines Kurses verdienen kann. Fachleute auf der ganzen Welt verwenden diese Abzeichen als Nachweis für bestimmte Kenntnisse oder Lernerfolge. Sie können eine Sammlung von Abzeichen erstellen, damit Sie sie Teilnehmern nach Abschluss der Lerninhalte zuweisen können. Um mit dem Erstellen von Abzeichen zu beginnen, können Sie auf **[!UICONTROL Abzeichen]** im linken Bereich. Siehe  [Hilfe zu Abzeichen](feature-summary/badges.md) für weitere Informationen.

### Feedback {#feedback}

Feedback ist einer der wichtigen Faktoren eines LMS, um den Lernfortschritt der Teilnehmer zu messen und die Qualität der Lerninhalte zu gewährleisten. Der Lern-Manager bietet zwei Arten von Feedback für Benutzer.

* L1-Feedback ist das Feedback, das die Teilnehmer nach Abschluss des Kurses geben.
* L3-Feedback ist das Feedback, das Manager den Teilnehmern basierend auf den Auswirkungen des Kurses auf das Verhalten der Teilnehmer und die täglichen Aktivitäten geben.

Diese Funktion ist für Organisationen optional. Administratoren können die Feedbackvorlagen gemäß den Anforderungen Ihres Unternehmens anpassen. Um diese Funktion verwenden zu können, muss der Administrator L1- und L3-Feedbackoptionen auf Kursinstanzebene aktivieren. Um das Feedback zu konfigurieren, wählen Sie einen beliebigen Kurs aus, klicken Sie im linken Bereich auf &quot;Standardwerte für Instanz&quot; und aktivieren Sie die Feedbackoption. Siehe [Feedback-Hilfe](feature-summary/courses.md) für weitere Informationen.

### Gamification {#gamification}

Das Interesse der Teilnehmer zu halten, während sie den Inhalt nutzen, ist eine der Herausforderungen, denen Unternehmen gegenüberstehen. Gamification erhöht die Kursabschlussrate, indem Teilnehmer mit Gaming-Techniken zur Erreichung ihrer Ziele motiviert werden. Teilnehmer können mit ihren Kollegen konkurrieren, um Punkte für verschiedene Lernaktivitäten zu sammeln und Bronze-, Silber-, Gold- und Platinlevel zu erreichen. Administratoren können jede Gamification-Aufgabe aktivieren/deaktivieren und die Zuweisung von Punkten zu Aufgaben ändern. Learning Manager bietet die Gamification-Funktion mit einigen Standardeinstellungen. Sie können die Funktion einige Zeit mit Standardeinstellungen verwenden und dann können Sie sich für eine Anpassung entscheiden. Es ist optional, dass Sie die Einstellungen für diese Funktion konfigurieren/ändern. Wenn Sie in Ihrem Unternehmen einen Experten für Fachgebiete haben, empfehlen wir Ihnen, die Einstellungen zu konfigurieren, bevor Sie sie verwenden. Siehe [Gamification-Hilfe](feature-summary/gamification.md) für weitere Informationen.

### Erstellen von Lernobjekten {#createlearningobjects}

Dies ist die logische Phase, in der alle drei Spuren (Spur 1, Spur 2 und Spur 3) zusammenlaufen, damit Sie den nächsten Aktionskurs einschlagen können.

Wenn Sie an dieser Stelle Module und Kurse erstellt haben, können Sie mit der Erstellung von Lernobjekten höherer Ebene, z. B. Zertifizierungen, Lernprogrammen oder Arbeitshilfen, fortfahren. Bevor Sie mit dem Erstellen von Lernobjekten beginnen, vergewissern Sie sich, dass Sie in der Learning Manager-Anwendung bereits einige Benutzer hinzugefügt und einige Module und Kurse erstellt haben.

#### Zertifizierungen erstellen {#createcertifications}

Die Zertifizierung ist ein Nachweis des Abschlusses eines Lerninhalts oder ein Leistungsnachweis für Teilnehmer auf einmaliger Basis oder in einem wiederkehrenden Zeitraum. Die Registrierung von Teilnehmern für Lerninhalte kann erhöht werden, indem den Teilnehmern nach Kursabschluss eine Zertifizierung bereitgestellt wird. Als Administrator können Sie ein Zertifizierungsprogramm erstellen, das entweder intern gehostet oder von einem Drittanbieter durchgeführt wird. Definieren Sie in der internen Zertifizierung die Kurse, die ein Teilnehmer absolvieren muss, um ein Zertifikat zu erhalten. Bevor Sie eine Zertifizierung erstellen, stellen Sie sicher, dass im Konto einige Kurse verfügbar sind. Siehe  [Hilfe zur Zertifizierung](feature-summary/certifications.md) für weitere Informationen zum Erstellen von Zertifizierungen.

#### Arbeitshilfen erstellen {#createjobaids}

Arbeitshilfen sind ein Repository mit Schulungsinhalten, das den Teilnehmern ohne Registrierung oder Abschlusskriterien zur Verfügung steht. Teilnehmer können sich während ihrer Arbeit auf diese Arbeitshilfen beziehen, um Unterstützung für Aktivitäten oder Aufgaben in einem Unternehmen zu erhalten. Auch wenn es nicht zwingend erforderlich ist, Arbeitshilfen als Teil der Kurserstellung zu verwenden, empfiehlt das Learning Manager-Team, Arbeitshilfen als bewährte Methode für Ihr Unternehmen zu erstellen. Weitere Informationen finden Sie unter  [Hilfe zu Arbeitshilfen](../authors/feature-summary/job-aids.md) für Informationen zum Erstellen von Arbeitshilfen.

#### Lernprogramme erstellen {#createlearningprograms}

Lernprogramme sind eine Reihe einzigartig gestalteter Kurse, die bestimmte Teilnehmerziele erfüllen. Bevor Sie Lernprogramme erstellen, stellen Sie sicher, dass Sie bereits einige Kurse erstellt haben oder dass in Ihrem Konto bereits Kurse verfügbar sind.  Obwohl es für ein Unternehmen optional ist, diese Funktion zu verwenden, empfiehlt das Learning Manager-Team, diese zu verwenden, um Ihren Mitarbeitern fokussiertes Lernen zu vermitteln. Um die Lernprogramme zu verwenden, klicken Sie im linken Teilfenster auf &quot;Lernprogramme&quot;, wählen Sie eine Gruppe von Kursen aus dem Katalog aus und veröffentlichen Sie sie. Weitere Informationen finden Sie unter [Hilfe zu Lernprogrammen](feature-summary/learning-programs.md) für spezifische Anweisungen.

### Erstellen von Katalogen {#createcatalogs}

Sie können Kataloge in einer Organisation verwenden, um zielgerichtete Inhalte zu erstellen oder Inhalte für definierte Gruppen von Teilnehmern zu klassifizieren. Im Lern-Manager ist ein Katalog eine Sammlung von Lernobjekten wie Kursen, Zertifizierungen oder Lernprogrammen. Sie können die Lernobjekte Ihrer Wahl beim Erstellen von Katalogen auswählen. Stellen Sie sicher, dass Sie bereits eine Reihe von Kursen, Zertifizierungen oder Lernprogrammen erstellt haben, bevor Sie die Kataloge erstellen. Sie können benutzerdefinierte Kataloge mit einer Reihe von Lernobjekten erstellen, wenn Sie sie internen oder externen Benutzergruppen zuweisen möchten. Weitere Informationen finden Sie unter  [Hilfe zu Katalogen](feature-summary/catalogs.md) für weitere Informationen zu Katalogen.

### E-Mail-Benachrichtigungen/Benutzerzugriff aktivieren {#turnonemailnotificationsuseraccess}

In dieser Phase können Sie E-Mail-Benachrichtigungen an die Benutzer Ihrer Anwendungen aktivieren und auch den Benutzerzugriff aktivieren.

## Phase 3 - Authoring-Kurse (Autor) {#phase3authoringcoursesauthor}

Inhaltsentwickler oder Autoren in Ihrem Unternehmen können mit dem Erstellen der Lerninhalte beginnen. Es ist obligatorisch, dass Sie Module und Kurse erstellen, da sie die Grundlage für alle Ihre Lerninhalte in der Learning Manager-Anwendung bilden.

### Module erstellen {#createmodules}

Module sind die grundlegenden Bausteine der Learning Manager-Anwendung. Um Ihre Lerninhalte zu organisieren, beginnen Sie mit der Erstellung von Modulen als Autor. Mit dem Lern-Manager können Sie einen der vier Typen von Kursmodulen auswählen, z. B. Klassenzimmer, Selbststudium, Aktivität und virtuelle Klassenzimmermodule. Siehe  [Modulhilfe](../authors/how-to-choose-modules.md) , um zu erfahren, welcher Kursmodul für die Anforderungen Ihres Unternehmens am besten geeignet ist.

### Kurse erstellen {#createcourses}

Administratoren können eine Autorenrolle in der Learning Manager-Anwendung übernehmen und Kurse erstellen. In der Learning Manager-Anwendung ist ein Kurs eine Grundeinheit mit einem Satz von Modulen, die dem Teilnehmer zugewiesen werden können. Teilnehmer absolvieren Kurse. Sie können mit dem Erstellen von Kursen beginnen, indem Sie die zuvor erstellten Module auswählen, Kenntnisse zuordnen, die die Teilnehmer aus dem Kurs erwerben sollen, einem Kurs Stufen, Credits und Abzeichen zuordnen, Arbeitshilfen, Voraussetzungen und Ressourcen basierend auf Ihrer Auswahl auswählen und den Kurs veröffentlichen. Sie können auch mehrere Instanzen eines Kurses erstellen, sodass Sie die Kursinstanzen mehreren Teilnehmern in verschiedenen Zeitzonen, Zeitplänen usw. zuweisen können. Weitere Informationen finden Sie unter  [Kurshilfen](../authors/feature-summary/courses.md)für weitere Informationen zum Erstellen eines Kurses.

### Erstellen von Lernobjekten {#Createlearningobjects-1}

Dies ist die logische Phase, in der alle drei Spuren (Spur 1, Spur 2 und Spur 3) zusammenlaufen, damit Sie den nächsten Aktionskurs einschlagen können.

Wenn Sie an dieser Stelle Module und Kurse erstellt haben, können Sie mit der Erstellung von Lernobjekten höherer Ebene, z. B. Zertifizierungen, Lernprogrammen oder Arbeitshilfen, fortfahren. Bevor Sie mit dem Erstellen von Lernobjekten beginnen, vergewissern Sie sich, dass Sie in der Learning Manager-Anwendung bereits einige Benutzer hinzugefügt und einige Module und Kurse erstellt haben.

#### Zertifizierungen erstellen {#Createcertifications-1}

Die Zertifizierung ist ein Nachweis des Abschlusses eines Lerninhalts oder ein Leistungsnachweis für Teilnehmer auf einmaliger Basis oder in einem wiederkehrenden Zeitraum. Die Registrierung von Teilnehmern für Lerninhalte kann erhöht werden, indem den Teilnehmern nach Kursabschluss eine Zertifizierung bereitgestellt wird. Als Administrator können Sie ein Zertifizierungsprogramm erstellen, das entweder intern gehostet oder von einem Drittanbieter durchgeführt wird. Definieren Sie in der internen Zertifizierung die Kurse, die ein Teilnehmer absolvieren muss, um ein Zertifikat zu erhalten. Bevor Sie eine Zertifizierung erstellen, stellen Sie sicher, dass im Konto einige Kurse verfügbar sind. Siehe  [Hilfe zur Zertifizierung](feature-summary/certifications.md) für weitere Informationen zum Erstellen von Zertifizierungen.

#### Arbeitshilfen erstellen {#CreateJobaids-1}

Arbeitshilfen sind ein Repository mit Schulungsinhalten, das den Teilnehmern ohne Registrierung oder Abschlusskriterien zur Verfügung steht. Teilnehmer können sich während ihrer Arbeit auf diese Arbeitshilfen beziehen, um Unterstützung für Aktivitäten oder Aufgaben in einem Unternehmen zu erhalten. Auch wenn es nicht zwingend erforderlich ist, Arbeitshilfen als Teil der Kurserstellung zu verwenden, empfiehlt das Learning Manager-Team, Arbeitshilfen als bewährte Methode für Ihr Unternehmen zu erstellen. Weitere Informationen finden Sie unter  [Hilfe zu Arbeitshilfen](../authors/feature-summary/job-aids.md) für Informationen zum Erstellen von Arbeitshilfen.

#### Lernprogramme erstellen {#Createlearningprograms-1}

Lernprogramme sind eine Reihe einzigartig gestalteter Kurse, die bestimmte Teilnehmerziele erfüllen. Bevor Sie Lernprogramme erstellen, stellen Sie sicher, dass Sie bereits einige Kurse erstellt haben oder dass in Ihrem Konto bereits Kurse verfügbar sind.  Obwohl es für ein Unternehmen optional ist, diese Funktion zu verwenden, empfiehlt das Learning Manager-Team, diese zu verwenden, um Ihren Mitarbeitern fokussiertes Lernen zu vermitteln. Um die Lernprogramme zu verwenden, klicken Sie im linken Teilfenster auf &quot;Lernprogramme&quot;, wählen Sie eine Gruppe von Kursen aus dem Katalog aus und veröffentlichen Sie sie. Weitere Informationen finden Sie unter [Hilfe zu Lernprogrammen](feature-summary/learning-programs.md) für spezifische Anweisungen.

## Phase 4 - Verwalten Ihres LMS (Learning Manager-Administrator) {#phase4managingyourlmscaptivateprimeadministrator}

### Ankündigungen {#announcements}

Ankündigungen sind für das Unternehmen nützlich, um alle wichtigen Informationen an alle Teilnehmer eines Kontos gleichzeitig zu verteilen. In der Learning Manager-Anwendung ist eine Ankündigung eine Multimedia-Nachricht (Text, Bild oder Video), die ein Administrator erstellen und an eine definierte Gruppe von Benutzergruppen und Lernobjekten senden kann. Sie können Ankündigungen sofort senden oder die automatische Auslösung an einem bestimmten Datum planen. Wenn Sie diese Funktion in der Lern-Manager-Anwendung verwenden möchten, wählen Sie im linken Bereich &quot;Ankündigungen&quot; aus und klicken Sie auf &quot;Hinzufügen&quot;, um Ankündigungen zu erstellen. Siehe [Hilfe zu Ankündigungen](feature-summary/announcements.md) für weitere Informationen.

### Benutzerregistrierung {#userenrollment}

Die Benutzerregistrierung ist ein wichtiger Schritt für eine LMS-Anwendung. In dieser Phase können Sie die Teilnehmer für verschiedene Lernobjekte der Learning Manager-Anwendung registrieren. Sie können Teilnehmer entweder manuell oder automatisiert registrieren, indem Sie Lernpläne verwenden.

#### Manuelle Registrierung {#manualenrollment}

* **Selbstregistrierung -** Wenn Sie diese Option beim Erstellen eines Lernobjekts aktivieren, können Teilnehmer sich selbst für die Lernobjekte registrieren.
* **Genehmigung durch Manager** - Wenn Sie diese Option beim Erstellen eines Kurses im Registrierungstyp auswählen, müssen Manager die Registrierung der Teilnehmer genehmigen.
* **Managernominierung** - Wenn Sie diesen Registrierungstyp während der Kurserstellung auswählen, müssen solche Kurse von Managern nominiert werden.
* **Registrierung durch Administrator** - In diesem Fall kann der Administrator einige Teilnehmer entsprechend den Anforderungen des Unternehmens registrieren.

Siehe [Hilfe zur Benutzerregistrierung](feature-summary/courses.md)für weitere Informationen.

Sie haben folgende Möglichkeiten, Teilnehmer für Lernobjekte manuell zu registrieren:

### Automatisierte Registrierung. {#automatedenrollment}

Automatisieren Sie die Registrierung der Teilnehmer für Lernobjekte mithilfe von Lernplänen.

#### Lernpläne (basierend auf Triggern) {#learningplansbasedontriggers}

Sie können Lernpläne verwenden, um Kurse, Lernprogramme oder Zertifizierungen basierend auf dem Auftreten bestimmter Ereignisse automatisch Teilnehmern zuzuweisen. Beispiel:

* Neuer Benutzer wird hinzugefügt
* Benutzer ändert Benutzergruppe
* Teilnehmer schließt ein Lernobjekt ab
* Benutzer schließt Kenntnisse ab

Siehe [Hilfe zu Lernplänen](feature-summary/learning-plans.md)  für weitere Informationen.

### Berichte erstellen {#createreports}

In dieser Phase können Sie mit dem Erstellen und Verwalten verschiedener Berichtstypen beginnen.

Mit dem Adobe-Lernmanager können Sie verschiedene Berichte erstellen, um die Aktivitäten der Teilnehmer zu verfolgen, zu überwachen und zu steuern. Zum Generieren von Berichten können Sie die folgenden drei Typen von Berichtsfunktionen verwenden:

* **Berichte-Dashboard** - Erstellen Sie Summierungsberichte, um verwertbare Einblicke in die Nutzung von Lerninhalten durch die Teilnehmer zu erhalten, basierend auf verschiedenen Kategorien wie Benutzergruppen, Effektivität, Teilnehmerzeit in Kursen und so weiter.
* **Teilnehmertranskripte** - Erstellen Sie teilnehmerorientierte Berichte mit dem vollständigen Verlauf der Teilnehmer vom Registrierungstag bis zum heutigen Tag.
* **Kursberichte** - Erstellen Sie Statistiken zur Kursnutzung durch Teilnehmer aus einzelnen Kursen. Sie können Quizberichte auch auf Kursebene erstellen.

Siehe  [Hilfe zu Berichten](feature-summary/reports.md) für weitere Informationen zum Berichtsgenerierungsprozess.

Weitere Informationen zur Nutzung der Funktionen der Learning Manager-Anwendung finden Sie unter [Hilfe zu Learning Manager](../topics.md) basierend auf jeder Rolle.

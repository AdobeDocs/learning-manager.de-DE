---
description: Dieses Dokument enthält die empfohlene Vorgehensweise für Unternehmen zur Einrichtung und Konfiguration von Adobe Learning Manager. Das Learning Manager-Team empfiehlt einen in Phasen unterteilten Ansatz für die ersten Schritte mit der Anwendung. Es ist nicht zwingend erforderlich, alle Phasen in einer bestimmten Reihenfolge zu durchlaufen.
jcr-language: en_us
title: Empfohlene Vorgehensweisen zum Einrichten von Learning Manager
contentowner: jayakarr
preview: true
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3387'
ht-degree: 71%

---



# Empfohlene Vorgehensweisen zum Einrichten von Learning Manager

Dieses Dokument enthält die empfohlene Vorgehensweise für Unternehmen zur Einrichtung und Konfiguration von Adobe Learning Manager. Das Learning Manager-Team empfiehlt einen in Phasen unterteilten Ansatz für die ersten Schritte mit der Anwendung. Es ist nicht zwingend erforderlich, alle Phasen in einer bestimmten Reihenfolge zu durchlaufen.

Diese Phasen können durch drei verschiedene Rollen von einer oder mehreren Personen basierend auf Ihrer Organisationseinrichtung durchgeführt werden. Die drei Rollen lauten wie folgt:

1. **IT-Administrator** - Der IT-Administrator führt aktivierungs- oder integrationsbezogene Aktivitäten durch, die mit der Learning Manager-Anwendung in einem Unternehmen verknüpft sind. Der IT-Administrator kann auch einzelne/mehrere Benutzer hinzufügen und die Rolle eines Integrationsadministrators ausführen.
1. **Autor** - Der Autor erstellt Lerninhalte, die für die Lernanforderungen des Unternehmens erforderlich sind. Der Autor von Schulungs- oder Lerninhalten in Ihrem Unternehmen kann mit dem Erstellen der grundlegenden Inhalte beginnen, die für die Learning Manager-Anwendung erforderlich sind.
1. **Learning Manager-Administrator** - Der Learning Manager-Anwendungsadministrator führt Konfigurations- und Einrichtungsaktivitäten durch. In einigen Unternehmen übernimmt der IT-Administrator unter Umständen auch die Rolle als Administrator der Learning Manager-Anwendung.

Sie können die unten stehende Infografik durchgehen, um sich einen Überblick über die Phasen und die zugehörigen Aufgaben zu verschaffen.

![](assets/learning-manager-getting-started.jpg)

In diesem Stadium wird davon ausgegangen, dass Ihr Unternehmen bereits den Lizenzschlüssel erhalten hat und Sie das Learning Manager-Konto aktiviert haben. Es folgen Erläuterungen zu den drei Ansätzen (siehe Infografik):

## Phase 1: Technische Einrichtung (IT-Administrator) {#phase1technicalsetupitadministrator}

In Track 1 kann der IT-Administrator Ihres Unternehmens zur Rolle des Integrationsadministrators in der Learning Manager-Anwendung wechseln und einige Aktivierungs- und Integrationsvorgänge wie folgt ausführen:

### Aktive Felder aktivieren/hinzufügen (Learning Manager-Administrator) {#enableaddactivefieldscaptivateprimeadministrator}

Zusätzlich zu den aktiven Feldern, die von den Benutzern während der Registrierung angegeben werden, kann der Administrator weitere aktive Felder hinzufügen. Außerdem kann der Administrator die Benutzerfelder aktivieren/deaktivieren. Die Werte für diese aktiven Felder werden aus den Metadaten aus verschiedenen Datenquellen generiert, die mit Benutzerkonten verknüpft sind. Weitere Informationen finden Sie in der [Hilfe zu aktiven Feldern](feature-summary/add-users-user-groups.md#active-fields).

### Einmalige Anmeldung (Single Sign-On, SSO) {#singlesignonsso}

Sie können mit der Adobe ID oder über einmalige Anmeldung (SSO) auf die Learning Manager-Anwendung zugreifen. Die einmalige Anmeldung (SSO) ist ein Verfahren, über das ein Benutzer einmal authentifiziert wird und mehrmals auf mehrere Anwendungen zugreifen kann. Diese Konfiguration ist für das Unternehmen nicht zwingend erforderlich. Wenn Ihr Unternehmen über einen auf SAML 2.0 basierten SSO-Anbieter verfügt, können Sie diesen für die Konfiguration der Learning Manager-Anwendung verwenden. Die Konfiguration ist auf Unternehmensebene und für die Learning Manager-Anwendung erforderlich. Wenn Sie SSO verwenden möchten, wenden Sie sich zwecks Konfigurationsanweisungen an den Support von Adobe. Weitere Informationen finden Sie in der Hilfe zu [Einstellungen](feature-summary/settings.md).

### Massenimport von Benutzern {#bulkimportofusers}

Wenn Sie eine große Anzahl von Benutzern in Ihrem Unternehmen haben, können Sie alle Benutzer mithilfe einer CSV-Datei komplett in die Learning Manager-Anwendung importieren. Bevor Sie diese Aufgabe ausführen, empfehlen wir Ihnen, die Benutzerliste aus der HR-Anwendung Ihres Unternehmens im CSV-Format zu exportieren. Selbst wenn Sie in diesem Stadium keinen Massenimport der Benutzer durchführen, können Sie sich mit dem CSV-Format vertraut machen. Um mit dem Importvorgang in Learning Manager zu beginnen, laden Sie die CSV-Datei hoch und ordnen Sie die Anwendungsdatenfelder den CSV-Spalten Ihrer Organisation zu. Weitere Informationen finden Sie in der [Hilfe zum Massenimport](add-users-in-bulk.md).

### Integration des FTP-Connectors {#ftpconnectorintegration}

Wenn Sie Mitarbeiter in Ihrem Unternehmen fortlaufend hinzufügen oder entfernen müssen, können Sie den Massenimport von Benutzern mithilfe des FTP-Connectors automatisieren. Sie müssen zunächst eine Verbindung herstellen. Anschließend können Sie eine CSV-Datei hochladen und die CSV-Attribute den entsprechenden Learning Manager-Feldern zuordnen. Sie können den automatischen Importvorgang planen und ihn bei Bedarf synchronisieren. Weitere Informationen finden Sie in der Hilfe für den [FTP-Connector](../integration-admin/feature-summary/connectors.md#ftpconnector).

### Integration des Salesforce-Connectors {#salesforceconnectorintegration}

Wenn Sie über ein Salesforce-Konto in Ihrem Unternehmen verfügen, können Sie den Import aller Benutzer von Salesforce in die Learning Manager-Anwendung automatisieren. Wenn Sie diese Funktion verwenden möchten, können Sie Learning Manager mithilfe des Salesforce-Connectors in das Salesforce-Konto integrieren und die Datensynchronisierung automatisieren. Verwenden Sie die automatische Planungsfunktion, um den automatisierten Benutzerimport regelmäßig durchzuführen. Sie können die Synchronisierung auch täglich durchführen. Weitere Informationen finden Sie in der [Hilfe zu Salesforce-Connector](../integration-admin/feature-summary/connectors.md#sfconnector).

### Adobe Connect-Integration {#adobeconnectintegration}

Wenn Sie Adobe Connect in Ihrem Unternehmen verwenden, können Sie es in die Adobe Learning Manager-Anwendung integrieren, um den Teilnehmern eine nahtlose Benutzererfahrung zu bieten. Durch diese Integration können die Teilnehmer innerhalb der Learning Manager-Anwendung mit nur einem Klick auf das virtuelle Klassenzimmer zugreifen, ohne dass sie sich erneut bei Adobe Connect anmelden müssen. Mit dieser Funktion können die Teilnehmer innerhalb der Learning Manager-Anwendung auch auf die aufgezeichneten virtuellen Klassenzimmersitzungen zugreifen. Um die Integration durchzuführen, müssen Sie die Einstellungen zuerst integrieren. Wählen Sie die Optionsfolge **Einstellungen > Adobe Connect > Jetzt konfigurieren**, geben Sie die Connect-URL sowie die Anmeldedaten an und führen Sie die Integration durch. Weitere Informationen finden Sie in der [Hilfe zu Adobe Connect](feature-summary/adobeconnect-integration.md).

### Registrierung der Salesforce-App {#salesforceappregistration}

Die Teilnehmer Ihres Unternehmens können nahtlos innerhalb ihrer Salesforce-Konten auf die Learning Manager-App zugreifen. Teilnehmer können über die Salesforce-Anwendung auf ihre zugewiesenen Lerninhalte (z. B. Kurse, Lernprogramme und Arbeitshilfen) zugreifen. Benutzer können außerdem über die Learning Manager-App in Salesforce auf Benachrichtigungen und Ankündigungen zugreifen. Um diese Funktion verwenden zu können, müssen Sie die Salesforce-App in der Learning Manager-Anwendung registrieren. Anweisungen zu Installation und Verwendung finden Sie in der [Hilfe zur Salesforce-App](../integration-admin/feature-summary/sfdc-app.md).

## Phase 2: Website-Konfiguration (Learning Manager-Administrator) {#phase2siteconfigurationcaptivateprimeadministrator}

Der Administrator der Learning Manager-Anwendung in Ihrem Unternehmen muss einige Funktionen konfigurieren bzw. einrichten, bevor Sie mit deren Implementierung für Ihre Teilnehmer beginnen.

### Branding {#branding}

Eine Organisation kann das Firmenlogo in der Learning Manager-Anwendung anzeigen, ihre eigene Domäne in der URL haben, den Namen der Organisation anzeigen und Farbschemata anzeigen, die der Marke einer Organisation entsprechen. Learning Manager ermöglicht Unternehmen, all diese Funktionen zu verwenden. Wenn Sie Einstellungen anpassen und Ihr eigenes Branding verwenden möchten, klicken Sie im linken Bereich auf den Abschnitt „Branding“. Klicken Sie neben all diesen Optionen auf „Bearbeiten“ und nehmen Sie Anpassungen Ihren Anforderungen entsprechend vor. Weitere Informationen finden Sie in der Hilfe zu [Branding und Designs](feature-summary/themes.md).

### Benutzer/Benutzergruppen hinzufügen {#addusersusergroups}

Da Teilnehmer die primären Benutzer Ihres Lerninhalts sind, ist das Hinzufügen von Benutzern im Learning Management-System der primäre Schritt. Fügen Sie Benutzer der Learning Manager-Anwendung hinzu und weisen Sie ihnen Rollen zu. Sie haben folgende Möglichkeiten, Benutzer hinzuzufügen:

#### Benutzer hinzufügen (intern) {#addusersinternal}

* **Als Einzelbenutzer**: Durch Hinzufügen einzelner Benutzer in der Learning Manager-Anwendung können Sie Test mit einigen Benutzern durchführen, bevor Sie diese in großer Zahl hinzuzufügen. Diese Option ist außerdem nützlich, wenn Sie nach dem Massenimport von Benutzern mehr einzelne Benutzer nach Bedarf hinzufügen möchten.
* **Selbstregistrierung** - Mit dieser Option können Administratoren ihren Mitarbeitern die Möglichkeit geben, sich bei Learning Manager zu registrieren.
* **Massenimport** (mit CSV-Upload): Mit dieser Option können Sie Benutzer gesammelt in die Learning Manager-Anwendung importieren. Als Voraussetzung müssen Sie die Liste der Benutzer im CSV-Format bereit halten, bevor Sie diese Funktion verwenden.

#### Benutzer hinzufügen (externe Profile) {#addusersexternalprofiles}

* Durch externe Registrierung: Durch Auswählen dieser Option können Sie externe Abteilungsmitglieder oder externe Mitarbeiter Ihres Unternehmens in der Anwendung registrieren.

#### Benutzergruppen hinzufügen {#addusergroups}

Die Learning Manager-Anwendung erstellt Standardbenutzergruppen basierend auf ähnlichen Attributen. Zusätzlich zu den Standardgruppen können Sie angepasste Benutzergruppen basierend auf Parametern (z. B. Bezeichnung, Standort) erstellen, damit Sie diese Gruppen in Gamification, Berichten usw. verwenden können. Weitere Informationen finden Sie in der [Hilfe zu „Benutzer hinzufügen“](feature-summary/add-users-user-groups.md).

### Rollen zuweisen {#assignroles}

Nach dem Hinzufügen der Benutzer zu Learning Manager kann der Administrator Benutzern den Unternehmensanforderungen entsprechend Rollen als Autor, Administrator oder Integrations-Admin zuweisen. Um Benutzern Rollen zuzuweisen, können Sie in der Administratoranmeldung im linken Fensterbereich auf **[!UICONTROL Benutzer]** klicken, das Kontrollkästchen für jeden Benutzernamen aktivieren und auf das Dropdownmenü **[!UICONTROL Aktionen]** klicken, um die Rolle auszuwählen, die Sie zuweisen möchten. Managerrollen werden von Adobe Learning Manager entsprechend den Rollen/Berechtigungen, die von Ihrem Unternehmen in der CSV-Datei angegeben wurden, zugewiesen. Sie können die Rollen von Benutzern als Manager auch ändern, indem Sie den Arbeitsablauf Benutzer bearbeiten verwenden. Weitere Informationen finden Sie in der [Hilfe zu „Benutzer hinzufügen“](feature-summary/add-users-user-groups.md).

### Benachrichtigungsvorlagen {#notificationtemplates}

Benachrichtigungen können für Benutzer in einem Learning Management System (LMS) sehr hilfreich sein, um ihren Status zu kennen oder über die Ereignisse/Aktivitäten informiert zu werden. Beim Erstellen von Kursen, beim Konfigurieren der Funktionen oder bei der Nutzung von Kursen treten Ereignisse für Benutzer ein, die Benachrichtigungen für Teilnehmer, deren Manager, Administratoren oder Autoren auslösen. In Learning Manager werden verschiedene E-Mail-Benachrichtigungsvorlagen in der Anwendung bereitgestellt. Als Administrator können Sie diese Ihren Unternehmensanforderungen entsprechend anpassen. Wenn Sie E-Mail-Benachrichtigungen erstellen möchten, wählen Sie im linken Bereich **E-Mail-Vorlagen** aus und klicken Sie auf den Namen der Vorlage. Weitere Informationen finden Sie in der [Hilfe zu E-Mail-Vorlagen](feature-summary/email-templates.md).

**E-Mail-Benachrichtigungen deaktivieren (empfohlen)**

Standardmäßig sind die Benachrichtigungen in der Learning Manager-Anwendung aktiviert. Sie können Benachrichtigungen in dieser Phase deaktivieren, wenn Sie Ihre Unternehmensmitarbeiter nicht informieren möchten.

### Abzeichen {#badges}

Abzeichen sind ein Leistungsnachweis, den sich Ihr Mitarbeiter für den Abschluss eines Kurses verdienen kann. Fachleute weltweit verwenden diese Abzeichen als Nachweis für das Erlangen bestimmter Qualifikationen oder Lernerfolge. Sie können eine Sammlung von Abzeichen erstellen, um diese Teilnehmern für den Abschluss von Lerninhalten zuweisen zu können. Wenn Sie mit der Erstellung von Abzeichen beginnen möchten, können Sie im linken Bereich auf die Funktion **[!UICONTROL Abzeichen]** klicken. Weitere Informationen finden Sie in der Hilfe zu [Abzeichen](feature-summary/badges.md).

### Feedback {#feedback}

Feedback gehört zu den wichtigsten Faktoren eines LMS, um den Lernfortschritt der Teilnehmer zu messen und die Qualität des Lerninhalts zu gewährleisten. In Learning Manager stehen Benutzern zwei Arten von Feedback zur Verfügung.

* L1-Feedback ist das Feedback von Teilnehmern nach Abschluss des Kurses.
* L3-Feedback ist das Feedback, das Manager den Teilnehmern basierend auf den Auswirkungen des Kurses auf das Verhalten der Teilnehmer und die täglichen Aktivitäten geben.

Das Verwenden dieser Funktion ist für Unternehmen optional. Administratoren können die Feedback-Vorlagen entsprechend der Anforderungen Ihres Unternehmens anpassen. Damit Sie diese Funktion verwenden können, muss der Administrator die Optionen für das L1- und L3-Feedback auf Kursinstanzstufe aktivieren. Wenn Sie das Feedback konfigurieren möchten, wählen Sie einen beliebigen Kurs aus, klicken Sie im linken Bereich auf „Standardwerte für Instanz“ und aktivieren Sie die Feedback-Option. Weitere Informationen finden Sie in der [Hilfe zum Feedback](feature-summary/courses.md).

### Gamification {#gamification}

Das Interesse der Teilnehmer beim Konsumieren des Inhalts aufrecht zu erhalten, ist eine der Herausforderungen, denen Unternehmen gegenüber stehen. Gamification erhöht die Kursabschlussrate, indem Teilnehmer durch Gaming-Techniken zur aktiven Teilnahme angeregt und motiviert werden, ihre Ziele zu erreichen. Teilnehmer können sich mit ihren Kollegen messen, um Punkte für verschiedene Lernaktivitäten zu sammeln, und die Stufen Bronze, Silber, Gold und Platin erreichen. Administratoren können jede Gamification-Aufgabe aktivieren/deaktivieren und die Zuweisung von Punkten zu Aufgaben ändern. In Learning Manager steht die Gamification-Funktion mit einigen Standardeinstellungen zur Verfügung. Sie können die Funktion einige Zeit mit den Standardeinstellungen verwenden und dann können Sie sich ggf. für deren Anpassung entscheiden. Das Konfigurieren/Ändern der Einstellungen dieser Funktion ist für Sie optional. Wenn Sie einen Fachexperten in Ihrem Unternehmen haben, wird die Konfiguration der Einstellungen vor deren Verwendung empfohlen. Weitere Informationen finden Sie in der [Hilfe zu Gamification](feature-summary/gamification.md).

### Lernobjekte erstellen {#createlearningobjects}

Dies ist die logische Phase, in der alle drei Ansätze (Ansatz 1, 2 und 3) zusammenlaufen, damit Sie zum nächsten Schritt übergehen können.

An dieser Stelle können Sie nach dem Erstellen von Modulen und Kursen mit der Erstellung von übergeordneten Lernobjekten (z. B. Zertifizierungen, Lernprogrammen oder Arbeitshilfen) fortfahren. Bevor Sie mit der Erstellung von Lernobjekten beginnen, stellen Sie sicher, dass Sie in der Learning Manager-Anwendung bereits einige Benutzer hinzugefügt sowie einige Module und Kurse erstellt haben.

#### Zertifizierungen erstellen {#createcertifications}

Die Zertifizierung ist ein Nachweis des Abschlusses eines Lerninhalts oder ein Leistungsnachweis für Teilnehmer (einmalig oder in einem wiederkehrenden Zeitraum). Die Registrierung von Teilnehmern für Lerninhalte kann erhöht werden, indem Zertifizierungen für die Teilnehmer nach Kursabschluss bereitgestellt werden. Als Administrator können Sie ein Zertifizierungsprogramm entweder intern gehostet oder von einer Drittpartei durchgeführt erstellen. Bei einer internen Zertifizierung definieren Sie die Kurse, die ein Teilnehmer absolvieren muss, um ein Zertifikat zu erhalten. Bevor Sie eine Zertifizierung erstellen, stellen Sie sicher, dass einige Kurse im Konto vorhanden sind. Weitere Informationen zum Erstellen von Zertifizierungen finden Sie in der [Hilfe zur Zertifizierung](feature-summary/certifications.md).

#### Arbeitshilfen erstellen {#createjobaids}

Arbeitshilfen sind ein Repository mit Schulungsinhalten, das den Teilnehmern ohne Registrierung oder Abschlusskriterien zur Verfügung steht. Die Teilnehmer können bei der Arbeit auf diese Arbeitshilfen zurückgreifen, wenn sie bei Aktivitäten oder Aufgaben im Unternehmen Unterstützung benötigen. Zwar ist die Verwendung von Arbeitshilfen als Teil der Kurserstellung nicht obligatorisch, doch empfiehlt das Learning Manager-Team, Arbeitshilfen als bewährtes Verfahren für Ihr Unternehmen zu erstellen. Informationen zum Erstellen von Arbeitshilfen finden Sie in der Hilfe zu [Arbeitshilfen](../authors/feature-summary/job-aids.md).

#### Lernprogramme erstellen {#createlearningprograms}

Lernprogramme umfassen eine Gruppe von Kursen, die speziell im Hinblick auf bestimmte Ziele für die Teilnehmer entwickelt wurden. Bevor Sie Lernprogramme erstellen, stellen Sie sicher, dass Sie bereits einige Kurse erstellt haben oder dass in Ihrem Konto bereits Kurse verfügbar sind.  Obwohl es für ein Unternehmen optional ist, diese Funktion zu verwenden, empfiehlt das Learning Manager-Team, diese zu verwenden, um Ihren Mitarbeitern fokussiertes Lernen zu vermitteln. Um mit der Verwendung von Lernprogrammen zu beginnen, klicken Sie im linken Bereich auf „Lernprogramme“, wählen Sie eine Gruppe von Kursen aus dem Katalog aus und veröffentlichen Sie sie. Genauere Anweisungen finden Sie in der Hilfe zu den [Lernprogrammen](feature-summary/learning-programs.md).

### Kataloge erstellen {#createcatalogs}

Sie können Kataloge in einem Unternehmen verwenden, um zielgerichtete Inhalte zu erstellen oder Inhalte für einen definierten Satz von Teilnehmern zu klassifizieren. In Learning Manager ist ein Katalog eine Sammlung von Lernobjekten (z. B. Kursen, Zertifizierungen oder Lernprogrammen). Sie können beim Erstellen von Katalogen die gewünschten Lernobjekte auswählen. Vergewissern Sie sich, dass Sie bereits eine Gruppe von Kursen, Zertifizierungen oder Lernprogrammen erstellt haben, bevor Sie die Kataloge erstellen. Sie können benutzerdefinierte Kataloge mit einem Satz von Lernobjekten erstellen, wenn Sie sie internen oder externen Benutzergruppen zuweisen möchten. Weitere Informationen zu Katalogen finden Sie in der Hilfe zu [Katalogen](feature-summary/catalogs.md).

### E-Mail-Benachrichtigungen/Benutzerzugriff aktivieren {#turnonemailnotificationsuseraccess}

In dieser Phase können Sie E-Mail-Benachrichtigungen an die Benutzer Ihrer Anwendungen aktivieren und auch den Benutzerzugriff aktivieren.

## Phase 3: Authoring von Kursen (Autor) {#phase3authoringcoursesauthor}

Inhaltsentwickler oder Autoren in Ihrem Unternehmen können mit dem Erstellen der Lerninhalte beginnen. Es ist obligatorisch, dass Sie Module und Kurse erstellen, da sie die Grundlage für alle Ihre Lerninhalte in der Learning Manager-Anwendung bilden.

### Module erstellen {#createmodules}

Module sind die grundlegenden Bausteine der Learning Manager-Anwendung. Um Ihre Lerninhalte zu organisieren, beginnen Sie, als Autor Module zu erstellen. Mit Learning Manager können Sie einen der vier Typen von Kursmodulen wählen, beispielsweise Klassenzimmer, Selbststudium, Aktivität und virtuelles Klassenzimmer. Weitere Informationen dazu, welcher Typ von Kursmodul für die Anforderungen Ihres Unternehmens am besten geeignet ist, finden Sie in der Hilfe zu [Modulen](../authors/how-to-choose-modules.md).

### Kurse erstellen {#createcourses}

Administratoren können die Autorenrolle in der Learning Manager-Anwendung annehmen und Kurse erstellen. In der Learning Manager-Anwendung bildet ein Kurs eine grundlegende Einheit mit einer Reihe von Modulen, die Teilnehmern zugewiesen werden können. Teilnehmer nutzen Kurse. Sie können mit dem Erstellen von Kursen beginnen, indem Sie die zuvor erstellten Module auswählen, Kenntnisse zuordnen, die Teilnehmer aus dem Kurs erlangen sollen, einem Kurs Stufen, Credits und Abzeichen zuordnen, basierend auf Ihrer Auswahl Arbeitshilfen, Voraussetzungen und Ressourcen auswählen und den Kurs veröffentlichen. Sie können auch mehrere Instanzen eines Kurses erstellen, damit Sie die Kursinstanzen mehreren Teilnehmern in verschiedenen Zeitzonen, Zeitplänen usw. zuweisen können. Weitere Informationen zum Erstellen eines Kurses finden Sie in der Hilfe zu [Kursen](../authors/feature-summary/courses.md).

### Lernobjekte erstellen {#Createlearningobjects-1}

Dies ist die logische Phase, in der alle drei Ansätze (Ansatz 1, 2 und 3) zusammenlaufen, damit Sie zum nächsten Schritt übergehen können.

An dieser Stelle können Sie nach dem Erstellen von Modulen und Kursen mit der Erstellung von übergeordneten Lernobjekten (z. B. Zertifizierungen, Lernprogrammen oder Arbeitshilfen) fortfahren. Bevor Sie mit der Erstellung von Lernobjekten beginnen, stellen Sie sicher, dass Sie in der Learning Manager-Anwendung bereits einige Benutzer hinzugefügt sowie einige Module und Kurse erstellt haben.

#### Zertifizierungen erstellen {#Createcertifications-1}

Die Zertifizierung ist ein Nachweis des Abschlusses eines Lerninhalts oder ein Leistungsnachweis für Teilnehmer (einmalig oder in einem wiederkehrenden Zeitraum). Die Registrierung von Teilnehmern für Lerninhalte kann erhöht werden, indem Zertifizierungen für die Teilnehmer nach Kursabschluss bereitgestellt werden. Als Administrator können Sie ein Zertifizierungsprogramm entweder intern gehostet oder von einer Drittpartei durchgeführt erstellen. Bei einer internen Zertifizierung definieren Sie die Kurse, die ein Teilnehmer absolvieren muss, um ein Zertifikat zu erhalten. Bevor Sie eine Zertifizierung erstellen, stellen Sie sicher, dass einige Kurse im Konto vorhanden sind. Weitere Informationen zum Erstellen von Zertifizierungen finden Sie in der [Hilfe zur Zertifizierung](feature-summary/certifications.md).

#### Arbeitshilfen erstellen {#CreateJobaids-1}

Arbeitshilfen sind ein Repository mit Schulungsinhalten, das den Teilnehmern ohne Registrierung oder Abschlusskriterien zur Verfügung steht. Die Teilnehmer können bei der Arbeit auf diese Arbeitshilfen zurückgreifen, wenn sie bei Aktivitäten oder Aufgaben im Unternehmen Unterstützung benötigen. Zwar ist die Verwendung von Arbeitshilfen als Teil der Kurserstellung nicht obligatorisch, doch empfiehlt das Learning Manager-Team, Arbeitshilfen als bewährtes Verfahren für Ihr Unternehmen zu erstellen. Informationen zum Erstellen von Arbeitshilfen finden Sie in der Hilfe zu [Arbeitshilfen](../authors/feature-summary/job-aids.md).

#### Lernprogramme erstellen {#Createlearningprograms-1}

Lernprogramme umfassen eine Gruppe von Kursen, die speziell im Hinblick auf bestimmte Ziele für die Teilnehmer entwickelt wurden. Bevor Sie Lernprogramme erstellen, stellen Sie sicher, dass Sie bereits einige Kurse erstellt haben oder dass in Ihrem Konto bereits Kurse verfügbar sind.  Obwohl es für ein Unternehmen optional ist, diese Funktion zu verwenden, empfiehlt das Learning Manager-Team, diese zu verwenden, um Ihren Mitarbeitern fokussiertes Lernen zu vermitteln. Um mit der Verwendung von Lernprogrammen zu beginnen, klicken Sie im linken Bereich auf „Lernprogramme“, wählen Sie eine Gruppe von Kursen aus dem Katalog aus und veröffentlichen Sie sie. Genauere Anweisungen finden Sie in der Hilfe zu den [Lernprogrammen](feature-summary/learning-programs.md).

## Phase 4: Verwalten Ihres LMS (Learning Manager-Administrator) {#phase4managingyourlmscaptivateprimeadministrator}

### Ankündigungen {#announcements}

Ankündigungen sind nützlich für das Unternehmen, um wichtige Informationen an alle Teilnehmer eines Kontos gleichzeitig zu verteilen. In der Learning Manager-Anwendung ist eine Ankündigung eine Multimedia-Nachricht (Text, Bild oder Video), die ein Administrator erstellen und an definierte Benutzergruppen und Lernobjekte übermitteln kann. Sie können Ankündigungen sofort senden oder deren automatische Auslösung an einem bestimmten Datum planen. Wenn Sie diese Funktion in der Learning Manager-Anwendung verwenden möchten, wählen Sie im linken Bereich „Ankündigungen“ aus und klicken Sie auf „Hinzufügen“, um Ankündigungen zu erstellen. Weitere Informationen finden Sie in der Hilfe zu [Ankündigungen](feature-summary/announcements.md).

### Benutzerregistrierung {#userenrollment}

Die Benutzerregistrierung ist ein wichtiger Schritt für eine LMS-Anwendung. In dieser Phase können Sie mit der Registrierung der Teilnehmer für verschiedene Lernobjekte der Learning Manager-Anwendung beginnen. Sie können Teilnehmer entweder manuell oder automatisch mithilfe von Lernplänen registrieren.

#### Manuelle Registrierung {#manualenrollment}

* **Selbstregistrierung -** Wenn Sie diese Option beim Erstellen eines Lernobjekts aktivieren, können sich die Teilnehmer selbst für die Lernobjekte registrieren.
* **Genehmigung durch Manager** - Wenn Sie diese Option beim Erstellen eines Kurses im Registrierungstyp auswählen, müssen Manager die Registrierung der Teilnehmer genehmigen.
* **Managernominierung** - Wenn Sie diesen Registrierungstyp während der Kurserstellung auswählen, müssen diese Kurse von Managern nominiert werden.
* **Registrierung durch Administrator** - In diesem Fall kann der Administrator einige Teilnehmer gemäß den Anforderungen des Unternehmens registrieren.

Weitere Informationen finden Sie in der [Hilfe zur Benutzerregistrierung](feature-summary/courses.md).

Sie können Teilnehmer für Lernobjekte unter Verwendung einer der folgenden vier Möglichkeiten manuell registrieren:

### Automatisierte Registrierung {#automatedenrollment}

Automatisieren Sie die Registrierung der Teilnehmer für Lernobjekte mithilfe von Lernplänen.

#### Lernpläne (basierend auf Auslöser) {#learningplansbasedontriggers}

Sie können Lernpläne verwenden, um Kurse, Lernprogramme und Zertifizierungen basierend auf dem Auftreten bestimmter Ereignisse automatisch den Teilnehmern zuzuweisen. Beispiel:

* Neuer Benutzer wird hinzugefügt
* Benutzer ändert Benutzergruppe
* Teilnehmer schließt ein Lernobjekt ab
* Benutzer erreicht eine Kompetenz

Weitere Informationen finden Sie im Inhalt der Hilfe zu [Lernplänen](feature-summary/learning-plans.md).

### Berichte erstellen {#createreports}

In dieser Phase können Sie mit der Erstellung und Verwaltung verschiedener Arten von Berichten beginnen.

Mit Adobe Learning Manager können Sie verschiedene Berichte erstellen, um die Aktivitäten der Teilnehmer zu verfolgen, zu überwachen und zu kontrollieren. Zum Generieren von Berichten können Sie die folgenden drei Typen von Berichtsfunktionen verwenden:

* **Berichte-Dashboard** - Erstellen Sie Summierungsberichte, um verwertbare Einblicke in die Nutzung von Lerninhalten durch Ihre Teilnehmer zu erhalten, basierend auf verschiedenen Kategorien wie Benutzergruppen, Effektivität, Teilnehmerzeit in Kursen usw.
* **Teilnehmertranskripte** - Erstellen Sie teilnehmerorientierte Berichte mit dem vollständigen Verlauf der Teilnehmer vom Registrierungstag bis zum heutigen Datum.
* **Kursberichte** - Erstellen Sie Statistiken zur Kursnutzung durch Teilnehmer aus einzelnen Kursen. Sie können Quizberichte auch auf Kursebene erstellen.

Weitere Informationen zum Berichtsgenerierungsprozess finden Sie in der [Hilfe zu Berichten](feature-summary/reports.md).

Weitere Informationen zur Nutzung der Funktionen der Learning Manager-Anwendung finden Sie in der [Hilfe zu Learning Manager](../topics.md) für jede Rolle.

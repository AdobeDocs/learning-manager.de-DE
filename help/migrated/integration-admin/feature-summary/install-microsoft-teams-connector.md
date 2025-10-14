---
description: Installieren des Microsoft Teams-Connectors in Adobe Learning Manager
jcr-language: en_us
title: Installieren des Microsoft Teams-Connectors in Adobe Learning Manager
contentowner: saghosh
exl-id: 68092187-ac69-4727-a3dc-f3047a1e164d
source-git-commit: 6192559436074c3270644850b202589961e7b81b
workflow-type: tm+mt
source-wordcount: '1138'
ht-degree: 17%

---

# Installieren des Microsoft Teams-Connectors in Adobe Learning Manager

## Übersicht

Microsoft Teams® ist eine beständige Chat-basierte Plattform für die Zusammenarbeit, die die Freigabe von Dokumenten, Online-Meetings und andere Funktionen für die Geschäftskommunikation vollständig unterstützt.

Adobe Learning Manager verwendet einen Connector für virtuelle Klassenzimmer, mit dem Microsoft Teams-Meetings mit Learning Manager integriert werden können.

Der Microsoft Teams-Connector verbindet Learning Manager und Microsoft Teams-Systeme, um eine automatische Synchronisierung virtueller Besprechungen zu ermöglichen. Die folgende Liste beschreibt die Funktionen des Microsoft Teams-Connectors:

**Virtuelle Sitzungen mit Microsoft Teams einrichten**

Mit diesem Connector können Sie Ihr Adobe Learning Manager-Konto in Ihr Microsoft Teams-Konto integrieren. Nach der Integration ermöglicht der Connector einem Autoren in Learning Manager, Microsoft Teams als Technologiedienstleister für die in Learning Manager erstellten Module vom Typ „Virtuelles Klassenzimmer“ zu verwenden.

**Microsoft Teams erlauben, Teilnehmer beim Betreten eines virtuellen Klassenzimmers zu authentifizieren**

Dieser Connector unterstützt Sie beim Einrichten des Microsoft Teams-Meetingveranstalters über den Lernmanager beim Erstellen eines Meetings. Der Besprechungsorganisator kann die Lobby verwalten, um den Zutritt zu einer Besprechung einzuschränken oder zuzulassen, sowie andere von Microsoft Teams bereitgestellte Besprechungsoptionen steuern.

**Synchronisierung der automatisierten Benutzerabwicklung verwenden**

Der automatisierte Benutzerabschlusssynchronisierungsprozess ermöglicht es einem Learning Manager-Administrator, automatisch die Abschlussdatensätze und die Aufzeichnungs-URL für das Microsoft Teams-Meeting abzurufen.

## Rollen in Microsoft Teams

Wenn Sie ein Meeting mit mehreren Teilnehmern organisieren, können Sie jedem Teilnehmer Rollen zuweisen, damit ein Teilnehmer weiß, was er in dem Meeting tun kann.

Es stehen zwei Rollen zur Auswahl: **Moderator** und **Teilnehmer**.

Weitere Informationen finden Sie unter [Rollen in einem Teams-Meeting - Microsoft](https://support.microsoft.com/en-us/office/roles-in-a-teams-meeting-c16fa7d0-1666-4dde-8686-0a0bfe16e019).

## Microsoft Teams-Connector einrichten

>[!NOTE]
>
>Die unten als &lt;Developer/Optional> markierten Elemente sind optional und dienen hauptsächlich zum Einrichten von Test-/Entwickler-Mandanten mit Microsoft, falls der Benutzer keinen Produktionsmandanten hat. Diese sind optional, da sie meist bereits vom Administrator Ihres Teams durchgeführt worden wären.

## Erstellen eines Entwicklerkontos für E5 Microsoft &lt;Developer/Optional>

Sie können auf den Microsoft Teams-Connector zugreifen, wenn Sie Office 365 E3 oder Office 365 E5 verwenden. Die empfohlene Option ist Office 365 E5.

* Besuchen Sie die Seite mit den [Microsoft-Abos](https://www.microsoft.com/en-in/microsoft-365/enterprise/compare-office-365-plans?&ef_id=CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE:G:s&OCID=AID2100137_SEM_CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE:G:s&lnkd=Google_O365SMB_Brand&gclid=CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE). Auf der Webseite können Sie entweder ein E3- oder E5-Konto kaufen oder auf Kostenlos testen klicken.
* Geben Sie die erforderlichen Informationen an und erstellen Sie ein Konto.

>[!NOTE]
>
>Das Konto muss das Format &quot;`<username>@<company name>.onmicrosoft.com`&quot; verwenden.

## Anwendungsconnector für Microsoft Teams erstellen

1. Besuchen Sie das [Microsoft Azure®-Portal](https://portal.azure.com/).
1. Melden Sie sich mit dem Microsoft E5-Konto an, das Sie im vorherigen Abschnitt erstellt haben.
1. Suchen Sie nach **Azure Active Directory**.
1. Klicken Sie auf **[!UICONTROL App-Registrierungen]**.
1. Klicken Sie auf **[!UICONTROL Neue Registrierung]**, geben Sie die folgenden Details ein und registrieren Sie die Anwendung:

   1. **Name** - Ein beliebiger Name Ihrer Wahl.
   1. **Unterstützte Kontotypen** - Konten in einem beliebigen Organisationsverzeichnis (beliebiges Azure Active Directory - Mandant).
   1. **Umleitungs-URI (optional)** - Optionales Feld, das die Antwort-URL angibt.

1. Beachten Sie in der Spalte **Essentials** die folgenden IDs, die während der Integration weiter verwendet werden:

   1. **Anwendungs-ID (Client)**
   1. **Verzeichnis (Mandant)-ID**

1. Suchen Sie nach Clientanmeldeinformationen und klicken Sie auf **[!UICONTROL Zertifikat oder Schlüssel hinzufügen]**.
1. Klicken Sie auf **[!UICONTROL Neuer Client-Schlüssel]** und fügen Sie die folgenden Details hinzu:

   1. **Beschreibung** - Geben Sie einen beliebigen Namen ein.
   1. **Läuft ab** - Beliebiger Wert (empfohlener Wert: 24 Monate). Stellen Sie sicher, dass neue Client-Anmeldeinformationen generiert werden, sobald die vorherige abläuft).

Beachten Sie den Client-Schlüssel, der während der Integration weiter verwendet wird.

## Zugriffsberechtigung für den Microsoft Teams-Connector abrufen

1. Besuchen Sie das [Microsoft Azure-Portal](https://portal.azure.com/).
1. Melden Sie sich mit der Microsoft E5 an, die Sie zuvor erstellt haben.
1. Suchen Sie nach **Azure Active Directory**.
1. Klicken Sie auf **[!UICONTROL App-Registrierungen]**.
1. Klicken Sie auf die App, die Sie im vorherigen Abschnitt erstellt haben.
1. Klicken Sie auf **[!UICONTROL API-Berechtigungen]**.
1. Klicken Sie auf **[!UICONTROL Berechtigung hinzufügen]**.
1. Wählen Sie **[!UICONTROL Microsoft Graph]** > **[!UICONTROL Anwendungsberechtigungen]** aus und fügen Sie die folgenden Berechtigungen hinzu:

   1. Chat.Read.All
   1. Directory.Read.All
   1. OnlineMeetingArtifact.Read.All
   1. OnlineMeetings.Read.All
   1. OnlineMeetings.ReadWrite.All
   1. User.Read.All
   1. OnlineMeetingRecording.Read.All

1. Klicken Sie auf **[!UICONTROL Administratorzugriff für Adobe gewähren]**.
1. Klicken Sie auf **[!UICONTROL App-Rollen]** > **[!UICONTROL App-Rolle erstellen]**.
1. Geben Sie die folgenden Werte ein:

   1. **Anzeigename** - Name des API-/Berechtigungsnamens (z. B. Calendars.ReadWrite).

   1. **Zulässige Membertypen** - Geben Sie sowohl Benutzer als auch Anwendungen an (Benutzer/Gruppen + Anwendungen).

   1. **Wert** - Name des API-/Berechtigungsnamens (z. B. Calendars.ReadWrite).

   1. **Beschreibung** - Name des API-/Berechtigungsnamens (z. B. Calendars.ReadWrite).

   1. **Möchten Sie diese App-Rolle aktivieren?** - Aktivieren Sie dieses Kontrollkästchen.

1. Wiederholen Sie die vorangegangenen Schritte für alle neun hinzugefügten API/Berechtigungen.

## Konfigurieren der Zugriffsrichtlinie mithilfe von PowerShell-Skripten

Um die Anwendungszugriffsrichtlinie für den Microsoft Teams-Connector durch Ausführen von PowerShell-Skripts zu konfigurieren, führen Sie die in diesem [Dokument](https://docs.microsoft.com/en-us/graph/cloud-communication-online-meeting-application-access-policy) beschriebene Vorgehensweise aus.

Dadurch kann der Connector auf Microsoft Teams-Onlinemeetings zugreifen.

>[!NOTE]
>
>Führen Sie im obigen Dokument auch den optionalen Schritt 5 aus, um sicherzustellen, dass jedem aktiven Benutzer die Rolle des Organisators in der Learning Manager-Autor-App gewährt werden kann. Wenn dieser Schritt nicht ausgeführt wird, verfügen die Benutzer nicht über die erforderlichen Zugriffsberechtigungen, um Organisatoren zu sein, und die Meetingerstellung schlägt fehl (Microsoft APIs betrachten den Organisator als Ersteller eines Teams-Meetings).

## Einrichten des Microsoft Teams-Connectors im Lernmanager

1. Melden Sie sich bei Learning Manager als **Integrationsadministrator** an.

1. Wählen Sie auf der Seite &quot;Connectors&quot; den Connector für Microsoft Teams aus und klicken Sie auf **[!UICONTROL Verbinden]**.

1. Geben Sie folgende Werte ein:

   1. **Verbindungsname** - Geben Sie den Namen an, den der Autor beim Erstellen der Sitzung sehen wird.

   1. **Microsoft Teams-Mandanten-ID**: Geben Sie den zuvor ermittelten Wert ein.

   1. **Microsoft Teams-Client-ID**: Geben Sie den zuvor ermittelten Wert ein.

   1. **Geheimer Microsoft Teams-Client**: Geben Sie den zuvor ermittelten Wert ein.

   1. **E-Mail-Adresse des Microsoft Teams-Administratorbenutzers**: Geben Sie die E-Mail-Adresse des Standardveranstalters ein. Dieser Benutzer (in der Regel ein Dienstbenutzer) ist der Ersteller des Meetings, falls kein expliziter Organisator in der Learning Manager Author-App ausgewählt ist.

## Benutzern Lizenzen zuweisen &lt;Developer/Optional>

1. [https://admin.microsoft.com/#/homepage](https://admin.microsoft.com/#/homepage) besuchen.
1. Klicken Sie auf **[!UICONTROL Benutzer]** > **[!UICONTROL Aktive Benutzer]**.
1. Klicken Sie auf **[!UICONTROL Weitere Aktionen für Benutzer]** für die Benutzer, denen Sie Zugriff auf Microsoft Teams gewähren möchten.
1. Klicken Sie auf **[!UICONTROL Produktlizenzen verwalten]**.
1. Lizenz für Office 365 E5 ohne Audiokonferenzen aktivieren.

<!--## Record a session

The API used for recording a session is a protected API. To access the API, you must request access from Microsoft. For more information, see this  [document](https://docs.microsoft.com/en-us/graph/teams-protected-apis).

In the document,

*"To request access to these protected APIs, complete the following  [request form](https://aka.ms/teamsgraph/requestaccess). We review access requests every Wednesday and deploy approvals every Friday, except during major holiday weeks in the U.S. Submissions during those weeks will be processed the following non-holiday week. To verify whether your request has been approved, test your application access on the next applicable Monday."*

For learners, the recording URL is displayed on the VC course overview page.

After 30 minutes of completing a course, the attendance for the learner gets marked. -->

## Häufig gestellte Fragen

+++Wer ist ein Organizer und ein Moderator?

In der [Dokumentation](https://support.microsoft.com/en-us/office/roles-in-a-teams-meeting-c16fa7d0-1666-4dde-8686-0a0bfe16e019) von Microsoft finden Sie verschiedene Rollen und Funktionen, die von Microsoft Teams unterstützt werden.

+++

+++Sollte ein Organisator ein registrierter Benutzer sowohl im Lernmanager als auch in den Microsoft Teams sein?

Ja, der Organisator sollte auch Teil von Learning Manager und Microsoft Teams sein. Darüber hinaus muss der Organisator Teil desselben Microsoft-Mandanten sein, der in der Integrationsadministrator-App konfiguriert ist.

+++

+++Sollte ein Moderator ein registrierter Benutzer sowohl im Lernmanager als auch in den Microsoft Teams sein?

Ja, der Moderator sollte auch Teil des Lernmanagers und des Microsoft Teams sein. Der Moderator muss über eine Azure Active Directory-ID verfügen (kann Teil desselben Mandanten wie der Organisator oder eines anderen Mandanten sein). Darüber hinaus können auch anonyme Benutzer (Benutzer, die sich nur mit dem Benutzernamen anmelden und nicht Teil von Active Directory sind) während des Meetings von den Veranstaltern/bestehenden Moderatoren zu Moderatoren gemacht werden.

+++

+++Microsoft Teams bietet Meetings, Webinare und Live-Veranstaltungen. Welches unterstützt der Teams-Connector?

Derzeit unterstützt der Teams-Connector nur Meetings in Microsoft Teams. Weitere Informationen finden Sie in diesem [Dokument](https://docs.microsoft.com/en-us/microsoftteams/quick-start-meetings-live-events).

+++

---
description: Microsoft Teams-Connector im Adobe Learning Manager installieren
jcr-language: en_us
title: Microsoft Teams-Connector im Adobe Learning Manager installieren
contentowner: saghosh
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '1258'
ht-degree: 0%

---



# Microsoft Teams-Connector im Adobe Learning Manager installieren

## Übersicht

Microsoft® Teams® ist eine beständige Chat-basierte Plattform für die Zusammenarbeit, die die Freigabe von Dokumenten, Online-Meetings und andere Funktionen für die Geschäftskommunikation vollständig unterstützt.

Adobe Learning Manager verwendet einen Connector für virtuelle Klassenzimmer, mit dem Microsoft Teams-Meetings mit Learning Manager integriert werden können.

Der Microsoft Teams-Connector verbindet Learning Manager- und Microsoft Teams-Systeme, um die automatische Synchronisierung virtueller Meetings zu ermöglichen. In der folgenden Liste werden die Funktionen des Microsoft Teams-Connectors beschrieben:

**Einrichten virtueller Sitzungen mit Microsoft Teams**

Dieser Connector unterstützt Sie bei der Integration Ihres Adobe Learning Manager-Kontos in Ihr Microsoft Teams-Konto. Nach der Integration ermöglicht der Connector es einem Autor in Learning Manager, Microsoft Teams als Technologiedienstleister für die in Learning Manager erstellten virtuellen Klassenzimmermodule zu verwenden.

**Microsoft Teams die Authentifizierung von Teilnehmern beim Betreten eines virtuellen Klassenzimmers erlauben**

Dieser Connector unterstützt Sie beim Einrichten des Microsoft Teams-Meetingveranstalters über den Lernmanager beim Erstellen eines Meetings. Der Meetingveranstalter kann die Lobby verwalten, um den Zugang zu einem Meeting einzuschränken oder zuzulassen, sowie andere Meetingoptionen von Microsoft Teams steuern.

**Verwendung der automatisierten Benutzerabschlusssynchronisation**

Der automatisierte Benutzerabschlusssynchronisierungsprozess ermöglicht es einem Learning Manager-Administrator, automatisch die Abschlussdatensätze und die Aufzeichnungs-URL für das Microsoft Teams-Meeting abzurufen.

## Rollen in Microsoft Teams

Wenn Sie ein Meeting mit mehreren Teilnehmern organisieren, können Sie jedem Teilnehmer Rollen zuweisen, damit ein Teilnehmer weiß, was er in dem Meeting tun kann.

Es gibt zwei Rollen, aus denen Sie wählen können: **Moderatorin** und **Anwesende**.

Weitere Informationen finden Sie unter  [Rollen in einem Teams-Meeting - Microsoft](https://support.microsoft.com/en-us/office/roles-in-a-teams-meeting-c16fa7d0-1666-4dde-8686-0a0bfe16e019).

## Microsoft Teams-Connector einrichten

>[!NOTE]
>
>Elemente markiert &lt;developer optional=&quot;&quot;> Die folgenden sind optional und dienen hauptsächlich zum Einrichten von Test-/Entwickler-Mandanten mit Microsoft, falls der Benutzer keinen Produktionsmandanten hat. Diese sind optional, da sie meist bereits vom Administrator Ihres Teams durchgeführt worden wären.

## Erstellen eines Entwicklerkontos für E5 Microsoft &lt;developer optional=&quot;&quot;>

Sie können auf den Microsoft Teams-Connector zugreifen, wenn Sie Office 365 E3 oder Office 365 E5 verwenden. Die empfohlene Option ist Office 365 E5.

* Auf der Seite [Microsoft-Abo-Seite](https://www.microsoft.com/en-in/microsoft-365/enterprise/compare-office-365-plans?&amp;ef_id=CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE:G:s&amp;OCID=AID2100137_SEM_CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE:G:s&amp;lnkd=Google_O365SMB_Brand&amp;gclid=CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE) . Auf der Webseite können Sie entweder ein E3- oder E5-Konto kaufen oder auf Kostenlos testen klicken.

* Geben Sie die erforderlichen Informationen an und erstellen Sie ein Konto.

>[!NOTE]
>
>Das Konto muss das Format verwenden. `<username>@<company name>.onmicrosoft.com`.

## Anwendungsconnector für Microsoft Teams erstellen

1. Auf der Seite  [Microsoft Azure®-Portal](https://portal.azure.com/).
1. Melden Sie sich mit dem Microsoft E5-Konto an, das Sie im vorherigen Abschnitt erstellt haben.
1. Suchen nach **Azure Active Directory**.
1. Klicken **[!UICONTROL App-Registrierungen]**.
1. Klicken **[!UICONTROL Neue Registrierung]**, geben Sie die folgenden Details ein und registrieren Sie die Anwendung:

   1. **Name** - Jeder Name Ihrer Wahl.
   1. **Unterstützte Kontotypen** - Konten in einem beliebigen Organisationsverzeichnis (beliebiges Azure Active Directory - Multitenant).
   1. **URI umleiten (optional)** - Optionales Feld zur Angabe der Antwort-URL.

1. Im Dialogfeld &quot; **Essentials** die folgenden IDs, die während der Integration weiter verwendet werden:

   1. **Anwendungs-ID (Client)**
   1. **Verzeichnis-ID (Mandant)**

1. Suchen Sie nach Clientanmeldeinformationen und klicken Sie auf **[!UICONTROL Zertifikat oder Geheimnis hinzufügen]**.
1. Klicken **[!UICONTROL Neuer Client-Schlüssel]** und fügen Sie die folgenden Details hinzu:

   1. **Beschreibung** - Geben Sie einen beliebigen Namen ein.
   1. **Läuft ab** - Beliebiger Wert (empfohlener Wert: 24 Monate). Stellen Sie sicher, dass neue Clientanmeldeinformationen generiert werden, sobald die vorherige abläuft.)

Beachten Sie den Client-Schlüssel, der während der Integration weiter verwendet wird.

## Zugriffsberechtigung für den Microsoft Teams-Connector abrufen

1. Auf der Seite  [Microsoft Azure-Portal](https://portal.azure.com/).
1. Melden Sie sich mit der Microsoft E5 an, die Sie zuvor erstellt haben.
1. Suchen nach **Azure Active Directory**.
1. Klicken **[!UICONTROL App-Registrierungen]**.
1. Klicken Sie auf die Applikation, die Sie im vorherigen Abschnitt erstellt haben.
1. Klicken **[!UICONTROL API-Berechtigungen]**.
1. Klicken **[!UICONTROL Berechtigung hinzufügen]**.
1. Auswählen **[!UICONTROL Microsoft Graph]** > **[!UICONTROL Anwendungsrechte]** und die folgenden Berechtigungen hinzufügen:

   1. Chat.Read.All
   1. Directory.Read.All
   1. OnlineMeetingArtifact.Read.All
   1. OnlineMeetings.Read.All
   1. OnlineMeetings.ReadWrite.All
   1. User.Read.All

1. Klicken **[!UICONTROL Administratorzugriff für Adobe gewähren]**.
1. Klicken **[!UICONTROL App-Rollen]** > **[!UICONTROL App-Rolle erstellen]**.
1. Geben Sie die folgenden Werte ein:

   1. **Anzeigename** - Name des API-/Berechtigungsnamens (z. B. Calendars.ReadWrite).

   1. **Zulässige Elementtypen** - Benutzer und Anwendungen (Benutzer/Gruppen + Anwendungen) angeben.

   1. **Wert** - Name des API-/Berechtigungsnamens (z. B. Calendars.ReadWrite).

   1. **Beschreibung** - Name des API-/Berechtigungsnamens (z. B. Calendars.ReadWrite).

   1. **Möchten Sie diese App-Rolle aktivieren?** - Aktivieren Sie dieses Kontrollkästchen.

1. Wiederholen Sie die vorangegangenen Schritte für alle neun hinzugefügten API/Berechtigungen.

## Konfigurieren der Zugriffsrichtlinie mithilfe von PowerShell-Skripten

Um die Anwendungszugriffsrichtlinie für den Microsoft Teams-Connector zu konfigurieren, indem Sie PowerShell-Skripte ausführen, führen Sie die folgenden Schritte aus:  [Dokument](https://docs.microsoft.com/en-us/graph/cloud-communication-online-meeting-application-access-policy).

Dadurch kann der Connector auf Microsoft Teams-Online-Meetings zugreifen.

>[!NOTE]
>
>Führen Sie im obigen Dokument auch den optionalen Schritt 5 aus, um sicherzustellen, dass jedem aktiven Benutzer die Rolle des Organisators in der Learning Manager-Autor-App gewährt werden kann. Wenn dieser Schritt nicht ausgeführt wird, verfügen die Benutzer nicht über die erforderlichen Zugriffsberechtigungen, um Organisatoren zu sein, und die Meetingerstellung schlägt fehl (Microsoft APIs betrachten den Organisator als Ersteller eines Teams-Meetings).

## Einrichten des Microsoft Teams-Connectors im Lernmanager

1. Melden Sie sich bei Learning Manager als Integrations-Admin an.

1. Wählen Sie auf der Seite Connectors die Option Microsoft Teams Connector und klicken Sie auf **[!UICONTROL Vernetzen]**.

1. Geben Sie folgende Werte ein:

   1. **Verbindungsname** - Geben Sie den Namen ein, den der Autor beim Erstellen der Sitzung sehen wird.

   1. **Microsoft Teams Mandanten-ID** - Geben Sie den zuvor ermittelten Wert ein.

   1. **Microsoft Teams-Client-ID** - Geben Sie den zuvor ermittelten Wert ein.

   1. **Geheimer Microsoft Teams-Client** - Geben Sie den zuvor ermittelten Wert ein.

   1. **Microsoft Teams-Admin-Benutzer-E-Mail** - Geben Sie die Standard-E-Mail-Adresse des Organisators ein. Dieser Benutzer (in der Regel ein Dienstbenutzer) ist der Ersteller des Meetings, falls kein expliziter Organisator in der Learning Manager Author-App ausgewählt ist.

## Benutzern Lizenzen zuweisen &lt;developer optional=&quot;&quot;>

1. Besuchen [https://admin.microsoft.com/#/homepage](https://admin.microsoft.com/#/homepage).
1. Klicken **[!UICONTROL Benutzer]** > **[!UICONTROL Aktive Benutzer]**.
1. Klicken **[!UICONTROL Weitere Aktionen für Benutzer]** für die Benutzer, denen Sie Zugriff auf Microsoft Teams gewähren möchten.
1. Klicken **[!UICONTROL Produktlizenzen verwalten]**.
1. Lizenz für Office 365 E5 ohne Audiokonferenzen aktivieren.

## Eine Session aufzeichnen

Die zum Aufzeichnen einer Sitzung verwendete API ist eine geschützte API. Um auf die API zugreifen zu können, müssen Sie den Zugriff von Microsoft anfordern. Weitere Informationen finden Sie in diesem  [Dokument](https://docs.microsoft.com/en-us/graph/teams-protected-apis).

Im Dokument

*&quot;Um den Zugriff auf diese geschützten APIs anzufordern, führen Sie die folgenden Schritte aus:  [Antragsformular](https://aka.ms/teamsgraph/requestaccess). Wir überprüfen Zugriffsanfragen jeden Mittwoch und stellen Genehmigungen jeden Freitag bereit, außer während großer Feiertagswochen in den USA. Einreichungen in diesen Wochen werden in der folgenden Woche ohne Feiertage bearbeitet. Um zu überprüfen, ob Ihre Anforderung genehmigt wurde, testen Sie Ihren Anwendungszugriff am nächsten entsprechenden Montag.&quot;*

Für Teilnehmer wird die Aufzeichnungs-URL auf der VC-Kursübersichtsseite angezeigt.

Nach 30 Minuten nach Abschluss eines Kurses wird die Anwesenheit für den Teilnehmer markiert.

## Häufig gestellte Fragen

+++Wer ist ein Organizer und ein Moderator?

In den  [Dokumentation](https://support.microsoft.com/en-us/office/roles-in-a-teams-meeting-c16fa7d0-1666-4dde-8686-0a0bfe16e019) von Microsoft für verschiedene Rollen und Funktionen, die von Microsoft Teams unterstützt werden.

+++

+++Sollte ein Organisator ein registrierter Benutzer sowohl im Lernmanager als auch in den Microsoft Teams sein?

Ja, der Organisator sollte auch Teil des Lernmanagers und der Microsoft Teams sein. Darüber hinaus muss der Organisator Teil desselben Microsoft-Mandanten sein, der in der Integrationsadministrator-App konfiguriert ist.

+++

+++Sollte ein Moderator ein registrierter Benutzer sowohl im Lernmanager als auch in den Microsoft Teams sein?

Ja, der Moderator sollte auch Teil des Lernmanagers und des Microsoft Teams sein. Der Moderator muss über eine Azure Active Directory-ID verfügen (kann Teil desselben Mandanten wie der Organisator oder eines anderen Mandanten sein). Darüber hinaus können auch anonyme Benutzer (Benutzer, die sich nur mit dem Benutzernamen anmelden und nicht Teil von Active Directory sind) während des Meetings von den Veranstaltern/bestehenden Moderatoren zu Moderatoren gemacht werden.

+++

+++Microsoft Teams bietet Meetings, Webinare und Live-Veranstaltungen. Welche Formate unterstützt der Teams-Connector?

Derzeit unterstützt der Teams-Connector nur Meetings in Microsoft Teams. Weitere Informationen finden Sie in diesem  [Dokument](https://docs.microsoft.com/en-us/microsoftteams/quick-start-meetings-live-events).

+++

---
description: Adobe Learning Manager-App für Microsoft Teams
jcr-language: en_us
title: Adobe Learning Manager-App für Microsoft Teams
contentowner: saghosh
source-git-commit: 81dd3cecf7393c08434a70e15457d967a56df8d3
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---


# Adobe Learning Manager-App für Microsoft Teams

## Einrichten

Das Einrichten von ALM in MS Teams umfasst drei Schritte und erfordert Unterstützung vom ALM-Administrator und Microsoft Azure-Administrator. In einigen Organisationen sind der Azure-Administrator und der MS Teams-Administrator nicht identisch und benötigen daher auch zusätzliche MS Teams-Administratoren.

**ALM-Admin - Integrations-Admin-Rolle genehmigt Teams-App**

Nachdem der Integrationsadministrator die MS Teams-App genehmigt hat, ist die Adobe Learning Manager-App im MS Teams App Store verfügbar und die Teilnehmer können darauf zugreifen. Die App enthält jedoch keine Benachrichtigungen und keine unbeaufsichtigte Anmeldung, und die App wird nicht für die Teilnehmer in MS Teams angeheftet.

**Microsoft Azure Admin genehmigt die Berechtigung für ALM-App im Azure Dashboard**

Der Azure-Administrator muss die erforderlichen Berechtigungen für die ALM-App genehmigen. Dadurch kann die ALM-App Benachrichtigungen an MS Teams senden und eine unbeaufsichtigte Anmeldung zulassen. Bei der unbeaufsichtigten Anmeldung müssen sich Benutzer nicht separat beim Adobe Learning Manager im Browser anmelden.

**MS Teams-Administrator erstellt eine Richtlinie für ALM-Teams**

Der MS Teams-Administrator in seinem Admin Center sollte die ALM-App für alle Benutzer anheften und als globale Richtlinie zulassen. Wenn ALM nur von einer bestimmten Gruppe im Unternehmen verwendet wird, muss der MS Teams-Administrator eine benutzerdefinierte Richtlinie auswählen und diese nur auf diese bestimmte Gruppe anwenden.

## Integration Admin-Rolle genehmigt Teams-App

Führen Sie die folgenden Schritte aus:

1. Wählen Sie in der Integrationsadministrator-App **[!UICONTROL Anwendungen]** > **[!UICONTROL Highlights]** und wählen Sie **[!UICONTROL ALM Teams-App]**.

   ![](assets/featuredapps.jpg)
   *ALM Teams-App auswählen*

1. Wählen Sie in der oberen rechten Ecke des Bildschirms **[!UICONTROL Genehmigen]**.

   ![](assets/integration_admin_approval_form.jpg)
   *Wählen Sie auf der Seite mit den App-Einstellungen Genehmigen .*

1. Auswählen **[!UICONTROL OK]** im angezeigten Dialogfeld.

   ![](assets/integration_admin_approved_dialog_box.jpg)
   *Nach Genehmigung auf &quot;OK&quot; klicken*

1. Nach der Genehmigung wird &quot;ALM Teams App&quot; im Abschnitt &quot;Externe Apps&quot; angezeigt.

   ![](assets/integration_admin_external_apps.jpg)
   *Die ALM Teams-App wird auf der Seite Apps angezeigt*

Jetzt können Benutzer auf MS Teams auf die ALM-App zugreifen.

## Microsoft Azure Admin genehmigt die Berechtigung für ALM-App im Azure Dashboard

Führen Sie die folgenden Schritte aus:

1. Navigieren Sie als Azure-Administrator zum Abschnitt Azure Active Directory verwalten im Azure-Dashboard.

   ![](assets/microsoft_azure.jpg)
   *Azure-Dashboard starten*

1. Fügen Sie den folgenden Link in ein separates Browserfenster ein:

   `https://login.microsoftonline.com/<tenantIdTobeReplaced>/oauth2/authorize?client_id=8d349d9f-bf59-4ece-8022-a41e87d81903&response_type=code&redirect_uri=https://learningmanager.adobe.com`

1. Ersetzen Sie im obigen Link `<tenantIdTobeReplaced>` mit der Mandanten-ID, die auf der Seite &quot;Übersicht&quot; unten verfügbar ist. Geben Sie die neue URL ein.

1. Fügen Sie die Adobe Learning Manager-App zu Ihren Azure-Anwendungen hinzu.

   ![](assets/microsoft_azure_dashboard.jpg)
   *Zu Azure hinzufügen*

1. Wählen Sie die Registerkarte Unternehmensanwendungen und dann Alle Anwendungen. ALMTeamsApp ist hier aufgelistet.

   ![](assets/microsoft_azure_enterprise_applications.jpg)
   *ALM-App anzeigen*

1. Klicken Sie auf die App und navigieren Sie zur Registerkarte Berechtigungen .

   ![](assets/microsoft_azure_ALMTeamsNonProdApp.jpg)
   *Registerkarte &quot;Berechtigungen&quot; anzeigen*

1. Wählen Sie auf der Registerkarte Berechtigungen &#39; **[!UICONTROL Administratorzustimmung für MSFT erteilen]**&#39;, um ALM-Teams-App-Berechtigungen zu erteilen.

   ![](assets/microsoft_azure_ALMTeamsNonProdApp_permissions.jpg)
   *Berechtigungen auswählen*

1. Auswählen **[!UICONTROL Akzeptieren]**.

   ![](assets/microsoft_azure_ALMTeamsNonProdApp_permission_request.jpg)
   *&quot;Akzeptieren&quot; auswählen*

1. Nach der Erteilung erhalten die Teilnehmer über diese Berechtigungen die ALM-App, sodass sie sich im Hintergrund anmelden und Benachrichtigungen an die Teilnehmer in der MS Teams-App senden können.

   ![](assets/microsoft_azure_ALMTeamsNonProdApp_permission_request_granted.jpg)
   *Zugriff wird gewährt*

## Der MS Teams-Administrator erstellt eine Richtlinie für die Teams-App

Führen Sie die folgenden Schritte aus:

1. Als MS Teams-Administrator erstellen Sie im Admin Center eine Richtlinie zum Hinzufügen der Teams-App zur Teams-App Ihrer Teilnehmer.

   ![](assets/microsoft_teams_admin_center.png)
   *Erstellen einer Richtlinie*

1. Navigieren Sie zum Abschnitt Setup-Richtlinien. Erstellen Sie eine globale Richtlinie und wählen Sie **[!UICONTROL Applikationen hinzufügen]** im Unterabschnitt Angeheftete Anwendungen .

   ![](assets/microsoft_teams_admin_center_add_installed_apps.png)
   *Richtlinie hinzufügen*

1. Suchen Sie im folgenden Dialogfeld nach **[!UICONTROL Adobe Learning Manager]** und fügen Sie die App hinzu. Dadurch wird der Adobe-Lernmanager im Abschnitt &quot;Installierte Apps&quot; hinzugefügt.

   ![](assets/microsoft_teams_admin_center_installed_apps.png)
   *Applikation installieren*

1. Speichern Sie diese Richtlinie. Dadurch ist die App für alle in der Organisation verfügbar.

Alternativ können Administratoren eine benutzerdefinierte Richtlinie anstelle einer globalen Richtlinie erstellen. Fügen Sie den Adobe-Lernmanager dieser benutzerdefinierten Richtlinie hinzu und wenden Sie die benutzerdefinierte Richtlinie dann nur auf die Benutzergruppen an, die auf den Adobe-Lernmanager zugreifen müssen.

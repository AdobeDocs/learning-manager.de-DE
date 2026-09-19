---
description: Dieses Dokument hilft Ihnen bei der Konfiguration der SSO-Authentifizierung für die Anmeldung bei Ihrem Learning Manager-Konto.
jcr-language: en_us
title: Anmelden bei Learning Manager über die SSO-Authentifizierung
contentowner: dvenkate
exl-id: ef5ab232-0a87-4f76-8dfd-b2497f360cbe
source-git-commit: 1529039e35d4190864e96826bfbea25dcad17c73
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 68%
---
# Anmelden bei Learning Manager über die SSO-Authentifizierung

Dieses Dokument hilft Ihnen bei der Konfiguration der SSO-Authentifizierung für die Anmeldung bei Ihrem Learning Manager-Konto.

Führen Sie für die Konfiguration der SSO-Authentifizierung folgende Schritte durch:

1. Öffnen Sie **[!UICONTROL Einstellungen]** > **[!UICONTROL Anmeldungs-Methoden.]**

   ![](assets/login-methods.png)

1. Wählen Sie je nach benötigter Option **[!UICONTROL Interne Benutzer]** oder **[!UICONTROL Externe Benutzer]**.
1. Klicken Sie auf das Dropdownmenü neben der Option **[!UICONTROL Anmeldung]** und wählen Sie **[!UICONTROL Single Sign-On]** aus.

   ![](assets/single-sign-on.png)

1. Um die Einstellungen für Single Sign-On (SSO) anzupassen, klicken Sie auf **[!UICONTROL Ändern.]**

   ![](assets/change.png)

1. Geben Sie die von Ihrem Dienstanbieter angegebene **[!UICONTROL IDP-initiierte Authentifizierungs-URL]** ein und laden Sie Ihre XML-Datei hoch, indem Sie auf **[!UICONTROL IDP-Metadaten-XML-Datei]** klicken.

   ![](assets/sso-configuration.png)

   Die SSO, die Sie in Learning Manager konfigurieren, muss SAML 2.0 unterstützen.

   Jetzt können Sie sich über die SSO-Authentifizierung bei Learning Manager anmelden.

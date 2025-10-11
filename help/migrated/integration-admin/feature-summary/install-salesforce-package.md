---
jcr-language: en_us
title: Installieren des Salesforce-Pakets
description: Learning Manager bietet ein Salesforce-App-Paket. Nach der Installation und Konfiguration in SFDC können Vertriebsmitarbeiter ihre Schulungen im SFDC-Portal durchführen. Mit dieser App können SFDC-Benutzer neue Schulungen durchsuchen, Empfehlungen anzeigen und diese direkt im SFDC-Portal nutzen. Benutzer erhalten auch die Ankündigungen, die von Administratoren in Form von Mastertiteln direkt in der App im SFDC-Portal gesendet werden.
contentowner: saghosh
exl-id: 2b1c32e7-81af-4c13-a2bd-66684cde084e
source-git-commit: 5d50bd56b6663b26fc6db0ff33d19ad809e9bf6a
workflow-type: tm+mt
source-wordcount: '1053'
ht-degree: 47%

---

# Installieren des Salesforce-Pakets

## Überblick

Learning Manager bietet ein Salesforce-App-Paket. Nach der Installation und Konfiguration in SFDC können Vertriebsmitarbeiter ihre Schulungen im SFDC-Portal durchführen. Mit dieser App können SFDC-Benutzer neue Schulungen durchsuchen, Empfehlungen anzeigen und diese direkt im SFDC-Portal nutzen. Benutzer erhalten auch die Ankündigungen, die von Administratoren in Form von Mastertiteln direkt in der App im SFDC-Portal gesendet werden.

### Einrichten in der Learning Manager-App

1. Melden Sie sich bei Ihrem Learning Manager-Admin-Konto als Integrationsadministrator an.
1. Klicken Sie auf **[!UICONTROL Anwendungen]** > **[!UICONTROL Empfohlene Apps]**.
1. Klicken Sie auf **[!UICONTROL Salesforce]**.
1. Beachten Sie auf der Salesforce-App-Seite die Anwendungs-ID (auch als Client-ID bezeichnet) und das in der Beschreibung erwähnte Client-Secret.
1. Klicken Sie auf **[!UICONTROL Genehmigen]**, und Ihre App muss erfolgreich genehmigt werden.
1. Klicken Sie auf **[!UICONTROL Entwicklerressourcen]** > **[!UICONTROL Zugriffstoken für Tests und Entwicklung]**.
1. Im Abschnitt &quot;Abrufen des OAuth-Codes&quot; müssen die Client-ID und der Umfang auf &quot;admin:read,admin:write&quot; festgelegt werden. Klicken Sie auf **[!UICONTROL Senden]**.
1. Geben Sie in „Aktualisierungstoken abrufen&quot; die Client-ID und das Client-Secret ein. Klicken Sie auf **[!UICONTROL Senden]** und notieren Sie das Aktualisierungstoken.

### Erstellen eines Kontos in der Salesforce-App

1. Erstellen Sie ein Konto auf der Salesforce-Anmeldeseite. Sie müssen ein Salesforce-Konto in der Entwickler- oder Unternehmensversion erstellen.  [Entwickler-Anmelde-URL](https://developer.salesforce.com/signup). Stellen Sie sicher, dass Sie für die Anmeldung bei Salesforce die E-Mail-ID verwenden, die Sie für Learning Manager verwendet haben.
1. Bestätigen Sie Ihr Konto über die Bestätigungs-E-Mail.
1. Erstellen Sie ein Kennwort und melden Sie sich bei Salesforce an.
1. Notieren Sie sich die Salesforce-URL nach der Anmeldung (z. B. site.lightning.force.com).

### Installieren des Learning Manager-Pakets

Wenn Sie das Paket installieren möchten, müssen Sie zunächst das vorhandene Paket in Salesforce löschen. Vor der Deinstallation müssen Sie die Einstellungen aktivieren, wie unten dargestellt. Das Anwenden dieser Einstellungen ist obligatorisch, da Sie das Paket sonst nicht installieren können.

![](assets/uninstall-package.png)

*Installieren des Learning Manager-Pakets*

>[!NOTE]
>
>Die Adobe Learning Manager-App wird nur in der Salesforce-Lightning-Ansicht unterstützt.

1. Starten Sie die [Lern-Manager-Paket-URL &#x200B;](https://test.salesforce.com/packaging/installPackage.apexp?p0=04tDb000000FvU2).
1. Klicken Sie auf der Seite **Anmeldung** auf **[!UICONTROL Benutzerdefinierte Domäne verwenden]**.
1. Geben Sie die Paket-URL ein und klicken Sie auf **[!UICONTROL Weiter]**. Auf der Installationsseite muss die Option Nur für Administratoren installieren ausgewählt sein. Ändern Sie diese Option nicht.
1. Klicken Sie auf **[!UICONTROL Installieren]**. Klicken Sie nach der Installation des Pakets auf **[!UICONTROL Fertig]**. Sie werden zur Seite „Installierte Pakete“ geleitet, auf der das installierte Adobe Learning Manager-Paket angezeigt wird.

1. Navigieren Sie zum App Launcher (neben „Einrichtung“) und suchen Sie Adobe Learning Manager.
1. Klicken Sie zum Konfigurieren der App auf **[!UICONTROL Konfigurieren]**.
1. Klicken Sie auf **[!UICONTROL Neu]** und fügen Sie die folgenden Details hinzu:

   * **Konfigurieren:** Geben Sie den gewünschten Namen ein.
   * **ClientID**: Geben Sie den Wert aus dem ersten Abschnitt ein.
   * **ClientSecret:** Geben Sie den Wert aus dem ersten Abschnitt ein.
   * **RefreshToken:** Geben Sie den Wert aus dem ersten Abschnitt ein.
   * **LearningManagerBaseURL:** Die URL der Site, auf der Learning Manager gehostet wird.
   * **Umleitung deaktivieren:** Deaktivieren Sie die Umleitung zur Teilnehmer-Startseite in Learning Manager.

>[!NOTE]
>
>Sie können nur eine einzelne Konfiguration erstellen. Wenn Sie versuchen, eine weitere Konfiguration hinzuzufügen, wird eine Fehlermeldung angezeigt. Die Konfiguration ordnet das Salesforce-Konto dem Teilnehmerkonto zu.

### Hinzufügen von Remotesite-Einstellungen

1. Klicken Sie oben rechts auf der Seite auf **[!UICONTROL Setup]**.
1. Suchen Sie in **Schnellsuche** nach Remotesite-Einstellungen.
1. Klicken Sie auf **[!UICONTROL Neue Remotesite]**.
1. Geben Sie die folgenden Details ein:

   1. **Remotesite-Name:** Geben Sie den gewünschten Namen ein.
   1. **Remotesite-URL:** Die URL der Site, auf der Learning Manager gehostet wird.

1. Starten Sie Learning Manager.

### Hinzufügen der Adobe-Domäne zu vertrauenswürdigen Salesforce-URLs

Gehen Sie wie folgt vor, um die Adobe-Domäne vertrauenswürdigen URLs hinzuzufügen:

1. Wechseln Sie in der Salesforce-Konsole zu **[!UICONTROL Setup]** > **[!UICONTROL Schnellsuche]**.
1. Suchen Sie nach **[!UICONTROL Vertrauenswürdige URLs]** und wählen Sie **[!UICONTROL Neue vertrauenswürdige URL]**.
1. Geben Sie im Feld **[!UICONTROL API-Name]** einen Namen ein.
1. Geben Sie im URL-Feld &quot;`*.adobe.com`&quot; ein.
1. Wählen Sie alle Kontrollkästchen in **CSP-Direktiven** aus, und speichern Sie die Änderungen.
1. Bearbeiten Sie das Aktualisierungstoken der Salesforce-App und speichern Sie sie.
1. Starten Sie die Salesforce-App neu.

### Aktivieren von Benachrichtigungen für die Learning Manager-App

1. Klicken Sie in der oberen rechten Ecke auf **Setup**.
1. Suchen Sie nach „Benutzerdefinierte Benachrichtigungen“.
1. Klicken Sie auf **[!UICONTROL Neu]**.
1. Geben Sie die folgenden Details ein:

   1. **Benutzerdefinierter Benachrichtigungsname:** LearningManagerNotification
   1. **API-Name:** LearningManagerNotification

1. Wählen Sie sowohl **Desktop** als auch **Mobil** als unterstützte Kanäle aus.

1. Klicken Sie auf **[!UICONTROL Speichern]**.
1. Um Push-Benachrichtigungen für Mobilgeräte zu aktivieren, führen Sie die folgenden Schritte aus:

   1. Installieren Sie die Salesforce-App für Mobilgeräte auf Ihrem Mobiltelefon.
   1. Melden Sie sich mit Ihren Anmeldedaten bei der App an.
   1. Wechseln Sie zu **Setup** > **Einstellungen für die Benachrichtigungszustellung**.
   1. Fügen Sie Salesforce für iOS und Android hinzu.

### Deinstallieren von Learning Manager aus Salesforce

1. Navigieren Sie in der Salesforce-App zu &quot;Installierte Pakete&quot;.
1. Klicken Sie auf **[!UICONTROL Deinstallieren]**.

## Konfigurieren von Learning Manager für Salesforce-Benutzer

Die Learning Manager-App ist auch für Benutzer verfügbar, die sich in einem beliebigen Salesforce-Konto befinden. Der Salesforce-Administrator kann Benutzer basierend auf den Profilen hinzufügen. Die Salesforce-Profile ähneln denen in Learning Manager. Beispiel: Administrator, Integrationsadministrator, Kursleiter. Der Salesforce-Administrator kann auch ein benutzerdefiniertes Profil erstellen.

### Profil

Als Salesforce-Administrator können Sie die Profile entweder Benutzern zuweisen oder ein benutzerdefiniertes Profil erstellen.

>[!NOTE]
>
>Die Benutzer müssen sowohl in Salesforce als auch in Learning Manager vorhanden sein.

![](assets/create-profile.png)

*Profil einem Teilnehmer zuweisen*

Beim Hinzufügen eines Teilnehmers müssen Sie dem Teilnehmer ein bestimmtes Profil zuweisen. Wechseln Sie dann zu diesem Profil und gewähren Sie den erforderlichen Zugriff.

Damit Teilnehmer die Learning Manager-App anzeigen können, müssen Sie die App für alle Teilnehmer aktivieren.

Als Nächstes müssen Sie die Berechtigung für den Zugriff auf die Learning Manager-App bereitstellen.

![](assets/permission-set.png)

*Berechtigungen für den Zugriff auf die Learning Manager-App hinzufügen*

Wenn Sie das Paket installieren, wird ein neuer Berechtigungssatz erstellt: **Adobe Learning Manager-Benutzer**. Wechseln Sie zum Berechtigungssatz und fügen Sie dann die Benutzer hinzu.

Wählen Sie die Benutzer aus und weisen Sie die Berechtigungen entsprechend zu. Die Teilnehmenden können jetzt auf die Learning Manager-App zugreifen.

Wählen Sie jetzt ein Profil aus, z. B. das Standardprofil eines Benutzers, und klicken Sie auf das Profil. Klicken Sie auf **[!UICONTROL Bearbeiten]** und aktivieren Sie im Abschnitt **Benutzerdefinierte Anwendungseinstellungen** das Kontrollkästchen **Adobe Learning Manager**. Dadurch können Benutzer auf die App zugreifen.

Wählen Sie im Abschnitt **Benutzerdefinierte Registerkarteneinstellungen** in der Dropdownliste **Teilnehmerstartseite** die Option **[!UICONTROL Standard an]**.

Sie müssen die App für alle Profile sichtbar machen.

Klicken Sie auf **[!UICONTROL Speichern]**, und die Teilnehmer, die zu allen Profilen gehören, greifen auf die Learning Manager-App zu.

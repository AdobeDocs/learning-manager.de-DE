---
jcr-language: en_us
title: Installieren des Salesforce-Pakets
description: Learning Manager bietet ein Salesforce-App-Paket. Nach der Installation und Konfiguration in SFDC können Vertriebsmitarbeiter ihre Schulungsaktivitäten im SFDC-Portal durchführen. Mit dieser App können SFDC-Benutzer neue Schulungen durchsuchen, Empfehlungen anzeigen und diese direkt im SFDC-Portal nutzen. Benutzer erhalten auch die Ankündigungen, die von Administratoren in Form von Mastertiteln direkt in der App im SFDC-Portal gesendet werden.
contentowner: saghosh
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 0%

---



# Installieren des Salesforce-Pakets

## Übersicht

Learning Manager bietet ein Salesforce-App-Paket. Nach der Installation und Konfiguration in SFDC können Vertriebsmitarbeiter ihre Schulungsaktivitäten im SFDC-Portal durchführen. Mit dieser App können SFDC-Benutzer neue Schulungen durchsuchen, Empfehlungen anzeigen und diese direkt im SFDC-Portal nutzen. Benutzer erhalten auch die Ankündigungen, die von Administratoren in Form von Mastertiteln direkt in der App im SFDC-Portal gesendet werden.

### Einrichten in der Learning Manager-App

1. Melden Sie sich bei Ihrem Learning Manager-Administratorkonto als Integrationsadministrator an.
1. Klicken **[!UICONTROL Anwendungen]** > **[!UICONTROL Highlights]**.
1. Klicken **[!UICONTROL Salesforce]**.
1. Beachten Sie auf der Salesforce-App-Seite die Anwendungs-ID (auch als Client-ID bezeichnet) und das in der Beschreibung erwähnte Client-Secret.
1. Klicken **[!UICONTROL Genehmigen]** und Ihre App muss erfolgreich genehmigt werden.
1. Klicken **[!UICONTROL Ressourcen für Entwickler]** > **[!UICONTROL Zugriffstoken für Tests und Entwicklung]**.
1. Im Abschnitt &quot;Abrufen des OAuth-Codes&quot; müssen die Client-ID und der Umfang auf &quot;admin:read,admin:write&quot; festgelegt werden. Klicken **[!UICONTROL Senden]**.
1. Geben Sie in &quot;Aktualisierungstoken abrufen&quot; die Client-ID und das Client-Secret ein. Klicken **[!UICONTROL Senden]** und notieren Sie das Aktualisierungstoken.

### Konto in der Salesforce-App erstellen

1. Erstellen Sie ein Konto auf der Salesforce-Anmeldeseite. Sie müssen ein Salesforce-Konto in der Entwickler- oder Unternehmensversion erstellen.  [Entwickler-Anmelde-URL](https://developer.salesforce.com/signup). Stellen Sie sicher, dass Sie für die Anmeldung bei Salesforce die E-Mail-ID verwenden, die Sie für Learning Manager verwendet haben.
1. Bestätigen Sie Ihr Konto über die Bestätigungs-E-Mail.
1. Erstellen Sie ein Kennwort und melden Sie sich bei Salesforce an.
1. Notieren Sie sich die Salesforce-URL nach der Anmeldung (z. B. site.lightning.force.com).

### Installieren des Lern-Manager-Pakets

Wenn Sie das Paket installieren möchten, müssen Sie zuerst das vorhandene Paket in Salesforce löschen. Vor der Deinstallation müssen Sie die Einstellungen aktivieren, wie unten gezeigt. Das Anwenden dieser Einstellungen ist obligatorisch, da Sie das Paket sonst nicht installieren können.

![](assets/uninstall-package.png)

*Installieren des Learning Manager-Pakets*

>[!NOTE]
>
>Die Adobe Learning Manager-App wird nur in der Salesforce-Lightning-Ansicht unterstützt.

1. Starten Sie die  [Lern-Manager-Paket-URL](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Ftest.salesforce.com%2Fpackaging%2FinstallPackage.apexp%3Fp0%3D04t1k0000008YWn&amp;data=04%7C01%7Ckillamse%40adobe.com%7Cf588f553fc694d2edee108d9a5c74711%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C637723097572585825%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=mhYKVdwvS4F7WPruy0Kvw%2FsqgWxzTQpaZJyEACu8CNw%3D&amp;reserved=0).
1. Im Dialogfeld &quot; **Anmelden** klicken Sie auf **[!UICONTROL Benutzerdefinierte Domäne verwenden]**.

1. Geben Sie die Paket-URL ein und klicken Sie auf **[!UICONTROL Weiter]**. Auf der Installationsseite muss die Option Nur für Administratoren installieren ausgewählt sein. Ändern Sie diese Option nicht.
1. Klicken **Insgroß**. Nachdem das Paket installiert wurde, klicken Sie auf **[!UICONTROL Fertig]**. Sie werden zur Seite &quot;Installierte Pakete&quot; geleitet, auf der das installierte Adobe Learning Manager-Paket angezeigt wird.

1. Navigieren Sie zum App Launcher (neben &quot;Einrichtung&quot;) und suchen Sie nach Adobe Learning Manager.
1. Um die App zu konfigurieren, klicken Sie auf **[!UICONTROL Konfigurieren]**.
1. Klicken **[!UICONTROL Neu]** und fügen Sie die folgenden Details hinzu:

   * **Konfiguration:** Geben Sie den gewünschten Namen ein.
   * **ClientID**: Geben Sie den Wert aus dem ersten Abschnitt ein.
   * **ClientSecret:** Geben Sie den Wert aus dem ersten Abschnitt ein.
   * **Token aktualisieren:** Geben Sie den Wert aus dem ersten Abschnitt ein.
   * **LearningManagerBaseURL:** Die URL der Site, auf der der Learning Manager gehostet wird.
   * **Umleitung deaktivieren:** Deaktivieren Sie die Umleitung zur Teilnehmer-Startseite im Lern-Manager.

>[!NOTE]
>
>Sie können nur eine einzelne Konfiguration erstellen. Wenn Sie versuchen, eine weitere Konfiguration hinzuzufügen, wird eine Fehlermeldung angezeigt. Die Konfiguration ordnet das Salesforce-Konto dem Teilnehmerkonto zu.

### Remotesite-Einstellungen hinzufügen

1. Klicken Sie oben rechts auf der Seite auf **[!UICONTROL Einrichten]**.
1. In **Schnellsuche** nach Remotesite-Einstellungen.
1. Klicken **[!UICONTROL Neue Remotesite]**.
1. Geben Sie die Details ein:

   1. **Remotesite-Name:** Geben Sie den gewünschten Namen ein.
   1. **Remotesite-URL:** Die URL der Site, auf der der Learning Manager gehostet wird.

1. Starten Sie den Lernmanager.

### Benachrichtigungen für die Learning Manager-App aktivieren

1. Klicken Sie in der oberen rechten Ecke auf **Einrichten**.
1. Suchen Sie nach &quot;Benutzerdefinierte Benachrichtigungen&quot;.
1. Klicken **[!UICONTROL Neu]**.
1. Geben Sie die folgenden Details ein:

   1. **Name der benutzerdefinierten Benachrichtigung:** LearningManagerNotification
   1. **API-Name:** LearningManagerNotification

1. Beide auswählen **Desktop** und **Mobil** als unterstützte Kanäle aus.

1. Klicken **[!UICONTROL Speichern]**.
1. Führen Sie die folgenden Schritte aus, um Push-Benachrichtigungen für mobile Geräte zu aktivieren:

   1. Installieren Sie die Salesforce-App für Mobilgeräte auf Ihrem Mobiltelefon.
   1. Melden Sie sich mit Ihren Anmeldeinformationen bei der App an.
   1. Wechseln zu **Einrichten** > **Einstellungen für die Benachrichtigungszustellung**.
   1. Salesforce für iOS und Android hinzufügen

### Deinstallieren von Learning Manager aus Salesforce

1. Navigieren Sie in der Salesforce-App zu &quot;Installierte Pakete&quot;.
1. Klicken **[!UICONTROL Deinstallieren]**.

## Learning Manager für Salesforce-Benutzer konfigurieren

Die Learning Manager-App steht auch Benutzern zur Verfügung, die in einem beliebigen Salesforce-Konto vorhanden sind. Der Salesforce-Administrator kann Benutzer basierend auf den Profilen hinzufügen. Die Salesforce-Profile ähneln denen im Learning Manager. Beispiel: Administrator, Integrationsadministrator, Kursleiter usw. Der Salesforce-Administrator kann auch ein benutzerdefiniertes Profil erstellen.

### Profil

Als Salesforce-Administrator können Sie die Profile entweder Benutzern zuweisen oder ein benutzerdefiniertes Profil erstellen.

>[!NOTE]
>
>Die Benutzer müssen sowohl in Salesforce als auch in Learning Manager vorhanden sein.

![](assets/create-profile.png)

*Zuweisen eines Profils zu einem Teilnehmer*

Beim Hinzufügen eines Teilnehmers müssen Sie dem Teilnehmer ein bestimmtes Profil zuweisen. Wechseln Sie dann zu diesem Profil und gewähren Sie den erforderlichen Zugriff.

Damit Teilnehmer die Learning Manager-App anzeigen können, müssen Sie die App für alle Teilnehmer aktivieren.

Der nächste Schritt besteht darin, die Berechtigung für den Zugriff auf die Learning Manager-App bereitzustellen.

![](assets/permission-set.png)

*Berechtigungen für den Zugriff auf die Learning Manager-App hinzufügen*

Wenn Sie das Paket installieren, wird ein neuer Berechtigungssatz erstellt. **Adobe Learning Manager-Benutzer**. Wechseln Sie zum Berechtigungssatz und fügen Sie dann die Benutzer hinzu.

Wählen Sie die Benutzer aus und weisen Sie die Berechtigungen entsprechend zu. Die Teilnehmer können jetzt auf die Learning Manager-App zugreifen.

Wählen Sie nun ein Profil aus, z. B. Standardprofil eines Benutzers, und klicken Sie auf das Profil. Klicken **[!UICONTROL Bearbeiten]** und in der &quot; **Benutzerdefinierte App-Einstellungen** das Kontrollkästchen **Adobe Learning Manager**. Dadurch wird die App für den Benutzer zugänglich.

Im Dialogfeld &quot; **Benutzerdefinierte Registerkarteneinstellungen** &quot; im Dialogfeld &quot; **Startseite für Teilnehmer** die Option **[!UICONTROL Standard Ein]**.

Sie müssen die App für alle Profile sichtbar machen.

Klicken **[!UICONTROL Speichern]** und die Teilnehmer, die zu allen Profilen gehören, greifen auf die Learning Manager-App zu.

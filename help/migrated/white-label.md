---
jcr-language: en_us
title: White Labels in der mobilen Adobe Learning Manager-App
description: White Labels sind eine Praxis, bei der Sie eine App oder einen Service mit Ihrem eigenen Branding umbenennen und so anpassen, als wären Sie der ursprüngliche Ersteller. In Adobe Learning Manager kannst du die Mobile App mit einer weißen Beschriftung versehen, sodass du ein Rebranding der App vornehmen und die App deinen Benutzern unter deinem eigenen Branding zur Verfügung stellen kannst.
contentowner: saghosh
exl-id: f37c86e6-d4e3-4095-9e9d-7a5cd0d45e43
source-git-commit: f146b3b9c278f1ac05ecaf741c6617f31982e3ac
workflow-type: tm+mt
source-wordcount: '1625'
ht-degree: 0%

---

# White Labels in der mobilen Adobe Learning Manager-App

Die mobile Adobe Learning Manager-App unterstützt jetzt die weiße Beschriftung, d. h., Sie können die App jetzt unter Ihrem eigenen Branding veröffentlichen.

## Wie Sie mit der Vorbereitung auf den Start Ihrer App mit weißem Etikett beginnen sollten

Führen Sie die folgenden Schritte aus, um Ihre eigene App mit weißem Etikett bereitzustellen und zu verwalten:

1. Bereiten Sie die Elemente (z. B. ein Startbildschirmbild) und den Text so vor, dass beide in der App und in der Beschreibung im App-/Play-Store verwendet werden können.

1. Weisen Sie eine technische Ressource zu, die Folgendes kann:

   * Push-Benachrichtigungszertifikatdateien werden generiert.
   * Signieren der vom ALM-Team bereitgestellten Anwendungsbinärdateien.
   * Hochladen und Verwalten des Veröffentlichungsprozesses. Der Veröffentlichungsprozess erfordert die Kommunikation zwischen Ihrem App-Manager und den Teams im App/Play Store, sodass Ihre App alle Veröffentlichungsrichtlinien erfüllt. Von ALM erhalten Sie eine vollständig kompatible App-Binärdatei.

## Übersicht

White Labels sind eine Praxis, bei der Sie eine App oder einen Service mit Ihrem eigenen Branding umbenennen und so anpassen, als wären Sie der ursprüngliche Ersteller. In Adobe Learning Manager kannst du die Mobile App mit einer weißen Beschriftung versehen, sodass du ein Rebranding der App vornehmen und die App deinen Benutzern unter deinem eigenen Branding zur Verfügung stellen kannst.

## Was kann angepasst werden

Folgende Elemente können angepasst werden:

### Felder

<table>

 <tbody>

  <tr>

   <td>

    <p>Konto-ID</p>

   </td>

   <td>

    <p>Die ID Ihres Kontos. Beachten Sie, dass Teilnehmer, die zu einem anderen Konto gehören, nicht auf die App mit weißer Beschriftung zugreifen können.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Zusätzliche Konto-IDs</p>

   </td>

   <td>

    <p>Fügen Sie bei Bedarf mehrere Konten (Unterdomänen) hinzu. Fügen Sie die Unterdomänen durch Kommas getrennt ohne Leerzeichen hinzu. Beispiel: acc01, acc02, acc03 usw.<br> <b>Hinweis:</b> Sie müssen die Konto-ID hinzufügen, wenn Sie die Unterdomänen angeben.</br> </p>

   </td>

  </tr>

  <tr>

   <td>

    <p>App-Name</p></td>

   <td>

    <p>Der Name, den Sie für die App verwenden möchten.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>App-Kurzname</p>

   </td>

   <td>

    <p>Wenn der Name der App lang ist, geben Sie der App einen kurzen Namen, der auf dem Gerät angezeigt wird.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Name der internen App</p></td>

   <td>

    <p>Der Name, mit dem das Betriebssystem die App identifiziert. Üblicherweise wird das Format com.company-name.product-name verwendet.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Name der internen App - iOS</p>

   </td>

   <td>

    <p>Benennen Sie die App anders, wenn sich Ihre Benutzer in iOS befinden. Es wird empfohlen, für iOS und Android denselben Namen zu verwenden.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>App-Symbol</p>

   </td>

   <td>

    <p>Das App-Symbol als png. Dieses Symbol wird in Ihrer App angezeigt. Das zu benennende Format ist account-id_appIcon.png. Die Abmessungen des App-Symbols sind 512 × 512 Pixel.<div>Bitte beachten Sie, dass Apple keinen Alpha-Kanal in App-Symbolen zulässt. Stellen Sie daher sicher, dass Sie den Alpha-Kanal aus dem Asset entfernen, bevor Sie es senden.</div></p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Startbildschirm der App</p></td>

   <td>

    <p>Geben Sie für den Begrüßungsbildschirm Ihrer App ein Bild (png) an, das angezeigt wird, wenn die Benutzer die App starten. Das zu benennende Format ist account-id_splashIcon.png. Die Abmessungen der quadratischen Splashscreens betragen 1052 × 1052 Pixel und der kreisförmigen Splashscreens 768 x 768 Pixel.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Client-ID und geheimer Clientschlüssel</p>

   </td>

   <td>

    <p>Der Integrations-Admin Ihres Kontos stellt die Details bereit, während Sie die App registrieren. Der Integrationsadministrator muss Folgendes verwenden:<ul><li>Teilnehmer:lesen,Teilnehmer:als Rolle schreiben</li><li>Interne App name://redirect als Umleitungs-URL</li></ul></p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Kontenlogo</p>

   </td>

   <td>

    <p>Die URL, über die das Logo Ihres Unternehmens gehostet wird. Geben Sie einen cpcontents-Link als Logo für das Konto an. Die URL muss webcodiert sein.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>App Store-ID für die App (iOS)</p>

   </td>

   <td>

    <p>Die für die Implementierung der Force-Aktualisierung erforderliche ID. Die App muss wissen, dass der Teilnehmer zum App Store weitergeleitet werden sollte, um die App zu aktualisieren.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Google Play Store-ID für die App (Android)</p>

   </td>

   <td>

    <p>Die für die Implementierung der Force-Aktualisierung erforderliche ID.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Hostname für Deep-Linking</p>

   </td>

   <td>

    <p>Um Ihre Deep Links zu hosten, verwenden Sie den Learning Manager. Wenn Sie eine andere URL für den Hostnamen als Deep-Link verwenden möchten, geben Sie die URL des Hosts an. Beispiel: learningmanager.adobe.com.</p>

   </td>

  </tr>

 </tbody>

</table>

>[!NOTE]
>
>Geben Sie die Daten an Ihre CSAMs weiter, damit sie sie in Ihre benutzerdefinierte App-Binärdatei einfügen können.


#### Sitezuordnung zur Verarbeitung benutzerdefinierter Deplinks aktualisieren

Wenn Sie eine benutzerdefinierte Domäne oder einen Learning Manager\*.adobe.com als Veranstalter verwenden, müssen Sie nichts unternehmen. Wenn Sie jedoch eine benutzerdefinierte Lösung oder einen bestimmten Hostnamen für die URLs verwenden, fügen Sie die Site-Zuordnungsdateien hinzu.

>[!CAUTION]
>
>Wenn die Dateien nicht vorhanden sind, funktionieren die Deeplinks nicht. Stellen Sie sicher, dass die Dateien vorhanden sind.


Weitere Informationen finden Sie unter den folgenden Links:

* [Android](https://learningmanager.adobe.com/.well-known/assetlinks.json)
* [iOS](https://learningmanager.adobe.com/.well-known/apple-app-site-association)

## Push-Benachrichtigungen generieren

Das Senden von Push-Benachrichtigungen an Android- und iOS-Apps erfordert zwei verschiedene Mechanismen.

* Generieren Sie für iOS die Push-Benachrichtigungszertifikate.
* Geben Sie für Android einen aus dem Firebase-Projekt generierten Serverschlüssel an.

Befolgen Sie die folgenden Anweisungen, um die Projekte in Firebase einzurichten:

### Push-Benachrichtigungen in iOS

Bei der Entwicklung von iOS-Anwendungen ist ein Push-Benachrichtigungszertifikat ein von Apple ausgestelltes kryptografisches Anmeldezertifikat, mit dem ein Server Push-Benachrichtigungen über die Push-Benachrichtigungsdienste (APNs) von Apple sicher an ein iOS-Gerät senden kann.

Das Zertifikat stellt eine sichere Kommunikation zwischen Ihrem Server (oder Anbieter) und den APNs von Apple sicher, wenn Push-Benachrichtigungen an iOS-Geräte gesendet werden.

Sowohl Android als auch iOS verwenden Firebase Cloud Messaging (FCM) als Dienst für das Senden von Push-Benachrichtigungen an Geräte.

### So generieren Sie das Zertifikat in iOS

Gehen Sie folgendermaßen vor:

1. Generieren oder laden Sie das **Push-Benachrichtigungszertifikat** und den privaten Schlüssel (.p12) herunter. Weitere Informationen finden Sie im [Apple-Entwicklerdokument](https://developer.apple.com/documentation/usernotifications/setting_up_a_remote_notification_server/establishing_a_certificate-based_connection_to_apns).

1. Installieren Sie die p12-Datei, nachdem die Datei heruntergeladen wurde. Verwenden Sie das Kennwort, um in Ihrem **Schlüsselbundzugriff** zu installieren.

1. Navigieren Sie zu **Meine Zertifikate** und exportieren Sie das Zertifikat. Stellen Sie sicher, dass Sie den MIME-Typ &quot;.cer&quot; auswählen.

1. Sobald Sie die p12-Datei und die cer-Datei verfügbar haben, führen Sie die folgenden Befehle aus:

```
- openssl pkcs12 -in privatekey.p12 -out myapnappkey.pem -nodes –clcerts

- openssl x509 -in privatekey.cer -inform DER -out myapnsappcert.pem 

- openssl s_client -connect gateway.sandbox.push.apple.com:2195 -cert myapnsappcert.pem -key myapnappkey.pem 
```

Wenn Sie eine Verbindung zum Server herstellen können, ist das von Ihnen erstellte Zertifikat gültig. Kopieren Sie aus der Datei myapnappkey.pem die Werte für das Zertifikat und den privaten Schlüssel.

### Push-Benachrichtigungen unter Android

Für Android muss der Benutzer die Datei services.json aus dem Firebase-Projekt bereitstellen, um den Eintrag zum SNS-Dienst hinzuzufügen.

Erstellen Sie ein Projekt in Firebase und geben Sie die Datei services.json für das CSM-Team frei. Diese Datei wird für den tokenbasierten Eintrag im SNS benötigt. Beachten Sie, dass der Serverschlüssel nicht mehr verwendet wird. Siehe [Projekt in Firebase erstellen](#create-project-in-firebase).

Führen Sie die folgenden Schritte aus, um die Datei services.json herunterzuladen:

1. Melden Sie sich bei der **Firebase**-Konsole an.
1. Wechseln Sie zu **Projekteinstellungen** und wählen Sie **Cloud Messaging** aus.
1. Suchen Sie **Firebase Cloud Messaging API** und wählen Sie **Dienstkonten verwalten** aus.
1. Wählen Sie auf der Seite **Dienstkonten** die **Dienstkonten** im linken Bereich aus.
1. Suchen Sie Ihren Projekteintrag und wählen Sie unter &quot;Aktionen&quot; **Details verwalten** aus.

   >[!NOTE]
   >
   >   Das Projekteintragsformat lautet &lt;-accountname->@appspot.gserviceaccount.com.

1. Wechseln Sie zur Registerkarte **Schlüssel** und wählen Sie **Schlüssel hinzufügen** aus.
1. Wenn kein Schlüssel vorhanden ist, wählen Sie **Neuen Schlüssel erstellen** und anschließend **JSON** als Schlüsseltyp aus. Dadurch wird die JSON-Datei generiert und heruntergeladen.
1. Wenn bereits ein Schlüssel vorhanden ist, wählen Sie **Vorhandenen Schlüssel hochladen**, fügen Sie den Schlüssel ein und laden Sie ihn hoch. Dadurch wird die JSON-Datei generiert und heruntergeladen.

<!-- Set up a project in Firebase and share the server key with the CSAM.-->

Wenden Sie sich an das CSM-Team und geben Sie die JSON-Datei frei, um den Eintrag den SNS-Diensten in AWS hinzuzufügen. Benutzer müssen den Eintrag für die Push-Benachrichtigung im SNS-Dienst registrieren lassen, sodass sie die oben generierten Zertifikate für die Validierung freigeben müssen.

## Erstellen eines Projekts in Firebase {#create-project-in-firebase}

### Android

Verwenden Sie dasselbe Projekt, das Sie in den Schritten oben erstellt haben, für Push-Benachrichtigungen erneut.

[Fügen Sie das Projekt ](https://learn.microsoft.com/en-us/xamarin/android/data-cloud/google-messaging/firebase-cloud-messaging) in Firebase hinzu, und rufen Sie die Datei ***google-services.json*** ab.

### iOS

[Fügen Sie das Projekt ](https://firebase.google.com/docs/ios/setup) zu Firebase hinzu, und rufen Sie die Datei ***GoogleService-Info.plist*** ab.

>[!IMPORTANT]
>
>Senden Sie die Dateien an das Adobe Learning Manager CSAM-Team, damit sie in den Build der Binärdatei Ihrer App aufgenommen werden.


## Signierte Binärdateien generieren

### iOS

<!--```
sh""" xcodebuild -exportArchive -archivePath Runner.xcarchive -exportPath "ipa_path/" -exportOptionsPlist {ExportFile} 

mv ipa_path/*.ipa "${env.AppName}_signed.ipa" """ 
```-->

Der Ordner `<root>` enthält die Datei **Runner.xcarchive.zip**. Führen Sie die folgenden Befehle aus, um die signierte Binärdatei zu generieren:

1. Führen Sie den folgenden Befehl aus, um das Archiv zu entpacken:

   ```
   unzip Runner.xcarchive.zip
   ```

2. Navigieren Sie zum App-Verzeichnis:

   ```
   cd Runner.xcarchive/Products/Applications/Runner.app
   ```

3. Kopieren Sie die mobile Bereitstellungsdatei:

   ```
   cp <path>/<mobile-provisioningfile>.mobileprovision embedded.mobileprovision
   ```

4. Kehren Sie zum Ordner &quot;`<root>`&quot; zurück (in dem sich Runner.xcarchive.zip befindet):

   ```
   cd <root>
   ```

5. Exportieren Sie das Archiv mit xcodebuild:

   ```
   xcodebuild -exportArchive -archivePath Runner.xcarchive -exportPath ipa_path/ -exportOptionsPlist <path>/<ExportOptions-file>.plist
   ```

6. Suchen Sie die .ipa-Datei im Ordner ipa_path.
7. Laden Sie die .ipa-Datei auf die Diawi-Website hoch.
8. Wählen Sie nach dem vollständigen Hochladen die Schaltfläche **[!UICONTROL Senden]** aus.
9. Nach der Fertigstellung erhalten Sie einen QR-Code und einen Link.
10. Öffnen Sie den QR-Code oder verknüpfen Sie ihn direkt in Safari.

Wenn das Gerät im Bereitstellungsprofil enthalten ist, sollte die Installation auf dem Gerät fortgesetzt werden.

>[!NOTE]
>
>Sie benötigen XCode 15.2 oder höher, um die signierten Binärdateien zu erstellen.


### Android

**Für APK-Datei**

```
sh""" <path>/apksigner sign --ks $storeFile --ks-pass "pass:$store_password" --ks-key-alias $key_alias --key-pass "pass:$key_password" --out app-release-signed.apk -v app-release.apk """
```

**Für eine ABB-Datei**

>[!NOTE]
>
>Zum Erstellen der signierten Binärdateien benötigen Sie die SDK-Build-Tools von Android.

Der Play Store erfordert für die Veröffentlichung Android-Binärdateien im arabischen Format. Daher stellen wir die nicht signierte .aab-Datei zur Verfügung.

>[!NOTE]
>
>Beim Erstellen einer KeyStore-Datei müssen Sie ein KeyStore-Kennwort, einen Signaturschlüssel-Alias und ein Signaturschlüssel-Alias-Kennwort generieren.

Führen Sie die folgenden Schritte aus, um die .aab-Datei zu signieren:

Führen Sie den folgenden Befehl aus:

```
<path>/jarsigner -verbose -sigalg SHA256withRSA -digestalg SHA-256 -keystore <keystore-file> app-release.aab <signingKeyAlias>
```

>[!NOTE]
>
>Der **[!UICONTROL jarsigner]** ist in Java enthalten. Stellen Sie sicher, dass Sie Java 21 verwenden.

Wenn Sie dazu aufgefordert werden, geben Sie die folgenden Kennwörter ein:

* Keystore-Kennwort
* Kennwort für Signaturschlüsselalias

Sie können die bereitgestellte App verwenden. Wenn Sie jedoch eine APK aus einer AB-Datei generieren müssen, führen Sie folgende Schritte aus:

>[!NOTE]
>
>Sie müssen **[!UICONTROL bundletool]** installieren, um APKs zu generieren.


Führen Sie den folgenden Befehl aus, um die apk-Datei zu erstellen:

```
java -jar <path>/bundletool-all.jar  build-apks --bundle=app-release.aab --output=my_app.apks --mode=universal
```

Führen Sie den folgenden Befehl aus, um die Datei zu entpacken:

```
unzip my_app.apks -d output_dir
```

Sie erhalten die apk-Datei aus dem Ordner **[!UICONTROL output_dir]**.

**Nächste Schritte**

Übertragen Sie die Binärdateien nach dem Generieren der Binärdateien in den Play Store oder in App Store.

## Wie werden die Änderungen angewendet?

Sendet die erforderlichen Elemente und Dateien an das CSM-Team. Das CSM-Team füllt dann das [Formular](https://forms.office.com/r/bJRRaRBvSh) mit den erforderlichen Änderungen aus und hängt die erforderlichen Assets an. Das Team überprüft dann die Änderungen und informiert die technischen Teams darüber. Das Engineering-Team generiert dann einen Build und gibt diesen an das CSM-Team weiter.

Das CSM-Team gibt die Version für den Kunden frei.

## Was nicht angepasst werden kann

* Bildschirm &quot;Kennwort aktualisieren&quot;
* Seite &quot;Konto erstellen&quot;

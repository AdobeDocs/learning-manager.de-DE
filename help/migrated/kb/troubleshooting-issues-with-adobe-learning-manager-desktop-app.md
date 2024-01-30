---
description: Dieses Dokument enthält grundlegende Tipps zur Fehlerbehebung, um einige häufige Probleme zu lösen, die bei der Installation und Verwendung der Adobe Learning Manager-Desktop-Anwendung auftreten.
jcr-language: en_us
title: Fehlerbehebung für die Adobe Learning Manager-Desktop-App
contentowner: kuppan
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '1447'
ht-degree: 54%

---



# Fehlerbehebung für die Adobe Learning Manager-Desktop-App

Dieses Dokument enthält grundlegende Tipps zur Fehlerbehebung, um einige häufige Probleme zu lösen, die bei der Installation und Verwendung der Adobe Learning Manager-Desktop-Anwendung auftreten.

## Ich habe folgendes Problem {#iamunabletodothefollowing}

+++Ich kann die Adobe Learning Manager-Desktopanwendung nicht herunterladen

1. Überprüfen Sie Ihre Internetverbindung und Firewalleinstellungen.
1. Klicken Sie unter „Social Learning“ auf **[!UICONTROL Neuer Beitrag]**, um einen Beitrag zu erstellen. Wenn Sie kein Board haben, erstellen Sie zuerst ein Board.
1. Klicken Sie auf eine der folgenden angezeigten Posting-Schaltflächen, um Inhalte wie Screenshots, Audioaufnahmen, Videoaufnahmen oder eine Learning Manager-Galerie zu erstellen. Sie werden zur Seite der Adobe Learning Manager-Desktop-Anwendung weitergeleitet, auf der Sie die Anwendung für Ihren Desktop herunterladen können.
1. Sie benötigen ein gültiges Adobe Learning Manager-Konto, für das Social Learning von Ihrem Administrator aktiviert wurde. Ihr Administrator hat möglicherweise auch Downloads über den Webbrowser deaktiviert. Wenden Sie sich an Ihren Adobe Learning Manager-Administrator, um weitere Informationen zum Herunterladen der Desktop-App zu erhalten.

+++

+++Ich kann die Adobe Learning Manager-Desktopanwendung nicht installieren

1. Vergewissern Sie sich, dass das System die Mindestsystemanforderungen erfüllt. Siehe [Systemanforderungen für die Adobe Learning Manager-App für Desktop](../learners/adobe-learning-manager-app-for-desktop/adobe-learning-manager-desktop-app-system-requirements.md).
1. Bereinigen Sie Reste früherer Installationen der Adobe Learning Manager-Desktop-Anwendung. Weitere Informationen finden Sie unter  [So reinigen Sie frühere Installationen](#howtocleanuppreviousinstallationsofadobelearningmanagerdesktopapp) für weitere Informationen.
1. Informationen zu Fehlern während des Installationsvorgangs finden Sie unter [So finden Sie Anwendungsprotokolle](#howtofindapplicationlogs). Wenden Sie sich an Ihren Administrator für die Adobe Learning Manager-Desktop-Anwendung, um weitere Hilfe zu erhalten.

+++

+++Ich kann die Adobe Learning Manager-Desktop-Anwendung nicht starten

1. Stellen Sie sicher, dass die Adobe Learning Manager-Desktop-Anwendung heruntergeladen und installiert wurde.
1. Klicken Sie in „Social Learning“ auf **[!UICONTROL Neuer Beitrag]** (wenn Sie keine Pinnwand haben, erstellen Sie zunächst eine). Klicken Sie auf eine der folgenden Optionen für die Schaltfläche &quot;Beitrag&quot;, die angezeigt werden: Screenshot erstellen, Audioaufnahme, Videoaufnahme, Adobe Learning Manager-Galerie. Sie werden zu einer Seite weitergeleitet, von der Sie die Adobe Learning Manager-Desktop-Anwendung starten können.
1. Falls die App nicht gestartet wird, können Sie sie auch über das Startmenü unter Windows oder über das Launchpad unter Mac OS X starten.

+++

+++Ich kann mich nicht bei meinem Konto in der Adobe Learning Manager-Desktop-Anwendung anmelden

1. Stellen Sie sicher, dass eine Verbindung zum Internet besteht und Ihre Firewall-Einstellungen die Adobe Learning Manager-Desktop-Anwendung nicht blockieren.
1. Stellen Sie sicher, dass Sie über ein gültiges Teilnehmerkonto für Adobe Learning Manager verfügen, für das Social Learning aktiviert ist.
1. Wenn Sie sich noch immer nicht anmelden können, beenden Sie die Adobe Learning Manager-Desktop-Anwendung, starten Sie sie neu und versuchen Sie es erneut.
1. Wenden Sie sich an Ihren Administrator für Adobe Learning Manager, um weitere Hilfe zu erhalten.

+++

+++Meine Webcam/mein Mikrofon wird in der Adobe Learning Manager-Desktopanwendung nicht aufgeführt

1. Stellen Sie sicher, dass Ihre Webcam/Ihr Mikrofon ordnungsgemäß angeschlossen ist und funktioniert.
1. Stellen Sie sicher, dass Sie die neuesten Treiber für Ihre Webcam/Ihr Mikrofon installiert haben. Einige Geräte funktionieren ohne dedizierte Treiber nicht ordnungsgemäß.
1. Setzen Sie die Anwendungsvoreinstellungen zurück und starten Sie die Adobe Learning Manager-Desktop-Anwendung erneut, um es nochmals zu versuchen. Weitere Informationen finden Sie unter [Zurücksetzen der App-Voreinstellungen](#howtoresetapplicationpreferences).
1. Wenn Sie macOS Mojave 10.14 verwenden, erteilen Sie der Adobe Learning Manager-Desktop-Anwendung die Berechtigung zum Zugriff auf Ihre Webcam/Ihr Mikrofon. Weitere Informationen finden Sie unter [Festlegen der Webcam-/Mikrofon-Berechtigungen unter macOS Mojave](#howtosetwebcammicrophonepermissionsonMacOSXMojave).

+++

+++Ich kann meine Beiträge über die Adobe Learning Manager-Desktopanwendung nicht veröffentlichen

1. Stellen Sie sicher, dass Ihnen von Ihrem Adobe Learning Manager-Administrator ein gültiges Teilnehmerkonto für Adobe Learning Manager eingerichtet wurde, für das Social Learning aktiviert ist.
1. Setzen Sie die Anwendungsvoreinstellungen zurück und starten Sie die Adobe Learning Manager-Desktop-Anwendung erneut, um es nochmals zu versuchen. Weitere Informationen finden Sie unter [Zurücksetzen der Anwendungsvoreinstellungen](#howtoresetapplicationpreferences).
1. Aktivieren Sie die erweiterte Protokollierung, wenn beim Veröffentlichen Fehler auftreten. Weitere Informationen finden Sie unter [Aktivieren der erweiterten Protokollierung](#howtoenableadvancedlogging). Starten Sie die Adobe Learning Manager-Desktop-Anwendung neu und wiederholen Sie die obigen Schritte, die den Fehler verursachen. Senden Sie die neuesten Anwendungsprotokolle an Ihren Adobe Manager-Administrator, um Hilfe zu erhalten. Weitere Informationen finden Sie unter [Suchen nach Anwendungsprotokollen](#howtofindapplicationlogs).

+++

+++Ältere Projekte können nicht angezeigt oder geöffnet werden

1. Sie können Projekte, die mit Ihrem Adobe Learning Manager-Konto erstellt wurden, nur auf dem Computer anzeigen, auf dem sie erstellt wurden.
1. Setzen Sie die Anwendungsvoreinstellungen zurück und starten Sie die Adobe Learning Manager-Desktop-Anwendung erneut, um es nochmals zu versuchen. Weitere Hilfe finden Sie unter [Zurücksetzen der Anwendungsvoreinstellungen](#howtoresetapplicationpreferences).
1. Wenn beim Öffnen von Projekten Fehler auftreten, aktivieren Sie die erweiterte Protokollierung. Weitere Informationen finden Sie unter [Erweiterte Protokollierung aktivieren](#howtoenableadvancedlogging). Starten Sie die Adobe Learning Manager-Desktop-Anwendung neu und wiederholen Sie die Schritte, die den Fehler verursachen. Senden Sie die neuesten Anwendungsprotokolle an Ihren Adobe Manager-Administrator, um Hilfe zu erhalten. Weitere Informationen finden Sie unter [Suchen nach Anwendungsprotokollen](#howtofindapplicationlogs).

+++

## Wie kann ich die Anwendungsvoreinstellungen zurücksetzen? {#howtoresetapplicationpreferences}

### Windows {#windows}

1. Um das Dialogfeld Ausführen zu öffnen, drücken Sie die **Windows + R** verwenden.
1. Typ `**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**` und drücken Sie die Eingabetaste.
1. Löschen Sie die Dateien mit dem Namen **preferences.json** und **preferences.xml**.

### Mac OS X {#macosx}

1. Öffnen Sie den Finder.
1. Zum Öffnen des Dialogfelds **Wechseln zu** Ordnerdialog, Drücken Sie **Cmd + Umschalt + G** verwenden.
1. Typ `**~/Library/Application Support/Adobe/Learning Manager 1.0**` und drücken Sie die Eingabetaste.
1. Löschen Sie die Dateien mit dem Namen **preferences.json** und **preferences.xml**.

## Suchen nach Anwendungsprotokollen {#howtofindapplicationlogs}

### Windows {#application-logs}

1. Um das Dialogfeld Ausführen zu öffnen, drücken Sie **Windows + R** verwenden.
1. Typ `**%TEMP%\\elthor**` und drücken Sie die Eingabetaste.
1. Sortieren Sie die Ordner nach **Änderungsdatum** und öffnen Sie den letzten Ordner. Dieser Ordner enthält die neuesten Anwendungsprotokolle.

### Mac OS X {#MacOSX-1}

1. Öffnen **Finder**.
1. Zum Öffnen des Dialogfelds **Gehe zu Ordner** &quot; die Tastenkombination **Cmd + Umschalt + G** verwenden.
1. Geben Sie &quot;**/var/folders**&quot; (ohne Anführungszeichen) und drücken Sie die Eingabetaste.
1. Suchen Sie nach &quot;**Elthor**&quot; in der Suchleiste und öffnen Sie den Ordner.
1. Sortieren Sie die Ordner nach dem **Änderungsdatum** und öffnen Sie den letzten Ordner. Dieser Ordner enthält die neuesten Anwendungsprotokolle.

## Wie aktiviere ich die erweiterte Protokollierung? {#howtoenableadvancedlogging}

### Windows {#Windows-1}

1. Um das Dialogfeld Ausführen zu öffnen, drücken Sie **Windows-Taste + R**.****
1. Geben Sie &quot;**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**&quot; (ohne Anführungszeichen) und drücken Sie die Eingabetaste.****
1. Sicherungskopie der Datei erstellen **preferences.json**, und öffnen Sie sie dann in einem Texteditor.****
1. Nach dem Schlüssel suchen **debugMode** und ändern Sie die value-Eigenschaft dieses Schlüssels in &quot;**korrekt**&quot; (ohne Anführungszeichen).

### Mac OS X {#MacOSX-2}

1. Öffnen Sie den Finder.
1. Zum Öffnen des Dialogfelds **Gehe zu Ordner** Dialog, drücken Sie **Cmd + Umschalt + G**.
1. Geben Sie &quot;**~/Library/Application Support/Adobe/Learning Manager 1.0**&quot; (ohne Anführungszeichen) und drücken Sie die Eingabetaste.
1. Erstellen Sie ein Backup der Datei **preferences.json** und öffnen Sie sie in einem Texteditor.
1. Nach dem Schlüssel suchen **debugMode** und ändern Sie die value-Eigenschaft dieses Schlüssels in &quot;**korrekt**&quot; (ohne Anführungszeichen)

## Wie kann ich Webcam-/Mikrofonberechtigungen für Mac OS X Mojave festlegen? {#howtosetwebcammicrophonepermissionsonmacosxmojave}

1. Klicken **[!UICONTROL Systemeinstellungen]** im Dock.
1. Klicken **[!UICONTROL Sicherheit und Datenschutz.]** > **[!UICONTROL Datenschutz].**
1. Klicken Sie auf die **[!UICONTROL Optionen für Webcam und Mikrofon]** und stellen Sie sicher, dass das Kontrollkästchen für Adobe Learning Manager aktiviert ist. Wenn Adobe Learning Manager nicht aufgeführt ist, müssen Sie zunächst die Adobe Learning Manager-Desktop-Anwendung installieren und starten.

## Bereinigen des Update-Cache von Adobe Learning Manager für Desktop {#howtocleanupadobecaptivateprimefordesktopupdatescache}

### Windows {#clean-previous-installation}

1. Um das Dialogfeld Ausführen zu öffnen, drücken Sie **Windows-Taste + R**.
1. Typ `**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**` und drücken Sie die Eingabetaste.
1. Löschen Sie den Ordner namens **updates**.

### Mac OS X {#MacOSX-3}

1. Öffnen Sie den Finder.
1. Zum Öffnen des Dialogfelds **Gehe zu Ordner** Dialog, drücken Sie **Cmd + Umschalt + G**.
1. Typ `**~/Library/Application Support/Adobe/Learning Manager 1.0**` und drücken Sie die Eingabetaste.
1. Löschen Sie den Ordner namens **updates**.

## Bereinigen des temporären Ordners von Adobe Learning Manager für Desktop {#howtocleanupadobecaptivateprimefordesktoptempfolder}

### Windows {#clean-previous-installation-1}

1. Um das Dialogfeld Ausführen zu öffnen, drücken Sie **Windows-Taste + R**.
1. Geben Sie &quot;**%TEMP%**&quot; (ohne Anführungszeichen) und drücken Sie die Eingabetaste.
1. Löschen Sie den Ordner &quot;**Elthor**&quot;.

### Mac OS X {#MacOSX-4}

1. Öffnen Sie den Finder.
1. Zum Öffnen des Dialogfelds **Gehe zu Ordner** Dialog, drücken Sie **Cmd + Umschalt + G** verwenden.
1. Geben Sie &quot;**/var/folders**&quot; (ohne Anführungszeichen) und drücken Sie die Eingabetaste.
1. Suchen Sie nach &quot;**Elthor**&quot; in der Suchleiste.
1. Löschen Sie den Ordner &quot;**Elthor**&quot;.

## Suchen nach Projekten in Adobe Learning Manager für Desktop {#howtolocateadobecaptivateprimefordesktopprojects}

### Windows {#Windows-2}

1. Um das Dialogfeld Ausführen zu öffnen, drücken Sie **Windows-Taste + R**.
1. Geben Sie &quot;**~/Documents/My Adobe Learning Manager Projects**&quot; (ohne Anführungszeichen) und drücken Sie die Eingabetaste.
1. Möglicherweise haben Sie oder Ihr Adobe Learning Manager-Administrator den Standardordner für Projekte geändert. Wenden Sie sich an Ihren Administrator, um weitere Hilfe zum Suchen und Bereinigen von Projekten zu erhalten.

### Mac OS X {#MacOSX-5}

1. Öffnen Sie den Finder.
1. Zum Öffnen des Dialogfelds **Gehe zu Ordner** Dialog, drücken Sie **Cmd + Umschalt + G** verwenden.
1. Geben Sie &quot;**~/Documents/My Adobe Learning Manager Projects**&quot; (ohne Anführungszeichen) und drücken Sie die Eingabetaste.

   Möglicherweise haben Sie oder Ihr Adobe Learning Manager-Administrator den Standardordner für Projekte geändert. Weitere Unterstützung beim Auffinden und Bereinigen von Projekten erhalten Sie von Ihrem Administrator.

## Bereinigen von Resten früherer Installationen der Adobe Learning Manager-Desktop-App {#howtocleanuppreviousinstallationsofadobelearningmanagerdesktopapp}

### Windows {#Windows-3}

1. Zum Öffnen des Dialogfelds **Dialogfeld &quot;Ausführen&quot;** nötigen **Windows-Tasten + R**.
1. Geben Sie regedit ein und suchen Sie nach &quot;**HKEY_LOCAL_MACHINE \\SOFTWARE\\Classes\\Installer\\**&quot; (ohne Anführungszeichen) oder &quot;**HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Installer\\UserData\\S-1-5-18\\Products\\**&quot; (ohne Anführungszeichen) und drücken Sie die Eingabetaste.
1. Suchen Sie den Ordner namens Adobe Learning Manager und die frühere Installation. Löschen Sie den Registrierungseintrag.  Sie finden die Taste, indem Sie die Taste F3 drücken.

### Mac OS X {#MacOSX-6}

Verschieben Sie die Dateien aus dem folgenden Pfad &quot;**/Programme/Adobe Learning Manager/Users/Shared/Adobe/Learning Manager Assets/1.0**&quot; in den Papierkorb und leeren Sie dann den Papierkorb.

---
jcr-language: en_us
title: Veröffentlichen in der Learning Manager-EU-Domäne nicht möglich
description: Veröffentlichung von Adobe Captivate in der Adobe Learning Manager EU-Domäne in Adobe Learning Manager nicht möglich.
contentowner: nluke
exl-id: fb8ae1af-9902-4901-8263-fb3ebff98fbc
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 83%

---

# Veröffentlichen in der Learning Manager-EU-Domäne nicht möglich {#unable-to-publish-to-learning-manager-eu-domain}

## Problem

Veröffentlichen aus Adobe Captivate in der Adobe Learning Manager-EU-Domäne nicht möglich.

## Fehler

Keine Konten gefunden

## Beschreibung

Es gibt Szenarien, in denen Autoren versuchen, einen Kurs von Adobe Captivate in Adobe Learning Manager zu veröffentlichen. Dies ist jedoch nicht möglich, da die Fehlermeldung „Kein Konto gefunden“ angezeigt wird.

## Ursache

Dieses Problem tritt auf, weil Adobe Captivate standardmäßig für die Veröffentlichung von Inhalten in der US-Domäne von Adobe Learning Manager konfiguriert ist.

## Lösung:

Zu beachtende Punkte:

* Wenn Sie geöffnet ist, schließen Sie die Adobe Captivate-Anwendung.
* Sie benötigen Administratorzugriff auf Ihrem Computer, um die folgenden Schritte auszuführen. Wenn Sie keinen Administratorzugriff haben, wenden Sie sich an Ihr IT-Team, um Hilfe zu erhalten.

Führen Sie die folgenden Schritte aus:

1. Wechseln Sie zum Installationsverzeichnis für Adobe Captivate.

   Beispiel: `kbd C:\\Program Files\\Adobe\\Adobe Captivate 2019 x64` (2019 ist die Captivate-Version. Sie weicht ab, wenn Sie eine andere Version von Adobe Captivate verwenden).

1. Kopieren Sie die Konfigurationsdatei **AdobeCaptivate.ini** auf Ihren Desktop.

   ![](assets/cp-captivate.ini.png)
   *Konfigurationsdatei anzeigen*

1. Öffnen Sie die von Ihrem Desktop kopierte Datei auf einem Notepad.
1. Ändern Sie den Wert von LearningManagerBaseUrl = `https://learningmanager.adobe.com/inappstarter` in LearningManagerBaseUrl = `https://learningmanagereu.adobe.com/inappstarter`

   ![](assets/cp-primebaseurl.png)
   *PrimeBaseURL anzeigen*

1. Speichern Sie die im Notepad vorgenommenen Änderungen.
1. Kopieren Sie die bearbeitete gespeicherte Datei und fügen Sie sie wieder in den Dateipfad ein. Ersetzen der Originaldatei in `kbd C:\\Program Files\\Adobe\\Adobe Captivate 2019 x64`
1. Starten Sie danach Adobe Captivate und versuchen Sie, die Veröffentlichung in Adobe Learning Manager durchzuführen.

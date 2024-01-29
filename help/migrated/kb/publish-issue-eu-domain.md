---
jcr-language: en_us
title: Veröffentlichung in der EU-Domäne des Learning Managers nicht möglich
description: Veröffentlichung von Adobe Captivate auf Adobe Learning Manager EU-Domäne im Adobe Learning Manager nicht möglich.
contentowner: nluke
source-git-commit: 69ac8f8ce5a0c077f31569571f9d9fbf16ecb943
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---



# Veröffentlichung in der EU-Domäne des Learning Managers nicht möglich {#unable-to-publish-to-learning-manager-eu-domain}

## Problem

Veröffentlichung von Adobe Captivate auf der EU-Domäne des Adobe Learning Manager nicht möglich.

## Fehler

Keine Konten gefunden

## Beschreibung

Es gibt Szenarien, in denen Autoren versuchen, einen Kurs von Adobe Captivate auf den Adobe Learning Manager zu veröffentlichen. Dies ist jedoch nicht möglich, da die Fehlermeldung &quot;Kein Konto gefunden&quot; angezeigt wird.

## Ursache

Dieses Problem tritt auf, weil Adobe Captivate standardmäßig so konfiguriert ist, dass Inhalte in der US-Domäne von Adobe Learning Manager veröffentlicht werden.

## Lösung:

Hinweise:

* Wenn Sie geöffnet sind, schließen Sie die Adobe Captivate-Anwendung.
* Sie benötigen Administratorzugriff auf Ihrem Computer, um die folgenden Schritte auszuführen. Falls Sie keinen Administratorzugriff haben, wenden Sie sich an Ihr IT-Team, um Unterstützung zu erhalten.

Führen Sie die folgenden Schritte aus:

1. Wechseln Sie zum Installationsverzeichnis für Adobe Captivate.

   Beispiel:  `kbd C:\\Program Files\\Adobe\\Adobe Captivate 2019 x64` (2019 ist die Captivate-Version. Sie weicht ab, wenn Sie eine andere Version von Adobe Captivate verwenden).

1. Konfigurationsdatei kopieren **AdobeCaptivate.ini** an Ihren Desktop senden.

   ![](assets/cp-captivate.ini.png)
   *Konfigurationsdatei anzeigen*

1. Öffnen Sie die von Ihrem Desktop kopierte Datei auf einem Notepad.
1. Ändern Sie den Wert von LearningManagerBaseUrl = `https://learningmanager.adobe.com/inappstarter` zu LearningManagerBaseUrl = `https://learningmanagereu.adobe.com/inappstarter`

   ![](assets/cp-primebaseurl.png)
   *PrimeBaseURL anzeigen*

1. Speichern Sie die im Notepad vorgenommenen Änderungen.
1. Kopieren Sie die bearbeitete gespeicherte Datei und fügen Sie sie wieder in den Dateipfad ein. Ersetzen Sie die Originaldatei in  `kbd C:\\Program Files\\Adobe\\Adobe Captivate 2019 x64`
1. Starten Sie anschließend Adobe Captivate und versuchen Sie, die Veröffentlichung auf Adobe Learning Manager durchzuführen.

---
description: Im Folgenden erfahren Sie, wie Sie HAR-Dateien in Google Chrome generieren.
jcr-language: en_us
title: Generieren einer HAR-Datei
contentowner: dvenkate
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---



# Generieren einer HAR-Datei

Im Folgenden erfahren Sie, wie Sie HAR-Dateien in Google Chrome generieren.

So generieren Sie eine HAR-Datei:

1. Öffnen Sie ein Google Chrome-Fenster und eine neue Registerkarte.
1. Öffnen Sie die Entwicklertools für die Seite, klicken Sie mit der rechten Maustaste auf > Inspect.
1. Öffnen Sie die **[!UICONTROL Netzwerk]** &quot; ändern. Stellen Sie sicher, dass die Schaltfläche für den roten Datensatz aktiviert ist. Aktivieren Sie die **[!UICONTROL Protokoll beibehalten]** ein.

   ![](assets/preserve-log-checkbox.png)

   *Aktivieren Sie das Kontrollkästchen Protokoll beibehalten auf der Registerkarte Netzwerk .*

1. Anmelden bei [Learning Manager](https://learningmanager.adobe.com/acapindex.html) mit Ihren Anmeldedaten verwenden und den Kurs belegen. Führen Sie alle Vorgänge aus, die zum Problem führen.
1. Klicken Sie in den Entwicklerwerkzeugen mit der rechten Maustaste und wählen Sie **Alle als HAR mit Inhalt speichern**.

   In einigen Versionen von Google Chrome müssen Sie möglicherweise **[!UICONTROL Kopieren]** > **[!UICONTROL Alle als HAR kopieren]**.

   ![](assets/copy-hra.png)

   *Alle HAR-Dateien kopieren*

1. Fügen Sie den kopierten Inhalt in eine Notepad-Datei ein. Speichern Sie es auf dem Desktop unter **logs.har** und senden Sie es per E-Mail an Adobe.

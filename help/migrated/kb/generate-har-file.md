---
description: Lesen Sie weiter, um zu erfahren, wie Sie HAR-Dateien in Google Chrome generieren.
jcr-language: en_us
title: Generieren einer HAR-Datei
contentowner: dvenkate
exl-id: 99fe78e8-b5e7-40a7-b9a5-efc2382de993
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 57%

---

# Generieren einer HAR-Datei

Lesen Sie weiter, um zu erfahren, wie Sie HAR-Dateien in Google Chrome generieren.

Gehen Sie folgendermaßen vor um eine HAR-Datei zu generieren:

1. Öffnen Sie ein Google Chrome-Fenster und öffnen Sie eine neue Registerkarte.
1. Öffnen Sie die Entwicklerwerkzeuge für die Seite, klicken Sie mit der rechten Maustaste > „Inspizieren“.
1. Öffnen Sie die Registerkarte **[!UICONTROL Netzwerk]**. Stellen Sie sicher, dass die Schaltfläche für den roten Datensatz aktiviert ist. Aktivieren Sie das Kontrollkästchen **[!UICONTROL Protokoll erhalten]**.

   ![](assets/preserve-log-checkbox.png)

   *Aktivieren Sie das Kontrollkästchen &quot;Protokoll beibehalten&quot; auf der Registerkarte &quot;Netzwerk&quot;.*

1. Melden Sie sich bei [Learning Manager](https://learningmanager.adobe.com/acapindex.html) mit Ihren Zugangsdaten an und nehmen Sie am Kurs teil. Führen Sie alle Vorgänge aus, die zu dem Problem führen.
1. Klicken Sie in den Entwicklertools mit der rechten Maustaste und wählen Sie **Alle als HAR mit Inhalt speichern**.

   In einigen Versionen von Google Chrome müssen Sie möglicherweise **[!UICONTROL Kopieren]** > **[!UICONTROL Alle als HAR]** kopieren auswählen.

   ![](assets/copy-hra.png)

   *Alle HAR-Dateien kopieren*

1. Fügen Sie den kopierten Inhalt in eine Notepad-Datei ein. Speichern Sie es auf dem Desktop unter **logs.har** und senden Sie es per E-Mail an Adobe.

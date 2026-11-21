---
title: Abgesicherter Prüfungsbrowser
description: Aktivieren Sie die Integration des sicheren Prüfungsbrowsers auf Kontoebene in Adobe Learning Manager, damit Autoren eine sichere Browserumgebung für native Tests benötigen können.
source-git-commit: 38dba6765ff013e446ab1f6098e9f1df0c24d0f9
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 1%
---

# Abgesicherter Prüfungsbrowser

Der abgesicherte Prüfungsbrowser bietet eine sichere Umgebung für Teilnehmer, um native Adobe Learning Manager-Tests absolvieren zu können, indem der Zugriff auf andere Browser und Anwendungen während einer Bewertung eingeschränkt wird.

Administratoren können die Integration des sicheren Prüfungsbrowsers auf Kontoebene aktivieren und eine Konfigurationsdatei (.seb) hochladen, um Quizeinschränkungen zu definieren. Nachdem die Integration aktiviert ist, können Autoren einzelne Quizze so konfigurieren, dass der sichere Prüfungsbrowser verwendet werden muss.

In diesem Artikel wird erläutert, wie Sie die Integration des sicheren Prüfungsbrowsers für Ihr Konto aktivieren.

## Integration des sicheren Prüfungsbrowsers aktivieren

Aktivieren Sie die Integration des sicheren Prüfungsbrowsers, um die Option Autoren bei der Konfiguration von Tests zur Verfügung zu stellen. Stellen Sie zunächst sicher, dass Sie über die Datei &quot;Safe Exam Browser&quot; für Ihr Konto verfügen.

So aktivieren Sie die Integration des sicheren Prüfungsbrowsers:

1. Melden Sie sich bei der ALM als **Administrator** an.
1. Wählen Sie **Einstellungen** > **Allgemein**.
1. Navigieren Sie zur **Integration des sicheren Prüfungsbrowsers**.
1. Wählen Sie **Bearbeiten**.

   Dadurch wird die **Integration des sicheren Prüfungsbrowsers** erweitert.

1. Wählen Sie **Aktivieren**.
1. Wählen Sie **Durchsuchen** aus, und laden Sie die Datei &quot;Safe Exam Browser&quot; vom System hoch. Weitere Informationen finden Sie in der Konfiguration [Abgesicherte Prüfungsbrowserdatei konfigurieren](#configure-the-seb-file-for-macos).

   ![Einstellungen für die Integration des sicheren Prüfungsbrowsers in den allgemeinen Einstellungen](assets/safe-exam-browser-integration-settings.png "Einstellungen für die Integration des sicheren Prüfungsbrowsers in den allgemeinen Einstellungen")

1. Wählen Sie **Speichern**.

   Der Browser für sichere Prüfungen ist jetzt für Autoren verfügbar, die ihn beim Konfigurieren unterstützter Quiz aktivieren können.

### Konfigurieren der .seb-Datei für macOS {#configure-the-seb-file-for-macos}

Erstellen Sie eine .seb-Datei mit dem SEB-Konfigurationstool, um Ihre Quizeinschränkungen, Sicherheitseinstellungen und zulässigen Anwendungen zu definieren. Stellen Sie vor der Verwendung des sicheren Prüfungsbrowsers (SEB) sicher, dass die .seb-Datei die folgenden Anforderungen erfüllt:

1. Setzen Sie den Parameter browserWindowWebView auf 3 (Ganzzahl), um SEB zu aktivieren.
1. Legen Sie startURL auf die URL fest, die der Zielumgebung entspricht.
1. Stellen Sie sicher, dass die SEB-Datei die erforderlichen quitURL-Informationen enthält.

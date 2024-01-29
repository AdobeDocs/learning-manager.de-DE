---
jcr-language: en_us
title: Learning Manager-Integration mit Slack
description: Learning Manager-Integration mit Slack
contentowner: dvenkate
source-git-commit: 864b1796f1ca99ae7b5643e8c58d1756ff2461a1
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---



# Learning Manager-Integration mit Slack

Wir haben **entfernt** **Slack** als Connector in Learning Manager. Sie haben keinen Zugriff mehr auf den Slack-Connector.

Als Slack-Benutzer können Sie die Adobe Learning Manager-App aus dem Slack-App-Verzeichnis in Ihren Slack-Teams installieren und Learning Manager-Inhalte direkt auf dem Slack erkunden. Sie können mit Primebot interagieren, um nach neuen Kursen zu suchen, Empfehlungen anzuzeigen und über bevorstehende Fristen im Learning Manager benachrichtigt zu werden. Sie können sich auch direkt von Slack aus registrieren und zu Ihren Lerninhalten springen.

Die Learning Manager-App für Slack wird in einer Azure-Instanz von Learning Manager nicht unterstützt.

## Installieren der Adobe Learning Manager-App {#installingadobecaptivateprimeapp}

Als Teilnehmer können Sie die CP Prime-App in Ihrem Slack-Konto installieren. Um die App zu installieren, öffnen Sie in Ihrem Slack-Konto das App-Verzeichnis und suchen Sie nach dem Learning Manager. Laden Sie die App herunter und installieren Sie sie. Wenn die App in Ihrem Konto nicht genehmigt wurde, wenden Sie sich zur Genehmigung an Ihren Integrationsadministrator. Wenn es bereits genehmigt ist, können Sie sich anmelden.

## Genehmigen der Anmeldung von Teilnehmern als Integrationsadministrator {#approvinglearnersigninasanintegrationadmin}

Um als Integrationsadministrator einem Teilnehmer die Berechtigung zur Verwendung der Prime-Anwendung auf dem Slack zu erteilen, führen Sie die folgenden Schritte aus.

1. Auswählen **[!UICONTROL Anwendungen]** aus dem linken Bereich und klicken Sie auf die Schaltfläche **[!UICONTROL Highlights]** &quot; ändern.

   ![](assets/featuredapps.jpg)

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Slack]** Kachel > die Slack-Integrationsseite wird geöffnet. Klicken **[!UICONTROL Genehmigen]** in der oberen rechten Ecke, um die Anwendung zu genehmigen.

   ![](assets/approval.png)

1. Gehen Sie zurück zur **[!UICONTROL Anwendungen]** angezeigt. Nach der Genehmigung sollte Slack im **[!UICONTROL Externe Apps]** &quot; ändern.
1. Teilnehmer können sich jetzt über den Slack bei ihrem Prime-Konto anmelden.

## Primebot-Funktionen {#primebotfunctionalities}

Sie können jetzt mit dem Primebot interagieren. Im Folgenden sind die Funktionen des Bots aufgeführt.

1 - Befehl

&#42;/prime&#42; können für einmalige, zielgerichtete Fragen zu Ihrem Adobe Learning Manager-Konto verwendet werden.

Die verfügbaren Unterbefehle sind:

&quot;/prime find&quot; `<query>` - nach Kursen, Zertifizierungen usw. suchen

&quot;/prime recommendation&quot; - Empfehlungen anzeigen

&quot;/prime terms&quot; - überfällige und bevorstehende Fristen anzeigen

&quot;/prime enrollments&quot; - Registrierungen anzeigen

&quot;/prime skills&quot; - Kenntnisse anzeigen

&quot;/prime notifications&quot; - Benachrichtigungen anzeigen

&quot;/prime catalogs&quot; - Kataloge anzeigen

&quot;/prime invite&quot; [Nur Administrator] Slack-Benutzer im aktuellen Team einladen, den primebot auszuprobieren

&quot;/prime profile&quot; - Profil anzeigen

&quot;/prime logout&quot; - Abmelden von Ihrem Prime-Konto in diesem Slack-Team

&quot;/prime help&quot; - Hilfe anzeigen

2 - Empfehlungen

Sie können einen Ausdruck wie `show my recommendations` , um eine personalisierte Liste der empfohlenen Kurse, Zertifizierungen und Lernprogramme von Ihrem Adobe Learning Manager-Konto zu erhalten.

3 - Suche

Sie können Ausdrücke wie `search for machine learning` oder `search for artificial intelligence`. Sie können die Art des Lernobjekts mit Ausdrücken wie `search for machine learning certifications`, `search for artificial intelligence courses` oder `search for adobe photoshop job aids`. Sie können auch in einem Katalog mit Ausdrücken wie `search for machine learning in Lynda catalog`.

4 - Fristen

Verwenden Sie Ausdruck wie `show my deadlines` , um eine Liste der überfälligen und bevorstehenden Fristen von Ihrem Adobe Learning Manager-Konto zu erhalten. Sie können überfällige oder bevorstehende Fristen mit Ausdrücken wie `show my overdue deadlines` oder `show my upcoming deadlines`.

---
jcr-language: en_us
title: Learning Manager-App für Salesforce
description: Salesforce ist eine der beliebtesten CRM-Lösungen unter Vertriebs- und Marketing-Teams. Indem Sie die Adobe Learning Manager-App in Salesforce verwenden, ermöglichen Sie den Benutzern den Zugriff auf ihre gesamten Lerninhalte direkt über die Salesforce-Benutzeroberfläche. Benutzer können auf die ihnen zugewiesenen Lerninhalte wie Kurse, Lernprogramme, Arbeitshilfen usw. direkt in Salesforce zugreifen. Benutzer können außerdem Benachrichtigungen über ihre Registrierungen und Ankündigungen vom Administrator erhalten.
contentowner: jayakarr
exl-id: 2efdf01e-43fb-4377-9334-2727c5358c76
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 57%

---

# Learning Manager-App für Salesforce

## Übersicht {#overview}

Salesforce™ ist eine der beliebtesten CRM-Lösungen unter Vertriebs- und Marketing-Teams. Indem Sie die Adobe Learning Manager-App in Salesforce verwenden, ermöglichen Sie den Benutzern den Zugriff auf ihre gesamten Lerninhalte direkt über die Salesforce-Benutzeroberfläche. Benutzer können auf die ihnen zugewiesenen Lerninhalte wie Kurse, Lernprogramme, Arbeitshilfen usw. direkt in Salesforce zugreifen. Benutzer können außerdem Benachrichtigungen über ihre Registrierungen und Ankündigungen vom Administrator erhalten.

Die Salesforce-App ist derzeit nicht verfügbar, da die Genehmigung vom Salesforce App Exchange noch aussteht. Wenn Sie eine Vorschau der Betaversion der App anzeigen möchten, wenden Sie sich an Ihren Kundenbetreuer oder Ihr Learning Manager-Support-Team.

## Installation und Einrichtung {#installationandsetup}

Erfahren Sie, wie Sie mithilfe der folgenden Schritte die Learning Manager-App für Salesforce installieren und einrichten.

### Voraussetzungen {#prerequisites}

1. Der Integrations-Administrator Ihres Unternehmens muss die Salesforce-App genehmigen. Diese App finden Sie im Bereich mit den vorgestellten Anwendungen der Learning Manager-Anwendung für die Rolle „Integrations-Admin“.
1. Zugriff auf das Salesforce-Konto Ihres Unternehmens, in dem die App installiert werden muss. In der Regel ist der Salesforce-Administrator in Ihrem Unternehmen die Person, die solche Apps installiert. Wenn Sie Learning Manager-Integrations-Administrator sind und kein Salesforce-Konto haben, wenden Sie sich an den Salesforce-Administrator Ihres Unternehmens.

### Installation {#installationsteps}

1. Bitten Sie Ihren Account Manager oder Customer Success Manager, Ihr Konto für die Nutzung dieser App zu aktivieren, und geben Sie dafür Ihre Learning Manager-Benutzerkonto-ID an. Fordern Sie außerdem die CSM-Datei für das installierbare Paket der Learning Manager Learner-App für Salesforce an.

1. Melden Sie sich bei Ihrem Learning Manager-Konto als Integrationsadministrator an und stellen Sie sicher, dass die Salesforce-App für Ihr Konto aktiviert ist.

1. Verwenden Sie zum Installieren der Learning Manager-App in Ihrem Salesforce-Konto das installierbare Paket, das von Ihrem Account Manager oder Customer Success Manager bereitgestellt wird. Sie benötigen Administratorrechte für das Salesforce-Konto, in dem Sie diese App installieren möchten.

1. Wählen Sie die entsprechende Option für Sie aus, wie in der Momentaufnahme gezeigt, und klicken Sie auf **[!UICONTROL Installieren]**.

   ![](assets/install-options.png)

   *Wählen Sie die Option &quot;Nur für Administratoren installieren&quot; aus*

   Wenn Sie sich für **Für bestimmte Profile installieren** entscheiden, wählen Sie eines oder mehrere Profile aus der Liste aus.

1. Klicken Sie im angezeigten Popup auf **[!UICONTROL Weiter]**, um den Zugriff durch Dritte zu bestätigen.

   In einer Meldung wird bestätigt, dass die App erfolgreich installiert wurde. Klicken Sie auf **Fertig**.

## Benachrichtigungskomponente auf Startseite hinzufügen {#addnotificationcomponenttothehomepage}

Das Team von Learning Manager empfiehlt, dass der Salesforce-Administrator auch die Learning Manager-Benachrichtigungskomponente zum Layout der Startseite hinzufügt. Diese Komponente ermöglicht Salesforce-Benutzern, Benachrichtigungen zu Zuweisungen und anderen Ankündigungen von Learning Manager zu erhalten, auch wenn sie nicht im Kontext der Lernanwendung stehen.

Um die Benachrichtigungskomponente für den Learning Manager zum Layout der Startseite hinzuzufügen, führen Sie die folgenden Schritte aus:

1. Klicken Sie oben rechts auf **[!UICONTROL Setup]**. Die Option &quot;Homepage-Layouts&quot; wird im linken Bereich angezeigt (siehe Abbildung unten).

   ![](assets/homepage-component.png)

   *Homepage-Layouts auswählen*

1. Wählen Sie das gewünschte Layout aus, und klicken Sie auf **[!UICONTROL Bearbeiten]**.
1. Wählen Sie die Adobe Learning Manager-Benachrichtigungsoption, die auf der Seite angezeigt wird, und klicken Sie auf **[!UICONTROL Weiter]**.
1. Wählen Sie die Reihenfolge der im linken Bereich angezeigten Komponenten aus, zeigen Sie eine Vorschau an, und klicken Sie auf **[!UICONTROL Speichern]**.

Weitere Informationen zur Anmeldung bei der Learning Manager-App und zur Verwendung dieser App in Salesforce als Teilnehmer finden Sie im Hilfeinhalt zur [Salesforce-App](../../learners/feature-summary/sfdc-app.md).

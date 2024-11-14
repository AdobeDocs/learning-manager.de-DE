---
jcr-language: en_us
title: Webhooks
description: Erfahren Sie mehr über Webhooks zum Senden von Echtzeitinformationen wie Kursanmeldungen, Kurserstellung und andere Informationen an eine bestimmte URL
contentowner: chandrum
exl-id: 472aaf2b-9c2f-4f43-a791-2b2d81e69471
source-git-commit: e4c3489db8207ead0416656161b918eba42f4582
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%

---

# Webhooks

Ein Webhook ermöglicht es einer Entität, automatisch Echtzeitdaten oder Benachrichtigungen an eine andere Entität zu senden, wenn ein bestimmtes Ereignis eintritt. Dadurch kann eine Anwendung anderen Anwendungen Informationen bereitstellen, ohne ständig danach zu fragen. Wenn ein Benutzer beispielsweise einen LMS-Kurs (Learning Management System) abschließt, kann ein Webhook diese Informationen automatisch an eine andere Plattform senden, z. B. ein CRM- oder Berichterstellungs-Tool. Webhooks werden häufig in Integrationen verwendet, um Prozesse zu automatisieren und die Notwendigkeit manueller Aktualisierungen zwischen Systemen zu reduzieren. Richten Sie Webhooks ein, indem Sie eine Rückruf-URL angeben, an die Sie die Daten senden würden.

## Webhooks und APIs

Webhooks und APIs helfen beiden Systemen dabei, miteinander zu kommunizieren, aber sie funktionieren auf unterschiedliche Weise. Bei APIs werden die Informationen nur freigegeben, wenn der Benutzer sie anfordert. Wenn ein Teilnehmer beispielsweise Kursfortschrittsdaten benötigt, sendet er eine Anforderung an die API, die dann die Informationen bereitstellt. Auf der anderen Seite senden Webhooks automatisch Daten, sobald ein Ereignis eintritt. Wenn ein Teilnehmer beispielsweise einen Kurs abschließt, sendet er die Daten sofort und ohne manuelle Anfragen an die Listener-URL.

## Was sind Echtzeit-APIs?

Mit Real-Time APIs können Anwendungen Daten sofort austauschen, wenn ein Ereignis eintritt. Im Gegensatz zu herkömmlichen APIs, die darauf warten, dass ein Benutzer Informationen anfordert, geben Echtzeit-APIs Daten in dem Moment frei, in dem sie auftreten. Webhooks fungieren als Echtzeit-API und helfen bei der sofortigen Freigabe der Daten, wenn das angegebene Ereignis eintritt. Die Echtzeit-API stellt sicher, dass diese Datenübertragung sofort erfolgt, ohne dass eine manuelle Anforderung erforderlich ist. So können die Systeme sofort aktualisiert werden.

## Webhook-Ereignisse

Webhook-Ereignisse sind bestimmte Aktionen in einem System, das automatisch Daten an eine Listener-URL sendet. Wenn sich ein Teilnehmer beispielsweise für einen Kurs registriert, wird ein Webhook-Ereignis ausgelöst, das die Registrierungsdetails an die Listener-URL sendet.
Webhook-Ereignisse werden in zwei Kategorien unterteilt:

* **Echtzeit-Ereignisse**: Ereignisse werden verarbeitet und in Echtzeit an eine Ziel-URL gesendet.
* **Nicht in Echtzeit stattfindende Ereignisse**: Ereignisse werden in Stapeln verarbeitet und zu bestimmten Zeiten gesendet anstatt in Echtzeit.

## Listener-URL

Eine Listener-URL ist ein Endpunkt oder ein Ziel, der bzw. das Dateninformationen empfängt, wenn ein Ereignis eintritt. Jedes Mal, wenn ein bestimmtes Ereignis eintritt, z. B. wenn sich ein Benutzer für einen Kurs registriert, sendet das System die Details automatisch ohne manuelle Anforderung an diese URL. Die Listener-URL ist die Adresse, an die alle diese Updates gesendet werden.
Webhook sendet die relevanten Informationen im JSON-Format. Hier ist eine Beispiel-Payload für ein Ereignis, das in Adobe Learning Manager ausgelöst wurde:

```
{
  "accountId": 1010,
  "events": [
    {
      "eventId": "d5fb7071-10a9-46b2-9f9e-79dde346c052",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": 1727414643000,
      "eventInfo": "1727414643000-047210-84242-0",
      "data": {
        "userId": 4279332,
        "loId": "course:7374992",
        "loInstanceId": "course:7376092_10250977",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1727414643
      }
    }
  ]
}
```

## Webhooks erstellen und verwalten - Integrationsadministrator

Führen Sie die folgenden Schritte aus, um die Webhooks-Integration in Adobe Learning Manager zu erstellen:

1. Melden Sie sich als **[!UICONTROL Integrationsadministrator]** an.
2. Wählen Sie auf der Startseite **[!UICONTROL Webhooks]** > **[!UICONTROL Webhook hinzufügen]** aus.

   ![](assets/create-webhook.png)
   _Webhook hinzufügen_

3. Geben Sie **[!UICONTROL Name]** und **[!UICONTROL Beschreibung]** des Webhooks ein.
4. Geben Sie die Listener-URL als **[!UICONTROL Ziel-URL]** ein, an die Sie die Ereignisdaten übergeben möchten.
5. Wählen Sie eine der Authentifizierungsmethoden aus:
Die Authentifizierung in Webhooks ist eine Sicherheitsmethode, mit der sichergestellt wird, dass die an eine Listener-URL gesendeten Daten aus einer vertrauenswürdigen Quelle stammen.
   * **[!UICONTROL Keine]**: Keine Authentifizierung erforderlich.
   * **[!UICONTROL Basic]**: Dies ist eine auf Anmeldeinformationen basierende Authentifizierung. Geben Sie den Benutzernamen und das Kennwort ein.
   * **[!UICONTROL Signatur]**: Das System erstellt eine spezielle Signatur und fügt sie den Webhook-Daten hinzu. Der empfangende Server überprüft diesen Code, um sicherzustellen, dass die Daten echt sind und nicht geändert wurden. Generieren Sie eine Signatur und verwenden Sie sie für die Authentifizierung. Laden Sie die Signatur als JSON herunter.
6. Wählen Sie die Webhook-Ereignisse aus der Dropdown-Liste **[!UICONTROL Trigger-Ereignisse]** aus.

   >[!NOTE]
   >
   >Sie können die Webhooks auch testen, indem Sie die Option Webhooks testen auf der Seite Webhook hinzufügen auswählen.

7. Wählen Sie den Schalter **[!UICONTROL Aktivierungsstatus]** aus, um den Webhook zu aktivieren. Nach der Aktivierung werden die Daten bei jedem Auftreten der ausgewählten Ereignisse übergeben.

>[!NOTE]
>
>Sie können bis zu 5 Webhooks erstellen und verwalten.

### Webhooks bearbeiten - Integrationsadministrator

Führen Sie die folgenden Schritte aus, um Webhooks aus Adobe Learning Manager zu bearbeiten:

1. Melden Sie sich als **[!UICONTROL Integrationsadministrator]** an.
2. Wählen Sie auf der Startseite **[!UICONTROL Webhooks]** aus.
3. Wählen Sie den Webhook aus, den Sie bearbeiten möchten.

   ![](assets/edit-webhook.png)
   _Webhook bearbeiten_
4. Wählen Sie **[!UICONTROL Bearbeiten]** aus, um die Details des Webhooks zu ändern, und wählen Sie **[!UICONTROL Speichern]** aus.

### Webhooks entfernen - Integrationsadministrator

Führen Sie die folgenden Schritte aus, um Webhooks aus Adobe Learning Manager zu bearbeiten:

1. Melden Sie sich als **[!UICONTROL Integrationsadministrator]** an.
2. Wählen Sie auf der Startseite **[!UICONTROL Webhooks]** aus.
3. Wählen Sie das webhook aus, das Sie löschen möchten.
4. Wählen Sie **[!UICONTROL Löschen]** aus, um die Webhooks zu entfernen.

![](assets/delete-webhooks.png)
_Webhook entfernen_

### Webhooks einstellen - Integrationsadministrator

Führen Sie die folgenden Schritte aus, um die Webhooks zu entfernen:

1. Melden Sie sich als **[!UICONTROL Integrationsadministrator]** an.
2. Wählen Sie auf der Startseite **[!UICONTROL Webhooks]** aus.
3. Wählen Sie den Webhook aus, den Sie bearbeiten möchten.
4. Wählen Sie **[!UICONTROL Bearbeiten]** aus und deaktivieren Sie den **[!UICONTROL Aktivierungsstatus]**, um den Webhook zu beenden.

![](assets/retire-webhook.png)
_Webhook einstellen_

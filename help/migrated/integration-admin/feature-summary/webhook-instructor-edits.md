---
description: Erhalten Sie Webhook-Ereignisse in Adobe Learning Manager, wenn Kursleiter Sitzungsdetails bearbeiten, und halten Sie Teilnehmerbenachrichtigungen und verbundene Systeme auf dem neuesten Stand.
jcr-language: en_us
title: Empfangen von Webhook-Ereignissen für die Bearbeitung von Kursleitersitzungen
exl-id: 6fa4b71b-a8f4-40a2-ab57-bb7f3016542c
source-git-commit: 90b45cb128b74ecb33a89bf42ef4d6e960101ff0
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%
---

# Webhook-Ereignisse für LO-Instanzbearbeitungen durch Kursleiter

Adobe Learning Manager stellt Webhook-Ereignisse bereit, die externe Systeme benachrichtigen, wenn eine Lernobjektinstanz (LO) geändert wird, z. B. eine Sitzung eines Kurses mit Kursleiter. Bisher wurden diese Ereignisse nur ausgelöst, wenn ein Administrator oder Autor eine LO-Instanz änderte. Webhook-Ereignisse werden jetzt auch ausgelöst, wenn ein Kursleiter die Details einer Sitzung bearbeitet.

Sie können diese Ereignisse verwenden, um externe Systeme wie E-Mail-Dienste, Kalender, Berichterstellungs-Tools oder Analyseplattformen auf dem neuesten Stand zu halten und die Änderungen der Kursleiter zu berücksichtigen. Beispielsweise können Sie Teilnehmer benachrichtigen, wenn sich eine Sitzungszeit ändert.

Bei der Bearbeitung durch Kursleiter wird das vorhandene Änderungsereignis der Lernobjektinstanz verwendet, sodass kein neuer Ereignistyp eingeführt wird.

>[!NOTE]
>
>Kursleiterbearbeitungen lösen einen Webhook nur aus, wenn ein aktiver Webhook das Änderungsereignis der Lernobjektinstanz abonniert. Erfahren Sie, wie Sie [Webhooks als Integrations-Admin erstellen und verwalten](/help/migrated/integration-admin/feature-summary/webhooks.md#create-manage-webhooks).

## Unterstützte Bearbeitungen von Kursleitern

Das Webhook-Ereignis wird ausgelöst, wenn ein Kursleiter eines der folgenden Sitzungsdetails bearbeitet:

* Sitzungszeiten

* Punktzahl

* Zeitzone

* Ort

* Registrierungslimit

* Limit für Warteliste

* Einsendungen zulassen

## Webhook-Nutzlaststruktur

Jede Webhook-Anforderung enthält die folgende Struktur der obersten Ebene:

```json
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "121da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235603297000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12324298_14453691",
        "loId": "course:12324298",
        "loType": "course"
      }
    }
  ]
}
```

Die gleiche Struktur wird verwendet, unabhängig davon, wer die LO-Instanz ändert. Die Payload gibt nicht an, ob ein Kursleiter, ein Administrator oder ein Autor die Änderung vorgenommen hat.

Wenn ein Kursleiter ein Sitzungsdetail ändert, z. B. die Zeitzone, das Registrierungslimit oder das Limit für die Warteliste, sendet der Webhook dieses Ereignis an Ihre Listener-URL. Verwenden Sie das Ereignis, um die neuesten Sitzungsdetails abzurufen und Teilnehmer zu benachrichtigen oder Ihre externen Systeme zu aktualisieren.

## Abrufen der aktualisierten Sitzungsdetails

Das webhook-Ereignis identifiziert die LO-Instanz, die geändert wurde. Um die aktualisierten Sitzungsdetails abzurufen, rufen Sie die öffentliche Lern-Manager-API (Prime-API) über das Ereignis &quot;`loId`&quot; auf:

```http
GET /primeapi/v2/learningObjects/{loId}
```

Suchen Sie die Instanz, die mit `loInstanceId` in der Antwort übereinstimmt, und vergleichen Sie sie dann mit den auf Ihrem System gespeicherten Daten.

## Integrationen mit Webhook-Ereignissen erstellen

Sie können die folgenden Webhook-Ereignisse verwenden, um:

* Senden Sie Teilnehmerbenachrichtigungen über einen externen E-Mail- oder Messaging-Dienst, wenn Sitzungsdetails wie Datum, Uhrzeit, Zeitzone oder Veranstaltungsort geändert werden.

* Synchronisieren Sie Sitzungsdaten mit externen Kalendern, Reporting- oder Analysesystemen.

* Verfolgen Sie Kapazitätsänderungen, wenn das Registrierungslimit oder das Wartelistenlimit einer Sitzung geändert wird.

* Überwachungspfade werden verwaltet, indem `eventId`, `timestamp` und `eventInfo` zusammen mit den LO- und Instanzeinstellungen protokolliert werden.

Ihr Webhook-Handler sollte mindestens:

* Nutzlast überprüfen und `events[]` analysieren.

* Verwenden Sie `eventName`, um das Änderungsereignis der Lernobjektinstanz zu identifizieren.

* Verwenden Sie `loId` und `loInstanceId`, um den entsprechenden Datensatz in Ihrem System zu suchen, und rufen Sie die öffentliche API auf, um die aktuellen Sitzungsdetails abzurufen.

* Verwenden Sie `eventId`, um eine doppelte Verarbeitung zu verhindern, wenn dasselbe Ereignis mehr als einmal übermittelt wird.

Das gleiche Ereignis wird an Kursleiter, Administratoren und Autoren gesendet, damit es bei der Integration häufiger als zuvor angezeigt wird. Vergleichen Sie die abgerufenen Sitzungsdetails mit den Daten in Ihrem System, bevor Sie eine Benachrichtigung senden. Teilnehmer werden nur benachrichtigt, wenn sich die relevanten Details ändern.

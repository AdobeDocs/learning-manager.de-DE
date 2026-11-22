---
description: Erfahren Sie, wie Sie die Board-Abonnementeinstellungen und Abonnenten-APIs verwenden, um Auswahl-E-Mails zu konfigurieren und Board-Abonnenten zu verwalten
jcr-language: en_us
title: API-Änderungen im November 2026
exl-id: 9b2d3856-810c-4352-bf18-667f698d4d70
source-git-commit: 4234f3cc3b9d77a7f9d197d2df2160ec62edd6d6
workflow-type: tm+mt
source-wordcount: '5724'
ht-degree: 4%
---

# API-Änderungen im Dezember 2026

## APIs für Benachrichtigungen von Diskussionsrunde-Kursleitern {#api-discussion-board-instructors}

In diesem Artikel werden die neuen APIs beschrieben, die Benachrichtigungen von Diskussionsrunde-Kursleitern unterstützen. Verwenden Sie sie, um Kursleiter und Kohortenmanager für Diskussionsforen zu abonnieren und zu steuern, welche Aktivität in ihren Auswahl-E-Mails angezeigt wird.

### API-Sequenz {#api-sequence}

Die APIs sind in zwei Gruppen unterteilt. Die `boardSubscriptionSettings`-API funktioniert auf Kontoebene. Die Abonnenten-API funktioniert auf Board-Ebene. Verwenden Sie die APIs in dieser Sequenz:

| Schritt | API | Zweck | Umfang |
|---|---|---|---|
| 1 | [`POST /boardSubscriptionSettings`](#api-create-settings) | Legen Sie die Einstellungen auf Kontoebene fest. | `admin:write` |
| 2 | [`PATCH /boardSubscriptionSettings`](#api-update-settings) | Aktualisieren der Einstellungen auf Kontoebene | `admin:write` |
| 3 | [`GET /boardSubscriptionSettings`](#api-get-settings) | Rufen Sie die Einstellungen auf Kontoebene ab. | `admin:read` |
| 4 | [`GET /boards/{id}/subscribers`](#api-get-subscribers) | Rufen Sie die Liste der Benutzer ab, die ein Board abonniert haben. | `admin:read` |
| 5 | [`POST /boards/{id}/subscribers`](#api-subscribe-users) | Abonnieren Sie Benutzer für ein Board. | `admin:write` |
| 6 | [`DELETE /boards/{id}/subscribers/{userId}`](#api-unsubscribe-user) | Abbestellen eines Benutzers für ein Board | `admin:write` |

### Authentifizierung und Berechtigungen

Jeder, der sich bei OAuth authentifiziert und über die Bereiche `admin:read` und `admin:write` verfügt, kann diese APIs aufrufen. Die APIs verwenden die folgenden OAuth-Geltungsbereiche:

* `admin:read` Auflisten von Abonnenten und Lesen von Benachrichtigungseinstellungen (`GET` Anforderungen).
* `admin:write` Erstellen oder ändern Sie die Benachrichtigungseinstellungen und fügen Sie Abonnenten hinzu oder entfernen Sie sie (`POST`, `PATCH` und `DELETE` Anfragen).

>[!NOTE]
>
>Der Zugriff auf das Board wird erneut überprüft, wenn eine Benachrichtigung gesendet wird. Wenn ein Abonnent den Zugriff auf ein Board verliert, wird die Übermittlung für dieses Board übersprungen, aber das Abonnement wird beibehalten. Die Bereitstellung wird fortgesetzt, wenn der Zugriff zurückkehrt.

### Einschränkungen und Überlegungen

* Die Anzahl der Abonnenten, die hinzugefügt werden können, ist begrenzt.
* Der Digest wird als einzelne E-Mail ohne Seitenumbruch gesendet und der E-Mail-Text weist eine Größenbeschränkung auf. Wählen Sie bei Foren mit großer Aktivität eine Digest-Häufigkeit aus, mit der jede E-Mail verwaltbar bleibt, z. B. alle 6 Stunden.
* Auswahl-Links öffnen den Beitrag, den Kommentar oder die Antwort nur für angemeldete Benutzer.

## API zum Erstellen von Einstellungen auf Kontoebene {#api-create-settings}

### Zweck der API {#purpose-create-settings}

Verwenden Sie diese API, um die Einstellungen auf Kontoebene für Board-Abonnementbenachrichtigungen zum ersten Mal festzulegen. Die Einstellungen steuern, wie Benachrichtigungen im gesamten Konto generiert werden:

* Welche Diskussionsforen-Ereignisse Benachrichtigungen generieren.
* Wie oft Auswahl-E-Mails gesendet werden.
* Ob Beiträge, Kommentare, Antworten und Abstimmungen enthalten sind.

Verwenden Sie &quot;[`PATCH /boardSubscriptionSettings`](#api-update-settings)&quot;, um die Einstellungen anschließend zu ändern.

### Endpunkt {#endpoint-create-settings}

```http
POST /primeapi/v2/boardSubscriptionSettings
```

| Eigenschaft | Wert |
|---|---|
| Umfang | `admin:write` |
| Anforderungsformat | `application/vnd.api+json;charset=UTF-8` |
| Antwortformat | `application/vnd.api+json;charset=UTF-8` |

### Anforderungstext {#request-body-create-settings}

Senden Sie die Einstellungen als Attribute einer `boardSubscriptionSettings`-Ressource.

| Feld | Typ | Beschreibung |
|---|---|---|
| `notifyNewPost` | boolesch | Gibt an, ob Abonnenten benachrichtigt werden, wenn ein neuer Beitrag zu einem Board hinzugefügt wird. |
| `notifyComment` | boolesch | Gibt an, ob Abonnenten benachrichtigt werden, wenn ein Kommentar zu einem Beitrag hinzugefügt wird. |
| `notifyReply` | boolesch | Gibt an, ob Abonnenten benachrichtigt werden, wenn eine Antwort auf einen Kommentar hinzugefügt wird. |
| `digestFrequencyHours` | Ganzzahl | Wie oft, in Stunden, wird die Auswahl-E-Mail gesendet. Gültige Werte reichen von 1 bis 168 (eine Woche). Beispielsweise sendet 24 eine tägliche und 168 eine wöchentliche Auswahl. |

### Beispielanforderung {#example-request-create-settings}

```bash
curl -X POST \
--header 'Content-Type: application/vnd.api+json;charset=UTF-8' \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
-d '{
  "data": {
    "type": "boardSubscriptionSettings",
    "attributes": {
      "notifyNewPost": true,
      "notifyComment": true,
      "notifyReply": true,
      "digestFrequencyHours": 24
    }
  }
}' \
'https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings'
```

### Beispielantwort - 201 Erstellt {#example-response-create-settings}

```json
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings"
  },
  "data": {
    "id": "1010",
    "type": "boardSubscriptionSettings",
    "attributes": {
      "digestFrequencyHours": 24,
      "notifyComment": true,
      "notifyNewPost": true,
      "notifyReply": true
    }
  }
}
```

### Antwortcodes {#response-codes-create-settings}

| Status | Bedeutung |
|---|---|
| 201 | Die Anforderung war erfolgreich. Die Einstellungen auf Kontoebene wurden erstellt. |
| 400 | Ein allgemeiner Fehler bei einer ungültigen Anforderung. |
| 401 | Der Anforderung fehlen gültige Anmeldeinformationen oder der Zugriff wurde aufgrund ungültiger Anmeldeinformationen verweigert. |

## API zum Aktualisieren von Einstellungen auf Kontoebene {#api-update-settings}

### Zweck der API {#purpose-update-settings}

Verwenden Sie diese API, um die Einstellungen auf Kontoebene zu aktualisieren, die Sie mit [`POST /boardSubscriptionSettings`](#api-create-settings) erstellt haben. Ändern Sie beispielsweise die Häufigkeit der Auswahl oder aktivieren oder deaktivieren Sie einen Ereignistyp.

### Endpunkt {#endpoint-update-settings}

```http
PATCH /primeapi/v2/boardSubscriptionSettings
```

| Eigenschaft | Wert |
|---|---|
| Umfang | `admin:write` |
| Anforderungsformat | `application/vnd.api+json;charset=UTF-8` |
| Antwortformat | `application/vnd.api+json;charset=UTF-8` |

### Anforderungstext {#request-body-update-settings}

Senden Sie die Attribute, die Sie ändern möchten, im selben Format wie die erstellte API: `notifyNewPost`, `notifyComment`, `notifyReply` und `digestFrequencyHours` Attribute, die Sie nicht senden, behalten ihre aktuellen Werte bei. Eine Beschreibung der einzelnen Attribute finden Sie unter [API zum Erstellen von Einstellungen auf Kontoebene](#api-create-settings).

### Beispielanforderung {#example-request-update-settings}

```bash
curl -X PATCH \
--header 'Content-Type: application/vnd.api+json;charset=UTF-8' \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
-d '{
  "data": {
    "type": "boardSubscriptionSettings",
    "attributes": {
      "notifyReply": true,
      "digestFrequencyHours": 12
    }
  }
}' \
'https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings'
```

### Beispielantwort - 200 OK {#example-response-update-settings}

```json
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings"
  },
  "data": {
    "id": "1010",
    "type": "boardSubscriptionSettings",
    "attributes": {
      "digestFrequencyHours": 12,
      "notifyComment": true,
      "notifyNewPost": true,
      "notifyReply": true
    }
  }
}
```

### Antwortcodes {#response-codes-update-settings}

| Status | Bedeutung |
|---|---|
| 200 | Die Anforderung war erfolgreich. Die Einstellungen auf Kontoebene wurden aktualisiert und die Antwort enthält die aktuellen Einstellungen. |
| 400 | Ein allgemeiner Fehler bei einer ungültigen Anforderung. |
| 401 | Der Anforderung fehlen gültige Anmeldeinformationen oder der Zugriff wurde aufgrund ungültiger Anmeldeinformationen verweigert. |

## API zum Abrufen von Einstellungen auf Kontoebene {#api-get-settings}

### Zweck der API {#purpose-get-settings}

Wenn Benutzer ein Board abonnieren, kann Adobe Learning Manager sie über Aktivitäten in diesem Board durch Auswahl-E-Mails benachrichtigen. Einstellungen auf Kontoebene legen fest, welche Aktivitätstypen eine Benachrichtigung auslösen und wie häufig die Auswertung gesendet wird.

Mit dieser API können Sie diese Einstellungen abrufen. Verwenden Sie diese Option, um die aktuelle Benachrichtigungskonfiguration in Ihrer Anwendung anzuzeigen oder um die Einstellungen zu überprüfen, bevor Sie von ihnen abhängige Funktionen erstellen.

### Endpunkt {#endpoint-get-settings}

```http
GET /primeapi/v2/boardSubscriptionSettings
```

| Eigenschaft | Wert |
|---|---|
| Umfang | `admin:read` |
| Antwortformat | `application/vnd.api+json;charset=UTF-8` |

### Beispielanforderung {#example-request-get-settings}

```bash
curl -X GET \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
'https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings'
```

### Beispielantwort - 200 OK {#example-response-get-settings}

```json
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings"
  },
  "data": {
    "id": "1010",
    "type": "boardSubscriptionSettings",
    "attributes": {
      "digestFrequencyHours": 24,
      "notifyComment": true,
      "notifyNewPost": true,
      "notifyReply": true
    }
  }
}
```

### Ressourcenschema {#resource-schema-get-settings}

**`boardSubscriptionSettings`Attribute**

| Feld | Typ | Beschreibung |
|---|---|---|
| `notifyNewPost` | boolesch | Gibt an, ob Abonnenten benachrichtigt werden, wenn ein neuer Beitrag zu einem Board hinzugefügt wird. |
| `notifyComment` | boolesch | Gibt an, ob Abonnenten benachrichtigt werden, wenn ein Kommentar zu einem Beitrag hinzugefügt wird. |
| `notifyReply` | boolesch | Gibt an, ob Abonnenten benachrichtigt werden, wenn eine Antwort auf einen Kommentar hinzugefügt wird. |
| `digestFrequencyHours` | Ganzzahl | Wie oft, in Stunden, wird die Auswahl-E-Mail gesendet. Gültige Werte reichen von 1 bis 168 (eine Woche). Verwenden Sie diesen Wert, um Benutzern mitzuteilen, wie oft mit der Auswahl-E-Mail zu rechnen ist. Beispiel: Zeigen Sie &quot;Daily&quot; bei einem Wert von 24 und &quot;Weekly&quot; bei einem Wert von 168 an. |

### Antwortcodes {#response-codes-get-settings}

| Status | Bedeutung |
|---|---|
| 200 | Die Anforderung war erfolgreich. Die Antwort enthält die Board-Abonnementeinstellungen auf Kontoebene. |
| 400 | Ein allgemeiner Fehler bei einer ungültigen Anforderung. |
| 401 | Der Anforderung fehlen gültige Anmeldeinformationen oder der Zugriff wurde aufgrund ungültiger Anmeldeinformationen verweigert. |

### Diese API in Ihrer Integration verwenden {#integration-get-settings}

Ein häufiger Anwendungsfall ist ein Bildschirm mit Benachrichtigungseinstellungen, der anzeigt, wie Board-Abonnement-E-Mails für das Konto konfiguriert sind.

1. Wenn der Bildschirm mit den Benachrichtigungseinstellungen der Anwendung geladen wird, rufen Sie `GET /boardSubscriptionSettings` an.
1. Zeigen Sie anhand der Werte in der Antwort an, welche Aktivitätstypen eine Benachrichtigung auslösen und wie oft die Auswahl-E-Mail gesendet wird.

## API zum Abrufen von Board-Abonnenten {#api-get-subscribers}

### Zweck der API {#purpose-get-subscribers}

Rufen Sie die Liste der Benutzer ab, die ein bestimmtes Board abonnieren. Benutzer, die ein Board abonnieren, werden über neue Aktivitäten darin benachrichtigt. Diese API gibt die Benutzer zurück, die derzeit ein bestimmtes Board abonnieren, zusammen mit Details darüber, wann und von wem jedes Abonnement erstellt wurde.

Verwenden Sie diese API, um eine Abonnentenliste in Ihrer Anwendung anzuzeigen, zu überprüfen, wer Updates für ein Board erhält, oder um Board-Abonnementdaten mit einem externen System zu synchronisieren.

Die Antwort ist paginiert. Verwenden Sie die Abfrageparameter &quot;`page[offset]`&quot; und &quot;`page[limit]`&quot;, um große Abonnentenlisten zu durchsuchen. Die zurückgegebenen Daten unterliegen den Berechtigungen des aufrufenden Benutzers auf dem angeforderten Board.

### Endpunkt {#endpoint-get-subscribers}

```http
GET /primeapi/v2/boards/{id}/subscribers
```

| Eigenschaft | Wert |
|---|---|
| Umfang | `admin:read` |
| Antwortformat | `application/vnd.api+json;charset=UTF-8` |

### Parameter {#parameters-get-subscribers}

| Parameter | In | Erforderlich | Standard | Beschreibung |
|---|---|---|---|---|
| `id` | Pfad | Ja | N/A | Die ID des Boards, dessen Abonnenten Sie abrufen möchten. Der Zugriff auf das Board hängt von den Berechtigungen des Anrufers ab. |
| `page[offset]` | Abfrage | Nein | 0 | Die Ausgangsposition der zurückzugebenden Datensätze. |
| `page[limit]` | Abfrage | Nein | 10 | Die Anzahl der Abonnenten, die pro Seite zurückgegeben werden sollen. Der maximal zulässige Wert ist 200. |

### Beispielanforderung {#example-request-get-subscribers}

```bash
curl -X GET \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
'https://learningmanager.adobe.com/primeapi/v2/boards/1234/subscribers?page[offset]=0&page[limit]=50'
```

### Beispielantwort - 200 OK {#example-response-get-subscribers}

```json
{
  "data": [
    {
      "id": "1234:5678",
      "type": "boardSubscriber",
      "attributes": {
        "boardId": 1234,
        "dateSubscribed": 1757000000000,
        "subscribedByUserId": 5678,
        "user": {
          "id": "5678",
          "name": "Jane Doe",
          "email": "jane.doe@example.com",
          "avatarUrl": "https://example.com/avatars/5678.png",
          "bio": "Learning enthusiast",
          "contentLocale": "en-US",
          "uiLocale": "en-US",
          "timeZoneCode": "PST",
          "userType": "INTERNAL",
          "state": "ACTIVE",
          "profile": "Learner",
          "roles": ["Learner"],
          "gamificationEnabled": true,
          "pointsEarned": 120,
          "pointsRedeemed": 20,
          "enrollOnClick": true,
          "preferredResolution": "720p",
          "lastLoginDate": "2026-09-23T18:12:04.000Z"
        }
      }
    }
  ]
}
```

### Ressourcenschema {#resource-schema-get-subscribers}

Die Antwort enthält eine neue Ressource, `boardSubscriber`. Die Attribute umfassen `boardId`, `dateSubscribed`, `subscribedByUserId` und `user`. Das eingebettete Benutzerobjekt enthält Abonnenteninformationen wie Benutzer-ID, Name, E-Mail-Adresse, Profil und Rollen sowie weitere Benutzer-Metadaten.

**`boardSubscriber`Attribute**

| Feld | Typ | Beschreibung |
|---|---|---|
| `id` | Zeichenfolge | Deckende Abonnement-ID. |
| `type` | Zeichenfolge | Der Ressourcentyp |
| `boardId` | Tage | ID des Boards, für das der Benutzer abonniert ist. |
| `dateSubscribed` | Tage | Zeitstempel, wann der Benutzer das Board abonniert hat. |
| `subscribedByUserId` | Tage | ID des Benutzers, der das Abonnement erstellt hat. |
| `user` | Einspruch | Details zum abonnierten Benutzer (eingebettet, siehe unten). |

**`user`(eingebettet, in einen Abonnenten)**

| Feld | Typ | Beschreibung |
|---|---|---|
| `id` | Zeichenfolge | Deckende Benutzer-ID. |
| `name` | Zeichenfolge | Anzeigename des Benutzers. |
| `email` | Zeichenfolge | E-Mail-Adresse des Benutzers. |
| `avatarUrl` | Zeichenfolge | URL des Profilbilds des Benutzers. |
| `bio` | Zeichenfolge | Kurze Biografie des Nutzers. |
| `binUserId` | Zeichenfolge | Interne Identifizierung des Anwenders. |
| `userUniqueId` | Zeichenfolge | Eindeutige Identifizierung des Benutzers im Konto. |
| `userType` | Zeichenfolge | Typ des Benutzers, z. B. interne oder externe. |
| `state` | Zeichenfolge | Aktueller Status des Benutzerkontos. |
| `profile` | Zeichenfolge | Dem Benutzer zugewiesenes Profil. |
| `roles` | Zeichenfolgen-Array | Rollen des Benutzers. |
| `contentLocale` | Zeichenfolge | Gebietsschema, in dem der Benutzer Inhalte anzeigen möchte. |
| `uiLocale` | Zeichenfolge | Gebietsschema, das für die Benutzeroberfläche verwendet wird. |
| `timeZoneCode` | Zeichenfolge | Für den Benutzer konfigurierte Zeitzone. |
| `preferredResolution` | Zeichenfolge | Bevorzugte Videoauflösung des Benutzers. |
| `enrollOnClick` | boolesch | Ob der Benutzer bei der Auswahl eines Lernobjekts automatisch registriert wird. |
| `gamificationEnabled` | boolesch | Ob Gamification für den Benutzer aktiviert ist. |
| `pointsEarned` | Tage | Gesamtanzahl der vom Benutzer gesammelten Gamification-Punkte. |
| `pointsRedeemed` | Tage | Gesamtanzahl der vom Benutzer eingelösten Gamification-Punkte. |
| `lastLoginDate` | Zeichenfolge | Datum und Uhrzeit der letzten Anmeldung des Benutzers. |
| `fields` | Einspruch | Benutzerdefinierte Benutzerfelder und ihre Werte. |
| `metadata` | Einspruch | Dem Benutzer sind zusätzliche Metadaten zugeordnet. |

### Antwortcodes {#response-codes-get-subscribers}

| Status | Bedeutung |
|---|---|
| 200 | Die Anforderung war erfolgreich. Die Antwort enthält die Teilnehmer des Boards. |
| 400 | Ein allgemeiner Fehler bei einer ungültigen Anforderung. Beispielsweise ist die Karten-ID oder ein Seitenumbruchwert fehlerhaft. |
| 401 | Der Anforderung fehlen gültige Anmeldeinformationen oder der Zugriff wurde aufgrund ungültiger Anmeldeinformationen verweigert. |

### Diese API in Ihrer Integration verwenden {#integration-get-subscribers}

Ein häufiger Anwendungsfall ist eine Admin- oder Moderatoransicht, in der jeder angezeigt wird, der Updates für ein Board erhält.

1. Wenn die Ansicht geladen wird, rufen Sie diesen Endpunkt mit der Board-ID und einem `page[limit]`-Wert auf, der für Ihr Layout geeignet ist (bis zu 200).
1. Zeigen Sie für jeden Abonnenten die Werte `user.name`, `user.email` und `dateSubscribed` an.
1. Wenn die Anzahl der zurückgegebenen Datensätze gleich `page[limit]` ist, sind möglicherweise mehr Abonnenten vorhanden. Rufen Sie den Endpunkt erneut auf, indem Sie `page[offset]` um die Seitengröße erhöhen, bis eine Seite weniger Datensätze zurückgibt als angefordert.

## API zum Abonnieren von Benutzern eines Boards {#api-subscribe-users}

### Zweck der API {#purpose-subscribe-users}

Abonnieren Sie einen oder mehrere Benutzer eines Diskussionsforums, damit sie Auswahl-E-Mails dafür erhalten. Identifizieren Sie Benutzer anhand der Benutzer-ID, der E-Mail-Adresse (in aufgelöste Benutzer-IDs innerhalb des Kontos) oder beidem. Sie können mehrere Benutzer in einer einzigen Anforderung hinzufügen. Siehe [Massenabonnements](#bulk-subscriptions).

### Endpunkt {#endpoint-subscribe-users}

```http
POST /primeapi/v2/boards/{id}/subscribers
```

| Eigenschaft | Wert |
|---|---|
| Umfang | `admin:write` |
| Anforderungsformat | `application/vnd.api+json;charset=UTF-8` |
| Antwortformat | `application/vnd.api+json;charset=UTF-8` |

### Parameter {#parameters-subscribe-users}

| Parameter | In | Erforderlich | Beschreibung |
|---|---|---|---|
| `id` | Pfad | Ja | Die ID des Boards, für das Benutzer abonniert werden sollen. |

### Anforderungstext {#request-body-subscribe-users}

Senden Sie die Benutzer als Attribute einer `boardSubscriberBulkRequest`-Ressource. Mindestens `userIds` oder `emails` ist erforderlich.

| Feld | Typ | Beschreibung |
|---|---|---|
| `data.attributes.userIds` | Zahlenfeld | Die IDs der zu abonnierenden Benutzer. |
| `data.attributes.emails` | Zeichenfolgen-Array | Die E-Mail-Adressen der Benutzer, die abonniert werden sollen. Jede Adresse wird in eine Benutzer-ID innerhalb des Kontos aufgelöst. |

### Beispielanforderung {#example-request-subscribe-users}

```bash
curl -X POST \
--header 'Content-Type: application/vnd.api+json;charset=UTF-8' \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
-d '{
  "data": {
    "type": "boardSubscriberBulkRequest",
    "attributes": {
      "userIds": [
        1234,
        5678
      ],
      "emails": [
        "abc@xyz.com"
      ]
    }
  }
}' \
'https://learningmanager.adobe.com/primeapi/v2/boards/1010/subscribers'
```

### Beispielantwort - 207 Multi-Status {#example-response-subscribe-users}

```json
{
  "added": [
    {
      "userId": "12345",
      "status": "SUCCESS"
    }
  ],
  "failed": [
    {
      "userId": "78910",
      "errorCode": "NO_BOARD_ACCESS"
    }
  ]
}
```

**Antwortattribute**

| Feld | Typ | Beschreibung |
|---|---|---|
| `added` | Feld | Die Benutzer, die abonniert wurden. Jeder Eintrag hat ein `userId` und ein `status`. Benutzer, die bereits ein Abonnement hatten, werden hier ebenfalls als Erfolge gemeldet. |
| `failed` | Feld | Die Benutzer, die nicht abonniert werden konnten. Jeder Eintrag hat ein `userId` und ein `errorCode`, z. B. `NO_BOARD_ACCESS`. |

### Antwortcodes {#response-codes-subscribe-users}

| Status | Bedeutung |
|---|---|
| 207 | Mehrere Status. Die Anforderung wurde verarbeitet, und die Antwort listet das Ergebnis für jeden Benutzer in `added` und `failed` auf. |
| 400 | Ein allgemeiner Fehler bei einer ungültigen Anforderung. |
| 401 | Der Anforderung fehlen gültige Anmeldeinformationen oder der Zugriff wurde aufgrund ungültiger Anmeldeinformationen verweigert. |
| 404 | Die angeforderte Ressource, z. B. das Board, wurde nicht gefunden. |
| 409 | Das Board ist inaktiv, gelöscht oder eingestellt, sodass die gesamte Anforderung abgelehnt wird. |

### Massenabonnements {#bulk-subscriptions}

Verwenden Sie ein Massenabonnement, um einer Diskussionsrunde in einer einzigen Anforderung mehrere Benutzer hinzuzufügen. Mit einem Massenabonnement können Sie die Anzahl der API-Aufrufe reduzieren, die Sie zum Verwalten von Abonnenten benötigen. Dies ist nützlich, wenn:

* Ein Kursleiter verwaltet mehrere Kohorten.
* Ein Kohortenmanager benötigt Zugriff auf viele Diskussionsforen.
* Ein externes System synchronisiert Board-Abonnements im Batch.
* Mehrere Kursleiter müssen während der Erstellung der Kohorte abonniert werden.

#### Verhalten beim Massenhinzufügen

Eine Massenanfrage kann Benutzer-IDs, E-Mail-Adressen oder eine Kombination aus beidem enthalten. Jeder Benutzer wird unabhängig verarbeitet.

#### Idempotentes Verhalten

Massen-Add ist idempotent. Wenn ein Benutzer bereits für das Board abonniert ist, ist die Anforderung erfolgreich, es wird kein doppeltes Abonnement erstellt und das vorhandene Abonnement bleibt unverändert. So können Clients Anfragen sicher wiederholen.

#### Teilweiser Erfolg

Einige Benutzer können abonniert werden, während andere die Validierung nicht bestehen. Der Vorgang schlägt nicht fehl, da mindestens ein Benutzer ungültig ist.

| Fall | Ergebnis |
|---|---|
| Der Benutzer existiert und hat Zugriff auf das Board. | Erfolgreich |
| Der Benutzer ist bereits angemeldet | Erfolgreich |
| Der Benutzer hat keinen Zugriff auf das Board. | Fehler (`NO_BOARD_ACCESS`) |
| Der Benutzer ist nicht vorhanden. | Fehlschlag |
| Der Benutzer ist inaktiv | Fehlschlag |
| Der Benutzer wurde gelöscht | Fehlschlag |

#### Antwortformat

Das Massenabonnement gibt einen HTTP 207-Multistatus mit einem `added`-Ergebnis und einem `failed`-Ergebnis für jeden Benutzer zurück, wie in der [Beispielantwort](#example-response-subscribe-users).

#### Häufige Validierungsfehler

* **Der Benutzer hat keinen Zugriff auf das Board.** Wenn ein Benutzer keine Sichtbarkeit für das Board hat, wird `NO_BOARD_ACCESS` für diesen Benutzer zurückgegeben. Die verbleibenden Benutzer werden weiterhin normal verarbeitet.
* **Das Board ist inaktiv, gelöscht oder eingestellt.** Wenn das Board nicht zu Abonnements berechtigt ist, wird die Anforderung mit dem HTTP 409-Konflikt abgelehnt.
* **Der Benutzer ist ungültig.** Wenn kein Benutzerkonto vorhanden, inaktiv oder gelöscht wurde, gibt der Vorgang einen Fehlereintrag für diesen Benutzer zurück.

## API zum Abbestellen eines Benutzers von einem Board {#api-unsubscribe-user}

### Zweck der API {#purpose-unsubscribe-user}

Abbestellen eines Benutzers in einem Diskussionsforum. Nachdem das Abonnement entfernt wurde, erhält der Benutzer keine Benachrichtigungen und Auswahl-E-Mails für dieses Board mehr.

### Endpunkt {#endpoint-unsubscribe-user}

```http
DELETE /primeapi/v2/boards/{id}/subscribers/{userId}
```

| Eigenschaft | Wert |
|---|---|
| Umfang | `admin:write` |
| Antwortformat | `application/vnd.api+json;charset=UTF-8` |

### Parameter {#parameters-unsubscribe-user}

| Parameter | In | Erforderlich | Beschreibung |
|---|---|---|---|
| `id` | Pfad | Ja | Die ID des Boards. |
| `userId` | Pfad | Ja | Die ID des Benutzers, dessen Abonnement Sie kündigen möchten. |

### Beispielanforderung {#example-request-unsubscribe-user}

```bash
curl -X DELETE \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
'https://learningmanager.adobe.com/primeapi/v2/boards/1234/subscribers/5678'
```

### Beispielantwort - 204 Kein Inhalt {#example-response-unsubscribe-user}

Die Antwort hat keinen Körper.

### Antwortcodes {#response-codes-unsubscribe-user}

| Status | Bedeutung |
|---|---|
| 204 | Die Anforderung war erfolgreich. Der Benutzer wurde vom Board abgemeldet. |
| 400 | Ein allgemeiner Fehler bei einer ungültigen Anforderung. |
| 401 | Der Anforderung fehlen gültige Anmeldeinformationen oder der Zugriff wurde aufgrund ungültiger Anmeldeinformationen verweigert. |
| 404 | Die angeforderte Ressource, z. B. das Board oder das Abonnement, wurde nicht gefunden. |

## Reihenfolge von Lesezeichen-APIs und Behandlung eingestellter Inhalte {#bookmark-api-ordering-retired-content}

### Zweck der API

Teilnehmer speichern Lesezeichen für Schulungen, die sie erneut aufrufen möchten. Vor dieser Änderung haben die Lesezeichen-APIs Lesezeichen in keiner bestimmten Reihenfolge zurückgegeben. Integrationen, insbesondere Headless-Implementierungen, konnten die zuletzt gespeicherten Lesezeichen nicht zuerst anzeigen. Teilnehmer mit vielen Lesezeichen mussten ältere Elemente durchblättern, um aktuelle zu finden.

Lesezeichen für eingestellte Lernobjekte blieben ebenfalls in der Liste. Die Auswahl einer Seite führte zum Fehler &quot;Seite nicht gefunden&quot;.

Diese Änderung verbessert die Lesezeichen-APIs auf zwei Arten:

* Lesezeichen werden in chronologischer Reihenfolge zurückgegeben, die neuesten zuerst.
* Lesezeichen für eingestellte Lernobjekte werden nicht mehr zurückgegeben.

Es werden keine neuen Endpunkte, Parameter oder Antwortattribute eingeführt. Bestehende Integrationen funktionieren weiterhin ohne Änderungen.

### Basis-URL und Konventionen

Die Lesezeichen-APIs verwenden den folgenden Basispfad und die folgenden Konventionen:

| Element | Wert |
|---|---|
| Basispfad | `/primeapi/v2` |
| Inhaltstyp | `application/vnd.api+json` |
| Authentifizierung | OAuth-Token mit Lesezugriff für Teilnehmer |
| Standardreihenfolge | Neuestes Lesezeichen zuerst |
| Neue Parameter | Ohne |
| Antwortstruktur | unverändert |

### Endpunkte

#### Endpunkte, die Lesezeichen zurückgeben

Die folgenden Endpunkte geben Lesezeichen in der neuen Reihenfolge zurück:

| Endpunkt | Rückgabe |
|---|---|
| `GET /primeapi/v2/learningObjects?filter.bookmarks=true` | Lernobjekte, die der Teilnehmer mit einem Lesezeichen versehen hat |
| `GET /primeapi/v2/bookmarks` | Lesezeichen für Teilnehmer |

#### Lernobjekte mit Lesezeichen in der richtigen Reihenfolge abrufen

`GET /primeapi/v2/learningObjects?filter.bookmarks=true`

<!-- Content Review by Claude: Please confirm the endpoint list. The dev-to-QE hand-off confirms ordering for GET /learningObjects?filter.bookmarks=true. The PRD (ALMER-442) also lists GET /primeapi/v2/bookmarks. Please also confirm the OAuth scope. -->

Gibt die Lernobjekte zurück, die der aufrufende Teilnehmer mit einem Lesezeichen versehen hat. Das zuletzt mit einem Lesezeichen versehene Element ist das erste und das älteste das letzte.

**Umfang:** Lesezugriff für Teilnehmer

Der Endpunkt akzeptiert den folgenden Abfrageparameter:

| Parameter | In | Erforderlich | Beschreibung |
|---|---|---|---|
| `filter.bookmarks` | Abfrage | Ja | Auf `true` setzen, um nur die Lernobjekte zurückzugeben, die der Teilnehmer mit einem Lesezeichen versehen hat |

**Beispielanforderung**

```http
GET /primeapi/v2/learningObjects?filter.bookmarks=true
Accept: application/vnd.api+json
Authorization: oauth <access-token>
```

**Beispiel 200 OK-Antwort**

Der Teilnehmer hat mit dem Lesezeichen &quot;Erste Schritte mit Adobe Analytics&quot;, &quot;Erstellen von Workspace-Projekten&quot; als &quot;Zweite&quot; und &quot;Erweiterte Segmentierung&quot; in Adobe Analytics als &quot;Letzte&quot; gekennzeichnet. Die Antwort listet sie von der neuesten zur ältesten auf. Andere Attribute werden aus Kurzgründen weggelassen.

```json
{
  "data": [
    {
      "id": "course:2400162",
      "type": "learningObject",
      "attributes": {
        "name": "Advanced Segmentation in Adobe Analytics"
      }
    },
    {
      "id": "course:2400160",
      "type": "learningObject",
      "attributes": {
        "name": "Building Workspace Projects"
      }
    },
    {
      "id": "course:2400159",
      "type": "learningObject",
      "attributes": {
        "name": "Getting Started with Adobe Analytics"
      }
    }
  ]
}
```

>[!NOTE]
>
>Die neue Reihenfolge ist das Standardverhalten und gilt für alle Konten.

### Lesezeichenanordnung

#### Anordnung von Lesezeichen

Lesezeichen werden nach dem Datum sortiert, an dem der Teilnehmer sie gespeichert hat, also vom neuesten zum ältesten Lesezeichen. Wenn ein Teilnehmer beispielsweise Kurs A, dann Kurs B und dann Kurs C mit einem Lesezeichen versieht, werden in der Antwort zuerst Kurs C, dann Kurs B und zuletzt Kurs A aufgeführt.

Wenn ein mit einem Lesezeichen versehenes LO an der 10. Position beispielsweise &quot;nicht gespeichert&quot; ist und später erneut mit einem Lesezeichen versehen wird, wird es als letztes mit einem Lesezeichen und zuerst in der Liste angezeigt.

Integrationen, die zuvor Lesezeichen auf dem Client sortiert haben, können diese Logik entfernen und die Ergebnisse in der zurückgegebenen Reihenfolge anzeigen.

### Umgang mit eingestellten Inhalten

#### Wie mit eingestellten Lernobjekten verfahren wird

Lesezeichen für eingestellte Lernobjekte werden in der Antwort nicht zurückgegeben, unabhängig davon, ob der Teilnehmer für das Lernobjekt registriert ist.

Mit einem Lesezeichen versehene eingestellte Lernobjekte werden nur angezeigt, wenn der Teilnehmer dafür registriert ist.

Teilnehmer sehen keine Lesezeichen mehr, die zum Fehler &quot;Seite nicht gefunden&quot; führen. Das Lesezeichen wird in den Ergebnissen ausgeblendet und nicht gelöscht.

### Kompatibilität

Durch diese Änderung werden die vorhandenen API-Verbraucher nicht beschädigt:

* Die Endpunkte und ihre Parameter bleiben unverändert.
* Die Antwortstruktur bleibt unverändert und es werden keine Attribute hinzugefügt oder entfernt.
* Nur die Reihenfolge der Ergebnisse und der Ausschluss eingestellter Lernobjekte unterscheiden sich von früheren Verhaltensweisen.

### Diese API in Ihrer Integration verwenden

Ein häufiger Anwendungsfall ist eine Liste &quot;Gespeichert für später&quot; in einer Headless-Lernumgebung. Sie möchten, dass die Teilnehmer ihre neuesten Lesezeichen zuerst sehen, ohne Links zu eingestellten Inhalten.

1. Rufen Sie `GET /primeapi/v2/learningObjects?filter.bookmarks=true` an, wenn der Teilnehmer die Liste öffnet.
2. Zeigen Sie die Lernobjekte in der zurückgegebenen Reihenfolge an. Das erste Element ist das zuletzt mit einem Lesezeichen versehene.
3. Entfernen Sie alle clientseitigen Sortierungen oder eingestellten Inhaltsdaten, die Sie als Problemumgehung hinzugefügt haben.
4. Anzahl der Lesezeichen anhand der Anzahl der Elemente in der Antwort anzeigen. Lesezeichen für eingestellte Lernobjekte sind nicht mehr enthalten.

### API-Unterstützung für mehrfach registrierte Instanzen im Teilnehmer-Compliance-Widget in der Teilnehmer-App {#api-multienrolled-instances-lc-widget}

Die öffentliche API unterstützt dieses Verhalten über einen optionalen Abfrageparameter für den vorhandenen Registrierungsendpunkt. Wenn Sie den Parameter auslassen, gibt die API die gleichen Ergebnisse wie zuvor zurück, sodass vorhandene Integrationen, einschließlich Headless-Implementierungen, weiterhin unverändert funktionieren.

**Endpunkt**

GET /primeapi/v2/enrollments

**Abfrageparameter**

includeMultiInstanceEnrollments (optional)

**Abfrage**

https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page\[limit\]=10&filter.loTypes=course&includeHierarchicalEnrollments=false&includeMultiInstanceEnrollments=true&sort=dateEnrolled

**Wert**

true. Der Standardwert ist false.

**Antworttext**

{

&quot;links&quot;: {

&quot;self&quot;: &quot;[https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page\[limit\]=10&amp;filter.loTypes=course&amp;sort=dateEnrolled&amp;includeHierarchicalEnrollments=false&amp;includeMultiInstanceEnrollments=true](https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page%5blimit%5d=10&filter.loTypes=course&sort=dateEnrolled&includeHierarchicalEnrollments=false&includeMultiInstanceEnrollments=true)&quot;,

&quot;next&quot;: &quot;[https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page\[limit\]=10&amp;filter.loTypes=course&amp;sort=dateEnrolled&amp;includeHierarchicalEnrollments=false&amp;includeMultiInstanceEnrollments=true&amp;page\[cursor\]=eyJjb3Vyc2VNdWx0aSI6MCwiam9iQWlkIjowLCJjb3Vyc2UiOjEwLCJsZWYFF mluZ1Byb2dyYW0iOjAsImNlcnRpZmljYXRpb24iOjB9](https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page%5blimit%5d=10&filter.loTypes=course&sort=dateEnrolled&includeHierarchicalEnrollments=false&includeMultiInstanceEnrollments=true&page%5bcursor%5d=eyJjb3Vyc2VNdWx0aSI6MCwiam9iQWlkIjowLCJjb3Vyc2UiOjEwLCJsZWFybmluZ1Byb2dyYW0iOjAsImNlcnRpZmljYXRpb24iOjB9)&quot;

},

&quot;Daten&quot;: \[

{

&quot;id&quot;: &quot;course:15067_30122_3400468&quot;,

&quot;type&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;attribute&quot;: {

&quot;completeDeadline&quot;: &quot;2026-02-24T10:50:45.000Z&quot;,

&quot;enrollmentSource&quot;: &quot;MGR_APPROVAL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;score&quot;: 0,

&quot;state&quot;: &quot;AUSSTEHENDE_GENEHMIGUNG&quot;

},

&quot;Beziehungen&quot;: {

&quot;Teilnehmer&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;3400468&quot;,

&quot;type&quot;: &quot;user&quot;

}

},

&quot;learningObject&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:15067&quot;,

&quot;type&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:15067_30122&quot;,

&quot;type&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;Daten&quot;: \[

{

&quot;id&quot;: &quot;course:15067_30122_41715_1_3400468&quot;,

&quot;type&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:1108800_1997400_3400468&quot;,

&quot;type&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;attribute&quot;: {

&quot;enrollmentSource&quot;: &quot;SELF_ENROLL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;score&quot;: 0,

&quot;state&quot;: &quot;AUSSTEHENDE_GENEHMIGUNG&quot;

},

&quot;Beziehungen&quot;: {

&quot;Teilnehmer&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;3400468&quot;,

&quot;type&quot;: &quot;user&quot;

}

},

&quot;learningObject&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:1108800&quot;,

&quot;type&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:1108800_1997400&quot;,

&quot;type&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;Daten&quot;: \[

{

&quot;id&quot;: &quot;course:1108800_1997400_2174574_0_3400468&quot;,

&quot;type&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:2027668_3707328_3400468&quot;,

&quot;type&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;attribute&quot;: {

&quot;enrollmentSource&quot;: &quot;MGR_APPROVAL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;score&quot;: 0,

&quot;state&quot;: &quot;AUSSTEHENDE_GENEHMIGUNG&quot;

},

&quot;Beziehungen&quot;: {

&quot;Teilnehmer&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;3400468&quot;,

&quot;type&quot;: &quot;user&quot;

}

},

&quot;learningObject&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:2027668&quot;,

&quot;type&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:2027668_3707328&quot;,

&quot;type&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;Daten&quot;: \[

{

&quot;id&quot;: &quot;course:2027668_3707328_2665897_0_3400468&quot;,

&quot;type&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:2030067_3709862_3400468&quot;,

&quot;type&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;attribute&quot;: {

&quot;enrollmentSource&quot;: &quot;MGR_APPROVAL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;score&quot;: 0,

&quot;state&quot;: &quot;AUSSTEHENDE_GENEHMIGUNG&quot;

},

&quot;Beziehungen&quot;: {

&quot;Teilnehmer&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;3400468&quot;,

&quot;type&quot;: &quot;user&quot;

}

},

&quot;learningObject&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:2030067&quot;,

&quot;type&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:2030067_3709862&quot;,

&quot;type&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;Daten&quot;: \[

{

&quot;id&quot;: &quot;course:2030067_3709862_2668467_0_3400468&quot;,

&quot;type&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:3081896_5749155_3400468&quot;,

&quot;type&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;attribute&quot;: {

&quot;enrollmentSource&quot;: &quot;MGR_APPROVAL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;score&quot;: 0,

&quot;state&quot;: &quot;AUSSTEHENDE_GENEHMIGUNG&quot;

},

&quot;Beziehungen&quot;: {

&quot;Teilnehmer&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;3400468&quot;,

&quot;type&quot;: &quot;user&quot;

}

},

&quot;learningObject&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:3081896&quot;,

&quot;type&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:3081896_5749155&quot;,

&quot;type&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;Daten&quot;: \[

{

&quot;id&quot;: &quot;course:3081896_5749155_3737554_0_3400468&quot;,

&quot;type&quot;: &quot;learningObjectResourceGrade&quot;

},

{

&quot;id&quot;: &quot;course:3081896_5749155_3737555_0_3400468&quot;,

&quot;type&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:2037893_3717940_3400468&quot;,

&quot;type&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;attribute&quot;: {

&quot;enrollmentSource&quot;: &quot;MGR_APPROVAL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;score&quot;: 0,

&quot;state&quot;: &quot;AUSSTEHENDE_GENEHMIGUNG&quot;

},

&quot;Beziehungen&quot;: {

&quot;Teilnehmer&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;3400468&quot;,

&quot;type&quot;: &quot;user&quot;

}

},

&quot;learningObject&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:2037893&quot;,

&quot;type&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:2037893_3717940&quot;,

&quot;type&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;Daten&quot;: \[

{

&quot;id&quot;: &quot;course:2037893_3717940_3676856_0_3400468&quot;,

&quot;type&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:3049434_5713130_3400468&quot;,

&quot;type&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;attribute&quot;: {

&quot;completeDeadline&quot;: &quot;2020-05-05T18:29:59.000Z&quot;,

&quot;enrollmentSource&quot;: &quot;MGR_APPROVAL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;score&quot;: 0,

&quot;state&quot;: &quot;AUSSTEHENDE_GENEHMIGUNG&quot;

},

&quot;Beziehungen&quot;: {

&quot;Teilnehmer&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;3400468&quot;,

&quot;type&quot;: &quot;user&quot;

}

},

&quot;learningObject&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:3049434&quot;,

&quot;type&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:3049434_5713130&quot;,

&quot;type&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;Daten&quot;: \[

{

&quot;id&quot;: &quot;course:3049434_5713130_3693595_0_3400468&quot;,

&quot;type&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:2001397_3679403_3400468&quot;,

&quot;type&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;attribute&quot;: {

&quot;enrollmentSource&quot;: &quot;MGR_APPROVAL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;score&quot;: 0,

&quot;state&quot;: &quot;AUSSTEHENDE_GENEHMIGUNG&quot;

},

&quot;Beziehungen&quot;: {

&quot;Teilnehmer&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;3400468&quot;,

&quot;type&quot;: &quot;user&quot;

}

},

&quot;learningObject&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:2001397&quot;,

&quot;type&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:2001397_3679403&quot;,

&quot;type&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;Daten&quot;: \[

{

&quot;id&quot;: &quot;course:2001397_3679403_2635974_0_3400468&quot;,

&quot;type&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:2037862_3717900_3400468&quot;,

&quot;type&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;attribute&quot;: {

&quot;enrollmentSource&quot;: &quot;MGR_APPROVAL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;score&quot;: 0,

&quot;state&quot;: &quot;AUSSTEHENDE_GENEHMIGUNG&quot;

},

&quot;Beziehungen&quot;: {

&quot;Teilnehmer&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;3400468&quot;,

&quot;type&quot;: &quot;user&quot;

}

},

&quot;learningObject&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:2037862&quot;,

&quot;type&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:2037862_3717900&quot;,

&quot;type&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;Daten&quot;: \[

{

&quot;id&quot;: &quot;course:2037862_3717900_3676816_0_3400468&quot;,

&quot;type&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

},

{

&quot;id&quot;: &quot;course:2037837_3717863_3400468&quot;,

&quot;type&quot;: &quot;learningObjectInstanceEnrollment&quot;,

&quot;attribute&quot;: {

&quot;completeDeadline&quot;: &quot;2020-02-29T18:29:59.000Z&quot;,

&quot;enrollmentSource&quot;: &quot;SELF_ENROLL&quot;,

&quot;hasPassed&quot;: false,

&quot;progressPercent&quot;: 0,

&quot;score&quot;: 0,

&quot;state&quot;: &quot;SONSTIGES&quot;

},

&quot;Beziehungen&quot;: {

&quot;Teilnehmer&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;3400468&quot;,

&quot;type&quot;: &quot;user&quot;

}

},

&quot;learningObject&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:2037837&quot;,

&quot;type&quot;: &quot;learningObject&quot;

}

},

&quot;loInstance&quot;: {

&quot;Daten&quot;: {

&quot;id&quot;: &quot;course:2037837_3717863&quot;,

&quot;type&quot;: &quot;learningObjectInstance&quot;

}

},

&quot;loResourceGrades&quot;: {

&quot;Daten&quot;: \[

{

&quot;id&quot;: &quot;course:2037837_3717863_3597363_0_3400468&quot;,

&quot;type&quot;: &quot;learningObjectResourceGrade&quot;

}

\]

}

}

}

\]

}

## Letztes Zugriffsdatum für die Lernpfadregistrierung {#api-last-access-date-lp-enrollment}

Mit Adobe Learning Manager können Sie benutzerdefinierte Metadaten, wie z. B. das Datum des letzten Zugriffs, bei einer Lernpfadregistrierung speichern. Sie legen die Metadaten über die API fest und lesen sie. Auf diese Weise können Sie den zeitgebundenen Zugriff auf zugewiesene Lernpfade verfolgen.

## Wissenswertes zu Metadaten für die Lernpfadregistrierung

Sie können bereits ein Datum für den letzten Zugriff auf eine Kursregistrierung über die API festlegen. Dieses Datum bestimmt, wie lange ein Teilnehmer auf den Kurs zugreifen kann. Registrierungen für Lernpfade unterstützen jetzt ein generisches Metadatenfeld, sodass Sie das Datum des letzten Zugriffs oder einen anderen Wert speichern können, den Sie nachverfolgen möchten.

Sie müssen das Feld nicht aktivieren oder eine spezielle Kopfzeile senden. Das Feld ist leer, bis Sie es festgelegt haben.

>[!NOTE]
>
>Die Metadaten dienen deinem eigenen Tracking. Adobe Learning Manager aktualisiert es nicht, wenn Teilnehmer einen Lernpfad oder seine Kurse öffnen, und es hat keine Kontrolle über den Zugriff auf den Lernpfad. Es wird auch nicht an die Kurse im Pfad weitergegeben. Jeder Kurs behält sein eigenes Datum für den letzten Zugriff, sodass Kurse im selben Pfad unterschiedliche Daten haben können. Verwalten Sie das Ablaufdatum des Zugriffs auf Kursebene weiterhin separat.

### Metadatenregeln {#metadata-rules}

* Der Wert muss ein JSON-Objekt sein. Eine Zeichenfolge, eine Zahl, ein Boolesche Wert oder ein Array gibt einen 400-Fehler mit der Meldung `metadata must be a JSON object` zurück.
* Sie können alle Tasten verwenden. Adobe Learning Manager validiert keine Schlüssel oder Werte und erzwingt kein Datumsformat. Die Beispiele in diesem Artikel verwenden Epochen-Millisekunden, das gleiche Format wie Kursdaten.
* Eine PATCH-Anforderung ersetzt das gesamte Metadatenobjekt. Es wird nicht mit vorhandenen Werten zusammengeführt, sodass Schlüssel, die Sie auslassen, entfernt werden.
* Durch die Einstellung &quot;`"metadata": null`&quot; werden alle Metadaten gelöscht und 200 zurückgegeben.
* Bei einer Anforderung mit einem leeren `attributes`-Objekt oder ohne `metadata`-Schlüssel bleiben die gespeicherten Metadaten unverändert.
* Wenn keine Metadaten festgelegt wurden oder nachdem Sie sie gelöscht haben, wird der Schlüssel &quot;`metadata`&quot; nicht in der Antwort angezeigt.

## Metadaten für eine vorhandene Registrierung festlegen

Verwenden Sie ein Admin-Token.

Senden Sie eine PATCH-Anforderung an den folgenden Endpunkt, wobei `{enrollmentId}` die Registrierungs-ID für den Lernpfad im Format `learningProgram:<lpId><instanceId><userId>` ist:

```
PATCH /primeapi/v2/users/{userId}/enrollments/{enrollmentId}
```

Verwenden Sie diesen Anforderungstext:

```json
{
  "data": {
    "id": "<enrollmentId>",
    "type": "learningObjectInstanceEnrollment",
    "attributes": {
      "metadata": {
        "lastAccessDate": 1745337600000
      }
    }
  }
}
```

### Metadaten festlegen, wenn Sie einen Teilnehmer registrieren

Verwenden Sie ein Admin-Token.

Senden Sie eine POST mit dem Lernpfad und den Instanz-IDs. Fügen Sie ein optionales `metadata`-Objekt in den Anforderungstext ein.

```
POST /primeapi/v2/users/{userId}/enrollments?loId=<lpId>&loInstanceId=<instanceId>
```

* Wenn `metadata` kein JSON-Objekt ist, gibt die Anforderung 400 zurück, und der Benutzer ist nicht registriert.
* Wenn der Benutzer bereits registriert ist, gibt die Anforderung 200 zurück und ändert nichts. Um Metadaten für eine bestehende Registrierung zu ändern, verwenden Sie die PATCH-Anforderung.
* Die Antwort enthält nicht die Metadaten. Sende eine GET-Anfrage, um sie zu lesen.

### Metadaten abrufen

Sie können Metadaten mit einem Administrator- oder einem Teilnehmer-Token abrufen. Die Anforderungen unterscheiden sich je nach Tokentyp.

| Token | Eine Registrierung erhalten | Liste der Registrierungen für Lernpfade |
|---|---|---|
| Administration | `GET /primeapi/v2/users/{userId}/enrollments/{enrollmentId}` | `GET /primeapi/v2/users/{userId}/enrollments?filter.loTypes=learningProgram` |
| Teilnehmer | `GET /primeapi/v2/enrollments/{enrollmentId}`<br>`GET /primeapi/v2/learningObjects/{id}?include=enrollment` | `GET /primeapi/v2/enrollments?filter.loTypes=learningProgram` |

>[!NOTE]
>
>Der `include=enrollment`-Parameter funktioniert nur mit einem Teilnehmertoken. Es wird für die Administratorrolle nicht unterstützt.

Die Antwort gibt das `metadata`-Objekt mit der Lernpfadregistrierung zurück.

### Metadaten in Headless- und externen Portalen verwenden

Externe Portale und Integrationen verwenden die gleichen API-Aufrufe. Verwenden Sie die Anforderung, die mit dem Token übereinstimmt, das Ihr Portal verwendet.

* **Wert in Ihrem Portal anzeigen:** Senden Sie die GET-Anforderung für Ihren Tokentyp aus der Tabelle oben und lesen Sie das `metadata`-Objekt aus der Antwort.
* **Aktualisieren Sie den Wert von einem externen System, z. B. einer Commerce-Plattform:** Senden Sie die PATCH-Anforderung mit einem Admin-Token.

## Job-API: Exportieren von Report Builder-Berichten mit generateCustomReport {#api-job-report-builder-exports}

Die Adobe Learning Manager-Version vom Dezember 2026 fügt der Job-API den neuen Auftragstyp &quot;`generateCustomReport`&quot; hinzu. Verwenden Sie diese Option, um alle Berichte, die Sie in Report Builder erstellt haben, automatisch zu exportieren, indem Sie die Berichts-ID übergeben.

In Kombination mit dem neuen L2-Quizdatensatz in der Report Builder können Sie jetzt:

* Exportieren Sie Quizdaten auf Fragenebene (L2) über mehrere Kurse und Module in einem einzelnen Bericht, anstatt `generateQuizReport` einmal für jeden Kurs auszuführen.
* Automatisieren Sie wiederkehrende Exporte, z. B. einen täglichen inkrementellen Export in Ihr Data Warehouse oder BI-Tool.

Vorhandene Auftragstypen, einschließlich `generateQuizReport`, bleiben unverändert.

### Vorbereitung

* Sie müssen Administrator sein. Der Auftragstyp &quot;`generateCustomReport`&quot; ist für andere Rollen nicht verfügbar.
* Erstellen und speichern Sie den Bericht zuerst im Report Builder. Erstellen Sie für L2-Quizdaten den Bericht aus dem L2-Quizdatensatz und fügen Sie die erforderlichen Felder auf Frageebene ein, z. B. Fragentext, Teilnehmerantwort, Punktzahl, Versuchsnummer und Antwortdatum.
* Notieren Sie sich die Bericht-ID. Sie übergeben sie in der Anforderung als `reportId`.

### Job erstellen

**Endpunkt**

```
POST /primeapi/v2/jobs
```

**Anforderungstext**

```json
{
  "data": {
    "type": "job",
    "attributes": {
      "description": "Daily L2 quiz export",
      "jobType": "generateCustomReport",
      "payload": {
        "reportId": "1478"
      }
    }
  }
}
```

**Attribute**

| Attribut | Erforderlich | Beschreibung |
|---|---|---|
| `jobType` | Ja | Muss `generateCustomReport` sein. |
| `payload.reportId` | Ja | Die ID des gespeicherten Report Builder-Berichts als Zeichenfolge. Muss eine positive Ganzzahl sein, die als Zeichenfolge übergeben wird, z. B. `"1478"`. Wenn Sie eine Zahl, 0, einen negativen, einen dezimalen oder einen leeren Wert senden, wird ein Fehler zurückgegeben. |
| `description` | Nein | Eine Beschreibung Ihrer Berufswahl. |
| `callbackUrl` | Nein | Eine URL, die aufgerufen werden soll, wenn der Auftrag abgeschlossen ist. Funktioniert genauso wie bei anderen Auftragstypen. |
| `payload.filters` | Nein | Siehe den Abschnitt unten. |

### Datumsfilter überschreiben (optional) {#override-date-filter}

```json
"payload": {
  "reportId": "1478",
  "filters": [
    { "columnName": "L2 Quiz - Response - Timestamp", "operator": "gte", "val": "2026-11-15T00:00:00.000Z" }
  ]
}
```

* Der gespeicherte Datumsfilter des Berichts wird nur für diese Ausführung ersetzt. Der Export umfasst `val` (einschließlich) bis zur Ausführung des Auftrags.
* `columnName` verwendet das Format `<Dataset name> - <Field name>`. Es muss mit einem Datumsfilter übereinstimmen, der bereits im Bericht vorhanden ist. Groß- und Kleinschreibung werden nicht beachtet, aber Abstand und Bindestriche müssen exakt übereinstimmen.
* `operator` ist optional und nur `gte` ist zulässig.
* `val` ist eine UTC-Zeit nach ISO 8601 innerhalb der letzten 7 Tage. Die Zeiten werden auf die Sekunde verkürzt.
* Sie können mehrere Spalten überschreiben. Eine leere Liste bedeutet, dass die gespeicherten Filter verwendet werden.
* Anwendungsfall: einem täglichen inkrementellen Export, der dort beginnt, wo der vorherige beendet wurde.

### Beim Erstellen eines Auftrags werden Fehler zurückgegeben

| Ursache | Nachricht |
|---|---|
| `reportId` fehlt | `reportId is required` |
| `reportId` ist keine positive Ganzzahl. | `reportId must be a positive integer string` |
| Datum nicht im ISO-Format | `filters.val must be in ISO format, e.g. 2020-01-01T18:30:00.000Z` |
| Datum älter als 7 Tage oder in Zukunft | `filters.val must be within the last 7 days` |
| Operator außer `gte` | `filters.operator must be gte` |
| Gleiche Spalte zweimal angegeben | `Duplicate filter column: <column>` |
| Spalte ist kein Filter im Bericht | `Unsupported custom report filter column: <column>` |
| Ein Auftrag für denselben Bericht wird noch ausgeführt | `There exists an similar job with id = <jobId> which has not finished yet` |

Beim Ausführen des Auftrags werden nur Probleme mit der gespeicherten Berichtsdefinition erkannt. In diesem Fall wird der Auftragsstatus zu `Failed`, und es wird kein Grund zurückgegeben.

### Berichtsanforderungen

Der Auftrag schlägt mit einer Fehlermeldung fehl, wenn der Bericht die folgenden Bedingungen nicht erfüllt:

* Die Berichtsdefinition enthält einen relativen Datumsfilter, z. B. letzte 7 Tage.
* Jeder Datumsfilter im Bericht darf maximal 7 Tage umfassen und nicht nur einen.
* Feste Datumsbereiche mit einem festgelegten Start- und Enddatum werden nicht unterstützt und der Auftrag schlägt fehl.
* Ein Bericht ohne Datumsfilter schlägt fehl. Dies schließt Berichte ein, die auf Datasets basieren, die kein Datumsfeld aufweisen.

>[!NOTE]
>
>Die POST wird sofort validiert. Eine ungültige Anforderung wird mit HTTP 400 abgelehnt. Der Grund hierfür ist `source.info`.

### Überprüfen Sie den Auftragsstatus und laden Sie den Bericht herunter.

**Endpunkt**

```
GET /primeapi/v2/jobs/{jobId}
```

Die Antwort verwendet dieselbe Struktur wie andere Auftragstypen. Wenn der Auftrag abgeschlossen ist, ist `status.code` `Completed` und `status.data.s3Url` enthält den Download-Link.

```json
{
  "data": {
    "type": "job",
    "id": "12345",
    "attributes": {
      "jobType": "generateCustomReport",
      "payload": {
        "reportId": "1478"
      },
      "status": {
        "code": "Completed",
        "data": {
          "s3Url": "valid for 7 days"
        }
      }
    }
  }
}
```

Die API gibt `Submitted`, `Completed` und `Failed` zurück. Die Datei ist eine einzelne CSV mit dem Namen &quot;`report.csv`&quot;.

>[!NOTE]
>
>Die Download-URL ist sieben Tage lang gültig. Laden Sie die Datei herunter, sobald der Auftrag abgeschlossen ist.

>[!IMPORTANT]
>
>Jeder mit diesem Link kann die Datei herunterladen, ohne sich anzumelden. Behandeln Sie die Verknüpfung genauso wie die darin enthaltenen Daten.

**Fehler bei Auftragsbeispiel**

```json
"status": { "code": "Failed" }
```

### Einschränkungen

Es kann jeweils nur ein `generateCustomReport`-Auftrag für einen Bericht ausgeführt werden. Eine zweite Anforderung wird abgelehnt, bis die erste abgeschlossen ist.

### Ausgabe des L2-Quizberichts

Wenn Sie einen Bericht aus dem L2-Quizdataset im Report Builder erstellen und ihn mit `generateCustomReport` exportieren, weist die Ausgabe folgende Eigenschaften auf:

* Die Ausgabe ist eine einzelne CSV-Datei mit dem Namen &quot;`report.csv`&quot;. Das Modul ist eine Spalte in der Datei. Wenn Sie einen Kurs auswählen, gibt der Bericht nur seine Quizmodule zurück.
* Jede Zeile stellt die Antwort eines Teilnehmers auf eine Frage in einem Versuch dar.
* Die Daten werden im Standardintervall für den Report Builder (ungefähr alle 15 Minuten) aktualisiert.
* Datums- und Uhrzeitwerte befinden sich in der Zeitzone Ihres Kontos. Die Spaltenüberschrift zeigt die Zeitzone an, z. B. `L2 Quiz - Response - Timestamp (America/Argentina/Salta)`.

### Felder im L2-Quizdatensatz

| Kategorie | Felder |
|---|---|
| Teilnehmer | Benutzer-ID |
| Kurs | Kurs-ID, Kursinstanzkennung, Kursname |
| Modul | Modul-ID, Modulname, Modulversion |
| Frage | Fragen-ID, Fragentext, Richtige Antwort, Interaktionstyp |
| Antwort | Antwort Antwort, erreichte Punktzahl, höchstmögliche Punktzahl, ist korrekt, Antwortzeitstempel |
| Versuchen | Versuchsnr. |

>[!NOTE]
>
>Der L2-Quizdatensatz ist nicht mit anderen Report Builder-Datensätzen verknüpft. Teilnehmername, E-Mail, Manager und benutzerdefinierte Attribute sind in diesem Bericht nicht verfügbar. Um eine Zeile einem Teilnehmer zuzuordnen, verwenden Sie die Benutzer-ID.

Sie können auch Berichte exportieren, die auf anderen Report Builder-Datensätzen mit `generateCustomReport` erstellt wurden. Welche Felder in der Ausgabe verfügbar sind, hängt vom Dataset ab.

## APIs zum Erstellen und Verwalten der Zoom-Verbindung

Verwenden Sie diese APIs zum Verwalten von Zoom-Verbindungen in Adobe Learning Manager. Sie können vorhandene Verbindungen abrufen, Zoom-Anmeldedaten speichern, Verbindungen erstellen oder aktualisieren, Zugriffsberechtigungen für Benutzergruppen und benutzerdefinierte Rollen konfigurieren und eine Verbindung aktivieren oder deaktivieren.

### Zoom-Verbindung-APIs einrichten

Das Einrichten und Verwalten einer Zoom-Verbindung erfordert vier API-Aufrufe. Legen Sie sie in dieser Reihenfolge an:

| Schritt | API | Zweck |
|---|---|---|
| 1 | `POST /ctr/authcred/uuid/20012` | Speichert die Zoom-Anmeldedaten. |
| 2 | `POST /ctr/app/esconnect` | Erstellt die Zoom-Verbindung oder aktualisiert eine vorhandene Verbindung. |
| 3 | `PUT /ctr/xtsa/{connectionId}/access` | Legt die Benutzergruppen und benutzerdefinierten Rollen fest, die die Verbindung verwenden können. |
| 4 | `POST /ctr/xtsas/{connectionId}/enable` | Aktiviert oder deaktiviert die Verbindung. |

>[!NOTE]
>
>Diese APIs verwenden die angemeldete Integrations-Admin-Sitzung. Sie verwenden keinen API-Schlüssel oder kein OAuth-Token.

### Basis-URL und Konventionen

Die Zoom Verbindung-APIs verwenden die folgenden Konventionen:

| Element | Wert |
|---|---|
| Basis-URL | `https://learningmanagerstage1.adobe.com` |
| Inhaltstyp | `application/json` |
| Authentifizierung | Sitzung eines angemeldeten Integrationsadministrators |
| Erforderliche Kopfzeilen | `content-type`, `accept`, `x-acap-caller-role: ROLE_INTEGRATIONADMIN`, `x-csrf-token` und `Cookie` |
| UUID des Integrationskatalogs für Zoom | `20012` |
| Verbindungslimit | 50 Zoomverbindungen |

Der `x-csrf-token`-Wert ist als `csrfToken` in der HTML der Integrations-Admin-Seite eingebettet. Der `Cookie`-Header enthält die Sitzungs-Cookies des angemeldeten Administrators.

### Vorbereitung

- Melden Sie sich als Integrationsadministrator an.
- Erstellen Sie eine Zoom Server-zu-Server OAuth-App. Notieren Sie sich die Client-ID, den Client-Schlüssel und die Konto-ID. Sie benötigen auch die E-Mail-Adresse des Zoom Super-Administrators.
- Rufen Sie `GET /ctr/xtsas/canCreateAccount/25` an. Es wird `true` zurückgegeben, wenn Sie eine weitere Zoom-Verbindung erstellen können.

### Schritt 1: Zoom-Anmeldedaten speichern {#save-credentials}

Rufen Sie diese API auf, bevor Sie eine Verbindung erstellen oder aktualisieren. Es speichert die Anmeldeinformationen, die die Verbindung verwendet, um eine Verbindung mit Zoom herzustellen.

```
POST /ctr/authcred/uuid/20012
```

Um eine vorhandene Verbindung zu aktualisieren, fügen Sie den Abfrageparameter &quot;`connectionId`&quot; hinzu:

```
POST /ctr/authcred/uuid/20012?connectionId={connectionId}
```

Der Anforderungstext besteht aus den Anmeldeinformationen als JSON-Text. Es handelt sich um eine JSON-Zeichenfolge, die JSON enthält, kein verschachteltes Objekt. Schließen Sie die äußeren Anführungszeichen ein.

| Schlüssel | Beschreibung |
|---|---|
| `clientId` | Die Client-ID der Zoom-App. |
| `clientSecret` | Das Client-Geheimnis der Zoom-App. Dieser Wert ist sensibel. |
| `accountId` | Die Zoom-Konto-ID. |
| `superAdmin` | Die E-Mail-Adresse des Zoom Super-Administrators. |

Beispiel für Anforderungstext:

```
"{\"clientId\":\"<ZOOM_CLIENT_ID>\", \"clientSecret\":\"<ZOOM_CLIENT_SECRET>\", \"accountId\":\"<ZOOM_ACCOUNT_ID>\", \"superAdmin\":\"<ADMIN_EMAIL>\"}"
```

Beispiel für `200 OK`-Antwort:

```json
{
  "code": 0,
  "description": "Success"
}
```

`code: 0` bedeutet, dass die Anmeldeinformationen gespeichert wurden.

### Schritt 2: Erstellen oder Aktualisieren der Zoom-Verbindung {#create-connection}

Diese API erstellt eine Zoom-Verbindung. Derselbe Endpunkt aktualisiert auch eine vorhandene Verbindung.

```
POST /ctr/app/esconnect
```

Der Anforderungstext enthält die folgenden Felder:

| Feld | Erforderlich | Beschreibung |
|---|---|---|
| `UUID` | Ja | Die UUID des Integrationskatalogs. Verwenden Sie `20012` für Zoom. |
| `listOfConnections` | Ja | Die zu erstellenden Verbindungen. Senden Sie ein Element. |
| `listOfConnections[].name` | Ja | Der Anzeigename der Verbindung, z. B. `Zoom_Partner_X`. |
| `listOfConnections[].tag` | Ja | Eine leere Zeichenfolge (`""`) wird gesendet, wenn Sie eine Verbindung erstellen. Lassen Sie es aus, wenn Sie eines aktualisieren. |
| `listOfConnections[].credentialsJson` | Ja | Die Anmeldeinformationen als JSON-Text. Verwenden Sie dieselbe Zeichenfolge, die Sie in Schritt 1 gesendet haben. |
| `listOfConnections[].schedules` | Ja | Der Synchronisierungszeitplan. Senden Sie `objectUUID` 10002, `priority` 1 und `type` 1. |
| `listOfConnections[].id` | Nur aktualisieren | Die ID der zu aktualisierenden Verbindung, z. B. `3474737`. |

Beispiel für Anforderungstext:

```json
{
  "UUID": 20012,
  "listOfConnections": [
    {
      "name": "Zoom_Example",
      "tag": "",
      "credentialsJson": "{\"clientId\":\"<ZOOM_CLIENT_ID>\", \"clientSecret\":\"<ZOOM_CLIENT_SECRET>\", \"accountId\":\"<ZOOM_ACCOUNT_ID>\", \"superAdmin\":\"<ADMIN_EMAIL>\"}",
      "schedules": [
        { "objectUUID": 10002, "priority": 1, "type": 1 }
      ]
    }
  ]
}
```

Beispiel für `200 OK`-Antwort:

```json
[3474737]
```

Die Antwort ist ein JSON-Array, das die ID der neuen Verbindung enthält. Verwenden Sie diese ID in den Schritten 3 und 4 und in allen Folgeaufrufen.

### Vergleich erstellen und aktualisieren

| Differenz | Erstellen | Update |
|---|---|---|
| `listOfConnections[].id` | Nicht gesendet | Die Verbindungs-ID |
| `listOfConnections[].tag` | `""` | Nicht gesendet |
| Berechtigungsaufruf in Schritt 1 | `POST /ctr/authcred/uuid/20012` | `POST /ctr/authcred/uuid/20012?connectionId={id}` |

### Schritt 3: Festlegen, wer die Verbindung verwenden darf {#set-access}

Diese API definiert, welche Benutzergruppen und benutzerdefinierten Rollen die Verbindung verwenden können.

```
PUT /ctr/xtsa/{connectionId}/access
```

Der Pfad verwendet für eine Verbindung das Singular &quot;`xtsa`&quot;. Der Plural `xtsas` ist die Sammlung von Verbindungen.

Der Anforderungstext ist ein JSON-Array. Jedes Element gewährt Zugriff auf eine Benutzergruppe oder eine benutzerdefinierte Rolle.

| Feld | Erforderlich | Beschreibung |
|---|---|---|
| `accessType` | Ja | `USER_GROUP` oder `CUSTOM_ROLE`. |
| `accessId` | Ja | Die ID der Benutzergruppe oder der benutzerdefinierten Rolle als Zeichenfolge. |

Beispiel für Anforderungstext:

```json
[
  { "accessType": "USER_GROUP", "accessId": "<groupId>" },
  { "accessType": "CUSTOM_ROLE", "accessId": "<roleId>" }
]
```

Die API gibt `204 No Content` ohne Text zurück, wenn die Zugriffsliste gespeichert wird.

>[!NOTE]
>
>Die Anforderung ersetzt die gesamte Zugriffsliste. Es hängt nicht daran an. Alles, was nicht im Körper ist, verliert den Zugang. Um alle Zugriffe zu entfernen, senden Sie ein leeres Array (`[]`).

### Schritt 4: Verbindung aktivieren oder deaktivieren {#enable-disable}

Diese API aktiviert oder deaktiviert eine Verbindung. Verwenden Sie sie, nachdem Sie die Verbindung erstellt haben, wann immer Sie ihren Status ändern müssen.

```
POST /ctr/xtsas/{connectionId}/enable
```

Der Pfad verwendet die Mehrzahl `xtsas`, wie die Aufrufe zum Auflisten und Löschen. Der Zugriffsaufruf in Schritt 3 verwendet den Singular `xtsa`.

| Path-Parameter | Typ | Beschreibung |
|---|---|---|
| `connectionId` | Zahl | Die ID der Verbindung. Es handelt sich um die von `GET /ctr/xtsas` zurückgegebene `id` und die in Schritt 2 zurückgegebene ID. |

Der Anforderungstext enthält die folgenden Felder:

| Feld | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `objectUUID` | Zahl | Ja | Das Synchronisierungsobjekt der Verbindung. Verwenden Sie `10002`, denselben Wert, den Sie in `schedules[].objectUUID` in Schritt 2 gesendet haben. |
| `operation` | Zahl | Ja | `1` senden. |
| `val` | Boolesche Wert | Ja | Der neue Status der Verbindung. Senden Sie `false`, um die Verbindung zu deaktivieren. Senden Sie `true`, um es zu aktivieren. |

Beispiel für eine Anforderung zum Deaktivieren einer Verbindung:

```json
{
  "objectUUID": 10002,
  "operation": 1,
  "val": false
}
```

Beispiel für einen Anforderungstext zum Aktivieren einer Verbindung:

```json
{
  "objectUUID": 10002,
  "operation": 1,
  "val": true
}
```

Beispielanforderung zum Deaktivieren einer Verbindung:

```bash
curl -X POST 'https://learningmanagerstage1.adobe.com/ctr/xtsas/<connectionId>/enable' \
  -H 'accept: application/json' \
  -H 'content-type: application/json' \
  -H 'x-acap-caller-role: ROLE_INTEGRATIONADMIN' \
  -H 'x-csrf-token: <CSRF_TOKEN>' \
  -H 'Cookie: <SESSION_COOKIES>' \
  --data '{"objectUUID":10002,"operation":1,"val":false}'
```

Rufen Sie zum Bestätigen des neuen Status &quot;`GET /ctr/xtsas`&quot; an, suchen Sie die Verbindung durch &quot;`id`&quot; und überprüfen Sie das Flag &quot;`enabled`&quot;.

>[!NOTE]
>
>Die `x-acap-caller-role`-Kopfzeile muss mit der Rolle des aktiven Profils übereinstimmen. Verwenden Sie für diese APIs `ROLE_INTEGRATIONADMIN`.

### Verbindung nach der Erstellung verwalten

Sie können die folgenden Aufrufe mit der Verbindungs-ID verwenden:

| Zweck | Anruf |
|---|---|
| Aktivieren oder Deaktivieren einer Verbindung | `POST /ctr/xtsas/{connectionId}/enable` |
| Zugriffsliste einer Verbindung lesen | `GET /ctr/xtsa/{connectionId}/access` |
| Lesezugriff für alle Zoom-Verbindungen | `GET /ctr/xtsas/access?UUID=20012` |
| Alle Verbindungen auflisten. Zoomverbindungen haben `extsysRefId` 25. | `GET /ctr/xtsas` |
| Verbindung anzeigen | `GET /ctr/app/connection/{id}/object/10002` |
| Verbindung endgültig löschen | `DELETE /ctr/xtsas/{id}` |

>[!NOTE]
>
>Der View-Aufruf gibt den Client-Schlüssel im Klartext zurück. Behandeln Sie den Client-Schlüssel als sensibel, und drehen Sie ihn, wenn er gelegt wird. Übertragen oder teilen Sie keine Sitzungs-Cookies, CSRF-Token oder Anmeldeinformationen, auch nicht in HAR-Dateien und kopierten cURL-Befehlen.

### Verwenden Sie diese APIs in Ihrer Integration

Ein häufiger Anwendungsfall ist das automatische Einrichten einer Zoom-Verbindung für ein neues Konto oder einen neuen Partner.

1. Rufen Sie `GET /ctr/xtsas/canCreateAccount/25` an, um zu bestätigen, dass Sie eine weitere Verbindung erstellen können.
2. Rufen Sie `POST /ctr/authcred/uuid/20012` mit den Zoom-Anmeldedaten an.
3. Rufen Sie &quot;`POST /ctr/app/esconnect`&quot; mit dem Namen der Verbindung, der gleichen Anmeldeinformationszeichenfolge und dem Synchronisierungszeitplan auf. Lesen Sie die Verbindungs-ID aus der Antwort.
4. Rufen Sie `PUT /ctr/xtsa/{connectionId}/access` mit den Benutzergruppen und benutzerdefinierten Rollen auf, die die Verbindung verwenden können.
5. Rufen Sie `POST /ctr/xtsas/{connectionId}/enable` mit `val` auf `true` oder `false` an, um die Verbindung zu aktivieren oder zu deaktivieren. Rufen Sie dann &quot;`GET /ctr/xtsas`&quot; an und überprüfen Sie das Flag &quot;`enabled`&quot;, um den Status zu bestätigen.
6. Um die Anmeldeinformationen später zu ändern, wiederholen Sie die Schritte 2 und 3 mit der Verbindungs-ID.



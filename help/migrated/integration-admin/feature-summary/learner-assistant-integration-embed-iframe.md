---
description: Erfahren Sie, wie Sie den Teilnehmer-Assistenten mithilfe eines iframe in Ihre App einbetten, einschließlich Einrichtung, Konfiguration und Ereignisbehandlung
jcr-language: en_us
title: Integrieren des Teilnehmerassistenten durch Einbetten von iFrame
source-git-commit: 1549a4592b7a930631dcff6b2e75ec3a3d4f5592
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 2%

---


# Einbetten des Teilnehmerassistenten mit einem iframe

## Übersicht

Adobe Learning Manager (ALM)-Benutzer können den **Teilnehmerassistenten** direkt in ihre eigenen Anwendungen für Teilnehmer einbetten (z. B. benutzerdefinierte Portale, LMS-Frontends, Lernzentren usw.) Verwenden einer Standard-HTML `<iframe>`.

Wenn der Teilnehmerassistent über iFrame eingebettet ist, bietet er Zugriff auf alle Funktionen des Teilnehmerassistenten, einschließlich:

* Orchestrator
* Antwort-Agent
* Knowledge Agent
* Lernpfad-Agent

>[!IMPORTANT]
>
>Durch die iFrame-Einbettung hat Ihre Anwendung vollen Zugriff auf die zugrunde liegenden Agenten des Teilnehmerassistenten. Ihre Anwendung (die &quot;übergeordnete App&quot;) ist jedoch für die Verarbeitung aller Ereignisse verantwortlich, die der Assistent ausgibt. Wenn ein Teilnehmer beispielsweise auf ein Zitat oder einen Kurslink in der Antwort des Assistenten klickt, gibt der Assistent ein Ereignis aus, und die übergeordnete Anwendung muss dieses Ereignis behandeln und die eigentliche Navigation ausführen. Der Teilnehmer-Assistent navigiert nicht im Namen Ihrer Anwendung.

## Voraussetzungen

Voraussetzungen:

* Ein ALM-Mandant mit aktiviertem Teilnehmerassistenten. Konfigurieren Sie die erforderlichen Kataloge auf der Seite &quot;Administratoreinstellungen&quot;.
* Ein gültiges Zugriffstoken zum Authentifizieren der Teilnehmer- (oder Admin-) Sitzung. Befolgen Sie zum Generieren eines Zugriffstokens die Anweisungen auf der Seite [Authentifizierung mit OAuth 2.0](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual#authentication-using-oauth-20). Die Seite enthält die Schritte, die zur Authentifizierung und Generierung des Zugriffstokens erforderlich sind, um fortzufahren.
* Die Möglichkeit, eine `<iframe>` in Ihre Anwendung einzubetten und mit ihr über die postMessage-API des Browsers zu kommunizieren.
* Front-End-Code der übergeordneten Anwendung, da die Anwendung auf Meldungen vom eingebetteten iFrame achten und darauf reagieren muss.

## Konfigurationsparameter für den Lern-Assistenten

| Parametername | Wert | Beschreibung |
|---|---|---|
| hostName | learningmanager.adobe.com | Gibt die Hostdomäne für die Anwendung an. |
| accessToken | token123 (tatsächliches Zugriffstoken) | Token zur Authentifizierung und Autorisierung der Benutzersitzung. |

## iFrame initialisieren

Übergeben Sie die Konfiguration über die postMessage-API an den Teilnehmer-Assistenten, indem Sie einen eingebetteten iFrame-Konfigurations-Handshake verwenden.

1. Die übergeordnete Anwendung bettet den Lernassistenten als `<iframe>` ein.
2. Wenn keine URL-basierte Konfiguration gefunden wird, sendet der Lernassistent ein ALM_CHAT_REQUEST_CONFIG-Ereignis an die übergeordnete Anwendung.
3. Die übergeordnete Anwendung reagiert mit einem ALM_CHAT_CONFIG-Ereignis, das die Nutzdatenkonfiguration enthält. Beispiel:

   ```json
   {
     "hostName": "learningmanager.adobe.com",
     "accessToken": "token123",
     "openByDefault": false,
     "isAdmin": false
   }
   ```

4. Nach erfolgreicher Initialisierung wird der Teilnehmerassistent gerendert und kann verwendet werden.

## iFrame-Ereigniszusammenfassung

Der Teilnehmerassistent und die übergeordnete Anwendung kommunizieren über postMessage-Ereignisse in beide Richtungen.

### Ausgehende Ereignisse (Teilnehmerassistent iFrame in übergeordnete App)

| Ereignisname | Beschreibung | Übergebene Parameter |
|---|---|---|
| ALM_CHAT_OPEN | Wird ausgelöst, wenn der Chat geöffnet wird. | -- |
| ALM_CHAT_CLOSED | Wird ausgelöst, wenn der Chat geschlossen wird. | -- |
| ALM_CHAT_LO_REDIRECT | Navigieren Sie zur personalisierten Lernpfad-Übersichtsseite. | loId, loType, instanceId |
| ALM_CHAT_URL_REDIRECT | Wird ausgelöst, wenn in der Chat-Nachricht auf einen externen Link geklickt wird. | url |
| ALM_CHAT_REQUEST_CONFIG | Fordert die Konfiguration von der übergeordneten Anwendung an. | -- |
| ALM_CHAT_WAITING_FOR_REPLY | Gibt an, dass der Assistent eine Anforderung verarbeitet oder auf eine Antwort wartet. | isWaitingForReply |
| ALM_CHAT_PERSONALIZED_PATH_CREATED | Wird ausgelöst, wenn ein Lernpfad gespeichert wird. | -- |

### Eingehende Ereignisse (übergeordnete App für Teilnehmerassistenten)

| Ereignisname | Beschreibung | Nutzlast |
|---|---|---|
| ALM_CHAT_CONFIG | Sendet die zur Initialisierung des Assistenten erforderliche Konfigurationsnutzlast. | Konfigurationsobjekt |
| ALM_CHAT_OPEN | Öffnet den Teilnehmer-Assistenten. | Ohne |
| ALM_CHAT_CLOSE | Schließt den Teilnehmer-Assistenten. | Ohne |
| ASK_AI_ASSISTANT_QUERY | Öffnet das Chat-Fenster und sendet eine Abfrage an den Assistenten. | { Abfrage: &quot;Fragentext&quot; } |

## Anforderungen an die Ereignisbehandlung in der übergeordneten Anwendung

Durch das Einbetten des Teilnehmerassistenten über iFrame wird er nicht zu einem vollständig eigenständigen Widget. Ihre übergeordnete Anwendung muss ausgehende Ereignisse aktiv überwachen und die entsprechende Aktion ausführen. Ihre Bewerbung sollte mindestens folgende Anforderungen erfüllen:

* Auf ALM_CHAT_REQUEST_CONFIG achten und mit ALM_CHAT_CONFIG antworten, damit der Assistent initialisiert werden kann.
* Handle ALM_CHAT_LO_REDIRECT: Wenn ein Teilnehmer auf eine Zitat- oder Quelldatei in der Antwort des Assistenten klickt, erhält Ihre Anwendung die loId, loType und instanceId und ist dafür verantwortlich, dass der Teilnehmer zum richtigen Kurs oder Lernobjekt navigiert.
* Handle ALM_CHAT_URL_REDIRECT: Wenn ein Teilnehmer auf einen externen Link in einer Chat-Nachricht klickt, erhält Ihre Anwendung die URL und ist für das Öffnen oder Navigieren zu dieser verantwortlich (z. B. auf einer neuen Registerkarte).
* Optional können Sie ALM_CHAT_OPENED / ALM_CHAT_CLOSED / ALM_CHAT_WAITING_FOR_REPLY nachverfolgen, um den Status des Assistenten in Ihrer eigenen Benutzeroberfläche widerzuspiegeln (z. B. Anzeigen einer Ladeanzeige, während isWaitingForReply auf &quot;true&quot; gesetzt ist).
* Optional können Sie ALM_CHAT_OPEN / ALM_CHAT_CLOSE / ASK_AI_ASSISTANT_QUERY verwenden, um den Assistenten programmgesteuert zu steuern. Öffnen Sie beispielsweise den Assistenten und füllen Sie eine Abfrage über eine **Hilfe**-Schaltfläche an einer anderen Stelle in Ihrer Anwendung aus.

## Benötigen Sie Hilfe?

Wenden Sie sich an Ihren Adobe Customer Success Manager, um eine technische exemplarische Vorgehensweise einzurichten.

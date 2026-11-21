---
description: Erfahren Sie, wie Kursleiter und Kohortenmanager E-Mail-Digests der Diskussions-Dashboard-Aktivität erhalten und wie Sie Einstellungen und Abonnenten mit APIs verwalten.
jcr-language: en_us
title: Diskussions-Dashboard - Kursleiterbenachrichtigungen
exl-id: 370c9add-5572-4555-8a95-ddb470c230f4
source-git-commit: 650ec8159a4291189dfc38b03701b7b96932233d
workflow-type: tm+mt
source-wordcount: '1231'
ht-degree: 0%
---

# Diskussions-Dashboard - Kursleiterbenachrichtigungen

## Übersicht

Benachrichtigungen für Diskussions-Dashboard-Kursleiter geben Kursleitern, Kohortenmanagern und Administratoren eine E-Mail-Übersicht über die neuesten Aktivitäten in den von ihnen überwachten Diskussions-Dashboards. Dies ist hilfreich für Kursleiter, die mehrere Kohorten verwalten und gleichzeitig an mehreren Boards teilnehmen.

Ein Kohortenmanager ist die Person, die eine Gruppe von Teilnehmern (eine Kohorte) verwaltet, die einen Kurs oder ein Programm gemeinsam nach demselben Zeitplan durchlaufen.

Anstatt jedes Board einzeln zu öffnen, erhalten Kursleiter in Echtzeit In-App-Warnungen und eine E-Mail-Übersicht über die Boards, die sie abonniert haben, in der von Ihnen konfigurierten Häufigkeit. Sie verwalten Board-Abonnements und Benachrichtigungseinstellungen über die [`boardSubscriptionSettings`-API](api-changes-dec-2026.md#api-sequence) und die [Abonnenten-API](api-changes-dec-2026.md#api-get-subscribers).

## Wichtigste Funktionen

* Sie können aktive Adobe Learning Manager-Benutzer für ausgewählte Diskussionsrunden abonnieren, indem Sie die Abonnenten-API ([`POST /boards/{id}/subscribers`](api-changes-dec-2026.md#api-subscribe-users), Bereich `admin:write`) verwenden. Ein Benutzer muss Zugriff auf das Board haben, wenn Benachrichtigungen gesendet werden.
* Benutzer erhalten in Echtzeit In-App-Benachrichtigungen zu aktivierten Ereignistypen und eine E-Mail-Auswahl, die nach Board gruppiert ist. Die Ereignistypen werden durch Einstellungen auf Kontoebene (`notifyNewPost`, `notifyComment` und `notifyReply`) in der [`boardSubscriptionSettings`-API &#x200B;](api-changes-dec-2026.md#api-sequence) gesteuert.
* Das Digest-Fenster ist der Zeitraum, in dem die Aktivität in einer Digest-E-Mail erfasst wird. Sie legen es auf Kontoebene mit dem `digestFrequencyHours`-Attribut von 1 bis 168 Stunden fest (z. B. 24 Stunden für eine tägliche Auswertung). Es gilt für alle Benutzer im Konto.
* Sie können Benutzer nach Benutzer-ID oder E-Mail-Adresse abonnieren und mehrere Benutzer in einer Anforderung hinzufügen ([Massenabonnements](api-changes-dec-2026.md#bulk-subscriptions)). Benutzer werden im Lern-Manager zuerst auf die übliche Weise erstellt.
* In der Auswahl-E-Mail werden alle neuen Beiträge, Kommentare und Antworten zu den aktivierten Ereignistypen mit dem Boardnamen, dem Namen des Autors und der E-Mail-Adresse sowie einem direkten Link aufgelistet. Außerdem wird die Anzahl der Aktualisierungen seit dem Beginn der Übersichtsphase angezeigt.
* Die `boardSubscriptionSettings`-API und die Abonnenten-API sind öffentliche APIs, sodass Sie Einstellungen und Abonnements ohne Benutzeroberfläche verwalten können (API-gesteuerte Integrationen).

## Anwendungsszenarien

Die folgenden Anwendungsfälle zeigen, wie Kursleiterbenachrichtigungen helfen:

| Anwendungsfall | So unterstützt die Benachrichtigung |
|---|---|
| Überwachen mehrerer Kohorten | Ein Kursleiter, der für mehrere Kohorten verantwortlich ist, kann von den Boards, die mit diesen Kohorten verknüpft sind, zusammengefasste Aktivitäten erhalten. |
| Interaktion der Teilnehmer überprüfen | Ein Kohortenmanager kann neue Beiträge überwachen und aktive Diskussionen identifizieren, ohne jedes Board separat zu überprüfen. |
| Nachverfolgung von Unterhaltungen | Kommentare und Antworten, die in der Auswahl enthalten sind, helfen Kursleitern, Diskussionen zu identifizieren, die Beratung oder Moderation erfordern. |

## Wichtige Überlegungen

* Ein Benutzer muss auf ein Board zugreifen können, wenn eine Benachrichtigung gesendet wird. Der Zugriff wird zum Zeitpunkt der Auslieferung erneut überprüft, nicht nur, wenn der Benutzer abonniert ist. Wenn ein Abonnent den Zugriff auf ein Board verliert, wird das Abonnement beibehalten, Benachrichtigungen für dieses Board werden jedoch übersprungen.
* Der Digest wird als eine E-Mail gesendet, sodass ein belegtes Board ihn sehr lang machen kann. Zum Beispiel könnte eine Kohorte von etwa 40 Teilnehmern in sechs Stunden mehrere Hundert Kommentare posten.
* Wenn Ihre Boards sehr aktiv sind, verwenden Sie eine kürzere Übersichtshäufigkeit, z. B. alle sechs Stunden, damit jede E-Mail verwaltbar bleibt. Legen Sie die Häufigkeit mit &quot;`digestFrequencyHours`&quot; in der [`boardSubscriptionSettings`-API &quot;](api-changes-dec-2026.md#api-create-settings)&quot; fest.
* Die Anzahl der Beiträge im E-Mail-Digest ist auf 20 pro Board und Digest beschränkt. Die gleiche Obergrenze gilt unabhängig für Kommentare (20) und Antworten (20) pro Board. Nur die angezeigten Listen werden abgeschnitten. Die Anzahl der Überschriften/Unterüberschriften spiegelt immer die wahre, nicht abgeschnittene Aktivität für das Fenster wider.
* Die Anzahl der Abonnenten ist auf 200 pro Board begrenzt.
* Da der Inhalt direkt in der E-Mail und nicht als Anhang gesendet wird, gilt für den Text der E-Mail auch eine Größenbeschränkung.

## Abonnementmodell, Berechtigungen und Berechtigung

* Ein Abonnent ist ein Benutzer, der Benachrichtigungen von einem Board erhält. Ein Board-Abonnement ist unabhängig von der bestehenden Follow-Beziehung zum Board-Benutzer.
* Jeder, der sich bei OAuth authentifiziert und über die Bereiche `admin:read` und `admin:write` verfügt, kann die Abonnementeinstellungen und Abonnenten-APIs verwenden. Mit `admin:read` können Sie Abonnenten auflisten und Einstellungen lesen. Mit `admin:write` können Sie Abonnenten hinzufügen oder entfernen und die Einstellungen ändern.
* Sie können jeden Learning Manager-Benutzer abonnieren, aber der Benutzer muss vorhanden sein, aktiv sein und Zugriff auf das Board haben, um Benachrichtigungen zu erhalten. Der Zugriff wird erneut überprüft, wenn Benachrichtigungen und Digests gesendet werden.
* Wenn ein Benutzer den Zugriff verliert, wird die Übermittlung für dieses Board übersprungen und das Abonnement wird beibehalten. Die Bereitstellung wird fortgesetzt, wenn der Zugriff zurückkehrt.
* Sie können einem Board in einer Anforderung mehrere Benutzer hinzufügen (Massenabonnements). Wenn ein Benutzer bereits abonniert ist, ist die Anforderung weiterhin erfolgreich und es wird kein Duplikat erstellt. Weitere Informationen zum Anforderungsformat, zur 207-Antwort mit mehreren Status sowie zu den Fehlerfällen finden Sie unter [Massenabonnements](api-changes-dec-2026.md#bulk-subscriptions).

## Inhalt der Zusammenfassung

### Enthaltene Ereignisse

Der Digest enthält neue Beiträge, Kommentare und Antworten, wenn die entsprechende Einstellung `true` in der [`boardSubscriptionSettings`-API &#x200B;](api-changes-dec-2026.md#api-create-settings) ist: `notifyNewPost`, `notifyComment` und `notifyReply` Sie legen diese mit `POST` oder `PATCH /boardSubscriptionSettings` fest. Alle Einstellungen sind standardmäßig `false`.

### Ausgeschlossene Ereignisse

Der Digest schließt Ereignisse aus, deren Zuordnungseinstellung in der [`boardSubscriptionSettings`-API &#x200B;](api-changes-dec-2026.md#api-create-settings) (z. B. `notifyComment`) `false` ist. Es wird kein Digest gesendet, wenn keine zulässige Aktivität vorhanden ist.

### Beispiel für Auswahl-E-Mail-Layout

Für jedes abonnierte Board, das berechtigt war, eine Auswahl-E-Mail zu senden. Sie ist wie folgt strukturiert:

* **Zusammenfassungszeile:** Die E-Mail wird mit der Gesamtzahl der Aktualisierungen im Board (z. B. sieben Aktualisierungen) und einer Aufschlüsselung nach Typ (z. B. neue Beiträge und Kommentare) zusammen mit der Zeit geöffnet, ab der die Aktivität gezählt wird.
* **Board-Abschnitt:** Aktivität ist unter dem Board-Namen gruppiert. Jeder Beitrag ist darunter aufgeführt.
* **Elementdetails:** Jeder Beitrag, Kommentar oder jede Antwort enthält den Namen und die E-Mail-Adresse des Benutzers, der ihn erstellt hat, sowie einen Link zum Element.
* **Links:** Wenn Sie einen Link auswählen, wird der Beitrag, der Kommentar oder die Antwort direkt geöffnet. Der Empfänger muss angemeldet sein, damit der Link geöffnet werden kann.
* **Kommentare und Antworten:** Diese werden in derselben E-Mail wie Beiträge angezeigt, sodass Kursleiter Nachbesprechungen zusammen mit neuen Themen sehen können.

## Benachrichtigungen konfigurieren

### Einstellungen mithilfe von APIs konfigurieren

Sie verwalten Benachrichtigungen über zwei öffentliche APIs: die [`boardSubscriptionSettings`-API &#x200B;](api-changes-dec-2026.md#api-sequence), die auf Kontoebene gilt, und die [-Abonnenten-API &#x200B;](api-changes-dec-2026.md#api-get-subscribers), die pro Board gilt. Beide verwenden die OAuth-Geltungsbereiche `admin:read` und `admin:write`. Rufen Sie sie in dieser Sequenz auf:

1. Legen Sie die Einstellungen auf Kontoebene mit [`POST /boardSubscriptionSettings`](api-changes-dec-2026.md#api-create-settings) fest.
1. Ändern Sie die Einstellungen später bei Bedarf mit [`PATCH /boardSubscriptionSettings`](api-changes-dec-2026.md#api-update-settings).
1. Rufen Sie die Einstellungen auf Kontoebene mit [`GET /boardSubscriptionSettings`](api-changes-dec-2026.md#api-get-settings) ab.
1. Listen Sie die Benutzer auf, die ein Board mit [`GET /boards/{id}/subscribers`](api-changes-dec-2026.md#api-get-subscribers) abonniert haben.
1. Abonnieren Sie Benutzer für ein Board mit [`POST /boards/{id}/subscribers`](api-changes-dec-2026.md#api-subscribe-users).
1. Abbestellen eines Benutzers für ein Board mit [`DELETE /boards/{id}/subscribers/{userId}`](api-changes-dec-2026.md#api-unsubscribe-user).

Verwenden Sie die `boardSubscriptionSettings`-API, um die Übersichtshäufigkeit in Stunden festzulegen und Beiträge, Kommentare und Antworten für die Übersichtsseite zu aktivieren oder zu deaktivieren. Beispiel: Ein Konto mit einer Digest-Häufigkeit von 1 Stunde erhält jede Stunde eine Digest-E-Mail. Alle Ereigniseinstellungen sind standardmäßig `false`.

### Abonnenten verwalten

Verwenden Sie die Abonnenten-API, um auszuwählen, welche aktiven Learning Manager-Benutzer welche Boards abonnieren. Ein Abonnement ist unabhängig von der bestehenden Board-Follow-Beziehung. Ein Benutzer muss für ein Board sichtbar sein, um seine Benachrichtigungen zu erhalten, was bedeutet, dass der Benutzer angemeldet sein sollte. Der Verlust der Sichtbarkeit unterdrückt die Bereitstellung, entfernt aber nicht das Abonnement.

### Funktion aktivieren

Um Kursleiterbenachrichtigungen zu aktivieren, erstellen Sie die Einstellungen auf Kontoebene und abonnieren Sie dann Benutzer für Boards, wie in [API-Änderungen in Nov 2026](api-changes-dec-2026.md) beschrieben. Danach sammelt das System neue Beiträge, Kommentare und Antworten, die während des konfigurierten Intervalls erstellt wurden. Nach Ablauf des Intervalls erhalten die Abonnenten eine zusammengefasste Benachrichtigung über die förderfähigen Aktivitäten in den teilnehmenden Boards.

Weitere Informationen zu den API-Änderungen in [API-Änderungen im Dezember 2026](api-changes-dec-2026.md).

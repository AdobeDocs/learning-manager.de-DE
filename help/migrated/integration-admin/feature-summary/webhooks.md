---
jcr-language: en_us
title: Webhooks
description: Erfahren Sie mehr über Webhooks zum Senden von Echtzeitinformationen wie Kursanmeldungen, Kurserstellung und andere Informationen an eine bestimmte URL
contentowner: chandrum
source-git-commit: e4b0526e11083d116bf4ca4b0816892e0e8f0f9d
workflow-type: tm+mt
source-wordcount: '1695'
ht-degree: 1%

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

## Echtzeit-Events.

| S.No | Webhook-Ereignisse | Beschreibung |
|---|---|---|
| 1 | CI_STATS | Wird ausgelöst, wenn sich die Verfügbarkeit von Lizenzen oder Wartelisten für eine Kursinstanz ändert. |
| 2 | COURSE_ENROLLMENT | Wird ausgelöst, wenn sich ein Teilnehmer für einen Kurs registriert. |
| 3 | COURSE_COMPLETED | Wird ausgelöst, wenn ein Teilnehmer einen Kurs abschließt. |
| 4 | LEARNING_PATH_ENROLLMENT | Wird ausgelöst, wenn sich ein Teilnehmer für einen Lernpfad registriert. |
| 5 | LEARNING_PATH_COMPLETED | Wird ausgelöst, wenn ein Teilnehmer einen Lernpfad abschließt. |
| 6 | CERTIFICATION_ENROLLMENT | Wird ausgelöst, wenn sich ein Teilnehmer für eine Zertifizierung registriert. |
| 7 | CERTIFICATION_COMPLETED | Wird ausgelöst, wenn ein Teilnehmer eine Zertifizierung abschließt. |
| 8 | COURSE_UNENROLLMENT | Wird ausgelöst, wenn ein Teilnehmer die Registrierung für einen Kurs widerruft. |
| 9 | LEARNING_PATH_UNENROLLMENT | Wird ausgelöst, wenn ein Teilnehmer die Registrierung für einen Lernpfad widerruft. |
| 10 | CERTIFICATION_UNENROLLMENT | Wird ausgelöst, wenn ein Teilnehmer die Registrierung für eine Zertifizierung widerruft. |
| 11 | LEARNING_OBJECT_DRAFT | Wird während der Erstellung eines Lernobjekts im Entwurfsstatus ausgelöst. |
| 12 | LEARNING_OBJECT_DELETION | Wird beim Löschen eines Lernobjekts ausgelöst. |
| 13 | LEARNING_OBJECT_MODIFICATION | Wird während der Änderung eines Lernobjekts ausgelöst. |
| 14 | LEARNING_OBJECT_INSTANCE_MODIFICATION | Wird während der Erstellung oder Änderung einer Lernobjektinstanz ausgelöst.<div><b>Hinweis:</b> Es wird empfohlen, Kursinstanzen erst nach Veröffentlichung des Kurses zu verwenden.</div> |
| 15 | LEARNING_OBJECT_INSTANCE_DELETION | Wird beim Löschen einer Lernobjektinstanz ausgelöst. |

## Ereignisse, die nicht in Echtzeit erfolgen

| S.No | Webhook-Ereignisse | Beschreibung |
|---|---|---|
| 1 | COURSE_ENROLLMENT_BATCH | Wird ausgelöst, wenn ein Administrator/Manager/eine Plattform Teilnehmer für einen Kurs registriert. |
| 2 | COURSE_COMPLETED_BATCH | Wird ausgelöst, wenn ein Administrator/Manager/eine Plattform einen Kurs als abgeschlossen markiert. |
| 3 | LEARNING_PATH_ENROLLMENT_BATCH | Wird ausgelöst, wenn ein Administrator/Manager/eine Plattform Teilnehmer für einen Lernpfad registriert. |
| 4 | LEARNING_PATH_COMPLETED_BATCH | Wird ausgelöst, wenn ein Administrator/Manager einen Lernpfad als abgeschlossen markiert. |
| 5 | CERTIFICATION_ENROLLMENT_BATCH | Wird ausgelöst, wenn ein Administrator/Manager/eine Plattform Teilnehmer für eine Zertifizierung registriert. |
| 6 | CERTIFICATION_COMPLETED_BATCH | Wird ausgelöst, wenn ein Administrator/Manager/eine Plattform eine Zertifizierung als abgeschlossen markiert. |
| 7 | LEARNER_PROGRESS | Verfolgt den Fortschritt eines Teilnehmers nach Abschluss eines Moduls. |
| 8 | COURSE_UNENROLLMENT_BATCH | Wird ausgelöst, wenn ein Administrator/Manager/eine Plattform die Registrierung von Teilnehmern für einen Kurs aufhebt. |
| 9 | LEARNING_PATH_UNENROLLMENT_BATCH | Wird ausgelöst, wenn ein Administrator/Manager/eine Plattform die Registrierung von Teilnehmern für einen Lernpfad aufhebt. |
| 10 | CERTIFICATION_UNENROLLMENT_BATCH | Wird ausgelöst, wenn ein Administrator/Manager/eine Plattform die Registrierung von Teilnehmern für eine Zertifizierung aufhebt. |
| 11 | LEARNING_OBJECT_MODIFICATION_BATCH | Wird während der Änderung eines Lernobjekts über den Migrationsarbeitsablauf ausgelöst. |
| 12 | LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH | Wird während der Erstellung oder Änderung einer Lernobjektinstanz über den Migrations-Workflow ausgelöst. |

## Best Practices für Webhooks

Webhooks ermöglichen ereignisgesteuerte Kommunikation zwischen Diensten in Echtzeit. Eine unsachgemäße Implementierung kann jedoch zu verlorenen Ereignissen, langsamer Systemleistung oder Sicherheitsrisiken führen. Im Folgenden finden Sie die Best Practices zur Implementierung von Webhooks, die sich auf Fehlertoleranz, Zuverlässigkeit und Sicherheit konzentrieren.

### Fehlertoleranz

Die Fehlertoleranz des ALM-Webhook-Systems gibt Abonnenten Empfehlungen zur Handhabung potenzieller Probleme, wie z. B. Ereignisverlust, doppelte Ereignisse und Auslieferung.

Für ALM ist das Verbindungszeitlimit auf 10 Sekunden und das Socket-Zeitlimit auf 5 Sekunden konfiguriert. Es wird erwartet, dass der Client die Nachricht bestätigt, sobald er sie erhält. Dadurch wird sichergestellt, dass der Client beim Verarbeiten von Nachrichten nicht verzögert. Falls eine nachgelagerte Verarbeitung zeitaufwendig ist, sollte der Client das Ereignis dennoch sofort bestätigen und die nachgelagerte Verarbeitung dann an ihrem Ende abwickeln.

#### Datenaufbewahrung

Die Veranstaltungen dauern 7 Tage. Wenn sie nicht innerhalb dieser Zeit verarbeitet werden, gehen sie dauerhaft verloren. Wenn die Wiederherstellung am letzten Tag erfolgt und mehr Zeit benötigt wird, verlängert das System die Aufbewahrungsfrist nicht.
Wenn Ereignisse schneller erzeugt werden, als sie verbraucht werden, können einige Ereignisse verloren gehen. Obwohl dies ungewöhnlich ist, sollten die Abonnenten überwachen, um zu verhindern, dass es zu einem langfristigen Problem wird.

#### Webhooks deaktivieren

Wenn ein Abonnent nicht auf Webhook-Ereignisse reagiert, versucht das ALM-System Webhooks mit exponentiellem Backoff erneut, um eine Überlastung des Abonnenten zu vermeiden.

Der Wiederholungsprozess beginnt mit einem anfänglichen Intervall von 5 Sekunden. Wenn der Abonnent nicht reagiert, verdoppelt sich die Wartezeit auf 10, 20, 40 und 80 Sekunden und steigt schließlich auf maximal 5 Minuten. Wenn die 5-minütige Aufbewahrungszeit erreicht ist, versucht das System weiterhin alle 5 Minuten erneut, bis die 7-tägige Aufbewahrungsfrist abgelaufen ist. Wenn der Abonnent während dieses gesamten Zeitraums immer noch nicht reagiert, wird der Webhook automatisch deaktiviert. In regelmäßigen Abständen wird eine Erinnerungs-E-Mail an den Abonnenten gesendet.

#### Ereignisse duplizieren

Wenn die Reaktionszeit eines Abonnenten nach der Verarbeitung eines Ereignisses mehr als 5 Sekunden beträgt, versucht das System möglicherweise erneut, dieses Ereignis zu verarbeiten. Es wird empfohlen, Ereignis-IDs zu verwenden, um den Überblick darüber zu behalten, welche Ereignisse bereits verarbeitet wurden. Wenn der Webhook nach dem Senden des Ereignisses abstürzt, aber bevor die Verarbeitung gespeichert wurde, kann dieselbe Gruppe von Ereignissen erneut versucht werden. Es wird empfohlen, Batch-IDs oder individuelle Ereignis-IDs zu verwenden, um Duplikate zu erkennen und zu ignorieren.

#### Nicht geordnete Ereignisse

ALM versucht, Ereignisse in der richtigen Reihenfolge zu halten, aber manchmal können Ereignisse auch außerhalb der Reihenfolge ausgeliefert werden, insbesondere zwischen Echtzeit- und Nicht-Echtzeit-Ereignissen.

Wenn ein Administrator mehrere Teilnehmer gleichzeitig für einen Kurs registriert, werden die Registrierungsereignisse als nicht in Echtzeit markiert. Wenn ein Teilnehmer den Kurs jedoch schnell abschließt, wird dieses Abschlussereignis als Echtzeit markiert und kann vor den Registrierungsereignissen bereitgestellt werden.

#### Empfehlung für Fehlertoleranz

Um diese Fehler zu vermeiden, sollten Abonnenten Webhook-Ereignisse aktiv überwachen und Warnungen für Probleme wie verpasste Ereignisse, doppelte Lieferungen oder nicht geordnete Sequenzen einrichten.

## Spezifische Richtlinien für Webhook-Ereignisse

1. Wenn Sie zuerst ein LEARNER_PROGRESS-Ereignis erhalten, ignorieren Sie die unten aufgeführten Ereignisse:

   * COURSE_ENROLLMENT
   * COURSE_ENROLLMENT_BATCH
   * LEARNING_PATH_ENROLLMENT
   * LEARNING_PATH_ENROLLMENT_BATCH
   * CERTIFICATION_ENROLLMENT
   * CERTIFICATION_ENROLLMENT_BATCH

2. Ignorieren Sie das Ereignis LEARNER_PROGRESS, wenn es nach den folgenden Ereignissen eintritt:

   * COURSE_COMPLETED
   * COURSE_COMPLETED_BATCH
   * LEARNING_PATH_COMPLETED
   * LEARNING_PATH_COMPLETED_BATCH
   * CERTIFICATION_COMPLETED
   * CERTIFICATION_COMPLETED_BATCH

3. Legen Sie mithilfe des Zeitstempelfelds fest, ob das Ereignis mit Ausnahme des Ereignisses LEARNER_PROGRESS ignoriert oder verarbeitet werden soll.


## Beispiel-Payloads für die Ereignisse

+++CI_STATS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "01234567-0458-4450-b5dd-6bc1edr4560",
      "eventName": "CI_STATS",
      "timestamp": 1725604147,
      "eventInfo": "1725604145-LoSt",
      "data": {
        "loInstanceId": "course:1234567_123456775",
        "waitlistCount": 0,
        "enrollmentCount": 10,
        "seatLimit": 30
      }
    }
  ]
}
```

+++

+++COURSE_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "29123ec1-4576-4ec5-a057-3a6dr45t9d6",
      "eventName": "COURSE_ENROLLMENT",
      "timestamp": 1725524713,
      "eventInfo": "1725524713000-040366-10488-0",
      "data": {
        "userId": 1234567,
        "loId": "course:1234567",
        "loInstanceId": "course:1234567_1234567",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": 1725524713
      }
    }
  ]
  }
```

+++

+++COURSE_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "29572ec1-4576-4ec5-a057-3wsd43r59d6",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": 1725524713,
      "eventInfo": "1725524713000-040366-10488-0",
      "data": {
        "userId": 1234567,
        "loId": "course:1234567",
        "loInstanceId": "course:12345678_123456788",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1725524713
      }
    }
  ]
  }
```

+++

+++COURSE_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "c1a3168c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED",
      "timestamp": 1725523823,
      "eventInfo": "1725523823000-040363-12018-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345671",
        "loInstanceId": "course:1234567_12345674",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": 1725523818,
        "hasPassed": true
      }
    }
  ]
}
```

+++

+++COURSE_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "c1a3168c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED_BATCH",
      "timestamp": 1725523823,
      "eventInfo": "1725523823000-040363-12018-0",
      "data": {
        "userId": 112345678,
        "loId": "course:12345678",
        "loInstanceId": "course:1234567_12345678",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": 1725523818,
        "hasPassed": true
      }
    }
  ]
}
```

+++

+++LEARNING_PATH_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "96ed0791-338f-4c4c-83bc-9fwfr4564965",
      "eventName": "LEARNING_PATH_ENROLLMENT",
      "timestamp": 1725604249,
      "eventInfo": "1725604248000-040653-71396-0",
      "data": {
        "userId": 11234567,
        "loId": "learningProgram:123456",
        "loInstanceId": "learningProgram:12345_134567",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": 1725604248
      }
    }
  ]
}
```

+++

+++LEARNING_PATH_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "96edft791-338f-4c4c-83bc-9f7erf94965",
      "eventName": "LEARNING_PATH_ENROLLMENT",
      "timestamp": 1725604249,
      "eventInfo": "1725604248000-040653-71396-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:12347",
        "loInstanceId": "learningProgram:12345_12345",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1725604248
      }
    }
  ]
  }
```

+++

+++LEARNING_PATH_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "e207104e-d554-4027-944b-08fty6fdddf",
      "eventName": "LEARNING_PATH_COMPLETED",
      "timestamp": 1725604392,
      "eventInfo": "1725604391000-040653-314618-0",
      "data": {
        "userId": 11080928,
        "loId": "learningProgram:12345",
        "loInstanceId": "learningProgram:12345_95662",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": 1725604380,
        "hasPassed": true
      }
    }
  ]
  }
```

+++

+++LEARNING_PATH_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "e207104e-d554-4027-944b-086debefdddf",
      "eventName": "LEARNING_PATH_COMPLETED",
      "timestamp": 1725604392,
      "eventInfo": "1725604391000-040653-314618-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:12345",
        "loInstanceId": "learningProgram:12345_95662",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": 1725604380,
        "hasPassed": true
      }
    } 
    ]
    }
```

+++

+++CERTIFICATION_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8bdfr76-148e-4128-80e9-b89123456755",
      "eventName": "CERTIFICATION_ENROLLMENT",
      "timestamp": 1725604672,
      "eventInfo": "1725604672000-040654-559128-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:1234567",
        "loInstanceId": "certification:123456_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": 1725604672
      }
    }
  ]
}
```

+++

+++CERTIFICATION_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8b2ee776-148e-4128-80e9-12345678",
      "eventName": "CERTIFICATION_ENROLLMENT_BATCH",
      "timestamp": 1725604672,
      "eventInfo": "1725604672000-040654-559128-0",
      "data": {
        "userId": 123456788,
        "loId": "certification:1234567",
        "loInstanceId": "certification:12345678_160299",
        "loType": "certification",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1725604672
      }
    }
  ]
  }
```

+++

+++CERTIFICATION_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "b8b63bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED",
      "timestamp": 1725604769,
      "eventInfo": "1725604768000-040654-756257-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:1245678",
        "loInstanceId": "certification:1234567_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": 1725604740
      }
    }
  ]
  }
```

+++

+++CERTIFICATION_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "b8b63bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED_BATCH",
      "timestamp": 1725604769,
      "eventInfo": "1725604768000-040654-756257-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:134567",
        "loInstanceId": "certification:1234567_160299",
        "loType": "certification",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": 1725604740
      }
    }
  ]
  }
```

+++

+++LEARNER_PROGRESS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "dd04d3a4-c3df-44fa-a1cf-7edd6e3d2075",
      "eventName": "LEARNER_PROGRESS",
      "timestamp": 1725604552,
      "eventInfo": "1725604551000-297002-5823-0",
      "data": {
        "loId": "course:7542090",
        "loType": "course",
        "userId": 12345678,
        "loInstanceId": "course:1234567_11234567",
        "dateStarted": 1725604380,
        "progressPercent": 50
      }
}
]
}
```

+++

+++COURSE_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "f3417817-8cb8-40ea-a441-813bec1c7724",
      "eventName": "COURSE_UNENROLLMENT",
      "timestamp": 1725515824,
      "eventInfo": "1725506253000-040298-24078-0",
      "data": {
        "userId": 12345671,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
      }
    }
  ]
}
```

+++

+++COURSE_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "f3417817-8cb8-40ea-a441-8123e45724",
      "eventName": "COURSE_UNENROLLMENT_BATCH",
      "timestamp": 1725515824,
      "eventInfo": "1725506253000-040298-24078-0",
      "data": {
        "userId": 123456781,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL"
    }
   }
  ]
}
```

+++

+++LEARNING_PATH_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8e5df878-1dfd-47ac-9bfe-7d123456d1",
      "eventName": "LEARNING_PATH_UNENROLLMENT",
      "timestamp": 1725516573,
      "eventInfo": "1725506667000-040299-28209-0",
      "data": {
        "userId": 12345678,
        "loId": "learning_program:1234567",
        "loInstanceId": "learning_program:1234567_109139",
        "loType": "learning_program",
        "enrollmentSource": "SELF_ENROLL",
       
      }
    }
]
}
```

+++

+++LEARNING_PATH_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8e5df878-1dfd-47ac-9bfe-7d4952e3edd1",
      "eventName": "LEARNING_PATH_UNENROLLMENT",
      "timestamp": 1725516573,
      "eventInfo": "1725506667000-040299-28209-0",
      "data": {
        "userId": 1234567,
        "loId": "learning_program:1234567",
        "loInstanceId": "learning_program:1234567_109139",
        "loType": "learning_program",
        "enrollmentSource": "ADMIN_ENROLL"
      }
    }
]
}
```

+++

+++CERTIFICATION_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "7902766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT",
      "timestamp": 1725517341,
      "eventInfo": "1725507900000-040304-1065-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:1234567",
        "loInstanceId": "certification:12345678_162078",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL"
      }
    }
  ]
}
```

+++

+++CERTIFICATION_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "7902766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT_BATCH",
      "timestamp": 1725517341,
      "eventInfo": "1725507900000-040304-1065-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:1234567",
        "loInstanceId": "certification:1234567_162078",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_DRAFT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1712349f-26ec-453c-b56a-cdf18a841948",
      "eventName": "LEARNING_OBJECT_DRAFT",
      "timestamp": 1725519188,
      "eventInfo": "1725519188000-040344-48604-0",
      "data": {
        "loId": "course:12345671",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_DELETION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "023456-5517-4c09-9cde-d953cdd8582c",
      "eventName": "LEARNING_OBJECT_DELETION",
      "timestamp": 1725605296,
      "eventInfo": "1234567800-040656-662792-0",
      "data": {
        "loId": "course:1234567",
        "loType": "course"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_MODIFICATION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "22345668-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION_BATCH",
      "timestamp": 1725523081,
      "eventInfo": "123456000-039736-54153-0",
      "data": {
        "loId": "learningProgram:1234567",
        "loType": "learningProgram"

      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_MODIFICATION_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "2234567068-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION_BATCH",
      "timestamp": 1725523081,
      "eventInfo": "123456700-039736-54153-0",
      "data": {
        "loId": "learningProgram:1234567",
        "loType": "learningProgram"

      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "b131da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION",
      "timestamp": 1725603298,
      "eventInfo": "1723456000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12345678_14453691",
        "loId": "course:12345678",
        "loType": "course"
        
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "b23458-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH",
      "timestamp": 1725603298,
      "eventInfo": "112345000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12345678_14453691",
        "loId": "course:1234568",
        "loType": "course"

      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_DELETION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234560-d73a-457b-83f3-666ba9654edb",
      "eventName": "LEARNING_OBJECT_INSTANCE_DELETION",
      "timestamp": 1725605491,
      "eventInfo": "17223456700-040657-236307-0",
      "data": {
        "loInstanceId": "course:1234567_14453849",
        "loId": "course:1234567",
        "loType": "course"

      }
    }
  ]
}
```

+++


---
jcr-language: en_us
title: Webhooks-Benutzerhandbuch
description: Erfahren Sie mehr über Webhooks Nutzung, Best Practices und Einschränkungen
contentowner: chandrum
exl-id: e6a63ffb-7fdd-46e4-b5e6-20ce36861cef
source-git-commit: 4b26eddf1285651a13ee9c71fdf677e8b92e6dc3
workflow-type: tm+mt
source-wordcount: '3369'
ht-degree: 1%

---

# Webhooks-Benutzerhandbuch

Webhooks sind eine Möglichkeit für Web-Anwendungen, automatisch und in Echtzeit miteinander zu kommunizieren.

Im Gegensatz zu herkömmlichen APIs, die darauf warten, dass ein Benutzer Informationen anfordert, geben Echtzeit-APIs Daten in dem Moment frei, in dem sie auftreten. Webhooks fungieren als Echtzeit-API und helfen bei der sofortigen Freigabe der Daten, wenn das angegebene Ereignis eintritt.

## Entitäten

Um Webhooks-Ereignisse zu verstehen, müssen wir zunächst die beteiligten Entitäten und die Auslöserbedingungen für diese Ereignisse kennen.

### Lernobjekte

Im Folgenden finden Sie die unterstützten Ereignisse für Lernobjekte (Kurs, Lernpfad oder Zertifizierungen).

#### Entwurf

Wenn ein Lernobjekt über die Benutzeroberfläche erstellt wird, wird es im Modus **Entwurf** gestartet. Dies bedeutet, dass das Lernobjekt noch nicht veröffentlicht ist und für die Teilnehmer nicht verfügbar ist. Das **LEARNING_OBJECT_DRAFT**-Ereignis wird ausgelöst, solange das Lernobjekt ein Entwurf bleibt. Alle nachfolgenden Aktualisierungen des Entwurfs lösen dieses Ereignis ebenfalls aus.

#### Update

Sobald das Lernobjekt veröffentlicht wurde, ändert sich sein Status von **Entwurf** in **Veröffentlicht**. Während dieses Übergangs generiert Webhook das Ereignis **LEARNING_OBJECT_MODIFICATION**, da das Lernobjekt von **Entwurf** in **Veröffentlicht** geändert wird. Alle nachfolgenden Änderungen und Aktualisierungen des LO lösen ebenfalls ein **LEARNING_OBJECT_MODIFICATION**-Ereignis aus.

Das **LEARNING_OBJECT_MODIFICATION**-Ereignis wird auch ausgelöst, wenn das Lernobjekt eingestellt wird. Dieser eingestellte Vorgang markiert die zugrunde liegenden Instanzen als aktualisiert, da diese Instanzen eingestellt werden, sobald sich das übergeordnete Lernobjekt im eingestellten Status befindet.

#### Löschen

Beim Löschen eines Lernobjekts wird das **LEARNING_OBJECT_DELETION**-Ereignis generiert. Dieses Ereignis zeigt an, dass das Lernobjekt gelöscht wurde und den Teilnehmern nicht mehr zur Verfügung steht.

Zusätzlich zu den Echtzeit-Ereignissen verfügen Lernobjektereignisse auch über ein Batch-Gegenstück (nicht in Echtzeit), das als Teil des **LEARNING_OBJECT_MODIFICATION_BATCH**-Ereignisses ausgelöst wird. Dieses Ereignis tritt während der Erstellung oder Änderung eines Lernobjekts über den Migrationsarbeitsablauf auf. Da Lernobjektentwurf- und -löschvorgänge nicht über die Migration unterstützt werden, gibt es keine entsprechenden Entwurfs- oder Löschereignisse für diese Aktionen.

### Lernobjektinstanzen

Im Folgenden finden Sie die unterstützten Ereignisse für Lernobjektinstanzen.

#### Update

Sobald eine Instanz erstellt wurde, wird das **LEARNING_OBJECT_INSTANCE_MODIFICATION**-Ereignis generiert. Lernobjektinstanzen in Adobe Learning Manager haben keinen **Draft**-Status. Daher unterstützt Adobe Learning Manager kein **LEARNING_OBJECT_INSTANCE_DRAFT-Ereignis**. Dieses Ereignis wird immer dann generiert, wenn eine Instanz erstellt, geändert oder eingestellt wird.

Dieses Ereignis wird nicht nur beim Erstellen, Aktualisieren oder Zurückziehen einer Instanz generiert, sondern auch automatisch generiert, wenn das übergeordnete Lernobjekt als **Zurückgezogen** markiert ist. Dies liegt daran, dass die zugrunde liegenden Instanzen auch als **Eingestellt** markiert werden müssen, wenn ein Lernobjekt eingestellt wird.

#### Löschen

Wenn eine Instanz gelöscht wird, wird das **LEARNING_OBJECT_INSTANCE_DELETION**-Ereignis generiert. Dieses Ereignis gilt nur für Kursinstanzen, die Module zum Selbststudium enthalten, da Administratoren in Adobe Learning Manager nur Kursinstanzen löschen können, bei denen der Modultyp zum Selbststudium dient. Adobe Learning Manager unterstützt keine expliziten Löschungen für andere Kursmodultypen, nicht für Lernpfadinstanzen oder Zertifizierungsinstanzen.

Die Lernobjektinstanz verfügt auch über ein nicht-Echtzeit-Gegenstück, das als Teil des **LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH**-Ereignisses verfügbar gemacht wird. Dieses Ereignis wird während der Erstellung oder Änderung einer Lernobjektinstanz über den Migrationsarbeitsablauf ausgelöst. Da Entwurfs- oder Löschvorgänge für Lernobjektinstanzen bei der Migration nicht unterstützt werden, sind entsprechende Entwurfs- oder Löschvorgänge nicht verfügbar.

### Registrierung

Sobald ein Teilnehmer eine Registrierungsaktion ausführt, wird ein Echtzeit-Registrierungsereignis ausgelöst. Je nach Lernobjekttyp kann das Echtzeit-Registrierungsereignis in eine der folgenden Kategorien fallen:

* COURSE_ENROLLMENT
* LEARNING_PATH_ENROLLMENT
* CERTIFICATION_ENROLLMENT

Registrierungsereignisse verfügen zusätzlich zu diesen Echtzeit-Ereignissen über Batch-Entsprechungen. Wenn eine Registrierung von einem Administrator, Manager oder einer Plattform ausgelöst wird, werden Registrierungsereignisse außerhalb der Echtzeit ausgelöst. Je nach Lernobjekttyp kann das Batch-Registrierungsereignis wie folgt aussehen:

* COURSE_ENROLLMENT_BATCH
* LEARNING_PATH_ENROLLMENT_BATCH
* CERTIFICATION_ENROLLMENT_BATCH

### Registrierung widerrufen

Wenn ein Teilnehmer eine Aktion zum Aufheben der Registrierung ausführt, wird ein Ereignis zum Aufheben der Registrierung in Echtzeit ausgelöst. Je nach Lernobjekttyp kann das Echtzeit-Abmeldeereignis in eine der folgenden Kategorien fallen:

* COURSE_UNENROLLMENT
* LEARNING_PATH_UNENROLLMENT
* CERTIFICATION_UNENROLLMENT

Zusätzlich zu diesen Ereignissen gibt es auch Ereignisse zum Aufheben der Registrierung für den Stapel. Wenn eine Abmeldung von einem Administrator, Manager oder einer Plattform markiert wird, werden Ereignisse der Abmeldung in nicht Echtzeit ausgelöst. Je nach Lernobjekttyp kann das Batch-Abmeldereignis wie folgt aussehen:

* COURSE_UNENROLLMENT_BATCH
* LEARNING_PATH_UNENROLLMENT_BATCH
* CERTIFICATION_UNENROLLMENT_BATCH

### Abschluss

Das Echtzeit-Abschlussereignis wird ausgelöst, wenn ein Teilnehmer ein Lernobjekt abschließt. Je nach Lernobjekttyp kann das Echtzeit-Abschlussereignis in eine der folgenden Kategorien fallen:

* COURSE_COMPLETED
* LEARNING_PATH_COMPLETED
* CERTIFICATION_COMPLETED

Zusätzlich zu diesen Echtzeit-Ereignissen gibt es auch Batch-Abschlussereignisse. Wenn beispielsweise ein Administrator, Manager oder eine Plattform ein Lernobjekt als abgeschlossen markiert, werden die Ereignisse für den Abschluss in Nicht-Echtzeit ausgelöst. Je nach Lernobjekttyp kann das Batch-Abschlussereignis in eine der folgenden Kategorien fallen:

* COURSE_COMPLETED_BATCH
* LEARNING_PATH_COMPLETED_BATCH
* CERTIFICATION_COMPLETED_BATCH

### Teilnehmerfortschritt

Immer wenn sich ein Teilnehmer bei einem Lernobjekt registriert und das Modul beginnt, wird sein Fortschritt verfolgt. Diese Daten sind im **LEARNER_PROGRESS**-Ereignis enthalten. Das Ereignis kann um bis zu 15 Minuten verzögert werden, da die Fortschrittsverfolgung auf einer komplexen Aggregationslogik basiert, die nicht in Echtzeit erfolgt.

### CI-Statistiken

Das **CI_STATS**-Echtzeitereignis wird ausgelöst, wenn es zu einer Änderung der Lizenz- oder Wartelistenverfügbarkeit für eine Kursinstanz kommt. Diese Daten werden nur auf Instanzebene erfasst. Darüber hinaus wird dieses Ereignis für Kurse und nicht für andere Lernpfade oder Zertifizierungen ausgelöst, da die Verfügbarkeit von Lizenzen und Wartelisten Attribute sind, die für einen Kurs und seine Instanz spezifisch sind.

## Reihenfolge der Veranstaltungen

Adobe Learning Manager stellt sicher, dass Veranstaltungen für jedes Konto sortiert werden. Bei der Korrelation von Meldungen zwischen Registrierung oder Abschluss und Fortschrittsereignissen kann es jedoch zu Abweichungen kommen. Dies geschieht, weil das Fortschrittsereignis des Teilnehmers um bis zu 15 Minuten verzögert werden kann, da die Fortschrittsverfolgung auf einer komplexen Aggregationslogik basiert, die nicht in Echtzeit erfolgt. Darüber hinaus stammen Fortschrittereignisse aus verschiedenen Datenquellen, sodass ihre Reihenfolge in Bezug auf Registrierungs- und Abschlussereignisse nicht garantiert werden kann. Daher bietet Adobe Learning Manager Kunden beim Abhören dieser Veranstaltungen Best Practices.

Wenn das Abschlussereignis vor dem Teilnehmerfortschrittsereignis eintritt, kann der Client das Teilnehmerfortschrittsereignis ignorieren. Dies liegt daran, dass das Teilnehmerfortschrittsereignis um bis zu 15 Minuten verzögert werden kann, während das Abschlussereignis ausgelöst werden kann, bevor das Fortschrittsereignis empfangen wird. Da der Empfang eines Abschlussereignisses anzeigt, dass das Lernobjekt abgeschlossen ist, bedeutet dies, dass der Fortschritt 100 % erreicht hat.

In seltenen Fällen, in denen das Registrierungsereignis nach dem Teilnehmerfortschrittsereignis eintritt, kann der Client das Registrierungsereignis ignorieren. Dies liegt daran, dass der Fortschritt nur verfolgt werden kann, nachdem sich der Teilnehmer für das Lernobjekt registriert hat. Das heißt, der Empfang eines Fortschrittsereignisses zeigt an, dass das Lernobjekt gestartet wurde, was erst nach einer erfolgreichen Registrierung erfolgt.

## Echtzeit-Events und Batch-Events.

Bestimmte Ereignisse haben wie oben erwähnt Echtzeit- und Nicht-Echtzeit-Pendants. Es kann Fragen dazu geben, wann Sie Echtzeit-Ereignisse abonnieren und wann Sie Nicht-Echtzeit-Ereignisse abonnieren. Im Folgenden finden Sie Richtlinien, die auf der Grundlage der oben beschriebenen Entitäten befolgt werden können.

### Echtzeit-Events.

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

### Ereignisse, die nicht in Echtzeit erfolgen

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

### Lernobjekte und ihre Instanzen

* Abonnieren Sie Echtzeit-Ereignisse, wenn Sie auf Änderungen an Lernobjekten achten möchten, die durch Benutzeroberflächenaktionen von Rollen wie Admin, Autor usw. vorgenommen wurden.
* Abonnieren Sie Ereignisse, die nicht in Echtzeit oder als Batch vorliegen, wenn Sie über Migrationsarbeitsabläufe vorgenommene Änderungen an Lernobjekten abhören möchten.

### Registrierung, Aufhebung der Registrierung und Abschluss

* Abonnieren Sie Echtzeit-Ereignisse, wenn Sie auf Registrierungen, Aufhebung der Registrierung oder Abschlüsse von Teilnehmern warten möchten.
* Abonnieren Sie Ereignisse, die nicht in Echtzeit oder als Batch vorliegen, wenn Sie Registrierungen, Aufhebung der Registrierung oder Abschlüsse hören möchten, die durch Admin, Manager, Plattform usw. gekennzeichnet sind.

### Teilnehmerfortschritt

* Abonnieren Sie die Veranstaltung, wenn Sie auf Fortschrittsänderungen eines Teilnehmers warten möchten.

>[!NOTE]
>
>In den oben genannten Szenarien (Registrierung, Aufhebung der Registrierung, Abschluss und Fortschritt) können die aus userId und loInstanceId bestehenden zusammengesetzten Attribute einen Datensatz eindeutig identifizieren.

### Kursinstanzstatistiken

* Abonnieren Sie das **CI_STATS**-Ereignis in Echtzeit, wenn Sie Änderungen an der Sitzplatzverfügbarkeit oder der Verfügbarkeit von Wartelisten abhören möchten.

## Webhook-Ereignis-Payload

Als Teil der Webhooks-Antwort-Nutzlast gibt Adobe Learning Manager die Attribute aus, die erforderlich sind, um eine Entität eindeutig zu identifizieren. Diese werden im gleichen Format und gemäß den von der öffentlichen API verwendeten Standards ausgegeben, um sicherzustellen, dass die Webhook-Daten mit den Daten der öffentlichen API synchronisiert sind. Zeigen Sie [Beispiel-Nutzdaten](/help/migrated/integration-admin/feature-summary/webhooks-usage-guide.md#sample-payloads-for-the-events) an, um die Nutzdaten für die verschiedenen Ereignisse anzuzeigen.

## Webhooks zum Erstellen einer externen Datenbank oder eines Benachrichtigungsdienstes verwenden

Einer der Anwendungsfälle, von denen wir gehört haben, wo Webhooks nützlich sein könnten, ist der Aufbau einer Datenbank auf Kundenseite. Adobe Learning Manager verfügt über eine eigene Datenbank und ein eigenes Schema, Kunden haben jedoch keinen Zugriff darauf.

Die Frage ist: Wie können Kunden eine Datenbank aufbauen, indem sie Ereignisse aus webhooks verwenden?

Da Adobe Learning Manager die Tabellendatensätze und das Schema nicht direkt verfügbar macht, können sich Kunden beim Erstellen einer externen Datenbank auf die Webhooks-Lösung verlassen, indem sie die Ereignisse zum Ausfüllen nutzen. In dieser Version stellen wir Ereignisse für Lernobjekte, Lernobjektinstanzen, Registrierung, Aufhebung der Registrierung, Abschluss, Fortschritt und Kursinstanzstatistiken bereit.

### Erstellen einer Datenbank aus Lernobjektereignissen

Die Lernobjektereignisse machen `loId` und `loType` verfügbar, um eine Entität zu identifizieren. Diese Attribute allein reichen jedoch nicht aus, um eine externe Lernobjektdatenbank zu erstellen. Kunden benötigen zusätzliche Felder, um das Lernobjekt weiter zu beschreiben.
Es gibt zwei Ansätze, um die zusätzlichen Daten abzurufen:

#### Generieren Sie einen Bericht zu Schulungsdaten, um alle Daten abzurufen

Dieser Ansatz sollte verwendet werden, wenn Lernobjekte in großen Mengen über Workflows wie Migration erstellt werden. Ziel ist es hier, den **[!UICONTROL Schulungsdaten]**-Bericht mit allen Lernobjekten zu generieren, die als Teil des Migrationsarbeitsablaufs aufgenommen wurden. Um den Importprozess zu optimieren, wird empfohlen, die Exportstartzeit auf den Zeitpunkt festzulegen, an dem die Migration ausgelöst wurde. Dadurch wird sichergestellt, dass nur die Lernobjekte, die über die Migration importiert wurden, in den Bericht exportiert werden, da historische Daten bereits in der Kundendatenbank verfügbar sind.

#### Abfragen der Informationen aus der öffentlichen API GET /learningObjects - Bereich &quot;Administrator&quot;

Dieser Ansatz sollte verwendet werden, wenn Lernobjekte über Echtzeit-Workflows erstellt werden. Der Kunde sollte über eine eigene Caching-Ebene verfügen, um die über die Ereignisse ausgegebenen Lernobjekte zu stapeln und dann die `GET /learningObjects`-API abzufragen, indem er diese Lernobjekt-IDs übergibt. Der Grund für eine Caching-Ebene besteht darin, sicherzustellen, dass die öffentlichen API-Ratenlimits nicht überschritten werden. Derzeit gelten für ` GET /learningObject`-APIs Administrationsgrenzwerte von 500 Anfragen pro Stunde. Wenn dieser Grenzwert überschritten wird, antwortet der öffentliche API-Dienst mit einer **HTTP 429 Too Many Requests-Nachricht**.

### Datenbank aus Lernobjektinstanz und CI_STATS-Ereignissen erstellen

Das Lernobjektinstanzereignis gibt die Attribute `loInstanceId`, `loId` und `loType` für Kurse und Lernpfade aus. Entsprechend gilt das **CI_STATS**-Ereignis nur für Kurse, da `seatLimit`, `seatAvailability`, `waitListLimit`, `waitlistAvailability` usw. nur für Kurse gelten.

In bestimmten Anwendungsfällen sind zusätzliche Instanzdaten wie Instanzname, Status usw. erforderlich. Um zusätzliche Instanzdaten abzurufen, ist der folgende Ansatz zu verfolgen:

#### Abfragen der Informationen aus &quot;public-api GET/learningobjects&quot; - Bereich &quot;Administrator&quot;

Kunden können die oben erwähnte `GET /learningObjects`-API zusammen mit den enthaltenen Instanzen verwenden, um die Informationen zu den Instanzen abzurufen. Sie sollten weiterhin den im [Abschnitt](/help/migrated/integration-admin/feature-summary/webhooks-usage-guide.md#query-the-information-from-the-public-api-get-learningobjects-admin-scope) genannten Ansatz verwenden, um sicherzustellen, dass die Höchstsätze nicht überschritten werden.


>[!NOTE]
>
>1. Zertifizierungen bieten nicht das Konzept von Instanzen in ALM.
>2. Es ist nicht erforderlich, zusätzliche Daten für CI_STATS abzurufen, da dieselben Informationen bereits als Teil der Lernobjekt-Instanzereignisse abgerufen worden wären.

### Datenbank aus Registrierungs-, Abmelde-, Abschluss- und Fortschrittsereignissen erstellen

Die Registrierung, Aufhebung der Registrierung, der Abschluss und der Fortschritt von Teilnehmern werden in Adobe Learning Manager als separate Ereignisse ausgegeben. Der Teilnehmer wird durch das `userId`-Attribut identifiziert. Es kann jedoch bestimmte Szenarien geben, in denen zusätzliche Teilnehmerinformationen wie Name, E-Mail usw. für nachgelagerte Workflows auf der Kundenseite erforderlich sind. Um diese Daten abzurufen, können Kunden den unten beschriebenen Ansatz verwenden:

#### Benutzerbericht von Administrator oder Connectors exportieren

Dieser Ansatz sollte immer dann verfolgt werden, wenn Massenarbeitsabläufe involviert sind, z. B. Massenregistrierung, Massenentregistrierung usw. Der Benutzerbericht aus Adobe Learning Manager enthält alle Informationen zu einem Benutzer. Durch Korrelieren der `userId`, die vom Webhook-Ereignis abgerufen wurde, können Kunden diesen Bericht nachschlagen (der auf Kundenseite als Datenbank, Cache oder API-Endpunkt verfügbar gemacht werden kann), um zusätzliche Details wie Name, E-Mail, UUID usw. abzurufen. Dieser Ansatz kann verwendet werden, um Benutzer wöchentlich oder täglich zu synchronisieren.

#### Abfragen von Informationen aus öffentlichen API-GET /users - Umfang des Administrators

Dieser Ansatz kann verfolgt werden, wenn die Benutzer im oben genannten Bericht nicht verfügbar sind. Die Kombination der Ansätze 1 und 2 stellt sicher, dass alle vorhandenen Benutzer, die in der Vergangenheit erstellt wurden, vom **[!UICONTROL Benutzerbericht]** abgedeckt werden können, während neu erstellte Benutzer weiterhin von der API abgerufen werden können. Wenn der **[!UICONTROL Benutzerbericht]** nicht über die Daten verfügt, kann der Kunde die Benutzer-IDs als Eingabeargumente an die `GET /users`-API senden, um Benutzerinformationen abzurufen. Diese Informationen sollten auf Kundenseite zwischengespeichert werden, um wiederholte Aufrufe der öffentlichen API für dieselbe Gruppe von Benutzern zu verhindern. Bitte beachten Sie, dass die Admin-Rate für GET/users-APIs derzeit auf 500 Anfragen pro Stunde festgelegt ist. Alle Anforderungen, die diesen Grenzwert überschreiten, führen zu einer Antwort von **HTTP 429 Too Many Requests**.

## Fehlertoleranz

Die Fehlertoleranz des ALM-Webhook-Systems gibt Abonnenten Empfehlungen zur Handhabung potenzieller Probleme, wie z. B. Ereignisverlust, doppelte Ereignisse und Auslieferung.

Für ALM ist das Verbindungszeitlimit auf 10 Sekunden und das Socket-Zeitlimit auf 5 Sekunden konfiguriert. Es wird erwartet, dass der Client die Nachricht bestätigt, sobald er sie erhält. Dadurch wird sichergestellt, dass der Client beim Verarbeiten von Nachrichten nicht verzögert. Falls eine nachgelagerte Verarbeitung zeitaufwendig ist, sollte der Client das Ereignis dennoch sofort bestätigen und die nachgelagerte Verarbeitung dann an ihrem Ende abwickeln.

### Datenaufbewahrung

Die Veranstaltungen dauern 7 Tage. Wenn sie nicht innerhalb dieser Zeit verarbeitet werden, gehen sie dauerhaft verloren. Wenn die Wiederherstellung am letzten Tag erfolgt und mehr Zeit benötigt wird, verlängert das System die Aufbewahrungsfrist nicht.
Wenn Ereignisse schneller erzeugt werden, als sie verbraucht werden, können einige Ereignisse verloren gehen. Obwohl dies ungewöhnlich ist, sollten die Abonnenten überwachen, um zu verhindern, dass es zu einem langfristigen Problem wird.

### Webhooks deaktivieren

Wenn ein Abonnent nicht auf Webhook-Ereignisse reagiert, versucht das ALM-System Webhooks mit exponentiellem Backoff erneut, um eine Überlastung des Abonnenten zu vermeiden.

Der Wiederholungsprozess beginnt mit einem anfänglichen Intervall von 5 Sekunden. Wenn der Abonnent nicht reagiert, verdoppelt sich die Wartezeit auf 10, 20, 40 und 80 Sekunden und steigt schließlich auf maximal 5 Minuten. Wenn die 5-minütige Aufbewahrungszeit erreicht ist, versucht das System weiterhin alle 5 Minuten erneut, bis die 7-tägige Aufbewahrungsfrist abgelaufen ist. Wenn der Abonnent während dieses gesamten Zeitraums immer noch nicht reagiert, wird der Webhook automatisch deaktiviert. In regelmäßigen Abständen wird eine Erinnerungs-E-Mail an den Abonnenten gesendet.

### Ereignisse duplizieren

Wenn die Reaktionszeit eines Abonnenten nach der Verarbeitung eines Ereignisses mehr als 5 Sekunden beträgt, versucht das System möglicherweise erneut, dieses Ereignis zu verarbeiten. Es wird empfohlen, Ereignis-IDs zu verwenden, um den Überblick darüber zu behalten, welche Ereignisse bereits verarbeitet wurden. Wenn der Webhook nach dem Senden des Ereignisses abstürzt, aber bevor die Verarbeitung gespeichert wurde, kann dieselbe Gruppe von Ereignissen erneut versucht werden. Es wird empfohlen, Batch-IDs oder individuelle Ereignis-IDs zu verwenden, um Duplikate zu erkennen und zu ignorieren.

### Empfehlung für Fehlertoleranz

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

## Best Practices für die Nutzung von Webhooks-Veranstaltungen

* Die Webhook-Lösung wird für Systeme mit hohem Durchsatz verwendet, bei denen Geschwindigkeit und geringe Latenz entscheidend sind. Der Kunde sollte daher sicherstellen, dass die Veranstaltung sofort nach ihrem Eingang anerkannt wird. Selbst wenn auf Kundenseite eine zusätzliche Verarbeitung erforderlich ist (z. B. das Abrufen von Daten aus Berichten, API oder das Ausführen anderer Aktionen), sollte die Bestätigung gesendet werden, sobald das Ereignis empfangen wird, und es liegt am Client, das Ereignis später zu verarbeiten.
* Wenn das Ereignis nicht so schnell wie möglich bestätigt wird, kann dies die Echtzeitfunktion der Ereignisse beeinträchtigen, da nachfolgende Ereignisse erst ausgegeben werden, wenn die vorherige Bestätigung empfangen wurde.
* Clients können mit einem HTTP 202 Accepted-Statuscode antworten, um zu bestätigen, dass das Ereignis akzeptiert wurde.

## Einschränkungen

* Arbeitshilfen werden für Webhook-Ereignisse in der Kategorie &quot;LOs&quot; nicht berücksichtigt, da sie in der Regel verwendet werden, um Teilnehmern beim Durchführen anderer Lernobjekte zu helfen.
* Ein Aussetzen einer Lernobjektinstanz würde als Aktualisierungsereignis betrachtet. Es gäbe kein Löschereignis für eine Instanz, da sie nur eingestellt, nicht gelöscht werden kann.
* Sitzungsänderungen werden als Teil des Instanzaktualisierungsereignisses erfasst. Dies gilt nur für Kurse. Bei Instanzen mit Lernpfaden oder Zertifizierungsinstanzen auf unterer Ebene erfolgt keine Weitergabe nach oben.
* Wenn ein Lernpfad einen Kurs enthält und ein Teilnehmer den Kurs über den Lernpfad abschließt, werden zwei **LearnerProgress**-Ereignisse generiert: eines für den Kurs und eines für den Lernpfad.
* Bestimmte Workflows berechnen Attribute von Lernobjekten, wie Dauer und Bereitstellungstyp, asynchron. Daher werden Ereignisse für diese Lernobjekte generiert, sobald die Verarbeitung des cron-Jobs abgeschlossen ist.
* Wenn ein Kurs über ein übergeordnetes Lernprogramm oder eine Zertifizierung registriert wird, werden die Ereignisse &quot;Registrierung&quot;, &quot;Aufhebung der Registrierung&quot; und &quot;Abschluss&quot; nur für das übergeordnete Lernprogramm oder die Zertifizierung ausgelöst. Diese Ereignisse werden für den untergeordneten Kurs nicht ausgelöst, da die Registrierung indirekt erfolgt ist.
* Webhooks werden nur für Konten mit dem Status &quot;**[!UICONTROL AKTIV]**&quot; unterstützt. Sie sind für **[!UICONTROL TRIAL]**- oder **[!UICONTROL INACTIVE]**-Konten nicht verfügbar.

## Beispiel-Payloads für die Ereignisse

+++CI_STATS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12345-0458-4450-b5dd-6bc1ef4f8b50",
      "eventName": "CI_STATS",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123456785-LoSt",
      "data": {
        "loInstanceId": "course:12345678_14448475",
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
      "eventId": "12345c1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "COURSE_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123424713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
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
      "eventId": "1234ec1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123424713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
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
      "eventId": "c2345c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "12345823000-040363-12018-0",
      "data": {
        "userId": 11080928,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14448484",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
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
      "eventId": "c23458c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123456823000-040363-12018-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14448484",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
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
      "eventId": "1234791-338f-4c4c-83bc-9f73ea794965",
      "eventName": "LEARNING_PATH_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404248000-040653-71396-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:1234567",
        "loInstanceId": "learningProgram:1234567_109139",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
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
      "eventId": "12340791-338f-4c4c-83bc-9f73ea794965",
      "eventName": "LEARNING_PATH_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404248000-040653-71396-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:1234557",
        "loInstanceId": "learningProgram:1234557_109139",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
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
      "eventId": "123404e-d554-4027-944b-086debefdddf",
      "eventName": "LEARNING_PATH_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234604391000-040653-314618-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:92348",
        "loInstanceId": "learningProgram:92348_95662",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
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
      "eventId": "12344e-d554-4027-944b-086debefdddf",
      "eventName": "LEARNING_PATH_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404391000-040653-314618-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:92348",
        "loInstanceId": "learningProgram:92348_95662",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
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
      "eventId": "1234e776-148e-4128-80e9-b896a460b655",
      "eventName": "CERTIFICATION_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "12344672000-040654-559128-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:123418",
        "loInstanceId": "certification:123418_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
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
      "eventId": "123472ec1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234524713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:123456798",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
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
      "eventId": "1234bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123454768000-040654-756257-0",
      "data": {
        "userId": 123456728,
        "loId": "certification:123418",
        "loInstanceId": "certification:134518_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z"
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
      "eventId": "123453bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234604768000-040654-756257-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:123418",
        "loInstanceId": "certification:123418_160299",
        "loType": "certification",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z"
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
      "eventId": "d1234d3a4-c3df-44fa-a1cf-7edd6e3d2075",
      "eventName": "LEARNER_PROGRESS",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235604551000-297002-5823-0",
      "data": {
        "loId": "course:7542090",
        "loType": "course",
        "userId": 12380928,
        "loInstanceId": "course:7232090_10423047",
        "dateStarted": "2024-11-08T03:49:52.000Z",
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
      "eventId": "f3237817-8cb8-40ea-a441-813bec1c7724",
      "eventName": "COURSE_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1345506253000-040298-24078-0",
      "data": {
        "userId": 12311591,
        "loId": "course:12324298",
        "loInstanceId": "course:12324298_14450088",
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
      "eventId": "f2317817-8cb8-40ea-a441-813bec1c7724",
      "eventName": "COURSE_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "17235506253000-040298-24078-0",
      "data": {
        "userId": 12311591,
        "loId": "course:12324298",
        "loInstanceId": "course:12324298_14450088",
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
      "eventId": "823df878-1dfd-47ac-9bfe-7d4952e3edd1",
      "eventName": "LEARNING_PATH_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235506667000-040299-28209-0",
      "data": {
        "userId": 12311591,
        "loId": "learning_program:123157",
        "loInstanceId": "learning_program:123157_109139",
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
      "eventId": "8e23f878-1dfd-47ac-9bfe-7d4952e3edd1",
      "eventName": "LEARNING_PATH_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235506667000-040299-28209-0",
      "data": {
        "userId": 12311591,
        "loId": "learning_program:123157",
        "loInstanceId": "learning_program:123157_109139",
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
      "eventId": "7232766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235507900000-040304-1065-0",
      "data": {
        "userId": 12311591,
        "loId": "certification:123199",
        "loInstanceId": "certification:123199_162078",
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
      "eventId": "7202766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1735507900000-040304-1065-0",
      "data": {
        "userId": 12511591,
        "loId": "certification:139199",
        "loInstanceId": "certification:139199_162078",
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
      "eventId": "12345da9f-26ec-453c-b56a-cdf18a841948",
      "eventName": "LEARNING_OBJECT_DRAFT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234519188000-040344-48604-0",
      "data": {
        "loId": "course:1234091",
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
      "eventId": "1234a690-5517-4c09-9cde-d953cdd8582c",
      "eventName": "LEARNING_OBJECT_DELETION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235605296000-040656-662792-0",
      "data": {
        "loId": "course:12319716",
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
  "accountId": 8308,
  "events": [
    {
      "eventId": "223e068-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123350842000-039736-54153-0",
      "data": {
        "loId": "learningProgram:123836",
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
  "accountId": 8308,
  "events": [
    {
      "eventId": "1234e068-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235350842000-039736-54153-0",
      "data": {
        "loId": "learningProgram:123836",
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

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1231da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123603297000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12324298_14453691",
        "loId": "course:12324298",
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
      "eventId": "12d16e90-d73a-457b-83f3-666ba9654edb",
      "eventName": "LEARNING_OBJECT_INSTANCE_DELETION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235605491000-040657-236307-0",
      "data": {
        "loInstanceId": "course:12319674_14453849",
        "loId": "course:12319674",
        "loType": "course"
      }
    }
  ]
}
```

+++

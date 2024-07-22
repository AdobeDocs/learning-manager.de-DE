---
jcr-language: en_us
title: API-Ratenbeschränkungen im Lern-Manager
contentowner: saghosh
preview: true
source-git-commit: 544c695a77c21dd9162b9b943b6119d27aa373dc
workflow-type: tm+mt
source-wordcount: '1757'
ht-degree: 51%

---



# API-Ratenbeschränkungen im Lern-Manager

## Einführung in die Tarifbegrenzung {#introductiontoratelimiting}

Adobe Learning Manager bietet eine umfangreiche Suite von REST-API, mit der Kunden Anwendungen erstellen können, die mit Learning Manager integriert werden können, oder sogar benutzerdefinierte Benutzererlebnisse und Erweiterungen für Workflows erstellen können, die ihrem Unternehmen helfen.

Wenn eine API aufgerufen wird, gibt es gemeinsame Rechenressourcen, die in den Learning Manager-Servern verwendet werden. Daher müssen wir vorsichtig und vorsichtig sein, um sicherzustellen, dass die Anwendungen gut funktionieren und die Leistungs- und Verfügbarkeitsmerkmale der Plattform nicht gefährden. Dies geschieht durch die Einführung von Limits für die Art und Weise, wie API-Clients Aufrufe tätigen (Häufigkeit und Geschwindigkeit).

Eine Anwendung könnte beispielsweise versuchen, alle Benutzer in diesem Konto abzurufen, und kann mehrere API-Aufrufe mit Paginierung und einer hohen Rate durchführen. Und aus Versehen könnte ein Entwickler dies in einer engen Schleife nennen, was zu einer enormen Belastung des Servers führen und Anwendungen träge machen und sogar die Plattform gefährden könnte, indem mehr Ressourcen verbraucht werden als beabsichtigt oder erforderlich ist.

Um dieses Problem zu lösen, führen wir Ratenbeschränkungen ein, wie viele API-Aufrufe von einem einzelnen Benutzer in einer bestimmten Client-Anwendung eines bestimmten Kontos gemacht werden können. Wir messen dies in Form von Anfragen pro Minute, abgekürzt als RPM. Wenn wir beispielsweise sagen, dass das Limit für GET API-Aufrufe 600 1/min beträgt, bedeutet dies einfach, dass ein einzelner Benutzer nicht mehr als maximal 600 Aufrufe in einer Minute durchführen kann. Wenn der Benutzer dieses Limit überschreitet, wird die Benutzerrate begrenzt. Die Anforderungen werden mit einer Granularität von Millisekunden verfolgt, sodass dieser Grenzwert 1 Anforderung alle 100 Millisekunden (ms) entspricht. Es gibt einen weiteren Parameter, Burst, der auch zusammen mit der Ratenbegrenzung definiert wird, die definiert, wie viele Anforderungen ein Benutzer über die angegebene Rate hinaus stellen kann (in unserem Fall 600 RPM). Wenn beispielsweise der Burst-Parameter 10 ist, bedeutet dies, dass bis zu 10 Slots in einer Warteschlange zugewiesen werden, und wenn eine Anforderung &quot;zu früh&quot; eintrifft (in unserem Fall früher als 100 ms), wird sie sofort verarbeitet, wenn ein Slot dafür in der Warteschlange verfügbar ist. Der Slot wird dann als &quot;belegt&quot; markiert und erst nach Ablauf der entsprechenden Zeit (in unserem Fall nach 100ms) für eine weitere Anforderung freigegeben. Der Traffic in der realen Welt erfolgt in der Regel mit Bursts, und hier hilft der Burst-Parameter. Für die Learning Manager-Plattform definieren wir Einschränkungen für eine bestimmte API-Version (z. B. V2), eine Rolle (Teilnehmer/Administrator) und ein Verb (GET/PUT/POST/DELETE/PATCH). In dem oben beschriebenen Beispiel würden wir sagen, dass die Höchstgrenze (600, 10) ist.

Obwohl wir im Learning Manager immer schon Kursbeschränkungen für die öffentliche API hatten, waren wir bei der Ermöglichung einer sehr hohen RPM bisher recht liberal. Mit dem Wachstum Ihrer bevorzugten Lernplattform haben wir jedoch ein schnelles Wachstum bei der Nutzung unserer API erlebt und wir haben uns entschieden, diese Ratenbegrenzungen explizit zu dokumentieren, zum Nutzen aller unserer Kunden und für ein besseres Management der Plattform. In diesem Zusammenhang haben wir unsere API aktualisiert und damit begonnen, eine neue API-Antwort (HTTP-Statuscode 429) zurückzugeben, die Sie bisher noch nicht gesehen haben. Diese Antwort wird für API-Clients bereitgestellt, wenn das Ratenlimit überschritten wird. Clientanwendungen müssen diesen Antwortcode jetzt so behandeln, dass er der Logik ihrer Anwendung entspricht. Dieses Dokument soll Entwicklern in erster Linie die Informationen zur Verfügung stellen, die sie benötigen, um die richtige Logik in ihren Code einzubinden, wenn sie eine solche Antwort sehen.

## Wie kann ich die erzwungenen Gebührenlimits bestätigen? {#howtoconfirmtheenforcedratelimits}

Für jede Anforderung enthalten die Antwortkopfzeilen die folgenden Informationen:

```
x-rate-limit: 600r/m 
x-burst: 10
```

* x-rate-limit gibt den Schwellenwert der Basisanforderungsrate in Form von Anforderungen pro Minute an.
* x-burst gibt an, wie viele Anforderungen, die über der Basisanforderungsrate liegen, angenommen werden, um sofort verarbeitet zu werden.

## Wie werden Fehler aufgefangen, die durch die Höchstsätze verursacht wurden? {#howtocatcherrorscausedbyratelimits}

Für jede Anforderung können Sie überprüfen, ob Sie das Ratenlimit erreicht haben. Wenn Sie den Antwortcode 429, &quot;{&quot;message&quot;:&quot;429 Zu viele Anforderungen&quot;}&quot; erhalten, haben Sie das Ratenlimit erreicht.

Es empfiehlt sich, Code in Ihr Skript einzufügen, der 429 Antworten abfängt. Wenn Ihr Skript den Fehler &quot;Zu viele Anforderungen&quot; ignoriert und weiterhin versucht, Anforderungen zu stellen, können Nullfehler auftreten. Zu diesem Zeitpunkt sind die Fehlerinformationen für die Diagnose des Problems nicht nützlich.

Beispielsweise kann eine Curl-Anforderung, die das Ratenlimit erreicht, die folgende Antwort zurückgeben:

```
< HTTP/2 429 
< date: Wed, 04 Nov 2020 06:53:04 GMT 
< content-type: application/json; charset=utf-8 
< server: openresty 
< x-rate-limit: 60r/m 
< x-burst: 10 
< retry-after: 10.752 
< access-control-allow-credentials: true 
< access-control-allow-methods: GET, POST, OPTIONS, PUT, HEAD, DELETE, PATCH 
< access-control-allow-headers: X-acap-all-roles, X-acap-account,X-acap-user,X-acap-caller-role,Keep-Alive,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type, x-experience-api-version, Authorization, X-CSRF-TOKEN, X-HTTP-Method-Override 
< strict-transport-security: max-age=31536000; includeSubDomains 
< x-frame-options: SAMEORIGIN 
< x-xss-protection: 1 
< x-content-type-options: nosniff 
< x-request-id: gwBBFC9741-58A5-43B1-B1FE-7D14275961E7 
< strict-transport-security: max-age=31536000; includeSubDomains
```

Die Antwort enthält Informationen zu den folgenden Schlüsseln:

```
status: 429 
retry-after: 10.752
```

Der Statuscode 429 bedeutet &quot;zu viele Anforderungen&quot; und dass die aktuelle Anforderung nicht verarbeitet wird. Der retry-after-Header gibt an, dass Sie den API-Aufruf in 10,752 Sekunden wiederholen können. Ihr Code sollte zusätzliche API-Anforderungen erst dann stellen, wenn genügend Zeit für einen Wiederholungsversuch verstrichen ist.

Der folgende Pseudocode zeigt eine einfache Möglichkeit, Ratenbegrenzungsfehler zu fangen:

```
response = request.get(url) 
if response.status equals 429: 
    alert('Rate limited. Waiting to retry…') 
    wait(response.retry-after) 
    retry(url)
```

Wir haben sogar ein Lern-Manager-Dummy-API erstellt, damit Sie herumspielen und sich mit der Handhabung des 429-Statuscodes vertraut machen können.

```
curl -X GET --header 'Accept: application/json' --header 'Authorization: oauth < 
<token>
  >' 'https://learningmanager.adobe.com/learningmanagerapi/v2/dummy 
</token>
```

Diese Dummy-API bietet folgende Einschränkungen:

```
x-rate-limit: 5r/m 
x-burst: 2
```

Das Limit für die Dummy-API ist absichtlich niedrig, sodass Sie sehr schnell an die Ratengrenzen stoßen und sich dann mehr auf die Entwicklung des Codes konzentrieren können, um die Ratengrenzenfehler zu erfassen und zu behandeln.

## Testen der Dummy-API {#testingthedummyapi}

Wir haben einen Endpunkt für Sie bereitgestellt, um zu überprüfen, wie die Ratenbegrenzung funktioniert. Dazu haben wir einen speziellen Endpunkt namens GET /dummy erstellt, der den Lesebereich des Teilnehmers hat. Diese API wurde bewusst für eine sehr strenge Ratenbegrenzung von 5 Anforderungen pro Minute mit einer Burst-Begrenzung = 2 konfiguriert.

Sie können dies ganz einfach testen, indem Sie diesen Endpunkt mit Raten unter 5 U/min und über 5 U/min erreichen. Schreiben Sie Code zur Verarbeitung des HTTPS-Statuscodes 429 und basierend auf den Informationen in den Antwortkopfzeilen.

Um es Ihnen leicht zu machen, können Sie sich diesen Beispiel-JavaScript-Code ansehen, der dies veranschaulicht. Klicken Sie auf [fiedeln](https://jsfiddle.net/ACAPJS/9yv8zcmL/) und den Code in Aktion zu sehen.

Für diese Anwendung müssen Sie ein Teilnehmerrollen-Anwendungstoken für Ihr Konto bereitstellen. Weitere Informationen zu API-Token finden Sie im [Handbuch für Anwendungsentwickler](https://captivateLearning Manager.adobe.com/docs/Learning). Sie können den Token Helper im Abschnitt mit Entwicklerressourcen der Learning Manager Integration Admin-Anwendung verwenden, um die Token zu generieren.

Diese Anwendung führt 10 Aufrufe der Dummy-API in einer Schleife auf einmal durch. Da das Ratenlimit (5, 2) für die Dummy-API ist, wird das Ratenlimit nach den ersten 5+2-Aufrufen überschritten, die vom Learning Manager empfangen werden. Sie erhalten eine Erfolgsantwort für sie.

Beachten Sie jedoch, wie diese Anwendung nach dem Statuscode 429 als Antwort und zur Verarbeitung sucht. Wenn diese Anwendung eine solche Antwort erhält, druckt sie die Details in der API-Antwort aus, wartet auf die vorgeschlagene Zeit und versucht die fehlgeschlagenen Versuche erneut.

## Empfohlene Verfahren für die Handhabung von Ratenbegrenzungen {#bestpracticestohandleratelimiting}

Daten in einem Konto ändern sich oft nicht so oft. Beispielsweise können sich die Kurse in einem Konto nicht so oft ändern. Anstatt zu versuchen, alle Daten jedes Mal abzurufen, sollten Sie prüfen, ob Sie die spezifischen Daten abrufen können, wenn Sie sie benötigen, und einen Cache-Mechanismus in Betracht ziehen. Auf diese Weise haben Sie, wenn Ihre Anwendung wirklich viele Anrufe tätigen muss, innerhalb Ihrer Gebührenlimits genügend Kontingent, um diese wichtigen Anrufe zu tätigen.

Manche Daten ändern sich möglicherweise öfter, und Sie müssen sie möglicherweise öfter abrufen. Selbst wenn ja, fragen Sie sich, ob Ihre Anwendung es sich leisten kann, leicht veraltete Daten zu haben (etwas, das sich möglicherweise in Ihrem Cache befindet, den Sie vor N Minuten abgerufen haben), da es möglicherweise keine Auswirkungen auf den Arbeitsablauf des Benutzers hat. Selbst wenn Sie frische Daten von den Servern benötigen, können Sie beim Abrufen genau der Daten, die Sie benötigen, vorsichtig sein, anstatt alles zu erhalten.

Es wird auch Zeiten geben, in denen Sie keine Wahl haben, viele Daten zu erhalten, weil die API möglicherweise nicht flexibel genug ist, um Ihnen mit nur einem Aufruf genau das zu geben, was Sie möchten. Prüfen Sie, ob die API Ihnen Filter und Sortierkriterien zur Verfügung stellt, mit denen die Anzahl der Aufrufe minimiert werden kann. Sie sollten dennoch das Caching in Betracht ziehen, da viele Benutzer in Ihrem Konto möglicherweise dieselben Daten benötigen.

Wenn Sie im Kontext einer interaktiven Anwendung mit einer GUI zu viele Daten erhalten, ist es wahrscheinlich, dass die Anwendung zu viel versucht und den Benutzer mit vielen Informationen/Funktionen überfordert, die sich auf das Benutzererlebnis Ihrer Anwendung auswirken.

Wenn Sie eine nicht interaktive Anwendung erstellen (z. B. einen täglichen Job), müssen Sie möglicherweise viele Daten gesammelt abrufen. In solchen Fällen sollten Sie die Job-API verwenden, die in erster Linie dazu entwickelt wurde, Massendaten im CSV-Format zurückzugeben. Beachten Sie, dass die Job-API über eine Kontingenteinschränkung verfügt, die Sie N Mal pro Tag aufrufen können.

Da Learning Manager die JSONAPI-Spezifikationen implementiert hat, gibt es API, in die Sie auch einige Daten seitlich laden können. Dies wird Ihnen helfen, zusätzliche API-Aufrufe zu vermeiden, aber Sie müssen dies damit eintauschen, dass Sie zu eifrig Daten erhalten. Da die seitlich geladenen Daten manchmal sehr groß sein können, machen Sie bei API-paginierten Aufrufen die maximale Seitengröße auf 10 beschränkt. Bei API-Aufrufen ohne Includes können Sie jedoch möglicherweise eine größere Seitengröße (bis zu 100) angeben.

Wenn Sie in kurzer Zeit viele API-Anfragen stellen, stoßen Sie schließlich an das API-Ratenlimit für Anfragen. Wenn Sie das Limit erreichen, beendet der Lern-Manager die Verarbeitung weiterer Anforderungen, bis eine bestimmte Zeit verstrichen ist.

Die Höchstsätze sind im letzten Abschnitt dieses Artikels beschrieben. Es wird empfohlen, dass Sie sich mit den Einschränkungen vertraut machen.

## Ratenbegrenzungen für V2-API-Endpunkte {#ratelimitsforv2apiendpoints}

Die folgende Tabelle enthält die Einschränkungen für die verschiedenen V2-Endpunkte. Gegenwärtig gelten die Höchstsätze nicht für die Kunden, aber sie werden ab TT/MM/JJJJ durchgesetzt. Daher ist es für Kunden wichtig, den Code ihrer vorhandenen Anwendungen zu überprüfen, um zu sehen, wie sie ihren Code anpassen können, um sich dieser Ratenlimits bewusst zu sein, und die API-Antworten mit dem HTTP-Statuscode 429 zu verarbeiten.

<table> 
 <tbody>
  <tr> 
   <td><p><b>Vorgang</b></p></td> 
   <td><p><b>Admin API</b></p></td> 
   <td><p><b>Teilnehmer-API</b></p></td> 
  </tr> 
  <tr> 
   <td><p>DELETE</p></td> 
   <td><p>(25, 10) <br></p></td> 
   <td><p>(20, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>PATCH</p></td> 
   <td><p>(60, 20)</p></td> 
   <td><p>(15, 5) <br></p></td> 
  </tr> 
  <tr> 
   <td><p>POST</p></td> 
   <td><p>(30, 10)<br></p></td> 
   <td><p>(30, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>PUT</p></td> 
   <td><p>(20, 10)<br></p></td> 
   <td><p>(20, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>GET</p></td> 
   <td><p>(100, 100)<br></p></td> 
   <td><p>(100, 30)<br></p></td> 
  </tr> 
 </tbody>
</table>


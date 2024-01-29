---
jcr-language: en_us
title: Handbuch für Anwendungsentwickler
description: Die Lern-Manager V1-API ist jetzt veraltet. Die V1-APIs funktionieren ab dem 28. Februar 2021 nicht mehr. Wir empfehlen Ihnen, V2-APIs zu verwenden, um mit dem Learning Manager zu interagieren.
contentowner: jayakarr
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '3279'
ht-degree: 0%

---



# Handbuch für Anwendungsentwickler

Die Lern-Manager V1-API ist jetzt veraltet. Die V1-APIs funktionieren ab dem 28. Februar 2021 nicht mehr. Wir empfehlen Ihnen, V2-APIs zu verwenden, um mit dem Learning Manager zu interagieren.

## Übersicht {#overview}

[Adobe Learning Manager](http://www.adobe.com/in/products/learningmanager.html) ist eine in der Cloud gehostete, auf die Kursteilnehmer zugeschnittene Selfservice-Lösung für Learning Management. Kunden können über die Learning Manager-API programmgesteuert auf Learning Manager-Ressourcen zugreifen, um sie mit anderen Unternehmensanwendungen zu integrieren. Die API kann auch von Adobe-Partnern verwendet werden, um das Wertversprechen von Learning Manager zu verbessern, indem die Funktionen erweitert oder in andere Anwendungen oder Services integriert werden.

### Anwendungsszenario {#usagescenario}

Mithilfe der Learning Manager-API können Entwickler eigenständige Anwendungen erstellen, die die Funktionalität von Learning Manager erweitern oder Learning Manager mit anderen Workflows für Unternehmensanwendungen integrieren. Sie können eine Webanwendung, einen Desktop-Client oder eine mobile App mit einer beliebigen Technologie Ihrer Wahl entwickeln. Als Entwickler können Sie über Learning Manager auf Ihre Anwendungsdaten zugreifen. Die Bereitstellung der von Ihnen entwickelten Anwendung erfolgt außerhalb der Learning Manager-Plattform, und Sie haben die vollständige Kontrolle über den Lebenszyklus der Softwareentwicklung, während die Anwendung weiterentwickelt wird. Anwendungen werden in der Regel von einer Kundenorganisation zur Verwendung mit ihrem Learning Manager-Konto entwickelt und diese Anwendungen sind für diese spezifische Kundenorganisation privat. Darüber hinaus können Adobe-Partner mit der Learning Manager-API generische Anwendungen erstellen, die von einer großen Gruppe von Learning Manager-Kunden verwendet werden können.

## Learning Manager API {#apidescription}

Die Learning Manager-API basiert auf den Prinzipien von REST und stellt wichtige Elemente des Learning Manager-Objektmodells Anwendungsentwicklern über HTTP zur Verfügung. Bevor Entwickler die Details der API-Endpunkte und der HTTP-Methoden kennen, können sie sich mit den verschiedenen Lern-Manager-Objekten, ihren Attributen und Beziehungen vertraut machen. Sobald die Modelle verstanden wurden, ist es hilfreich, ein grundlegendes Verständnis der Struktur von API-Anfragen und -Antworten sowie einige gängige Programmierbegriffe zu erlangen, die wir in der API allgemein verwenden.

Ausführliche Informationen zu den verschiedenen API-Endpunkten und -Methoden finden Sie unter  [Dokumentation zur Learning Manager-API](https://learningmanager.adobe.com/docs/primeapi/v2/).

## API-Authentifizierung {#apiauthentication}

Wenn Sie eine Anwendung schreiben, die API-Aufrufe an Learning Manager ausführt, müssen Sie Ihre Anwendung mithilfe der Integrations-Admin-App registrieren.

Learning Manager-APIs verwenden das OAuth 2.0-Framework zum Authentifizieren und Autorisieren Ihrer Clientanwendungen.

**Vorgehensweise**

**1. Anwendung einrichten**

Sie können die Anwendung mit der Client-ID und dem Client-Secret einrichten, um die richtigen Endpunkte zu verwenden. Nachdem Sie die Anwendung registriert haben, können Sie clientId und clientSecret abrufen. Die Get-URL sollte im Browser verwendet werden, da sie die Learning Manager-Benutzer mit ihren vorkonfigurierten Konten wie SSO, Adobe ID usw. authentifiziert.

```
GET https://learningmanager.adobe.com/oauth/o/authorize?client_id=<Enter your clientId>&redirect_uri=<Enter a url to redirect to>&state=<Any String data>&scope=<one or more comma separated scopes>&response_type=CODE.
```

Nach erfolgreicher Authentifizierung leitet Ihr Browser zu dem in der oben genannten URL angegebenen redirect_uri weiter. Ein Parameter **Kodex** und dem Umleitungs-URI angehängt.

**2. Aktualisierungstoken aus dem Code abrufen**

`POST https://learningmanager.adobe.com/oauth/token Content-Type: application/x-www-form-urlencoded`

Hauptteil der Stellenanforderung:

```
client_id: 
<enter your clientid>
 & 
 client_secret: 
 <enter your clientsecret>
  & 
  code: 
  <code from step 1></code>
 </enter>
</enter>
```

**3.** **Abrufen eines Zugriffstokens aus dem Aktualisierungstoken**

URL zum Abrufen des Zugriffstokens:

POST [https://learningmanager.adobe.com/oauth/token/refresh](https://learningmanager.adobe.com/oauth/token/refresh) Content-Type: application/x-www-form-urlencoded

Hauptteil der Stellenanforderung:

```
client_id: 
<enter your clientid>
 & 
 client_secret: 
 <enter your clientsecret>
  & 
  refresh_token: 
  <refresh token>
   
  </refresh>
 </enter>
</enter>
```

**URL zum Überprüfen der Details zum Zugriffstoken**

`GET https://learningmanager.adobe.com/oauth/token/check?access_token=<access_token>`

**Nutzungsbeschränkung**

Ein Zugriffstoken ist sieben Tage lang gültig. Nach einem Tag müssen Sie mithilfe des Aktualisierungstokens ein neues Zugriffstoken generieren. Wenn Sie ein neues Zugriffstoken aus dem Aktualisierungstoken generieren, während ein vorhandenes Zugriffstoken noch gültig ist, wird das vorhandene Token zurückgegeben.

Einige der häufig verwendeten Begriffe in der Learning Manager-API werden unten als Referenz erläutert.

**Umfasst**

Entwickler können auf ein einzelnes API-Objektmodell sowie auf mehrere mit diesem Modell verknüpfte Modelle zugreifen. Um auf die nachfolgenden verwandten Modelle zugreifen zu können, müssen Sie die Beziehung jedes Modells zu anderen Modellen kennen. **Umfasst** ermöglicht Entwicklern den Zugriff auf die abhängigen Modelle. Sie können mehrere Modelle durch Kommas trennen. Beispiele zur Verwendung und weitere Informationen zu **umfasst** finden Sie weitere Informationen im Abschnitt zum Beispiel-API-Modell auf dieser Seite.

**API-Anfrage**

Die API-Anforderungen können durch eine HTTP-Anforderung gestellt werden. Abhängig vom Endpunkt und der Methode kann der Entwickler verschiedene HTTP-Verben wie GET, PUT, POST, DELETE, PATCH usw. wählen. Für einige Anforderungen können Abfrageparameter übergeben werden. Wenn der Benutzer eine Anforderung für ein bestimmtes Datenmodell sendet, kann er auch die entsprechenden Modelle anfordern, wie in den JSON API-Spezifikationen beschrieben. Die Struktur einer typischen API-Anforderung wird unter [Beispielmodellverwendung](#main-pars_header_1415780624).

**API-Antwort**

Wenn eine API-Anforderung von einem Client gestellt wird, wird ein SON-Dokument gemäß der JSON-API-Spezifikation abgerufen. Die Antwort enthält außerdem den HTTP-Statuscode, den der Entwickler überprüfen kann, um die entsprechenden nächsten Schritte in seiner Anwendungslogik auszuführen. Die Struktur einer typischen API-Antwort wird unter  [Beispielmodellverwendung](#main-pars_header_1415780624).

**Fehler**

Wenn eine API-Anforderung fehlschlägt, wird eine Fehlerantwort abgerufen. Der in der Antwort zurückgegebene HTTP-Statuscode gibt die Art des Fehlers an. Fehlercodes werden in der API-Referenz für jedes Modell mit Zahlen dargestellt. 200, 204, 400 und 404 sind einige der häufigsten Fehler, die in APIs angezeigt werden und auf HTTP-Zugriffsprobleme hinweisen.

**Felder**

Die Attribute des API-Objekts und seine Beziehungen werden zusammen als Felder bezeichnet. Siehe [JSON-API für weitere Informationen.](http://jsonapi.org/format/#document-resource-object-fields) Sie können Felder als Parameter verwenden, während Sie API-Aufrufe durchführen, um ein oder mehrere bestimmte Attribute aus dem Modell abzurufen. Wenn der Fields-Parameter fehlt, ruft der API-Aufruf alle verfügbaren Attribute aus dem Modell ab. Im folgenden API-Aufruf werden z. B. Felder[Fertigkeit]=name ruft nur das Namensattribut des Kenntnismodells ab.

https://learningmanager.adobe.com/primeapi/v2/users/{userId}/userSkills/{id}?include=skillLevel.skill&amp;fields[skill]=name

**Seitenumbruch**

Manchmal führt eine API-Anforderung zu einer langen Liste von Objekten, die in der Antwort zurückgegeben werden. In solchen Fällen ermöglicht das Seitenumbruchattribut dem Entwickler, die Ergebnisse sequenziell in Form mehrerer Seiten abzurufen, wobei jede Seite einen Bereich von Datensätzen enthält. Beispielsweise können Sie mit dem Seitenumbruchattribut im Lern-Manager die maximale Anzahl von Datensätzen festlegen, die auf einer Seite angezeigt werden sollen. Außerdem können Sie den Bereichswert von Datensätzen definieren, die auf der Seite angezeigt werden sollen.

**Sortieren**

Das Sortieren ist in API-Modellen zulässig. Wählen Sie basierend auf dem Modell die Art der Sortierung aus, die auf die Ergebnisse angewendet werden soll. Die Sortierung kann in aufsteigender oder absteigender Reihenfolge angewendet werden. Wenn Sie beispielsweise `code sort=name`aufsteigend sortiert nach Namen. Wenn Sie `code sort=-name`, es wird absteigend nach Name sortiert. Siehe [JSON-API-Spezifikation für weitere Informationen](http://jsonapi.org/format/#fetching-sorting).

## Abbildung: API-Verwendung {#samplemodel}

Lassen Sie uns ein Szenario in Betracht ziehen, in dem ein Entwickler den Namen der Kenntnisse, die für die Kenntnisstufe zugewiesenen Höchstpunkte und die vom Teilnehmer für diese Kenntnisse gesammelten Punkte abrufen möchte.

Ein userSkill-Modell in Learning Manager-APIs besteht aus den Standardattributen id, type, dateAchieved, dateCreated, pointsEarned. Wenn ein Entwickler also die GET-Methode verwendet, um Details des userSkill-Modells abzurufen, werden die aktuellen Daten zu den Standardattributen in der Antwortausgabe angezeigt.

In diesem Szenario möchte der Entwickler jedoch den Namen der Qualifikation und die Punkte der Qualifikationsstufe für den Benutzer abrufen. Mit der Learning Manager-API können Sie mithilfe von Beziehungsfeldern und Include-Parametern auf diese verknüpften Informationen zugreifen. Die verknüpften Modelle für userSkill werden im Beziehungs-Tag abgerufen. Sie können die Details der einzelnen verknüpften Modelle abrufen, indem Sie diese Modelle zusammen mit userSkill aufrufen. Um diese Informationen abzurufen, verwenden Sie **`code include`** Parameter mit durch Punkte (Punkte) getrennten Werten für jedes der zugehörigen Modelle. Sie können Komma als Trennzeichen verwenden, um ein anderes Modell anzufordern, z. B. user include=skillLevel.skill,course

**API-Aufruf**

`https://learningmanagerqe1.adobe.com/primeapi/v1/users/%7buserId%7d/userSkills/%7bid%7d?include=skillLevel.skill&fields%5bskill%5d=name&fields%5bskillLevel%5d=maxCredits&fields%5buserSkill%5d=pointsEarned`

Beispielsweise kann userId 746783 werden und userSkills id: 746783_4426_1.

**Antwort des API-Aufrufs**

```
\{ 
 "links": {"self": "https://learningmanager.adobe.com/primeapi/v2/users/746783/userSkills/746783_4426_1?include=skillLevel.skill&fields[userSkill]=pointsEarned&fields[skillLevel]=maxCredits&fields[skill]=name"}, 
 "data": { 
 "id": "746783_4426_1", 
 "type": "userSkill", 
 "attributes": {"pointsEarned": 5}, 
 "links": {"self": "https://learningmanager.adobe.com/primeapi/v2/users/746783/userSkills/746783_4426_1"} 
 }, 
 "included": [ 
 { 
 "id": "4426", 
 "type": "skill", 
 "attributes": {"name": "Java"}, 
 "links": {"self": "https://learningmanager.adobe.com/primeapi/v2/skills/4426"} 
 }, 
 { 
 "id": "4426_1", 
 "type": "skillLevel", 
 "attributes": {"maxCredits": 10} 
 } 
 ] 
} 
```

## Learning Manager-Modelle {#models}

Mit der Lern-Manager-API können Entwickler auf Lern-Manager-Objekte als RESTful-Ressourcen zugreifen. Jeder API-Endpunkt stellt eine Ressource dar, in der Regel eine Objektinstanz wie ein Abzeichen oder eine Auflistung solcher Objekte. Die Entwickler verwenden dann die HTTP-Verben wie PUT, GET, POST und DELETE, um die CRUD-Vorgänge für diese Objekte (Auflistungen) auszuführen.

+++V1-API

Das folgende Diagramm stellt die verschiedenen Elemente des Lern-Manager-Objektmodells in der V1-API dar.

![](assets/er-diag-primemodels.png)

In der folgenden Tabelle werden verschiedene Elemente des Lern-Manager V1-Objektmodells beschrieben:

<table border="1" cellspacing="0" cellpadding="0">
 <tbody>
  <tr>
   <td>
    <p><strong>Seriennummer</strong></p></td>
   <td>
    <p><strong>Lern-Manager-Objekt</strong></p></td>
   <td>
    <p><strong>Beschreibung</strong></p></td>
  </tr>
  <tr>
   <td>
    <p>1.      </p></td>
   <td>
    <p>Anwender</p></td>
   <td>
    <p>Der Benutzer ist das Schlüsselmodell im Lern-Manager. Benutzer sind in der Regel die internen oder externen Teilnehmer eines Unternehmens, die Lernobjekte nutzen. Sie können jedoch zusammen mit der Teilnehmerrolle einige andere Rollen wie Autor und Manager spielen. Benutzer-ID, Typ und E-Mail sind einige der Inline-Attribute. </p></td>
  </tr>
  <tr>
   <td>
    <p>2.      </p></td>
   <td>
    <p>Bahn</p></td>
   <td>
    <p>Kurs ist eines der Lernobjekte, die im Lern-Manager unterstützt werden und aus einem oder mehreren Modulen bestehen. </p></td>
  </tr>
  <tr>
   <td>
    <p>3.      </p></td>
   <td>
    <p>Modul</p></td>
   <td>
    <p>Ein Modul ist ein Baustein zum Erstellen von Lernobjekten im Lern-Manager. Module können vier verschiedene Typen aufweisen, z. B. Klassenzimmer, virtueller Klassenzimmer, Aktivität und Selbststudium. Verwenden Sie dieses Modulmodell, um die Details aller Module in einem Konto abzurufen. </p></td>
  </tr>
  <tr>
   <td>
    <p>4.      </p></td>
   <td>
    <p>Beglaubigung</p></td>
   <td>
    <p>Die Zertifizierung wird Teilnehmern basierend auf dem erfolgreichen Abschluss von Kursen erteilt. Kurse sind in der Anwendung erforderlich, bevor Sie Zertifizierungen verwenden. </p></td>
  </tr>
  <tr>
   <td>
    <p>5.      </p></td>
   <td>
    <p>Lernprogramm</p></td>
   <td>
    <p>Lernprogramme sind individuell gestaltete Kurse, die den spezifischen Lernanforderungen der Benutzer entsprechen. In der Regel werden Lernprogramme verwendet, um Lernziele zu fördern, die sich über einzelne Kurse erstrecken. </p></td>
  </tr>
  <tr>
   <td>
    <p>6.      </p></td>
   <td>
    <p>Ausweis</p></td>
   <td>
    <p>Ein Abzeichen ist ein Leistungsnachweis, den Teilnehmer erhalten, wenn sie bestimmte Meilensteine erreichen, während sie innerhalb eines Kurses fortschreiten. </p></td>
  </tr>
  <tr>
   <td>
    <p>7.      </p></td>
   <td>
    <p>Fertigkeit</p></td>
   <td>
    <p>Das Qualifikationsmodell besteht aus Stufen und Credits. Kenntnisse können von den Teilnehmern nach Abschluss des entsprechenden Kurses erworben werden. </p></td>
  </tr>
  <tr>
   <td>
    <p>8.      </p></td>
   <td>
    <p>certificationEnrollment</p></td>
   <td>
    <p>Dieses Modell enthält Details zur Registrierung eines Benutzers für eine einzelne Zertifizierung.</p></td>
  </tr>
  <tr>
   <td>
    <p>9.  </p></td>
   <td>
    <p>courseEnrollment</p></td>
   <td>
    <p>Dieses Modell enthält Details zur Registrierung eines Benutzers für einen einzelnen Kurs. </p></td>
  </tr>
  <tr>
   <td>
    <p>10.  </p></td>
   <td>
    <p>courseInstance</p></td>
   <td>
    <p>Einem Kurs können eine oder mehrere Instanzen zugeordnet sein. Sie können Kursinstanzen abrufen </p></td>
  </tr>
  <tr>
   <td>
    <p>11.  </p></td>
   <td>
    <p>courseSkill</p></td>
   <td>
    <p>Ein courseSkill-Modell gibt den Fortschritt einer einzelnen Qualifikation an, die durch das Abschließen eines Kurses erreicht wird.</p></td>
  </tr>
  <tr>
   <td>
    <p>12.  </p></td>
   <td>
    <p>courseModule</p></td>
   <td>Ein courseModule-Modell gibt an, wie ein Modul in einen Kurs eingeschlossen ist. Zum Beispiel, ob das Modul für Vortests oder für Inhalte verwendet wird.</td>
  </tr>
  <tr>
   <td>
    <p>13.  </p></td>
   <td>learningProgramInstance</td>
   <td>
    <p>Ein Lernprogramm kann aus mehreren Instanzen bestehen, die ähnliche Eigenschaften eines Lernprogramms annehmen, oder aus benutzerdefinierten Instanzen. </p></td>
  </tr>
  <tr>
   <td>
    <p>14.  </p></td>
   <td>
    <p>Arbeitshilfe</p></td>
   <td>
    <p>Die Arbeitshilfe ist ein Lerninhalt, der Teilnehmern ohne Registrierung oder Abschlusskriterien zur Verfügung steht. Sie können Informationen zu Datum, Status, ID sowie zu zugehörigen Modellen wie Version der Arbeitshilfe, Autoren und Kenntnisstand abrufen und aktualisieren. </p></td>
  </tr>
  <tr>
   <td>
    <p>15.  </p></td>
   <td>
    <p>jobAidVersion</p></td>
   <td>
    <p>Der Arbeitshilfe können eine oder mehrere Versionen zugeordnet sein, basierend auf der Anzahl der Überarbeitungen des Inhalts und der Anzahl der Uploads. Dieses Modell enthält Details zu einer einzelnen Arbeitshilfeversion. </p></td>
  </tr>
  <tr>
   <td>
    <p>16.  </p></td>
   <td>
    <p>learningProgramInstanceEnrollment</p></td>
   <td>
    <p>Das Lernprogramm besteht aus einer oder mehreren Instanzen. Teilnehmer können sich für eine Lernprogramminstanz selbst registrieren oder vom Administrator zugewiesen werden. Dieses Modell enthält Details zur Registrierung eines Benutzers für eine einzelne Lernprogramminstanz. </p></td>
  </tr>
  <tr>
   <td>
    <p>17.  </p></td>
   <td>
    <p>moduleVersion</p></td>
   <td>
    <p>Ein Modul kann eine oder mehrere Versionen enthalten, basierend auf den Uploads überarbeiteter Inhalte. Verwenden Sie dieses Modell, um spezifische Informationen zu einer einzelnen Modulversion zu erhalten. </p></td>
  </tr>
  <tr>
   <td>
    <p>18.  </p></td>
   <td>
    <p>skillLevel</p></td>
   <td>
    <p>Eine Kenntnisstufe umfasst einen oder mehrere Kurse, die genutzt werden müssen, um eine Stufe zusammen mit den zugehörigen Credits zu erwerben. </p></td>
  </tr>
  <tr>
   <td>
    <p>19.  </p></td>
   <td>
    <p>userBadge</p></td>
   <td>
    <p>UserBadge verknüpft ein einzelnes Abzeichen mit einem einzelnen Benutzer. Es enthält Details wie den Zeitpunkt, zu dem es erreicht wurde, assertionUrl usw. </p></td>
  </tr>
  <tr>
   <td>
    <p>20.  </p></td>
   <td>
    <p>userSkill</p></td>
   <td>
    <p>UserSkill gibt an, wie viel von einer einzelnen Kenntnisstufe ein einzelner Benutzer erreicht.</p></td>
  </tr>
 </tbody>
</table>

+++

+++V2-API

Im Folgenden sind die verschiedenen Elemente des Learning Manager-Klassendiagramms in der V2-API aufgeführt.

![](assets/v2api-class-diagram.jpg)

<table>
 <tbody>
  <tr>
   <th><b>Lern-Manager-Objekt</b></th>
   <th><b>Beschreibung</b></th>
  </tr>
  <tr>
   <td>Bericht</td>
   <td>Kapselt die Details eines Learning Manager-Kunden.</td>
  </tr>
  <tr>
   <td><code>
     badge
    </code></td>
   <td>Ein Abzeichen ist ein Leistungsnachweis, den Teilnehmer erhalten, wenn sie bestimmte Meilensteine erreichen, während sie innerhalb eines Kurses fortschreiten. <br></td>
  </tr>
  <tr>
   <td><code>
     catalog
    </code></td>
   <td>ist eine Sammlung von Lernobjekten.</td>
  </tr>
  <tr>
   <td><code>
     user
    </code></td>
   <td>Der Benutzer ist das Schlüsselmodell im Lern-Manager. Benutzer sind in der Regel die internen oder externen Teilnehmer eines Unternehmens, die Lernobjekte nutzen. Sie können jedoch zusammen mit der Teilnehmerrolle einige andere Rollen wie Autor und Manager spielen. Benutzer-ID, Typ und E-Mail sind einige der Inline-Attribute. </td>
  </tr>
  <tr>
   <td>Hilfsmittel</td>
   <td>Dies wird verwendet, um jede Inhaltsressource zu modellieren, die ein Modul kapseln möchte. Alle Ressourcen, die in <code>
     an
    </code> <code>
     loResource
    </code> sind in Bezug auf das Lernziel gleichwertig, unterscheiden sich jedoch in Bezug auf den Bereitstellungstyp oder das Inhaltsgebietsschema.<br></td>
  </tr>
  <tr>
   <td>userNotification</td>
   <td>Dieses Modell enthält Benachrichtigungsinformationen für einen Teilnehmer.<br></td>
  </tr>
  <tr>
   <td>userSkill</td>
   <td>UserSkill gibt an, wie viel von einer einzelnen Kenntnisstufe ein einzelner Benutzer erreicht.<br></td>
  </tr>
  <tr>
   <td>userBadge</td>
   <td>UserBadge bezieht sich auf ein einzelnes Abzeichen <code>
     with
    </code> für einen einzelnen Benutzer. Es enthält Details wie den Zeitpunkt, zu dem es erreicht wurde, <code>
     assertionUrl
    </code> usw. <br></td>
  </tr>
  <tr>
   <td>Fertigkeit</td>
   <td>Das Qualifikationsmodell besteht aus Stufen und Credits. Kenntnisse können von den Teilnehmern nach Abschluss des entsprechenden Kurses erworben werden. <br></td>
  </tr>
  <tr>
   <td>skillLevel</td>
   <td>Eine Kenntnisstufe umfasst einen oder mehrere Kurse, die genutzt werden müssen, um eine Stufe zusammen mit den zugehörigen Credits zu erwerben. <br></td>
  </tr>
  <tr>
   <td>learningObject</td>
   <td>Ein Lernobjekt ist eine Abstraktion für verschiedene Arten von Objekten, bei denen sich Benutzer anmelden und von denen sie lernen können. Derzeit verfügt der Lern-Manager über die vier Typen von Lernobjekten - Kurs, Zertifizierung, Lernprogramm <code>
     and
    </code> Arbeitshilfe.<br></td>
  </tr>
  <tr>
   <td>learningObjectInstance<br></td>
   <td>Eine bestimmte Instanz eines Lernobjekts.<br></td>
  </tr>
  <tr>
   <td>learningObjectResource</td>
   <td>Dies entspricht dem Konzept der <code>
     module
    </code>. Ein Kurs besteht aus einem <code>
     of
    </code> Weitere Module. In Learning Manager kann ein Modul auf verschiedene gleichwertige Arten bereitgestellt werden. Daher <code>
     loResource
    </code> im Wesentlichen alle diese äquivalenten Ressourcen einkapselt.<br></td>
  </tr>
  <tr>
   <td>loResourceGrade<br></td>
   <td>Dies umfasst das Ergebnis des Benutzers, der eine bestimmte Ressource im Kontext eines Lernobjekts nutzt, bei dem er registriert ist. Es enthält Informationen wie die von <code>
     user
    </code> in der Ressource den prozentualen Fortschritt des Benutzers, den Status "Bestanden/Nicht bestanden" und die Punktzahl, die der Benutzer in einem zugeordneten Quiz erzielt hat.<br></td>
  </tr>
  <tr>
   <td>Kalender<br></td>
   <td>Ein Kalenderobjekt ist eine Liste von <code>
     upcoming classroom
    </code> oder virtuellen Klassenzimmerkursen, bei denen sich der Benutzer anmelden kann.<br></td>
  </tr>
  <tr>
   <td>l1FeedbackInfo<br></td>
   <td>L1-Feedback umfasst die Antworten eines Teilnehmers auf die Feedback-Fragen zu Lernobjekten. In der Regel wird dies erfasst, nachdem der Benutzer ein Lernobjekt abgeschlossen hat, wenn konfiguriert, um ein solches Feedback von Teilnehmern zu erfassen.<br></td>
  </tr>
  <tr>
   <td>Einschreibung<br></td>
   <td>Diese Abstraktion umfasst die Details der Transaktion, die die Zuweisung eines bestimmten Benutzers zu einer bestimmten Lernobjektinstanz darstellt.<br></td>
  </tr>
 </tbody>
</table>

+++

Liste der Objektattribute und Beziehungen.

+++account

**Attribute**
dateCreated\
gamificationEnabled\
id\
Gebietsschema\
loginUrl\
logoUrl\
name\
Subdomain\
themeData\
timeZoneCode

**Beziehungen**
contentLocales(localizationMetadata)\
gamificationLevels(gamificationLevel)\
timeZones(timeZone)\
uiLocales(localizationMetadata)

+++

+++badge

**Attribute**
id\
imageUrl\
name\
Status

+++

+++catalog

**Attribute**
dateCreated\
dateUpdated\
Beschreibung\
id\
isDefault\
isInternallySearchable\
isListable\
name\
Status

+++

+++data

**Attribute**
id\
Namen

+++

+++gamification

**Attribute**
Farbe\
name\
Punkte

+++

+++learningObject

**Attribute**
authorNames\
dateCreated\
datePublished\
dateUpdated\
effectivenessIndex\
enrollmentType\
id\
imageUrl\
isExternal\
isSubLoOrderEnforce\
loType\
Status\
Tags

**Beziehungen**
authors(user)\
enrollment(learningObjectInstanceEnrollment)\
instances(learningObjectInstance)\
prerequisiteLOs(learningObject)\
skills(learningObjectSkill)\
subLOs(learningObject)\
additionalLOs(learningObject)\
additionalResources(resource)

+++

+++learningObjectInstance

**Attribute**
completeDeadline\
dateCreated\
enrollmentCount\
id\
isDefault\
seatLimit\
Status\
Gültigkeit

**Beziehungen**
badge(badge)\
l1FeedbackInfo(feedbackInfo)\
learningObject(learningObject)\
loResources(learningObjectResource)\
localizedMetadata(localizationMetadata)\
subLoInstances(learningObjectInstance)

+++

+++learningObjectInstanceEnrollment

**Attribute**
dateCompleted\
dateEnrolled\
dateStarted\
hasPassed\
id\
progressPercent\
Partitur\
Status

**Beziehungen**
learner(user)\
learnerBadge(userBadge)\
learningObject(learningObject)\
loInstance(learningObjectInstance)\
loResourceGrades(learningObjectResourceGrade)

+++

+++learningObjectResource

**Attribute**
externalReporting\
id\
loResourceType\
resourceType\
Version

**Beziehungen**
learningObject(learningObject)\
loInstance(learningObjectInstance)\
localizedMetadata(localizationMetadata)\
resources(resource)

+++

+++learningObjectResourceGrade

**Attribute**
dateCompleted\
dateStarted\
dateSuccess\
Dauer\
hasPassed\
id\
progressPercent\
Partitur

**Beziehungen**
loResource(learningObjectResource)

+++

+++learningObjectSkill

**Attribute**
Abspann\
id\
**Beziehungen**
learningObject(learningObject)\
skillLevel(skillLevel)

+++

+++recommendation

**Attribute**
id\
Grund

**Beziehungen**
learningObject(learningObject)

+++

+++resource

**Attribute**
authorWunschdauer\
completeDeadline\
contentStrukturinfoUrl\
contentType\
contentZipSize\
contentZipUrl\
dateCreated\
dateStart\
wantedDuration\
downloadUrl\
extraData\
hasQuiz\
hasToc\
id\
instructorNames\
isDefault\
Gebietsschema\
Lage\
name\
onlyQuiz\
reportingInfo\
reportingType\
seatLimit

+++

+++skill

**Attribute**
Beschreibung\
id\
name\
Status

**Beziehungen**
levels(skillLevel)

+++

+++skillLevel

**Attribute**
id\
waagerecht\
maxCredits\
name\
**Beziehungen**
badge(badge)\
skill(skill)

+++

+++user

**Attribute**
avatarUrl\
Biografie\
contentLocale\
email\
Felder\
id\
name\
pointsEarned\
Profil\
Rollen\
Status\
timeZoneCode\
uiLocale

**Beziehungen**
account(account)\
manager(user)

+++

+++userBadge

**Attribute**
assertionUrl\
dateAchieved\
id\
modelType

**Beziehungen**
badge(badge)\
learner(user)\
model(learningObject)

+++

+++userCalendar

**Attribute**
Bahn\
courseType\
dateStart\
eingeschrieben\
id\
Monat\
Vierteljahr

**Beziehungen**
containerLO(learningObject)\
course(learningObject)

+++

+++userNotification

**Attribute**
actionTaken\
Rinne\
dateCreated\
id\
Nachricht\
modelIds\
modelNames\
modelTypes\
vorlesen\
Rolle

+++

+++userSkill

**Attribute**
dateAchieved\
dateCreated\
id\
pointsEarned

**Beziehungen**
learnerBadge(userBadge)\
learningObject(learningObject)\
skillLevel(skillLevel)\
user(user)

+++

## Anwendungsentwicklungsprozess {#registration}

## Voraussetzungen {#prerequisites}

Als Entwickler müssen Sie ein Testkonto auf Learning Manager erstellen, damit Sie vollen Zugriff auf alle Rollen in diesem Konto haben. Um eine Anwendung schreiben zu können, muss ein Entwickler einige Benutzer und Kurse erstellen und das Konto in einen angemessenen Zustand versetzen, damit die zu entwickelnde Anwendung auf einige Beispieldaten zugreifen kann.

## Client-ID und Geheimnis erstellen {#createclientidandsecret}

1. In **Integrationsadministrator** Anmeldung klicken Sie auf **[!UICONTROL Anwendungen]** im linken Bereich.

   ![](assets/application-development-menu.png)

   *Anwendungen im Integrations-Admin auswählen*

1. Klicken **[!UICONTROL Registrieren]** in der oberen rechten Ecke der Seite, um Ihre Anwendungsdetails zu registrieren. Die Registrierungsseite wird angezeigt.

   ![](assets/register-application.png)

   *Registrieren Sie die Anwendung*

   Es ist zwingend erforderlich, alle Felder auf dieser Seite auszufüllen.

   **Anwendungsname**: Geben Sie Ihren Anwendungsnamen ein. Es ist nicht zwingend erforderlich, denselben Anwendungsnamen zu verwenden. Es kann sich um einen beliebigen gültigen Namen handeln.

   **URL**: Wenn Sie die genaue URL kennen, unter der die Anwendung gehostet wird, können Sie sie erwähnen. Wenn Sie es nicht wissen, können Sie Ihre Unternehmens-URL erwähnen. Ein gültiger URL-Name ist in diesem Feld obligatorisch.

   **Domänen umleiten**: Geben Sie den Domänennamen der Anwendung ein, zu der die Learning Manager-Anwendung nach der OAuth-Authentifizierung umgeleitet werden soll. Sie können hier mehrere URLs erwähnen, Sie müssen jedoch die gültigen URLs verwenden, z. B. `http://google.com`, `http://yahoo.com` usw.

   **Beschreibung:** Geben Sie eine kurze Beschreibung für Ihre Anwendung ein.

   **Umfang:** Wählen Sie eine der vier verfügbaren Optionen, um den Umfang der Anwendung zu definieren. Basierend auf Ihrer hier genannten Auswahl sind die Learning Manager-API-Endpunkte für Ihre Anwendung zugänglich. Wenn Sie z. B. **Lesezugriff auf Teilnehmerrolle**&quot; sind alle Teilnehmer-API-Endpunkte des Lern-Managers schreibgeschützt für Ihre Anwendung.

   **Nur für dieses Konto?**\
   **Ja** - Wenn Sie &quot;Ja&quot; wählen, ist die Anwendung für andere Kontoadministratoren nicht sichtbar.\
   **Nein** - Wenn Sie &quot;Nein&quot; auswählen, können auch andere Kontoadministratoren auf diese Anwendung zugreifen, sie müssen jedoch die Anwendungs-ID verwenden, um auf diese Anwendung zuzugreifen. Die Anwendungs-ID wird generiert und im Bearbeitungsmodus der Learning Manager-Anwendung angezeigt.

   Wenn Sie **Lese- und Schreibzugriff auf Administratorrollen** als Geltungsbereich bei der Registrierung der Anwendung an und wählen Sie **Lesezugriff auf Administratorrolle** Beim Erstellen der APIs können Sie weiterhin Schreibzugriff auf die Anwendung haben, da der Registrierungsbereich der Anwendung den Autorisierungs-Workflow ersetzt.

1. Klicken **[!UICONTROL Registrieren]** rechts oben, nachdem Sie die Details auf der Registrierungsseite ausgefüllt haben.

## Anwendungsentwicklung und -tests {#applicationdevelopmentandtesting}

Die Learning Manager-API kann von Entwicklern zum Erstellen beliebiger Anwendungen verwendet werden. Entwickler müssen sicherstellen, dass ihre Konten aus einigen gültigen Benutzern und Kursen bestehen. Sie können einige Dummy-Benutzer und -Kurse erstellen und Aktivitäten im Testkonto simulieren, sodass sie die Funktionalität der Anwendung testen können.

## Anwendungsbereitstellung {#applicationdeployment}

Wir empfehlen, dass der Learning Manager-Administrator oder ein Integrationsadministrator für das Produktionskonto die Verantwortung dafür übernimmt, die Anwendung Benutzern in ihrem Unternehmen zur Verfügung zu stellen. Nachdem die Anwendung getestet wurde und als produktionsbereit gilt, informieren Sie den Administrator über das Produktionskonto. Idealerweise möchten die Administratoren eine neue Client-ID und ein neues Client-Secret für die Anwendung im Produktionskonto generieren und die erforderlichen Schritte ausführen, um sie auf sichere Weise in die Anwendung zu integrieren. Das tatsächliche Verfahren für die Bereitstellung von Anwendungen ist von Unternehmen zu Unternehmen unterschiedlich, und der Learning Manager-Administrator Ihres Unternehmens muss die IT-/IS-Abteilung Ihres Unternehmens um Unterstützung bitten, um die Bereitstellung abzuschließen.

## Genehmigung externer Anwendungen {#externalapplicationapproval}

Sie können externe Anwendungen hinzufügen, indem Sie auf **Genehmigen** in der oberen rechten Ecke des Fensters **Anwendungen** angezeigt. Geben Sie die ID der externen Anwendung an und klicken Sie auf **Speichern.**

![](assets/add-external-application.png)

*Hinzufügen und Genehmigen einer externen Anwendung*

## Häufig gestellte Fragen

+++Verfügt Learning Manager über eine E-Commerce-Integration?

Adobe Learning Manager verfügt nicht über eine E-Commerce-Integration. Wir bieten jedoch APIs an, damit Sie Ihr eigenes Headless LMS erstellen und E-Commerce-Funktionen implementieren können.
+++

---
jcr-language: en_us
title: Handbuch für Anwendungsentwickler
description: Die Learning Manager V1-API ist jetzt veraltet. Die V1-APIs funktionieren ab dem 28. Februar 2021 nicht mehr. Wir empfehlen Ihnen, V2-APIs zu verwenden, um mit dem Learning Manager zu interagieren.
contentowner: jayakarr
source-git-commit: efb9772aac1359601ae988d9a081d395786b44fe
workflow-type: tm+mt
source-wordcount: '3383'
ht-degree: 63%

---



# Handbuch für Anwendungsentwickler

>[!NOTE]
>
>Die Learning Manager V1-API ist jetzt veraltet. Wir empfehlen Ihnen, V2-APIs zu verwenden, um mit dem Learning Manager zu interagieren.


## Übersicht {#overview}

[Adobe Learning Manager](http://www.adobe.com/in/products/learningmanager.html) ist eine in der Cloud gehostete, auf die Kursteilnehmer zugeschnittene Selfservice-Lösung für Learning Management. Kunden können über die Learning Manager-API programmatisch auf Learning Manager-Ressourcen zugreifen, um sie in andere Unternehmensanwendungen zu integrieren. Die API kann auch von Adobes Partnern verwendet werden, um den Wertbeitrag von Learning Manager zu steigern, entweder durch Erweitern von dessen Funktionsumfang oder durch Integration in gängige Anwendungen oder Dienste.

### Anwendungsszenario {#usagescenario}

Mithilfe der Learning Manager-API können Entwickler eigenständige Anwendungen herstellen, die den Funktionsumfang von Learning Manager erweitern oder Learning Manager in Arbeitsabläufe in anderen Unternehmensanwendungen integrieren. Sie können eine Webanwendung, einen Desktop-Client oder eine mobile App mit einer beliebigen Technologie Ihrer Wahl entwickeln. Als Entwickler können Sie über Learning Manager auf Ihre Anwendungsdaten zugreifen. Die Bereitstellung der von Ihnen entwickelten Anwendung erfolgt außerhalb der Learning Manager-Plattform, und Sie haben die vollständige Kontrolle über den Lebenszyklus der Softwareentwicklung, während die Anwendung weiterentwickelt wird. Anwendungen werden üblicherweise im Unternehmen des Kunden zur Verwendung mit dessen Learning Manager-Konto entwickelt und diese Anwendungen sind „privat“, d. h. nur für dieses Kundenunternehmen verfügbar. Außerdem können Adobe-Partner mit der Learning Manager-API generische Anwendungen erstellen, die von einem breiten Spektrum von Learning Manager-Kunden verwendet werden können.

## Learning Manager-API {#apidescription}

Die Learning Manager-API basiert auf den Prinzipien von REST und stellt wichtige Elemente des Objektmodells von Learning Manager über HTTP für Anwendungsentwickler bereit. Entwickler können sich mit den verschiedenen Learning Manager-Objekten, ihren Attributen und Beziehungen vertraut machen, bevor sie die Details zu den API-Endpunkten und den HTTP-Methoden kennen. Nachdem ein zuverlässiges Verständnis der Modelle vorhanden ist, empfiehlt es sich, Grundkenntnisse der Struktur von API-Anfragen und -Antworten zu erwerben und einige häufig vorkommende Programmierungsbegriffe zu erlernen, die in der gesamten API unterstützt werden.

Ausführliche Informationen zu den verschiedenen API-Endpunkten und -Methoden finden Sie unter  [Dokumentation zur Learning Manager-API](https://learningmanager.adobe.com/docs/primeapi/v2/).

>[!IMPORTANT]
>
>Mit den Adobe Learning Manager-Teilnehmer-APIs können Sie ein benutzerdefiniertes Lernerlebnis für Ihre Benutzer erstellen. Die Verwendung dieser APIs erfordert ein gültiges Benutzertoken und darf nur für Arbeitsabläufe mit einem vollständig lizenzierten/registrierten Teilnehmer verwendet werden. Sie dürfen nicht, wie es der Fall ist, für irgendeine Art von Datenabruf verwendet werden, um nicht angemeldete Benutzer/freigegebene Benutzer oder andere solche Fälle zu unterstützen. Nicht angemeldete Nutzungsszenarien erfordern eine besondere Handhabung. Wenden Sie sich an das Team für Lösungsarchitekturen, falls Sie Fragen zur geeigneten Verwendung dieser APIs haben, und vergewissern Sie sich, dass ein Lösungsarchitekt eine Lösung überprüft hat, bevor Sie sie bereitstellen.

## API-Authentifizierung {#apiauthentication}

Wenn Sie eine Anwendung entwickeln, die API-Aufrufe an Learning Manager sendet, müssen Sie Ihre Anwendung mithilfe der Integrations-Admin-App registrieren.

Learning Manager-APIs verwenden das OAuth 2.0-Framework zum Authentifizieren und Autorisieren Ihrer Clientanwendungen.

**Vorgehensweise** 

**1. Anwendung einrichten**

Sie können die Anwendung mit der Client-ID und dem Client-Secret einrichten, um die richtigen Endpunkte zu verwenden. Nachdem Sie die Anwendung registriert haben, können Sie clientId und clientSecret abrufen. Die GET-URL sollte im Browser verwendet werden, da sie zur Authentifizierung der Learning Manager-Benutzer mit ihren vorkonfigurierten Konten wie SSO, Adobe ID usw. genutzt wird.

```
GET https://learningmanager.adobe.com/oauth/o/authorize?client_id=<Enter your clientId>&redirect_uri=<Enter a url to redirect to>&state=<Any String data>&scope=<one or more comma separated scopes>&response_type=CODE.
```

Nach erfolgreicher Authentifizierung leitet Ihr Browser Sie zu dem in der oben genannten URL angegebenen redirect_uri weiter. Ein **Parametercode** wird zusammen mit dem Umleitungs-URI angehängt.

**2. Aktualisierungstoken aus dem Code abrufen**

`POST https://learningmanager.adobe.com/oauth/token Content-Type: application/x-www-form-urlencoded`

Hauptteil der Post-Anforderung:

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

Hauptteil der Post-Anforderung:

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

Ein Zugriffstoken ist sieben Tage lang gültig. Nach einem Tag müssen Sie mithilfe des Aktualisierungstokens ein neues Zugriffstoken erstellen. Wenn Sie ein neues Zugriffstoken aus dem Aktualisierungstoken generieren, während ein vorhandenes Zugriffstoken noch gültig ist, wird das vorhandene Token zurückgegeben.

Als Referenz werden weiter unten einige in der Learning Manager-API häufig verwendete Begriffe erklärt.

**Includes**

Entwickler können sowohl auf ein einzelnes API-Objektmodell als auch auf mehrere mit diesem Modell verknüpfte Modelle zugreifen. Um auf die nachfolgenden verknüpften Modelle zuzugreifen, müssen Sie die Beziehung jedes Modells zu anderen Modellen kennen. **Umfasst** ermöglicht Entwicklern den Zugriff auf die abhängigen Modelle. Sie können mehrere Modelle durch Kommas trennen. Beispiele zur Verwendung und weitere Informationen zu **umfasst** finden Sie weitere Informationen im Abschnitt zum Beispiel-API-Modell auf dieser Seite.

**API-Anforderung**

Die API-Anfragen können über eine HTTP-Anfrage gestellt werden. Je nach Endpunkt und Methode stehen eventuell verschiedene HTTP-Verben wie GET, PUT, POST, DELETE, PATCH usw. zur Verfügung. Bei manchen Anforderungen können Abfrageparameter übergeben werden. Wenn der Benutzer eine Anforderung für ein bestimmtes Datenmodell sendet, kann er auch verknüpfte Modelle anfordern wie in den Spezifikationen für die JSON-API beschrieben. Die Struktur einer typischen API-Anforderung wird unter [Nutzungsbeispiel für Modell](#main-pars_header_1415780624) beschrieben.

**API-Antwort**

Bei einer API-Anforderung durch einen Client wird ein JSON-Dokument gemäß der JSON-API-Spezifikation abgerufen. Die Antwort enthält außerdem den HTTP-Statuscode, den der Entwickler überprüfen kann, um die entsprechenden nächsten Schritte in seiner Anwendungslogik auszuführen. Die Struktur einer typischen API-Antwort wird unter  [Beispielmodellverwendung](#main-pars_header_1415780624).

**Fehler**

Wenn eine API-Anforderung fehlschlägt, geht eine Fehlerantwort ein. Der in der Antwort zurückgegebene HTTP-Statuscode gibt die Art des Fehlers an. Fehlercodes werden für jedes Modell in der API-Referenz mit Zahlen dargestellt. 200, 204, 400 und 404 sind einige der häufigsten Fehler, die in APIs angezeigt werden und auf HTTP-Zugriffsprobleme hinweisen.

**Fields**

Die Attribute des API-Objekts und seine Beziehungen werden zusammenfassend als Felder bezeichnet. Weitere Informationen finden Sie unter [JSON API.](http://jsonapi.org/format/#document-resource-object-fields) Sie können Felder als Parameter verwenden, während Sie API-Aufrufe durchführen, um ein oder mehrere bestimmte Attribute aus dem Modell abzurufen. Wenn der Fields-Parameter fehlt, ruft der API-Aufruf alle verfügbaren Attribute aus dem Modell ab. Im folgenden API-Aufruf werden z. B. Felder[Fertigkeit]=name ruft nur das Namensattribut des Kenntnismodells ab.

https://learningmanager.adobe.com/primeapi/v2/users/{userId}/userSkills/{id}?include=skillLevel.skill&amp;fields[skill]=name

**Paginierung**

Manchmal wird in der Antwort auf eine API-Anforderung eine lange Liste von Objekten zurückgegeben. In solchen Fällen ermöglicht das Paginierungsattribut dem Entwickler, die Ergebnisse nacheinander in Form mehrerer Seiten abzurufen, wobei jede Seite einen Bereich von Datensätzen enthält. Sie können beispielsweise mit dem Paginierungsattribut in Learning Manager festlegen, wie viele Datensätze maximal auf einer Seite angezeigt werden können. Außerdem können Sie den Bereichswert von Datensätzen definieren, die auf der Seite angezeigt werden sollen.

**Paginierung**

Die Sortierung ist in API-Modellen zulässig. Wählen Sie basierend auf dem Modell die Art der Sortierung aus, die auf die Ergebnisse angewendet werden soll. Die Sortierung kann in aufsteigender oder absteigender Reihenfolge angewendet werden. Wenn Sie beispielsweise `code sort=name`aufsteigend sortiert nach Namen. Wenn Sie `code sort=-name`, es wird absteigend nach Name sortiert. Siehe [JSON-API-Spezifikation für weitere Informationen](http://jsonapi.org/format/#fetching-sorting).

## Abbildung: Verwendung der API {#samplemodel}

Lassen Sie uns ein Szenario in Betracht ziehen, in dem ein Entwickler den Namen der Kenntnisse, die für die Kenntnisstufe zugewiesenen Höchstpunkte und die vom Teilnehmer für diese Kenntnisse gesammelten Punkte abrufen möchte.

Ein userSkill-Modell in Learning Manager-APIs umfasst standardmäßig die Attribute id, type, dateAchieved, dateCreated und pointsEarned. Wenn ein Entwickler die GET-Methode verwendet, um Details des userSkill-Modells abzurufen, werden die aktuellen Daten für die Standardattribute in der Antwortausgabe angezeigt.

In diesem Szenario möchte der Entwickler jedoch den Kenntnisnamen und die Punkte des Teilnehmers für eine Kenntnisstufe abrufen. In der Learning Manager-API können Sie auf diese verknüpften Informationen über Beziehungsfelder und Include-Parameter zugreifen. Die verknüpften Modelle für userSkill werden im Beziehungs-Tag abgerufen. Sie können die Details aller verknüpften Modelle abrufen, indem Sie diese Modelle zusammen mit userSkill aufrufen. Um diese Informationen abzurufen, verwenden Sie **`code include`** Parameter mit durch Punkte (Punkte) getrennten Werten für jedes der zugehörigen Modelle. Sie können Komma als Trennzeichen verwenden, um ein anderes Modell anzufordern, z. B. user include=skillLevel.skill,course

**API-Aufruf**

`https://learningmanagerqe1.adobe.com/primeapi/v1/users/%7buserId%7d/userSkills/%7bid%7d?include=skillLevel.skill&fields%5bskill%5d=name&fields%5bskillLevel%5d=maxCredits&fields%5buserSkill%5d=pointsEarned`

Beispiel: userId könnte den Wert 746783 annehmen, userSkills id: 746783_4426_1.

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

Mit der Learning Manager-API können Entwickler auf Learning Manager-Objekte als RESTful-Ressourcen zugreifen. Jeder API-Endpunkt stellt eine Ressource dar, typischerweise eine Instanz eines Objekts, etwa ein Abzeichen, oder eine Gruppe solcher Objekte. Die Entwickler können dann mithilfe von HTTP-Verben wie PUT, GET, POST und DELETE die CRUD-Operationen für diese Objekte bzw. Gruppen durchführen.

+++V1-API

Die folgende Grafik zeigt die verschiedenen Elemente des Learning Manager-Objektmodells in V1 API.

![](assets/er-diag-primemodels.png)

In der folgenden Tabelle werden verschiedene Elemente des Lern-Manager V1-Objektmodells beschrieben:

<table border="1" cellspacing="0" cellpadding="0">
 <tbody>
  <tr>
   <td>
    <p><strong>Seriennummer</strong></p></td>
   <td>
    <p><strong>Learning Manager-Objekt</strong></p></td>
   <td>
    <p><strong>Beschreibung</strong></p></td>
  </tr>
  <tr>
   <td>
    <p>1.      </p></td>
   <td>
    <p>Benutzer</p></td>
   <td>
    <p>Der Benutzer (user) ist das wichtigste Modell in Learning Manager. Die Benutzer sind typischerweise die internen oder externen Teilnehmer in einer Organisation und nutzen Lernobjekte. Sie können jedoch außer der Teilnehmerrolle auch andere Rollen wie z. B. Autor oder Manager haben. „User id“, „type“ und „email“ gehören zu den Inline-Attributen. </p></td>
  </tr>
  <tr>
   <td>
    <p>2.      </p></td>
   <td>
    <p>Kurs</p></td>
   <td>
    <p>Ein Kurs (course) ist eines der in Learning Manager unterstützten Lernobjekte. Er besteht aus einem oder mehreren Modulen. </p></td>
  </tr>
  <tr>
   <td>
    <p>3.      </p></td>
   <td>
    <p>module</p></td>
   <td>
    <p>Ein Modul (module) ist ein Baustein zum Erstellen von Lernobjekten in Learning Manager. Es gibt vier verschiedene Typen von Modulen: wie Klassenzimmer, virtuelles Klassenzimmer, Aktivität und Selbststudium. Verwenden Sie dieses Modulmodell, um Details aller Module in einem Konto abzurufen. </p></td>
  </tr>
  <tr>
   <td>
    <p>4.      </p></td>
   <td>
    <p>certification</p></td>
   <td>
    <p>Die Zertifizierung (certification) wird den Teilnehmern nach erfolgreichem Abschluss eines Kurses verliehen. In der Anwendung müssen Kurse vorhanden sein, bevor Sie Zertifizierungen verwenden können. </p></td>
  </tr>
  <tr>
   <td>
    <p>5.      </p></td>
   <td>
    <p>learning program</p></td>
   <td>
    <p>Lernprogramme (learning program) sind speziell entwickelte Kurse für den spezifischen Lernbedarf von Benutzern. In der Regel werden Lernprogramme verwendet, um Lernziele zu erreichen, die mehrere einzelne Kurse umfassen. </p></td>
  </tr>
  <tr>
   <td>
    <p>6.      </p></td>
   <td>
    <p>badge</p></td>
   <td>
    <p>Ein Abzeichen (badge) erhalten Teilnehmer als Anerkennung, wenn sie während der Arbeit an einem Kurs bestimmte Meilensteine erreichen. </p></td>
  </tr>
  <tr>
   <td>
    <p>7.      </p></td>
   <td>
    <p>skill</p></td>
   <td>
    <p>Das Modell für Kenntnisse (skill) setzt sich aus Stufen und Punktzahlen zusammen. Die Teilnehmer erwerben Kenntnisse durch Abschließen der relevanten Kurse. </p></td>
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
    <p>Ein Lernprogramm kann aus mehreren Instanzen bestehen, die ähnliche Eigenschaften eines Lernprogramms aufnehmen oder benutzerdefiniert sein können. </p></td>
  </tr>
  <tr>
   <td>
    <p>14.  </p></td>
   <td>
    <p>job aid</p></td>
   <td>
    <p>Die Arbeitshilfen (job aid) sind Lerninhalte, die Teilnehmern ohne Registrierung oder Abschlusskriterien zur Verfügung stehen. Sie können Informationen zu Aktualisierungsdatum, Status und ID sowie verknüpfte Modelle wie die Version der Arbeitshilfe, Autoren und Kenntnisstufe abrufen. </p></td>
  </tr>
  <tr>
   <td>
    <p>15.  </p></td>
   <td>
    <p>jobAidVersion</p></td>
   <td>
    <p>Zu einer Arbeitshilfe können je nach Anzahl der Überarbeitungen ihre Inhalts und der Anzahl der Uploads eine oder mehrere Versionen gehören. Dieses Modell enthält Details einer einzelnen Version der Arbeitshilfe. </p></td>
  </tr>
  <tr>
   <td>
    <p>16.  </p></td>
   <td>
    <p>learningProgramInstanceEnrollment</p></td>
   <td>
    <p>Ein Lernprogramm besteht aus einer oder mehreren Instanzen. Teilnehmer können sich selbst zu einer Lernprogramminstanz anmelden oder vom Administrator zugewiesen werden. Dieses Modell enthält Details zur Registrierung eines Benutzers für eine einzelne Lernprogramminstanz. </p></td>
  </tr>
  <tr>
   <td>
    <p>17.  </p></td>
   <td>
    <p>moduleVersion</p></td>
   <td>
    <p>Für ein Modul können eine oder mehrere Versionen vorhanden sein, je nachdem, wie oft überarbeiteter Inhalt hochgeladen wurde. Verwenden Sie dieses Modell, um spezifische Informationen zu einer einzelnen Modulversion zu erhalten. </p></td>
  </tr>
  <tr>
   <td>
    <p>18.  </p></td>
   <td>
    <p>skillLevel</p></td>
   <td>
    <p>Eine Kenntnisstufe besteht aus einem oder mehreren Kursen, die bearbeitet werden müssen, um die Stufe und die dazugehörige Punktzahl zu erreichen. </p></td>
  </tr>
  <tr>
   <td>
    <p>19.  </p></td>
   <td>
    <p>userBadge</p></td>
   <td>
    <p>UserBadge verbindet ein einzelnes Abzeichen mit einem einzelnen Benutzer. Es enthält Details wie etwa den Zeitpunkt, zu dem es erreicht wurde, assertionUrl usw. </p></td>
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
   <th><b>Learning Manager-Objekt</b></th>
   <th><b>Beschreibung</b></th>
  </tr>
  <tr>
   <td>account</td>
   <td>Kapselt die Details eines Learning Manager-Kunden.</td>
  </tr>
  <tr>
   <td><code>
     badge
    </code></td>
   <td>Ein Abzeichen (badge) erhalten Teilnehmer als Anerkennung, wenn sie während der Arbeit an einem Kurs bestimmte Meilensteine erreichen. <br></td>
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
   <td>Der Benutzer (user) ist das wichtigste Modell in Learning Manager. Die Benutzer sind typischerweise die internen oder externen Teilnehmer in einer Organisation und nutzen Lernobjekte. Sie können jedoch außer der Teilnehmerrolle auch andere Rollen wie z. B. Autor oder Manager haben. „User id“, „type“ und „email“ gehören zu den Inline-Attributen. </td>
  </tr>
  <tr>
   <td>resource</td>
   <td>Dies wird verwendet, um jede Inhaltsressource zu modellieren, die ein Modul einbeziehen will. Alle Ressourcen, die in <code>
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
   <td>skill</td>
   <td>Das Modell für Kenntnisse (skill) setzt sich aus Stufen und Punktzahlen zusammen. Die Teilnehmer erwerben Kenntnisse durch Abschließen der relevanten Kurse. <br></td>
  </tr>
  <tr>
   <td>skillLevel</td>
   <td>Eine Kenntnisstufe besteht aus einem oder mehreren Kursen, die bearbeitet werden müssen, um die Stufe und die dazugehörige Punktzahl zu erreichen. <br></td>
  </tr>
  <tr>
   <td>learningObject</td>
   <td>Ein Lernobjekt ist ein Abstrakt für verschiedene Arten von Objekten, bei denen sich Benutzer anmelden und von denen sie lernen können. Derzeit verfügt der Lern-Manager über die vier Typen von Lernobjekten - Kurs, Zertifizierung, Lernprogramm <code>
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
   <td>Dies umfasst das Ergebnis des Benutzers, der eine bestimmte Ressource im Kontext eines Lernobjekts konsumiert, bei dem er angemeldet ist. Es enthält Informationen wie die von <code>
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
   <td>L1 Feedback enthält die Antworten, die von einem Teilnehmer für die Feedbackfragen gegeben werden, die Lernobjekten zugeordnet sind. In der Regel wird dies erfasst, nachdem der Benutzer ein Lernobjekt abgeschlossen hat, wenn konfiguriert, um ein solches Feedback von Teilnehmern zu erfassen.<br></td>
  </tr>
  <tr>
   <td>Registrierung<br></td>
   <td>Dieses Abstrakt umfasst die Einzelheiten der Transaktion, die die Zuordnung eines bestimmten Benutzers zu einer bestimmten Lernobjektinstanz darstellt.<br></td>
  </tr>
 </tbody>
</table>

+++

Liste der Objektattribute und -beziehungen

+++account

**Attribute**
dateCreated\
gamificationEnabled\
-ID\
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
-ID\
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
-ID\
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
-ID\
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
-ID\
progressPercent\
Ergebnis\
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
-ID\
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
-ID\
progressPercent\
Ergebnis

**Beziehungen**
loResource(learningObjectResource)

+++

+++learningObjectSkill

**Attribute**
Abspann\
-ID\
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
-ID\
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
-ID\
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
E-Mail\
Felder\
-ID\
name\
pointsEarned\
profile\
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
-ID\
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
-ID\
Monat\
Quartal

**Beziehungen**
containerLO(learningObject)\
course(learningObject)

+++

+++userNotification

**Attribute**
actionTaken\
Rinne\
dateCreated\
-ID\
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
-ID\
pointsEarned

**Beziehungen**
learnerBadge(userBadge)\
learningObject(learningObject)\
skillLevel(skillLevel)\
user(user)

+++

## Anwendungsentwicklungsprozess {#registration}

## Voraussetzungen {#prerequisites}

Als Entwickler müssen Sie ein Testkonto bei Learning Manager erstellen, damit Sie vollen Zugriff auf alle Rollen in diesem Konto haben. Um eine Anwendung entwickeln zu können, muss ein Entwickler einige Benutzer und Kurse erstellen und das Konto in einen funktionsfähigen Zustand versetzen, damit Beispieldaten vorhanden sind, auf die die zu entwickelnde Anwendung zugreifen kann.

## Client-ID und Secret erstellen {#createclientidandsecret}

1. In **Integrationsadministrator** Anmeldung klicken Sie auf **[!UICONTROL Anwendungen]** im linken Bereich.

   ![](assets/application-development-menu.png)

   *Anwendungen im Integrations-Admin auswählen*

1. Klicken **[!UICONTROL Registrieren]** in der oberen rechten Ecke der Seite, um Ihre Anwendungsdetails zu registrieren. Die Registrierungsseite wird angezeigt.

   ![](assets/register-application.png)

   *Registrieren Sie die Anwendung*

   Alle Felder auf dieser Seite müssen ausgefüllt werden.

   **Anwendungsname**: Geben Sie den Namen Ihrer Anwendung ein. Es ist nicht zwingend erforderlich, denselben Anwendungsnamen zu verwenden. Es kann sich um einen beliebigen gültigen Namen handeln.

   **URL**: Wenn Sie die genaue URL kennen, auf der die Anwendung gehostet wird, können Sie sie angeben. Wenn Sie sie nicht kennen, können Sie Ihre Firmen-URL angeben. Ein gültiger URL-Name ist in diesem Feld obligatorisch.

   **Domänen umleiten**: Geben Sie den Domänennamen der Anwendung ein, zu der die Learning Manager-Anwendung nach der OAuth-Authentifizierung umleiten soll. Sie können hier mehrere URLs erwähnen, Sie müssen jedoch die gültigen URLs verwenden, z. B. `http://google.com`, `http://yahoo.com` usw.

   **Beschreibung:** Geben Sie eine kurze Beschreibung für Ihre Anwendung ein.

   **Umfang:** Wählen Sie eine der vier verfügbaren Optionen, um den Umfang der Anwendung zu definieren. Die hier von Ihnen gewählte Option bestimmt, wie Ihre Anwendung auf die Learning Manager-API-Endpunkte zugreifen kann. Wenn Sie z. B. **Lesezugriff auf Teilnehmerrolle**&quot; sind alle Teilnehmer-API-Endpunkte des Lern-Managers schreibgeschützt für Ihre Anwendung.

   **Nur für dieses Konto?**\
   **Ja** - Wenn Sie &quot;Ja&quot; wählen, ist die Anwendung für andere Kontoadministratoren nicht sichtbar.\
   **Nein** - Wenn Sie &quot;Nein&quot; auswählen, können auch andere Kontoadministratoren auf diese Anwendung zugreifen, sie müssen jedoch die Anwendungs-ID verwenden, um auf diese Anwendung zuzugreifen. Die Anwendungs-ID wird generiert und im Bearbeitungsmodus der Learning Manager-Anwendung angezeigt.

   Wenn Sie **Lese- und Schreibzugriff auf Administratorrollen** als Geltungsbereich bei der Registrierung der Anwendung an und wählen Sie **Lesezugriff auf Administratorrolle** Beim Erstellen der APIs können Sie weiterhin Schreibzugriff auf die Anwendung haben, da der Registrierungsbereich der Anwendung den Autorisierungs-Workflow ersetzt.

1. Klicken Sie oben rechts auf **[!UICONTROL Registrieren]**, nachdem Sie die Details auf der Registrierungsseite ausgefüllt haben.

## Anwendungsentwicklung und Tests {#applicationdevelopmentandtesting}

Mithilfe der Learning Manager-API können Entwickler beliebige Anwendungen erstellen. Entwickler müssen sicherstellen, dass ihre Konten aus einigen gültigen Benutzern und Kursen bestehen. Sie können einige Testbenutzer und -kurse erstellen und Aktivitäten im Testkonto simulieren, um die Funktionsfähigkeit der Anwendung zu prüfen.

## Anwendungsbereitstellung {#applicationdeployment}

Wir empfehlen, dass der Learning Manager-Administrator oder ein Integrationsadministrator für das Produktionskonto die Verantwortung für die Bereitstellung der Anwendung für die Benutzer im Unternehmen übernimmt. Sobald die Anwendung getestet wurde und als produktionsbereit betrachtet wird, informieren Sie den Administrator bezüglich des Produktionskontos. Im Idealfall entscheiden die Administratoren, im Produktionskonto eine neue Client-ID und ein neues Client-Secret für die Anwendung zu generieren, und führen die nötigen Schritte aus, um sie auf sichere Weise in die Anwendung zu integrieren. In der Praxis ist das Verfahren zum Bereitstellen von Anwendungen in jedem Unternehmen unterschiedlich, und der Learning Manager-Administrator in Ihrem Unternehmen benötigt für die Bereitstellung Unterstützung durch die IT/IS-Abteilung.

## Genehmigung externer Anwendungen {#externalapplicationapproval}

Sie können externe Anwendungen hinzufügen, indem Sie auf **Genehmigen** in der oberen rechten Ecke des Fensters **Anwendungen** angezeigt. Geben Sie die ID der externen Anwendung an und klicken Sie auf **Speichern**.

![](assets/add-external-application.png)

*Hinzufügen und Genehmigen einer externen Anwendung*

## Häufig gestellte Fragen

+++Verfügt Learning Manager über eine E-Commerce-Integration?

Adobe Learning Manager verfügt über keine E-Commerce-Integration. Wir bieten jedoch APIs an, damit Sie Ihr eigenes Headless-LMS erstellen und E-Commerce-Funktionen implementieren können.
+++

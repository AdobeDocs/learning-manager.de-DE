---
jcr-language: en_us
title: API-Dokumentation zur eingebetteten Player-Interaktion
description: Erfahren Sie mehr über verschiedene APIs zum Abhören von Ereignissen und Auslösen von Aktionen im eingebetteten Player
contentowner: chandrum
exl-id: 4734ecc1-cc8a-40b0-8997-32a31ec661ec
source-git-commit: 3d183dc40e4d1962d25160b74d8cf6cfa26e3171
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 69%

---

# API-Dokumentation zur eingebetteten Player-Interaktion

Adobe Learning Manager bietet eine Bibliothek, die in eine App integriert werden kann. Diese Bibliothek bietet verschiedene APIs, um Ereignisse zu überwachen und Aktionen im eingebetteten Player auszulösen.

Mithilfe der bereitgestellten APIs können Sie andere Aktionen für den Player wiedergeben, anhalten und ausführen.

## Bibliothek laden

Die Bibliothek ist an diesem [Speicherort](https://cpcontents.adobe.com/public/publiccdn/playerInteractionLib.min.js) verfügbar.

Führen Sie die untengenannten Schritte aus, um die Bibliothek zu laden:

1. Laden Sie die JS-Datei in die Nutzeranwendung.
2. Beim Laden der Bibliothek wird window.cpPlayerLib aufgefüllt.

>[!NOTE]
>
>Wenn Sie nicht prod US verwenden, legen Sie die Parameter cpPlayerLib.env und cpPlayerLib.sourceOrigin basierend auf Ihrer env fest.

Die Standardwerte sind:

* window.cpPlayerLib.env = [https://learningmanager.adobe.com/app/player](https://learningmanager.adobe.com/app/player);
* window.cpPlayerLib.sourceOrigin = &quot;[https://cpcontents.adobe.com](https://cpcontents.adobe.com/)&quot;;

### Verfügbare Methoden

Die Bibliothek cpPlayerLib besteht aus den folgenden Funktionen:

**startPlayer**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>startPlayer</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Lädt einen Player in die App.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>loId: Die Lernobjekt-ID.</li><li>accountId: Die Konto-ID des ALM-Kontos.</li><li>userId: Die Benutzer-ID.</li><li>accessToken: Das Zugriffstoken.</li><li>domRefId: Die ID des div-Containers, in dem der Player gerendert werden muss.</li><li>onModuleLoaded: Diese Funktion wird aufgerufen, wenn die Module mit den folgenden Details geladen werden.</li><br><li>contentType</li><li>loID</li><li>moduleId</li><li>completed</li><li>currentLanguage</li><li>availableLanguages</li><li>isCCAvailable</li><li>ccEnabled</li></br></td>
</tr>
<tr>
<td>Rückgabe</td>
<td>Gibt ein Versprechen zurück. Nach Auflösung des Versprechens wird ein playerObj bestanden.</td>
</tr>
<tr>
<td>Ausnahme</td>
<td>Das Versprechen führt zu einer Ausnahme.</td>
</tr>
<tr>
<td>Beispielcode</td>
<td>cpPlayerLib.startPlayer(loId, accountId, userId, accessToken, domRefId, onModuleLoaded).then(playerObj) =&gt; {//playerObj verfügt über die APIs für die Interaktion mit dem Player}) &gt;</td>
</tr>
</tbody>
</table>

**getAllPlayers**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>getAllPlayers</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Gibt alle Player-Objekte auf der aktuellen Seite zurück.</td>
</tr>
<tr>
<td>Parameter</td>
<td>Ohne</td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>cpPlayerLib.getAllPlayers()</td>
</tr>
</tbody>
</table>

**getPlayer**


<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>getPlayer</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Gibt ein Playerobjekt mit der angegebenen Lernobjekt-ID zurück.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>loId: Die Lernobjekt-ID.</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>cpPlayerLib.getPlayer(loId)</td>
</tr>
</tbody>
</table>

**navigateToModule**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>navigateToModule</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Zum nächsten Modul navigieren.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>moduleId: Die Modul-ID.</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.navigateToModule(moduleID)</td>
</tr>
</tbody>
</table>

**Weiter**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>next</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Zum nächsten Modul navigieren.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>Ohne</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.next()</td>
</tr>
</tbody>
</table>

**Zurück**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>previous</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Zum vorherigen Modul navigieren.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>Ohne</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.previous()</td>
</tr>
</tbody>
</table>

**toggleTOC**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>toggleTOC</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Das Inhaltsverzeichnisfenster auf dem Player umschalten.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>Ohne</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.toggleTOC()</td>
</tr>
</tbody>
</table>

**toggleNotes**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>toggleNotes</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Das Bedienfeld „Anmerkungen“ auf dem Player umschalten.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>Ohne</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.toggleNotes()</td>
</tr>
</tbody>
</table>

**toggleClosedCaption**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>toggleClosedCaption</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Schalten Sie die Anzeige von Untertiteln im Player um.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>Ohne</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.toggleClosedCaption()</td>
</tr>
</tbody>
</table>

**changeLanguage**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>changeLanguage</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Ändern Sie die Sprache des Inhalts auf dem Player.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>language: Der anzugebende Sprachcode.</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.changeLanguage("es")</td>
</tr>
</tbody>
</table>

**closePlayer**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>closePlayer</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Schließen Sie den Player und entfernen Sie ihn von der Seite. </td>
</tr>
<tr>
<td>Parameter</td>
<td><li>Ohne</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.closePlayer()</td>
</tr>
</tbody>
</table>

**togglePlayPause**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>togglePlayPause</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Wechseln Sie zwischen Wiedergabe und Pause des Inhalts auf dem Player.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>Ohne</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.togglePlayPause()</td>
</tr>
</tbody>
</table>

**setVolume**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>setVolume</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Die Lautstärke des Players festlegen. Der Wert muss zwischen 0 und 1 liegen.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>volume: Der Wert für die Lautstärke. Der gültige Bereich liegt zwischen 0 und 1. </li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.setVolume(0.5)</td>
</tr>
</tbody>
</table>

**setPlayBackSpeed**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>setPlayBackSpeed</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Legen Sie die Geschwindigkeit der Wiedergabe im Player fest.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>speed: Der Wert der anzugebenden Geschwindigkeit. Gültige Werte sind .25, .5, .75, 1, 1.25, 1.5, 1.75, 2.</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.setPlayBackSpeed(1.25)</td>
</tr>
</tbody>
</table>

**Suchen**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>seek</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Zu einem beliebigen Zeitpunkt im Video springen.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>time: Der Zeitpunkt, zu dem gesprungen werden soll. Die Zeit wird in Sekunden angegeben.</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.seek(50)</td>
</tr>
</tbody>
</table>

**Vorwärts**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>forward</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Im Video 10 Sekunden vorwärts springen.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>Ohne</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.forward()</td>
</tr>
</tbody>
</table>

**rückwärts**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>backward</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Im Video 10 Sekunden rückwärts springen.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>Ohne</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.backward()</td>
</tr>
</tbody>
</table>

**navigateToPage**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>navigateToPage</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Zur angegebenen Seite der PPT-/PDF-Datei wechseln.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>pageNumber: Die Seitennummer, zu der gewechselt werden soll.</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.navigateToPage (5)</td>
</tr>
</tbody>
</table>

**nextPage**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>nextPage</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Zur nächsten Seite der PPT-/PDF-Datei wechseln.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>Ohne</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.nextPage()</td>
</tr>
</tbody>
</table>

**vorherigeSeite**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>previousPage</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Zur vorherigen Seite der PPT-/PDF-Datei wechseln.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>Ohne</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.previousPage()</td>
</tr>
</tbody>
</table>

**zoomIn**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>zoomIn</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Den Inhalt einer PPT-/PDF-Datei vergrößern.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>Ohne</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.zoomIn()</td>
</tr>
</tbody>
</table>

**zoomOut**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>zoomOut</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Den Inhalt einer PPT-/PDF-Datei verkleinern.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>Ohne</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.zoomOut()</td>
</tr>
</tbody>
</table>

**downloadJobAid**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>downloadJobAid</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Laden Sie eine Arbeitshilfe aus einem Kurs herunter.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>Ohne</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.downloadJobAid()</td>
</tr>
</tbody>
</table>

**toggleJobAidPullout**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>toggleJobAidPullout</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Gibt an, ob Sie eine Arbeitshilfe herunterladen möchten.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>Ohne</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.toggleJobAidPullout()</td>
</tr>
</tbody>
</table>

**fullScreen**

<table>
<tbody>
<tr>
<td>Methodenname</td>
<td>fullScreen</td>
</tr>
<tr>
<td>Beschreibung</td>
<td>Stellen Sie den Player auf den Vollbildmodus ein.</td>
</tr>
<tr>
<td>Parameter</td>
<td><li>Ohne</li></td>
</tr>
</tr>
<tr>
<td>Beispielcode</td>
<td>playerObj.fullScreen()</td>
</tr>
</tbody>
</table>

## Liste der Ereignisse

**onPlayerEvents(callBack)**

Bei der Registrierung wird die Rückruffunktion bei allen Player-Ereignissen aufgerufen. Die Ereignisnamen lauten wie folgt:

* PLAY (Video/Audio/CP)
* PAUSE (Video/Audio/CP)
* TIMEUPDATE (Video/Audio/CP)
* PAGECHANGE (PPT/PDF)
* NOTEADDED (Alle Inhalte)
* LAUNCHED (Alle Inhalte)
* STARTED (Alle Inhalte)
* COMPLETED (Alle Inhalte)
* PASSED (Alle Inhalte)
* FAILED (Alle Inhalte)

**onStreamingEvents(callBack)**

Bei der Registrierung wird die Rückruffunktion für alle Player-Anweisungen aufgerufen, die zur Verfolgung der Benutzeraktivität gesendet werden.

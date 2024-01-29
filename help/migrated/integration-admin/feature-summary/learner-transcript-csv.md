---
jcr-language: en_us
title: Teilnehmertranskript-CSV interpretieren
description: Teilnehmertranskript-CSV interpretieren
contentowner: saghosh
preview: true
source-git-commit: fba5e5ddc1964b485be473bf356806f234688cf4
workflow-type: tm+mt
source-wordcount: '2997'
ht-degree: 0%

---



# Teilnehmertranskript-CSV interpretieren

Das Teilnehmertranskript ist einer der beliebtesten Berichte, die im Adobe-Lernmanager verwendet werden. Mit diesem Bericht lassen sich nahezu alle Details in einem einzigen Bericht im CSV-Format abrufen.

Der Bericht ist nicht nur ein Bericht, den Benutzer abrufen können, um das Lernverhalten zu verfolgen und zu analysieren, sondern er kann auch als das Format angesehen werden, in dem der Lern-Manager eingerichtet werden kann, um Daten über das Lernverhalten in externe Anwendungen/Systeme zu exportieren.

Ein typisches Unternehmensszenario besteht darin, regelmäßig ein Teilnehmertranskript für Learning Manager zu exportieren, es zu analysieren und Teilnehmer zu extrahieren, die ein wichtiges Lernprogramm abschließen, und einen Geschenkgutschein zu bestellen, um zeitnahe Abschlüsse zu erkennen und zu belohnen.

Ein weiterer Anwendungsfall besteht darin, die Lernverhaltensdaten einem Enterprise Data Warehouse hinzuzufügen, in dem man möglicherweise Lerndaten mit anderen Unternehmensdaten kombinieren möchte, um die Zusammenhänge zwischen Lernverhalten und anderen Prozessdaten zu analysieren.

Im restlichen Dokument wird kurz beschrieben, wie Sie das Teilnehmertranskript vom Learning Manager abrufen können. Anschließend erfahren Sie, wie die einzelnen Zeilen und Spalten des Berichts interpretiert werden.

Diese Informationen können für jeden Entwickler nützlich sein, der beabsichtigt, den Lern-Manager durch Verarbeitung der exportierten Teilnehmertranskriptdaten in andere Systeme zu integrieren.

## Teilnehmertranskript über die Benutzeroberfläche abrufen {#fetchlearnertranscriptfromtheuserinterface}

Über die Profileinstellungen kann ein Teilnehmer sein Transkript herunterladen. Weitere Informationen finden Sie unter *** [Teilnehmertranskript herunterladen](../../administrators/feature-summary/learner-transcripts.md)***.

Administratoren können Teilnehmertranskripte für das gesamte Unternehmen, für eine bestimmte Benutzergruppe oder für eine bestimmte Gruppe von Lernobjekten bzw. für eine bestimmte Gruppe von Benutzern und Lernobjekten generieren. Sie können auch alle Lerndatensätze für eine Zeitintervalldauer abrufen und angeben, ob Informationen auf Modulebene erforderlich sind (Informationen auf Modulebene werden standardmäßig weggelassen). Weitere Informationen finden Sie unter [***Teilnehmertranskripte herunterladen***](../../administrators/feature-summary/learner-transcripts.md).

<!--Update above link?-->

Administratoren können das System auch so einrichten, dass das Teilnehmertranskript regelmäßig per E-Mail gesendet wird.

Das über die Benutzeroberfläche generierte Teilnehmertranskript ist eine Excel-Datei, die auch das &quot;Kenntnistranskript&quot; enthält. Dieses Dokument befasst sich auf den Inhalt im CSV-Format, also auf den Bericht mit Lernaktivitäten im Hinblick auf Registrierung, Beginn, Fortschritt oder Abschluss eines Lernobjekts.

## Teilnehmertranskript exportieren {#exportlearnertranscript}

Wenn das Teilnehmertranskript von einem externen System verwendet werden muss, stellt der Lern-Manager eine Funktion mit dem Namen &quot;Daten exportieren&quot; bereit, wobei das Teilnehmertranskript einer der Datentypen ist, die exportiert werden können. Wie in der Präambel erläutert, ist dies für die Integration von Learning Manager in ein externes System erforderlich, das Lernverhaltensdaten verarbeiten muss, oder für die Befüllung eines Enterprise Data Warehouse mit Lernverhaltensdaten.

Weitere Informationen zur Unterstützung des Teilnehmertranskript-Exports durch die Connectors finden Sie unter [Abschnitt &quot;Daten exportieren&quot;](/help/migrated/integration-admin/feature-summary/connectors.md) in den FTP-, Box- und PowerBI-Connectors.

Diese Connectors dienen dazu, Daten regelmäßig (einmal alle n Tage) in eine nachgelagerte Anwendung zu exportieren. Diese Connectors exportieren also bei jedem Durchlauf nur die inkrementellen Lernverhaltensdaten. Beachten Sie, dass diese Connectors das Abrufen von Datensätzen nicht zulassen, die sich auf eine bestimmte Untergruppe von Benutzern oder Lernobjekten beziehen - es handelt sich immer um Daten über alle Benutzer und alle Lernobjekte in diesem Konto.

Bei PowerBI sollte der Kunde einen Arbeitsbereich bereitstellen, in dem Learning Manager diese Daten inkrementell in ein dynamisch erstelltes Dataset exportieren kann. Dieser Connector exportiert lediglich Daten, und die Kunden müssen bei Bedarf eigene Berichte/Dashboards auf der Grundlage dieses Datensatzes erstellen.

Im nächsten Abschnitt wird erläutert, wie ein nachgelagertes System die Datensätze im Teilnehmertranskript interpretieren soll.

## Teilnehmertranskript interpretieren {#interpretthelearnertranscript}

Jede Zeile in einem Teilnehmertranskript kann als ein Lernverhalten betrachtet werden, das in einem bestimmten Zeitraum im Lernmanager erfasst wurde. In der Regel exportieren die Connectors &quot;inkrementelle Daten&quot;, sodass die Zeilen Lernaktivitäten darstellen, die zwischen der letzten und der aktuellen Ausführung des Connectors stattgefunden haben.

Natürlich können Sie über die Connectors auch das Teilnehmertranskript nach Bedarf abrufen. In diesem Fall kann der Benutzer ein Startdatum angeben, und als Enddatum wird der jetzige Zeitpunkt angenommen. In der Regel wird dieser Vorgang nur einmal durchgeführt, und anschließend wird der Connector für den Export des inkrementellen Teilnehmertranskripts alle n Tage zu einer bestimmten Tageszeit eingerichtet (der Standardwert von N ist 1).

Im Folgenden soll definiert werden, was ein inkrementelles Teilnehmertranskript ist.

Im Teilnehmertranskript stellt jede Zeile eine bestimmte Aktivität mit einem bestimmten Teilnehmer und einem bestimmten Lernobjekt dar. Hier ist hauptsächlich der Status eines Teilnehmers in Bezug auf das Lernobjekt interessant: **Registriert**, **Begonnen**, **In Bearbeitung** und **Abgeschlossen**. Daher werden im Teilnehmertranskript auch vier entsprechende Datumsangaben erfasst.

Es gibt nun drei Arten von Lernobjekten, bei denen der Lern-Manager den Fortschritt der Teilnehmer verfolgt. Die exportierten Daten enthalten Fortschrittsinformationen auf Modulebene, also zur detailliertesten Inhaltseinheit, die ein Teilnehmer im Lern-Manager erleben kann.

* **Kurs** - Zusammenstellung eines oder mehrerer Module
* **Lernprogramm** - Zusammenstellung eines oder mehrerer Kurse
* **Zertifizierung** - Zusammenstellung eines oder mehrerer Kurse.

Jede Zeile im Teilnehmertranskript kann die Interaktion eines bestimmten Benutzers mit einem Modul, einem Kurs, einem Lernprogramm oder einer Zertifizierung zeigen. Wenn ein Benutzer für ein Lernprogramm registriert ist, zeigt das Transkript an, dass der Benutzer

Die Spalten des Teilnehmertranskripts enthalten verschiedene Informationen zu den einzelnen Lernaktivitäten. In den folgenden Tabellen wird die Semantik der einzelnen Spalten beschrieben.

## Teilnehmertranskript

<table> 
 <tbody> 
  <tr> 
   <th width="158" valign="bottom"><p><b>Spaltenname</b></p></th> 
   <th width="160" valign="bottom"><p><b>Werttyp</b></p></th> 
   <th width="306" valign="bottom"><p><b>Beschreibung</b></p></th> 
  </tr> 
  <tr> 
   <td><p><b>Name</b></p></td> 
   <td><p>Nie leer</p></td> 
   <td><p>Name des Teilnehmers</p></td> 
  </tr> 
  <tr> 
   <td><p><b>email</b></p></td> 
   <td><p>Nie leer</p></td> 
   <td><p>E-Mail-Adresse des Teilnehmers</p></td> 
  </tr> 
  <tr> 
   <td valign="bottom"><b>Adobe ID</b></td> 
   <td valign="bottom">Kann leer sein</td> 
   <td valign="bottom">Adobe ID des Teilnehmers</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Eindeutige ID des Benutzers</b></td> 
   <td height="19" width="283">Kann leer sein</td> 
   <td height="19" width="728">Eindeutige Benutzer-ID des Teilnehmers. Diese Spalte basiert auf der Backend-Einstellung, ob auf Kontoebene aktiviert/deaktiviert ist.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Name des Lernplans</b></p></td> 
   <td valign="middle"><p>Kann leer sein</p></td> 
   <td valign="middle">Name des Lernplans (falls vorhanden), über den der Benutzer automatisch zugewiesen wurde.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>LP/Zertifizierung/Kurs</b></p></td> 
   <td valign="middle"><p>Nie leer</p></td> 
   <td valign="middle"><p>Name des Lernprogramms, der Zertifizierung oder des Kurses</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Typ</b></p></td> 
   <td valign="middle">Nie leer</td> 
   <td valign="middle"><p>Der Typ des Lernobjekts, bei dem der Benutzer registriert wurde.</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Kurs</b></p></td> 
   <td valign="middle"><p>Kann leer sein</p></td> 
   <td valign="middle">Name des Kurses, für den der Benutzer registriert ist. Wenn diese Spalte leer ist, stellt die Zeile entweder eine Zertifizierung oder ein Lernprogramm dar. </td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Eindeutige LO-ID</b></td> 
   <td height="19" width="283">Kann leer sein</td> 
   <td height="19" width="728">Eindeutige Lernobjekt-ID des LO. Diese Spalte basiert auf der Einstellung, ob auf Kontoebene aktiviert/deaktiviert ist.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Instanz  </b></p></td> 
   <td valign="middle">Nie leer</td> 
   <td valign="middle">Name der Instanz des LO, bei dem der Benutzer registriert ist. </td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Auswahlkriterien</b></p></td> 
   <td valign="middle"><p>Nie leer</p></td> 
   <td valign="middle"><p>Grundlage für die Registrierung (Angabe, wie dieser Teilnehmer für dieses LO registriert wurde).</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Modul</b></p></td> 
   <td valign="middle"><p>Kann leer sein</p></td> 
   <td valign="middle">Name des Moduls innerhalb der Kurse. Wenn diese Spalte leer ist, stellt diese Zeile entweder einen Kurs, ein Lernprogramm oder eine Zertifizierung dar.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Version</b></td> 
   <td height="19" width="283">Kann leer sein</td> 
   <td height="19" width="728">Version des Moduls</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Lieferart</b></td> 
   <td height="19" width="283">Kann leer sein</td> 
   <td height="19" width="728">Bereitstellungstyp des Moduls - eLearning, F2F, VC, Aktivität.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Sprache</b></td> 
   <td height="19" width="283">Kann leer sein</td> 
   <td height="19" width="728">Sprache, in der das Modul vom Teilnehmer verwendet wird. In dieser Spalte wird der Wert nur für eLearning-Module angezeigt.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Kommentar</b></td> 
   <td height="19" width="283">Kann leer sein</td> 
   <td height="19" width="728">Kommentare, die vom Administrator, dem Kursleiter für den Teilnehmer hinzugefügt wurden, während er die Anwesenheit des Benutzers markiert.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Registrierungsdatum (Asien/Kalkutta-Zeitzone)</b></td> 
   <td height="19" width="283">Nie leer</td> 
   <td height="19" width="728">Datum der Registrierung des Teilnehmers für den LO-Typ.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Startdatum (Zeitzone Asien/Kalkutta)</b></td> 
   <td><p>Kann leer sein</p></td> 
   <td height="19" width="728">Datum, an dem der Teilnehmer das LO gestartet hat. Wenn diese Spalte leer ist, hat der Teilnehmer diesen Vorgang noch nicht gestartet.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Abschlussdatum (Zeitzone Asien/Kalkutta)</b></td> 
   <td><p>Kann leer sein</p></td> 
   <td><p>Datum, an dem der Teilnehmer diesen Vorgang abgeschlossen hat. Wenn diese Spalte leer ist, hat der Teilnehmer diesen Vorgang noch nicht abgeschlossen.</p></td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Frist (Zeitzone Asien/Kalkutta)</b></td> 
   <td><p>Kann leer sein</p></td> 
   <td height="19" width="728">Datum, an dem der Teilnehmer dieses LO abschließen soll. Wenn diese Spalte leer ist, gibt es dafür keine Frist.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>überfällig</b></td> 
   <td height="19" width="283">Ja/Nein</td> 
   <td height="19" width="728">Aktueller Überfälligkeitsstatus des Teilnehmers, der für das LO registriert ist. Ja/Nein</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Status</b></p></td> 
   <td valign="middle">Nicht gestartet/Abgeschlossen/In Bearbeitung/Registrierung aufgehoben</td> 
   <td valign="middle">Aktueller Fortschritt in % des Teilnehmers, der für das LO registriert ist.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Fortschritt %</b></p></td> 
   <td valign="middle">Kann leer sein</td> 
   <td valign="middle"><p>Gibt an, inwieweit der Teilnehmer diesen Vorgang abgeschlossen hat.</p></td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Aufgewandte Zeit (Minuten)</b></td> 
   <td height="38" width="283">Kann leer sein</td> 
   <td height="38" width="728">Die vom Teilnehmer im LO aufgewendete Lernzeit, die Zeilen auf Modulebene zeigen die einzelne modulweise aufgewendete Lernzeit an. Die Zeilen für die Kurs-/Programm-/Zertifikatsebene zeigen die aggregierte aufgewendete Lernzeit an.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Bewertung</b></p></td> 
   <td valign="middle">Bestanden/Nicht bestanden</td> 
   <td valign="middle">Zeigt den Erfolg des Teilnehmers. "Bestanden", wenn der Benutzer die Erfolgskriterien erfüllt hat, ansonsten "Nicht bestanden".</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Punktzahl für Quiz</b></p></td> 
   <td valign="middle">Kann leer sein</td> 
   <td valign="middle">Die neueste Quizpunktzahl des Teilnehmers. Kann leer sein, wenn der Teilnehmer kein Quiz versucht hat oder der Inhalt kein Quiz enthält oder der Administrator/Kursleiter keine Punktzahl zugewiesen hat.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Quiz_score_max</b></td> 
   <td height="38" width="283">Kann leer sein</td> 
   <td height="38" width="728">Die neueste maximal mögliche Quizpunktzahl für das Modul. Kann leer sein, wenn der Teilnehmer nicht versucht hat, das Quiz durchzuführen, oder wenn der Inhalt kein Quiz enthält.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Highest_Quiz_score</b></td> 
   <td height="38" width="283">Kann leer sein</td> 
   <td height="38" width="728">Die höchste Quizpunktzahl, die der Teilnehmer bei mehreren Versuchen erzielt hat. Kann leer sein, wenn der Teilnehmer das Quiz nicht versucht hat oder der Inhalt kein Quiz enthält oder der Administrator/Kursleiter keine Punktzahl zugewiesen hat.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Highest_Quiz_score_max</b></td> 
   <td height="38" width="283">Kann leer sein</td> 
   <td height="38" width="728">Die höchstmögliche Quizpunktzahl für das Modul. Kann leer sein, wenn der Teilnehmer nicht versucht hat, das Quiz durchzuführen, oder wenn der Inhalt kein Quiz enthält.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Angenommene Versuche</b></td> 
   <td height="19" width="283">Kann leer sein</td> 
   <td height="19" width="728">Die Gesamtanzahl der bisherigen Versuche des Teilnehmers für dieses Modul.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Maximal zulässige Versuche</b></td> 
   <td height="19" width="283">Kann leer sein</td> 
   <td height="19" width="728">Die maximale Anzahl der Versuche, die der Teilnehmer hat, um das Modul zu nutzen.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>userState</b></p></td> 
   <td valign="middle">Nie leer</td> 
   <td valign="middle">Benutzerstatus des Teilnehmers: Aktiv/Gelöscht/Ausgesetzt.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Gruppierbares aktives Feld</b></td> 
   <td height="38" width="283">Kann leer sein</td> 
   <td height="38" width="728">Für jedes gruppierbare aktive Feld in Ihrem Konto gibt es eine Spalte, in der der Spaltenname der Name des aktiven Felds ist und der Wert der spezifische Wert ist, den der Teilnehmer für dieses Feld hat.</td> 
  </tr> 
  <tr> 
   <td><p><b>Managername</b></p></td> 
   <td><p><i>Kann leer sein</i></p></td> 
   <td height="19" width="728">Managername des Teilnehmers</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Anzahl der Registrierungen</b></td> 
   <td height="38" width="283">1 oder 0</td> 
   <td height="38" width="728">Anzahl der Registrierungen des Teilnehmers für das LO. Die Zeile mit der höchsten LO-Ebene zeigt einen Wert = '1' an. Die Unterschulungen zeigen den Wert 0 an.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Anzahl der Beginne</b></td> 
   <td height="19" width="283">1 oder 0</td> 
   <td height="19" width="728">Anzahl der Teilnehmer für das LO wurde gestartet. Die Zeile mit der höchsten LO-Ebene zeigt einen Wert = '1' an. Die Unterschulungen zeigen den Wert 0 an.</td> 
  </tr> 
  <tr> 
   <td height="58" width="283"><b>Anzahl der Abschlüsse</b></td> 
   <td height="58" width="283">1 oder 0</td> 
   <td height="58" width="728">Abschlussanzahl des Teilnehmers für das LO. In der Zeile mit dem LO auf höchster Ebene wird ein Wert = '1' angezeigt, wenn der Teilnehmer den Abschluss in dieser Schulung noch nicht abgeschlossen hat. Die Unterschulungen zeigen auch im Status "Ausstehend" den Wert 0 an. In der Zeile mit der höchsten LO-Stufe wird ein Wert = '0' angezeigt, wenn der Teilnehmer die Schulung abgeschlossen hat.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Fällig in N Tagen</b></td> 
   <td height="38" width="283">1 oder 0</td> 
   <td height="38" width="728">Dies zeigt den Wert "1" oder "0" an, je nachdem, für welche Instanz der Termin des Schulungsteilnehmers registriert ist. Es hängt vom Wert ab, der im Feld Lernzusammenfassung im I-Blatt &gt; Fälligkeitsdatum in eingegeben wird.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Fällig in N Tagen für Benutzer</b></td> 
   <td height="38" width="283">1 oder 0</td> 
   <td height="38" width="728">Dies zeigt den Wert "1" oder "0" an, je nachdem, für welche Instanz der Termin des Schulungsteilnehmers registriert ist. Es hängt vom Wert ab, der im Feld Lernzusammenfassung II &gt; "Fälligkeitsdatum in" eingegeben wurde.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Anzahl von (Fortschritt größer als N %)</b></td> 
   <td height="38" width="283">1 oder 0</td> 
   <td height="38" width="728">Dies zeigt den Wert "1" oder "0" an, je nachdem, wie der Teilnehmer die Schulung absolviert hat. Es hängt von dem Wert ab, der im Feld Lernzusammenfassungs-I-Blatt &gt; "Fortschritt größer als" eingegeben wurde.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Anzahl von (Fortschritt größer als N %) für Benutzer</b></td> 
   <td height="38" width="283">1 oder 0</td> 
   <td height="38" width="728">Dies zeigt den Wert "1" oder "0" an, je nachdem, wie der Teilnehmer die Schulung absolviert hat. Es hängt vom Wert ab, der im Feld Lernzusammenfassung II &gt; "Fortschritt größer als" eingegeben wurde.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283">T<b>Ausbildungs-ID</b></td> 
   <td height="19" width="283">Nie leer</td> 
   <td height="19" width="728">Schulungs-ID der Schulung.</td> 
  </tr> 
  <tr> 
   <td height="20" width="283"><b>Dauer der Schulung oder des Moduls (Minuten)</b></td> 
   <td height="20" width="283">Nie leer</td> 
   <td height="20" width="728">Gesamtschulung oder Moduldauer (Min.) der Standardinstanz der Schulung.</td> 
  </tr> 
 </tbody> 
</table>

### Lernzusammenfassung I

<table cellpadding="1" cellspacing="0" border="1"> 
 <tbody> 
  <tr> 
   <th>Spaltenname<br></th> 
   <th>Werttyp</th> 
   <th>Beschreibung</th> 
  </tr> 
  <tr> 
   <td height="19" width="264">Typ</td> 
   <td height="19" width="253">Alle, Lernprogramm, Zertifikat, Kurs.</td> 
   <td height="19" width="412">Der LO-Typ, für den die Lernzusammenfassungstabelle Daten anzeigen soll.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Gruppierbares Feld (Profil)</td> 
   <td height="19" width="253">Nie leer</td> 
   <td height="19" width="412">Das Profil, für das die Lernzusammenfassungstabelle Daten anzeigen soll.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Managername</td> 
   <td height="38" width="253">Nie leer</td> 
   <td height="38" width="412">Der Name des Managers, dessen untergeordnete LO-Engagementdaten in der Übersicht zu Lernprogrammen angezeigt werden sollen.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Zeilenbeschriftungen</td> 
   <td height="19" width="253">Nie leer</td> 
   <td height="19" width="412">Der LO-Name mit der Liste der Teilnehmer, die für das LO registriert sind.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Anzahl der registrierten Teilnehmer</td> 
   <td height="19" width="253">Nie leer</td> 
   <td height="19" width="412">Anzahl der Teilnehmer, die sich für das LO registriert haben.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Anzahl der Teilnehmer, die begonnen haben</td> 
   <td height="19" width="253">Nie leer</td> 
   <td height="19" width="412">Anzahl der Teilnehmer, die das LO gestartet haben.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Anzahl der Teilnehmer, die abgeschlossen haben</td> 
   <td height="19" width="253">Nie leer</td> 
   <td height="19" width="412">Anzahl der Teilnehmer, die das LO abgeschlossen haben.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Anzahl der Teilnehmer, die Fortschritte gemacht haben &gt;= N %</td> 
   <td height="38" width="253">Nie leer</td> 
   <td height="38" width="412">Anzahl der Teilnehmer, die Fortschritte gemacht haben &gt;= N % (Werte).</td> 
  </tr> 
  <tr> 
   <td height="39" width="264">Anzahl der Teilnehmer mit Fälligkeitsdatum in N Tagen</td> 
   <td height="39" width="253">Nie leer</td> 
   <td height="39" width="412">Anzahl der Teilnehmer mit Fälligkeitsdatum in N Tagen (Werte).</td> 
  </tr> 
 </tbody> 
</table>

### Lernzusammenfassung II

| Spaltenname | Werttyp | Beschreibung |
|---|---|---|
| Typ | Alle, Lernprogramm, Zertifikat, Kurs. | Der LO-Typ, für den die Lernzusammenfassungstabelle Daten anzeigen soll. |
| Gruppierbares Feld (Profil) | Nie leer | Das Profil, für das die Lernzusammenfassungstabelle Daten anzeigen soll. |
| Managername | Nie leer | Der Name des Managers, dessen untergeordnete LO-Engagementdaten in der Übersicht zu Lernprogrammen angezeigt werden sollen. |
| Zeilenbeschriftungen | Nie leer | Der Name des Teilnehmers mit der Liste der LOs, bei denen der Teilnehmer registriert ist. |
| Anzahl der registrierten Lernobjekte | Nie leer | Anzahl der Lernobjekte, bei denen der Teilnehmer registriert ist. |
| Anzahl der gestarteten Lernobjekte | Nie leer | Anzahl der Lernobjekte, die der Teilnehmer gestartet hat. |
| Anzahl abgeschlossener Lernobjekte | Nie leer | Anzahl der Lernobjekte, die der Teilnehmer abgeschlossen hat. |
| Anzahl der Lernobjekte, die fortgeschritten sind >= N % | Nie leer | Anzahl der Teilnehmer Objekte, bei denen der Teilnehmer Fortschritte gemacht hat >= N %. |
| Anzahl der Lernobjekte mit Fälligkeitsdatum in N Tagen | Nie leer | Anzahl der Lernobjekte mit Fälligkeitsdatum in N Tagen. |

### Compliance-Zusammenfassung

| Spaltenname | Werttyp | Beschreibung |
|---|---|---|
| Typ | Alle, Lernprogramm, Zertifikat, Kurs. | Der LO-Typ, für den die Lernzusammenfassungstabelle Daten anzeigen soll. |
| Zeilenbeschriftungen (linke Spalte) | Nie leer | Der Name des Teilnehmers mit der Liste der LOs, bei denen der Teilnehmer registriert ist. |
| Zeilenbeschriftungen (linke Spalte) | Nie leer | Der Name des Teilnehmers mit der Liste der LOs, bei denen der Teilnehmer registriert ist. |

### Kompetenzprotokoll

| .Spaltenname | Werttyp | Beschreibung |
|---|---|---|
| Name | Nie leer | Name des Teilnehmers |
| email | Nie leer | E-Mail-Adresse des Teilnehmers |
| Adobe ID | Kann leer sein | Adobe ID des Teilnehmers |
| Eindeutige ID des Benutzers | Kann leer sein | Eindeutige Benutzer-ID des Teilnehmers. Diese Spalte basiert auf der Backend-Einstellung, ob auf Kontoebene aktiviert/deaktiviert ist. |
| Kenntnisse | Nie leer | Dem Teilnehmer wurde ein Kenntnisname zugewiesen. |
| Kenntnisstand | Nie leer | Dem Teilnehmer wurde Kenntnisstufe zugewiesen. |
| Erforderliche Credits | Nie leer | Gesamtanzahl der Credits, die der Teilnehmer benötigt, um die Qualifikation zu erreichen. |
| Verdiente Credits | Nie leer | Gesamtanzahl der vom Teilnehmer für die Kenntnisse verdienten Credits. |
| Abschluss in Prozent | Nie leer | Fortschritt in Prozent, um die Kenntnisse zu erwerben. |
| Zugewiesenes Datum (UTC-Zeitzone) | Nie leer | Datum, an dem die Qualifikation dem Teilnehmer zugewiesen wurde. |
| Erreichtes Datum (UTC-Zeitzone) | Nie leer | Datum, an dem der Teilnehmer die Qualifikation erreicht hat. |
| userState | Nie leer | Benutzerstatus des Teilnehmers: Aktiv/Gelöscht/Ausgesetzt. |
| Gruppierbares aktives Feld | Kann leer sein | Für jedes gruppierbare aktive Feld in Ihrem Konto gibt es eine Spalte, in der der Spaltenname der Name des aktiven Felds ist und der Wert der spezifische Wert ist, den der Teilnehmer für dieses Feld hat. |
| Managername | Kann leer sein | Managername des Teilnehmers. |

### Zusammenfassung der Kenntnisse I

| Spaltenname | Werttyp | Beschreibung |
|---|---|---|
| Nachher | Nie leer | Anzahl der Teilnehmer, die die Kenntnisse erworben haben, vor der eingegebenen Anzahl (Wert) an Tagen, die aktualisiert werden muss. |
| Name | Alle oder beliebige Teilnehmernamen | Der Teilnehmername, dem Kenntnisse zugewiesen sind. |
| Managername | Nie leer | Der Name des Managers, dessen untergeordnete Qualifikationsmanagementdaten in der Zusammenfassungstabelle &quot;Qualifikationen&quot; angezeigt werden sollen. |
| Zeilenbeschriftungen | Nie leer | Der Qualifikationsname mit der Liste der Teilnehmer, die der Qualifikation zugewiesen sind. |
| Anzahl der Benutzer, die diese Kenntnisse haben sollten | Nie leer | Anzahl der Teilnehmer, die Kenntnissen zugewiesen sind. |
| Anzahl der Benutzer, die diese Qualifikation erreicht haben | Nie leer | Anzahl der Teilnehmer, die die Qualifikation erreicht haben. |
| Anzahl der Teilnehmer, deren Kenntnisse aktualisiert werden müssen | Nie leer | Anzahl der Teilnehmer, deren Kenntnisse aktualisiert werden müssen. |
| Prozentsatz der Konformität (basierend auf den erreichten Kenntnissen) | Nie leer | Der Prozentsatz des Fortschritts der zugewiesenen Kenntnisse. |

### Zusammenfassung der Qualifikationen II

| Spaltenname | Werttyp | Beschreibung |
|---|---|---|
| Nachher | Nie leer | Anzahl der Teilnehmer, die die Kenntnisse vor der eingegebenen Anzahl (Wert) an Tagen erreicht haben, die aktualisiert werden muss. |
| Kenntnisse | Alle oder beliebige Kenntnisnamen | Die Namen der Kenntnisse, die Teilnehmern zugewiesen sind. |
| Managername | Nie leer | Der Name des Managers, dessen untergeordnete Qualifikationsmanagementdaten in der Zusammenfassungstabelle &quot;Qualifikationen&quot; angezeigt werden sollen. |
| Zeilenbeschriftungen | Nie leer | Der Name des Teilnehmers mit der zugewiesenen Liste der Kenntnisse. |
| Anzahl der Kenntnisse, die jeder Benutzer haben sollte | Nie leer | Anzahl der Kenntnisse, die dem Teilnehmer zugewiesen wurden. |
| Anzahl der Kenntnisse, die jeder Benutzer hat | Nie leer | Anzahl der vom Teilnehmer erreichten Kenntnisse. |
| Anzahl der Kenntnisse, die aktualisiert werden müssen | Nie leer | Anzahl der Teilnehmer, deren Kenntnisse aktualisiert werden müssen. |
| Prozentsatz der Kompatibilität | Nie leer | Der Prozentsatz des Fortschritts der zugewiesenen Kenntnisse. |

* Manchmal können Administratoren ein Lernobjekt noch lange nach der Schulung manuell als abgeschlossen markieren (insbesondere bei Präsenzkursen). Wenn in einem solchen Szenario &quot;Daten exportieren&quot; für den täglichen LT-Export eingerichtet ist, ist das tatsächliche Abschlussdatum möglicherweise bereits verstrichen, sodass der Export nie solche Abschlussdatensätze erhält, die lange nach der Schulung als abgeschlossen markiert wurden. Wenn dies erkannt wird, sollten Sie das Transkript ab einem bestimmten Startdatum bis zu einem bestimmten Datum (nach Bedarf) in der Benutzeroberfläche exportieren und es dann zur &quot;späten Verarbeitung&quot; an die nachgelagerte Anwendung übermitteln. Dabei müssen Sie möglicherweise Datensätze ignorieren, die bereits verarbeitet wurden.
* &quot;Mehrere Versuche&quot; für ein Modul hängt davon ab, ob dies für dieses LO aktiviert ist. Wenn diese Option aktiviert ist, wird in einer CSV-Zeile für ein Modul ein einziger Versuch angezeigt. Unter Umständen werden nicht alle Versuche an einem Tag gemeldet, sodass die Gesamtzahl der Versuche um mehr als einen Versuch steigt. Außerdem kann ein Versuch nicht unbedingt zu einer besseren Punktzahl führen, und Sie erhalten dann immer nur die beste Punktzahl.

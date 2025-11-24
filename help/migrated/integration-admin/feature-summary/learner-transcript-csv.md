---
jcr-language: en_us
title: Teilnehmertranskript-CSV interpretieren
description: Teilnehmertranskript-CSV interpretieren
contentowner: saghosh
preview: true
source-git-commit: fcc50e80f94bdcbc8de2cddac92f1a12b55e1e18
workflow-type: tm+mt
source-wordcount: '2997'
ht-degree: 88%

---



# Teilnehmertranskript-CSV interpretieren

Das Teilnehmertranskript gehört zu den beliebtesten Berichten in Adobe Learning Manager. Mit diesem Bericht lassen sich nahezu sämtliche Details in einer einzigen CSV-Datei zusammenstellen.

Dieser Bericht hilft zum einen den Benutzern, das Lernverhalten zu verfolgen und zu analysieren, und fungiert zum anderen als Format, in dem Learning Manager die Daten zum Lernverhalten in externe Anwendungen/Systeme exportiert.

In einem typischen Unternehmensszenario wird regelmäßig ein Teilnehmertranskript für Learning Manager exportiert und analysiert. So lässt sich feststellen, welche Teilnehmer ein wichtiges Lernprogramm abschließen, damit Geschenkgutscheine als Anerkennung und Belohnung für zeitnahe Abschlüsse bestellt werden können.

Außerdem ist es möglich, die Lernverhaltensdaten in ein Enterprise Data Warehouse aufzunehmen, in dem die Lerndaten mit anderen Unternehmensdaten kombiniert werden, sodass die Zusammenhänge zwischen Lernverhalten und anderen Prozessdaten in Analysen erkennbar werden.

Im restlichen Dokument wird kurz beschrieben, wie Sie das Teilnehmertranskript aus Learning Manager abrufen können. Anschließend erfahren Sie, wie die einzelnen Zeilen und Spalten des Berichts interpretiert werden.

Diese Informationen sind für alle Entwickler nützlich, die Learning Manager durch die Verarbeitung exportierter Teilnehmertranskriptdaten in andere Systeme integrieren.

## Teilnehmertranskript über die Benutzeroberfläche abrufen {#fetchlearnertranscriptfromtheuserinterface}

Über die Profileinstellungen kann ein Teilnehmer sein Transkript herunterladen. Weitere Informationen finden Sie unter ***[Teilnehmertranskript herunterladen](/help/migrated/administrators/feature-summary/reports/learner-transcripts.md)***.

Administratoren können Teilnehmertranskripte für das gesamte Unternehmen, für eine bestimmte Benutzergruppe oder für einen bestimmten Satz von Lernobjekten generieren (oder auch für einen bestimmten Satz von Benutzern und Lernobjekten gleichzeitig). Außerdem ist es möglich, alle Lerndatensätze für einen bestimmten Zeitraum abzurufen und anzugeben, ob Informationen auf Modulebene erforderlich sind (diese Informationen entfallen standardmäßig). Weitere Informationen finden Sie unter [***Teilnehmertranskripte herunterladen***](/help/migrated/administrators/feature-summary/reports/learner-transcripts.md).

<!--Update above link?-->

Administratoren können das System auch so einrichten, dass das Teilnehmertranskript regelmäßig per E-Mail gesendet wird.

Das über die Benutzeroberfläche generierte Teilnehmertranskript ist eine Excel-Datei, die auch das &quot;Kenntnistranskript&quot; enthält. Dieses Dokument befasst sich auf den Inhalt im CSV-Format, also auf den Bericht mit Lernaktivitäten im Hinblick auf Registrierung, Beginn, Fortschritt oder Abschluss eines Lernobjekts.

## Teilnehmertranskript exportieren {#exportlearnertranscript}

Wenn das Teilnehmertranskript an ein externes System übermittelt werden muss, kann es über die Learning Manager-Funktion „Daten exportieren“ exportiert werden; diese Funktion bietet verschiedene Datentypen an, u. a. eben das Teilnehmertranskript. Wie in der Präambel erläutert, ist dies für die Integration von Learning Manager in ein externes System erforderlich, das Lernverhaltensdaten verarbeiten muss, oder für die Befüllung eines Enterprise Data Warehouse mit Lernverhaltensdaten.

Weitere Informationen zur Unterstützung des Teilnehmertranskript-Exports durch die Connectors finden Sie unter [Daten exportieren](/help/migrated/integration-admin/feature-summary/connectors.md) in den FTP-, Box- und PowerBI-Connectors.

Über diese Anschlüsse werden die Daten regelmäßig (einmal alle n Tage) in eine nachgelagerte Anwendung exportiert. Bei jedem Durchlauf exportieren diese Connectors lediglich die inkrementellen Lernverhaltensdaten. Beachten Sie, dass diese Connectors das Abrufen von Datensätzen nicht zulassen, die sich auf eine bestimmte Untergruppe von Benutzern oder Lernobjekten beziehen - es handelt sich immer um Daten über alle Benutzer und alle Lernobjekte in diesem Konto.

Bei PowerBI sollte der Kunde einen Arbeitsbereich bereitstellen, in dem Learning Manager diese Daten inkrementell in ein dynamisch erstelltes Dataset exportieren kann. Dieser Connector exportiert lediglich die Daten, und die Kunden müssen bei Bedarf eigene Berichte/Dashboards auf der Grundlage dieses Datasets erstellen.

Im nächsten Abschnitt wird erläutert, wie ein nachgelagertes System die Datensätze im Teilnehmertranskript interpretieren soll.

## Teilnehmertranskript interpretieren {#interpretthelearnertranscript}

Jede Zeile in einem Teilnehmertranskript kann als ein Lernverhalten betrachtet werden, das in einem bestimmten Zeitraum im Lernmanager erfasst wurde. In der Regel exportieren die Connectors &quot;inkrementelle Daten&quot;, sodass die Zeilen Lernaktivitäten darstellen, die zwischen der letzten und der aktuellen Ausführung des Connectors stattgefunden haben.

Das Teilnehmertranskript lässt sich über die Connectors natürlich auch je nach Bedarf abrufen. In diesem Fall kann der Benutzer ein Startdatum angeben, und als Enddatum wird der jetzige Zeitpunkt angenommen. In der Regel wird dieser Vorgang nur einmalig durchgeführt, und anschließend wird der Connector für den Export des inkrementellen Teilnehmertranskripts alle n Tage zu einer bestimmten Tageszeit eingerichtet (n ist standardmäßig 1).

Im Folgenden soll definiert werden, was ein inkrementelles Teilnehmertranskript ist.

Jede Zeile im Teilnehmertranskript steht für eine bestimmte Aktivität mit einem bestimmten Teilnehmer und einem bestimmten Lernobjekt. Wir sind hauptsächlich an dem Status eines Teilnehmers in Bezug auf das Lernobjekt interessiert: **Registriert**, **Begonnen**, **In Bearbeitung** und **Abgeschlossen**. Im Teilnehmertranskript sind entsprechend vier Datumsangaben vermerkt.

Es gibt nun drei Arten von Lernobjekten, bei denen der Lern-Manager den Fortschritt der Teilnehmer verfolgt. Die exportierten Daten enthalten Fortschrittsinformationen auf Modulebene, also zur detailliertesten Inhaltseinheit, die ein Teilnehmer im Lern-Manager erleben kann.

* **Kurs** - eine Komposition aus mindestens einem Modul
* **Lernprogramm** - Zusammenstellung mit mindestens einem Kurs
* **Zertifizierung** - Zusammenstellung mit mindestens einem Kurs.

Jede Zeile im Teilnehmertranskript kann die Interaktion eines bestimmten Benutzers mit einem Modul, einem Kurs, einem Lernprogramm oder einer Zertifizierung zeigen. Wenn ein Benutzer für ein Lernprogramm registriert wird, ist diese Registrierung im Transkript ersichtlich.

Die Spalten des Teilnehmertranskripts enthalten verschiedene Informationen zu den verschiedenen Lernaktivitäten (Erläuterung siehe folgende Tabellen).

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
   <td><p><b>E-Mail</b></p></td> 
   <td><p>Nie leer</p></td> 
   <td><p>E-Mail-Adresse des Teilnehmers</p></td> 
  </tr> 
  <tr> 
   <td valign="bottom"><b>Adobe ID</b></td> 
   <td valign="bottom">Kann leer sein</td> 
   <td valign="bottom">Adobe-ID des Teilnehmers</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Eindeutige ID des Benutzers</b></td> 
   <td height="19" width="283">Kann leer sein</td> 
   <td height="19" width="728">Eindeutige Benutzer-ID des Teilnehmers. Bei dieser Spalte hängt es von der Backend-Einstellung ab, ob sie auf Kontoebene aktiviert/deaktiviert ist.</td> 
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
   <td height="19" width="283"><b>LO Eindeutige ID</b></td> 
   <td height="19" width="283">Kann leer sein</td> 
   <td height="19" width="728">Eindeutige ID des LO für das Lernobjekt. Bei dieser Spalte hängt es von der Einstellung ab, ob sie auf Kontoebene aktiviert/deaktiviert ist.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Instanz  </b></p></td> 
   <td valign="middle">Nie leer</td> 
   <td valign="middle">Name der Instanz des LO, bei dem der Benutzer registriert ist. </td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Auswahlkriterien</b></p></td> 
   <td valign="middle"><p>Nie leer</p></td> 
   <td valign="middle"><p>Grundlage für die Registrierung (Angabe, wie dieser Teilnehmer bei diesem LO registriert wurde).</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Modul</b></p></td> 
   <td valign="middle"><p>Kann leer sein</p></td> 
   <td valign="middle">Name des Moduls innerhalb der Kurse. Wenn diese Zeile leer ist, stellt die Zeile entweder einen Kurs, ein Lernprogramm oder eine Zertifizierung dar.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Version</b></td> 
   <td height="19" width="283">Kann leer sein</td> 
   <td height="19" width="728">Version des Moduls</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Bereitstellungstyp</b></td> 
   <td height="19" width="283">Kann leer sein</td> 
   <td height="19" width="728">Liefertyp des Moduls – eLearning, F2F, VC, Aktivität.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Sprache</b></td> 
   <td height="19" width="283">Kann leer sein</td> 
   <td height="19" width="728">Sprache, in der das Modul von Teilnehmern genutzt wird. In dieser Spalte wird nur Wert für eLearning-Module angezeigt.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Kommentar</b></td> 
   <td height="19" width="283">Kann leer sein</td> 
   <td height="19" width="728">Kommentare, die vom Administrator, Kursleiter für den Teilnehmer hinzugefügt wurden, während die Benutzerteilnahme markiert wurde.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Registrierungsdatum (Asien/Calcutta Zeitzone)</b></td> 
   <td height="19" width="283">Nie leer</td> 
   <td height="19" width="728">Datum der Registrierung durch den Teilnehmer für den LO-Typ.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Startdatum (Asien/Calcutta Zeitzone)</b></td> 
   <td><p>Kann leer sein</p></td> 
   <td height="19" width="728">Datum, an dem der Teilnehmer das LO gestartet hat. Wenn diese Spalte leer ist, hat der Teilnehmer diesen Vorgang noch nicht gestartet.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Abschlussdatum (Asien/Calcutta Zeitzone)</b></td> 
   <td><p>Kann leer sein</p></td> 
   <td><p>Datum, an dem der Teilnehmer diesen Vorgang abgeschlossen hat. Wenn diese Spalte leer ist, hat der Teilnehmer diesen Vorgang noch nicht abgeschlossen.</p></td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Termin (Asien/Calcutta Zeitzone)</b></td> 
   <td><p>Kann leer sein</p></td> 
   <td height="19" width="728">Datum, bis zu dem der Teilnehmer dieses LO abschließen soll. Wenn diese Spalte leer ist, wurde keine Frist festgelegt.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Überfällig</b></td> 
   <td height="19" width="283">Ja//Nein</td> 
   <td height="19" width="728">Aktueller Überfällig-Status des Teilnehmers, der sich für das LO registriert hat. Ja//Nein</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Status</b></p></td> 
   <td valign="middle">Nicht gestartet/Abgeschlossen/Wird ausgeführt/Nicht registriert</td> 
   <td valign="middle">Aktueller Fortschritt (in %) des Teilnehmers, der sich für das LO registriert hat.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Fortschritt %</b></p></td> 
   <td valign="middle">Kann leer sein</td> 
   <td valign="middle"><p>Angabe, inwieweit der Teilnehmer diesen Vorgang bereits abgeschlossen hat.</p></td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Verbrachte Zeit (Minuten)</b></td> 
   <td height="38" width="283">Kann leer sein</td> 
   <td height="38" width="728">Die Lernzeit, die der Teilnehmer im LO verbracht hat, wird in den Zeilen auf Modulebene für die einzelnen Module für die Lernzeit angegeben. Die Zeilen für die Kurs-/Programm-/Zertifikatsebene zeigen die aggregierte verbrachte Lernzeit an.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Bewertung</b></p></td> 
   <td valign="middle">Bestanden/Nicht bestanden</td> 
   <td valign="middle">Zeigt den Erfolg des Teilnehmers. „Bestanden“, wenn der Benutzer die Erfolgskriterien erfüllt hat, ansonsten „Nicht bestanden“.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Punktzahl für Quiz</b></p></td> 
   <td valign="middle">Kann leer sein</td> 
   <td valign="middle">Die aktuellste Quizpunktzahl, die der Teilnehmer erhalten hat. Kann leer sein, wenn der Teilnehmer das Quiz nicht versucht hat oder der Inhalt kein Quiz enthält oder dem Administrator/Kursleiter keine Punktzahl zugewiesen wurde.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Quiz_score_max</b></td> 
   <td height="38" width="283">Kann leer sein</td> 
   <td height="38" width="728">Die aktuellste maximale Quizpunktzahl für das Modul. Kann leer sein, wenn der Teilnehmer das Quiz nicht versucht hat oder der Inhalt kein Quiz enthält.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Highest_Quiz_score</b></td> 
   <td height="38" width="283">Kann leer sein</td> 
   <td height="38" width="728">Die höchste Quizpunktzahl, die der Teilnehmer bei mehreren Versuchen erzielt hat. Kann leer sein, wenn der Teilnehmer das Quiz nicht versucht hat oder der Inhalt kein Quiz enthält oder dem Administrator/Kursleiter keine Punktzahl zugewiesen wurde.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Highest_Quiz_score_max</b></td> 
   <td height="38" width="283">Kann leer sein</td> 
   <td height="38" width="728">Die höchstmögliche Quizpunktzahl für das Modul. Kann leer sein, wenn der Teilnehmer das Quiz nicht versucht hat oder der Inhalt kein Quiz enthält.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Unternommene Versuche</b></td> 
   <td height="19" width="283">Kann leer sein</td> 
   <td height="19" width="728">Die Gesamtanzahl der bisherigen Versuche des Teilnehmers für dieses Modul.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Maximal zulässige Versuche</b></td> 
   <td height="19" width="283">Kann leer sein</td> 
   <td height="19" width="728">Die maximale Anzahl zulässiger Versuche für den Teilnehmer, das Modul zu nutzen.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Benutzerstatus</b></p></td> 
   <td valign="middle">Nie leer</td> 
   <td valign="middle">Benutzerstatus des Teilnehmers: Aktiv/Gelöscht/Ausgesetzt</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Gruppierbares aktives Feld</b></td> 
   <td height="38" width="283">Kann leer sein</td> 
   <td height="38" width="728">Für jedes gruppierbare aktive Feld in Ihrem Konto gibt es eine Spalte. Der Spaltenname ist dabei der Name des aktiven Felds und als Wert ist der jeweilige Wert des Teilnehmers für dieses Feld angegeben.</td> 
  </tr> 
  <tr> 
   <td><p><b>Managername</b></p></td> 
   <td><p><i>Kann leer sein</i></p></td> 
   <td height="19" width="728">Name des Managers des Teilnehmers</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Anzahl der Registrierungen</b></td> 
   <td height="38" width="283">1 oder 0</td> 
   <td height="38" width="728">Registrierungsanzahl des Teilnehmers für das LO. Die LO-Zeile der höchsten Ebene zeigt einen Wert = ‚1‘ an. Die Unterschulungen zeigen den Wert 0 an.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Anzahl Begonnen</b></td> 
   <td height="19" width="283">1 oder 0</td> 
   <td height="19" width="728">Anzahl Begonnen des Teilnehmers für das LO. Die LO-Zeile der höchsten Ebene zeigt einen Wert = ‚1‘ an. Die Unterschulungen zeigen den Wert 0 an.</td> 
  </tr> 
  <tr> 
   <td height="58" width="283"><b>Anzahl der Abschlüsse</b></td> 
   <td height="58" width="283">1 oder 0</td> 
   <td height="58" width="728">Anzahl der Abschlüsse des Teilnehmers für das LO. Die LO-Zeile der höchsten Ebene zeigt den Wert = ‚1‘ an, wenn der Abschluss der Schulung durch den Teilnehmer aussteht. Die Unterschulungen zeigen den Wert 0 an, selbst wenn sie im Status „Ausstehend“ sind. Die LO-Zeile der höchsten Ebene zeigt einen Wert = ‚0‘ an, wenn der Teilnehmer die Schulung abgeschlossen hat.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Fällig in N Tagen</b></td> 
   <td height="38" width="283">1 oder 0</td> 
   <td height="38" width="728">Es wird ein Wert von ‚1‘ oder ‚0‘ angezeigt, je nachdem, für welche Instanz der Schulungsteilnehmer registriert ist. Das hängt von dem Wert ab, der in das Feld „Übersicht zu Lernprogrammen I &gt; ‚Bevorstehender Termin in‘“ eingegeben wurde.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Fällig in N Tagen für Benutzer</b></td> 
   <td height="38" width="283">1 oder 0</td> 
   <td height="38" width="728">Es wird ein Wert von ‚1‘ oder ‚0‘ angezeigt, je nachdem, für welche Instanz der Schulungsteilnehmer registriert ist. Das hängt von dem Wert ab, der in das Feld „Übersicht zu Lernprogrammen II &gt; Bevorstehender Termin in‘“ eingegeben wurde.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Anzahl von (Fortschritt größer als N %)</b></td> 
   <td height="38" width="283">1 oder 0</td> 
   <td height="38" width="728">Je nach Lernfortschritt in der Schulung wird der Wert ‚1‘ oder ‚0‘ angezeigt. Das hängt von dem Wert ab, der im Feld „Übersicht zu Lernprogrammen I &gt; ‚Fortschritt größer als‘“ eingegeben wurde.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Anzahl von (Fortschritt größer als N %) für Benutzer</b></td> 
   <td height="38" width="283">1 oder 0</td> 
   <td height="38" width="728">Je nach Lernfortschritt in der Schulung wird der Wert ‚1‘ oder ‚0‘ angezeigt. Das hängt von dem Wert ab, der in das Feld „Übersicht zu Lernprogrammen II &gt; ‚Fortschritt größer als‘“ eingegeben wurde.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283">S<b>chulungs-ID</b></td> 
   <td height="19" width="283">Nie leer</td> 
   <td height="19" width="728">Schulungs-ID der Schulung.</td> 
  </tr> 
  <tr> 
   <td height="20" width="283"><b>Dauer der Schulung oder des Moduls (Min.)</b></td> 
   <td height="20" width="283">Nie leer</td> 
   <td height="20" width="728">Gesamtdauer der Schulung oder des Moduls (Min.) der Standardinstanz der Schulung.</td> 
  </tr> 
 </tbody> 
</table>

### Übersicht zu Lernprogrammen I

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
   <td height="19" width="412">Der LO-Typ, für den die Zusammenfassungstabelle „Lernprogramme“ Daten anzeigen soll.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Gruppierbares Feld (Profil)</td> 
   <td height="19" width="253">Nie leer</td> 
   <td height="19" width="412">Das Profil, für das die Zusammenfassungstabelle „Lernprogramme“ Daten anzeigen soll.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Managername</td> 
   <td height="38" width="253">Nie leer</td> 
   <td height="38" width="412">Der Name des Managers, zu dessen Mitarbeitern LO-Engagementdaten in der Zusammenfassungstabelle „Lernprogramme“ angezeigt werden sollen.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Zeilenbeschriftungen</td> 
   <td height="19" width="253">Nie leer</td> 
   <td height="19" width="412">Der LO-Name mit der Liste der Teilnehmer, die für das LO registriert sind.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Anzahl der Teilnehmer, die registriert sind</td> 
   <td height="19" width="253">Nie leer</td> 
   <td height="19" width="412">Anzahl der Teilnehmer, die für das LO registriert sind.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Anzahl der Teilnehmer, die begonnen haben</td> 
   <td height="19" width="253">Nie leer</td> 
   <td height="19" width="412">Anzahl der Teilnehmer, die das LO begonnen haben</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Anzahl Teilnehmer, die abgeschlossen haben</td> 
   <td height="19" width="253">Nie leer</td> 
   <td height="19" width="412">Anzahl der Teilnehmer, die das LO abgeschlossen haben.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Anzahl der Teilnehmer, die Fortschritte &gt;= N % gemacht haben</td> 
   <td height="38" width="253">Nie leer</td> 
   <td height="38" width="412">Anzahl der Teilnehmer, die Fortschritte &gt;= N % (Werte) gemacht haben.</td> 
  </tr> 
  <tr> 
   <td height="39" width="264">Anzahl der Teilnehmer mit Termin in N Tagen</td> 
   <td height="39" width="253">Nie leer</td> 
   <td height="39" width="412">Anzahl der Teilnehmer mit Termin in N Tagen (Werte).</td> 
  </tr> 
 </tbody> 
</table>

### Übersicht zu Lernprogrammen II

| Spaltenname | Werttyp | Beschreibung |
|---|---|---|
| Typ | Alle, Lernprogramm, Zertifikat, Kurs. | Der LO-Typ, für den die Zusammenfassungstabelle „Lernprogramme“ Daten anzeigen soll. |
| Gruppierbares Feld (Profil) | Nie leer | Das Profil, für das die Zusammenfassungstabelle „Lernprogramme“ Daten anzeigen soll. |
| Managername | Nie leer | Der Name des Managers, zu dessen Mitarbeitern LO-Engagementdaten in der Zusammenfassungstabelle „Lernprogramme“ angezeigt werden sollen. |
| Zeilenbeschriftungen | Nie leer | Der Name des Teilnehmers mit der zugewiesenen Liste der LOs. |
| Anzahl der Lernobjekte, die registriert sind | Nie leer | Anzahl der Lernobjekte, für die der Teilnehmer registriert ist. |
| Anzahl der Lernobjekte | Nie leer | Anzahl der Lernobjekte, die der Teilnehmer gestartet hat. |
| Anzahl der abgeschlossenen Lernobjekte | Nie leer | Anzahl der Lernobjekte, die der Teilnehmer abgeschlossen hat. |
| Anzahl der Lernobjekte mit einem Fortschritt >= N % | Nie leer | Anzahl der Lernobjekte, bei denen der Teilnehmer Fortschritte >= N % gemacht hat. |
| Anzahl der Lernobjekte mit Termin in N Tagen | Nie leer | Anzahl der Lernobjekte mit Termin in N Tagen. |

### Compliance-Übersicht

| Spaltenname | Werttyp | Beschreibung |
|---|---|---|
| Typ | Alle, Lernprogramm, Zertifikat, Kurs. | Der LO-Typ, für den die Zusammenfassungstabelle „Lernprogramme“ Daten anzeigen soll. |
| Zeilenbeschriftungen (linke Spalte) | Nie leer | Der Name des Teilnehmers mit der zugewiesenen Liste der LOs. |
| Zeilenbeschriftungen (linke Spalte) | Nie leer | Der Name des Teilnehmers mit der zugewiesenen Liste der LOs. |

### Kenntnis-Transkript

| .Spaltenname | Werttyp | Beschreibung |
|---|---|---|
| Name | Nie leer | Name des Teilnehmers |
| E-Mail | Nie leer | E-Mail-Adresse des Teilnehmers |
| Adobe ID | Kann leer sein | Adobe-ID des Teilnehmers |
| Eindeutige ID des Benutzers | Kann leer sein | Eindeutige Benutzer-ID des Teilnehmers. Bei dieser Spalte hängt es von der Backend-Einstellung ab, ob sie auf Kontoebene aktiviert/deaktiviert ist. |
| Kenntnisse | Nie leer | Name der Kenntnisse, die dem Teilnehmer zugewiesen wurden. |
| Kenntnisstufen | Nie leer | Dem Teilnehmer zugewiesene Kenntnisstufen. |
| Erforderliche Punktzahl | Nie leer | Gesamtsumme der vom Teilnehmer benötigten Punkte, um die Kenntnisse zu erwerben. |
| Erhaltene Punkte | Nie leer | Gesamtsumme der Punkte, die der Teilnehmer für die Qualifikation erhalten hat. |
| Abgeschlossen % | Nie leer | Fortschritt (in Prozent) zum Erreichen der Kenntnisse. |
| Zugewiesen am (UTC-Zeitzone) | Nie leer | Datum, an dem die Kenntnisse dem Teilnehmer zugewiesen wurden. |
| Erreicht am (UTC-Zeitzone) | Nie leer | Datum, an dem der Teilnehmer die Kenntnisse erlangt hat. |
| Benutzerstatus | Nie leer | Benutzerstatus des Teilnehmers: Aktiv/Gelöscht/Ausgesetzt |
| Gruppierbares aktives Feld | Kann leer sein | Für jedes gruppierbare aktive Feld in Ihrem Konto gibt es eine Spalte. Der Spaltenname ist dabei der Name des aktiven Felds und als Wert ist der jeweilige Wert des Teilnehmers für dieses Feld angegeben. |
| Managername | Kann leer sein | Name des Managers des Teilnehmers. |

### Übersicht über Kenntnisse I

| Spaltenname | Werttyp | Beschreibung |
|---|---|---|
| Nachher | Nie leer | Anzahl der Teilnehmer, die die Kenntnisse vor der eingegebenen Anzahl (Wert) an Tagen erreicht haben, die aktualisiert werden muss. |
| Name | Alle oder beliebiger Teilnehmername | Der Name des Teilnehmers, dem Kenntnisse zugewiesen sind. |
| Managername | Nie leer | Der Name des Managers, zu dessen Mitarbeitern Kenntnis-Engagementdaten in der Zusammenfassungstabelle „Kenntnisse“ angezeigt werden sollen. |
| Zeilenbeschriftungen | Nie leer | Der Kenntnisname mit der Liste der Teilnehmer, die den Kenntnissen zugewiesen sind. |
| Anzahl der Benutzer, die diese Kenntnisse haben sollten | Nie leer | Anzahl der Teilnehmer, die den Kenntnissen zugewiesen sind. |
| Anzahl der Benutzer, die diese Kenntnisse erworben haben | Nie leer | Anzahl der Teilnehmer, die die Kenntnisse erreicht haben. |
| Anzahl der Teilnehmer, deren Kenntnisse aufgefrischt werden müssen | Nie leer | Anzahl der Teilnehmer, deren Kenntnisse aktualisiert werden müssen. |
| Prozent der Compliance (Basierend auf erreichten Kenntnissen) | Nie leer | Der Prozentsatz des Fortschritts bezüglich der zugewiesenen Kenntnisse. |

### Übersicht über Kenntnisse II

| Spaltenname | Werttyp | Beschreibung |
|---|---|---|
| Nachher | Nie leer | Anzahl der Teilnehmer, die die Kenntnisse vor der eingegebenen Anzahl (Wert) an Tagen erreicht haben, die aktualisiert werden muss. |
| Kenntnisse | Alle oder beliebiger Kenntnisname | Die Namen der Kenntnisse, die Teilnehmern zugewiesen sind. |
| Managername | Nie leer | Der Name des Managers, zu dessen Mitarbeitern Kenntnis-Engagementdaten in der Zusammenfassungstabelle „Kenntnisse“ angezeigt werden sollen. |
| Zeilenbeschriftungen | Nie leer | Der Name des Teilnehmers mit der zugewiesenen Liste der Kenntnisse. |
| Anzahl der Kenntnisse, die jeder Benutzer haben sollte | Nie leer | Anzahl der Kenntnisse, die dem Teilnehmer zugewiesen wurden. |
| Anzahl der Kenntnisse, die jeder Benutzer hat | Nie leer | Anzahl der Kenntnisse, die vom Teilnehmer erreicht wurden. |
| Anzahl der Kenntnisse, die aktualisiert werden müssen | Nie leer | Anzahl der Teilnehmer, deren Kenntnisse aktualisiert werden müssen. |
| Prozentsatz der Kompatibilität | Nie leer | Der Prozentsatz des Fortschritts bezüglich der zugewiesenen Kenntnisse. |

* Manchmal können Administratoren ein Lernobjekt noch lange nach der Schulung manuell als abgeschlossen markieren (insbesondere bei Präsenzkursen). Wenn in einem solchen Szenario die Funktion „Daten exportieren“ für den täglichen LT-Export eingerichtet ist, liegt das tatsächliche Abschlussdatum möglicherweise in der Vergangenheit. Diese Abschlussdatensätze, die lange nach der Schulung als abgeschlossen markiert wurden, gehen daher nie in den Export ein. Wenn dies erkannt wird, sollten Sie das Transkript ab einem bestimmten Startdatum bis zu einem bestimmten Datum (nach Bedarf) in der Benutzeroberfläche exportieren und es dann zur &quot;späten Verarbeitung&quot; an die nachgelagerte Anwendung übermitteln. Dabei müssen Sie möglicherweise Datensätze ignorieren, die bereits verarbeitet wurden.
* Die Angabe für „Mehrere Versuche“ für ein Modul ist davon abhängig, ob diese Option für das betreffende LO aktiviert ist. Wenn diese Option aktiviert ist, wird in einer CSV-Zeile für ein Modul jeweils ein bestimmter Versuch angezeigt. Unter Umständen werden nicht alle Versuche an einem Tag gemeldet, sodass die Gesamtzahl der Versuche um mehr als einen Versuch steigt. Außerdem kann ein Versuch nicht unbedingt zu einer besseren Punktzahl führen, und es wird jeweils nur die beste Punktzahl angezeigt.

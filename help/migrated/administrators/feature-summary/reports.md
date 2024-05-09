---
description: Informieren Sie sich über die Berichte, die mit der Administratorrolle in der Learning Manager-Anwendung verknüpft sind.
jcr-language: en_us
title: Berichte
contentowner: manochan
exl-id: 31b176b7-4b8f-4851-a0c5-4eee58bceb41
source-git-commit: 037619bb6157f6b4fc3a739571f4766b2d634900
workflow-type: tm+mt
source-wordcount: '6931'
ht-degree: 60%

---

# Berichte

Informieren Sie sich über die Berichte, die mit der Administratorrolle in der Learning Manager-Anwendung verknüpft sind.

Mit Adobe Learning Manager können Sie verschiedene Berichte erstellen, um die Aktivitäten der Teilnehmer zu verfolgen, zu überwachen und zu kontrollieren. Aktivitäten von Teilnehmern werden verfolgt und automatisch in der Datenbank erfasst. Manager- und Administratoren-Berichte werden von der Datenbank aus erstellt.

## Übersicht {#overview}

Berichte für Administratoren und Manager werden auf ähnliche Weise erstellt. Manager können Berichte über ihre Mitarbeiter anzeigen, Administratoren hingegen alle Berichte im Unternehmen.

Berichte werden in einem Dashboard generiert. Ein Bericht muss sich in einem Dashboard befinden. A **[!UICONTROL Standard-Dashboard]** ist standardmäßig auf der Berichtsseite vorhanden. Alle Berichte, die Sie hinzufügen, werden in dieses Standard-Dashboard verschoben. Um einem einzelnen Dashboard einen Bericht hinzuzufügen, wählen Sie in der Dropdownliste **[!UICONTROL Bericht hinzufügen]**. Genauere Informationen über das Erstellen von Dashboards finden Sie im Bereich „Dashboards“ auf dieser Seite.

## Berichtstypen {#typesofreports}

Adobe Learning Manager unterstützt vier wichtige Berichtstypen wie z. B. Abschluss, aufgewandte Zeit, Kenntnisse und Effektivität. Mit den folgenden Berichtstypen können Sie mehr als 300 unterschiedliche Berichtsvarianten generieren:

* Statistiken zur Kursbereitstellung für Teilnehmer
* Bericht zur Effektivität von Kursen
* Kenntnisbasierter Bericht über Teilnehmer
* Statistik zur Registrierung der Teil für Lernprogramme
* Von den Teilnehmern aufgewandte Lernzeit
* Anzahl der Teilnehmer
* Abschluss der Zertifizierung

## Dashboards für Benutzeraktivität {#useractivitydashboards}

Zeigen Sie eine Zusammenfassung aller Benutzeraktivitäten auf der Plattform im Zeitverlauf an. Konfigurieren Sie Benutzergruppen und wenden Sie Filter an.

Das Dashboard für Benutzeraktivität zeigt die Aktivität der Benutzer im Konto an. Die drei aufgeführten Berichte sind:

* **Registrierte Benutzer:** Dieser Bericht enthält Informationen zur Anzahl der Benutzer, die Woche für Woche bei Ihrem Konto registriert sind. Bei Konten mit der Lizenzierung „Monatlich aktive Einheiten in diesem Monat“ zeigt der Bericht stattdessen die MAU-Einheiten an.

* **Benutzerbesuchsbericht:** Dieser Bericht enthält Informationen über die Anzahl der Benutzer, die täglich auf die Plattform zugreifen. Der Monatsbericht ist ebenfalls verfügbar.

* **Bericht über Zeitaufwand:** Dieser Bericht enthält Informationen zur täglich auf der Plattform verbrachten Lernzeit. Der Monatsbericht ist ebenfalls verfügbar.

### Registrierte Benutzer {#registeredusers}

Learning Manager zeichnet jede Woche die Anzahl der im System registrierten Benutzer auf. Administratoren können diesen Bericht anzeigen, um die registrierte Anzahl der Benutzer an diesem Wochentag zu erfahren. Die einmal für eine Woche gespeicherte registrierte Anzahl ändert sich nicht. Daher steht die registrierte historische Anzahl nicht in Beziehung zur aktuellen Gruppe von Teilnehmern im System.

Dieser Bericht enthält Informationen zur Anzahl der Benutzer, die Woche für Woche bei Ihrem Konto registriert sind.

Bei Konten mit der Lizenzierung „Monatlich aktive Einheiten in diesem Monat“ zeigt der Bericht stattdessen die MAU-Einheiten an.

![](assets/registered-usersreport.png)
*Bericht über registrierte Benutzer*

***Für Konten mit Einheit für monatlichen Zugriff:***

**Bericht über monatlich aktive Benutzer**

Dieser Bericht zeigt die Anzahl der Teilnehmer an, die jeden Monat auf der Lernplattform aktiv sind. Der Benutzer gilt für den Monat als aktiv, wenn er eine der hier genannten Lernaktionen ausführt. Dies ist die gleiche Weise, wie „Monatlich aktive Einheiten in diesem Monat“ gezählt werden.

Die einmal für einen Monat gespeicherte aktive Anzahl ändert sich nicht. Daher steht die angezeigte historische Anzahl nicht in Beziehung zur aktuellen Gruppe von Teilnehmern im System.

### Benutzerbesuche {#uservisits}

Dieser Bericht zeigt die Gesamtzahl der Teilnehmer, die in einem Tag oder Monat auf das System zugreifen. Das Durchsuchen der Lernplattform ohne Nutzung des Lernangebots wird auch als „Zugriff“ auf die Lernplattform betrachtet. Dies hilft dem Administrator, die Gesamtzahl der Benutzer zu ermitteln, die auf das System zugreifen. Am ersten Tag des Monats erstellt Learning Manager einen Datensatz mit allen Benutzern, die im Vormonat auf die Plattform zugegriffen haben. Außerdem werden die Benutzergruppeninformationen für diese Benutzer erfasst.

Nur die vom Administrator konfigurierten Benutzergruppen werden aufgezeichnet. Dadurch können Administratoren auch Filter auf Benutzergruppen für historische Monatsdaten anwenden. Beachten Sie: Falls die Benutzergruppenkonfiguration geändert wurde und Learning Manager in früheren Monaten keine Daten für diese Benutzergruppe aufgezeichnet hat, kann Learning Manager die Daten für diese neu konfigurierten Benutzergruppen nicht für vorherige Monate anzeigen.

Dieser Bericht enthält Benutzer, die mit allen Formaten wie Web, mobiler App, fragwürdigen benutzerdefinierten Lösungen usw. auf die Plattform zugreifen. Im Diagramm zur Verwendung der Geräte-App werden speziell nur die Benutzer berücksichtigt, die mit der Geräte-App von Learning Manager auf die Plattform zugreifen. Dadurch können Administratoren die Verwendung der mobilen App in ihrem Konto erkennen.

![](assets/user-visit-report.png)
*Bericht über Benutzerbesuche*

### Bericht über Zeitaufwand zum Lernen {#learningtimespentreport}

Hier sehen Sie zweiachsige Liniendiagramme, die den gesamten Zeitaufwand zum Lernen für alle Teilnehmer über einen Zeitraum von 12 Monaten anzeigen. Die zweite Achse stellt den mittleren Zeitaufwand zum Lernen einer einzelne Person dar.

Der Zeitaufwand für verschiedene Lernobjekte wie Lernprogramme und Zertifizierungen wird für Folgendes berechnet:

* Selbststudium mit statischen und interaktiven Inhalten
* Aktivitätskurse mit URL.
* Wochenendsitzungen mit aktiviertem Wochenendflag
* VC-Connect-Sitzung, bei der die Anwesenheit automatisch markiert wird
* Die für verschiedene Lernobjekte wie Lernprogramme und Zertifizierungen aufgewendete Zeit
* xAPI-Anweisungen für einen xAPI-Aktivitätskurs.

Sie können das Diagramm weiter als Excel-Tabelle exportieren.

Ein Filter zur Auswahl der Benutzergruppenkonfiguration erleichtert die Anzeige der Daten hinsichtlich verschiedener Benutzergruppen.

Der ausgewählte Datums- und Benutzergruppenfilter wird auf alle relevanten Diagramme im Dashboard angewendet.

>[!NOTE]
>
>Für die Berichte **[!UICONTROL Benutzerbesuche]** und **[!UICONTROL Zeitaufwand zum Lernen]** werden die Standarddaten (wenn keine Benutzergruppe konfiguriert ist) für das gesamte Konto angezeigt.

## Dashboard für Schulungsinhalt {#trainingcontentdashboard}

Das Dashboard für Schulungsinhalt bietet Einblicke in Schulungen, die auf der Plattform verfügbar sind. Sie können beliebte Schulungen anzeigen oder alle verfügbaren Schulungen verfolgen.

### Schulungsbericht {#trainingsreport}

Dieser Bericht enthält Informationen über alle Schulungen, die Monat für Monat (im Veröffentlichungszustand) auf der Plattform verfügbar sind. Er informiert über die Anzahl der im Laufe der Zeit angebotenen Schulungen.

![](assets/training-report.png)
*Schulungsbericht*

### Bericht über aktive Schulungen {#activetrainingsreport}

Dieser Bericht enthält Informationen zu den Schulungen, die über den ausgewählten Zeitraum aktiv sind. Aktive Schulungen sind Schulungen, die im jeweiligen Zeitraum registriert sind, im Player angezeigt oder abgeschlossen werden.

Für aktive Schulungen stehen Daten aller internen Gruppen von Stammbenutzern (mit Managerrolle) zur Auswahl, wenn keine Benutzergruppenkonfiguration vorgenommen wurde. Neben den Stammbenutzergruppen können Sie bei Bedarf 10 weitere Benutzergruppen konfigurieren.

![](assets/active-trainingsreport.png)
*Bericht über aktive Schulungen*

>[!NOTE]
>
>Die Daten werden nicht wie erwartet angezeigt, wenn **[!UICONTROL Alle Benutzer]** und **[!UICONTROL 12 Monate]** Filter ausgewählt sind, die Daten jedoch angezeigt werden, wenn Sie **[!UICONTROL Alle internen Benutzergruppen].**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Referenz</b></p></td>
   <td>
    <p><b>Metrisch</b></p></td>
   <td>
    <p><b>Beschreibung</b></p></td>
  </tr>
  <tr>
   <td>
    <p>1</p></td>
   <td>
    <p>Startverhältnis (%)</p></td>
   <td>
    <p>Verhältnis zwischen der Anzahl der Teilnehmer, die den Kurs gestartet haben, und der Anzahl der Registrierungen.</p></td>
  </tr>
  <tr>
   <td>
    <p>2</p></td>
   <td>
    <p>Abschlussverhältnis (%)</p></td>
   <td>
    <p>Verhältnis zwischen allen Benutzern, die den Kurs abgeschlossen haben, und allen Benutzern, die den Kurs gestartet haben.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>3</p></td>
   <td>
    <p>Teilnehmerfeedback</p></td>
   <td>
    <p>Durchschnitt aller eingegangenen L1-Feedback-Antworten auf einer Skala von 1 bis 10, gerundet auf die nächste ganze Zahl.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>Manager-Feedback</p></td>
   <td>
    <p>Durchschnitt aller eingegangenen L3-Feedback-Antworten auf einer Skala von 1 bis 5, gerundet auf die nächste ganze Zahl<br></p></td>
  </tr>
 </tbody>
</table>

Der Schulungsbericht enthält zwei zusätzliche Spalten:

1. Durchschnittliche Sternebewertung eines Kurses.
1. Anzahl der Teilnehmer, die den Kurs bewertet haben.
1. Eingebetteter Pfad
1. ID für eingebetteten Pfad
1. ID für eingebetteten Kurs

>[!NOTE]
>
>Startverhältnis, Abschlussverhältnis, Teilnehmerfeedback und Manager-Feedback werden von den angewendeten Filtern nicht beeinflusst. Die Filter wirken sich nur auf Registrierung, Ansichten und Abschlüsse aus.

>[!NOTE]
>
>Für beide Berichte (Schulungsinhalt, Benutzeraktivität) können Sie maximal 10 Benutzergruppen konfigurieren. Es kann bis zu 24 Stunden dauern, bis die Verarbeitung abgeschlossen ist und die neu konfigurierten Filter verfügbar sind.

## Dashboards für Lernzusammenfassungen {#dashboards}

### Dashboard-Berichte erstellen

>[!INFO]
>
>In dieser Schulung erfahren Sie, wie Sie Dashboard-Berichte aus der Datenbank generieren.<br><br>[![Knopf](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=R3B5NPDN&amp;mv=display&amp;mv2=display#/course/8318854)</br></br>


Wenn Sie die Schulung nicht starten können, schreiben Sie an <almacademy@adobe.com>.

Sehen Sie sich einen zusammenfassenden Bericht über alle Lernaktivitäten in der Plattform an. Auf dieser Seite können Sie die folgenden Zusammenfassungsinformationen für das Team des ausgewählten Stammbenutzers und die externen Profile sehen. Der Zeitbereich kann auch ausgewählt werden:

* Lernzusammenfassung in Form von Registrierungen, Ansichten und Abschlüssen
* Top-Qualifikationen
* Compliance-Zusammenfassung

![](assets/summary-charts.png)
*Zusammenfassungsdiagramme*

Wenn es interne Stammebenen-Manager gibt, werden diese nacheinander angezeigt.

Alle externen Profile werden nach internen Profilen aufgelistet (interne Stammbenutzer).

Wenn ein externes Profil über einen Manager verfügt, wird die Managerhierarchie in der **[!UICONTROL Daten werden angezeigt für]** Dropdown-Liste. Der Benutzer wird auf allen Detailseiten in der Managerhierarchie aufgeführt (Lernzusammenfassung, Compliance und Kenntnisstatus).

Andernfalls werden alle individuellen Benutzerdetails in der Liste angezeigt.

Um detailliertere Informationen zu den Registrierungen für verschiedene interne Teams anzuzeigen, klicken Sie auf **[!UICONTROL Lernzusammenfassungsdetails]**.

![](assets/learning-sunnarydetails.png)
*Lernzusammenfassungsdetails*

Wenn Sie auf eine Registrierung klicken, können Sie die Teilnehmer für jeden Manager sehen und die Registrierung für welche Lernobjekte. Sie können auch die Details der einzelnen Teilnehmer zu Fortschritt und Abschluss sehen.

![](assets/learners-for-a-manager.png)
*Teilnehmer, die einem Manager zugewiesen sind*

Klicken Sie auf ein beliebiges Team und exportieren Sie seinen Bericht als CSV-Datei. Ein Administrator kann den Bericht für jede Benutzergruppe oder jeden einzelnen Benutzer exportieren, indem er die Benutzergruppe oder den einzelnen Benutzer auswählt und dann die Details aus dem Fenster &quot; **[!UICONTROL Aktion]** Dropdown-Liste.

Sie können auch ein Balkendiagramm mit den Qualifikationen anzeigen, die gerade erworben wurden. Sie können Kenntnisse hinzufügen/entfernen, die Sie im Diagramm verwenden möchten.

![](assets/skill-status-stackedbarchart.png)
*Gestapeltes Balkendiagramm zum Kenntnisstatus*

In der endgültigen Visualisierung können Sie den Konformitätsstatus der Teilnehmer überprüfen und geeignete Maßnahmen ergreifen.

Außerdem kann ein Administrator einzelne Schulungsdaten im Fenster &quot; **[!UICONTROL Kompatibilitäts-Dashboard]**.

Der Administrator hat beispielsweise drei Schulungen zur Überwachung der Konformität identifiziert. Learning Manager bietet die Kompatibilitäts-Momentaufnahme für alle drei Schulungen gleichzeitig.

Jetzt kann ein Administrator auf eine Schulung klicken und schnell die Konformität für die ausgewählte Schulung anzeigen.

![](assets/compliance-dashboard.png)
*Kompatibilitäts-Dashboard anzeigen*

Sie können auch den Konformitätsstatus für jedes interne Team sehen.

Klicken Sie auf den Link **[!UICONTROL Konformitätsstatusdetails]** unten in der Visualisierung.

Sie können sehen, dass für ein Team die Anzahl der Teilnehmer im Team die Lernkonformität verletzt oder respektiert.

![](assets/compliance-statusofateam.png)
*Konformitätsstatus eines Teams*

### Schulungen für Manager freigeben

Learning Manager bietet allen Administratoren und Managern ein Compliance-Dashboard. Manager finden es sehr nützlich, die Einhaltung der Richtlinien durch ihre Teammitglieder für eine bestimmte Schulung zu verfolgen. Gleichzeitig möchten Administratoren, dass alle Manager Compliance-Schulungen zu ihrem Dashboard hinzufügen und verfolgen.

Im Lern-Manager zeigt der Katalog **[!UICONTROL Für Manager freigeben]** ermöglicht es Administratoren, Schulungen mit Managern zu teilen, sodass sie dem Compliance-Dashboard eines Managers hinzugefügt werden können. Manager müssen also keine Maßnahmen ergreifen und können sofort mit der Überwachung der Compliance beginnen.

Ein Administrator kann eine Reihe von Schulungskursen mit Managern einzeln oder mit einer Gruppe teilen. Diese Freigabe kann einem Manager dabei helfen, die Einhaltung der Richtlinien durch sein Team für die angegebene Schulung einfach zu verfolgen.

Der Administrator kann eine Standardliste der Compliance-Schulung &quot;pushen&quot;, die im Compliance-Dashboard des Managers angezeigt wird.

### Schulungen teilen

1. In **[!UICONTROL Berichte]** > **[!UICONTROL Übersicht zu Lernprogrammen]**, scrollen Sie nach unten und klicken Sie auf die Registerkarte **[!UICONTROL Für Manager freigeben]**.

   ![](assets/share-with-managers.png)
   *Schulungen mit Managern teilen*

1. Um eine Schulung oder mehrere Schulungen hinzuzufügen, klicken Sie auf **[!UICONTROL Mehr freigeben]**.

1. Im Dialogfeld &quot; **[!UICONTROL Für Manager freigeben]** &quot; die Schulung(en) und den Manager(en) aus.

   ![](assets/select-training.png)
   *Wählen Sie Schulungen aus, die Sie mit Managern teilen möchten*

1. Klicken Sie auf **[!UICONTROL Freigeben]**.

Die Schulung wird jetzt für den angegebenen Manager freigegeben.

### Schulung anzeigen

Klicken Sie in der Liste der freigegebenen Schulungen auf **[!UICONTROL Anzeigen]**. Sie können die Schulung anzeigen, die einem Manager oder einigen Managern zugewiesen ist.

### Schulungen zurückziehen

1. Um einem Manager die Schulung zu entziehen, klicken Sie auf **[!UICONTROL zurückziehen]**.

1. Klicken **[!UICONTROL Fortfahren]**. Dadurch werden zuvor freigegebene Schulungen aus dem Compliance-Dashboard des Managers zurückgezogen.

## Benutzerdefinierte Berichte

Administratoren können bestimmte Berichte mithilfe der benutzerdefinierten Vorlage generieren, die auf der Registerkarte &quot; **[!UICONTROL Berichte]** Abschnitt.

### Beispielberichte {#samplereports}

Die Registerkarte **[!UICONTROL Beispielberichte]** zeigt einige Musterberichte an, die aufgrund von Beispieldaten erstellt wurden. Sehen Sie sich diese Berichte an, um zu verstehen, welche funktionsreichen Berichtsvarianten Sie mit Ihren Kontodaten generieren können.

### Dashboard-Berichte {#dashboardreports}

Ein Dashboard ist eine Sammlung von Berichten. Berichte können nach Ihren Wünschen in einem Dashboard gruppiert werden. Klicken Sie auf diese Dashboard-Registerkarte, um alle von Ihnen erstellten Dashboards anzuzeigen. Im Fenster &quot; **[!UICONTROL Dashboard anzeigen]** können Sie das voreingestellte Board auswählen oder ein Dashboard, das Sie erstellt haben.

### Excel-Berichte {#excelreports}

Auf der Registerkarte **[!UICONTROL Excel-Berichte]** können Sie Berichte im XLS-Dateiformat exportieren.

Die folgenden Berichtstypen können heruntergeladen werden.

* Kursberichte
* Teilnehmertranskripte
* Bericht für Ankündigungen
* Bericht zu Arbeitshilfen
* Inhaltsprüfpfad
* Benutzerprüfpfad
* Anmelde-/Zugriffsbericht
* Gamification-Transkripte
* Gamification-Prüfpfad

### Teilnehmertranskripte {#learnertranscripts}

In den Teilnehmertranskripten in Excel-Berichten werden die Spalten „Benötigte Credits“ und „Verdiente Credits“ in Dezimalzahlen angezeigt. 

### Kursberichte {#coursereports}

Als Administrator können Sie Berichte für Kurse herunterladen. Führen Sie die folgenden Schritte aus:

1. Öffnen **[!UICONTROL Berichte]** > **[!UICONTROL Benutzerdefinierte Berichte]** > **[!UICONTROL Excel-Berichte]** > **[!UICONTROL Kursberichte]**.
1. Das Dialogfeld **[!UICONTROL Kursbericht]** wird angezeigt. Wählen Sie den Kurs aus, von dem Sie den Bericht abrufen möchten, und klicken Sie auf **[!UICONTROL Anzeigen]**.

   ![](assets/course-reports.png)
   *Kursberichte*

1. Sie werden auf die Kursseite weitergeleitet. Sie können die Quizpunktzahl nach Benutzer und Frage exportieren, basierend auf jeder Registrierung, indem Sie den spezifischen Registrierungstyp auswählen.
1. Wählen Sie **[!UICONTROL Quizpunktzahl exportieren]**, um den Bericht zu exportieren. Das Dialogfeld **[!UICONTROL Erstellen einer Berichtsanforderung]** wird geöffnet. Klicken Sie auf **[!UICONTROL OK]**, um zu bestätigen.

   ![](assets/generating-reportrequest.png)
   *Erstellen einer Berichtsanforderung*

   >[!NOTE]
   >
   >Der exportierte Bericht zur Quizpunktzahl enthält die Bewertungsdetails für jeden Versuch, wenn die Option „Mehrfachversuch“ für das Modul konfiguriert ist.

### Teilnehmertranskripte {#LearnerTranscripts-1}

Mit Adobe Learning Manager können die Administratoren eines Unternehmens die Transkripte erstellen, die mit den Teilnehmenden verknüpft sind. Der Teilnehmertranskriptbericht enthält Folgendes:

1. Teilnehmertranskript: Dashboard für Lernaktivitäten
1. Kenntnisse: Dashboard für Kenntnisse
1. Kompatibilitäts-Dashboard

In den Teilnehmertranskripten in Excel-Berichten werden die Spalten „Benötigte Credits“ und „Verdiente Credits“ in Dezimalzahlen angezeigt. 

Weitere Informationen zum Erstellen von Teilnehmertranskriptberichten und weitere Informationen finden Sie unter [Teilnehmertranskripte](learner-transcripts.md).

### Berichte für Ankündigungen {#announcementsreports}

Als Administrator können Sie einen Bericht aller Ankündigungen generieren, die Sie senden. Der Bericht enthält Details zu:

* Ankündigungstyp
* Name der Ankündigung
* Ankündigungsdatum
* Status der Ankündigung
* Teilnehmername

Um einen Bericht herunterzuladen, führen Sie einen der folgenden Schritte aus:

1. Öffnen **[!UICONTROL Berichte]** > **[!UICONTROL Benutzerdefinierte Berichte]** > **[!UICONTROL Excel-Berichte]** > **[!UICONTROL Bericht für Ankündigungen]**. Das Dialogfeld **[!UICONTROL Erstellen einer Berichtsanforderung]** wird geöffnet. Klicken Sie auf OK.
1. [!UICONTROL **Ankündigungen**] > [!UICONTROL **Aktionen**] > [!UICONTROL **Bericht exportieren**].

   ![](assets/announcements.png)
   *Bericht für Ankündigungen*

1. Sie können einen Bericht für eine bestimmte Ankündigung extrahieren, indem Sie auf **[!UICONTROL Bericht exportieren]** unter dem Symbol &quot;Einstellungen&quot;.

   ![](assets/announcements-specific-report.png)
   *Bericht für bestimmte Ankündigungen*

### Bericht zu Arbeitshilfen {#jobaidsreport}

Arbeitshilfen sind Schulungsmaterialien, auf die ein Teilnehmer zugreifen kann, ohne dass sie sich für spezifische Lernobjekte wie beispielsweise für einen Kurs oder ein Lernprogramm registrieren müssen. Administratoren können Arbeitshilfen extrahieren und herunterladen.

Der extrahierte Bericht enthält Informationen zu folgenden Themen:

* Name
* Typ der Arbeitshilfe
* Status der Arbeitshilfe (veröffentlicht oder eingestellt)
* Registrierungsdatum
* Datum des Abschlusses
* Downloaddatum
* Teilnehmername
* Managername
* Erstellt von

Führen Sie eine der folgenden Schritte aus, um einen Bericht herunterzuladen:

* Öffnen  **[!UICONTROL Berichte]** > **[!UICONTROL Benutzerdefinierte Berichte]** > **[!UICONTROL Excel-Berichte]** > **[!UICONTROL Arbeitshilfeberichte]**. Das Dialogfeld **[!UICONTROL Erstellen einer Berichtsanforderung]** wird geöffnet. Klicken Sie auf **[!UICONTROL OK]**.
* Öffnen **[!UICONTROL Arbeitshilfe]** > **[!UICONTROL Aktionen]** > **[!UICONTROL Bericht exportieren]**.

![](assets/job-aids.png)
*Bericht zu Arbeitshilfen*

* Sie können einen Bericht für eine bestimmte Arbeitshilfen extrahieren, indem Sie auf **[!UICONTROL Bericht exportieren]** unter dem Symbol „Einstellungen“ klicken.

![](assets/job-aid-specific-download.png)
*Bericht für bestimmte Arbeitshilfe*

### Bericht zu Arbeitshilfen

Nachdem Sie **[!UICONTROL Bericht zu Arbeitshilfen]** in der Liste sehen Sie zwei Optionen:

![Arbeitshilfebericht](assets/job-aids-new.png)
*USer-Registrierungsbericht für Arbeitshilfen herunterladen*

**Alle Arbeitshilfen**: Wenn die Anzahl der Arbeitshilfen im Konto weniger als 10 Millionen beträgt, enthält der generierte Bericht Registrierungsinformationen aller Arbeitshilfen. Dies ist die Standardauswahl. Wenn die Anzahl der Zeilen 10 Millionen überschreitet, wird ein Fehler angezeigt und Sie müssen die erforderlichen Arbeitshilfen manuell auswählen.

**Ausgewählte Arbeitshilfen**: Wenn Sie diese Option auswählen, können Sie die Arbeitshilfen eingeben, für die Sie den Bericht generieren möchten. Sie können maximal 10 Arbeitshilfen auswählen. Adobe Learning Manager überprüft, ob die Anzahl der Arbeitshilfen 10 Millionen übersteigt.

![Registrierung des Arbeitshilfeberichts](assets/job-aids-2-new.png)
*Arbeitshilfe auswählen*

**Bericht zu Arbeitshilfen**

Wenn Sie diese Option auswählen, werden die Details aller im System vorhandenen Arbeitshilfen zusammen mit ihren Metadaten und Schulungen heruntergeladen.

Der heruntergeladene Bericht enthält folgende Felder:

* Name der Arbeitshilfe
* Sprache(n)
* ID
* Typ
* Dauer (Minuten)
* Status
* Veröffentlicht am (UTC-Zeitzone)
* Erstellt nach Name
* Erstellt nach E-Mail
* Erstellt nach eindeutiger ID
* Katalog(e)
* Lernpfad(e)
* Kurs(e)
* Tag(s)
* Kenntnis(se)

**Bericht zur Registrierung von Arbeitshilfen für Benutzer**

Der Registrierungsbericht enthält Details zur Benutzerregistrierung und andere Informationen.

Der heruntergeladene Bericht enthält folgende Felder:

* Name der Arbeitshilfe
* Typ
* Status
* Registrierungsdatum (UTC-Zeitzone)
* Datum abgeschlossen (UTC-Zeitzone)
* Downloaddatum (UTC-Zeitzone)
* Teilnehmendenname
* E-Mail
* Eindeutige ID des Benutzers
* Managername
* E-Mail-Adresse des Managers
* Eindeutige Manager-Benutzer-ID
* Nach Name zugewiesen
* Per E-Mail zugewiesen
* Zugwiesen nach eindeutiger Benutzer-ID
* Erstellt nach Name
* Erstellt nach E-Mail
* Erstellt nach eindeutiger ID
* Arbeitscode
* Neues Feld
* Profil

### Berichte zu Inhaltsprüfpfaden {#contentaudittrailreports}

Verwenden Sie die **[!UICONTROL Inhaltsprüfpfad]** Bericht-Generator zum Generieren eines Berichts über alle Änderungen und Bearbeitungen, die an einem Kurs während seiner Lebensdauer im System vorgenommen wurden. Der generierte Bericht enthält die folgenden Informationen.

* Objekt-ID
* Objektname
* Objekttyp
* Änderungstyp
* Beschreibung
* ID des referenzierten Objekts
* Referenzierter Objektname 
* Geändert von Benutzername
* Geändert von Benutzer-ID
* Änderungsdatum (UTC-Zeitzone) 

Informationen zu Metadaten werden nicht im generierten Bericht aufgerufen.

Um einen Kursprüfprotokollbericht zu generieren, führen Sie die folgenden Schritte aus.

1. Auswählen **[!UICONTROL Bericht]** > **[!UICONTROL Excel-Berichte]** > **[!UICONTROL Kursprüfprotokoll]**. Das Dialogfeld **[!UICONTROL Inhaltsprüfpfad]** wird angezeigt.

   ![](assets/course-audit-trial.png)
   *Kursprüfprotokoll*

1. Wählen Sie den Kurs, die Lernprogramme und Zertifizierung aus, von deren die den Bericht herunterladen möchten. Wenn nicht angegeben, werden alle Berichte standardmäßig heruntergeladen.
1. Wählen Sie einen Datumsbereich für den Bericht aus und klicken Sie auf **[!UICONTROL Generieren]**.
1. Der Bericht wird erstellt und Sie werden benachrichtigt, dass der Prüfbericht bereit ist. Sie können den Bericht herunterladen.

### Berichte zu Benutzerprüfpfaden {#useraudittrailreports}

Der Benutzerprüfpfad erfasst den Lebenszyklus von Benutzern, Benutzergruppen und Selbstregistrierungsprofilen. Hier werden das Hinzufügen, Löschen, ein Wechseln des Managers für Benutzer erfasst. Die Erstellung und Löschung von Selbstregistrierungsprofilen werden aufgezeichnet. Sie können die Selbstregistrierung auch aussetzen und fortsetzen.

Sie können externe Profile hinzufügen, aktivieren, deaktivieren, aussetzen oder fortsetzen, die Selbstregistrierung hingegen hinzufügen, löschen, aussetzen oder fortsetzen. CSV-Uploads werden ebenfalls erfasst.

1. Auswählen  **[!UICONTROL Bericht > Excel-Bericht > Benutzerprüfpfad]**. Das Dialogfeld &quot;Benutzerprüfpfad&quot; wird angezeigt.
1. Das Dialogfeld „Benutzerprüfpfad“ wird angezeigt. Wählen Sie den Datumsbereich im Popupmenü. Sie können den Bericht wahlweise für die letzte Woche oder den letzten Monat generieren oder ein benutzerdefiniertes Datum wählen.

   ![](assets/user-audit-trail.png)
   *Benutzerprüfpfad*

1. Klicken Sie auf **[!UICONTROL Generieren]**, um den Bericht zu generieren.

Es gibt zwei Filter im Dialogfeld **[!UICONTROL Benutzerprüfpfad-Bericht]**.

**Filter &quot;Datumsbereich&quot;:** Wählen Sie den Datumsbereich aus, für den Sie den Bericht generieren möchten. Es gibt drei Optionen:

* Letzte Woche
* Letzter Monat
* Benutzerdefiniertes Datum

Filter &quot;Teilnehmer wählen&quot;: Suchen Sie nach einem Benutzer oder einer Benutzergruppe.

Der exportierte Bericht enthält Daten der Benutzer, die beide Suchkriterien erfüllen.

![](assets/user-audit-trail.png)
*Benutzerprüfpfad*

>[!NOTE]
>
>Wenn Kenntnisse zugewiesen oder entfernt werden, können sie für den Benutzerprüfungsbericht verfolgt werden, sowohl für zugewiesene als auch für entfernte Kenntnisse.

### Bericht über die Konfiguration der Erweiterung

Dieser Bericht enthält Informationen zu den Konfigurationsdetails aller hinzugefügten nativen Erweiterungen, einschließlich ihres Aktivierungsstatus. Informationen zum Herunterladen des Erweiterungsberichts finden Sie unter [Erweiterungsbericht herunterladen](native-extensibility.md#download-extension-report).

### xAPI-Aktivitätsbericht

Dieser Bericht enthält die Daten aller xAPI-Anweisungen, die während xAPI-Aktivitätsmodulen aufgezeichnet und generiert wurden.

Um diesen Bericht herunterzuladen, führen Sie die folgenden Schritte aus:

1. Auswählen  **[!UICONTROL Bericht > Excel-Bericht > xAPI-Aktivitätsbericht]**. Das Dialogfeld &quot;xAPI-Aktivitätsbericht&quot; wird angezeigt.
1. Wählen Sie den Datumsbereich im Popupmenü. Sie können den Bericht wahlweise für die letzte Woche oder den letzten Monat generieren oder ein benutzerdefiniertes Datum wählen.
1. Wählen Sie Teilnehmer und Aktivität aus dem Dropdown-Menü aus.
1. Auswählen **[!UICONTROL Generieren]** , um den Bericht zu generieren.

### Gamification-Berichte {#gamification}

Administratoren können das Gamification-Transkript im CSV-Format herunterladen. Sie können den Bericht entweder für einzelne Benutzer oder Benutzergruppen herunterladen. Benutzername, Benutzer-E-Mail-Adresse, Benutzer-UUID, erreichte Gesamtpunktzahl des Benutzers, Aufteilung der gesammelten Punkte, Name der Gruppen, in denen der Benutzer spielt, Name des Managers und Werte für aktive Felder werden alle im Bericht abgerufen. Administratoren können diesen Bericht verwenden, um Benutzerrangfolgen auf Organisationsebene oder für eine bestimmte Gruppe zu bewerten und zu analysieren.

1. Wählen Sie Bericht > Excel-Bericht > Gamification-Bericht.

   ![](assets/gamification.png)
   *Gamification-Bericht*

1. Das Dialogfeld „Gamification-Transkripte“ wird angezeigt. Wählen Sie Teilnehmer anhand ihres Namens, Profils, ihrer Benutzergruppen, ihrer E-Mail-ID oder ihrer UUID aus.

   ![](assets/gamification-transcriptsdialog.png)
   *Dialog Gamification-Transkripte*

1. Klicken  **[!UICONTROL Generieren]** , um den Bericht zu generieren.

   Nachdem Sie den Bericht eines Teilnehmers erstellt haben, müssen Sie in der Lage sein, die aktuellen und erreichten Informationen für alle Benutzer (intern, extern oder gelöscht) im Konto zu exportieren. Sie können auch die Daten für die von einem Teilnehmer erreichte Kenntnisstufe überprüfen:

   * Datum, an dem Bronze erreicht wurde
   * Datum, an dem Silber erreicht wurde
   * Datum, an dem Gold erreicht wurde
   * Datum, an dem Platin erreicht wurde

   Diese Spalten enthalten die Daten, an denen die Kenntnisstufe zum ersten Mal erreicht wurde. Die Spalte **[!UICONTROL Aktuelle Stufe]** zeigt die aktuelle Stufe des Teilnehmers an.

   Wenn der Administrator die Gamification zurücksetzt, werden alle Punkte des Teilnehmers entsprechend zurückgesetzt.

### Gamification-Audit-Bericht {#gamification-audit-trail}

Dieser Bericht enthält den Verlauf und die Gründe für die Gamification-Punkte der Teilnehmer, die für jede Regel gesammelt wurden.

### Bericht herunterladen

1. Wählen Sie die Gamification-Prüfprotokoll-URL aus.
1. Im Fenster &quot; **Gamification-Prüfprotokoll** den Datumsbereich aus.
1. Auswählen **Generieren**.

Der Bericht wird als CSV-Datei heruntergeladen. Die Datei enthält die folgenden Spalten:

* Name
* E-Mail/UUID,
* Status
* Aktion
* Punkte,
* Ausgleichspunkte
* Regel/Aufgabe
* Regel-/Teilaufgabe,
* Regel-/Aufgabendetails
* Typ,
* Name
* InstanznameErreichtes Datum (UTC-Zeitzone)
* Regel-/Vorgangsstartzeit
* Regel-/Vorgangsendzeit

### Bericht zur Registrierung und Aufhebung der Registrierung {#enrollmentandunenrollmentreport}

Administratoren und Manager können einen Bericht der Teilnehmer extrahieren, die sich registriert bzw. ihre Registrierung aufgehoben haben. Als Administrator können Sie alle Teilnehmer, Administrator oder Manager sehen, die von einer Instanz eines Kurses des Lernprogramms oder der Zertifizierung registriert wurden oder deren Registrierung aufgehoben wurde und Sie können den Bericht exportieren. Als Manager können Sie jedoch nur einen Bericht Ihrer Teammitglieder abrufen. Als Manager können Sie nicht die gelöschten Teilnehmer oder Ihren eigenen Namen in der Manager-Anwendung als registrierter oder nicht registrierter Teilnehmer sehen.

Um einen Bericht herunterzuladen, führen Sie die folgenden Schritte aus: Öffnen Sie die  **[!UICONTROL Kurs/Lernprogramm/Zertifizierung]** > **[!UICONTROL Teilnehmer]** > **[!UICONTROL Aktion]** > **[!UICONTROL Bericht exportieren]**.

![](assets/unenrollment.png)
*Bericht zur Aufhebung der Registrierung*

### Feedbackbericht {#feedback-report}

Als Administrator können Sie jetzt sowohl Teilnehmer-Feedback (L1) als auch Manager-Feedback (L3) für ausgewählte Schulungen für einen bestimmten Zeitraum abrufen.

Sie können die Daten über die Benutzeroberfläche oder über den PowerBI-Connector exportieren, um eine detaillierte Analyse durchzuführen.

L1- und L3-Feedbackberichte bieten die Möglichkeit, einen konsolidierten Feedbackbericht für die L1- und L3-Antworten für ausgewählte Schulungen für eine **einjährige** oder für bis zu 10 ausgewählte Schulungen für einen beliebigen Datumsbereich.

Melden Sie sich als Administrator an, und klicken Sie auf **[!UICONTROL Berichte]** > **[!UICONTROL Benutzerdefinierte Berichte]** und klicken Sie in der Liste der Berichte auf **[!UICONTROL Feedbackbericht]**.

![](assets/download-feedbackreport.png)
*Feedbackbericht herunterladen*

Wenn Sie nach Auswahl der Filter auf &quot;Herunterladen&quot; klicken, erhalten Sie eine Benachrichtigung, dass Sie den Bericht im CSV-Format herunterladen können.

Der heruntergeladene Bericht enthält Details wie Schulungsname und -typ, Instanzname, Name und E-Mail-Adresse des Teilnehmers, Typ des Feedbacks: L1 oder L3, Datumsangaben des übermittelten Feedbacks für neue Daten.

Für vorhandene Daten vor dieser Funktionsimplementierung wird das LO-Abschlussdatum angezeigt, LO-Abschlussdatum, L1-Feedbackfrage: Selbststufiger aktueller Text und Klassenzimmertext in verschiedenen Spalten, L1-Feedback: entsprechende Antworten, Name und E-Mail-Adresse des Managers, L3-Feedbackwert und Sendedatum, aktive Felder.

Sie können die Daten auch von der Benutzeroberfläche oder auf den Power BI exportieren, wodurch alle Schulungen für einen beliebigen Datumsbereich für eine tiefere Analyse unterstützt werden.

### Schulungsbericht {#training-report}

Learning Manager unterstützt den Schulungsbericht, mit dem Administratoren Schulungsdetails und die zugehörigen Metadaten wie Autor, Veröffentlichungsdatum, Kenntnisse, Katalogbeschriftungen usw. herunterladen können.

Klicken Sie in der Admin-App auf **[!UICONTROL Berichte]** > **[!UICONTROL Benutzerdefinierte Berichte]** > **[!UICONTROL Excel-Berichte]** > **[!UICONTROL Schulungsbericht]**.

Sie können Berichte für Folgendes herunterladen:

* Ausgewählte Schulungen (maximal 10): Eine oder mehrere Schulungen (bis zu 10) aus einem beliebigen Katalog werden ausgewählt.
* Alle Schulungen im ausgewählten Katalog (maximal 5) – Katalogauswahl ist bis zu fünf Katalogen verfügbar.
* Alle Schulungen – alle Schulungen im Konto

![](assets/download-trainingreport.png)
*Schulungsbericht herunterladen*

Im Abschnitt &quot;Erweiterte Optionen&quot; sind die folgenden Optionen verfügbar:

* Kurszuordnungen mit Lernprogramm/Zertifizierung einschließen
* Modulebeneninformationen einschließen

Nachdem Sie die Filter ausgewählt und auf &quot;Herunterladen&quot; geklickt haben, erhalten Sie eine Benachrichtigung, dass Sie den Bericht im CSV-Format herunterladen können.

Der Bericht enthält folgende Felder:

*Katalogname, Schulungstyp, Schulungs-ID, eindeutige Schulungs-ID, Schulungsname, untergeordnete Schulungen, Module, Dauer von Schulung oder Modul, Format, Status der Schulung, Kenntnisse, Autor, Datum der letzten Veröffentlichung, Datum des letzten Abschlusses, Anzahl der Registrierungen durch Kursleiter, Anzahl der Beginne, Anzahl der Abschlüsse, durchschnittliche L1-Punktzahl, durchschnittliche L2-Punktzahl, durchschnittliche L3-Punktzahl, erhaltene L1-Antworten, erhaltene L2-Antworten, erhaltene L3-Antworten, Katalogbeschriftungen und -tags.*

![](assets/more-options.png)
*Weitere Optionen*

### Sitzungsübersicht – Bericht {#session-summary-report}

Der Sitzungsübersichtsbericht enthält alle Sitzungen, die für einen Teilnehmer innerhalb eines bestimmten Datums geplant sind.

Dadurch kann der Administrator alle Sitzungsdetails für virtuelle und Klassenzimmer exportieren, die in den angegebenen Datumsbereich fallen. Der Administrator kann den Sitzungsbericht auch in Bezug auf bestimmte Schulungen oder Kursleiter exportieren.

Dadurch kann der Administrator auch die geplanten monatlichen Sitzungen nachvollziehen und den Zeitplan der Kursleiter und die bereits durchgeführten Sitzungen identifizieren.

Klicken Sie als Administrator auf **[!UICONTROL Benutzerdefinierte Berichte]** > **[!UICONTROL Sitzungsübersicht - Bericht]**.

Wählen Sie im folgenden Dialogfeld den Datumsbereich und entweder eine Schulung oder einen Kursleiter für den Bericht aus.

![](assets/session-summary-report.png)
*Sitzungsübersicht - Bericht*

Die heruntergeladene CSV-Datei enthält die folgenden Felder:

* Startdatum und -uhrzeit
* Enddatum und -uhrzeit

* Modulname
* Sitzungsdauer (in Minuten)
* Sitzanzahl
* Standort
* Instanzname
* Kursname
* Kurs-ID
* Kursleitername
* Kursleiter-E-Mail
* Anzahl der Registrierungen
* Sitzungstyp
* Limit für Warteliste
* Warteliste – Anzahl
* Warteliste – Benutzer-E-Mail-Adressen
* Standortinformationen
* Standortregion

### Bericht zur Auslastung von Kursleiter(innen)

Dieser Bericht erfasst die Zeit (in Minuten), die Kursleiter(innen) täglich mit zugewiesenen Sitzungen verbringen. Der Bericht kann für einen Zeitraum von drei Monaten ab dem ausgewählten Startdatum heruntergeladen werden.

Klicken Sie auf **[!UICONTROL Berichte]** > **[!UICONTROL Benutzerdefinierte Berichte]** > **[!UICONTROL Bericht zur Auslastung der Kursleiter]**.

Wählen Sie einen oder mehrere Kursleiter(innen) und den Datumsbereich aus.

![Bericht zur Kursleiterauslastung herunterladen](assets/utilization-report.png)
*Bericht zur Kursleiterauslastung herunterladen*

Der heruntergeladene Bericht enthält die folgenden Felder:

* Kursleitername
* Kursleiter(innen)-ID
* Kompetenzniveau
* Datumsangaben in Spalten. Wenn Kursleiter(innen) an einem Tag ausgelastet sind, wird die Anzahl der Sitzungen aufgeführt. Wenn Kursleiter(innen) an einem Tag nicht ausgelastet sind, wird der Wert Null angezeigt.

Der Bericht enthält Datensätze für drei Monate ab dem ausgewählten Monat.

Um Datensätze aller Kursleiter(innen) abzurufen, lassen Sie das Feld &quot;Kursleiter(in)&quot; leer.

Außerdem kann ein(e) benutzerdefinierte(r) Administrator(in) mit der Berechtigung zum Generieren von Berichten diesen Bericht abrufen.

### Benutzerprüfpfad-Bericht

Dieser Bericht enthält Informationen über Teilnehmer, die Instanzen gewechselt haben, z. B. zwischen &quot;von der Instanz&quot; und &quot;zur Instanz&quot;, die nach Zeit, Datum usw. gewechselt haben.

Wählen Sie die Teilnehmenden oder eine Benutzergruppe aus.

Klicken Sie auf **[!UICONTROL Berichte]** > **[!UICONTROL Benutzerdefinierte Berichte]** > **[!UICONTROL Bericht zu Benutzerprüfpfaden]**.

![Benutzerprüfprotokollbericht herunterladen](assets/user-audit-report.png)

*Benutzerprüfprotokollbericht herunterladen*

### Lernplanbericht

Dieser Bericht enthält Details zu allen Lernplänen in einem Konto, z. B. zugehörige Benutzergruppen, Status und Auslöserinformationen.

Der Bericht enthält Folgendes:

* Name des Lernplans
* Typ (tritt auf, wenn)
* Schulung (abgeschlossen)
* Kenntnisse (erreicht)
* Datum (Datum)
* Aktion
* Status, erstellt von
* Erstellungsdatum
* Datum der letzten Änderung
* Benutzergruppe (gilt für)
* Benutzergruppe (hinzufügen zu)
* Registrieren nach
* Lernelementtyp(en)
* Lernelement(e)
* Lernelementinstanz(en)
* Lernelement
* Abschlussdatum
* Erinnerung für Lernelement
* Bereichskatalog
* Bereichsbenutzergruppe

## E-Mail Abonnements {#emailsubscriptions}

Sie erhalten Ihre wichtigsten Berichte per E-Mail, indem Sie sie abonnieren.

### E-Mail-Abonnements einrichten

>[!INFO]
>
>In dieser Schulung erfahren Sie, wie Sie E-Mail-Abonnements für Dashboard-Berichte einrichten.<br><br>[![Knopf](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=PLHRQ62N&amp;mv=display&amp;mv2=display#/course/8318927)</br></br>


Wenn Sie die Schulung nicht starten können, schreiben Sie an <almacademy@adobe.com>.

In **[!UICONTROL Berichte]** &quot; auf die Schaltfläche  **[!UICONTROL Abonnement]** &quot; ändern. Die Seite zum Abonnieren von Berichten erscheint.

Beginnen Sie mit der Eingabe des Berichtnamens in das Feld &quot;Berichte&quot;, um den Namen des Berichts aus der Dropdownliste auszuwählen. Wählen Sie die E-Mail-Häufigkeit aus der Dropdown-Liste aus. Sie können den Betreff der E-Mail hinzufügen und eine alternative E-Mail-ID angeben.

Sie können Abonnements bearbeiten und löschen.

## Historische Berichte

Historische Berichte in Adobe Learning Manager (ALM) beziehen sich auf die Berichte, die die historischen Daten und Aktivitäten innerhalb der Lernplattform erfassen. Diese Berichte bieten Einblicke in frühere Teilnehmeraktivitäten, Schulungsinhalte, die Leistung von Benutzergruppen und andere relevante Daten. Die historischen Berichte ermöglichen es Administratoren, den Fortschritt und die Effektivität von Lerninitiativen im Laufe der Zeit zu verfolgen, zu überwachen und zu analysieren.

### Kurszugriffsberichte

Die Kurszugriffsberichte enthalten Informationen über den erneuten Besuch der einzelnen Kurse.

Um diesen Bericht herunterzuladen, führen Sie die folgenden Schritte aus:

1. Wechseln zu **[!UICONTROL Berichte]** > **[!UICONTROL Benutzerdefinierte Berichte]** > **[!UICONTROL Historische Berichte]**.
1. Auswählen **[!UICONTROL Kurszugriffsbericht]**. Das Dialogfeld Erstellen einer Berichtsanforderung wird geöffnet.
1. Wählen Sie das Jahr und das Quartal aus dem Dropdown-Menü aus.
1. Auswählen **[!UICONTROL Generieren]**.

### Anmelde-/Zugriffsberichte

Die Anmelde-/Zugriffsberichte enthalten Informationen zu Benutzeranmeldungen und -zugriff. Sie können einen Bericht mit Daten von jeweils drei Monaten erstellen.

Um diesen Bericht herunterzuladen, führen Sie die folgenden Schritte aus:

1. Wechseln zu **[!UICONTROL Berichte]** > **[!UICONTROL Benutzerdefinierte Berichte]** > **[!UICONTROL Historische Berichte]**.
1. Auswählen **[!UICONTROL Anmelde-/Zugriffsbericht]**. Das Dialogfeld Erstellen einer Berichtsanforderung wird geöffnet.
1. Wählen Sie das Jahr und das Quartal aus dem Dropdown-Menü aus.
1. Auswählen **[!UICONTROL Generieren]**.

## Dashboard erstellen {#createadashboard}

1. Klicken Sie rechts auf der Seite auf Dashboard hinzufügen , um eigene Dashboards zu erstellen.

   ![](assets/add-dashboards.png)
   *Dashboards hinzufügen*

1. Geben Sie den Namen und die Beschreibung des Dashboards ein.
1. Wenn Sie das Dashboard für einen Manager freigeben möchten, wählen Sie diesen im **[!UICONTROL Freigeben für]** ein. Sie können für diese Aktion alle normalen Auswahlkriterien verwenden.
1. Klicken **[!UICONTROL Speichern].**

Sie können das kürzlich erstellte Dashboard in der Liste **[!UICONTROL Dashboard-Berichte]** sehen.

Um Ihrem Dashboard Berichte hinzuzufügen, klicken Sie in der rechten oberen Ecke Ihres Dashboard-Fensters auf das Dropdownmenü und dann auf **[!UICONTROL Bericht hinzufügen]**. Der so erstellte Bericht wird mit Ihrem Dashboard verknüpft.

>[!NOTE]
>
>Berichte, die Sie erstellen, indem Sie in der rechten oberen Ecke der Seite &quot;Berichte&quot; auf &quot;Hinzufügen&quot; klicken, werden Ihrem Standard-Dashboard hinzugefügt.

## Freigegebene Dashboards {#shareddashboards}

Freigegebene Dashboards sind eine Sammlung von Berichten, die andere Benutzer im Unternehmen für Sie freigegeben haben. Alle Berichte, die Sie diesen freigegebenen Dashboards hinzufügen, werden automatisch für andere Benutzer freigegeben, die Zugriff auf dieses Dashboard haben.

Sie haben zwei Möglichkeiten, das Board freizugeben:

* Durch Eingabe von Benutzern in **[!UICONTROL Freigeben für]** Feld, für das das Dashboard freigegeben wird.
* Sie wählen in der Dropdownliste die Option „Dashboard bearbeiten“ und geben die Benutzerdetails zur Freigabe des Dashboards ein.

>[!NOTE]
>
>Ein Manager kann die Berichte seiner Teammitglieder nur über ein freigegebenes Dashboard anzeigen.

## Downloads {#downloads}

Das exportierte Blatt mit Dashboard-Berichten enthält detaillierte Informationen anstelle der Berichtzusammenfassung. Der heruntergeladene Bericht folgt dem Format eines Teilnehmertranskripts.

## Berichte erstellen {#report}

1. Klicken Sie auf „Berichte“ im linken Bereich. Die Seite mit der Berichtzusammenfassung wird angezeigt.

   >[!NOTE]
   >
   >Standardmäßig befinden sich mindestens drei Beispielberichte auf der Registerkarte „Beispiel-Board“. Sie können diese Beispielberichte nicht bearbeiten, sondern nur anzeigen, um zu sehen, wie Sie sie erstellen und anpassen können.

1. Klicken Sie oben rechts auf der Seite auf **[!UICONTROL Hinzufügen]**.
1. Im Dialogfeld **[!UICONTROL Bericht hinzufügen]** können Sie in der Dropdown-Liste „Typ“ einen der vordefinierten Berichte auswählen oder **[!UICONTROL Benutzerdefiniert]** auswählen. Wenn Sie einen vordefinierten Bericht auswählen, sehen Sie, dass das Formular bereits ausgefüllt ist. Sie können weitere Änderungen an einigen Feldern vornehmen und auf **[!UICONTROL Speichern]** klicken. Dadurch wird der Bericht zu Ihrem Standard-Dashboard hinzugefügt.

   ![](assets/create-report.png)
   *Bericht erstellen*

   Unter **[!UICONTROL Berichtstyp]** können Sie einen Satz vordefinierter Berichte oder benutzerdefinierte Werte auswählen. Sie können die folgenden Berichte als Teil der vordefinierten Berichte aufrufen:

   * Zugewiesene und erreichte Kenntnisse
   * Kursregistrierungen und -abschlüsse
   * Effektivität von Kursen
   * Lernprogrammregistrierungen und -abschlüsse
   * Aufgewandte Lernzeit pro Kurs
   * Aufgewandte Lernzeit pro Quartal
   * Abschluss der Zertifizierung

1. Wählen Sie die **[!UICONTROL Y-Achse]** für Ihren Bericht aus den Drop-Down-Optionen. Für einige der ausgewählten Kriterien können Sie entweder eine oder mehrere Status von den Statusoptionen daneben auswählen. Beim primären Kriterium der Statistik zur Kursregistrierung können die Status beispielsweise „Abgeschlossen“, „Nicht abgeschlossen“ und „Registriert“ lauten. Daten des primären Bereichs werden im Bericht in Form von Balkendiagrammen dargestellt.

   ![](assets/axes-for-reports.png)
   *Achsen für Berichte*

1. Wählen Sie aus den Dropdown-Optionen die Kriterien für die sekundäre **[!UICONTROL Y-Achse]** bzw. den Bereich für Ihren Bericht aus. Wählen Sie zum Beispiel für eine Option betreffend die Registrierung für ein Lernprogramm einen oder mehrere Status aus dem Status-Dropdown-Menü neben der Option aus. Sekundäre Bereichsdaten werden im Bericht in Form von Liniendiagrammen dargestellt.
1. Wählen Sie aus den Dropdown-Optionen die für Ihren Bericht geeigneten X**-Achsen**-Kriterien aus. Wenn Sie das Datum als Kriterium für die x-Achse ausgewählt haben, steht Ihnen eine Option zur Gruppierung des x-Achsen-Kriteriums nach Tag, Monat, Quartal und Jahr zur Verfügung.
1. Wählen Sie die gewünschte Option aus dem Dropdown-Menü für die Zeitspanne aus. Die verfügbaren Optionen sind:

   * Letzter Monat
   * Quartal
   * Jahr
   * QTD (letzte 90 Tage)
   * YTD (letzte 365 Tage)
   * Datumsbereich Geben Sie Werte in die Felder **[!UICONTROL Von]** und **[!UICONTROL Bis]**-Datum ein.

   ![](assets/time-filter-for-report.png)

1. **Bereich „Filter“**

   Filter werden im Dialogfeld „Bericht hinzufügen“ am unteren Rand basierend auf Berichtstypen, die Sie ausgewählt haben, angezeigt. Einige der wichtigsten Filter sind nachfolgend aufgeführt.

   * **Manager:** Sie können jeden der Manager basierend auf der Hierarchieebene auswählen. Bei einigen Managern können untergeordnete Manager vorhanden sein, denen wiederum mehrere Mitarbeiter unterstellt sind.
   * **Profil:** Wählen Sie die Bezeichnung Ihres Mitarbeiters aus. Das hilft dabei, Berichte von Mitarbeitern basierend auf ihrem Profil/ihrer Einstufung abzurufen. Beispiel: Informatiker, Ingenieur.
   * **Benutzergruppe:** Wählen Sie die Benutzergruppe aus, je nachdem, wie Sie die Berichte filtern möchten. Learning Manager ruft die Benutzergruppen auf, die für Ihr Konto definiert wurden, aus der Benutzerfunktion aus.
   * **Inhalt:** Sie können Ihren Bericht nach Kursen filtern, indem Sie diese in der Dropdownliste auswählen.

   Erweitern Sie diesen Abschnitt und wählen Sie die gewünschten Filter aus.

   ![](assets/choose-filters.png)
   *Filter auswählen*

1. Klicken **[!UICONTROL Speichern]** , um das Erstellen eines Berichts abzuschließen.

   ![](assets/sample-report.png)
   *Beispielbericht*

## Bericht bearbeiten {#editareport}

Klicken Sie im Bericht auf den Dropdown-Pfeil und wählen Sie die Option aus. **[!UICONTROL Bericht bearbeiten]**.

![](assets/edit-a-report-1.png)
*Bericht bearbeiten*

Nehmen Sie die erforderlichen Änderungen am Bericht vor. Um die Änderungen zu speichern, klicken Sie auf **[!UICONTROL Speichern]**.

## Verschieben eines Berichts in ein Dashboard {#moveareporttoadashboard}

Wählen Sie diese Option, um den aktuellen Bericht in ein vorhandenes Dashboard zu verschieben. Um den Bericht zu verschieben, klicken Sie auf die Option **[!UICONTROL In Dashboard verschieben]**.

![](assets/move-a-report.png)
*Verschieben eines Berichts in ein Dashboard*

Wählen Sie das Dashboard aus, in das der Bericht verschoben werden soll, und klicken Sie auf **[!UICONTROL Verschieben]**.

## Erstellen Sie eine Kopie eines Berichts {#createacopyofareport}

Um eine Kopie des Berichts zu erstellen, wählen Sie die Option **[!UICONTROL Kopie erstellen]**.

![](assets/copy-a-report.png)
*Erstellen einer Kopie eines Berichts*

Wählen Sie das Dashboard aus, in das Sie den Bericht kopieren möchten. Um den Kopiervorgang zu starten, klicken Sie auf **[!UICONTROL Kopieren]**.

## Löschen eines Berichts {#deleteareport}

Um einen Bericht zu löschen, wählen Sie die Option **[!UICONTROL Bericht löschen]**. Nachdem Sie den Bericht gelöscht haben, können Sie den Bericht nicht wiederherstellen. Das Vorgang kann nicht rückgängig gemacht werden. Gehen Sie beim Löschen eines Berichts mit Vorsicht vor.

![](assets/delete-a-report.png)
*Bericht löschen*

## Herunterladen eines Berichts {#downloadareport}

Um den Bericht herunterzuladen, wählen Sie die Option **[!UICONTROL Bericht herunterladen]**.

![](assets/download-a-report.png)
*Bericht herunterladen*

## Ändern der Größe eines Berichts {#resizeareport}

Größe ändern Sie können die Größe Ihrer Berichte ändern in 1×1 (mittel) und 1×2 (groß). Auf diese Weise können Sie Ihre Berichte besser anzeigen. Sie können diese Berichte auch ganz einfach schwenken und zoomen.

## Filter {#filters}

Filter werden im Dialogfeld **[!UICONTROL Bericht hinzufügen]** am unteren Rand basierend auf Berichtstypen, die Sie ausgewählt haben, angezeigt. Einige der wichtigsten Filter sind nachfolgend aufgeführt.

**Manager** Sie können jeden der Manager basierend auf der Hierarchieebene auswählen. Bei einigen Managern können untergeordnete Manager vorhanden sein, denen wiederum mehrere Mitarbeiter unterstellt sind.

**Profil** Wählen Sie die Bezeichnung Ihres Mitarbeiters aus. Das hilft dabei, Berichte von Mitarbeitern basierend auf ihrem Profil/ihrer Einstufung abzurufen. Beispiel: Informatiker, Ingenieur.

**Benutzergruppe** Wählen Sie die Benutzergruppe aus, je nachdem, wie Sie die Berichte filtern möchten. Learning Manager ruft die Benutzergruppen auf, die für Ihr Konto definiert wurden, aus der Benutzerfunktion aus.

**Kurs** Sie können Ihren Bericht nach Kursen filtern, indem Sie diese in der Dropdownliste auswählen.

![](assets/sample-report-admin.png)
*Bericht filtern*

Über der Legende für das Diagramm können Sie ein Zoomfeld anzeigen Bewegen Sie den Cursor darauf und ziehen Sie das Cursorkreuz über irgendeinen Teil des Zoomfelds des Diagrammbereichs, um ihn zu zoomen.

Sie können die Werte der sekundären y-Achse in Form einer Linie durch die Diagrammbalken anzeigen. Im oben angeführten Beispiel sehen Sie beispielsweise die Werte für die Effektivität in einer grauen Linie durch das Diagramm.

## Benutzergruppenberichte {#user-group-reporting}

Verfolgen Sie nach, wie Benutzergruppen wie gut Abteilungen, externe Partner und Rollen im Vergleich zu anderen Benutzergruppen oder im Vergleich zu anderen Lernobjektiven funktionieren.

### Benutzergruppen {#usergroups}

Um Berichte basierend auf Benutzergruppen zu generieren, wählen Sie **[!UICONTROL Benutzergruppe]** in der x-Achse aus der Liste der Dropdown-Optionen, wie im folgenden Screenshot gezeigt.

![](assets/user-group-reports.png)
*Benutzergruppenberichte*

Um eine Benutzergruppe auszuwählen, geben Sie den Namen der Gruppe ein. Sie können die vorgeschlagenen Gruppen sehen, die gemäß der von Ihnen eingegebenen Zeichenfolge angezeigt werden. Wenn Sie eine Liste mit Gruppen sehen, wählen Sie die gewünschte Benutzergruppe aus.

Sie können auch mithilfe der Typ-Ahead-Suche mehrere Benutzergruppen auswählen.

Wenn Sie mehrere Benutzergruppen ausgewählt haben, wird, nachdem Sie den Bericht speichern und erstellen, der Bericht mit allen Benutzergruppen, die im Balkendiagramm neben jeder x-Achse dargestellt werden, erstellt.

Dieser Benutzergruppebericht ermöglicht Ihnen, die Leistung von einer Abteilung/Division/Rolle von Rolle mit anderen zu vergleichen, um ihre Lernleistungen auszuwerten.

### Benutzerdefinierte Benutzergruppen/Benutzerattribute {#customusergroupsuserattributes}

Sie können eigene Benutzergruppen mit der Funktion „Benutzer/Benutzergruppen hinzufügen“ in Learning Manager erstellen. Nachdem Sie die Benutzergruppen erstellt haben, können Sie die Berichte für die benutzerdefinierten Benutzergruppen mit einer Liste der Attribute wie Ort oder Zweigstelle generieren.

Wählen Sie in der x-Achse die Benutzerattributoption und wählen Sie das Attribut aus der Liste **aussuchen** daneben. Um einen benutzerdefinierten Benutzergruppebericht basierend auf diesen Attributen zu erstellen, müssen Sie auch die entsprechende Benutzergruppe im Filter auswählen.

## Anzeigen von Berichten {#viewingreports}

Auf der Seite „Berichte“ können Sie alle Berichte anzeigen. Sie können jeden Bericht minimieren, indem Sie auf das Minussymbol (-) in der rechten oberen Ecke jedes Berichts klicken. Klicken Sie auf das (+) Symbol, um den Bericht wieder anzuzeigen.

## Schnellansicht mit verschiedenen Datumswerten {#quickviewwithdifferentdates}

Sie können den Datumsbereich/-wert für jeden Bericht ändern und diesen schnell für ein anderes Datum anzeigen, ohne dabei den Bericht selbst zu ändern und zu speichern. Klicken Sie auf das Bearbeitungssymbol (wie in der Abbildung unten mit einem Pfeil gezeigt) neben dem Datumsbereich, z. B. QTD, letztes Jahr. Wählen Sie einen neuen Wert aus dem Dropdown-Menü aus und klicken Sie auf das Häkchen, um die Änderung zu bestätigen. Sie können die Änderungen verwerfen, indem Sie auf „X“ klicken.

>[!NOTE]
>
>Die Kalenderdaten bei der Anzeige des Berichts sind temporär. Wenn Sie die Option „Herunterladen“ wählen, wird diese Berichtsansicht nicht heruntergeladen. Es handelt sich dabei nur um eine temporäre Ansicht.

![](assets/learner-count-report.png)
*Anzahl der Teilnehmer anzeigen*

## Schnellansicht mit verschiedenen Managern {#quickviewwithdifferentmanagers}

Wenn Ihnen mehrere Manager unterstellt sind, können Sie die Berichte für jeden Manager schnell anzeigen. Wählen Sie in der Dropdownliste den Managernamen, um einen spezifischen Bericht für den entsprechenden Manager anzuzeigen.

>[!NOTE]
>
>Die Managerwerte, die Sie verwenden, um den Bericht anzuzeigen, sind temporär. Wenn Sie die Option „Herunterladen“ wählen, wird diese Berichtsansicht nicht heruntergeladen. Es handelt sich dabei nur um eine temporäre Ansicht.

## Kursberichte anzeigen {#viewcoursereports}

### Kursberichte generieren

>[!INFO]
>
>In dieser Schulung erfahren Sie, wie Sie Kursberichte exportieren und E-Mail-Abonnements für diese Berichte einrichten.<br><br>[![Knopf](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=R726NKNM&amp;mv=display&amp;mv2=display#/course/8318904)</br></br>


Wenn Sie die Schulung nicht starten können, schreiben Sie an <almacademy@adobe.com>.

Sie können zu jedem Kurs spezifische Berichte anzeigen.

1. Klicken **[!UICONTROL Kursberichte anzeigen]** auf der Registerkarte &quot;Meine Dashboards&quot; auf der Seite &quot;Berichte&quot;.\
   Ein Popup-Fenster wird angezeigt. Es wird ein Texteingabefeld angezeigt, in das Sie den erforderlichen Kurs eingeben können und in der Dropdown-Liste vorgeschlagene Kursnamen angezeigt werden. Wählen Sie aus der angezeigten Liste den Kurs aus.

   ![](assets/view-course-report-300x117.png)

   *Kursberichte anzeigen*

1. Wählen Sie aus der Dropdown-Liste den gewünschten Kurs aus und klicken Sie auf „Anzeigen“.
1. Sie werden zur Ergebnisseite mit den Quizpunktzahlen des ausgewählten Kurses umgeleitet, um den kursspezifischen Bericht anzuzeigen.

**Berichte bearbeiten/in Dashboard verschieben/Kopie erstellen/löschen/Größe ändern**

Klicken Sie in der rechten oberen Ecke eines Berichts auf den Pfeil der Dropdownliste, um die Dropdownoptionen für Bearbeiten, Verschieben ins Dashboard, Erstellen einer Kopie, Löschen und Größenänderung anzuzeigen.

![](assets/edit-options-dashboard-300x126.png)

*Berichte bearbeiten/in Dashboard verschieben/Kopie erstellen/löschen/Größe ändern*

**[!UICONTROL Bearbeiten]** Um nach dem Ändern von Daten zu den Anfangswerten zurückzukehren, klicken Sie auf &quot;Zurücksetzen&quot;. Klicken Sie auf „Speichern“, nachdem Sie die Werte geändert haben.

**[!UICONTROL Zum Dashboard verschieben]** Sie können den aktuellen Bericht in ein anderes Dashboard verschieben, das Sie aus der Liste der Dashboards auswählen.

**[!UICONTROL Kopie erstellen]** Sie können den Bericht in dasselbe oder ein anderes Dashboard kopieren, das Sie aus der Liste der Dashboards auswählen.

**[!UICONTROL Löschen]** Klicken Sie auf Löschen , um den Bericht zu entfernen. Bevor Sie den Bericht löschen können, wird eine Warn- bzw. Bestätigungsmeldung angezeigt.

**[!UICONTROL Größe ändern]** Sie können die Größe Ihrer Berichte ändern in 1×1 (mittel) und 2×2 (groß).

## Berichte für Peer-Konten erstellen und anzeigen {#generateandviewreportsforpeeraccount}

Als Administrator können Sie nicht nur Berichte für Ihr Konto erstellen, sondern auch Berichte für von Ihnen festgelegte Peer-Konten erstellen und anzeigen.

Wenn Sie ein Peer-Konto mit einem anderen Benutzer eingerichtet haben, können Sie die Berichte für dieses Peer-Konto über die Seite **[!UICONTROL Berichte]** anzeigen. Beim Erstellen eines Berichts finden Sie das Feld **[!UICONTROL Konto auswählen]** vor. Wählen Sie aus der Dropdownliste aller Peer-Konten, mit denen Sie verknüpft sind, das Konto, für das Sie die freigegebenen Berichte anzeigen möchten.

Wenn bei der Erstellung eines Peer-Kontos die Option „Freigegebene Kataloge“ nicht aktiviert war, wird das betreffende Konto nicht in dieser Liste angezeigt.

![](assets/acc1-jpg.png)
*Berichte für Peer-Konten verwalten*

1. Wählen Sie die x-Achse und die y-Achse sowie das Datum für diesen Bericht aus.
1. Beachten Sie, dass im Feld „Filter“ die Schaltfläche „Freigegebene Kataloge“ automatisch aktiviert ist. Dies ist erforderlich. Wenn die Option „Freigegebene Kataloge“ nicht aktiviert ist, bedeutet dies, dass Sie keine Berichte für das Peer-Konto erstellen oder anzeigen können.
1. Wählen Sie aus der Dropdownliste unter „Freigegebene Kataloge“ den freigegebenen Katalog, für den Sie den Bericht anzeigen möchten.
1. Klicken Sie auf [!UICONTROL **Speichern**].

   ![](assets/acc2.png)
   *Freigegebenen Katalog für Peer-Konto auswählen*

1. Nachdem Sie auf **[!UICONTROL Speichern]** können Sie die grafische Darstellung Ihrer Berichte in Ihrem Standard-Dashboard anzeigen. Über dieses Dashboard können Sie den Bericht weiter nach dem Manager für das jeweilige Peer-Konto filtern.
1. Änderungen, die Sie auf Ihrer Seite an dem Katalog vornehmen, spiegeln sich sofort in den vom Peer erstellten Berichten und in dessen Dashboard wider. Wenn jedoch der Peer den Katalog ändert, erscheinen die Änderungen nicht automatisch in Ihrem Dashboard.
1. Wenn Sie möchten, dass Ihr Dashboard automatisch aktualisiert wird, muss der Peer Ihnen eine neue Peer-Anforderung senden.

   >[!NOTE]
   >
   >Manager können Peer-Berichte nicht anzeigen.

## Häufig gestellte Fragen {#frequentlyaskedquestions}

+++Wie kann ein benutzerdefiniertes Dashboard für einen Manager freigegeben werden?

Geben Sie beim Erstellen eines Dashboards den Namen und die Beschreibung ein. Geben Sie zur Freigabe für den Manager den Namen des Managers in das Feld **[!UICONTROL Freigeben für]** ein.

![](assets/share-dashboard-manager.png)
*Dashboard freigeben*
+++

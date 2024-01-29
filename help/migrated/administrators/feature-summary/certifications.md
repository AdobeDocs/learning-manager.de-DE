---
description: Erfahren Sie, wie Sie Zertifizierungen erstellen, Teilnehmer registrieren und veröffentlichte Zertifizierungen bearbeiten.
jcr-language: en_us
title: Zertifikationen
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 0%

---



# Zertifikationen

Erfahren Sie, wie Sie Zertifizierungen erstellen, Teilnehmer registrieren und veröffentlichte Zertifizierungen bearbeiten.

Mit dieser Funktion können Sie Ihre Teilnehmer einmalig oder in einem wiederkehrenden Zeitraum zertifizieren. Nur Administratoren können Zertifizierungen für Teilnehmer definieren.

Als Administrator können Sie ein Zertifizierungsprogramm erstellen, das entweder intern gehostet oder von einem Drittanbieter durchgeführt wird. Im Falle einer internen Zertifizierung definieren Sie die Kurse, die ein Teilnehmer absolvieren muss, um ein Zertifikat zu erhalten. Veröffentlichen Sie das Programm und weisen Sie es den Teilnehmern zu.

## Zertifizierung erstellen {#createacertification}

1. Klicken **[!UICONTROL Zertifizierung]** im linken Bereich.\
   Eine Seite mit einer Liste aller Zertifizierungen im Status Entwurf und veröffentlicht wird angezeigt.

1. Zertifizierungen in verschiedenen Modi anzeigen:

   1. Klicken **[!UICONTROL Entwurf]** &quot; alle Zertifizierungen im Entwurfsstatus an. Sie müssen die Erstellung abschließen.
   1. Klicken **[!UICONTROL Veröffentlicht]** , um alle von Ihnen veröffentlichten Zertifizierungen anzuzeigen.
   1. Klicken **[!UICONTROL Alle]** , um die Zertifizierungen in allen Status anzuzeigen.
   1. Sortieren Sie die Liste der Zertifizierungen in aufsteigender oder absteigender Reihenfolge oder nach dem Datum ihrer Aktualisierung.

1. Klicken **[!UICONTROL Hinzufügen]**.

   Eine neue Zertifizierungsseite wird angezeigt.

![](assets/add-new-certification.png)

*Seite zum Hinzufügen einer Zertifizierung anzeigen*

1. Fügen Sie den Zertifikatnamen und die Beschreibung hinzu.

<table>
 <tbody>
  <tr>
   <th>Feld</th>
   <th>Beschreibung</th>
  </tr>
  <tr>
   <td>Tage bis zum Abschluss</td>
   <td>Termin für die Zertifizierung. Geben Sie einen numerischen Wert ein.</td>
  </tr>
  <tr>
   <td>Typ</td>
   <td>
    <p>Die Art der Zertifizierung:</p>
    <ul>
     <li><b>Wiederkehrend</b>- Wählen Sie diese Option, wenn die Zertifizierung nach jedem Jahr, nach zwei Jahren oder drei Jahren erfolgen soll.</li>
     <li><b>Unbefristet</b>- Wählen Sie diese Option, wenn die Zertifizierung nur einmal erforderlich sein soll.</li>
    </ul></td>
  </tr>
  <tr>
   <td>Neuzuweisung</td>
   <td>Wählen Sie aus, ob das Zertifikat basierend auf dem Abschlussdatum oder basierend auf dem Registrierungsdatum zugewiesen werden soll.<br></td>
  </tr>
  <tr>
   <td>Gültigkeit (in Monaten) <br></td>
   <td>Geben Sie an, wie lange die Zertifizierung gültig bleiben kann.</td>
  </tr>
  <tr>
   <td>Abfolge von Kursen<br></td>
   <td>Entscheiden Sie, ob Teilnehmer die Kurse in geordneter oder ungeordneter Weise absolvieren sollen.<br></td>
  </tr>
  <tr>
   <td>Registrierung aufheben<br></td>
   <td>Aktivieren oder deaktivieren Sie die Option, um Teilnehmern zu ermöglichen, sich selbst zu registrieren.</td>
  </tr>
  <tr>
   <td>Zertifizierungsaussteller<br></td>
   <td>
    <p>Auswählen <b>Intern</b> , wenn sie zu Ihrer Organisation gehört, oder wählen Sie <b>Extern</b> für Zertifizierungen externer Unternehmen.</p>
    <p>Wenn Sie <b>Externe Zertifizierung</b>, werden zwei weitere Optionen angezeigt:</p>
    <ul>
     <li>Wie Datum der Genehmigung<br></li>
     <li>Eingereicht von Teilnehmer<br></li>
    </ul>
    <p>Teilnehmer können das richtige Abschlussdatum für externe Zertifizierungen angeben. In früheren Versionen wurde das Abschlussdatum standardmäßig von Prime basierend auf dem Genehmigungsdatum des Managers festgelegt. Das vom Teilnehmer angegebene Abschlussdatum sollte größer sein als das Erstellungsdatum des Zertifikats.<span>.</span></p></td>
  </tr>
  <tr>
   <td>Dauer</td>
   <td>Wenn Sie "Externe Zertifizierung" ausgewählt haben, geben Sie die Dauer in Minuten an.</td>
  </tr>
  <tr>
   <td>Tags</td>
   <td>Geben Sie die Tags ein, die Sie dem Zertifikat zuordnen möchten. Tags sind hilfreich, wenn Sie nach dem Zertifikat suchen möchten.</td>
  </tr>
  <tr>
   <td>Kataloge auswählen<br></td>
   <td>Wählen Sie den Katalog aus, in dem das Zertifikat enthalten ist.</td>
  </tr>
 </tbody>
</table>

Wählen Sie die Kurse aus, die der Zertifizierung hinzugefügt werden sollen **[!UICONTROL Kurse]** > **[!UICONTROL Katalog]** &quot; ändern.

Bewegen Sie die Maus über jede Kurskachel und klicken Sie auf &quot;+&quot;, um sie zur Zertifizierung hinzuzufügen. Klicken **[!UICONTROL Vorschau]** , um den Kurs als Teilnehmer anzuzeigen, bevor Sie ihn hinzufügen.

1. Klicken **[!UICONTROL Lehrplan]** &quot; die Liste der Kurse an, die Sie hinzugefügt haben.
1. Klicken **[!UICONTROL Veröffentlichen]**.

## Kursinstanzzuordnung für Zertifizierungen {#courseinstancemappingforcertifications}

Kurs und Instanz für Zertifizierungen zuordnen:

1. Klicken Sie im linken Bereich auf Zertifizierungen .
1. Wählen Sie in der Liste der Zertifizierungen &quot;Zertifizierung der Zertifizierung anzeigen&quot; aus, für die Sie den Kurs und die Instanz zuordnen möchten.
1. Klicken Sie im linken Teilfenster auf &quot;Kurse&quot;. Die Kurse für die Zertifizierung werden angezeigt. Klicken Sie auf Bearbeiten.
1. Bewegen Sie den Mauszeiger über den Kurs, für den Sie die Instanzzuordnung festlegen möchten, und wählen Sie &quot;Kursinstanzzuordnung&quot;.
1. Wählen Sie im daraufhin angezeigten Popup-Fenster die Instanz des Kurses aus, der für die von Ihnen ausgewählte Zertifizierung bereitgestellt werden soll.
1. Klicken Sie auf Speichern.

Ein Administrator kann einem Lernprogramm Klassenzimmer und Kurse vom Typ &quot;Virtueller Klassenzimmer&quot; hinzufügen. Jede Sitzung, die der Autor während der Erstellung des Kurses festgelegt hat, wird zur Standardinstanz. Wenn der Administrator einem Lernprogramm Kurse hinzufügt, werden diese standardmäßig der Standardinstanz aller Kurse zugeordnet. Der Administrator kann die Instanzzuordnung jedoch ändern. Die Anzahl der einem Lernprogramm hinzugefügten Kurse wird auch auf der Instanzenseite angezeigt (siehe unten).

## Vollständige Katalogsteuerung aktivieren {#catalog}

Wie vollständige Gewährung [Katalogsteuerung für Lernergebnisse oder Module](shared-catalog-full-control.md)können Sie auch die vollständige Katalogsteuerung für Zertifizierungen aktivieren.

## Registrieren oder Aufheben der Registrierung von Teilnehmern für die Zertifizierung {#enrollorunenrolllearnerstothecertification}

Weitere Informationen zum Registrieren von Teilnehmern und zu den folgenden Schritten finden Sie unter [Registrieren von Teilnehmern](courses.md#main-pars_header_1058138132).

## Registrierung für Teilnehmer aufheben {#unenrollmentforlearners}

Beim Erstellen von Zertifizierungen kann der Administrator auswählen, ob Teilnehmer selbst die Registrierung für die Zertifizierung aufheben können. Wenn der Administrator die Option auswählt, können die Teilnehmer selbst die Registrierung aufheben.

![](assets/unenrollment.png)

*Auswählen, um die Registrierung von Teilnehmern aufzuheben*

## Als abgeschlossen markieren {#markcompletion}

Administratoren können eine Zertifizierung mithilfe der für sie verfügbaren Option als abgeschlossen markieren. Gehen Sie wie folgt vor, um den Abschluss einer Zertifizierung zu markieren.

1. Öffnen **[!UICONTROL Zertifizierung]** > **[!UICONTROL Teilnehmer]**.

   Die Seite &quot;Teilnehmer&quot; wird mit der Liste der registrierten Teilnehmer geöffnet.

1. Wählen Sie einen, mehrere oder alle Teilnehmer aus, um den Abschluss der Zertifizierung mithilfe des Kontrollkästchens zu markieren, das für jeden Teilnehmer verfügbar ist.
1. Klicken  **[!UICONTROL Aktion]** > **[!UICONTROL Als abgeschlossen markieren.]**

   Beachten Sie, dass bei einer Zertifizierung mit mehreren Kursen der Abschluss für alle Kurse markiert wird.

## Pflichtkurse für externe Zertifizierungen {#mandatory}

In früheren Versionen von Learning Manager war der Kursabschluss vom Teilnehmer in der externen Zertifizierung nicht zwingend erforderlich, um ein Zertifikat abzuschließen.

Sie können jetzt Kurse verbindlich festlegen, indem Sie die Option **[!UICONTROL Erforderliche Kurse als obligatorisch für den Abschluss des Zertifikats festlegen]** auf der Registerkarte &quot;Stundenplan&quot;, während Sie die Zertifizierungen bearbeiten.

## Bearbeiten einer veröffentlichten Zertifizierung {#editingapublishedcertification}

Eine Zertifizierung kann von einem Administrator in einem veröffentlichten Status bearbeitet werden. In diesem Status kann der Administrator alle Abschnitte einer Zertifizierung bearbeiten und erneut veröffentlichen.

Um eine veröffentlichte Zertifizierung zu bearbeiten, klicken Sie auf die Zertifizierungskarte und dann auf **[!UICONTROL Bearbeiten]** oben rechts auf der Seite.

Wenn Sie beim Bearbeiten der Abschnitte einer Zertifizierung die Seite verlassen müssen, müssen Sie die Zertifizierung erneut veröffentlichen. Sie erhalten eine Dialogfeldbestätigung, in der Sie aufgefordert werden, die Zertifizierung erneut zu veröffentlichen.

## Abonnement {#subscription}

Ein Administrator kann Quizpunktzahlen und Teilnehmerstatusberichte abrufen. Sie können die Berichtsfrequenz, den E-Mail-Betreff und die E-Mail-ID des Empfängers festlegen. Je nach festgelegter Häufigkeit erhält der Empfänger eine E-Mail mit dem angehängten Bericht.

![](assets/report-subscription.jpeg)

*Berichtshäufigkeit und andere Eigenschaften festlegen*

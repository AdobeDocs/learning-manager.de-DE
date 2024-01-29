---
description: Lesen Sie diesen Artikel, um zu erfahren, wie Sie Teilnehmerprofileinstellungen festlegen und ein Profilfoto hinzufügen. Erfahren Sie, wie Sie das Teilnehmertranskript für Ihr Profil herunterladen.
jcr-language: en_us
title: Profileinstellungen
contentowner: manochan
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '783'
ht-degree: 0%

---



# Profileinstellungen

Lesen Sie diesen Artikel, um zu erfahren, wie Sie Teilnehmerprofileinstellungen festlegen und ein Profilfoto hinzufügen. Erfahren Sie, wie Sie das Teilnehmertranskript für Ihr Profil herunterladen.

## Konfigurieren von Profileinstellungen {#configuringprofilesettings}

1. Klicken Sie in der rechten oberen Ecke der Seite auf den Dropdown-Pfeil neben Ihrem Profil oder Foto.
1. Wählen Sie Profileinstellungen.
1. Im angezeigten Popup-Dialogfeld können Sie die folgenden Aktionen ausführen:

   * Profilfoto hinzufügen/aktualisieren: Zeigen Sie mit der Maus auf das Foto. Klicken Sie auf Hochladen und fügen Sie ein Foto hinzu. Klicken Sie auf Bearbeiten , um das Foto zu ändern.
   * Foto löschen: Zeigen Sie mit der Maus auf das Profilfoto. Klicken Sie auf Löschen.
   * Fügen Sie Inhalt über mich hinzu, indem Sie auf den Textbereich darunter klicken.
   * Ändern Sie den Inhalt von &quot;Über mich&quot;, indem Sie neben dem Feld auf &quot;Bearbeiten&quot; klicken.
   * Legen Sie das Gebietsschema für Ihr Profil fest. Wählen Sie in der Dropdown-Liste Gebietsschema die gewünschte Sprache aus.
   * Legen Sie das aktuelle Gebietsschema für Ihr Profil fest.
   * Legen Sie die Zeitzone für Ihr Profil fest.
   * Laden Sie das Teilnehmertranskript mit Ihren Daten herunter.

   ![](assets/learner-preferences.png)
   *Anzeigen der Teilnehmervoreinstellungen*

   Wenn Sie auf den Link &quot;XLS-Transkript für mein Lernprotokoll herunterladen&quot; klicken, wird ein Excel-Arbeitsblatt auf Ihr System heruntergeladen. Dieses Excel-Arbeitsblatt enthält Details zu den von Ihnen belegten Lernobjekten, dem Abschlussstatus jedes Lernobjekts, den entsprechenden Fälligkeitsdaten, den erreichten Kenntnissen usw. Laden Sie dieses Blatt herunter, um schnell einige allgemeine Daten für Ihr Lernprofil abzurufen.

1. Wenn ein Administrator Auswahl-E-Mail aktiviert hat und Sie nicht in der DND-Liste aufgeführt sind, können Sie Auswahl-E-Mails abonnieren oder abbestellen. Aktivieren Sie die Option unten.

   ![](assets/digest-email-option-learner.png)
   *Auswahl-E-Mails abonnieren oder abbestellen*

   Je nach der vom Administrator festgelegten Häufigkeit erhält der Teilnehmer die E-Mail vierzehntägig oder monatlich.

## Auswahl-E-Mails abbestellen {#unsubscribefromdigestemails}

Wenn Sie eine E-Mail erhalten, können Sie die Auswahl-E-Mail abbestellen, indem Sie auf die Schaltfläche **Abonnement kündigen** am Ende der E-Mail.

Nachdem Sie auf **[!UICONTROL Abonnement kündigen]** klicken, werden Sie zu Ihrem **Profileinstellungen** , auf der Sie die Option zum Empfangen von E-Mails deaktivieren können.

## Anatomie einer Auswahl-E-Mail {#anatomyofadigestemail}

Eine Auswahl-E-Mail besteht aus den folgenden Abschnitten:

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Abschnitt</b></p></td>
   <td>
    <p><b>Beschreibung</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Persönliche Schulungszusammenfassung</p></td>
   <td>
    <p>In diesem Abschnitt werden die Schulungsmetriken eines Teilnehmers personalisiert, indem die Anzahl der für Schulungen aufgewendeten Minuten angegeben wird.</p>
    <p>Basierend auf der vom Teilnehmer verbrachten Zeit wird der Inhalt entsprechend den unten definierten Regeln angepasst:</p>
    <p>Wenn (benötigte_Zeit) &gt;= 60 Minuten, wird der folgende Text angezeigt:</p>
    <p><i>"Während der vergangenen zwei Wochen/des vergangenen Monats haben Sie <b>(benötigte_Zeit)</b> Minuten Schulung, um deine Kenntnisse zu erweitern. Im Folgenden finden Sie einige Empfehlungen, wie Sie mehr lernen können." </i></p>
    <p> Wenn (benötigte_Zeit) &lt; 60 Minuten, wird der folgende Text angezeigt:</p>
    <p><i>"Während der vergangenen zwei Wochen/des vergangenen Monats haben Sie <b>(benötigte_Zeit)</b> Minuten Schulung, um deine Kenntnisse zu erweitern. Im Folgenden finden Sie einige Empfehlungen, die Ihnen hoffentlich helfen, loszulegen und weiterzumachen."</i></p></td>
  </tr>
  <tr>
   <td>
    <p>Schulungsaktivität</p></td>
   <td>
    <p>In diesem Abschnitt wird die Zusammenfassung der Schulungsaktivitäten für dieses Konto auf Organisationsebene angezeigt.</p>
    <p>Die Zusammenfassung der Schulungsaktivitäten umfasst Folgendes: </p>
    <ul>
     <li>Anzahl der im Konto verfügbaren Schulungen.</li>
     <li>Anzahl der Mitlernenden, die aktiv an den Schulungsaktivitäten teilgenommen haben.</li>
     <li>Anzahl der von den Kollegen aufgewendeten Lernstunden.</li>
     <li>Durchschnittliche Zeit (in Minuten), die Kollegen für die Weiterbildung im Konto aufgewendet haben.</li>
    </ul></td>
  </tr>
  <tr>
   <td>
    <p>Empfohlene Kurse</p></td>
   <td>
    <p>Dies ist ein personalisierter Abschnitt, der die empfohlenen Schulungen für Teilnehmer enthält. In diesem Abschnitt können Teilnehmer drei Schulungen sehen, die von der Empfehlungs-Engine ausgewählt wurden.</p>
    <p>Jede Schulung verfügt über die Schaltfläche "Durchsuchen". Wenn sie angeklickt wird, wird sie zur Startseite der Teilnehmer-App weitergeleitet.  </p></td>
  </tr>
  <tr>
   <td>
    <p>Leaderboard</p></td>
   <td>
    <p>Zeigt ein Balkendiagramm an, in dem jeder Balken einen Teilnehmer darstellt, zusammen mit Gamification-Punkten für jeden Teilnehmer (nur, wenn der Administrator Gamification für alle Teilnehmer aktiviert hat).</p>
    <p>In der Leaderboard wird Folgendes angezeigt:</p>
    <ul>
     <li>Punkte, die ein Teilnehmer gesammelt hat.</li>
     <li>Die Punkte, die zum Erreichen der nächsten Stufe benötigt werden.</li>
    </ul>
    <p>Es gibt auch ein Mini-Leaderboard, in dem der Leader angezeigt wird, und zwei Teilnehmer, die dem Teilnehmer in diesem Benutzerbereich am nächsten sind.</p>
    <p>Wenn das Leaderboard leer ist, wird dieser Abschnitt nicht in der E-Mail angezeigt.</p></td>
  </tr>
  <tr>
   <td>
    <p><a>Social-Media-Beiträge</a></p></td>
   <td>
    <p>In diesem Abschnitt werden die drei letzten Social-Media-Beiträge angezeigt.</p>
    <p>Ein Teilnehmer kann das Erstellungsdatum, den Namen des Forums, gegebenenfalls den Titel des Beitrags, den Benutzernamen und das Symbol des Erstellers sehen. Der Beitrag kann auch ein Video, ein Dokument, eine PDF-Datei oder eine andere Datei enthalten.</p>
    <p>Jeder Beitrag enthält Links, über die der Teilnehmer zur Seite für soziales Lernen in der Teilnehmer-App weitergeleitet wird.</p>
    <p>Wenn keine aktuellen Beiträge vorliegen, ist dieser Abschnitt in der E-Mail für den Teilnehmer nicht sichtbar.</p></td>
  </tr>
 </tbody>
</table>

## Häufig gestellte Fragen {#frequentlyaskedquestions}

**1. Wie kann ich ein Teilnehmertranskript als Teilnehmer herunterladen?**

Klicken Sie oben rechts auf Ihre **[!UICONTROL Benutzerprofil]** > **[!UICONTROL Profileinstellungen]**. Klicken Sie im angezeigten Dialogfeld auf **Eigenes Lernprotokoll (XLS) herunterladen**.

![](assets/dowload-lt.png)
*Teilnehmertranskript herunterladen*

---
description: Erfahren Sie mehr über die Learning Manager-Kontoeinstellungen, die Sie als Administrator konfigurieren können.
jcr-language: en_us
title: Einstellungen
contentowner: manochan
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3791'
ht-degree: 0%

---



# Einstellungen

Erfahren Sie mehr über die Learning Manager-Kontoeinstellungen, die Sie als Administrator konfigurieren können.

Sie können Ihre Administratorprofileinstellungen ändern und Ihre Kontoeinstellungen aktualisieren. Anzeigen Ihrer Profilinformationen, Hinzufügen/Ändern von Profilfotos und Ändern von **[!UICONTROL Über mich]** Inhalt. Aktualisieren Sie Ihre Unternehmensinformationen, richten Sie Anmeldungsmethoden für Benutzer ein und richten Sie Connect-Integration über die Kontoeinstellungen ein.

## Kontoeinstellungen {#accountsettings}

Um die Kontoeinstellungen Ihrer Organisation zu aktualisieren, klicken Sie auf **[!UICONTROL Einstellungen]** im linken Bereich.

**Grundlegende Informationen (Unternehmensinformationen)**

Klicken **[!UICONTROL Ändern]** auf der Seite und bearbeiten Sie Land, Zeitzone, Gebietsschema und Geschäftsjahr.

**Administrator kontaktieren konfigurieren**

Wenn Sie die E-Mail-Adressen für den Support-Administrator für Ihr Unternehmen ändern oder hinzufügen möchten, können Sie diese konfigurieren, indem Sie auf **[!UICONTROL Allgemein]** im linken Bereich. Klicken **[!UICONTROL Ändern]** angrenzend an **[!UICONTROL Support-E-Mail-ID]** und die E-Mail-IDs hinzufügen. E-Mail wird an diese Administratoren gesendet, wenn Teilnehmer klickt **[!UICONTROL Administrator kontaktieren]** &quot; oben auf der Seite.

Fügen Sie zusätzliche E-Mails mit Semikolon als Trennzeichen hinzu.

**Anmeldemethoden** - Administratoren können den Modus auswählen, über den Ihre internen oder externen Benutzer auf das Konto zugreifen können.

* **Interne Benutzer:** Für interne Benutzer können Sie die Adobe ID oder die SSO als Anmeldemodus festlegen.
* **Externe Benutzer:** Für externe Benutzer können Sie die Adobe ID oder die SSO oder die Lernmanager-ID festlegen.

Wenn Sie die Lern-Manager-ID wählen, können sich externe Benutzer bei diesem Konto anmelden, nachdem sie ihren Lern-Manager-Benutzernamen und ihr Kennwort erstellt haben.

>[!NOTE]
>
>Wenn es mehrere externe Profilsätze gibt, können alle Profile einen beliebigen Login-Typ haben. Wenn der Anmeldetyp beispielsweise Adobe ID ist, müssen sich alle Profile nur mit Adobe ID anmelden. Jedes Profil kann nicht seinen eigenen Anmeldetyp haben.

Sie können über Adobe ID oder Single Sign-on auf die Learning Manager-Anwendung zugreifen. Die einmalige Anmeldung (SSO) ist ein Verfahren, mit dem ein Benutzer sich einmal authentifizieren kann und mehrmals auf mehrere Anwendungen zugreifen kann. Diese Konfiguration ist für das Unternehmen nicht obligatorisch. Wenn Ihre Organisation über einen SAML 2.0-basierten SSO-Anbieter verfügt, können Sie diesen zum Konfigurieren der Learning Manager-Anwendung verwenden. Die Konfiguration ist auf Organisationsebene und für die Learning Manager-Anwendung erforderlich. Wenn Sie SSO verwenden möchten, wenden Sie sich an den Adobe-Support, um Konfigurationsanweisungen zu erhalten.

**Feedback**

Klicken **[!UICONTROL Feedback]** auf der linken Seite, um den Fragebogen einzurichten, um Feedback von Teilnehmern zu erhalten, nachdem Sie einen Kurs absolviert haben. Siehe [Kursfunktionshilfe](courses.md) zum Erstellen von Feedback L1 und L3.

**Mehrere Versuche**

Auswählen **[!UICONTROL Einstellungen]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Mehrere Versuche]**.

Wenn Sie das Kontrollkästchen &quot;Mehrere Versuche&quot; aktivieren, können die Autoren &quot;Mehrere Versuche&quot; für interaktive E-Learning-Kurse oder -Module festlegen. Wenn Sie das zweite Kontrollkästchen auswählen, können Administratoren &quot;Unendliche Versuche&quot; standardmäßig für alle neu erstellten interaktiven E-Learning-Kurse festlegen.

![](assets/admin-config.png)

*Aktivieren Sie das Kontrollkästchen &quot;Mehrere Versuche&quot;*

**Kursmoderation**

Klicken **[!UICONTROL Allgemein]** im linken Teilfenster und wählen Sie die Option &quot;Kursmoderation&quot;, um die Funktion &quot;Kursmoderation&quot; zu aktivieren. Weitere Informationen zu dieser Funktion finden Sie unter [Kursmoderation](courses.md#main-pars_header_1879001177).

**Diskussionsforum**

Wenn Sie das Kontrollkästchen &quot;Diskussions-Dashboard&quot; aktivieren, können Teilnehmer und Kursleiter in der Teilnehmer-App auf der Seite &quot;Kurse&quot; auf der Registerkarte &quot;Diskussionen&quot; Kommentare zu Kursen veröffentlichen. Wenn diese Funktion jedoch auf Kursebene nicht aktiviert ist, haben die Einstellungen auf Kursebene Vorrang vor Administratoreinstellungen.

**Teilnehmer-Dashboard**

Klicken Sie im linken Teilfenster auf Teilnehmer-Dashboard. Auf dieser Seite können Sie Widgets auswählen, die auf der Teilnehmerseite angezeigt werden sollen. Wählen Sie die Widgets, die Sie auf der Teilnehmerseite aktivieren möchten. Die nicht ausgewählten Widgets werden nicht auf der Teilnehmerseite angezeigt.

**Adobe Connect**

Klicken **[!UICONTROL Adobe Connect]** im linken Bereich, um das Adobe Connect-Konto zum Hosten von virtuellen Klassenzimmersitzungen zu konfigurieren. Weitere Informationen finden Sie unter  [Adobe Connect](adobeconnect-integration.md) Feature-Hilfe.

## Allgemeine Einstellungen {#general}

Aktivieren oder deaktivieren Sie die folgenden Einstellungen:

<table>
 <tbody>
  <tr>
   <th>
    <p><b>Name</b></p>
    </th>
   <th>
    <p><b>Beschreibung</b></p>
   </th>
  </tr>
  <tr>
   <td>Kurseffektivität anzeigen</td>
   <td>Wenn diese Option aktiviert ist, können Teilnehmer die aktuelle Kurseffektivität auf der Kurskachel sehen. Diese Funktion ist nur für Kurse verfügbar. Die Sternebewertung wird für Lernprogramme oder Zertifikate nicht unterstützt. Es ist für Kurse und Lernprogramme verfügbar, aber nicht für Zertifizierungen.</td>
  </tr>
  <tr>
   <td>Kursmoderation</td>
   <td>Wenn diese Option aktiviert ist, müssen alle Änderungen an Kursen vom Administrator genehmigt werden, bevor die Kurse für die Teilnehmer sichtbar sind.</td>
  </tr>
  <tr>
   <td>Diskussionsforum</td>
   <td>Wenn Sie das Kontrollkästchen "Diskussions-Dashboard" aktivieren, können Teilnehmer und Kursleiter in der Teilnehmer-App auf der Seite "Kurse" auf der Registerkarte "Diskussionen" Kommentare zu Kursen veröffentlichen. Wenn diese Funktion jedoch auf Kursebene nicht aktiviert ist, haben die Einstellungen auf Kursebene Vorrang vor Administratoreinstellungen.</td>
  </tr>
  <tr>
   <td>Mehrere Versuche</td>
   <td>Wenn diese Option aktiviert ist, kann der Autor mehrere Versuche für Kursmodule konfigurieren.</td>
  </tr>
  <tr>
   <td>Neue Kenntnisse entdecken</td>
   <td>Wenn diese Option aktiviert ist, können die Teilnehmer Peer- und Führungskenntnisse entdecken und die Kenntnisse ihrer Wahl abonnieren.</td>
  </tr>
  <tr>
   <td>Sichtbarkeit für Kenntnisse/Tags</td>
   <td>Zeigen Sie Teilnehmern alle Kenntnisse und Tags an. Sie können entweder alle Kenntnisse und Tags anzeigen oder Kenntnisse und Tags, die zugewiesen sind, oder die Teil der Kataloge sind, die für den Teilnehmer sichtbar sind.</td>
  </tr>
  <tr>
   <td>Eindeutige Lernobjekt-IDs</td>
   <td>Wenn diese Option aktiviert ist, kann ein Administrator oder ein Autor eine eindeutige ID für jedes Lernobjekt hinzufügen.</td>
  </tr>
  <tr>
   <td>Filterfelder anzeigen</td>
   <td>
    <p><a id="filter-panels"></a>Legen Sie fest, welche Filterfelder Benutzern in der Teilnehmer-Anwendung zur Verbesserung ihrer Suchergebnisse zur Verfügung stehen Folgende Optionen stehen zur Verfügung:</p>
    <ul>
     <li>Kataloge</li>
     <li>Typ</li>
     <li>Format</li>
     <li>Dauer</li>
     <li>Kenntnisse</li>
     <li>Qualifikationsstufen</li>
     <li>Tags</li>
    </ul>
    <p>Wenn der Teilnehmer die Teilnehmer-App in den Abschnitten "Meine Lernprogramme" und "Katalog" startet, kann der Teilnehmer die Filter in den entsprechenden Fenstern sehen.</p>
    <p><b>Hinweis: </b>Die Filter <b>Format </b>und <b>Dauer </b>sind standardmäßig deaktiviert und werden den Teilnehmern nicht unmittelbar nach der Veröffentlichung angezeigt. Der Administrator sollte sie aktivieren. <br></p></td>
  </tr>
  <tr>
   <td>Katalogliste anzeigen</td>
   <td>Wenn diese Option aktiviert ist, können die Teilnehmer eine Liste aller für sie verfügbaren Kataloge anzeigen. Teilnehmer können dies verwenden, um die Anzeige der Lernobjekte zu verfeinern.</td>
  </tr>
  <tr>
   <td>Produktterminologie</td>
   <td>Learning Manager verfügt über eine Standardterminologie, die im gesamten Produkt verwendet wird. Passen Sie die Terminologie an die Anforderungen Ihres Unternehmens an.</td>
  </tr>
  <tr>
   <td>Modulversionsupdate</td>
   <td>Konfigurieren Sie die Standardeinstellung zum Aktualisieren von Inhalten. Die Einstellungen können für jeden Inhalt auf der Kursseite geändert werden.</td>
  </tr>
  <tr>
   <td>Benutzer automatisch registrieren</td>
   <td>Wenn diese Option aktiviert ist, werden neu importierte Benutzer automatisch registriert. Standardmäßig müssen Benutzer manuell registriert werden, bevor sie den Lern-Manager verwenden können.</td>
  </tr>
  <tr>
   <td><a id="autodelete"></a>Interne Benutzer automatisch löschen</td>
   <td>Wenn diese Option aktiviert ist, werden interne Benutzer automatisch gelöscht, wenn sie für eine bestimmte Anzahl von Tagen nicht auf das System zugreifen. Diese Funktion gilt für Benutzer, die nur die Rolle haben. <b>Teilnehmer</b>. Um den Zugriff wiederherzustellen, müssen Benutzer sich an den Administrator wenden.<br></td>
  </tr>
  <tr>
   <td>Katalogbeschriftungen anzeigen</td>
   <td>Wenn diese Option aktiviert ist, können Administratoren und Autoren Katalogbeschriftungen und Werte festlegen und sie mit Lernobjekten verknüpfen.</td>
  </tr>
  <tr>
   <td>Teilnehmer können ihre Punktzahl anzeigen</td>
   <td>Wenn diese Option aktiviert ist, können die Teilnehmer ihre Punktzahl im Teilnehmertranskript anzeigen.</td>
  </tr>
  <tr>
   <td>Auswahl-E-Mail</td>
   <td>
    <p>Ein Administrator kann das Senden einer E-Mail an Teilnehmer aktivieren oder deaktivieren. Der Administrator kann auch die Häufigkeit der gesendeten E-Mails steuern.</p>
    <ul>
     <li>Für <b>Kontokorrentkonto</b>, Auswahl-E-Mails sind standardmäßig deaktiviert, sodass sie vom Administrator manuell aktiviert werden können.</li>
     <li>Für <b>Testkonten</b>, die Option für Auswahl-E-Mails bleibt deaktiviert und der Administrator kann die Option nicht aktivieren.</li>
    </ul>
    <p>Wenn die Funktion deaktiviert ist, gilt:</p>
    <ul>
     <li>Die Option <b>Auswahl-E-Mail</b> wird deaktiviert.</li>
     <li>Ein Teilnehmer kann die Benutzereinstellung für das Auswahl-E-Mail-Abonnement nicht sehen.</li>
    </ul>
    <p> Wenn die Funktion aktiviert ist, gilt:</p>
    <ul>
     <li>Der Administrator kann die Option "Auswahl-E-Mail" aktivieren und ändern.</li>
     <li>Im Fenster " <b>Profileinstellungen </b>in der Teilnehmer-App kann ein Teilnehmer (nicht in der DND-Liste) die Auswahl-E-Mail abonnieren/abbestellen.</li>
    </ul></td>
  </tr>
  <tr>
   <td>Symbole der Schulungskarte aktivieren<br></td>
   <td>Sofern aktiviert, werden Symbole auf Schulungskarten in der Teilnehmer-App angezeigt.<br></td>
  </tr>
  <tr>
   <td>Links für Fußzeile</td>
   <td>
    <p>Fügen Sie Links oder E-Mail-IDs hinzu, die als Fußzeilen angezeigt werden. Sie können maximal drei Fußzeilenlinks hinzufügen.</p>
    <p>Um die Links in der Fußzeile anzupassen, führen Sie die folgenden Schritte aus:</p>
    <ol>
     <li>Klicken <b>Mehr hinzufügen</b>den Namen und die URL oder E-Mail-ID in die angegebenen Felder ein. Stellen Sie der URL http:// oder https:// voran.</li>
     <li>Um die Änderung in alle Ländereinstellungen zu übertragen, klicken Sie auf <b>Replizieren</b>. Dadurch wird sichergestellt, dass alle Sprachen den Namen und die URL erhalten.</li>
     <li>Klicken Sie zum Speichern der Änderungen auf <b>Speichern</b>. Sie können eine Popup-Nachricht sehen, die die Änderung bestätigt. Nachdem Sie auf "OK" geklickt haben, wird die Fußzeile mit den neu hinzugefügten Links ausgefüllt.</li>
    </ol>
    <p>Darüber hinaus haben Sie folgende Möglichkeiten:</p>
    <ul>
     <li>Klicken Sie auf <b>Zurücksetzen</b> , um die Standardwerte im Dialogfeld " <b>Hilfe</b> und <b>Administrator kontaktieren</b> Felder.</li>
     <li>Passen Sie den Link in der Fußzeile für alle Sprachen an. Klicken Sie auf <b>Sprache</b> " die Sprache aus und fügen Sie das Dialogfeld " <b>Name</b> und <b>URL</b> in die angegebenen Felder ein. Nachdem Sie die Änderungen gespeichert haben, werden die aktualisierten Links in der Fußzeile angezeigt.<br></li>
    </ul></td>
  </tr>
  <tr>
   <td>Berichtszeitzone<br></td>
   <td>
    <p>Legen Sie eine Voreinstellung auf Kontoebene fest, um das Lerntranskript in die folgenden Zeitzonen zu exportieren:</p>
    <ul>
     <li>UTC (Standardverhalten)</li>
     <li>Zeitzonenvoreinstellung auf Kontoebene</li>
    </ul>
    <p>Das mit der Jobs-API heruntergeladene Teilnehmertranskript lädt die Daten auch in die ausgewählte Zeitzone herunter.</p>
    <p><b>Hinweis: </b>Es wird unmittelbar nach der Veröffentlichung standardmäßig keine Änderung im Teilnehmertranskript erwartet. Administratoren können diese Einstellung über "Administrator &gt; Einstellungen &gt; Allgemein &gt; Berichtszeitzone" konfigurieren.</p></td>
  </tr>
 </tbody>
</table>

<table border="0" cellpadding="0" cellspacing="0" width="1709">
 <tbody>
  <tr>
   <td height="20" width="147">Name</td>
   <td>Beschreibung</td>
  </tr>
  <tr>
   <td height="20">Kurseffektivität anzeigen</td>
   <td>Wenn diese Option aktiviert ist, können Teilnehmer die aktuelle Kurseffektivität auf der Kurskachel sehen.</td>
  </tr>
  <tr>
   <td height="20">Kursmoderation</td>
   <td>Wenn diese Option aktiviert ist, müssen alle Änderungen an Kursen vom Administrator genehmigt werden, bevor die Kurse für die Teilnehmer sichtbar sind.</td>
  </tr>
  <tr>
   <td height="20">Diskussionsforum</td>
   <td>Wenn Sie das Kontrollkästchen "Diskussions-Dashboard" aktivieren, können Teilnehmer und Kursleiter in der Teilnehmer-App auf der Seite "Kurse" auf der Registerkarte "Diskussionen" Kommentare zu Kursen veröffentlichen. Wenn diese Funktion jedoch auf Kursebene nicht aktiviert ist, haben die Einstellungen auf Kursebene Vorrang vor Administratoreinstellungen.</td>
  </tr>
  <tr>
   <td height="20">Mehrere Versuche</td>
   <td>Wenn diese Option aktiviert ist, kann der Autor mehrere Versuche für Kursmodule konfigurieren.</td>
  </tr>
  <tr>
   <td height="20">Neue Kenntnisse entdecken</td>
   <td>Wenn diese Option aktiviert ist, können die Teilnehmer Peer- und Führungskenntnisse entdecken und die Kenntnisse ihrer Wahl abonnieren.</td>
  </tr>
  <tr>
   <td height="20">Sichtbarkeit für Kenntnisse/Tags</td>
   <td>Zeigen Sie Teilnehmern alle Kenntnisse und Tags an. Sie können entweder alle Kenntnisse und Tags anzeigen oder Kenntnisse und Tags, die zugewiesen sind, oder die Teil der Kataloge sind, die für den Teilnehmer sichtbar sind.</td>
  </tr>
  <tr>
   <td height="20">Eindeutige Lernobjekt-IDs</td>
   <td>Wenn diese Option aktiviert ist, kann ein Administrator oder ein Autor eine eindeutige ID für jedes Lernobjekt hinzufügen.</td>
  </tr>
  <tr>
   <td rowspan="10" height="191">Filterfelder anzeigen</td>
   <td>Legen Sie fest, welche Filterfelder Benutzern in der Teilnehmer-Anwendung zur Verbesserung ihrer Suchergebnisse zur Verfügung stehen Folgende Optionen stehen zur Verfügung:</td>
  </tr>
  <tr>
   <td height="19">Kataloge</td>
  </tr>
  <tr>
   <td height="19">Typ</td>
  </tr>
  <tr>
   <td height="19">Format</td>
  </tr>
  <tr>
   <td height="19">Dauer</td>
  </tr>
  <tr>
   <td height="19">Kenntnisse</td>
  </tr>
  <tr>
   <td height="19">Qualifikationsstufen</td>
  </tr>
  <tr>
   <td height="19">Tags</td>
  </tr>
  <tr>
   <td height="19">Wenn der Teilnehmer die Teilnehmer-App in den Abschnitten "Meine Lernprogramme" und "Katalog" startet, kann der Teilnehmer die Filter in den entsprechenden Fenstern sehen.</td>
  </tr>
  <tr>
   <td height="20">Hinweis: Die Filter Format und Dauer werden standardmäßig deaktiviert und den Teilnehmern nicht unmittelbar nach der Veröffentlichung angezeigt. Der Administrator sollte sie aktivieren. </td>
  </tr>
  <tr>
   <td height="20">Katalogliste anzeigen</td>
   <td>Wenn diese Option aktiviert ist, können die Teilnehmer eine Liste aller für sie verfügbaren Kataloge anzeigen. Teilnehmer können dies verwenden, um die Anzeige der Lernobjekte zu verfeinern.</td>
  </tr>
  <tr>
   <td height="20">Produktterminologie</td>
   <td>Learning Manager verfügt über eine Standardterminologie, die im gesamten Produkt verwendet wird. Passen Sie die Terminologie an die Anforderungen Ihres Unternehmens an.</td>
  </tr>
  <tr>
   <td height="20">Modulversionsupdate</td>
   <td>Konfigurieren Sie die Standardeinstellung zum Aktualisieren von Inhalten. Die Einstellungen können für jeden Inhalt auf der Kursseite geändert werden.</td>
  </tr>
  <tr>
   <td height="20">Benutzer automatisch registrieren</td>
   <td>Wenn diese Option aktiviert ist, werden neu importierte Benutzer automatisch registriert. Standardmäßig müssen Benutzer manuell registriert werden, bevor sie den Lern-Manager verwenden können.</td>
  </tr>
  <tr>
   <td height="20">Interne Benutzer automatisch löschen</td>
   <td>Wenn diese Option aktiviert ist, werden interne Benutzer automatisch gelöscht, wenn sie für eine bestimmte Anzahl von Tagen nicht auf das System zugreifen. Diese Funktion gilt für Benutzer, die nur die Rolle Teilnehmer haben. Um den Zugriff wiederherzustellen, müssen Benutzer sich an den Administrator wenden.</td>
  </tr>
  <tr>
   <td height="20">Katalogbeschriftungen anzeigen</td>
   <td>Wenn diese Option aktiviert ist, können Administratoren und Autoren Katalogbeschriftungen und Werte festlegen und sie mit Lernobjekten verknüpfen.</td>
  </tr>
  <tr>
   <td height="20">Teilnehmer können ihre Punktzahl anzeigen</td>
   <td>Wenn diese Option aktiviert ist, können die Teilnehmer ihre Punktzahl im Teilnehmertranskript anzeigen.</td>
  </tr>
  <tr>
   <td rowspan="9" height="172">Auswahl-E-Mail</td>
   <td>Ein Administrator kann das Senden einer E-Mail an Teilnehmer aktivieren oder deaktivieren. Der Administrator kann auch die Häufigkeit der gesendeten E-Mails steuern.</td>
  </tr>
  <tr>
   <td height="19">Bei aktiven Konten sind Auswahl-E-Mails standardmäßig deaktiviert, sodass sie vom Administrator manuell aktiviert werden können.</td>
  </tr>
  <tr>
   <td height="19">Bei Testkonten bleibt die Option für Auswahl-E-Mails deaktiviert und der Administrator kann die Option nicht aktivieren.</td>
  </tr>
  <tr>
   <td height="19">Wenn die Funktion deaktiviert ist, gilt:</td>
  </tr>
  <tr>
   <td height="19">Die Option Auswahl-E-Mail wird deaktiviert.</td>
  </tr>
  <tr>
   <td height="19">Ein Teilnehmer kann die Benutzereinstellung für das Auswahl-E-Mail-Abonnement nicht sehen.</td>
  </tr>
  <tr>
   <td height="19"> Wenn die Funktion aktiviert ist, gilt:</td>
  </tr>
  <tr>
   <td height="19">Der Administrator kann die Option "Auswahl-E-Mail" aktivieren und ändern.</td>
  </tr>
  <tr>
   <td height="20">Über die Profileinstellungen in der Teilnehmer-App kann ein Teilnehmer (nicht in der DND-Liste) die Auswahl-E-Mail abonnieren/abbestellen.</td>
  </tr>
  <tr>
   <td height="20">Symbole der Schulungskarte aktivieren</td>
   <td>Sofern aktiviert, werden Symbole auf Schulungskarten in der Teilnehmer-App angezeigt.</td>
  </tr>
  <tr>
   <td rowspan="8" height="153">Links für Fußzeile</td>
   <td>Fügen Sie Links oder E-Mail-IDs hinzu, die als Fußzeilen angezeigt werden. Sie können maximal drei Fußzeilenlinks hinzufügen.</td>
  </tr>
  <tr>
   <td height="19">Um die Links in der Fußzeile anzupassen, führen Sie die folgenden Schritte aus:</td>
  </tr>
  <tr>
   <td height="19">1. Klicken Sie auf Mehr hinzufügen, geben Sie den Namen und die URL oder E-Mail-ID in die angegebenen Felder ein. Stellen Sie der URL http:// oder https:// voran.</td>
  </tr>
  <tr>
   <td height="19">2. Klicken Sie auf "Replizieren", um die Änderung in alle Ländereinstellungen zu übertragen. Dadurch wird sichergestellt, dass alle Sprachen den Namen und die URL erhalten.</td>
  </tr>
  <tr>
   <td height="19">3. Um die Änderungen zu speichern, klicken Sie auf "Speichern". Sie können eine Popup-Nachricht sehen, die die Änderung bestätigt. Nachdem Sie auf "OK" geklickt haben, wird die Fußzeile mit den neu hinzugefügten Links ausgefüllt.</td>
  </tr>
  <tr>
   <td height="19">Darüber hinaus haben Sie folgende Möglichkeiten:</td>
  </tr>
  <tr>
   <td height="19">Klicken Sie auf das Symbol Zurücksetzen , um die Standardwerte in den Feldern Hilfe und Administrator kontaktieren zurückzusetzen.</td>
  </tr>
  <tr>
   <td height="20">Passen Sie den Link in der Fußzeile für alle Sprachen an. Klicken Sie auf die Dropdown-Liste Sprache , wählen Sie die Sprache aus und fügen Sie den Namen und die URL in die angegebenen Felder ein. Nachdem Sie die Änderungen gespeichert haben, werden die aktualisierten Links in der Fußzeile angezeigt.</td>
  </tr>
  <tr>
   <td rowspan="5" height="96">Berichtszeitzone</td>
   <td> Legen Sie eine Voreinstellung auf Kontoebene fest, um das Lerntranskript in die folgenden Zeitzonen zu exportieren:</td>
  </tr>
  <tr>
   <td height="19">UTC (Standardverhalten)</td>
  </tr>
  <tr>
   <td height="19">Zeitzonenvoreinstellung auf Kontoebene</td>
  </tr>
  <tr>
   <td height="19">Das mit der Jobs-API heruntergeladene Teilnehmertranskript lädt die Daten auch in die ausgewählte Zeitzone herunter.</td>
  </tr>
  <tr>
   <td height="20">Hinweis: Es wird unmittelbar nach der Veröffentlichung standardmäßig keine Änderung im Teilnehmertranskript erwartet. Administratoren können diese Einstellung über "Administrator &gt; Einstellungen &gt; Allgemein &gt; Berichtszeitzone" konfigurieren.</td>
  </tr>
  <tr>
   <td height="19">Badgr-Integration</td>
   <td>Wenn diese Option aktiviert ist, können die Teilnehmer ihre Abzeichen auf die Badgr-Website hochladen. In Kundenschulungsszenarien möchten Unternehmen ihre Kunden "zertifizieren" und ihnen die Möglichkeit geben, diese Anmeldedaten über soziale Medien anzuzeigen. Dies motiviert den Teilnehmer, eine Schulung zu absolvieren und seine Leistungen mit anderen zu teilen. </td>
  </tr>
  <tr>
   <td height="135">
    <p>Bewertung anzeigen</p></td>
   <td>
    <ul>
     <li>Wenn die Option <b>Kurseffektivität</b> aktiviert ist, können die Teilnehmer nur den Wert der Kurseffektivität sehen.</li>
     <li>Wenn die Option <b>Sternebewertung</b> aktiviert ist, können Teilnehmer nur die durchschnittliche Sternebewertung sehen sowie die Anzahl der Teilnehmer, die den Kurs bewertet haben.<br></li>
    </ul>
    <p>Diese Funktion ist nur für Kurse verfügbar. Die Sternebewertung wird für Lernprogramme oder Zertifikate nicht unterstützt.<br><br><b>Hinweis: </b>Diese Änderung betrifft nur die Teilnehmer-App. </p>
    <p>In allen anderen Apps (Admin, Autor, Manager, benutzerdefinierter Administrator, benutzerdefinierter Autor) haben Änderungen an den Einstellungen (Sternebewertung/Kurseffektivität/Deaktivierung der Bewertungsanzeige) keine Auswirkungen. </p>
    <p>Bei neuen Konten wird der " <b>Bewertungen anzeigen</b> Abschnitt hat die Möglichkeit, <b>Sternebewertung</b> standardmäßig aktiviert ist.</p>
    <p>Wenn das Konto zuvor die Option <b>Kurseffektivität</b> aktiviert ist, wird die Schaltfläche <b>Bewertungen anzeigen</b> wird mit der Option Kurseffektivität aktiviert. Wenn die Option <b>Kurseffektivität</b>s deaktiviert ist, wird das Dialogfeld <b>Bewertungen anzeigen</b> wird ebenfalls deaktiviert. Wenn die Option <b>Bewertungen anzeigen</b> aktiviert ist, wird die Option <b>Sternebewertung</b> ist standardmäßig aktiviert.</p></td>
  </tr>
 </tbody>
</table>

<table>
 <tbody>
  <tr>
   <td>
    <p>Lernpfade</p></td>
   <td>
    <p>Wenn die Option <b>Erweiterte Funktionen des Lernplans aktivieren</b> aktiviert ist, können Administratoren Lernpläne in Lernpläne aufnehmen und diese Lernpläne mit Kursen kombinieren. Diese Option ist unumkehrbar.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Kursleiter-Management<br></p></td>
   <td>
    <p>Aktivieren Sie diese Einstellung, um die Liste der Kursleiter einzuschränken, die beim Erstellen von Klassenzimmer-/virtuellen Klassenzimmersitzungen ausgewählt werden können. Alle Benutzer, für die der Kursleiter Berechtigungen hat, können nur als Kursleiter einer Sitzung zugewiesen werden. Diese Einschränkung gilt nicht für Migrationsarbeitsabläufe.<br></p></td>
  </tr>
 </tbody>
</table>

## AI-basierte Empfehlung

Der Lern-Manager enthält eine brandneue Teilnehmer-Startseite, die modern, inhaltsorientierter und den Wünschen des Teilnehmers entsprechend personalisiert ist. AI-basierte Lernempfehlungen zielen darauf ab, das Engagement der Teilnehmer zu verbessern, Lernlücken zu erkennen und sie zu beheben.

Der Empfehlungsalgorithmus ist darauf ausgelegt, mehrere Eingabequellen zu verwenden, einschließlich Branchendaten zu Arbeitsrollen, Titeln und Beschreibungen, die Adobe von seinen Partnern bezogen hat. Diese Daten werden dann verwendet, um die AI-Algorithmen der Adobe zu trainieren, sodass der Learning Manager eine Karte erstellen kann, die branchenorientierte Kenntnisse mit Tätigkeitsbezeichnungen und/oder -bezeichnungen verbindet. Dies wird dann zu einer einzigen Eingabe in den Empfehlungsalgorithmus.

Learning Manager analysiert dann mithilfe von Themenmodellierungsalgorithmen die Schulungsinhalte innerhalb eines Kontos und ordnet sie den Kenntnissen zu.

Learning Manager verwendet Peer-Aktivitätsdaten als ein weiteres Signal, um den Empfehlungsalgorithmus personalisiert zu steuern. Hier werden Aktivitäten wie Registrierung, Abschluss und explizites Feedback der Teilnehmer verwendet.

Darüber hinaus verwendet der Lern-Manager explizite und implizite Informationen, die von einzelnen Teilnehmern gesammelt wurden, um Empfehlungen weiter zu personalisieren. Ein Teilnehmer kann seine Interessensbereiche explizit über Registrierungen angeben, und der Lern-Manager erhält diese Informationen implizit basierend darauf, wie der Teilnehmer am Ende die Schulungen absolviert.

Schließlich kann der Administrator auch den Empfehlungsalgorithmus mithilfe von Teilnehmerattributen beeinflussen, die Learning Manager beim Definieren von Peer-Gruppen berücksichtigen sollte, und indem er Schulungen für bestimmte Benutzergruppen hervorhebt.

## Umbenennen von Lernobjekten {#renaminglearningobjects}

Diese Funktion ist nur in englischer Sprache verfügbar.

Administratoren können jetzt Lernobjekte im Lern-Manager umbenennen. Die folgenden Begriffe können umbenannt werden.

Modul\
Kurs\
Lernprogramm\
Zertifizierung\
Lernplan\
Arbeitshilfe\
Katalog\
Kenntnisse\
Ausweis\
Ankündigung\
Eigenes Lernen\
Leaderboard\
Effektivität\
Voraussetzung\
Vorarbeit\
Kerninhalt\
Testout\
Selbststudium\
Überblendet\
Klassenzimmer\
Virtuelles Klassenzimmer\
Aktivität

Führen Sie die folgenden Schritte aus, um die Begriffe umzubenennen.

1. Klicken Sie als Administrator auf **[!UICONTROL Einstellungen]** > **[!UICONTROL Allgemein]** > **[!UICONTROL Produktterminologie]**. Die Option &quot;Produktterminologie&quot; wird geöffnet.

   ![](assets/product-terminology.png)

   *Produktterminologie umbenennen*

1. Änderungen können durch Hochladen einer modifizierten Produktterminologievorlage und Herunterladen der Beispiel-CSV-Datei vorgenommen werden. Um die Beispiel-CSV-Datei herunterzuladen, klicken Sie auf das Symbol **[!UICONTROL Hier herunterladen]** aus.
1. Die heruntergeladene CSV-Datei enthält den Namen der Objekte in Spalte A. Wählen Sie in Spalte B den Namen aus, den Sie dem jeweiligen Objekt zuweisen möchten. Beachten Sie, dass Sie die Singular- und Pluralform des Namens, getrennt durch ein (|), aktualisieren müssen.
1. Sie können eine oder mehrere Zeilen ändern. Sie können entweder die nicht geänderten Zeilen beibehalten oder sie vor dem Hochladen aus der CSV-Datei entfernen.
1. Laden Sie die geänderte CSV-Datei hoch und klicken Sie auf **[!UICONTROL Speichern]**. Der Learning Manager wird entsprechend Ihren Änderungen aktualisiert.
1. Um auf die Standardbegriffe zurückzusetzen, klicken Sie auf **[!UICONTROL Produktterminologie zurücksetzen]**.

   ![](assets/with-reset-option.png)

   *Produktterminologien zurücksetzen*

## Profileinstellungen {#profilesettings}

1. Klicken Sie in der rechten oberen Ecke neben Ihrem Foto/Konto auf die Dropdownliste und wählen Sie **[!UICONTROL Profileinstellungen]**.
1. Im Popup-Dialogfeld können Sie ein Foto hinzufügen/ändern, indem Sie mit der Maus darauf zeigen und auf **[!UICONTROL Bearbeiten]** im Bereich &quot;Profilfoto&quot;.
1. Hinzufügen/Ändern **[!UICONTROL Über]** Inhalt durch Klicken auf **[!UICONTROL Bearbeiten]** direkt daneben.
1. Klicken **[!UICONTROL Speichern].**

## Inhaltsordner {#content-folder}

Learning Manager unterstützt Ordner für private Inhalte. Ein Administrator kann Ordner für private Inhalte konfigurieren und über benutzerdefinierte Rollen bestimmten benutzerdefinierten Autoren Zugriff darauf gewähren. Beachten Sie, dass Standardautoren (auch als Vollautoren bezeichnet) weiterhin Zugriff auf alle Inhalte im Konto haben. Somit haben Vollautoren Zugriff auf alle Ordner und alle Inhalte.

Inhaltsordner können von Administratoren konfiguriert werden. Erst nach der Konfiguration werden Inhaltsordner für Autoren sichtbar und sie erhalten die Möglichkeit, den Inhalt in einem oder mehreren Ordnern zu platzieren.

Um einen Inhaltsordner hinzuzufügen, klicken Sie in der Administrator-App auf **[!UICONTROL Einstellungen]** > **[!UICONTROL Inhaltsordner]**.

![](assets/manage-content-folders.png)

*Inhaltsordnereinstellungen ändern*

### Ordner

Ein Ordner ist ein Repository mit Inhalten, das eine Teilmenge der gesamten Inhaltsbibliothek ist, die in einem Konto mit den folgenden Eigenschaften verfügbar ist:

* Nur ein Administrator kann einen Ordner erstellen, bearbeiten oder löschen.
* Ein Administrator kann den Zugriff auf Ordner steuern, indem er Rollen nur für benutzerdefinierte Administratoren definiert.
* Inhalt **muss jederzeit mit mindestens einem Ordner verknüpft sein**. Zunächst werden alle Inhalte mit dem öffentlichen Ordner verknüpft, was später geändert werden kann.
* Der Inhalt kann zum Zeitpunkt der Erstellung mit mehreren Ordnern verknüpft werden, was auch durch einen Kopiervorgang möglich ist
* Alle Ordnernamen müssen innerhalb des Kontos eindeutig sein, andernfalls tritt ein Fehler beim Benennen eines Ordners auf.

Ordner steuern nur die Sichtbarkeit von Inhalten und erstellen keine Kopien von Inhalten. Daher wird die Bearbeitung des Inhalts in allen zugehörigen Ordnern widergespiegelt.

### Öffentlicher Ordner

Ein öffentlicher Ordner ist immer in einem Konto vorhanden, und zunächst wird der gesamte Inhalt Teil dieses Ordners sein. Später können Autoren Inhalte aus diesem Ordner in andere Ordner verschieben. Ein öffentlicher Ordner verfügt über die folgenden Eigenschaften:

* Alle Inhalte, die mit diesem Ordner verknüpft sind, sind standardmäßig für alle Arten von Autoren zugänglich.
* Inhalte, die Teil eines öffentlichen Ordners sind, können nicht Teil eines anderen Ordners sein. Das Gegenteil trifft auch zu.

Dieser Ordner kann nicht Teil einer konfigurierbaren Rollendefinition sein. Wenn also ein öffentlicher Ordner nicht in einer konfigurierbaren Rollendefinition enthalten ist, wird der Zugriff auf einen öffentlichen Ordner nicht eingeschränkt.

### Privater Ordner

* Jeder von einem Administrator erstellte Ordner ist ein privater Ordner.

### Ordnervorgänge

**Ordner hinzufügen**

Um einen Ordner hinzuzufügen, klicken Sie auf **[!UICONTROL Hinzufügen]** oben rechts im Fenster.

**Ordner löschen**

Sie können auch einen Ordner löschen. Wählen Sie den zu löschenden Ordner aus, klicken Sie auf das Menü &quot;Aktionen&quot; und dann auf **[!UICONTROL Ordner löschen]**.

>[!NOTE]
>
>Ordner können gelöscht werden, wenn der gesamte zugehörige Inhalt auch mit anderen Ordnern verknüpft ist. Wenn Inhalte vorhanden sind, die nur mit dem zu löschenden Ordner verknüpft sind, verschieben Sie zunächst den Inhalt in einen anderen Ordner und löschen Sie dann den Ordner.

## Standorte für Klassenzimmer

Administratoren können mit dieser Einstellung eine Bibliothek mit Speicherorten für Klassenzimmer erstellen und konfigurieren. Autoren können einen vorkonfigurierten Speicherort auswählen, um ihr Klassenzimmerereignis einzurichten. Wählen Sie einen Speicherort aus der Bibliothek aus, um die Standortinformationen, die URL und die Lizenzbeschränkung automatisch auszufüllen.

Als Administrator haben Sie folgende Möglichkeiten:

### Speicherorte in CSV importieren

Fügen Sie Ihrem Konto Speicherorte hinzu, indem Sie eine CSV-Datei mit Speicherorten importieren. Die CSV-Datei muss die Spalte City enthalten.

### Hinzufügen eines Speicherorts

Fügen Sie Folgendes hinzu:

1. Name des Standorts: Geben Sie den Namen des Klassenzimmers ein.
2. Standortinformationen: Geben Sie die Informationen zum Standort ein.
3. Region: Der eingegebene Wert wird als Filter &quot;Schulungsstandorte&quot; für Teilnehmer angezeigt.
4. URL des Speicherorts: Geben Sie die URL des Speicherorts ein.
5. Sitzplatzbeschränkung: Geben Sie die Sitzplatzkapazität des Raumes ein.

![Klassenzimmerposition](assets/location-alm.gif)

*Fügen Sie Speicherorte für Klassenzimmer hinzu*

Sie können den Speicherort auch mithilfe einer CSV-Datei hinzufügen. Die CSV-Datei muss die folgenden Felder enthalten:

* name
* Info
* url
* Sitzplatzbeschränkung
* Region

<!--![Add classroom locations](assets/add-classroom-csv.png)-->

## Häufig gestellte Fragen {#frequentlyaskedquestions}

+++Wie kann ich unterschiedliche Ordner für die Inhaltsbibliothek erstellen?

Klicken **[!UICONTROL Einstellungen]** > **[!UICONTROL Inhaltsordner]**. Um einen Ordner hinzuzufügen, klicken Sie auf **[!UICONTROL Hinzufügen]** in der oberen rechten Ecke und geben Sie im Dialogfeld den Namen und die Beschreibung des Ordners ein.

Inhaltsordner können von Administratoren konfiguriert werden. Erst nach der Konfiguration werden Inhaltsordner für Autoren sichtbar und sie erhalten die Möglichkeit, den Inhalt in einem oder mehreren Ordnern zu platzieren.

Weitere Informationen finden Sie im Abschnitt [Inhaltsordner](settings.md#content-folder).
+++

+++Wie kann ich das Geschäftsjahr für das Konto hinzufügen?

In **[!UICONTROL Einstellungen]** > **[!UICONTROL Grundlegende Informationen]** auf **[!UICONTROL Ändern]**. Im Fenster &quot; **[!UICONTROL Geschäftsjahr beginnt am]** den Monat aus.
+++

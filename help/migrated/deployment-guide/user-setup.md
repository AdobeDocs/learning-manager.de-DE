---
jcr-language: en_us
title: Einrichten von Benutzern im Lern-Manager
contentowner: shhivkum
preview: true
source-git-commit: 0fabd369e70e15ba22fead0177a24aafd851d88d
workflow-type: tm+mt
source-wordcount: '1816'
ht-degree: 0%

---



# Einrichten von Benutzern im Lern-Manager

## Interne und externe Benutzer {#internalandexternalusers}

In jedem LMS, einschließlich Learning Manager, ist die Verwaltung von Benutzern ein wichtiger Aspekt. Mit dem Learning Manager können Sie Benutzer als interne und externe Benutzer klassifizieren. Interne Benutzer sind Benutzer, die einer bestimmten Organisation oder Gruppe angehören. Im Allgemeinen sind Benutzer innerhalb eines Unternehmens interne Benutzer. Diese Benutzer verfügen über bestimmte Lernobjekte mit bestimmten Fristen, die von ihren Managern oder vom Administrator zugewiesen werden.

Im Gegensatz dazu sind externe Benutzer in der Regel temporäre Benutzer eines bestimmten Learning Manager-Kontos. Diese Benutzer können auf bestimmte Lernobjekte zugreifen, indem sie auf einen temporären externen Link klicken, den sie per E-Mail erhalten. Die externen Benutzerprofile haben in der Regel ein Ablaufdatum. Beispielsweise kann ein Unternehmen, das Zertifizierungen für Java durchführt, jeden Benutzer haben, der sich vorübergehend anmeldet, um relevante Kurse abzuschließen und dann die Zertifizierung zu versuchen. Schulungen und Kurse für externe Benutzer sind in der Regel ebenfalls mit begrenzter Kapazität ausgestattet.

Lesen Sie weiter, um zu erfahren, wie Sie interne und externe Benutzer in Learning Manager hinzufügen.

## Externe Benutzer einrichten {#setupexternalusers}

Als Administrator möchten Sie möglicherweise externe Benutzer, z. B. Mitarbeiter von Partnerorganisationen, zu Ihrem Learning Manager-Konto hinzufügen. So fügen Sie externe Benutzer hinzu

1. Im **[!UICONTROL **Administrator**]**Anmeldeseite, klicken Sie auf **[!UICONTROL **Benutzer**]**im linken Navigationsbereich.
1. Im **[!UICONTROL **Benutzer**]**page, click **[!UICONTROL **Extern**]**im linken Navigationsbereich. Das System zeigt die Seite &quot;Externe Benutzer&quot; mit einer Liste der externen Benutzer an (falls zutreffend).
1. Klicken Sie auf **[!UICONTROL **Hinzufügen**]**oben rechts auf der Seite.

   ![](assets/set-up-external-users-step3.png)

1. Im **[!UICONTROL **Benutzer hinzufügen**]**Die folgenden Felder sind obligatorisch:

   * **[!UICONTROL **Profilname**:]**Geben Sie den Namen für das externe Profil an, das Sie erstellen.
   * **[!UICONTROL ** Manager-E-Mail **:]** Geben Sie die E-Mail-Adresse des Managers für den externen Benutzer an.
   * **[!UICONTROL ** Plätze **:]** Geben Sie die Anzahl der Teilnehmer an, die sich für den Kurs anmelden können.
   * **[!UICONTROL ** Ablauf **:]** Geben Sie das Ablaufdatum an, nach dem ein externer Benutzer den Kurs nicht mehr registrieren oder nutzen kann.

1. Klicken **[!UICONTROL ** Erweiterte Einstellungen **.]**
1. Legen Sie optional die folgenden Optionen fest, wenn Sie ein externes Profil erstellen:

   * **[!UICONTROL ** Bild hinzufügen **:]** Ziehen Sie das gewünschte Bild per Drag &amp; Drop. Dieses Bild wird auf der Teilnehmerseite für Benutzer angezeigt.
   * **[!UICONTROL ** Anmeldeanforderung **:]** Geben Sie die Anzahl der Tage an, die der Benutzer für die Anmeldung benötigt. Wenn der externe Benutzer diese Anmeldefrist überschreitet, kann der Teilnehmer nicht auf das Lernobjekt zugreifen oder es nutzen.
   * **[!UICONTROL ** Zulässige Domänen **:]** Geben Sie die durch Kommas getrennten Domänen an. Nur Benutzer mit den angegebenen Domänen können sich für das Konto registrieren.
   * **[!UICONTROL ** E-Mail-Verifizierung erforderlich **:]** Aktivieren Sie dieses Kontrollkästchen, wenn eine Bestätigungs-E-Mail an Benutzer gesendet werden soll.



1. Klicken **[!UICONTROL Speichern.]**



   ![](assets/set-up-external-users-step7.png)

   Ein Popup-Dialogfeld mit der URL wird angezeigt. Sie können diese URL kopieren und an die externen Benutzer senden. Standardmäßig wird eine E-Mail mit dieser URL an den Benutzer gesendet.

1. Wenn Sie externe Profile hinzufügen, werden sie im Fenster &quot; **[!UICONTROL ** Seite für externe Benutzer **(** Administrator **>** Benutzer **>** Extern **).]** Für diese Benutzer werden auch die Höchstzahl der Lizenzen, das Ablaufdatum und die Anmeldeanforderungen angezeigt.
1. Um die Einstellungen eines externen Benutzers jederzeit zu bearbeiten, klicken Sie auf den Benutzernamen. Die **[!UICONTROL Externe Registrierung bearbeiten]** &quot; wird angezeigt. Ändern Sie die Einstellungen und klicken Sie auf **[!UICONTROL ** Speichern **.]**
1. Sie können die Begrüßungs-E-Mail erneut senden oder die URL jederzeit kopieren, indem Sie auf die Symbole &quot;E-Mail-Adresse&quot;/&quot;URL kopieren&quot; neben dem externen Profil klicken.

   ![](assets/set-up-external-users-step10.png)

## Halten Sie das externe Benutzerprofil an {#pausetheexternaluserprofile}

Nachdem Sie dem Lern-Manager eine externe Benutzergruppe hinzugefügt haben, können Sie auch den Registrierungsprozess für externe Benutzer anhalten. Wenn Sie anhalten, wird der Registrierungsprozess für externe Benutzer blockiert. Dieser Vorgang funktioniert jedoch nur, wenn die Benutzer sich noch nicht registriert haben, indem sie die Einladung annehmen.

Um die externen Benutzergruppen anzuhalten, klicken Sie auf **[!UICONTROL **Aktionen**]**oben rechts auf der Seite und wählen Sie **[!UICONTROL Anhalten]**.

## Externes Benutzerprofil fortsetzen {#resumeexternaluserprofile}

Sie können die Sperre (Pause) jederzeit widerrufen, indem Sie die Option &quot;Fortsetzen&quot; wählen. Klicken Sie auf **[!UICONTROL **Aktionen**]**oben rechts auf der Seite, und wählen Sie **[!UICONTROL Fortsetzen]**.

**[!UICONTROL Externe Benutzerstatus]**

Im Lern-Manager gelten die folgenden Status für externe Benutzer:

* **Inaktiver Zustand** - In diesem Status ist die Registrierung für externe Benutzer abgelaufen. Administratoren legen das Ablaufdatum für die externen Benutzer fest, während sie sie über den Arbeitsablauf zum Hinzufügen von Benutzern hinzufügen.
* **Aktiver Zustand** - In diesem Status können sich die externen Benutzer bei der Learning Manager-Anwendung registrieren und sich auch bei der Anwendung anmelden.
* **Anhalten** - In diesem Status ist der Registrierungsprozess für externe Benutzer blockiert. Die vorhandenen Benutzer können sich jedoch weiterhin anmelden.

## Interne Benutzer einrichten {#setupinternalusers}

Als Administrator möchten Sie möglicherweise Benutzer für Ihr Unternehmen oder Ihre Organisation einrichten. Diese Benutzer werden auch als interne Benutzer bezeichnet. Interne Benutzer können sich entweder mit Single Sign On oder mit Adobe ID bei der Anwendung anmelden. Diese Benutzer können dann auf die Lernobjekte gemäß ihren Anforderungen zugreifen und diese nutzen. Es gibt drei Möglichkeiten, interne Benutzer für eine Organisation einzurichten:

* Mehrere Benutzer gleichzeitig mithilfe einer CSV-Datei hinzufügen
* Hinzufügen von Benutzern durch Selbstregistrierung
* Hinzufügen eines einzelnen internen Benutzers



## Benutzer mithilfe einer CSV-Datei hinzufügen {#addingusersusingacsvfile}

Sie können diese Methode auswählen, um interne Benutzer hinzuzufügen, wenn die Anzahl der Benutzer groß ist. Wenn Sie zum ersten Mal Benutzer mit einer CSV-Datei hinzufügen, müssen Sie die CSV-Dateninhalte den Anwendungsbezeichnungen zuordnen. Wenn Sie anschließend neue Benutzer hinzufügen oder die Benutzerdaten aktualisieren, wird dieselbe Zuordnung beibehalten. So fügen Sie mehrere interne Benutzer gleichzeitig hinzu

1. Im Fenster &quot; **[!UICONTROL Administratorstartseite]** klicken Sie auf **[!UICONTROL **Benutzer**]**im linken Navigationsbereich.
1. Klicken **[!UICONTROL ** Hinzufügen **>** CSV hochladen **.]**
1. Klicken Sie im Popup-Dialogfeld auf **[!UICONTROL ** Importieren **.]**
1. Navigieren Sie zu dem Speicherort, an dem Sie die CSV-Datei gespeichert haben. Klicken **[!UICONTROL Öffnen]**.
1. Importieren Sie die CSV-Datei und ordnen Sie den Inhalt der CSV-Datei den Anwendungsbezeichnungen zu. Dieser Schritt gilt nur, wenn Sie die CSV-Datei zum ersten Mal hochladen.
1. Klicken Sie auf **[!UICONTROL **Speichern**]**, um die Zuordnung zu speichern.
1. Klicken Sie auf **[!UICONTROL **Hinzufügen**]**zum Hochladen der CSV-Datei, die bereits den Anwendungsdaten zugeordnet ist.

### Überlegungen zum Erstellen der CSV-Datei für den Upload: {#considerationswhencreatingthecsvfileforupload}

Wenn Sie die CSV-Datei zum Hochladen interner Benutzer erstellen, sind die folgenden Pflichtfelder aufgeführt, für die Sie Daten eingeben müssen: Name des Mitarbeiters, E-Mail-Adresse des Mitarbeiters, Profil oder Bezeichnung des Mitarbeiters und Managerhierarchie.

Der Name und die E-Mail-Adresse jedes Mitarbeiters können den Anwendungsdaten direkt zugeordnet werden. Beachten Sie, dass Sie eine E-Mail-Adresse angeben müssen, die in der CSV-Datei als Manager-E-Mail angegeben ist. Sie können entweder die Manager-ID beim Erstellen der CSV-Datei definieren oder die E-Mail-ID angeben, die der Manager-ID beim Hochladen der CSV-Datei entspricht.

***Bevor Sie eine ID als Manager-ID eines Mitarbeiters hinzufügen, stellen Sie sicher, dass der Manager als Mitarbeiter in der CSV-Datei hinzugefügt wird.***

***Stellen Sie sicher, dass zwischen den Einträgen keine zusätzlichen Leerzeichen stehen, damit die CSV-Datei erfolgreich hochgeladen werden kann.***

Hier sehen Sie eine Beispiel-Momentaufnahme einer CSV-Datei:

![](assets/considerations-whencreatingthecsvfileforupload.png)

Um eine Beispiel-CSV-Datei herunterzuladen, laden Sie `<give link to zip file>`.

<!--Zip file reference, no source file-->

### Einrichten von Stammbenutzern {#settinguprootuser}

Automatisierter Massenimport von Benutzern.

## Hinzufügen von Benutzern durch Selbstregistrierung {#addingusersthroughselfregistration}

Sie können nicht nur mehrere interne Benutzer gleichzeitig hinzufügen, sondern auch Benutzer durch Selbstregistrierung hinzufügen. Sie können die Selbstregistrierung verwenden, um Mitarbeitern die Möglichkeit zu geben, sich als Teilnehmer bei Ihrem Learning Manager-Konto zu registrieren. Wenn Sie ein Selbstregistrierungsprofil erstellen, wird eine eindeutige URL erstellt. Geben Sie diese URL für den Mitarbeiter frei, damit er sich im Learning Manager registrieren kann.

1. Im Fenster &quot; **[!UICONTROL Administratorstartseite]** klicken Sie auf **[!UICONTROL Benutzer]** im linken Navigationsbereich.
1. Klicken **[!UICONTROL ** Hinzufügen **>** Selbstregistrierung **.]**

   ![](assets/adding-users-throughself-registration-step2.png)

1. Im Dialogfeld &quot; **[!UICONTROL Benutzer hinzufügen]** den Namen des Mitarbeiters im Dialogfeld **[!UICONTROL Profilname]** ein.
1. Im Dialogfeld &quot; **[!UICONTROL Managername]** den Namen des Managers des Mitarbeiters ein.
1. Optional können Sie das Profilbild des Mitarbeiters mit der **[!UICONTROL Bild hinzufügen]** ein.
1. Klicken **[!UICONTROL Speichern]**.

   ![](assets/adding-users-throughself-registration-step6.png)

   Das System zeigt ein weiteres Popup-Dialogfeld mit der Meldung an, dass das Profil erfolgreich erstellt wurde. In diesem Dialogfeld wird außerdem eine eindeutige URL generiert.

1. Geben Sie diese URL für den Mitarbeiter frei, damit er sich selbst als Teilnehmer registrieren kann.

   ![](assets/adding-users-throughself-registration-step7.png)

## Einzelne Benutzer im Lern-Manager hinzufügen {#addsingleusersincaptivateprime}

Das Hinzufügen einzelner Benutzer ist die dritte Methode, mit der Sie Ihrem Konto interne Benutzer hinzufügen können. Wenn Sie einige Benutzer hinzufügen möchten, ist dieses Verfahren ideal. Hinzufügen eines einzelnen Benutzers:

1. Im Fenster &quot; **[!UICONTROL Administratorstartseite]** klicken Sie auf **[!UICONTROL Benutzer]** im linken Navigationsbereich.
1. Klicken **[!UICONTROL ** Hinzufügen **>** Einzelbenutzer **.]**



1. Geben Sie im Popupmenü &quot;Benutzer hinzufügen&quot; die folgenden Details für Benutzer an:

   * **[!UICONTROL Name]** **[!UICONTROL :]** Geben Sie den Namen des Mitarbeiters oder internen Benutzers an. Dieses Feld ist obligatorisch.

   * **[!UICONTROL Email]** **[!UICONTROL :]** Geben Sie die E-Mail-ID des Mitarbeiters an. Dieses Feld ist obligatorisch.

   * **[!UICONTROL Profil]** **[!UICONTROL :]** Geben Sie die Bezeichnung oder die Stellenbezeichnung des Mitarbeiters an.

   * **[!UICONTROL ** Managername **:]** Geben Sie den Namen des Managers an. Der Manager sollte bereits in der Datenbank hinzugefügt werden, um hier angegeben zu werden.
   * **[!UICONTROL ** DOJ **:]** Geben Sie das Datum des Eintritts des Mitarbeiters an.
   * **[!UICONTROL **Speicherort**:]**Geben Sie den Standort des Mitarbeiters an. Wenn sich Ihre Organisation beispielsweise an mehreren geografischen Standorten befindet, geben Sie den Standort an, an dem sich der Mitarbeiter befindet.



   ![](assets/add-single-usersincaptivateprime-step3.png)

1. Klicken **[!UICONTROL Hinzufügen]**.
1. Das System zeigt eine Meldung an, dass der Benutzer erfolgreich hinzugefügt wurde. Der Benutzer erhält einen Bestätigungslink in der angegebenen E-Mail-ID. Der Benutzer kann auf diesen Link klicken, um sein Konto zu aktivieren und mit dem Zugriff auf den Lernmanager zu beginnen.

   ![](assets/add-single-usersincaptivateprime-step5.png)

## Verwalten von Benutzergruppen im Lern-Manager {#managingusergroupsincaptivateprime}

Benutzergruppe ist nichts anderes als eine Gruppe von Benutzern, die zu einer definierten Kategorie gehören. Als Administrator können Sie Benutzergruppen verwenden, um Teilnehmer basierend auf ihren Attributen schnell auszuwählen. Darüber hinaus können Sie der Benutzergruppe schnell Logos oder Kataloge zuweisen und benutzerdefinierte Fortschrittsberichte erstellen.

Es gibt zwei Arten von Benutzergruppen im Lern-Manager: benutzerdefinierte und automatisch generierte. Wenn Sie Ihrem Konto Teilnehmer hinzufügen, werden einige Standardgruppen automatisch basierend auf den Rollen und Eigenschaften der Benutzer in Ihrem Konto erstellt. Diese Gruppen werden automatisch generiert. Beispiel: eine Gruppe mit allen Teilnehmern oder allen Autoren.

***Sie können den Namen und die Beschreibung automatisch generierter Gruppen nicht bearbeiten.***

Um die automatisch generierten Benutzergruppen im Lern-Manager anzuzeigen, klicken Sie im linken Bereich auf **[!UICONTROL Automatisch generiert]**. Die Anwendung zeigt eine Liste aller automatisch generierten Benutzergruppen an, die für Ihr Konto verfügbar sind.

Sie können auch benutzerdefinierte Gruppen mit einer ausgewählten Benutzerliste im Lern-Manager erstellen. Mit benutzerdefinierten Gruppen können Sie einen Namen, eine Beschreibung und die Attribute für die Benutzergruppe angeben. Benutzerdefinierte Gruppen, die Sie im Lern-Manager erstellen, sind dynamischer Natur. Das heißt, wenn neue Benutzer mit ähnlichen Attributen hinzugefügt werden, werden sie automatisch zu diesen Benutzergruppen hinzugefügt.

## Benutzerdefinierte Benutzergruppen erstellen {#createcustomusergroups}

1. Klicken Sie auf der Startseite des Learning Manager-Administrators auf **[!UICONTROL Benutzer]**.
1. Klicken Sie auf der Seite Benutzerdefinierte Benutzergruppen auf **[!UICONTROL **Hinzufügen**]**oben rechts auf der Seite.

   Das System zeigt das Fenster &quot; **[!UICONTROL Benutzergruppe hinzufügen]** &quot; eingeben.

   ![](assets/creating-custom-usergroups.png)

1. Geben Sie den Namen und die Beschreibung für Ihre Benutzergruppe an. Zum Beispiel Dev-Users , zu denen Benutzer des Produktentwicklungsteams gehören.
1. Fügen Sie Benutzer zur benutzerdefinierten Benutzergruppe hinzu, indem Sie den Benutzernamen oder das Profil des Benutzers in das Feld **[!UICONTROL ** Benutzer hinzufügen **ein.]**
1. Um der benutzerdefinierten Gruppe weitere Benutzer hinzuzufügen, klicken Sie auf **[!UICONTROL ** Weitere Benutzer hinzufügen **.]**
1. Klicken Sie nach dem Hinzufügen aller Benutzer auf **[!UICONTROL Speichern]**zum Speichern der benutzerdefinierten Benutzergruppe.


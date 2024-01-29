---
jcr-language: en_us
title: Häufig gestellte Fragen für Administratoren
description: Häufig gestellte Fragen für Adobe Learning Manager-Administratoren
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '2398'
ht-degree: 0%

---



# Häufig gestellte Fragen für Administratoren

<table>
 <tbody>
  <tr>
   <td><img src="assets/administrator2.png"></td>
   <td>
    <p>Im Folgenden erhalten Sie Informationen zu den häufig gestellten Fragen zum Learning Manager, die der Administratorrolle zugeordnet sind. </p></td>
  </tr>
 </tbody>
</table>

+++Kann ich mehrere Benutzer gleichzeitig hinzufügen? Wie?

Ja, Sie können mehrere Benutzer gleichzeitig hinzufügen, indem Sie die CSV-Upload-Funktion verwenden. Klicken  [hier](/help/migrated/administrators/add-users-in-bulk.md) für weitere Informationen.

+++

+++Wie kann ich die E-Mail-ID korrigieren, die beim Erstellen der Anmeldung für meine Teilnehmer falsch eingegeben wurde?

Um die Benutzeranmeldung zu korrigieren, müssen Sie eine CSV-Datei in den Lern-Manager importieren. Unten auf dieser Seite wird als Referenz eine Beispiel-CSV-Datei angehängt. Da E-Mails als eindeutige Kennungen für eine Person betrachtet werden, können sie nicht bearbeitet werden. Führen Sie folgende Schritte aus:

1. Fügen Sie denselben Benutzer mit der korrekten E-Mail-ID in die CSV-Datei ein und stellen Sie sicher, dass er als Manager anderer Benutzer bleibt, indem Sie seine E-Mail-ID der Spalte &quot;E-Mail des Managers des Mitarbeiters&quot; in der Beispiel-CSV hinzufügen.
1. Andere Benutzer in Ihrem Konto zur CSV hinzufügen, einschließlich sich selbst
1. Importieren Sie diese Datei in die Learning Manager-Admin-App->Benutzer->Hinzufügen->CSV importieren.
1. Ordnen Sie alle Felder den entsprechenden CSV-Spalten zu, wenn Sie im Dialogfeld dazu aufgefordert werden.
1. Klicken Sie auf Speichern.

Benutzer sollten auf der Teilnehmerseite hinzugefügt werden.

[Beispiel für Learning Manager CSV.csv](https://helpx.adobe.com/content/dam/help/en/captivate_prime/learning-manager-sample-csv.zip)

+++

+++Wie richte ich Warnungen ein?

In Adobe Learning Manager 1.0 können Sie Benachrichtigungen erstellen. Siehe  [Benachrichtigungsfrage](/help/migrated/administrators/feature-summary/user-notifications.md) für weitere Informationen.

+++

+++Wie füge ich Zertifikate für Kurse hinzu?

Adobe Learning Manager stellt keine Zertifikate für die Kurse zur Verfügung. Der Administrator kann jedoch Abzeichen für die einzelnen Kurse erstellen, indem er im linken Bereich auf die Registerkarte Abzeichen klickt. Wenn der Administrator Teilnehmer für einen Kurs registriert, kann er auch ein Abzeichen damit verknüpfen.

+++

+++Wie importiere ich Signaturen für die Zertifikate?

Im Adobe Learning Manager gibt es keine Funktion zum Importieren von Signaturen für die Zertifizierung oder das Abzeichen.

+++

+++Kann ich einen Kalender für die Kurse einrichten? Wie?

In der Version Adobe Learning Manager 1.0 gibt es keine Möglichkeit, einen Kalender für die Kurse einzurichten.

+++

+++Wie registriere ich die Teilnehmer auf der Warteliste direkt?

Die Teilnehmer werden auf eine Warteliste für jeden Klassenzimmerkurs gesetzt, wenn die Lizenzen begrenzt sind, basierend auf der Reihenfolge ihrer Registrierung. Administratoren können Teilnehmer auf der Warteliste auswählen und ihnen Lizenzen zuweisen, die die Obergrenze für die Lizenzen für jeden Klassenzimmerkurs ersetzen. Die Teilnehmer werden für den Kurs registriert, sobald der Administrator ihnen eine Lizenz zuweist.

1. Klicken Sie im linken Teilfenster auf &quot;Kurse&quot;, nachdem Sie sich als Administrator angemeldet haben.
1. Klicken Sie in der Liste der verfügbaren Kurse auf den Kursnamen eines beliebigen Präsenzkurses Ihrer Wahl. Eine neue Seite mit detaillierten Informationen zum Kurs wird angezeigt.
1. Klicken Sie auf Warteliste im linken Bereich der Kursdetailseite. Eine Liste der auf die Warteliste gesetzten Teilnehmer wird auf der Seite angezeigt.
1. Wählen Sie die Teilnehmer aus und klicken Sie auf &quot;Lizenzen zuweisen&quot;, um die Teilnehmer direkt für die Kurse zu registrieren, wobei die Obergrenze für die Lizenzen aufgehoben wird.

Weitere Informationen finden Sie unter  [Warteliste und Anwesenheit](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md) Funktion.

+++

+++Wie kann ich die Anwesenheit von Teilnehmern am Klassenzimmermodul aufzeichnen?

Ja, Sie können die Anwesenheit mit den folgenden Schritten erfassen:

1. Klicken Sie im linken Teilfenster auf &quot;Kurse&quot;, nachdem Sie sich als Administrator angemeldet haben.
1. Klicken Sie in der Liste der verfügbaren Kurse auf den Kursnamen eines beliebigen Klassenzimmermoduls/Kurses Ihrer Wahl. Eine neue Seite mit detaillierten Informationen zum Kurs wird angezeigt.
1. Wählen Sie die Teilnehmer aus und klicken Sie auf Speichern , um den Kursabschluss aufzuzeichnen.

Wenn ein Kurs mehrere Module umfasst und der Teilnehmer nur eines davon abgeschlossen hat, können Sie ein einzelnes Modul auswählen und auf &quot;Speichern&quot; klicken, um den Abschluss für den Teilnehmer zu markieren. Wenn der Teilnehmer alle Module eines Kurses abgeschlossen hat, können Sie auf die Option &quot;Alle auswählen&quot; und dann auf &quot;Speichern&quot; klicken.

Weitere Informationen finden Sie unter  [Warteliste und Anwesenheit](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md) Funktion.

+++

+++Wie schließe ich die L3-Feedbackoption ein?

Sie können L3-Feedback hinzufügen, während Sie Teilnehmer für die Kurse registrieren. Fügen Sie eine L3-Feedbackfrage hinzu, indem Sie die folgenden Schritte ausführen:

1. Klicken Sie im linken Teilfenster auf &quot;Kurse&quot;, nachdem Sie sich als Administrator angemeldet haben. Auf der rechten Seite werden Listen mit allen Kursen angezeigt.
1. Klicken Sie auf die Kurskachel, für die Sie L3-Feedback hinzufügen möchten.
1. Klicken Sie im linken Teilfenster auf &quot;Standardwerte für Instanz&quot;.
1. Klicken Sie auf den Kreis auf der Umschaltfläche neben L3 - Feedback zu Verhaltensänderungen , um ihn auszuwählen.
1. Fügen Sie die L3-Feedbackfrage im Textbereich unter L3-Frage hinzu.

+++

+++Wie beantrage ich die Nominierung des Managers für einen vom Manager nominierten Kurs?

Als Administrator können Sie die Nominierung des Managers für die Kurse beantragen, indem Sie die folgenden Schritte ausführen:

1. Klicken Sie im linken Teilfenster auf &quot;Kurse&quot;
1. Bewegen Sie die Maus über einen vom Manager nominierten Kurs und klicken Sie auf **[!UICONTROL Managernominierung anfordern]**.

1. Klicken Sie in der Liste der Instanzen auf **[!UICONTROL Von Managern nominiert]** Link gefolgt von **[!UICONTROL Manager hinzufügen]** Link.

1. Fügen Sie den Namen des Managers und die Anzahl der zugewiesenen Lizenzen hinzu und klicken Sie auf das Häkchen, um die Änderungen zu speichern.

Beim Erstellen der Kurse wählt der Autor den Kurstyp &quot;Von Manager nominiert&quot;.

+++

+++Wie registriere ich einen Teilnehmer für einen bestimmten Kurs?

Registrieren Sie Teilnehmer für Kurse, indem Sie die folgenden Schritte ausführen:

1. Klicken Sie im linken Teilfenster auf &quot;Kurse&quot;, nachdem Sie sich als Administrator angemeldet haben. Auf der rechten Seite wird eine Liste aller Kurse angezeigt.
1. Wählen Sie den Kurs aus, für den Sie Teilnehmer hinzufügen möchten, und bewegen Sie den Mauszeiger darüber.
1. Klicken Sie auf Teilnehmer registrieren und fügen Sie den Namen der Teilnehmer hinzu. **Hinweis:** Sie können einen oder mehrere Teilnehmer gleichzeitig hinzufügen.

+++

+++Wie kann ich Teilnehmern bestimmte Kenntnisse zuweisen?

Weisen Sie Teilnehmern Kompetenzen zu, indem Sie die folgenden Schritte ausführen:

1. Klicken **[!UICONTROL Kenntnisse]** im linken Bereich, nachdem Sie sich als Administrator angemeldet haben.
1. Wählen Sie eine oder mehrere Qualifikationen aus, indem Sie die Kontrollkästchen für jede Qualifikation aktivieren und dann auf **[!UICONTROL Aktionen]** in der rechten oberen Ecke der Seite.
1. Klicken Sie auf Benutzern zuweisen.
1. Beginnen Sie mit der Eingabe des Benutzernamens, wählen Sie ihn aus der Dropdown-Liste aus und klicken Sie auf **[!UICONTROL Speichern]**.

   >[!NOTE]
   >
   >Sie können mehrere Teilnehmer für Qualifikationen registrieren, indem Sie auf Weitere Benutzer hinzufügen klicken und den 4. Schritt wiederholen.

+++

+++Wie kann ich eine Lernprogrammsitzung erstellen?

Um ein Lernprogramm zu erstellen, führen Sie die folgenden Schritte aus:

1. Klicken Sie im linken Teilfenster auf &quot;Lernprogramm&quot;. Die Seite &quot;Lernprogramme&quot; wird mit einer Liste der vorhandenen Lernprogramme angezeigt.
1. Klicken Sie in der rechten oberen Ecke der Seite auf Hinzufügen .\
   Geben Sie den Programmnamen, die Übersicht und die Beschreibung ein und klicken Sie auf &quot;Speichern&quot;.
1. Klicken Sie im linken Teilfenster auf &quot;Kurse&quot;.
1. Fügen Sie einen oder mehrere Kurse hinzu, indem Sie auf die Kachel eines Kurses klicken.

   >[!NOTE]
   >
   >Sie müssen das Lernprogramm veröffentlichen, bevor Sie Teilnehmer oder eine Instanz registrieren.

1. Klicken Sie im linken Teilfenster auf &quot;Instanzen&quot; und dann auf **[!UICONTROL Neue Instanzen hinzufügen]** in der rechten Ecke der Seite, um Details zur Instanz anzuzeigen.

Weitere Informationen zu Lernprogrammen finden Sie unter  [Lernprogrammfunktion.](/help/migrated/administrators/feature-summary/learning-programs.md)

+++

+++Wie kann ich Berichte für alle Rollen ändern oder anpassen?

Klicken Sie auf den Dropdownpfeil in der oberen rechten Ecke jedes Berichts, um Berichte zu bearbeiten/zu ändern. Klicken Sie nach Abschluss der Änderungen auf Speichern und zeigen Sie den geänderten Bericht an.

+++

+++Wie ändere ich Kurse, Lernprogramme und das Unternehmensprofil?

Sie können Kurse und Lernprogramme auch nach der Veröffentlichung bearbeiten. Weitere Informationen finden Sie unter  [Kurse](/help/migrated/administrators/feature-summary/courses.md) und  [Lernprogramme](/help/migrated/administrators/feature-summary/learning-programs.md) Hilfeinhalte.

Um das Unternehmensprofil zu ändern, klicken Sie auf **[!UICONTROL Einstellungen]** im linken Bereich und klicken Sie auf **[!UICONTROL Ändern]** oben rechts auf der Seite.

+++

+++Wie suche ich nach den Kursen?

Klicken Sie im linken Teilfenster auf &quot;Kurse&quot;, nachdem Sie sich als Administrator angemeldet haben. Eine Liste aller verfügbaren Kurse wird angezeigt.

Sie können Kurse auf zwei Arten durchsuchen:

1. Klicken Sie auf das Suchsymbol in der rechten oberen Ecke. Ein Suchfeld wird angezeigt. Geben Sie den Kursnamen oder zu Ihren Kursen passende Schlüsselwörter ein, um nach diesen zu suchen.
1. Durch Filtern der Kursliste mithilfe der Filter.

Sie können die Kurse nach Status filtern, z. B. &quot;Alle&quot;, &quot;Veröffentlicht&quot; und &quot;Eingestellt&quot;, indem Sie auf jede dieser Optionen klicken. Sie können auch nach Kompetenzen suchen, indem Sie auf &quot;Kompetenzen&quot; klicken und die einzelnen Kompetenzen auswählen.

Abhängig von Ihrer Wahl können Sie die gefilterte Liste der Kurse anzeigen und die erforderlichen Kurse auswählen.

+++

+++Kann ich das Design der Anwendung ändern? Wie?

Ja, Sie können die Designs und das Branding der Learning Manager-Anwendung gemäß den Anforderungen Ihres Unternehmens ändern. Ein Satz von fünf repräsentativen Bildern wird bereitgestellt, um Ihre Farbdesignänderungen in der Vorschau anzuzeigen, bevor Sie sie auf Ihre Anwendung anwenden. Durchsuchen Sie diese Bilder, indem Sie auf die Symbole &lt; und > auf der linken bzw. rechten Seite der Bilder klicken, um eine Vorschau anzuzeigen.

Klicken **[!UICONTROL Branding]** im linken Bereich, um Ihren Organisationsnamen zu aktualisieren, die Subdomäne, Protokollstile und Designs zu ändern. Klicken **[!UICONTROL Bearbeiten]** neben jedem dieser Themen, um den Inhalt zu ändern.

Siehe  [Hilfe zu Farbdesigns und Branding](/help/migrated/administrators/feature-summary/themes.md) für weitere Informationen.

+++

+++Wie kann ich Abzeichen für die Kurse einrichten?

1. Klicken Sie im linken Teilfenster auf &quot;Abzeichen&quot;, nachdem Sie sich als Administrator angemeldet haben.
1. Klicken Sie in der rechten oberen Ecke der angezeigten Seite auf Hinzufügen .
1. Fügen Sie einen Abzeichennamen hinzu.
1. Laden Sie das Abzeichen hoch, indem Sie auf Abzeichen hochladen klicken und auf Speichern klicken.

+++

+++Wie richte ich Gamification-Punkte für die Kurse ein?

Sie können Gamification-Punkte für Teilnehmer einrichten, indem Sie die folgenden Schritte ausführen:

1. Klicken Sie auf Gamification, nachdem Sie sich als Administrator angemeldet haben. Es erscheint eine Seite mit einer Liste der Bronze-, Silber-, Gold- und Platin-Stufen und den zu erreichenden Punkten, die jeder Stufe entsprechen. Eine Liste der Aufgaben und der entsprechenden Punkte sind verfügbar.
1. Klicken Sie auf das Bearbeitungssymbol neben jeder Aufgabe, um die Punkte einzurichten/zu ändern.

Siehe  [Gamification-Funktion](/help/migrated/administrators/feature-summary/gamification.md) für weitere Informationen.

+++

+++Wie erstelle ich Berichte für Manager und Teilnehmer?

Sie können Berichte erstellen, indem Sie die folgenden Schritte ausführen:

1. Klicken Sie auf Berichte im linken Bereich. Die Seite mit der Berichtzusammenfassung wird angezeigt.
1. Klicken Sie auf der Seite Berichte auf **[!UICONTROL Hinzufügen]** in der oberen rechten Ecke.

   **[!UICONTROL Bericht hinzufügen]** &quot; wird angezeigt.

1. Füllen Sie alle erforderlichen Felder aus und klicken Sie auf &quot;Speichern&quot;.

Nur Administratoren und Manager können Berichte erstellen oder anzeigen. Siehe [Berichtfunktion](/help/migrated/administrators/feature-summary/reports.md) für weitere Informationen.

+++

+++Wie ändere ich die Rollen &quot;Teilnehmer&quot;, &quot;Manager&quot; und &quot;Autor&quot;?

Sie können Ihre Kontoanmeldung für andere Rollen wie Teilnehmer, Manager und Autor ändern, ohne sich von Ihrem Konto abmelden zu müssen.

1. Klicken Sie auf den Dropdown-Pfeil neben Ihrem Profilbild in der oberen rechten Ecke der Seite.\
   Ein Popupmenü wird angezeigt.
1. Wählen Sie jede verfügbare Rolle aus, um Zugriff auf die entsprechenden Rollenkonten zu erhalten.

+++

+++Wie füge ich Benachrichtigungen für Benutzer ein?

Manager, Autoren und Teilnehmer können Benachrichtigungen basierend auf den Kursaktivitäten sehen. Der Administrator kann die Benachrichtigungen für alle Benutzer aktivieren/deaktivieren, indem er die folgenden Schritte ausführt:

1. Klicken Sie im linken Bereich auf E-Mail-Vorlagen und wählen Sie die Registerkarten Allgemein, Benutzerregistrierungen, Abschlüsse und Feedback aus.
1. Klicken Sie in der Liste unten auf die Ja/Nein-Umschaltflächen neben **jedem Ereignis** und wählen Sie Ja, um die Benachrichtigung zu aktivieren. Klicken Sie auf Nein, um das Senden von Benachrichtigungen für ein bestimmtes Ereignis zu deaktivieren.

+++

+++Wie lasse ich eine externe Registrierung für die Kurse zu?

Adobe Learning Manager bietet Ihnen die Möglichkeit, externe Abteilungsmitglieder oder externe Mitarbeiter Ihres Unternehmens für die Anwendung zu registrieren.

1. Klicken **[!UICONTROL Benutzer]** im linken Bereich.
1. Klicken **[!UICONTROL Extern]** im linken Bereich.
1. Klicken **[!UICONTROL Hinzufügen]** oben rechts auf der Seite.

   Das Dialogfeld &quot;Benutzer hinzufügen&quot; wird angezeigt.

1. Fügen Sie den Profilnamen, die Manager-E-Mail, die zugewiesenen Lizenzen und Ablaufinformationen hinzu. Sie können dem externen Profil auch ein Bild hinzufügen.
1. Klicken **[!UICONTROL Speichern]**.

Der Administrator kann die Registrierungs-URL kopieren und an die externe Registrierungsgruppe senden. Die externen Benutzer können sich registrieren, sich bei der Learning Manager-Anwendung anmelden und auf ihre Kurse zugreifen.

+++

+++Wie füge ich einen Fragebogen für das L1-Feedback hinzu?

Erstellen Sie einen Feedback-Fragebogen, der von den Teilnehmern verwendet werden kann, nachdem sie die Kurse absolviert haben. Standardmäßig sind drei Beispielfragen verfügbar. Führen Sie die folgenden Schritte aus, um einen Fragebogen zu erstellen.

1. Klicken Sie im linken Teilfenster auf Feedback . Ein Fenster für den Feedbackfragebogen wird angezeigt.
1. Klicken **[!UICONTROL Bearbeiten]** , um den Fragebogen hinzuzufügen bzw. zu ändern.

Sie können einen Fragebogen hinzufügen und ihn nur dann anzeigen, wenn Sie ihn benötigen. Klicken Sie auf das Kontrollkästchen, um eine bestimmte Frage zu aktivieren/deaktivieren.

+++

+++Wie richte ich die Kenntnisse und Stufen ein?

1. Klicken Sie auf Kompetenzen im linken Bereich des Fensters Administrator.
1. Klicken Sie auf Hinzufügen , um neue Kompetenzen hinzuzufügen.
1. Fügen Sie den Namen der Kompetenz, die Beschreibung und die entsprechenden Credits für jede Stufe hinzu.

   Standardmäßig ist für jede Kompetenz eine einzige Stufe mit 0 Credits verfügbar.

1. Klicken [!UICONTROL **Stufe hinzufügen**] , um jeder Kompetenz eine neue Stufe hinzuzufügen, und klicken Sie auf Speichern. Sie können bis zu 5 Ebenen hinzufügen.

Nachdem die Kompetenz gespeichert wurde, können Sie keine Stufen mehr aus der Kompetenz entfernen. Der Administrator kann Teilnehmer auch einer bestimmten Kompetenz und Stufe zuweisen.

+++

+++Wie richte ich das Abrechnungssystem für die Kurse meiner Organisation ein?

1. Klicken [!UICONTROL **Abrechnung**] im linken Bereich.

   Rechnungsinformationen werden auf der Seite angezeigt.

1. Klicken Sie auf [!UICONTROL **Abonnieren**] &quot; ändern.
1. Geben Sie die Anzahl der Pakete ein, die Sie bestellen möchten, und klicken Sie in der rechten oberen Ecke der Seite auf &quot;Bestellung aufgeben&quot;.

   Wählen Sie die Anzahl der Pakete basierend auf der Anzahl der Teilnehmer in Ihrem Unternehmen aus und geben Sie Ihre Bestellung auf. Bei einem bestellungsorientierten Prozess erreichen Sie uns unter  [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com).

1. Geben Sie Ihre Kontaktinformationen ein, wählen Sie den Kreditkartentyp, geben Sie Kreditkarteninformationen an und klicken Sie auf Bestellung abschließen.

Siehe [Abrechnungsmanagement](/help/migrated/administrators/feature-summary/billing-management.md) finden Sie weitere Informationen.

+++

+++Kann ich das Zertifikatdesign anpassen? Wie?

Im Adobe-Lernmanager können Sie Teilnehmer erkennen, indem Sie Abzeichen ausgeben. Weitere Informationen finden Sie unter Abzeichen.  Weitere Informationen finden Sie auch unter Zertifizierungsfunktion.

+++

+++Wie richte ich mein Unternehmensprofil ein?

1. Nachdem Sie sich als Administrator angemeldet haben, klicken Sie auf **[!UICONTROL Informationen zur Organisation]** im linken Bereich.
1. Fügen Sie Unternehmensprofil, Unterdomäne und Logo hinzu, indem Sie auf der Seite auf jede dieser Optionen klicken.

+++

+++Wie füge ich Kurse hinzu?

Um Kurse hinzuzufügen, müssen Sie Ihre Rolle als Autor wechseln. Sie können die Liste der verfügbaren Kurse nur basierend auf ihrem Status anzeigen **[!UICONTROL Vollständig]**, **[!UICONTROL Veröffentlicht]** und **[!UICONTROL Rentner]**.

Um Kurse anzuzeigen, klicken Sie auf **[!UICONTROL Kurse]** im linken Fensterbereich. Siehe  [Erstellen von Kursen](/help/migrated/administrators/feature-summary/courses.md)für weitere Informationen

+++

+++Wie füge ich der Anwendung verschiedene Rollen hinzu?

Um neue Benutzer hinzuzufügen, führen Sie die folgenden Schritte aus:

1. Klicken Sie im linken Teilfenster auf &quot;Benutzer&quot;, nachdem Sie sich als Administrator angemeldet haben. Sie können Benutzer auch hinzufügen, indem Sie im linken Fensterbereich auf Erste Schritte klicken und auf Benutzer hinzufügen klicken.
1. Um neue Benutzer hinzuzufügen, klicken Sie in der oberen rechten Ecke der Seite auf Hinzufügen .

Standardmäßig wird allen neuen Benutzern die Teilnehmerrolle zugewiesen. Sie können den Teilnehmern Administrator- oder Autorenrollen zuweisen, indem Sie auf **[!UICONTROL Aktionen]** in der oberen rechten Ecke der Seite und wählen Sie **[!UICONTROL Rolle zuweisen]** > **[!UICONTROL Erstellen]** oder **[!UICONTROL Administrator werden]**.

Siehe  [Neue Benutzer hinzufügen](/help/migrated/administrators/feature-summary/add-users-user-groups.md) für detaillierte Informationen zum Hinzufügen von Teilnehmern, Autoren und Administratoren.

+++

+++Wie kann ich ein Hintergrundbild für einen Teilnehmer ändern?

Wenden Sie sich an das Learning Manager-Supportteam.

+++

+++Wo finde ich meine Learning Manager-Konto-ID?

Sie können die Konto-ID von dem Browser abrufen, in dem der Lern-Manager geöffnet ist.

*/app/admin?i_qp_user_id=12761637&amp;**accountId=6849***

+++

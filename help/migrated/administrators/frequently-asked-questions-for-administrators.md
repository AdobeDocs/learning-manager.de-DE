---
jcr-language: en_us
title: Häufig gestellte Fragen für Administratoren
description: Häufig gestellte Fragen für Adobe Learning Manager-Administratoren
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '2398'
ht-degree: 55%

---



# Häufig gestellte Fragen für Administratoren

<table>
 <tbody>
  <tr>
   <td><img src="assets/administrator2.png"></td>
   <td>
    <p>Im Folgenden erhalten Sie Informationen zu den Funktionen und häufig gestellten Fragen zur Administratorrolle in Learning Manager. </p></td>
  </tr>
 </tbody>
</table>

+++Kann ich mehrere Benutzer gleichzeitig hinzufügen? Wenn ja, wie?

Ja, Sie können mit der CSV-Upload-Funktion mehrere Benutzer gleichzeitig hinzufügen. Klicken  [hier](/help/migrated/administrators/add-users-in-bulk.md) für weitere Informationen.

+++

+++Wie kann ich die E-Mail-ID korrigieren, die beim Erstellen der Anmeldung für meine Teilnehmer falsch eingegeben wurde?

Um die Benutzeranmeldung zu korrigieren, müssen Sie eine CSV-Datei in Learning Manager importieren. Als Orientierungshilfe ist am Ende dieser Seite eine CSV-Beispieldatei angehängt. Da die E-Mail-Adresse als eindeutiger Bezeichner für eine Person gilt, kann sie nicht bearbeitet werden. Führen Sie die folgenden Schritte aus:

1. Fügen Sie denselben Benutzer mit der korrekten E-Mail-ID in die CSV-Datei ein und stellen Sie sicher, dass er als Manager anderer Benutzer bleibt, indem Sie seine E-Mail-ID der Spalte &quot;E-Mail des Managers des Mitarbeiters&quot; in der Beispiel-CSV hinzufügen.
1. Fügen Sie der CSV-Datei andere Benutzer Ihres Kontos hinzu, einschließlich sich selbst.
1. Importieren Sie diese Datei in der Admin-App von Learning Manager über „Benutzer“ > „Hinzufügen“ > „CSV importieren“.
1. Ordnen Sie im Dialogfeld auf Anforderung die Felder den entsprechenden CSV-Spalten zu.
1. Klicken Sie auf „Speichern“.

Benutzer sollten auf der Teilnehmerseite hinzugefügt werden.

[Beispiel für Learning Manager CSV.csv](https://helpx.adobe.com/content/dam/help/en/captivate_prime/learning-manager-sample-csv.zip)

+++

+++Wie richte ich Warnungen ein?

In Adobe Learning Manager 1.0 können Sie Benachrichtigungen erstellen. Siehe  [Benachrichtigungsfrage](/help/migrated/administrators/feature-summary/user-notifications.md) für weitere Informationen.

+++

+++Wie füge ich Zertifikate für Kurse hinzu?

Adobe Learning Manager gibt keine Zertifikate für Kurse aus. Der Administrator kann jedoch Abzeichen für die einzelnen Kurse erstellen, indem er im linken Bereich auf die Registerkarte Abzeichen klickt. Wenn ein Administrator die Teilnehmer eines Kurses registriert, kann er dem Kurs zugleich ein Abzeichen zuordnen.

+++

+++Wie importiere ich Signaturen für die Zertifikate?

Adobe Learning Manager umfasst keine Funktion zum Importieren von Unterschriften für Zertifizierungen oder Abzeichen.

+++

+++Kann ich einen Kalender für die Kurse einrichten? Wenn ja, wie?

In der Version Adobe Learning Manager 1.0 gibt es keine Möglichkeit, einen Kalender für die Kurse einzurichten.

+++

+++Wie registriere ich die Teilnehmer auf der Warteliste direkt?

Bei Präsenzkursen mit einer begrenzten Anzahl von Lizenzen werden die Teilnehmer in der Reihenfolge ihrer Registrierung auf eine Warteliste gesetzt. Administratoren können Teilnehmer von der Warteliste auswählen und ihnen Lizenzen zuweisen. Dabei wird die Obergrenze für den jeweiligen Kurs außer Kraft gesetzt. Die Teilnehmer werden für den Kurs registriert, sobald der Administrator ihnen Lizenzen zuweist.

1. Melden Sie sich dafür zuerst als Administrator an und klicken Sie dann im linken Teilfenster auf Kurse.
1. Klicken Sie in der Liste verfügbarer Kurse auf den Namen des Präsenzkurses Ihrer Wahl. Eine neue Seite mit genauen Informationen über den Kurs erscheint.
1. Klicken Sie auf „Warteliste“ im linken Bereich der Seite mit den Kursinformationen. Auf der Seite wird die Warteliste der Teilnehmer angezeigt.
1. Wählen Sie die Teilnehmer aus und klicken Sie auf „Lizenzen zuweisen“, um die Teilnehmer direkt für den Kurs zu registrieren und dabei die Obergrenze außer Kraft zu setzen.

Weitere Informationen finden Sie unter  [Warteliste und Anwesenheit](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md) Funktion.

+++

+++Wie kann ich die Anwesenheit von Teilnehmern am Klassenzimmermodul aufzeichnen?

Sie können die Anwesenheit mit den unten angeführten Schritten erfassen:

1. Klicken Sie auf „Kurse“ im linken Bereich, nachdem Sie sich als Administrator angemeldet haben.
1. Klicken Sie in der Liste verfügbarer Kurse auf den Namen des Präsenzmoduls/-kurses Ihrer Wahl. Es wird eine neue Seite mit ausführlichen Kursinformationen angezeigt.
1. Wählen Sie die Teilnehmer aus und klicken Sie auf „Speichern“, um den Kursabschluss zu vermerken.

Wenn ein Kurs mehrere Module umfasst und der Teilnehmer nur eines davon abgeschlossen hat, können Sie dieses Modul markieren und auf „Speichern“ klicken, um den Abschluss des Teilnehmers zu vermerken. Wenn der Teilnehmer alle Module eines Kurses abgeschlossen hat, können Sie auf die Option „Alle auswählen“ und dann auf „Speichern“ klicken.

Weitere Informationen finden Sie unter  [Warteliste und Anwesenheit](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md) Funktion.

+++

+++Wie schließe ich die L3-Feedbackoption ein?

Beim Registrieren von Kursteilnehmern können Sie L3-Feedback hinzufügen. Um die Aufforderung nach L3-Feedback zu hinzuzufügen, führen Sie die untengenannten Schritte aus:

1. Melden Sie sich dafür zuerst als Administrator an und klicken Sie dann im linken Teilfenster auf „Kurse“. Rechts auf der Seite wird eine Liste aller Kurse angezeigt.
1. Klicken Sie auf die Kurskachel, für die Sie L3-Feedback hinzufügen möchten.
1. Klicken Sie im linken Teilfenster auf „Standardwerte für Instanz“.
1. Klicken Sie auf den Kreis auf der Umschaltfläche neben L3 - Feedback zu Verhaltensänderungen , um ihn auszuwählen.
1. Fügen Sie die L3-Feedbackfrage im Textbereich unter „L3-Frage“ hinzu.

+++

+++Wie beantrage ich die Nominierung des Managers für einen vom Manager nominierten Kurs?

Als Administrator können Sie die Nominierung des Managers für die Kurse beantragen, indem Sie die folgenden Schritte ausführen:

1. Klicken Sie im linken Teilfenster auf „Kurse“.
1. Bewegen Sie die Maus über einen vom Manager nominierten Kurs und klicken Sie auf **[!UICONTROL Managernominierung anfordern]**.

1. Klicken Sie in der Liste der Instanzen auf **[!UICONTROL Von Managern nominiert]** Link gefolgt von **[!UICONTROL Manager hinzufügen]** Link.

1. Fügen Sie den Managernamen und die Anzahl der zugeteilten Lizenzen hinzu. Klicken Sie dann auf das Häkchen, um die Änderungen zu speichern.

Während der Kurserstellung wählt der Autor den Kurstyp „Nominierung durch Manager“.

+++

+++Wie registriere ich einen Teilnehmer für einen bestimmten Kurs?

Führen Sie die unten genannten Schritte aus, um Teilnehmer zu registrieren:

1. Melden Sie sich dafür zuerst als Administrator an und klicken Sie dann im linken Teilfenster auf „Kurse“. Rechts auf der Seite wird eine Liste aller Kurse angezeigt.
1. Wählen Sie den Kurs, dem Sie Teilnehmer hinzufügen möchten, und zeigen Sie mit der Maus darauf.
1. Klicken Sie auf Teilnehmer registrieren und fügen Sie den Namen der Teilnehmer hinzu. **Hinweis:** Sie können einen oder mehrere Teilnehmer gleichzeitig hinzufügen.

+++

+++Wie kann ich Teilnehmern bestimmte Kenntnisse zuweisen?

Weisen Sie Teilnehmern mit den nachfolgenden Schritten Kompetenzen zu:

1. Klicken **[!UICONTROL Kenntnisse]** im linken Bereich, nachdem Sie sich als Administrator angemeldet haben.
1. Wählen Sie eine oder mehrere Qualifikationen aus, indem Sie die Kontrollkästchen für jede Qualifikation aktivieren und dann auf **[!UICONTROL Aktionen]** in der rechten oberen Ecke der Seite.
1. Klicken Sie auf „Benutzern zuweisen“.
1. Beginnen Sie mit der Eingabe des Benutzernamens, wählen Sie ihn aus der Dropdown-Liste aus und klicken Sie auf **[!UICONTROL Speichern]**.

   >[!NOTE]
   >
   >Sie können mehrere Teilnehmer für Qualifikationen registrieren, indem Sie auf Weitere Benutzer hinzufügen klicken und den 4. Schritt wiederholen.

+++

+++Wie kann ich eine Lernprogrammsitzung erstellen?

Um ein Lernprogramm zu erstellen, gehen Sie wie folgt vor:

1. Klicken Sie im linken Teilfenster auf „Lernprogramm“. Die Seite „Lernprogramme“ wird mit einer Liste der vorhandenen Lernprogramme angezeigt.
1. Klicken Sie in der rechten oberen Ecke der Seite auf „Hinzufügen“.\
   Geben Sie den Programmnamen, die Übersicht und die Beschreibung ein und klicken Sie auf &quot;Speichern&quot;.
1. Klicken Sie im linken Teilfenster auf „Kurse“.
1. Fügen Sie einen oder mehrere Kurse hinzu, indem Sie auf die Kachel eines Kurses klicken.

   >[!NOTE]
   >
   >Sie müssen das Lernprogramm veröffentlichen, bevor Sie Teilnehmer oder eine Instanz registrieren.

1. Klicken Sie im linken Teilfenster auf &quot;Instanzen&quot; und dann auf **[!UICONTROL Neue Instanzen hinzufügen]** in der rechten Ecke der Seite, um Details zur Instanz anzuzeigen.

Weitere Informationen zu Lernprogrammen finden Sie unter  [Lernprogrammfunktion.](/help/migrated/administrators/feature-summary/learning-programs.md)

+++

+++Wie kann ich Berichte für alle Rollen ändern oder anpassen?

Um Berichte zu bearbeiten, klicken Sie in der rechten oberen Ecke der Berichte jeweils auf die Dropdownliste. Klicken Sie auf „Speichern“, nachdem Sie mit den Änderungen fertig sind, und zeigen Sie den geänderten Bericht an.

+++

+++Wie ändere ich Kurse, Lernprogramme und das Unternehmensprofil?

Sie können Kurse und Lernprogramme auch bearbeiten, nachdem sie veröffentlicht wurden. Weitere Informationen finden Sie unter  [Kurse](/help/migrated/administrators/feature-summary/courses.md) und  [Lernprogramme](/help/migrated/administrators/feature-summary/learning-programs.md) Hilfeinhalte.

Um das Unternehmensprofil zu ändern, klicken Sie auf **[!UICONTROL Einstellungen]** im linken Bereich und klicken Sie auf **[!UICONTROL Ändern]** oben rechts auf der Seite.

+++

+++Wie suche ich nach den Kursen?

Melden Sie sich dafür zuerst als Administrator an und klicken Sie dann im linken Teilfenster auf „Kurse“. Es wird eine Liste aller verfügbaren Kurse angezeigt.

Für die Suche nach Kursen haben Sie zwei Möglichkeiten:

1. Klicken Sie auf das Suchsymbol in der rechten oberen Ecke. Ein Suchfeld erscheint. Geben Sie den Kursnamen oder beliebige zu Ihren Kursen passende Suchbegriffe ein, um nach diesen zu suchen.
1. Durch Filtern der Kursliste mithilfe der Filter.

Sie können die Kurse nach Status filtern, z. B. &quot;Alle&quot;, &quot;Veröffentlicht&quot; und &quot;Eingestellt&quot;, indem Sie auf jede dieser Optionen klicken. Sie können auch nach Kompetenzen suchen, indem Sie auf &quot;Kompetenzen&quot; klicken und die einzelnen Kompetenzen auswählen.

Anhand Ihrer Auswahl können Sie die gefilterte Kursliste anzeigen und die erforderlichen Kurse auswählen.

+++

+++Kann ich das Design der Anwendung ändern? Wenn ja, wie?

Ja, Sie können die Designs und das Branding der Learning Manager-Anwendung gemäß den Anforderungen Ihres Unternehmens ändern. Ein Set mit fünf repräsentativen Bildern wird bereitgestellt, um Ihre Farbdesignänderungen in der Vorschau anzuzeigen, bevor Sie sie in Ihre Anwendung übernehmen. Navigieren Sie durch diese Bilder, indem Sie auf die Symbole &lt; und > links bzw. rechts neben den Bildern klicken, um sie in der Vorschau anzuzeigen.

Klicken **[!UICONTROL Branding]** im linken Bereich, um Ihren Organisationsnamen zu aktualisieren, die Subdomäne, Protokollstile und Designs zu ändern. Klicken **[!UICONTROL Bearbeiten]** neben jedem dieser Themen, um den Inhalt zu ändern.

Siehe  [Hilfe zu Farbdesigns und Branding](/help/migrated/administrators/feature-summary/themes.md) für weitere Informationen.

+++

+++Wie kann ich Abzeichen für die Kurse einrichten?

1. Klicken Sie im linken Teilfenster auf &quot;Abzeichen&quot;, nachdem Sie sich als Administrator angemeldet haben.
1. Klicken Sie in der rechten oberen Ecke der angezeigten Seite auf „Hinzufügen“.
1. Fügen Sie den Abzeichennamen hinzu.
1. Laden Sie das Abzeichen hoch, indem Sie auf „Abzeichen hochladen“ und auf „Speichern“ klicken.

+++

+++Wie richte ich Gamification-Punkte für die Kurse ein?

Sie können Gamification-Punkte für Teilnehmer festsetzen, indem sie die folgenden Schritte ausführen:

1. Klicken Sie auf Gamification, nachdem Sie sich als Administrator angemeldet haben. Es wird eine Seite mit einer Liste der Stufen „Bronze“, „Silber“, „Gold“ und „Platin“ sowie den jeweils erforderlichen Punkten angezeigt. Eine Liste mit Aufgaben und entsprechenden Punkten ist verfügbar.
1. Um die Punkte einzurichten bzw. zu ändern, klicken Sie neben den einzelnen Aufgaben auf das Bearbeitungssymbol.

Siehe  [Gamification-Funktion](/help/migrated/administrators/feature-summary/gamification.md) für weitere Informationen.

+++

+++Wie erstelle ich Berichte für Manager und Teilnehmer?

Sie können die Berichte mit den unten angeführten Schritten erstellen:

1. Klicken Sie auf „Berichte“ im linken Bereich. Die Seite mit der Berichtzusammenfassung wird angezeigt.
1. Klicken Sie auf der Seite Berichte auf **[!UICONTROL Hinzufügen]** in der oberen rechten Ecke.

   **[!UICONTROL Bericht hinzufügen]** &quot; wird angezeigt.

1. Füllen Sie alle erforderlichen Felder aus und klicken Sie auf &quot;Speichern&quot;.

Nur Administratoren und Manager können Berichte erstellen und anzeigen. Siehe [Berichtfunktion](/help/migrated/administrators/feature-summary/reports.md) für weitere Informationen.

+++

+++Wie ändere ich die Rollen &quot;Teilnehmer&quot;, &quot;Manager&quot; und &quot;Autor&quot;?

Sie können mit Ihrer Kontoanmeldung zu anderen Rollen wie Teilnehmer, Manager und Autor wechseln, ohne dass Sie sich aus Ihrem Konto abmelden müssen.

1. Klicken Sie in der rechten oberen Ecke der Seite auf den Pfeil der Dropdownliste neben Ihrem Profilbild.\
   Ein Popupmenü wird angezeigt.
1. Wählen Sie hier die verfügbaren Rollen, um Zugriff auf das jeweilige Konto zu erhalten.

+++

+++Wie füge ich Benachrichtigungen für Benutzer ein?

Manager, Autoren und Teilnehmer sehen die zu ihren Kursaktivitäten gehörigen Benachrichtigungen. Der Administrator kann die Benachrichtigungen für alle Benutzer mit den nachfolgenden Schritten aktivieren bzw. deaktivieren:

1. Klicken Sie im linken Bereich auf E-Mail-Vorlagen und wählen Sie die Registerkarten Allgemein, Benutzerregistrierungen, Abschlüsse und Feedback aus.
1. Klicken Sie in der Liste unten auf die Ja/Nein-Umschaltflächen neben **jedem Ereignis** und wählen Sie Ja, um die Benachrichtigung zu aktivieren. Klicken Sie auf „Nein“, um das Senden von Benachrichtigungen zu einem bestimmten Ereignis zu deaktivieren.

+++

+++Wie lasse ich eine externe Registrierung für die Kurse zu?

Adobe Learning Manager bietet die Möglichkeit, Mitarbeiter von außerhalb der Abteilung oder externe Mitarbeiter Ihres Unternehmens bei der Anwendung anzumelden.

1. Klicken **[!UICONTROL Benutzer]** im linken Bereich.
1. Klicken **[!UICONTROL Extern]** im linken Bereich.
1. Klicken **[!UICONTROL Hinzufügen]** oben rechts auf der Seite.

   Das Dialogfeld &quot;Benutzer hinzufügen&quot; wird angezeigt.

1. Fügen Sie den Profilnamen, die Manager-E-Mail, zugeteilte Lizenzen und Ablaufinformationen hinzu. Sie können dem externen Profil auch ein Bild hinzufügen.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

Der Administrator kann die Registrierungs-URL kopieren und sie an die externe Gruppe schicken, deren Teilnehmer sich registrieren sollen. Die externen Benutzenden können sich registrieren, sich bei Learning Manager anmelden und auf ihre Kurse zugreifen.

+++

+++Wie füge ich einen Fragebogen für das L1-Feedback hinzu?

Erstellen Sie einen Feedback-Fragebogen, den die Teilnehmer ausfüllen können, nachdem sie die Kurse abgeschlossen haben. Standardmäßig stehen drei Beispielfragen zur Verfügung. Erstellen Sie Fragebogen wie folgt:

1. Klicken Sie im linken Teilfenster auf „Feedback“. Es wird ein Fenster mit einem Feedback-Fragebogen angezeigt.
1. Klicken **[!UICONTROL Bearbeiten]** , um den Fragebogen hinzuzufügen bzw. zu ändern.

Sie können mehrere Fragebogen hinzufügen und diese jeweils nur bei Bedarf einblenden. Um bestimmte Fragen zu aktivieren bzw. zu deaktivieren, klicken Sie auf die dazugehörigen Kontrollkästchen.

+++

+++Wie richte ich die Kenntnisse und Stufen ein?

1. Klicken Sie auf Kompetenzen im linken Bereich des Fensters Administrator.
1. Klicken Sie auf „Hinzufügen“, um neue Kompetenzen hinzuzufügen.
1. Fügen Sie den Kompetenznamen, die Beschreibung und die Credits für die einzelnen Stufen hinzu.

   Standardmäßig ist für jede Kompetenz eine einzige Stufe mit 0 Credits verfügbar.

1. Klicken [!UICONTROL **Stufe hinzufügen**] , um jeder Kompetenz eine neue Stufe hinzuzufügen, und klicken Sie auf Speichern. Sie können bis zu 5 Stufen hinzufügen.

Nach dem Speichern der Kompetenz können Sie keine Stufen mehr entfernen. Administratoren können die Teilnehmer einer bestimmten Kompetenz und Stufe zuweisen.

+++

+++Wie richte ich das Abrechnungssystem für die Kurse meiner Organisation ein?

1. Klicken [!UICONTROL **Abrechnung**] im linken Bereich.

   Rechnungsinformationen werden auf der Seite angezeigt.

1. Klicken Sie auf [!UICONTROL **Abonnieren**] &quot; ändern.
1. Geben Sie im Feld „Teilnehmerpakete“ die Anzahl der Pakete ein, die Sie bestellen möchten, und klicken Sie in der rechten oberen Ecke der Seite auf „Bestellung aufgeben“.

   Wählen Sie die Anzahl der Pakete basierend auf der Anzahl der Teilnehmer in Ihrem Unternehmen aus und geben Sie Ihre Bestellung auf. Bei einem bestellungsorientierten Prozess erreichen Sie uns unter  [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com).

1. Geben Sie Ihre Kontaktdaten ein, wählen Sie den Kreditkartentyp, geben Sie die Details der Kreditkarte ein und klicken Sie auf „Bestellung abschließen“.

Siehe [Abrechnungsmanagement](/help/migrated/administrators/feature-summary/billing-management.md) finden Sie weitere Informationen.

+++

+++Kann ich das Zertifikatdesign anpassen? Wenn ja, wie?

Im Adobe-Lernmanager können Sie Teilnehmer erkennen, indem Sie Abzeichen ausgeben. Weitere Informationen finden Sie unter Abzeichen.  Weitere Informationen finden Sie auch unter Zertifizierungsfunktion.

+++

+++Wie richte ich mein Unternehmensprofil ein?

1. Nachdem Sie sich als Administrator angemeldet haben, klicken Sie auf **[!UICONTROL Informationen zur Organisation]** im linken Bereich.
1. Fügen Sie Unternehmensprofil, Unterdomäne und Logo hinzu, indem Sie auf der Seite auf jede dieser Optionen klicken.

+++

+++Wie füge ich Kurse hinzu?

Um Kurse hinzuzufügen, müssen Sie zur Autorenrolle wechseln. Sie können die Liste der verfügbaren Kurse nur basierend auf ihrem Status anzeigen **[!UICONTROL Vollständig]**, **[!UICONTROL Veröffentlicht]** und **[!UICONTROL Rentner]**.

Um Kurse anzuzeigen, klicken Sie auf **[!UICONTROL Kurse]** im linken Fensterbereich. Siehe  [Erstellen von Kursen](/help/migrated/administrators/feature-summary/courses.md)für weitere Informationen

+++

+++Wie füge ich der Anwendung verschiedene Rollen hinzu?

Um neue Benutzer hinzuzufügen, gehen Sie wie folgt vor:

1. Klicken Sie im linken Bereich auf „Benutzer“, nachdem Sie sich als Administrator angemeldet haben. Sie können Benutzer auch hinzufügen, indem Sie im linken Teilfenster auf „Erste Schritte“ und dann auf „Benutzer hinzufügen“ klicken.
1. Um neue Benutzer hinzuzufügen, klicken Sie in der rechten oberen Ecke der Seite auf „Hinzufügen“.

Standardmäßig wird allen neuen Benutzern die Teilnehmerrolle zugewiesen. Sie können den Teilnehmern Administrator- oder Autorenrollen zuweisen, indem Sie auf **[!UICONTROL Aktionen]** in der oberen rechten Ecke der Seite und wählen Sie **[!UICONTROL Rolle zuweisen]** > **[!UICONTROL Erstellen]** oder **[!UICONTROL Administrator werden]**.

Siehe  [Neue Benutzer hinzufügen](/help/migrated/administrators/feature-summary/add-users-user-groups.md) für detaillierte Informationen zum Hinzufügen von Teilnehmern, Autoren und Administratoren.

+++

+++Wie kann ich ein Hintergrundbild für einen Teilnehmer ändern?

Wenden Sie sich an das Learning Manager-Supportteam.

+++

+++Wo finde ich meine Learning Manager-Konto-ID?

Sie können die Konto-ID über den Browser abrufen, in dem Learning Manager geöffnet ist.

*/app/admin?i_qp_user_id=12761637&amp;**accountId=6849***

+++

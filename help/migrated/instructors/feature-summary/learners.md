---
description: Lesen Sie den folgenden Artikel, um zu erfahren, wie Sie die Teilnehmer verwalten, kursbezogene E-Mail senden und Erinnerungen für Sitzungen senden können.
jcr-language: en_us
title: Verwalten der Teilnehmer für Ihre Sitzung
contentowner: shhivkum
exl-id: 2f4f8589-2350-4683-a141-809084d6309a
source-git-commit: 890315af5dc413c859315dc12d5d9618f67afc8e
workflow-type: tm+mt
source-wordcount: '1898'
ht-degree: 47%

---

# Verwalten der Teilnehmer für Ihre Sitzung

Lesen Sie den folgenden Artikel, um zu erfahren, wie Sie die Teilnehmer verwalten, kursbezogene E-Mail senden und Erinnerungen für Sitzungen senden können.

## Siehe Sitzungen oder Module mit ausstehenden Überprüfungen {#pending}

Als Kursleiter können Sie die Sitzungen oder Module mit ausstehenden Überprüfungen anzeigen.

Auf der Seite &quot;Sitzungen/Module&quot; wird eine Spalte **Überprüfungen ausstehend** mit der Anzahl der ausstehenden Überprüfungen für die entsprechende Sitzung/Aktivität anzeigt.

## Verwalten der Warteliste für die Sitzung {#managewaitlistforyoursession}

Wenn sich die Teilnehmer für Ihr Modul anmelden, können Sie den aktuellen Status der Einschreibung und die Warteliste auf der Seite „Warteliste“ sehen.

1. Wählen Sie in der Kursleiter-App im linken Navigationsbereich „Geplante Sitzungen“ > „Warteliste“.

   Sie können die maximale Anzahl von Lizenzen, die Anzahl der Lizenzen, die gerade verwendet werden und die freien Lizenzen sehen. In der Tabelle werden außerdem Teilnehmer aufgeführt, die sich auf der Warteliste befinden. Sie ist leer, wenn es keine Warteschlangen auf der Warteliste gibt.

   ![](assets/waitlist.png)
   *Teilnehmer auf Warteliste anzeigen*

1. Wählen Sie in der Warteliste-Tabelle den/die Teilnehmer, den/die Sie bestätigten möchten.
1. Wählen Sie „Aktionen“ > „Teilnehmer bestätigen“.

   Die Teilnehmer, die Sie bestätigt haben, werden der Liste „Bestätigte Teilnehmer“ hinzugefügt.

Kursleiter haben die Möglichkeit, die Registrierung von Teilnehmern für Sitzungen aufzuheben. Dadurch wird auch die Registrierung bei den dazugehörigen Lernprogrammen aufgehoben. Wählen Sie die Registerkarte **[!UICONTROL Warteliste]**. Wählen Sie mithilfe der Kontrollkästchen die Teilnehmer aus, deren Registrierung aufgehoben werden soll. Um die Registrierung aufzuheben, wählen Sie **[!UICONTROL Aktionen]** > **[!UICONTROL Registrierung von Teilnehmern aufheben]**.

![](assets/unenroll-learners.png)
*Registrierung der Teilnehmer aufheben*

### Wartelistenbericht

Mit dem neuen **[!UICONTROL Wartelistenbericht]** von Adobe Learning Manager können Kursleiter die Liste der auf die Warteliste gesetzten Teilnehmer für alle Instanzen eines Kurses herunterladen. Kursleiter können über den Abschnitt **[!UICONTROL Warteliste]** auf der Seite **[!UICONTROL Sitzungsübersicht]** auf diesen Bericht zugreifen.

Die folgenden Spalten sind im Bericht &quot;Warteliste&quot; verfügbar:

* Kursname
* Instanzname
* Instanzen-ID
* Instanzenstatus
* Benutzername
* E-Mail
* Eindeutige ID des Benutzers
* Registriert am (UTC-Zeitzone)
* Status
* Warteliste Nummer
* Limit für Warteliste
* Maximale Anzahl Lizenzen

So laden Sie den Bericht im Abschnitt &quot;Kursleiter&quot; herunter:

1. Melden Sie sich als **[!UICONTROL Kursleiter]** an.
2. Wählen Sie eine beliebige Sitzung auf der Startseite aus.
3. Wählen Sie die Option **[!UICONTROL Warteliste]** auf der Seite **[!UICONTROL Sitzungsübersicht]** aus.
4. Wählen Sie **[!UICONTROL Aktionen]** > **[!UICONTROL Bericht exportieren]**, um den Bericht **[!UICONTROL Warteliste]** herunterzuladen.

## Vermerken der Teilnahme an Ihrer Sitzung {#markattendanceforyoursession}

Sie können die Anzahl der bestätigten Teilnehmer, die an der Sitzung teilnehmen, deren Namen, deren Teilnahmestatus sowie andere Details auf der Seite „Teilnehmer“ sehen.

1. Klicken Sie im linken Navigationsbereich auf „Geplante Sitzungen“ > „Teilnehmer“.
1. Wählen Sie den/die Teilnehmer aus der Teilnehmerliste aus und führen Sie einen der folgenden Schritte aus:

   * Um die Teilnahme zu vermerken, klicken Sie auf „Aktionen“ > „Teilnahme vermerken“. Sobald der Status als „Teilgenommen“ vermerkt wurde, können Sie den Status nicht mehr ändern.
   * Um den Status als „Nicht-teilgenommen“ zu vermerken, klicken Sie auf „Aktionen“ > „Nicht-teilgenommen“.
   * Um einen Teilnehmer aufgrund einer Absage oder aus anderen Gründen zu löschen, klicken Sie auf &quot;Aktionen&quot; > &quot;Teilnehmer löschen&quot;.

   Ein Teilnehmer kann ein Modul erst abschließen, wenn der Teilnahmestatus „Teilgenommen“ lautet.

   ![](assets/markattendance.png)
   *Anwesenheit der Teilnehmer markieren*

### QR-Codes für Teilnehmerregistrierung und Teilnahme herunterladen

Kursleiter können QR-Codes für ihre zugewiesenen Sitzungen herunterladen, damit sich Teilnehmer für eine Kursinstanz anmelden und die Teilnahme oder den Abschluss durch Scannen des QR-Codes markieren können.

Dadurch können Kursleiter die Teilnahme an Sitzungen unabhängig verwalten, ohne dass Administratorunterstützung erforderlich ist.

Die folgenden Schritte sind für beide geeignet:

* Sitzungen im Klassenzimmer
* Online-Lernumgebungen

Für eine Sitzung im physischen Klassenzimmer müssen Sie als Kursleiter den richtigen QR-Code generieren und ihn in den Klassenzimmer einfügen (oder ihn umgehen), in dem die Teilnehmer an der Sitzung teilnehmen, damit sie den QR-Code scannen und ihre Registrierung, Teilnahme oder beides abhängig vom QR-Code markieren können.

Bei einer Online-Klassenzimmersitzung können Sie als Kursleiter den generierten QR-Code per E-Mail, über ein Messaging-System oder auf andere Weise senden, sodass die Teilnehmer den QR-Code scannen und ihre Registrierung, Teilnahme oder beides je nach QR-Code markieren können.


#### QR-Codes für eine Sitzung herunterladen

1. Melden Sie sich mit der Rolle **Kursleiter** bei Adobe Learning Manager an.
2. Wechseln Sie zum **Kursleiter-Dashboard**.
3. Öffnen Sie die relevante **Kursinstanz**.
4. Wählen Sie die Registerkarte **Sitzungen** aus.
5. Wählen Sie eine Sitzung aus, die Ihnen zugewiesen wurde.
6. Wählen Sie **Session QR Code**.
   ![](assets/instructor-QR-code.png)

Sie können die folgenden QR-Codes herunterladen:

* **QR-Registrierungscode** - ermöglicht Teilnehmern die Registrierung in der Kursinstanz
* **QR-Code für Anwesenheit** - markiert die Anwesenheit für die Sitzung
* **Registrierung + Teilnahme-QR-Code** - registriert Teilnehmer und markiert die Teilnahme in einem einzigen Scan.

Der QR-Code wird als PDF heruntergeladen und kann digital freigegeben oder während der Sitzung angezeigt werden.

#### Was passiert, wenn Teilnehmer den QR-Code scannen?

* Teilnehmer scannen den QR-Code mit einem Mobilgerät.
* Adobe Learning Manager validiert den Teilnehmer und die Sitzung.
* Basierend auf dem QR-Codetyp:
   * Teilnehmer sind für die Kursinstanz registriert oder
   * Anwesenheit und Abschluss werden für die Sitzung aufgezeichnet.

Alle Aktualisierungen werden automatisch in den Teilnehmerdatensätzen, Transkripten und Berichten widergespiegelt.

#### Anmerkungen

* QR-Codes sind nur für Kursleiter verfügbar, die der Sitzung zugewiesen sind.
* Die für den Kurs und die Sitzung konfigurierten Regeln für Registrierung, Teilnahme und Abschluss gelten weiterhin.
* Bestehender Teilnehmerfortschritt und Berichterstellungs-Workflows bleiben unverändert.

#### Anwendungsszenarien

* Unternehmen, die große Mengen an Vor-Ort-Sitzungen durchführen (z. B. Produktschulungen für Fachkräfte), können es den Kursleitern ermöglichen, sitzungsspezifische QR-Codes zu drucken, die die Teilnahme mit einem Scan registrieren und markieren.

* Bei Schulungen für Einzelhandel, Fertigung und Gesundheitswesen, bei denen Teilnehmer oft direkt vom Boden aus oder ohne vorherige Anmeldung an Sitzungen teilnehmen, kann ein QR-Code &quot;Anmeldung + Teilnahme&quot; an der Tür platziert werden. Dies ermöglicht es Teilnehmern, ihre Anmeldung und Anwesenheit über ihre Telefone selbst zu bearbeiten.

* Schulungen für Partner oder Kunden ermöglichen es dem Trainer vor Ort, sich einfach an Änderungen im Raum, zusätzliche Sitzungen oder zusätzliche Teilnehmer anzupassen, ohne den Administrator um neue QR-Codes bitten zu müssen.

### Kalendereinladungen

* Wenn sich ein Teilnehmer oder ein Kursleiter in einem Klassenzimmer oder einer virtuellen Klassenzimmersitzung registriert hat, sendet der Lern-Manager eine Kalendereinladung (ICS-Datei).
* Die Kalendereinladung umfasst:
   * Datum und Uhrzeit der Sitzung
   * Sitzungsdetails
   * **Link zur direkten Sitzung** in der Kalenderbeschreibung

Die Teilnehmer können die Kalenderveranstaltung öffnen und direkt aus ihrem Kalender an der Sitzung teilnehmen.

#### An einer Sitzung von Gmail teilnehmen

1. Öffnen Sie **Google-Kalender**.
2. Wählen Sie das Sitzungsereignis aus.
3. Klicken Sie in den Ereignisdetails auf den Link **Sitzung beitreten**.
4. Die Sitzung wird direkt in Adobe Learning Manager oder dem konfigurierten Tool für virtuelle Klassenzimmer geöffnet.

Sie müssen nicht die ursprüngliche E-Mail öffnen, um auf den Sitzungslink zuzugreifen.

#### Teilnahme an einer Sitzung von anderen Kalender-Clients

Der Sitzungslink ist im Kalenderereigniskörper enthalten und kann abgerufen werden über:

* Microsoft Outlook
* Apple Calendar
* Andere Kalenderanwendungen, die ICS-Dateien unterstützen

#### Anmerkungen

* Kalendereinladungen werden automatisch vom Learning Manager generiert.
* Die Zeitzoneninformationen in der Kalendereinladung werden basierend auf der ausgewählten Zeitzone des Teilnehmers angepasst.
* Diese Verbesserung gilt für neu generierte Kalendereinladungen.
* Administratoren oder Kursleiter müssen keine zusätzliche Konfiguration vornehmen.


## Als erfolgreich markieren

Kursleiter können den Erfolgsstatus jedes Teilnehmers direkt auf der Teilnehmerseite als bestanden oder abgelehnt markieren. Mit dieser Funktion können Kursleiter das Ergebnis von Sitzungen im Klassenzimmer oder virtuellen Klassenzimmer basierend auf der Leistung der Teilnehmer genau aufzeichnen.

So markieren Sie den Erfolg für Teilnehmer:

1. Melden Sie sich bei Adobe Learning Manager als Kursleiter an.
2. Wählen Sie im linken Navigationsbereich **[!UICONTROL Bevorstehende Sitzungen]** aus.
3. Wählen Sie **[!UICONTROL Teilnehmer]** aus.
4. Wählen Sie die Teilnehmer aus und wählen Sie dann **[!UICONTROL Aktionen]**.
5. Wählen Sie eine der folgenden Optionen aus, um den Erfolg für die ausgewählten Teilnehmer zu markieren:

   * **[!UICONTROL Als anwesend markieren und Bestanden]**: Als bestanden markierte Teilnehmer haben das Modul erfolgreich abgeschlossen.
   * **[!UICONTROL Anwesend markieren und fehlgeschlagen]**: Die als &quot;Nicht bestanden&quot; markierten Teilnehmer haben das Modul abgeschlossen, aber nicht bestanden.

   ![Das Dropdown-Menü &quot;Aktionen&quot;, in dem die Optionen &quot;Teilgenommen und bestanden markieren&quot; und &quot;Teilgenommen und nicht bestanden markieren&quot; für Kursleiter hervorgehoben werden, um den Erfolgsstatus jedes Teilnehmers festzulegen](/help/migrated/instructors/feature-summary/assets/mark-success-instructor.png)
   _Teilnehmerseite, auf der das Menü &quot;Aktionen&quot; mit markierten Optionen &quot;Teilgenommen markieren&quot; und &quot;Teilgenommen markieren&quot; und &quot;Teilgenommen markieren&quot; und &quot;Fehlgeschlagen&quot; für die Aufzeichnung von Teilnehmerergebnissen markiert ist_

6. Wählen Sie in der Bestätigungsmeldung **[!UICONTROL Ja]** aus.

## Senden Sie eine E-Mail an die Teilnehmer {#sendemailstolearners}

Sie können die E-Mails an bestimmte oder alle Teilnehmer der Sitzung senden. Die Funktion „E-Mail senden“ ist sehr nützlich, wenn Sie die Teilnahme von Teilnehmern bestätigen möchten oder wenn Sie Informationen zu den Sitzungen senden möchten. Sie können auch die Option „E-Mail an alle senden“ nutzen, um Aufgaben- oder Sitzungsmaterial per E-Mail oder allgemeine Informationen an alle Teilnehmer zu schicken.

Um E-Mails von der Teilnehmerseite in der Kursleiter-App an die Teilnehmer zu senden, führen Sie einen der folgenden Schritte aus:

* Um E-Mails an bestimmte Teilnehmer der Sitzung zu senden, wählen Sie den Teilnehmer aus und klicken Sie auf „Aktionen“ > „Senden“ > „E-Mail an Ausgewählte“.
* Um eine E-Mail an alle Teilnehmer zu senden, um Kursmaterial oder eine Aufgabe zu senden, klicken Sie auf „Aktionen“ > „E-Mail an alle senden“.

## Einladungsantworten erfassen

Kursleiter können die Einladungsantworten von Teilnehmern nur erfassen, wenn die Option **[!UICONTROL Antwort einladen]** vom ACAP-Administrator aktiviert wurde. Um diese Funktion zu aktivieren, müssen Administratoren das Supportteam unter [learningmanagersupport@adobe.com](mailto:learningmanagersupport@adobe.com) kontaktieren.

Anschließend können Sie Einladungsantworten im Abschnitt **[!UICONTROL Teilnehmer]** anzeigen. Gehen Sie zu einer beliebigen Sitzung, wählen Sie **[!UICONTROL Teilnehmer]** aus und wählen Sie die Einladungsantwort aus dem Dropdown-Menü aus.

![](assets/invitation-status.png)

## Exportieren der Teilnehmerliste {#exportinglearnerslist}

Als Kursleiter können Sie die Teilnahme für alle Ihre Teilnehmer ganz einfach vermerke, indem Sie die Liste der eingeladenen Teilnehmer als PDF exportieren. Die Funktion zum Exportieren der Teilnehmerliste finden Sie auf der Seite „Teilnehmer“ im linken Teilfenster. Klicken Sie auf „Aktionen“ > „Teilnehmerliste exportieren (PDF)“.

Nachdem die Teilnehmerliste für Ihre Sitzung bestätigt wurde, können Sie die Liste als PDF-Datei exportieren. In dieser druckerfreundlichen PDF-Datei werden die Teilnehmer als Tabelle angezeigt. Sie können dann die Teilnahme vermerken oder Punktzahlen bereitstellen und Hinweise für Teilnehmer in einer PDF erstellen oder vergeben.

Achten Sie auf den QR-Code in der oberen rechten Ecke dieses PDF-Dokuments. Mit dieser Funktion können einzelne Teilnehmer den Code mithilfe der Learning Manager-Mobilanwendung scannen, damit Teilnehmer ihre Teilnahme vermerken können.

![](assets/exportpdf.png)
*QR-Code scannen, um Anwesenheit zu vermerken*

## Übertragungen genehmigen oder ablehnen {#approveorrejectsubmissions}

Wenn Teilnehmer Dokumente wie Aufgaben, Berichte oder Bewertungen für Ihre Sitzung hochgeladen haben, können Sie die Dokumente auf der Seite „Übertragungen“ sehen. Sie können die Materialien für die Bewertung des Teilnehmers verwenden und die Übermittlung genehmigen oder. ablehnen.

1. Klicken Sie im linken Bereich entweder auf „Bevorstehende Sitzungen“ oder auf „Letzte Sitzungen“, basierend auf den bereits geplanten Sitzungen.
1. Klicken Sie auf den Kurs, für den Sie die Übertragungen sehen möchten.

   Klicken Sie im linken Teilfenster auf „Übertragungen“.

1. Sie können die Übertragungen von Teilnehmern für diese Sitzung, die Sie ausgewählt haben, ansehen. Wählen Sie die Übertragung aus, die Sie genehmigen oder ablehnen möchten und klicken Sie auf „Genehmigen“ oder „Ablehnen“.

   Der Status der Übertragungen ändert sich je nach Aktion auf „Genehmigen“ oder „Ablehnen“.

## Konfigurierungserinnerungen für Ihre Sitzung {#configureremindersforyoursession}

1. Klicken Sie im linken Teilfenster auf „Bevorstehende Sitzungen“.
1. Klicken Sie auf den Kurs, für den Sie die Erinnerungen festlegen möchten. Klicken Sie im linken Teilfenster auf „Erinnerungen“.
1. Klicken Sie auf der Kachel „Erinnerung auf „Erinnerung festlegen“.

   ![](assets/setreminder.png)
   *Konfigurieren Sie Erinnerungen für Ihre Sitzung*

1. Führen Sie folgende Schritte aus:

   * Legen Sie im Dialogfenster „Erinnerungseinstellungen“ die Option fest, wann die Erinnerung an die Teilnehmer gesendet werden soll: Vor dem Termin, Zum Termin oder Nach dem Termin.
   * Legen Sie im Feld „Tage vor dem Termin“ die Anzahl der Tage vor dem Termin fest, wann Sie die Erinnerung an die Teilnehmer senden möchten.
   * Legen Sie die Wiederholung für Ihre Erinnerung fest.

   ![](assets/remindersettings.png)
   *Erinnerungseinstellungen anzeigen*

1. Führen Sie einen der folgenden Schritte aus:

   * Speichern Sie die Erinnerung, indem Sie das Kontrollkästchen anhaken.
   * Klicken Sie auf das Kreuz, um die Erinnerung abzubrechen.

   Eine automatisierte Kurserinnerung wird an alle Teilnehmer zu dem Datum gesendet, das Sie in den Einstellungen für Ihre Erinnerungen angegeben haben.

   Wenn Sie bereits Erinnerungen zu Ihren Sitzungen festgelegt haben, können Sie diese in den Kacheln „Vorhandene Erinnerungen“ sehen. Darüber hinaus können Sie zusätzliche Erinnerungen Ihren vorhandenen Erinnerungen hinzufügen.

   Um eine vorhandene Erinnerung zu löschen, klicken Sie auf die Erinnerung. Klicken Sie im angezeigten Popup-Menü auf das Symbol „Löschen“ (Papierkorbsymbol), um die Erinnerung zu löschen.

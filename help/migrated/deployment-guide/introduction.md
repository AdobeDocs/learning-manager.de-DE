---
jcr-language: en_us
title: Implementierungshandbuch für Learning Manager
description: Learning Manager ist ein Learning Management System (LMS), mit dem Schulungsexperten ansprechende und verfolgbare Lernmaterialien bereitstellen können, die zu den Anforderungen und Zielen eines Unternehmens beitragen können. Mit dem Lern-Manager können Kursleiter oder Manager Kurse und andere Lernobjekte in einer bestimmten Reihenfolge für Teilnehmer zuweisen.
contentowner: shhivkum
preview: true
source-git-commit: 2317aa899a82abe24d38c4e40a06df3646fde310
workflow-type: tm+mt
source-wordcount: '3246'
ht-degree: 0%

---



# Implementierungshandbuch für Learning Manager

## Einführung {#introduction}

Learning Manager ist ein Learning Management System (LMS), mit dem Schulungsexperten ansprechende und verfolgbare Lernmaterialien bereitstellen können, die zu den Anforderungen und Zielen eines Unternehmens beitragen können. Mit dem Lern-Manager können Kursleiter oder Manager Kurse und andere Lernobjekte in einer bestimmten Reihenfolge für Teilnehmer zuweisen. Dieses Tool bietet außerdem mehrere leistungsstarke Funktionen wie einen Multiformat-Fluidic Player, Gamification, Abzeichen und ein benutzerfreundliches Teilnehmer-Dashboard. Um alle diese Funktionen nutzen zu können, ist es jedoch wichtig, zunächst Learning Manager zu konfigurieren und einzurichten.

Dieses Handbuch enthält schrittweise Anweisungen zum Einstieg in Learning Manager. Dieses Dokument enthält auch detaillierte Informationen zur Konfiguration und Einrichtung. Lesen Sie weiter, um zu erfahren, wie Sie mit Learning Manager beginnen.

## Für wen ist dieser Leitfaden gedacht? {#whoisthisguideintendedfor}

Als Learning Manager-Benutzer können Sie den Hut eines Administrators, Autors, Kursleiters, Managers oder Teilnehmers tragen. Dieses Handbuch richtet sich an Benutzer, die wahrscheinlich an der Einrichtung eines LMS für ein Unternehmen oder einen Kunden beteiligt sind:

* **IT-Administrator** - Als IT-Administrator können Sie den Learning Manager aktivieren oder in Ihr Unternehmen integrieren. Ein IT-Administrator kann auch einzelne oder mehrere Benutzer hinzufügen und die Rolle eines Integrationsadministrators oder eines Administrators übernehmen, der den Learning Manager mit Anwendungen von Drittanbietern integriert.
* **Autor** - Als Autor von Learning Manager können Sie Lerninhalte erstellen, die für die Lernanforderungen eines Unternehmens erforderlich sind. Ein Autor ist an der Erstellung des grundlegenden Inhalts beteiligt, der in den Lern-Manager hochgeladen wird.

* **Learning Manager-Administrator** - Ein Learning Manager-Administrator führt die Konfigurations- und Einrichtungsaktivitäten im Zusammenhang mit der Anwendung durch. In einigen Unternehmen kann ein IT-Administrator auch die Rolle eines Learning Manager-Administrators spielen.

## Erste Schritte mit der Bereitstellung von Learning Manager {#getstartedwithcaptivateprimedeployment}

Nachdem Sie Learning Manager gekauft haben, aktivieren Sie Ihr Learning Manager-Konto mit dem erhaltenen Lizenzschlüssel. Fahren Sie mit den folgenden Konfigurationen fort, wie in der folgenden Abbildung dargestellt:

![](assets/getting-started-withcaptivateprime.jpg)

## Konfigurieren Sie Ihre Site im Learning Manager {#configureyoursiteincaptivateprime}

Bevor Sie mit dem Hinzufügen und Implementieren von Lernobjekten in Learning Manager beginnen, sind einige Schlüsselkonfigurationen erforderlich. Beginnen Sie mit der Konfiguration Ihrer Site für Ihre Organisation. Die Standortkonfiguration umfasst die folgenden Schritte:

* Einrichten von Branding und Logo für Ihre Organisation
* Konfigurieren von E-Mail-Vorlagen
* Grundlegende Kontoeinstellungen konfigurieren
* Feedbackeinstellungen konfigurieren
* Konfigurieren der Einstellungen im Teilnehmer-Dashboard

### Einrichten von Branding und Logo {#setupbrandingandlogo}

Als Administrator können Sie das Branding und die Designs so festlegen, dass sie den Branding-Anforderungen Ihrer Organisation entsprechen. Gehen Sie wie folgt vor, um das Branding und die Designs für Ihre Website festzulegen:

### Logo und Banner festlegen: {#settingthelogoandbanner}

Verwenden Sie die Logo- und Banner-Einstellungen, um das Logo Ihres Unternehmens in Learning Manager anzuzeigen. Konfigurieren Sie die Branding-Optionen, um die Domäne des Unternehmens in der URL festzulegen, den Namen des Unternehmens anzuzeigen und Farbschemata anzuzeigen, die dem Branding des Unternehmens entsprechen. So konfigurieren Sie die Branding-Einstellungen:

* Melden Sie sich bei Ihrem Learning Manager-Konto als Administrator an.
* Klicken Sie im linken Teilfenster auf **Branding**.
* Auf der Seite Branding können Sie die folgenden Optionen konfigurieren, indem Sie auf **Bearbeiten** für die Option, die Sie ändern möchten:

   * **Name der Organisation** : Der Wert, den Sie hier angeben, bestimmt den Namen, der auf dem Banner auf jeder Seite Ihrer Site angezeigt wird.
   * **Unterdomäne**: Dieser Wert bestimmt die URL für Ihre Site.
   * **Logostile**: Das Bild in diesem Feld wird als Logo in der oberen rechten Ecke jeder Seite angezeigt. Hier können Sie auswählen, ob nur das Logo oder der Name Ihres Unternehmens oder das Logo und der Name des Unternehmens angezeigt werden sollen.

![](assets/setting-the-themesforyoursite.png)

>[!NOTE]
>
>Sie können den Namen und das Logo nur mithilfe des Brandings konfigurieren. Die Position des Logos oder des Bildes kann nicht geändert werden.

***Learning Manager unterstützt die folgenden Dateiformate für Logobilder: .png, .jpeg, .jpg, .gif, .bmp***

### Festlegen der Designs für Ihre Site {#settingthethemesforyoursite}

Mit dem Learning Manager können Sie das Erscheinungsbild Ihrer Site mithilfe von Designs ändern. Die Anwendung bietet die folgenden Farbschemata zur Auswahl:

* Prime-Standard
* Kieselsteine
* Fasching
* Herbst
* Winterhimmel

Sie können eines der Farbschemata auswählen, die mit Ihrem Unternehmensbranding übereinstimmen.

1. Klicken Sie im linken Navigationsbereich des Learning Manager auf **[!UICONTROL Branding]**.
1. Im Dialogfeld &quot; **Designs** klicken Sie auf **[!UICONTROL Bearbeiten]**. Mit der Anwendung können Sie ein neues Design auswählen. Wenn Sie ein Design auswählen, können Sie sofort die Farbschemata sehen, die für die wichtigsten Elemente der Benutzeroberfläche verwendet werden.

   ![](assets/setting-the-themesforyoursite.png)

1. Darüber hinaus können Sie die **Farbe für oberen Balken**, **Akzentfarbe** und den Katalog **Seitenleistenhelligkeit**.  Für diese wichtigen Elemente der Benutzeroberfläche können Sie Ihre eigenen Markenfarben verwenden.
1. Um die Werte auf das Standardfarbschema für Ihr Design zurückzusetzen, klicken Sie auf **[!UICONTROL Design zurücksetzen]**. Die Farben für die wichtigsten Elemente der Benutzeroberfläche werden auf die Standardoptionen für das ausgewählte Design festgelegt.
1. Nachdem Sie das Design ausgewählt haben, klicken Sie auf **[!UICONTROL Hinweise anzeigen]** , um die Beschriftungen oder Hinweise in der Vorschau anzuzeigen.

   ![](assets/setting-the-themesforyoursite-step5.png)

   Eine Diashow mit mehreren Bildern im Katalog **Designs** Abschnitt. Mit dieser Diashow können Sie sofort eine Vorschau des Designs oder Farbschemas anzeigen. Sie können eine Vorschau der ausgewählten Seiten anzeigen, z. B. Startseite, Teilnehmer-Dashboard usw.

1. Wenn Sie die Änderungen in einem Browser in der Vorschau anzeigen möchten, klicken Sie auf **[!UICONTROL Live-Vorschau]**. Es wird ein Popupfenster mit einer Live-Designvorschau angezeigt, in dem Sie entweder das Farbschema ändern oder die Standardoptionen beibehalten können. Um eine Vorschau Ihrer Optionen in einem Browser anzuzeigen, klicken Sie auf **[!UICONTROL Vorschau]** in diesem Popup-Fenster.

   ![](assets/setting-the-themesforyoursite-step6.png)

1. Die ausgewählten Optionen werden vorübergehend auf Ihre Site angewendet. Wenn Sie das ausgewählte Design und die Farbeinstellungen speichern möchten, klicken Sie auf **[!UICONTROL Anwenden]**.
1. Nachdem Sie ein Design ausgewählt und angewendet haben, klicken Sie auf ****[!UICONTROL Speichern]**** , um Ihre Auswahl zu speichern.

## Konfigurieren von E-Mail-Vorlagen {#configureemailtemplates}

Als Administrator sollten Sie als Nächstes E-Mail-Vorlagen für verschiedene Ereignisse konfigurieren. Sie können E-Mail-Vorlagen, die an Benutzer gesendet werden sollen, aktivieren, deaktivieren und ändern. Es gibt drei Hauptkategorien von E-Mail-Vorlagen:

* Allgemeine E-Mail-Vorlagen: Diese E-Mails werden für generische Ereignisse ausgelöst. Zum Beispiel eine Willkommensbenachrichtigung, wenn sich ein Benutzer zum ersten Mal anmeldet.
* E-Mail-Vorlagen, die mit einem Lernobjekt oder einer Aktivität verknüpft sind: Diese E-Mails werden an Teilnehmer, Autoren oder Manager gesendet, wenn es eine Lernaktivität gibt. Beispiel: E-Mails, die nach der Kursregistrierung, der Teilnahme am Klassenzimmer, dem Kursabschluss usw. ausgelöst werden.
* Erinnerungen und Updates: Diese E-Mails werden ausgelöst, wenn Benutzer Updates oder Erinnerungen für ein Ereignis benötigen. Beispiel: Ein Teilnehmer erhält eine Erinnerung für einen bevorstehenden Kurs oder ein Administrator erhält eine E-Mail-Benachrichtigung für einen freigegebenen Bericht.

Sie können diese E-Mail-Benachrichtigungen über das Administrator-Dashboard aktivieren und konfigurieren. Um zu erfahren, wie Sie E-Mail-Vorlagen festlegen, führen Sie die folgenden Schritte aus:

1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL ** E-Mail-Vorlagen **.]**
1. Klicken Sie auf eine der folgenden Registerkarten:**[!UICONTROL ** Allgemein **/** Lernaktivität **/** Erinnerungen und Updates **.]** Nehmen wir an, Sie klicken auf **[!UICONTROL ** Lernaktivität **.]**
1. Klicken Sie auf die Umschaltfläche für die Aktivität, für die Sie eine E-Mail auslösen möchten. In diesem Beispiel nehmen wir an, dass Sie auf **[!UICONTROL ** Lernprogramm - Registriert von Administrator/Manager **.]**

   ![](assets/configure-email-templates-step3.png)

   Das System zeigt die Popup-Meldung &quot;Erfolgreich aktiviert&quot; an. Wenn ein Manager oder Administrator einen Teilnehmer für einen Kurs registriert, erhält der Teilnehmer jetzt eine E-Mail von diesem Learning Manager-Konto.

1. Sie können die Standard-E-Mail-Vorlage ändern. Klicken Sie dazu auf die Veranstaltung. Klicken Sie in diesem Beispiel auf **[!UICONTROL Lernprogramm - Registriert von Administrator/Manager.]**
1. Im Dialogfeld &quot; **[!UICONTROL Vorlagenvorschau]** ein Popupfenster öffnen, werden zwei Registerkarten angezeigt: [!UICONTROL Teilnehmer] und [!UICONTROL Manager].

   ![](assets/configure-email-templates-step5.png)

   Klicken Sie für jede dieser Registerkarten auf den E-Mail-Text, um den Inhalt zu ändern. Klicken Sie zum Speichern der Änderungen an der E-Mail-Vorlage auf **[!UICONTROL Speichern]**.

   Wenn sich ein Teilnehmer jetzt für einen Kurs vom Manager oder Administrator registriert, erhalten der Teilnehmer und sein Manager eine E-Mail-Benachrichtigung.

   ***Hinweis: Die Änderungen gelten nur für die E-Mail-Vorlage, die mit dem ausgewählten Ereignis verknüpft ist.***

1. Beachten Sie, dass Sie die Konto-URL oder die Signatur in der E-Mail-Vorlage nicht ändern konnten. Um die **[!UICONTROL Konto-URL]** oder **[!UICONTROL Unterschrift]** auf die Schaltfläche **[!UICONTROL Einstellungen]** &quot; ändern. Auf dieser Registerkarte können Sie das E-Mail-Banner, die E-Mail-Signatur und die Konto-URL ändern.

   Der Konto-URL-Link wird in allen E-Mails unmittelbar vor der Signatur angezeigt. Geben Sie die gewünschte URL ein und klicken Sie auf **[!UICONTROL Speichern]**. Diese URL ist nur für interne Benutzer sichtbar.

   Bei einem E-Mail-Banner können Sie die Farbe des Banners ändern, indem Sie  **[!UICONTROL ** Banner-Hintergrund **.]** Sie können auch ein benutzerdefiniertes Bild als Banner verwenden, indem Sie die Option **[!UICONTROL Benutzerdefiniertes Bild]** aus. Klicken  **[!UICONTROL Speichern]** nachdem Sie die Änderungen vorgenommen haben.

   ***Hinweis: Die benutzerdefinierte Bildgröße für das E-Mail-Banner muss 1240x200px betragen. Bilder, die größer als die empfohlene Größe sind, werden beschnitten.***

   ***Learning Manager unterstützt nur die Dateitypen .jpg, .jpeg und .png für E-Mail-Banner.***

   ![](assets/configure-email-templates-step6.png)

1. Sie können auch Optionale Manager-E-Mails aktivieren. Wenn Sie die Option **[!UICONTROL Aktivieren]** Wenn ein direkter Bericht eine E-Mail von diesem Prime-Konto erhält, wird der Manager auch in die Mailing-Liste aufgenommen.

   ***Hinweis: Die Einstellungen auf dieser Registerkarte gelten global für alle Vorlagen.***

### Konfigurieren von E-Mail-Vorlagen für ein Lernobjekt {#configureemailtemplatesforalearningobject}

Neben der Festlegung von E-Mail-Vorlagen auf globaler Ebene können Sie als Administrator auch E-Mail-Vorlagen für ein bestimmtes Lernobjekt konfigurieren. In diesem Fall gelten alle Änderungen, die Sie an der E-Mail-Vorlage vornehmen, nur für dieses Lernobjekt.

Diese Option ist auch für Autoren verfügbar, wenn Autoren ein Lernobjekt einrichten.

E-Mail-Vorlagen für ein Lernobjekt konfigurieren:

1. Klicken Sie auf den Kurs, das Lernprogramm oder die Zertifizierung, für den bzw. die Sie die E-Mail-Vorlage konfigurieren möchten.
1. Klicken Sie im linken Teilfenster auf **[!UICONTROL ** E-Mail-Vorlagen **.]** Das System zeigt eine ****[!UICONTROL Vorlagenvorschau]**** ein Popupfenster.
1. Ändern Sie den Betreff oder den Text der E-Mail-Vorlage und klicken Sie auf **[!UICONTROL **Speichern**]**um die Änderungen zu übernehmen.
1. Um die Änderungen abzubrechen, klicken Sie auf **[!UICONTROL ** Auf Original zurücksetzen **.]**

### E-Mail-Empfang für Benutzer beschränken {#restrictusersfromreceivingemails}

Als Administrator können Sie auswählen, wer E-Mails vom Learning Manager erhält und wer nicht. Sie können dies mit dem Dialogfeld &quot; ****[!UICONTROL Eingeschränkter Benutzer]**** in der ****[!UICONTROL Einstellungen]** **tab. Benutzer können dieser Liste mit ihrem Namen, ihrer E-Mail-ID oder ihrer eindeutigen Benutzer-ID hinzugefügt werden. Die Benutzer, die unter dieser Option aufgeführt sind, erhalten keine E-Mail-Kommunikation vom Learning Manager.

## Kontoeinstellungen konfigurieren {#configureyouraccountsettings}

Mit dem Lern-Manager können Sie einige Kontoeinstellungen konfigurieren, z. B. grundlegende Einstellungen, Feedbackeinstellungen, allgemeine Einstellungen und Einstellungen für das Teilnehmer-Dashboard. Die folgenden Verfahren erläutern Ihnen, wie diese Einstellungen jeweils konfiguriert werden:

### Grundlegende Einstellungen konfigurieren {#configurebasicsettings}

1. Klicken Sie auf der Lern-Manager-Startseite auf ****[!UICONTROL Einstellungen]****. Standardmäßig zeigt das System die Seite &quot;Grundlegende Informationen&quot; mit den Feldern für die Standardsprache und den Speicherort an.
1. Klicken ****[!UICONTROL Ändern]**** in der oberen rechten Ecke der Seite, um die einfachen Informationen zu bearbeiten.
1. Konfigurieren Sie die folgenden Optionen:

   * **Land**: Wählen Sie das Land aus diesem Dropdownfeld aus.
   * **Zeitzone**: Legen Sie die entsprechende Zeitzone für Ihren Standort fest.
   * **Gebietsschema**: Wählen Sie die gewünschte Sprache aus. Wenn Sie die Sprache in diesem Feld ändern, wird die Änderung auf alle Benutzer angewendet, die diese Anwendung verwenden. Jeder Benutzer kann jedoch die Sprache seiner Voreinstellungen individuell ändern.
   * **Geschäftsjahr beginnt am**: Wählen Sie den Monat aus, in dem das Geschäftsjahr für Ihre Organisation beginnt.



   ![](assets/configure-basic-settings-step3.png)

## Feedbackeinstellungen konfigurieren {#configurefeedbacksettings}

Mit dem Lern-Manager können Sie Feedback von Teilnehmern für einen Kurs sammeln. Es ist auch möglich, mithilfe des Lern-Managers Feedback zu Teilnehmern zu sammeln. Um Feedback einzuholen, müssen Sie zunächst die L1- und L3-Arten von Feedback konfigurieren.

L3-Feedback ist das Feedback, das ein Manager einem Teilnehmer gibt. Sie können dieses Feedback verwenden, um die Leistung der Teilnehmer im Zeitverlauf zu verfolgen. L1-Feedback ist das Feedback, das ein Teilnehmer zu einem Kurs abgibt. Mit dieser Art von Feedback kann ein Administrator direktes Feedback zu einem Kurs sammeln.

Als Administrator können Sie die Feedbackeinstellungen global konfigurieren. Gehen Sie dazu wie folgt vor:

1. Klicken Sie auf der Lern-Manager-Startseite auf **[!UICONTROL Einstellungen]**.
1. Klicken Sie im linken Teilfenster auf **[!UICONTROL Allgemein]**.
1. Um L1-Feedback zu konfigurieren, klicken Sie auf das Symbol **[!UICONTROL L1-Feedback]** &quot; ändern. Sie sehen die Optionen zum Konfigurieren einer obligatorischen Frage und mehrerer optionaler Fragen. Dies sind die Fragen, die ein Teilnehmer anzeigt, während er nach Abschluss eines Kurses Feedback gibt. Die Fragen sind als Anweisungen formuliert, sodass die Teilnehmer ihre Antwort auf einer Skala von 1 bis 5 auswählen können.

   Der erste Teil des L1-Feedbacks ist eine obligatorische Frage dazu, wie es für einen Teilnehmer ist, diesen Kurs einem Freund oder einem Kollegen zu empfehlen.

   ***Hinweis: Die Pflichtfrage kann nicht bearbeitet oder geändert werden.***

   ![](assets/configure-feedbacksettings-step3.png)

1. Um die anderen Fragen für Ihren Feedback-Fragebogen zu konfigurieren, klicken Sie auf die Fragen im Dialogfeld &quot; ****[!UICONTROL Selbststudium.]**** oder ****[!UICONTROL Klassenzimmerkurse]****. Wenn Sie auf eine Frage klicken, können Sie die Standardfragen im System bearbeiten.



   ![](assets/configure-feedbacksettings-step4.png)

1. Sie können die Standardfragen aktivieren oder deaktivieren oder die Standardfragen vollständig an Ihre Anforderungen anpassen. Sie können beispielsweise die Standardfrage &quot;Der Schulungsgegenstand war für mich relevant&quot; entfernen und die Frage durch &quot;Ich fand die Schulung nützlich und relevant&quot; ersetzen.
1. Nachdem Sie die Fragen für Teilnehmer fertig gestellt haben, können Sie die Einstellungen für Erinnerungen konfigurieren. Standardmäßig gibt es eine vorhandene Erinnerung, in der die Anwendung automatische Erinnerungen an Teilnehmer sendet, wenn ein Kurs erfolgreich abgeschlossen wurde. Diese Erinnerung wird außerdem alle zwei Wochen wiederholt, bis der Teilnehmer antwortet. Sie können die vorhandene Erinnerung ändern, indem Sie auf die Erinnerung klicken, oder eine neue Erinnerung hinzufügen.

   ![](assets/configure-feedbacksettings-step6.png)

1. Konfigurieren Sie die Einstellungen für Erinnerungen, indem Sie die folgenden Optionen ausführen:

   * **Wann werden**: Geben Sie an, ob Sie die Feedbackanforderung entweder nach Kursabschluss oder nach Kursabschluss senden möchten.
   * **Tage nach Abschluss**: Geben Sie die Anzahl der Tage an, nach denen Sie die Feedback-Anforderung senden möchten. Dieses Feld ist nur sichtbar, wenn es aktiviert ist ****[!UICONTROL Nach Kursabschluss]****.

   * **Wiederauftreten**: Geben Sie an, ob Sie die Feedback-Erinnerung täglich, jede Woche oder jeden Monat senden möchten. Sie können auch angeben, für wie viele Wochen die Erinnerung gesendet werden soll.

1. Klicken Sie auf das Häkchen, um die Einstellungen für Ihre Erinnerung zu speichern.
1. Nachdem Sie alle Feedbackeinstellungen festgelegt haben, klicken Sie auf **[!UICONTROL **Speichern**]**oben rechts auf der Seite.

## L3-Feedback konfigurieren: {#configurel3feedback}

L3-Feedback enthält die Fragen, die an den Manager eines Teilnehmers gesendet werden, nachdem der Teilnehmer einen Kurs abgeschlossen hat. L3-Feedback ermöglicht es einem Administrator, Änderungen des Verhaltens oder der Kenntnisse eines Teilnehmers im Laufe der Zeit zu verfolgen. Um dieses Feedback zu konfigurieren, klicken Sie auf der Seite &quot;Feedback&quot; auf die Schaltfläche ****[!UICONTROL L3-Feedback]**** &quot; ändern. Sie sehen eine Standardfrage. Der Manager muss diese Frage anhand einer Fünf-Punkte-Ratingskala beantworten.

![](assets/configure-l3-feedback.png)

Ähnlich wie beim L1-Feedback können Sie die Erinnerungen für L3-Feedback konfigurieren. Sie können entweder die vorhandene Erinnerung ändern oder eine neue Feedback-Erinnerung hinzufügen.

Nachdem Sie die Feedbackfrage und die Erinnerungseinstellungen abgeschlossen haben, klicken Sie auf ****[!UICONTROL Speichern]**** , um Ihre Einstellungen anzuwenden.

## Feedback auf Instanzebene konfigurieren {#configurefeedbackataninstancelevel}

Im vorherigen Verfahren wurden die Schritte zum Konfigurieren der Feedbackeinstellungen auf globaler Ebene beschrieben. Das heißt, die Einstellungen werden auf alle Kurse angewendet. Zusätzlich zu diesen globalen Fragen können Sie als Administrator oder Autor zusätzliche L1- und L3-Feedbackfragen auf Instanzebene konfigurieren.

So konfigurieren Sie die Feedbackeinstellungen auf Instanzebene:

1. Klicken Sie auf der Learning Manager-Startseite auf **[!UICONTROL Kurse]**.
1. Bewegen Sie den Mauszeiger über den Kurs, für den Sie die Feedbackeinstellungen konfigurieren möchten. Klicken [!UICONTROL **Kurs anzeigen**.]

   ![](assets/configure-feedbackataninstancelevel.png)

1. Klicken Sie auf der Seite mit den Kursdetails auf **[!UICONTROL Standardwerte für Instanzen]** im Abschnitt Konfigurieren .
1. Im Dialogfeld &quot; [!UICONTROL **Sprache**] die Sprache aus, in der der Feedback-Fragebogen angezeigt werden soll.
1. Aktivieren Sie das L1-Reaktionsfeedback, wenn Sie Feedback von Teilnehmern einholen möchten. Sie können in diesem Abschnitt bis zu zwei Fragen hinzufügen. Teilnehmer können beschreibende Antworten auf diese Fragen geben.
1. Wählen Sie das **[!UICONTROL Obligatorisch machen]** aktivieren, wenn Sie eine oder beide Fragen als Pflichtfragen definieren möchten.
1. Wählen Sie das **[!UICONTROL Fragebogen sofort nach Kursabschluss anzeigen]** wenn Sie möchten, dass Teilnehmer den Feedback-Fragebogen unmittelbar nach Abschluss des Kurses anzeigen können.

   ![](assets/configure-feedbackataninstancelevel-step7.png)

1. So konfigurieren Sie das L3-Feedback zu Verhaltensänderungen auf Instanzebene: ****[!UICONTROL Aktivieren]**** das L3-Feedback. Die Anwendung zeigt eine vordefinierte, obligatorische Frage und eine leere Frage an, bei der Sie eine Frage Ihrer Wahl eingeben können.
1. Für die vordefinierte Frage zur Verbesserung des Teilnehmers nach der Teilnahme am Kurs liegt die Antwort im Likert-Skalierungsformat vor. Das heißt, Manager müssen eine Option auf einer Skala von Strongly Agree to Strongly Disagree wählen.
1. Geben Sie die zweite Frage für den Manager an. Manager können eine beschreibende Antwort auf diese Frage geben.
1. Wählen Sie das ****[!UICONTROL Obligatorisch machen]**** aktivieren, wenn Sie die zweite Frage als Pflichtfrage definieren möchten.

   ![](assets/configure-feedbackataninstancelevel-step11.png)

1. Konfigurieren Sie optional die Einstellungen für Erinnerungen auf Instanzebene. Wenn Sie die Einstellungen für Erinnerungen hier nicht konfigurieren, werden die Einstellungen für globale Erinnerungen automatisch zugewiesen.
1. Nachdem Sie die Feedbackfragen und die Erinnerungseinstellungen abgeschlossen haben, klicken Sie auf **[!UICONTROL **Speichern**]**zum Anwenden der Einstellungen.

   ***Hinweis: Die Feedbackeinstellungen gelten nicht für Zertifizierungen.***

## Allgemeine Einstellungen konfigurieren {#configuregeneralsettings}

Mit den allgemeinen Einstellungen im Lern-Manager können Administratoren allgemeine Einstellungen konfigurieren, die sich auf andere Funktionen in der Anwendung auswirken. Beispielsweise können Sie allgemeine Einstellungen verwenden, um anzugeben, ob die Kurseffektivität für die Teilnehmer sichtbar gemacht werden kann. Allgemeine Einstellungen konfigurieren:

1. Klicken Sie auf der Lern-Manager-Startseite auf ****[!UICONTROL Einstellungen]****.
1. Klicken Sie im linken Teilfenster auf ****[!UICONTROL Allgemein]****.
1. Auf der Seite &quot;Allgemeine Einstellungen&quot; können Sie die folgenden Optionen konfigurieren:

   Bei all diesen Optionen ist die Funktion, die jede Option betrifft, unterschiedlich. Bei Bedarf können wir zu jeder der detaillierten Funktionen Querverweise anbringen.

   * **Kurseffektivität anzeigen**: Aktivieren Sie diese Option, wenn die Teilnehmer die Effektivität eines Kurses im Kurstitel sehen sollen.
   * **Option zum Zurücksetzen des Moduls**: Aktivieren Sie diese Option, wenn Sie Teilnehmern die Möglichkeit geben möchten, ein Modul zurückzusetzen. Teilnehmer können dann ihre Module zurücksetzen, wenn sie einen Fehler haben oder wenn sie das Modul teilweise abgeschlossen haben und erneut beginnen möchten.
   * **Kursmoderation**: Aktivieren Sie diese Option, wenn die Änderungen an einem Kurs von einem Administrator genehmigt werden sollen, bevor die Änderungen für die Teilnehmer sichtbar sind.
   * **Diskussionsforum**: Aktivieren Sie diese Option, wenn Teilnehmer Diskussionsforen für Kurse anzeigen und daran teilnehmen sollen. Wenn Sie die Option **Diskussionsforum** können Teilnehmer und Kursleiter Kommentare für Kurse veröffentlichen. Wenn diese Funktion jedoch auf Kursebene nicht aktiviert ist, haben die Einstellungen auf Kursebene Vorrang vor Administratoreinstellungen.

   * **Neue Kenntnisse entdecken**: Aktivieren Sie diese Option, wenn Sie möchten, dass Teilnehmer Peer- und Führungskompetenzen ausprobieren.
   * **Eindeutige Lernobjekt-IDs**: Aktivieren Sie diese Option, wenn Sie Autoren die Möglichkeit geben möchten, Lernobjekten eindeutige IDs hinzuzufügen.
   * **Katalogliste anzeigen**: Aktivieren Sie diese Option, wenn die Teilnehmer alle verfügbaren Kataloge anzeigen sollen. Mit dieser Option können Teilnehmer ihre Lernobjektliste verfeinern.



   ![](assets/configure-generalsettings-step3.png)

## Konfigurieren der Einstellungen für das Teilnehmer-Dashboard {#configurelearnerdashboardsettings}

Mit dem Teilnehmer-Dashboard im Lern-Manager können Teilnehmer ihre obligatorischen und empfohlenen Kurse unabhängig von ihren Leistungen, Kenntnissen und Ankündigungen anzeigen. Administratoren können entscheiden, wie dieses Teilnehmer-Dashboard angezeigt wird, indem sie die Einstellungen für das Teilnehmer-Dashboard konfigurieren. Mit diesen Einstellungen können Administratoren Widgets auf der Teilnehmerseite festlegen. Diese Einstellungen geben auch an, wie und wo die Widgets im Teilnehmer-Dashboard platziert werden. Als Administrator können Sie eine Vorschau des Layouts des Teilnehmer-Dashboards anzeigen, bevor Sie die Einstellungen anwenden.

1. Klicken Sie auf der Lern-Manager-Startseite auf **[!UICONTROL Einstellungen]**.
1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL ** Teilnehmer-Dashboard **.]**
1. Wählen Sie die Widgets aus, die Sie aktivieren möchten. Wenn Sie die Auswahl eines Widgets aufheben, wird das Widget sofort aus der Vorschau entfernt. Teilnehmer können dieses Widget nicht in ihrem Dashboard sehen.
1. Klicken ****[!UICONTROL Speichern]**** , um die Einstellungen anzuwenden.

   ![](assets/configure-learnerdashboardsettings-step4.png)

1. Um die Standardeinstellungen anzuwenden, klicken Sie auf **[!UICONTROL Stellen Sie die Standardeinstellungen wieder her.]** In diesem Fall werden alle Widgets außer **[!UICONTROL Willkommens- und Kurzankündigungen]** sichtbar sind.

   ***Auch nachdem Sie die Einstellungen im Teilnehmer-Dashboard aktiviert haben, können Teilnehmer Widgets in ihren jeweiligen Dashboards ändern und verschieben.***


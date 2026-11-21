---
title: Eine Live Hub-Sitzung erstellen
description: Erfahren Sie, wie Sie einen Live Hub-Kurs erstellen, Kursinstanzen hinzufügen, Kursleiter mit dem Kursleiter-Finder zuweisen, Teilnehmer registrieren und das Branding des Raums anpassen.
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 9d05ad4a059bd1fec6e64f050070dae336ba2d1b
workflow-type: tm+mt
source-wordcount: '1617'
ht-degree: 0%
---

# Eine Live Hub-Sitzung erstellen

Verwenden Sie den Live Hub , um Live-Schulungen mit Kursleiter innerhalb eines Adobe Learning Manager-Kurses bereitzustellen. Sie können Live-Hub-Sitzungen mit Inhalten zum Selbststudium kombinieren, um ein gemischtes Lernerlebnis zu schaffen.

Wenn Sie einem Kurs ein Modul für ein virtuelles Klassenzimmer hinzufügen, wählen Sie das virtuelle Schulungstool aus, das die Live-Sitzung hostet. Sie können **Live Hub**, die integrierte KI-gestützte virtuelle Schulungslösung der Adobe, oder einen externen Anbieter wie **Adobe Connect** verwenden.

>[!NOTE]
>
> Der Live-Hub wird nur dann als Option für das virtuelle Live-Schulungstool angezeigt, wenn Ihr Administrator ihn in den Einstellungen des Live-Hub aktiviert hat. Wenn sie nicht aktiviert ist, verwenden Sie stattdessen einen externen Anbieter wie Adobe Connect. Weitere Informationen finden Sie unter [Live Hub aktivieren](../administrators/feature-summary/enable-live-hub.md).

Beim Erstellen eines Live Hub-Kurses haben Sie folgende Möglichkeiten:

* Fügen Sie einem Kurs eine oder mehrere Live Hub-Sitzungen hinzu.

* Wählen Sie Kursleiter manuell aus, oder verwenden Sie KI-gestützte Kursleiterempfehlungen.

* Konfigurieren Sie den Kurs mit einer einzelnen Standardinstanz, oder erstellen Sie mehrere Instanzen für verschiedene Zeitpläne oder Zielgruppen.

In diesem Artikel wird erläutert, wie Sie einen Live Hub-Kurs erstellen, Kursleiter zuweisen und Kursinstanzen konfigurieren.

## Live Hub-Kurs erstellen

Eine Standardinstanz wird automatisch erstellt, wenn Sie ein virtuelles Klassenzimmermodul hinzufügen. Dies ist nützlich, wenn Sie eine einzelne Sitzung oder einen Standardplan für alle Teilnehmer bereitstellen möchten.

So erstellen Sie einen Live Hub-Kurs:

1. Melden Sie sich bei Adobe Learning Manager als Autor an.

1. Wählen Sie **Kurse erstellen**.

1. Wählen Sie auf der Seite **Kurskatalog** die Option **Hinzufügen** aus, und geben Sie dann die folgenden Details ein:

   1. Kursname

   1. Kurze Beschreibung

   ![Kursnamenbeschreibung hinzufügen](assets/add-course-name-description.png)
   *Geben Sie den Kursnamen und die Kurzbeschreibung ein, bevor Sie dem Kurs Module hinzufügen.*

1. Wählen Sie im Abschnitt **Module** die Option **Inhalt** > **Module hinzufügen** aus. 6 <br>Das Popupfenster **Modultyp auswählen** wird angezeigt.

1. Wählen Sie **Virtuelles Klassenzimmer** und geben Sie die Kursdetails ein, einschließlich Titel, Beschreibung, Zeitzone, Start- und Enddatum sowie Start- und Endzeit.

1. Wählen Sie **Live Hub** in **Virtuelle Live-Schulungstools** aus.

   ![Tool &quot;Live Hub auswählen&quot;](assets/select-live-hub-tool.png)
   *Wählen Sie &quot;Live Hub&quot; aus, um KI-gestützte Kursleiterempfehlungen für die Sitzung zu aktivieren.*

1. Fügen Sie Kursleiter hinzu, indem Sie eine der folgenden Optionen verwenden:

   1. Geben Sie Kursleiternamen in das Feld **Kursleiter** ein.

   1. Wählen Sie **Finden Sie Kursleiter, die AI verwenden**, um von AI empfohlene Kursleiter anzuzeigen. Weitere Informationen finden Sie unter [Kursleiter mithilfe des Kursleiter-Finders hinzufügen](#add-instructors-using-instructor-finder).

1. Wählen Sie **Hinzufügen** > **Speichern**.

1. Wählen Sie die erforderlichen Kenntnisse im Abschnitt **Kurskenntnisse** aus.

1. Wählen Sie die **Kenntnisstufe** aus, und überprüfen oder aktualisieren Sie dann die **maximalen Credits**.

   ![Kurskenntnisstufe zuweisen](assets/assign-course-skill-level.png)
   *Weisen Sie Kenntnisse und Kenntnisstufen zu, um die Credits zu definieren, die Teilnehmer durch Abschluss des Kurses erwerben.*

1. Wählen Sie **Speichern** > **Publish**. Der Kurs wurde erfolgreich in Adobe Learning Manager erstellt.

## Kursinstanz erstellen

Ein Administrator kann eine oder mehrere Instanzen eines Kurses erstellen, um ihn für verschiedene Zielgruppen, Zeitpläne oder Standorte anzubieten. Jede Instanz verfügt über eigene Sitzungsdetails, sodass Sie jeder Instanz desselben Kurses unterschiedliche Kursleiter, Empfehlungen im Kursleiter-Finder und Timings zuweisen können.

So erstellen Sie eine Kursinstanz:

1. Melden Sie sich bei Adobe Learning Manager als Autor an.

1. Öffnen Sie den Kurs und wählen Sie dann im linken Bereich **Instanzen** aus.

   ![Standardinstanzseite](assets/default-instance-page.png)
   *Die Standardinstanz wird automatisch erstellt, wenn Sie ein virtuelles Klassenzimmermodul hinzufügen.*

1. Wählen Sie **Neue Instanz hinzufügen**.

1. Geben Sie den **Instanznamen**, **Startdatum** und **Ausfülltermin** ein. Wählen Sie **Weitere Optionen anzeigen**, um zusätzliche Einstellungen zu konfigurieren.

   ![Neues Instanzformular hinzufügen](assets/add-new-instance-form.png)
   *Geben Sie einen Instanznamen, ein Startdatum und einen Abschlusstermin ein, um eine neue Kursinstanz zu erstellen.*

1. Wählen Sie **Speichern** aus. <br> Die neue Instanz wird der Liste **Instanzen** hinzugefügt.

   ![Instanzen listen neue Instanz auf](assets/instances-list-new-instance.png)
   *Die neue Instanz wird neben der Standardinstanz in der Instanzenliste angezeigt.*

1. Wählen Sie die Nummer unter **Sitzungen** aus, um die **Sitzungsdetails** anzuzeigen.

   Symbol zum Bearbeiten von ![Sitzungsdetails](assets/session-details-edit-icon.png)
   *Sitzungsdetails zeigen an, welche Timing-, Kursleiter- und Standortfelder noch konfiguriert werden müssen.*

1. Wählen Sie das Bearbeitungssymbol (Stiftsymbol) neben den Sitzungsdetails aus, um das Konfigurationsfeld für die Sitzung zu öffnen.

   Konfigurationsbereich für ![Sitzung](assets/session-configuration-panel.png)
   *Konfigurieren Sie den Zeitplan, den Kursleiter und den Speicherort für eine bestimmte Sitzungsinstanz.*

1. Geben Sie im Feld **Kursleiter** Namen manuell ein, oder wählen Sie **Kursleiter mithilfe von AI suchen** für Kursleiter, die von AI empfohlen werden. Weitere Informationen finden Sie unter [Kursleiter mithilfe des Kursleiter-Finders hinzufügen](#add-instructors-using-instructor-finder).

1. Geben Sie die Details zum **Speicherort** ein, und wählen Sie dann **Speichern** aus. Die Sitzung wird mit den konfigurierten Timings, Kursleitern und Standortdetails aktualisiert.

## Kursleiter mit dem Kursleiter-Finder hinzufügen

Verwenden Sie statt manuell nach Kursleitern zu suchen und diese hinzuzufügen **Kursleiter-Finder**, um KI-gestützte Kursleiter-Empfehlungen für die Sitzung zu erhalten. Der Finder sucht nach Kursleitern, die anhand der Kursdetails und der erforderlichen Fähigkeiten ermittelt werden, berücksichtigt aber auch den Ferienkalender der Organisation, die Verfügbarkeit von Kursleitern und die Auslastung der Kursleiter, um die geeignetsten Kursleiter vorzuschlagen. Weitere Informationen finden Sie unter [Kursleiter hinzufügen und verwalten](./instructor-management.md).

>[!NOTE]
>
> Der Kursleiter-Finder wird nur angezeigt, wenn Ihr Administrator den Kursleiter-Finder-Assistenten in den Live Hub-Einstellungen aktiviert hat. Weitere Informationen finden Sie unter [Live Hub aktivieren](../administrators/feature-summary/enable-live-hub.md).

So fügen Sie Kursleiter mit dem Kursleiter-Finder hinzu:

1. Navigieren Sie zum Abschnitt **Kursleiter** im Modul **Virtuelles Klassenzimmer**.

1. Wählen Sie **Kursleiter mithilfe von AI suchen**. <br> Der Bereich **AI Assistant** wird auf der rechten Seite geöffnet.

   ![AI Assistant Panel Instructor Recommendations](assets/ai-assistant-panel-instructor-recommendations.png)
   *Verwenden Sie das Bedienfeld &quot;AI-Assistent&quot;, um Empfehlungen für Kursleiter und Zeitfenster auf der Grundlage der Sitzungsdetails abzurufen.*

1. Überprüfen Sie die Liste der empfohlenen Kursleiter.

1. Navigieren Sie zu dem Kursleiter, den Sie zuweisen möchten, und wählen Sie dann **Hinzufügen** aus. <br> Der ausgewählte Kursleiter wird dem Feld **Kursleiter** als Tag hinzugefügt.

## Kurs für große Sitzungen erstellen {#create-large-session}

Der Live Hub unterstützt große Sessions mit bis zu 5.000 Teilnehmern. Wenn Sie einen Kurs mit dieser Kapazität erstellen, konfiguriert Live Hub automatisch den Raum für eine große Zielgruppe und wendet die entsprechenden Funktionsbeschränkungen an.

So erstellen Sie eine große Sitzung:

1. Melden Sie sich bei der ALM als **Autor** an.
1. Wählen Sie **Hinzufügen** auf der Seite **Kurskatalog** aus.
1. Geben Sie den Kursnamen und die Beschreibung ein.
1. Wählen Sie im Abschnitt **Module** die Option **Inhalt** > **Module hinzufügen** aus. Das Popupfenster **Modultyp auswählen** wird angezeigt.
1. Wählen Sie **Virtuelles Klassenzimmer** und geben Sie die Kursdetails ein, einschließlich Titel, Beschreibung, Zeitzone, Start- und Enddatum sowie Start- und Endzeit.
1. Wählen Sie **Live Hub** in **Virtuelle Live-Schulungstools** aus.
1. Wählen Sie **5000 Teilnehmerkapazität aktivieren**. Wenn Sie diese Option nicht aktivieren, unterstützt die Sitzung bis zu 1100 Teilnehmer.

   ![Dialogfeld &quot;Virtuelles Klassenzimmer&quot; mit ausgewähltem Live-Hub und der Option &quot;5000 Teilnehmer aktivieren&quot;](assets/virtual-classroom-enable-5000-attendee-capacity.png "Dialogfeld &quot;Virtuelles Klassenzimmer&quot; mit ausgewähltem Live-Hub und der Option &quot;5000 Teilnehmer aktivieren&quot;")

1. Wählen Sie **Speichern** > **Publish**.

### Funktionen in großen Sessions

Wenn ein Kursleiter die Sitzung öffnet, zeigen die Raumeinstellungen an, dass Einschränkungen für große Sitzungen gelten.

| Funktion | Verhalten in einer großen Sitzung |
|---|---|
| **Teilnehmer** | Eine große Session unterstützt bis zu 5.000 Teilnehmer. Sobald die Sitzung dieses Limit erreicht hat, können keine weiteren Teilnehmer mehr teilnehmen. |
| **Kameras** | Bis zu 10 Kursleiter können ihre Kameras gleichzeitig aktivieren. Teilnehmer können ihre Kameras nicht aktivieren. Wenn das Limit für die Kamera erreicht wurde, wird eine Meldung angezeigt, wenn ein anderer Kursleiter versucht, seine Kamera zu aktivieren.<p>Zugleich gestellte Kameras werden als Stapel verarbeitet. Daher kann die Anzahl der aktiven Kameras den konfigurierten Grenzwert überschreiten. In der QuickInfo der Schaltfläche &quot;Kamera&quot; wird jedoch weiterhin das konfigurierte Limit angezeigt. |
| **Mikrofone** | Bis zu 20 Teilnehmer können die Stummschaltung ihrer Mikrofone gleichzeitig aufheben. Wenn das Mikrofonlimit erreicht ist, wird eine Meldung angezeigt, wenn ein anderer Teilnehmer versucht, die Stummschaltung aufzuheben.<p>Gleichzeitig gestellte Mikrofonanfragen werden als Stapel verarbeitet. Dies hat zur Folge, dass die Anzahl der Teilnehmer, die die Stummschaltung aufheben, vorübergehend die konfigurierte Grenze überschreiten kann. |
| **Arbeitsräume** | Das Symbol für den Arbeitsraum bleibt sichtbar, aber Kursleiter können keine Arbeitsräume starten. Eine Meldung wird angezeigt, wenn versucht wird, eine zu starten. |
| **Bildschirmfreigabe und Whiteboard** | Nur Kursleiter können ihre Bildschirme freigeben und das Whiteboard verwenden. Kursleiter können diese Berechtigungen nicht für Teilnehmer bereitstellen. |
| **Privater Chat** | Teilnehmer können private Nachrichten an Kursleiter senden, aber keine privaten Nachrichten an andere Teilnehmer senden. |
| **Eingabeindikator** | Die Tippanzeige wird in großen Sitzungen nicht angezeigt. |
| **Chat, Reaktionen, Fragen und Wortmeldungen** | Das System verarbeitet diese Interaktionen stapelweise, sodass sie nach einer kurzen Verzögerung auftreten können. Der Live-Hub gruppiert auch Reaktionen und zeigt jeweils eine begrenzte Anzahl an. |
| **Chatverlauf** | Das System entfernt automatisch ältere Chat-Nachrichten, wenn der Chat-Verlauf zu groß wird, um die Stabilität der Sitzung aufrechtzuerhalten. |
| **Umfragen, Tests, Aufzeichnung und Anwesenheit** | Diese Funktionen funktionieren auf die gleiche Weise wie in regulären Sitzungen. |
| **KI-Funktionen** | <ul><li>Das System erkennt Fragen im Chat und zeigt sie im Bereich **Fragen** an, obwohl sie möglicherweise nach einer kurzen Verzögerung angezeigt werden.</li><li>KI-Funktionen für Arbeitsräume sind nicht verfügbar, da große Sitzungen keine Arbeitsräume unterstützen.</li><li>Andere KI-Funktionen funktionieren genauso wie in regulären Sitzungen.</li></ul> |

>[!NOTE]
>
>Ohne die Option **5000 Teilnehmerkapazität aktivieren** unterstützt eine reguläre Sitzung bis zu 1.100 Teilnehmer, 50 Kameras und 20 nicht stummgeschaltete Teilnehmer.

## Teilnehmer für den Kurs registrieren

Die Registrierung von Teilnehmern für einen Live Hub-Kurs hat zwei Möglichkeiten:

1. Ein **Administrator** registriert die Teilnehmer gemäß den Anforderungen des Unternehmens für den Kurs. Weitere Informationen finden Sie unter [Kursinstanzen und Lernpfade erstellen](https://experienceleague.adobe.com/de/docs/learning-manager/using/admin/courses).

1. Teilnehmer können sich selbst direkt über die Seite **Katalog** für den Kurs registrieren. Wenn der Kurs für die Selbstregistrierung konfiguriert ist, werden die Teilnehmer sofort registriert und können über **Meine Lernergebnisse** auf den Kurs zugreifen. Weitere Informationen finden Sie unter [Meine Lernergebnisse](https://experienceleague.adobe.com/de/docs/learning-manager/using/learner/courses).

Nach der Registrierung werden die Teilnehmer dem Kurs hinzugefügt und erhalten eine Benachrichtigung in ihrem Adobe Learning Manager-Konto. Abhängig von den E-Mail-Benachrichtigungseinstellungen des Kontos erhalten die Teilnehmer möglicherweise auch eine Einladung zur Teilnahme am Kurs per E-Mail.

## Branding für Live-Hub-Räume anpassen

Administratoren können das Erscheinungsbild von Live Hub-Räumen anpassen, um sie dem Branding Ihrer Organisation anzupassen. Verwenden Sie die **Designs**-Einstellungen in Adobe Learning Manager, um Markenfarben, Logos und visuelles Styling über Live Hub-Sitzungen hinweg anzuwenden.

Das benutzerdefinierte Branding trägt zu einem konsistenten Lernerlebnis bei und stellt sicher, dass Live-Schulungen die Identität Ihres Unternehmens widerspiegeln.

Weitere Informationen zum Konfigurieren von Designs finden Sie im Artikel [Farbdesigns](../administrators/feature-summary/themes.md#color-themes).

---
description: Als Administrator können Sie Aktivitäten, die im Sozialen Lernen durchgeführt werden, aktivieren, deaktivieren und überwachen. Sobald die Funktion "Soziales Lernen" aktiviert ist, können Teilnehmer sie anzeigen und mit der Teilnahme am sozialen Lernen beginnen.
jcr-language: en_us
title: Überwachung und Moderation von Soziales Lernen als Administrator
contentowner: kuppan
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3604'
ht-degree: 0%

---



# Überwachung und Moderation von Soziales Lernen als Administrator

Als Administrator können Sie Aktivitäten, die im Sozialen Lernen durchgeführt werden, aktivieren, deaktivieren und überwachen. Sobald die Funktion &quot;Soziales Lernen&quot; aktiviert ist, können Teilnehmer sie anzeigen und mit der Teilnahme am sozialen Lernen beginnen.

## Aktivieren und Konfigurieren von Einstellungen im sozialen Lernen {#enableandconfiguresettingsinsociallearning}

Um die Funktion &quot;Soziales Lernen&quot; zu aktivieren und zu konfigurieren, gehen Sie wie folgt vor:

1. Klicken **[!UICONTROL Social Learning]** im linken Navigationsbereich. Sie werden zur Aktivitätsseite weitergeleitet.
1. Aktivieren **[!UICONTROL Social Learning]** -Funktion über die **[!UICONTROL Aktivieren]** in der Aktivitätsseite, wenn Sie sie zum ersten Mal aktivieren. Andernfalls kann sie über die **[!UICONTROL Einstellungen]** angezeigt.

   Ein Popup-Dialogfeld wird angezeigt (siehe Screenshot unten).

   ![](assets/artboard-20-2x.png) ![](assets/enable-social-learningforthefirsttime.png)

   *Social Learning aktivieren*

<!-- ![](assets/enable-social-learningfeatureinsettings.png) ![](assets/enable-social-learningdialog.png)-->

Der Administrator kann Einstellungen für Soziales Lernen konfigurieren. Einstellungen umfassen Typen von Inhaltskurationen wie **[!UICONTROL Manuelle Kuratierung]** und **[!UICONTROL Keine Kuration]**. Die Bereichseinstellungen können auf einen anderen Bereich festgelegt werden, z. B. auf den Benutzertyp (intern/extern) oder andere aktive Felder im Konto. Der Administrator kann den URL-Pfad festlegen, von dem Teilnehmer die Adobe Learning Manager-Desktopanwendung herunterladen können.

## Kuratierung von Inhalten {#contentcuration}

Da Soziales Lernen ein informelles Lernen ist, ist seine Funktionalität ähnlich wie bei anderen Social-Media-Plattformen. Social-Media-Posts stören oft, weil sie oft irrelevante Inhalte konsumieren, die ihre Produktivität beeinträchtigen. Dieser Gedanke kann von Content-Moderation und Kuration bedient werden.

**[!UICONTROL Manuelle Kuratierung]** und **[!UICONTROL Keine Kuration]** Es gibt zwei Kurationsoptionen, die vom Administrator ausgewählt werden können.

**[!UICONTROL Automatische Unterstützung für manuelle Kuratierung]:** Learning Manager verfügt über eine auf künstlicher Intelligenz basierende Auto-Kuration-Engine, mit der Sie die Essenz des Inhalts jedes beliebigen Formats intelligent herausfinden können, das später den gewünschten Teilnehmern bereitgestellt werden kann. Es kann auch Inhalte genehmigen oder ablehnen, die auf der Grundlage des angegebenen Confidence-Scores veröffentlicht werden.

Zum Beispiel ist Adarsh ein Lerner und er fand einen Blog interessant, also postet er ihn auf der Social Learning Plattform des Adobe Learning Managers. Der Beitrag wird dann an die KI-gestützte Content Curation Engine weitergeleitet, die die im Inhalt vorhandenen Kenntnisse vorhersagt und diese mit den entsprechenden Board-Kenntnissen vergleicht. Wenn eine der Qualifikationen übereinstimmt, wird der Inhalt veröffentlicht, andernfalls wird er zur manuellen Kuration gesendet.

Der Mindestwert für die Vertrauenswürdigkeit, der für die Buchung erforderlich ist, ist 50 %.

**[!UICONTROL Manuelle Kuratierung]:** Um die Authentizität des Inhalts zu überprüfen, bevor er live geschaltet wird, kann der Administrator die Einstellung &quot;Manuelle Kuratierung&quot; aktivieren. Sobald die Einstellung für die manuelle Kuration aktiviert ist, wird sie an die Top SMEs (maximal 3) für die Kuration gesendet. Basierend auf der durchschnittlichen Antwort wird die Stelle entsprechend genehmigt/abgelehnt. Wenn die Antwort größer als gleich 50 Prozent ist, geht der Beitrag live anders abgelehnt. Weitere Informationen über KMU: [hier klicken](social-learning-configurations-as-an-admin.md#SubjectMatterExpertsSMEs).

## Automatische Kuration des Inhalts {#autocuration}

Die manuelle Moderation von Inhalten ist häufig fehleranfällig und zeitaufwendig. Darüber hinaus ist das Verfahren nicht skalierbar und für ein hohes Volumen an sozialen Aktivitäten ungeeignet. Daher wird das Kuratieren von Inhalten automatisch kritisch, wenn viele Benutzer bedient werden, die sozial aktiv sind.

Im Lern-Manager gibt es eine Option zum automatischen Kuratieren von Inhalten. Die Kuration wird von einer AI-fähigen Engine gesteuert, die mit den vordefinierten Kenntnissen arbeitet, nachdem der Administrator die vordefinierten Kenntnisse mit Kenntnissen verknüpft hat. Weitere Informationen finden Sie unter [Zuordnung von Kenntnisdomänen](curation-skills.md).

Bei der automatischen Kuration sind die folgenden Inhaltstypen zulässig:

* PDF
* Audio- und Videodateien
* Presentations - PPT oder PPTX
* Documents - .doc, .docx

Ein Administrator kann die Option aktivieren, um Inhalte automatisch in der Administrator-App zu kuratieren.

1. Klicken Sie im linken Bereich der Admin-App auf **[!UICONTROL Social Learning]**.
1. Klicken Sie auf der Seite auf die Registerkarte **[!UICONTROL Einstellungen]**.
1. Option aktivieren **[!UICONTROL Automatische Unterstützung für manuelle Kuratierung]**.

   ![](assets/auto-curation.png)

   *Wählen Sie die Option Manuelle Kuratierung mit automatischer Unterstützung aus.*

Wenn ein Benutzer einen Inhalt in ein Board hochlädt, scrubbt ein AI-basierter Algorithmus den Text vom Inhalt ab und der Text wird dann an die Kurations-Engine übergeben. Die Kurations-Engine sucht nach den im Inhalt vorhandenen Kenntnissen.

Die vorhergesagten Kenntnisse aus dem hochgeladenen Inhalt stimmen mit denen mit dem Board überein, in dem der Inhalt hochgeladen wurde.  Wenn Kenntnisse mit einer Vertrauensbewertung von mehr als 50 % der Board-Kenntnisse übereinstimmen, wird der Inhalt im Board veröffentlicht. Wenn der Confidence-Score kleiner als 50 % ist, wird der Inhalt zur manuellen Kuration gesendet.

Wenn ein Inhalt automatisch kuratiert wird, erhält der Benutzer eine Benachrichtigung, dass der Inhalt in dem Board verfügbar ist, in das er zuvor hochgeladen wurde.

![](assets/only-ai-based.png)

*Flussdiagramm der Kurationseinstellungen*

Es wird empfohlen, dass der Administrator SMEs für Kenntnisse hinzufügt, wenn die manuelle Kuration nur aktiviert ist. Der Administrator kann SME hinzufügen, indem er Benutzern mit Kenntnissen über SME-Punkte im Voraus bereitstellt. Weitere Informationen über die Bereitstellung von Punkten für KMU:  [hier klicken](social-learning-configurations-as-an-admin.md#SubjectMatterExpertsSMEs).

**Keine Kuration:** Alle Beiträge der Teilnehmer werden automatisch ohne Inhaltsmoderation veröffentlicht.

<!--![](assets/artboard-6-2x.png)-->

## Häufig gestellte Fragen zur automatischen Kuration von Inhalten {#faq-auto-curation}

+++Wie viel Zeit hat ein SME, um einen Beitrag zu kuratieren?

Ein SME erhält mindestens 24 Stunden, um einen Beitrag zu kuratieren. Aufgrund von Zeitzonenunterschieden kann sie auf 47 Stunden erhöht werden.

+++

+++Wird der Kurs an die nächsten drei SME weitergeleitet, wenn alle drei zur Verfügung stehen? Werden immer drei SME einbezogen?

Der Kurationsantrag wird am ersten Tag an die Top-SME geleitet. Wenn sie nicht antworten, wird der Antrag am folgenden Tag an die nächsten drei SME weitergeleitet.

Wenn die drei neuen SME nicht antworten, wird der Antrag an die Moderatoren des Boards gerichtet.

Wenn die Board-Moderatoren nicht antworten, wird der Antrag automatisch genehmigt.

+++

+++Wenn zwei SME kuratieren und einer nicht - geht der Antrag an den vierten SME oder wird der Durchschnitt der von der ersten SME-Runde für den Beitrag bewerteten Beiträge übernommen?

Für die Genehmigung des Beitrags ist eine Genehmigungsrate von 50 % erforderlich. Ebenso wird die Ablehnung des Beitrags mit 50 % angegeben. Bei jeder Genehmigung durch einen SME wird bewertet, ob 50 % erreicht wurden.

Wenn er nach einem Tag keine 50 % erreicht, wird er an die nächsten SME weitergeleitet, wodurch die vorherigen unbeantworteten Kurationsanträge verfallen.

Beispiel: Am ersten Tag wird der Kurationsantrag an drei SME geleitet; einer von ihnen stimmt zu, zwei antworten nicht. Am nächsten Tag geht der Kurationsantrag an die nächsten drei SME. Auf dieser Ebene gibt es jetzt insgesamt vier aktive SME. Mindestens zwei SEMs müssen es genehmigen, um die Kuration zu genehmigen.(Wenn zwei zustimmen und zwei ablehnen, wird das, was die ersten 50 % erreicht, übernommen.)

+++

+++Soweit ich weiß, wird ein &quot;Moderator&quot; nur zugewiesen (und das ist nicht obligatorisch), wenn jemand ein neues Board erstellt. Was nützt es, wenn ein Teilnehmer einem Board einen &quot;Moderator&quot; zuweist, wenn SMEs den Kenntnissen zugewiesen werden, mit denen ein Board verbunden ist?

Im Folgenden sind die Zuständigkeiten eines Moderators des Soziales Board aufgeführt:

* Möglichkeit, den Board-Namen, die Beschreibung, die Board-Sichtbarkeitseinstellungen und andere Konfigurationen zu bearbeiten.
* Möglichkeit, einen Beitrag auf dem Board zu löschen, wenn der Beitrag für die Zielgruppe nicht geeignet ist.
* Der Moderator erhält Benachrichtigungen über Missbrauch melden für das Board.
* Der Moderator erhält Kurationsanträge, wenn kein SME für das Board vorhanden ist.

+++

+++Unser Schulungsteam wird die Kenntnisse, die mit der Kenntnisstufe verbunden sind, sowie die KMU, die den Kenntnissen zugewiesen sind, erweitern bzw. überwachen.

SME werden basierend auf Kenntnissen hinzugefügt/zugewiesen, nicht auf Kenntnisstufen. Dies ist so beabsichtigt.

+++

+++Was ist der Unterschied zwischen einem &quot;Moderator für Soziales Lernen&quot; und einem &quot;SME für Soziales Lernen&quot;?

**Moderatoren:** Sekundäre Eigentümer des Boards. Sie werden während der Board-Erstellung von den Erstellern hinzugefügt, sodass sie das Board auch in Abwesenheit des Erstellers steuern können. Standardmäßig ist der Ersteller des Boards der Moderator.

**KMU:** Fachexperten sind Experten mit spezifischen Kenntnissen. Der Administrator kann bestimmten Kenntnissen SME zuweisen, um Inhalte dieser Kenntnisse zu kuratieren. SME erhalten die Kurationsanträge für Boards, die mit ihren Kenntnissen verknüpft sind. Teilnehmer können auch SME werden, indem sie SME-Punkte sammeln.

+++

+++Wenn zwei oder drei SME bestimmten Kenntnissen zugewiesen werden, hängt eine Genehmigung oder Ablehnung eines Social-Learning-Beitrags von der Kuration aller SME ab oder davon, wer zuerst kuratiert?

Für die Genehmigung des Beitrags ist eine Genehmigungsrate von 50 % erforderlich. Ebenso wird die Ablehnung des Beitrags mit 50 % angegeben. Bei jeder Genehmigung durch einen SME wird bewertet, ob 50 % erreicht wurden.

Wenn er nach einem Tag keine 50 % erreicht, wird er an die nächsten SME weitergeleitet, wodurch die vorherigen unbeantworteten Kurationsanträge verfallen.

+++

## Bereichseinstellungen {#scopesettings}

Im Sozialen Lernen bestimmt ein Umfang die Boards, die Sie sehen, die die Sichtbarkeit des Inhalts steuern. Wenn ein Benutzer einen Bereich hat, z. B. ***Vendor_A***, er kann nur Boards und zugehörige Beiträge sehen, die von anderen erstellt wurden, die demselben Bereich angehören ***Vendor_A***.

Dadurch können Administratoren eine Kohorte von Benutzern, z. B. Lieferanten, Partnern oder Abteilungen in einem Unternehmen, separat verwalten.

Ermöglichen Sie soziales Lernen und Leaderboard für interne und externe Benutzer.

Es gibt separate Abschnitte, um interne und externe Benutzer zu aktivieren.

**Für interne Teilnehmer aktivieren**

In diesem Abschnitt können Sie die Benutzereigenschaft auswählen, um den Umfang des sozialen Lernens für interne Benutzer zu definieren. Benutzer mit den gleichen Merkmalen **Wert** Teilen Sie den gleichen Bereich für Soziales Lernen.

Im Fenster &quot; **Benutzermerkmal** die gewünschte Option aus.

![](assets/choose-value-of-usercharacteristic.png)

*Wählen Sie die Benutzereigenschaften aus, um den Bereich zu definieren.*

Standardmäßig ist die Option **[!UICONTROL Alle internen Benutzer]** in der Dropdown-Liste Benutzermerkmal ist immer ausgewählt.

Sie können den Umfang interner Benutzer basierend auf ihren aktiven Feldern festlegen.

**Für externe Teilnehmer aktivieren**

Um den Lernbereich für externe Benutzer zu definieren, verwenden Sie ein externes Profil. Teilnehmer mit demselben externen Profil teilen sich einen gemeinsamen Raum für Soziales Lernen.

![](assets/choose-an-externalprofile.png)

*Bereich für externe Teilnehmer aktivieren*

Externe Benutzer werden basierend auf ihren externen Profilen festgelegt.

Wenn Sie z. B. in der Liste oben die Option **[!UICONTROL Acme Corp]** können alle Teilnehmer, die zu Acme Corp gehören, die von ihnen erstellten Boards sehen. Wenn Sie die Option **Henry Cavill**, die Teilnehmer können kein Board sehen, das von Henry Cavill erstellt wurde.

Der Administrator kann die Sichtbarkeit des Inhalts basierend auf dem aktiven Feld im Fenster &quot; **[!UICONTROL Benutzermerkmal]** ein.

Der Administrator kann z. B. den Bereich auf **[!UICONTROL Benutzertyp (intern/extern)]** -Benutzer. Wenn Sie als Suchbereich &quot;Benutzertyp&quot; festlegen, ist der von einem internen Teilnehmer auf der Plattform für soziales Lernen freigegebene Inhalt nur für andere interne Teilnehmer in der Organisation und nicht für die externen Benutzer sichtbar und umgekehrt.

Nachdem der Administrator ein Benutzermerkmal ausgewählt hat, kann er die Funktion für soziales Lernen auf Teilnehmer und Teilnehmergruppen beschränken, indem er das Kontrollkästchen unter dem Feld Benutzermerkmal aktiviert. Klicken Sie auf das Wertfeld, um den Teilnehmer oder die Teilnehmergruppen auszuwählen, für den bzw. die Sie die Funktion Soziales Lernen aktivieren möchten.

Standardmäßig wird der Umfang durch das Attribut **[!UICONTROL Benutzertyp]** die interne oder externe Teilnehmer sind.

Wenn das aktive Feld keinen Wert enthält, wird das Dialogfeld &quot; **[!UICONTROL Wert]** ist für den Administrator nicht sichtbar.

<!--![](assets/scope-settings.png) ![](assets/scope-settings1-png.jpg)-->

Benutzer können ihre Inhalte auch mithilfe der Adobe Learning Manager-Desktopanwendung veröffentlichen. Abhängig davon, ob Sie Mac oder Windows verwenden, klicken Sie auf die angegebenen Links, um die Desktop-Anwendung herunterzuladen, und führen Sie die angegebenen Schritte aus, um sie auf Ihrem System zu installieren. Wenn Sie Probleme bei der Installation haben, [hier klicken](../../kb/troubleshooting-issues-with-adobe-learning-manager-desktop-app.md).

## Berechtigungen zum Erstellen von Boards {#permission}

Um die Erstellung von Boards durch alle Teilnehmer einzuschränken und die Boards effektiv zu moderieren, kann ein Administrator einer ausgewählten Gruppe von Benutzern Berechtigungen zum Erstellen von Boards erteilen.

![](assets/grant-permissiontocreateboards.png)

*Berechtigungen zum Erstellen eines Boards festlegen*

Standardmäßig ist die Option **[!UICONTROL Alle Teilnehmer]** aktiviert ist.

**[!UICONTROL Alle Teilnehmer]:** Wenn Sie diese Option auswählen, können alle internen und externen Benutzer Boards erstellen.

**Eine Gruppe von Teilnehmern:** Wenn Sie diese Option auswählen, werden nur Benutzer, die über die Berechtigung zum Erstellen eines Boards verfügen, die **[!UICONTROL Neues Board erstellen]** im Sozialen Lernen. Wählen Sie die Benutzergruppe aus, der die Berechtigung zum Erstellen eines Boards erteilt werden muss. Sie können auch automatisch generierte sowie benutzerdefinierte Benutzergruppen hinzufügen.

<!--![](assets/grant-permissiontoausergroup.png)-->

Benutzer mit demselben Bereich können nur das Board sehen. Für Benutzer, die nicht über die Berechtigung verfügen, wird das Dialogfeld &quot; **[!UICONTROL Neues Board erstellen]** Link bleibt unsichtbar.

Warten Sie 60 Minuten, bis die Änderungen wirksam werden.

## Spezielle Benutzer {#privilege}

Ein Administrator kann einer Benutzergruppe besondere Berechtigungen erteilen, mit denen Mitglieder der Gruppe an allen Boards teilnehmen können. Alle Einschränkungen, die im Abschnitt Bereichseinstellungen festgelegt wurden, werden von der speziellen Benutzergruppe umgangen.

Die Benutzergruppe kann entweder automatisch generiert oder benutzerdefiniert sein.

Ein Benutzer, dem diese Berechtigung gewährt wurde, hat Zugriff auf alle Boards, mit Ausnahme von **private Boards**.

![](assets/special-users.png)

*Besondere Rechte gewähren*

Wenn der Administrator eine Benutzergruppe auswählt, können standardmäßig alle Benutzer in der Gruppe auf alle Boards zugreifen, unabhängig vom Umfang des Benutzers. Jeder Benutzer mit diesen erhöhten Rechten kann alle internen und externen Boards anzeigen und daran teilnehmen.

Spezielle Benutzer erhalten Kurationsanfragen über alle Bereiche hinweg, wenn Benutzer über ausreichende SME-Punkte für diese Kenntnisse verfügen.

Wenn der Benutzer nicht über die erforderlichen SME-Punkte verfügt, werden die Kurationsberechtigungen an die drei wichtigsten SME dieser Kenntnisse weitergegeben.

Im neuen Umfang erhält er Punkte für Aktivitäten in allen Boards.

In den Abschnitten des Sozialen Leaderboards kann ein Benutzer alle Benutzer seines Bereichs zusammen mit speziellen Benutzern anzeigen.

Wenn Ihnen besondere Benutzerrechte gewährt wurden, können Sie alle Benutzer im Konto in Ihrer Rangliste sehen, unabhängig vom Umfang der Benutzer.

Wenn spezielle Benutzer durch ausreichende Punktzahl zu SME werden, werden sie im **[!UICONTROL Top-Fachexperten]** im sozialen Leaderboard.

Warten Sie 60 Minuten, bis die Änderungen wirksam werden.

## Anpassen des sozialen Banners {#customize-social-banner}

Der Administrator kann den Titel und den Untertitel anpassen, die auf der Sozialen Lernen-Startseite im Headerbild angezeigt werden. Alles was der Administrator als Titel und Untertitel eingibt, wird auf der Startseite des Teilnehmers angezeigt.

1. Klicken Sie in der Admin-App auf **[!UICONTROL Social Learning]** > **[!UICONTROL Einstellungen]**.
1. Klicken **[!UICONTROL Anpassen]**.
1. Ändern Sie das Bannerbild. Die Abmessungen des Bildes müssen mindestens **1.600 px x 240 px**.
1. Schalten Sie die Option zum Ausblenden oder Anzeigen der **[!UICONTROL Weitere Infos]** auf dem Banner.
1. Geben Sie den Titel und den Untertitel in die unten angegebenen Felder ein:

   ![](assets/image012.png)

   *Anpassen des sozialen Banners*

Es gibt noch einige weitere Optionen:

* **[!UICONTROL Sprache]:** Wählen Sie aus der Dropdown-Liste die Sprache aus, in die Titel und Untertitel übersetzt werden sollen. Sie können auch benutzerdefinierten Text für verschiedene Sprachen hinzufügen.
* **[!UICONTROL Replizieren]:** Klicken Sie auf diese Schaltfläche, um Titel und Untertitel in allen Sprachen zu replizieren.
* **[!UICONTROL Zurücksetzen]:** Klicken Sie auf diese Schaltfläche, um zum ursprünglichen Titel und Untertitel zurückzukehren.

Auf der Soziales Lernen-Startseite werden die vom Administrator bereitgestellten Informationen als Kopfzeile der Seite angezeigt.

<!--![](assets/banner-learner.png)-->

## Trends {#trends}

Die Trends der sozialen Aktivität des Teilnehmers können auf der Registerkarte Aktivität im Abschnitt Trends angezeigt und verfolgt werden. Diese Daten können für verschiedene Zeiträume angezeigt werden, wie die letzten sieben Tage, den letzten Monat, die letzten drei Monate und die ganze Zeit.

Die letzten sieben Tage ist der Standardwert im Datumsfilter.

>[!NOTE]
>
>Die letzten sieben Tage ist der Standardwert im Datumsfilter.

Die erste Grafik stellt dem Administrator die folgenden Informationen für den vom Datumsfilter ausgewählten Zeitraum zur Verfügung:

1. **[!UICONTROL Neue Beiträge]**: Zeigt die Anzahl der neuen Beiträge an, die innerhalb des Datumszeitraums erstellt wurden. Außerdem wird die Gesamtzahl der Beiträge für den gesamten Zeitraum angezeigt.
1. **[!UICONTROL Prozentsatz der aktiven Benutzer]**: Zeigt den Gesamtprozentsatz der aktiven Benutzer im sozialen Lernen im Vergleich zur Gesamtzahl der im Konto verfügbaren Benutzer an.
1. **[!UICONTROL Neue Boards]**: Zeigt die Anzahl der neuen Boards an, die erstellt wurden. Außerdem wird die Gesamtzahl der Boards für den gesamten Zeitraum angezeigt.

Die zweite Grafik ist ein Liniendiagramm, das den Trend der Anzahl der Boards oder Beiträge anzeigt, die basierend auf dem Zeitraum erstellt wurden, der vom Datumsfilter ausgewählt wurde. Klicken Sie auf den Filter, um die verschiedenen Zeitoptionen anzuzeigen, z. B. die letzten sieben Tage, den letzten Monat, die letzten drei Monate und die gesamte Zeit.

![](assets/trends.png)

*Neue Grafik mit dem Trend*

## Kenntnisse {#skills}

In diesem Abschnitt können Sie alle Kenntnisse anzeigen, die in der Plattform für soziale Aktivitäten verwendet wurden. Der Administrator kann das Suchfeld verwenden, um nach Kenntnissen zu suchen, die beim Erstellen eines Boards und beim Zuordnen von SMEs noch nicht verwendet werden. Auf diese Weise erhalten SMEs eine Benachrichtigung, wenn ein Board mit diesen Kenntnissen erstellt wird, und sie können den Beitrag als Teil des manuellen Kurations-Workflows überprüfen.

Bei einem Konto mit deaktiviertem Soziales Lernen werden keine Kenntnisse angezeigt. Die Suchleiste ist auch für solche Konten verfügbar, sodass der Administrator die Möglichkeit hat, nach Kenntnissen zu suchen und SMEs hinzuzufügen.

Der Administrator kann die Aktivitätsbewertung, die Anzahl der Beiträge, Boards, Benutzer und den Namen der SMEs für jede Qualifikation anzeigen, die beim Erstellen eines Boards oder Beitrags verwendet wurde.

<!--![](assets/modify-smes-2.png)-->

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Sl Nein.</b></p></td>
   <td>
    <p><b>Spaltenname</b></p></td>
   <td>
    <p><b>Erläuterung</b></p></td>
  </tr>
  <tr>
   <td>
    <p>1</p></td>
   <td>
    <p>Qualifikationsname</p></td>
   <td>
    <p>Zeigt die Namen der Kenntnisse an, die im Sozialen Lernen verwendet werden.</p></td>
  </tr>
  <tr>
   <td>
    <p>2</p></td>
   <td>
    <p>Punktzahl für Aktivität</p></td>
   <td>
    <p>Zeigt die Summe der Aktivitätspunkte aller Boards an, die zu Kenntnissen gehören.</p></td>
  </tr>
  <tr>
   <td>
    <p>3</p></td>
   <td>
    <p>Beiträge</p></td>
   <td>
    <p>Zeigt die Gesamtzahl der Beiträge an, die mit Kenntnissen erstellt wurden.</p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>Boards</p></td>
   <td>
    <p>Zeigt die Gesamtzahl der Boards an, die mit Kenntnissen erstellt wurden.</p></td>
  </tr>
  <tr>
   <td>
    <p>5</p></td>
   <td>
    <p>Benutzer</p></td>
   <td>
    <p>Zeigt die Gesamtzahl der Teilnehmer an, die diese Kenntnisse verwendet haben.</p></td>
  </tr>
  <tr>
   <td>
    <p>6</p></td>
   <td>
    <p>KMU</p></td>
   <td>
    <p>Zeigt die aktuellen Top-3-SMEs für diese Kenntnisse an. Der Administrator kann SMEs hinzufügen oder ändern, indem er auf den Link klickt.</p></td>
  </tr>
 </tbody>
</table>

## Kompetenzdomäne {#skilldomain}

Basierend auf den hauptsächlich von Lernmanager-Endbenutzern verwendeten Kenntnissen hat Adobe Learning Manager eine Liste von 25 Kenntnisdomänen kategorisiert, die das automatische Kurationssystem zum Kuratieren von Inhalten verwendet. Der Administrator muss die konfigurierten Enterprise-Kenntnisse den von Prime bereitgestellten Kenntnisdomänen zuordnen. Die Zuordnung von Kenntnissen kann auf der Seite &quot;Administratorkenntnisse&quot; erfolgen, während Sie Kenntnisse erstellen oder vorhandene Kenntnisse ändern. Weitere Informationen zum Zuordnen oder Hinzufügen von Kenntnissen: [hier klicken](skills-levels.md#Createaskillandalevel).

+++Liste der Kenntnisdomänen, die vom Kurationssystem des Lern-Managers verwendet werden

1. Buchhaltung
1. Analytics
1. Geschäftsethik
1. Wirtschaftsrecht
1. Geschäftsprozess
1. Computersicherheit
1. Customer Relationship Management
1. Design
1. Finanzwesen
1. Personalmanagement
1. Informationstechnologie
1. Lernressourcen
1. Management
1. Marketing
1. Medizin
1. Produktion und Fertigung
1. Qualitätsmanagement
1. Vertrieb
1. Wissenschaftliche Forschung und Ingenieurwesen
1. Social Media
1. Soft Skills
1. Strategisches Management
1. Supply Chain Management
1. Technische Kommunikation
1. Sicherheit am Arbeitsplatz

+++

## Fachexperten (KMU) {#subjectmatterexpertssmes}

**Fachexperten** sind Menschen, die über ein beträchtliches Wissen und Fachwissen in Bezug auf ihre Fähigkeiten verfügen. Ein **KMU** spielt eine wichtige Rolle beim sozialen Lernen, wenn der Administrator die Kurationseinstellungen als manuell festgelegt hat oder wenn die automatische Kurationsmethode den Inhalt nicht kuratieren kann. Nur die drei besten SME werden in der Spalte SME angezeigt.

## Voraussetzungen für KMU {#requirementstobeansme}

Der KMU-Status kann nur erworben werden, indem KMU-Punkte durch Aktivitäten im Bereich Soziales Lernen gesammelt werden. Der Administrator kann einem SME basierend auf seinem Fachwissen Punkte zuweisen.

## Hinzufügen von SME zu Kenntnissen {#addingsmestoaskill}

Um SMEs zu Kenntnissen hinzuzufügen, führen Sie die folgenden Schritte aus:

1. Klicken **[!UICONTROL SME hinzufügen]** oder **[!UICONTROL SME ändern]**.

   ![](assets/add-smes-06.png)

   *SME hinzufügen oder ändern*

1. Klicken **[!UICONTROL Erweiterte Optionen]** aus dem Popup-Dialogfeld.

   ![](assets/advanced-optionssmes.png)

   *Dialogfeld &quot;Erweiterte Optionen&quot; anzeigen*

1. Suchen Sie nach dem Benutzer mit Fachkenntnissen. Nachdem der Benutzer gefunden wurde, geben Sie die Anzahl der Punkte ein, die Sie ihm in der **Punkte hinzufügen** Eingabefeld.

   Wenn der Benutzer bereits Punkte hat, wird die Anzahl der neuen Punkte, die dem Benutzer gegeben wurden, zur aktuellen Anzahl der Punkte hinzugefügt.

   Standardmäßig ist der aktuelle Punkt für jeden neuen Benutzer von Soziales Lernen 0.

   ![](assets/advanced-options.png)

   *Punkte für einen Benutzer hinzufügen*

1. Durch Auswahl des Dialogfelds **[!UICONTROL Minimale SME-Punkte aktivieren]** können Sie einen Grenzwert für die Mindestanzahl von Punkten festlegen, die ein Benutzer benötigt, um als SME in der Liste der besten SMEs angezeigt zu werden. Sobald der Schwellenwert festgelegt ist, werden SME, deren Punkte kleiner als oder gleich dem erforderlichen Mindestpunktwert sind, nicht mehr in den SME-Listen aufgeführt.

   Wenn die Option **[!UICONTROL Minimale SME-Punkte aktivieren]** nicht aktiviert ist, werden die drei häufigsten Benutzer mit den höchsten Punkten als SME für diese bestimmten Kenntnisse betrachtet.

1. Klicken **[!UICONTROL Speichern]** , um die vorgenommenen Änderungen anzuzeigen.

## SME-Punktesystem {#smepointsystem}

**Die KMU erhalten die folgenden Punkte:**

* 2 Punkte werden einem Benutzer jedes Mal vergeben, wenn ein anderer Benutzer einen von ihm erstellten Beitrag hochlädt.
* 2 Punkte werden einem Benutzer jedes Mal gegeben, wenn ein anderer Benutzer seinen Kommentar aufwirbt.
* 5 Punkte werden einem Teilnehmer zum Beantworten einer Frage gegeben.
* 2 weitere Punkte werden dem Teilnehmer jedes Mal gegeben, wenn die angegebene Antwort eine Aufwertung erhält.

## SME-Statuspunkte basierend auf Kurationsaktivität {#smestatuspointsbasedoncurationactivity}

**KMU erhalten eine Anzahl von Punkten, die auch auf Kurationsaktivitäten für folgende Bereiche basieren:**

* Wenn ein Beitrag zur manuellen Kuration gesendet wird, weil die automatische Kuration nicht sicher ist, ob der Inhalt relevant ist oder nicht, erhält der SME 5 Punkte bei Einreichung der Moderation.

## Konfigurationen herunterladen {#downloadconfigurations}

<!--![](assets/download-config.png)-->

Bei Unternehmensservern kann der Administrator den Speicherort ändern, von dem Teilnehmer die Desktop-Anwendung sowohl für Windows als auch für Mac herunterladen können.

![](assets/enterprise-servers.png)

*Download-Speicherort ändern*

Enterprise Server-URL muss öffentlich gehostet werden.

## Abrechnungsplan für monatliche aktive Benutzer für soziale Aktivitäten {#socialactivitiesformonthlyactiveusersbillingplan}

Jedes Mal, wenn ein Benutzer ein neues soziales Board, einen sozialen Beitrag oder einen sozialen Kommentar erstellt, wird dies als gültige Aktivität gezählt, die auf die **Benutzer für die monatliche Aktivierung**(MAU) , wenn das Konto dem MAU-Abrechnungsmodell folgt. Weitere Informationen finden Sie unter [Abrechnungsmanagement](billing-management.md).

## Häufig gestellte Fragen {#frequentlyaskedquestions}

+++Wie kann Soziales Lernen für externe Teilnehmer aktiviert werden?

In **[!UICONTROL Social Learning]** > **[!UICONTROL Einstellungen]** im Abschnitt Bereichseinstellungen die Option **[!UICONTROL Für externe Teilnehmer aktivieren]**. Wählen Sie in der Dropdown-Liste ein externes Profil aus und definieren Sie den Lernbereich für dieses Profil.

![](assets/social-scope-external-users.png)

*Wählen Sie die Option Für externe Teilnehmer aktivieren aus.*
+++

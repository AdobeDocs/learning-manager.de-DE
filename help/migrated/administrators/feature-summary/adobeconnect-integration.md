---
jcr-language: en_us
title: Adobe Connect-Integration
description: Autoren können während der Erstellung von Kursen Kurse für das virtuelle Klassenzimmer über Adobe Connect erstellen. Um Adobe Connect für Ihr Learning Manager-Konto zu aktivieren, müssen Sie den Administrator Ihres Unternehmens kontaktieren.
contentowner: jayakarr
exl-id: 13458f93-9ea7-4aab-8b33-3c4f4dd5886d
source-git-commit: 857dddf46e3900fbe2db4e345da2d29050ef3c82
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 49%

---

# Adobe Connect-Integration

Die Administratoren in einem Unternehmen können die Einstellungen des Learning Manager-Kontos dahingehend konfigurieren, dass die Adobe Connect-Integration aktiviert wird.

## Adobe Connect konfigurieren {#configureadobeconnect}

1. Melden Sie sich als Administrator an und klicken Sie im linken Bereich auf **[!UICONTROL Einstellungen]**, um die grundlegenden Informationen über Ihr Unternehmen anzuzeigen. Klicken Sie im linken Fensterbereich auf **[!UICONTROL Adobe Connect]**.

   ![](assets/left-pane.png)

   *Adobe Connect im linken Fensterbereich auswählen*

1. Klicken Sie auf den Link **[!UICONTROL Jetzt konfigurieren]** im Abschnitt **[!UICONTROL Adobe Connect-Konfiguration]**.

   <!--![](assets/configure-now-connect.png)-->

1. Geben Sie den Domänennamen und die Anmeldedaten Ihres Unternehmens für Adobe Connect an.

   ![](assets/adobeconnect-config.png)

   *Domänennamen und Anmeldeinformationen hinzufügen*

   Beispiel für eine Adobe Connect-URL: mycompany.adobeconnect.com\
   Sie müssen die E-Mail-ID des Administrators des Adobe Connect-Kontos angeben.

   Nur von Adobe gehostete Connect-Konten werden in Learning Manager unterstützt. Beispiel; &#39;.adobeconnect.com&#39;.

1. Klicken Sie auf **[!UICONTROL Integrieren].**.

   Nach der Authentifizierung der E-Mail-ID zeigt Learning Manager die Meldung an, dass Connect erfolgreich integriert wurde. Sie können damit beginnen, Ihre Kurse im virtuellen Klassenzimmer automatisch über Adobe Connect anzusehen.

   Der Adobe Connect-Kontoadministrator muss die Bedingungen für die Verwendung von Adobe Connect akzeptieren. Wenn dies nicht akzeptiert wird, schlägt die Authentifizierung der Anmeldung möglicherweise fehl. Nach der Erstellung des Adobe Connect-Kontos, müssen Sie sich bei dem Konto anmelden. Bei dieser erstmaligen Anmeldung wird eine Seite mit den Bedingungen angezeigt.

   <!--![](assets/mail-confirmation.png)-->

## Informationen für Sitzung im virtuellen Klassenzimmer hinzufügen {#addvirtualclassroomsessioninformation}

Wenn der Autor eines Kurses im virtuellen Klassenzimmer keine Sitzungsinformationen angegeben hat, kann der Administrator die Sitzungsdetails einbeziehen.

Melden Sie sich als Administrator an und klicken Sie auf den Namen des Kurses im virtuellen Klassenzimmer. Klicken Sie im linken Teilfenster auf **[!UICONTROL Instanzen]** und dann auf **[!UICONTROL Sitzungsdetails]**.  Klicken Sie in der rechten Ecke der Seite &quot;Sitzungsdetails&quot; auf das Symbol &quot;Bearbeiten&quot;, um die Sitzungsinformationen hinzuzufügen.

![](assets/session-creation-admin.png)

*Sitzungsinformationen für virtuelle Klassenzimmer hinzufügen*

Mit der Integration von Adobe Learning Manager und Adobe Connect für das Erstellen von Modulen oder Sitzungen vom Typ „Virtuelles Klassenzimmer“ muss Ihr Connect-Konto Meetingräume mit einer ausreichenden Anzahl von Räumen und Benutzenden unterstützen. Diese Meetingräume werden zum Hosten von Modulen vom Typ „Virtuelles Klassenzimmer“ in Learning Manager verwendet. Ein neuer Connect-Meetingraum wird von Learning Manager für jedes Modul oder jede Sitzung vom Typ „Virtuelles Klassenzimmer“ dynamisch in Learning Manager erstellt.

Sie müssen Adobe Connect unabhängig von Adobe Learning Manager separat erwerben.

## Teilnehmeranwesenheit {#learnersattendance}

Wenn der Veranstalter des Kurses im virtuellen Klassenzimmer nicht an der Sitzung teilnimmt, wird die Anwesenheit der Teilnehmer, die an der Sitzung teilgenommen haben, nicht automatisch registriert. In solchen Fällen kann der Administrator die Anwesenheit manuell aufzeichnen.

Klicken Sie auf den Kurs im virtuellen Klassenzimmer, klicken Sie im linken Teilfenster der folgenden Seite auf &quot;Anwesenheit&quot; und erfassen Sie die Anwesenheit.

## Unterstützung für Adobe Connect-Seminare mit großem Publikum

Adobe Learning Manager unterstützt die Auswahl von Seminarräumen aus Adobe Connect beim Einrichten einer virtuellen Klassenzimmersitzung in Connect. Zuvor konnte der Administrator nur den Meetingraumtyp auswählen. Diese Funktion ermöglicht es Administratoren mit einer gültigen Seminarlizenz, einmalige oder große Veranstaltungen (bis zu 1.500 Teilnehmer) in ALM zu planen und zu verwalten.

Weitere Informationen zum Seminarraum finden Sie in diesem [Artikel](https://helpx.adobe.com/de/adobe-connect/using/creating-seminars.html).

### Unterstützung für den Zugriff auf Sitzungsanalysen

Kursleiter können für abgeschlossene Adobe Connect-Sitzungen über einen neuen Link im Session-Dashboard auf Session Analytics zugreifen.

![](assets/adobe-connect-session-url.png)
_Sitzungs-URL auswählen_

Dieser Link öffnet das Dashboard für die Sitzungsanalyse in Connect, das detaillierte Einblicke in die Sitzungsinteraktion bietet.
Diese Funktion ist nur für Sitzungen verfügbar, die über Adobe Connect durchgeführt werden. Die Sitzungsanalyse umfasst:

* **[!UICONTROL Engagement]**: Übersicht über die Gesamtleistung der Live-Sitzung
* **[!UICONTROL Interaktionen]**: Detaillierte Aufschlüsselung der Teilnehmeraktivität auf verschiedene Pods
* **[!UICONTROL Teilnehmeraktivität]**: Zusammenfassung der Teilnehmerinteraktion
* **[!UICONTROL Berichte herunterladen]**: Option zum Herunterladen von Berichten für podspezifische Interaktionsdaten

![](assets/session-dashboard.png)
_Sitzungs-Dashboard_

Weitere Informationen zur Sitzungsanalyse finden Sie in diesem [Artikel](https://helpx.adobe.com/in/adobe-connect/using/session-dashboard.html).

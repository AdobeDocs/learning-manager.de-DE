---
description: Hier erfahren Sie, wie Sie den Adobe Connect Connector mit Adobe Learning Manager integrieren.
jcr-language: en_us
title: Adobe Connect Connector
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 2%

---


# Adobe Connect-Connector in Adobe Learning Manager

## Einführung

Adobe Learning Manager ist mit Adobe Connect integriert, um die Bereitstellung und Verwaltung von Schulungen im virtuellen Klassenzimmer zu erleichtern. Mit dieser Integration können Sie Sitzungen planen, dauerhafte oder dynamische Meetingräume verwenden, die Anwesenheit erfassen, Quizergebnisse importieren und Teilnehmern Sitzungsaufzeichnungen zur Verfügung stellen.

## Adobe Connect konfigurieren

So konfigurieren Sie Adobe Connect:

1. Melden Sie sich bei Adobe Learning Manager als Integrationsadministrator an.
2. Bewegen Sie den Mauszeiger über die Kachel **Adobe Connect** und wählen Sie **Verbinden** aus.

   ![](assets/adobe-connect-connector1.png)
   _Wählen Sie &quot;Verbinden&quot; aus, um den Adobe Connect-Connector zu konfigurieren_

3. Geben Sie die folgenden Details ein:

   - **Verbindungsname**
   - **Adobe Connect-URL**
   - **Admin-E-Mail verbinden**
4. Geben Sie die **Connect Admin-Anmelde-ID** ein (erforderlich, wenn keine E-Mail-Anmeldung für Adobe Connect verwendet wird).

   ![](assets/adobe-connect-connector2.png)
   _Geben Sie die erforderlichen Details für die Adobe Connect-Konfiguration ein_

5. Wählen Sie **Connect-Authentifizierung aktivieren**.

   >[!NOTE]
   >
   >Nur von Adobe gehostete Connect-Konten werden unterstützt. (Die Domäne muss mit .adobeconnect.com enden.)

6. Wählen Sie **Verbinden**.

Nachdem Sie die Administrator-E-Mail-ID authentifiziert haben:

- Adobe Learning Manager zeigt eine Erfolgsmeldung an, die bestätigt, dass Connect integriert ist.
- Die Anforderung wird zur Genehmigung an das Adobe Connect-Backend-Team gesendet. Dies dauert in der Regel ein bis zwei Tage.

>[!IMPORTANT]
>
>Der Adobe Connect-Kontoadministrator muss die Nutzungsbedingungen akzeptieren, wenn er sich zum ersten Mal anmeldet. Ist dies nicht der Fall, schlägt die Anmeldeauthentifizierung möglicherweise fehl.

## Informationen für Sitzung im virtuellen Klassenzimmer hinzufügen

Wenn ein Autor keine Sitzungsdetails für einen Kurs im virtuellen Klassenzimmer angegeben hat, kann der Administrator sie hinzufügen:

1. Melden Sie sich als Administrator an.
2. Wählen Sie den VC-Kurs aus.
3. Wählen Sie **Instanzen** aus, und wählen Sie dann **Sitzungsdetails** aus.
4. Wählen Sie das Symbol **Bearbeiten** aus, um Sitzungsinformationen hinzuzufügen oder zu aktualisieren.

>[!NOTE]
>
>Ihr Connect-Konto muss über genügend Meetingräume und Kapazitäten für Benutzer gleichzeitig verfügen, um virtuelle Klassenzimmer auszuführen. Jede Sitzung im virtuellen Klassenzimmer von Adobe Learning Manager erstellt automatisch einen neuen Connect-Meetingraum, es sei denn, Sie verwenden einen dauerhaften Raum.

## Dauerhafte Meetingräume

Adobe Connect unterstützt dauerhafte Meetingräume, die weiterhin zur Wiederverwendung verfügbar bleiben.

- Sie können eine virtuelle Klassenzimmersitzung mit einem vorhandenen dauerhaften Raum in Connect erstellen.
- Sie können auch festlegen, dass Adobe Learning Manager stattdessen für jede Sitzung einen dynamischen Raum erstellt.

Wenn Teilnehmer mit Adobe Connect an einer Sitzung teilnehmen, betreten sie den Raum über den Lernmanager mit sicherer Authentifizierung.

Nach Abschluss einer Sitzung können die Teilnehmer auf die Sitzungsaufzeichnung und das Kennwort in ihrer Learning Manager-App zugreifen.

## Importieren von Quizpunktzahlen aus Adobe Connect

Adobe Learning Manager kann Quizdaten aus Adobe Connect-Sitzungen importieren und sie mit anderen Berichterstellungs-Workflows kombinieren. Dazu gehören Quizpunktzahlen, Teilnehmerantworten und Abschlussdaten, wie Module zum Selbststudium funktionieren.

### Workflow für Quizimport

#### Adobe Connect (Veranstalter)

- Der Connect-Veranstalter erstellt einen Kurs und lädt Inhalte hoch, die ein interaktives Quiz enthalten.
- Der Veranstalter richtet eine VC-Schulung (Virtual Classroom) ein und verknüpft den Kurs entweder mit dem VC oder verwendet die Option **Kurs freigeben**, um ihn während der Sitzung freizugeben.

#### Adobe Learning Manager (Autor)

- Der Autor erstellt einen Kurs in Adobe Learning Manager, dessen Modultyp auf **Virtuelles Klassenzimmer** festgelegt ist.
- Wählen Sie im Dropdown-Menü **Konferenzsystem** die Option **Connect** als VC-Anbieter aus.
- Wählen Sie den vom Veranstalter in Connect erstellten **dauerhaften Meetingraum** aus.
- Weisen Sie einen Kursleiter zu, speichern und veröffentlichen Sie den Kurs.

#### Adobe Learning Manager (Teilnehmer)

- Der Teilnehmer registriert sich für den Kurs und nimmt an der Connect VC-Sitzung teil.
- Der Connect-Veranstalter ermöglicht dem Teilnehmer den Zugriff auf die Sitzung.

### Adobe Connect (Veranstalter &amp; Teilnehmer)

- Der Veranstalter gibt das Quiz in der Sitzung frei.
- Der Teilnehmer schließt das Quiz ab und beendet die Sitzung.

### Adobe Learning Manager (Synchronisation und Admin)

- Wenn die Sitzung endet, synchronisiert Adobe Learning Manager die Quizdaten automatisch.
- Der Quizimport-Arbeitsablauf beginnt nach Ablauf der geplanten Dauer.
- Um den Fortschritt zu verfolgen, kann der Integrationsadministrator den **Ausführungsstatus** im Adobe Connect-Connector überprüfen.
- Sobald der Import abgeschlossen ist, wird der Status auf **Abgeschlossen** aktualisiert.

Der Administrator kann dann die importierten Ergebnisse überprüfen:

- **Anwesenheit und Punktzahl:** Zeigen Sie die endgültigen Quizergebnisse und die Anwesenheit an.
- **L2 Quizpunktzahl:**
   - **Nach Benutzer:** Zeigt einzelne Punktzahlen in Punkten und Prozentsätzen an.
   - **Nach Frage:** Zeigt Quizergebnisse in einem Berichtsdiagramm an.

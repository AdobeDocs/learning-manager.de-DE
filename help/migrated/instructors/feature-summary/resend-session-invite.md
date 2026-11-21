---
description: Erfahren Sie, wie Administratoren erneut Sitzungseinladungen an Teilnehmer senden, die in einer virtuellen Klassenzimmersitzung in Adobe Learning Manager registriert sind
jcr-language: en_us
title: Sitzungseinladung erneut senden
exl-id: 12ee20a8-4521-4235-8120-596812da7809
source-git-commit: 90b45cb128b74ecb33a89bf42ef4d6e960101ff0
workflow-type: tm+mt
source-wordcount: '1527'
ht-degree: 2%
---

# Sitzungseinladungen erneut senden

## Übersicht

>[!NOTE]
>
>Das Retrigging ist nur für VC-Sitzungen (Virtual Classroom) verfügbar. Andere Modultypen wie Klassenzimmer und Module zum Selbststudium (E-Learning) werden nicht unterstützt.

Teilnehmer können eine Einladung aus mehreren Gründen verpassen. Mit der Option **Resend** können Sie als Administrator, der über die Berechtigung zum Bearbeiten von Kursen verfügt, eine VC-Sitzung auf der Instanzseite öffnen, nach den Teilnehmern suchen und die E-Mail mit der Sitzungseinladung senden. Learning Manager sendet die E-Mail nach Bedarf außerhalb des Registrierungsereignisflusses. Der Teilnehmer erhält die Sitzungsdetails und eine Kalendereinladung, und der Registrierungsstatus bleibt unverändert.

## Anwendungsszenarien

Im Folgenden finden Sie die Anwendungsfälle, in denen Sie eine Sitzungseinladung erneut senden würden.

* **Eine versäumte Einladung wiederherstellen.** Senden Sie die Einladung erneut an einen Teilnehmer, dessen Postfach voll war, dessen E-Mail an Spam gesendet wurde oder dessen ursprüngliche E-Mail nicht zugestellt wurde.
* **Anzahl der Fehlanzeigen reduzieren.** Senden Sie die Sitzungsdetails und die Kalendereinladung direkt vor der Sitzung oder am Tag der Sitzung erneut.
* **Vermeiden Sie Problemumgehungen bei der Registrierung.** Senden Sie eine Einladung erneut, ohne die Registrierung des Teilnehmers aufzuheben und ihn erneut zu registrieren, sodass der Registrierungsstatus und die Sitzungsregistrierung intakt bleiben.
* **Support-Tickets reduzieren.** Administratoren lösen &quot;fehlende Einladungen&quot; selbst auf, ohne das Support-Team einzubeziehen.

## Voraussetzungen

* Die Sitzung ist eine VC-Sitzung.
* Der Teilnehmer wird für die Zielsitzung registriert. Der Lern-Manager sendet die Einladung nur an Teilnehmer, die für die Sitzung registriert sind.
* Die Sitzung ist bereits vorhanden. Mit dieser Funktion werden keine Sitzungen erstellt oder geändert.
* Die vorhandene E-Mail-Vorlage &quot;Sitzungseinladung&quot; wird verwendet. Mit dieser Funktion wird keine neue E-Mail-Vorlage eingeführt.

## Unterstützte Konfigurationen

| Element | Support |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Rollen | Administratoren mit der Berechtigung, den Kurs zu bearbeiten. Kursleiter für die Sitzungen, denen sie zugewiesen sind. |
| Katalogelementtypen | Kurse und Lernpfade |
| Modultyp | Sitzungen im virtuellen Klassenzimmer (VC) |
| Sitzungen | Aktuelle und zukünftige Sessions. Ältere Sitzungen werden nicht unterstützt. |
| VC-Anbieter | Alle für die Sitzung konfigurierten Anbieter wie Zoom, Teams und Adobe Connect |
| E-Mail-Vorlagen | Die für das Lernobjekt konfigurierten Vorlagen: eine E-Mail mit Sitzungsdetails und eine Kalendereinladung |
| Empfänger | Einzelne Teilnehmer, die für die Sitzung registriert sind. Benutzergruppen werden nicht unterstützt. |
| Auslöser | Manuell, über die Aktion &quot;Sitzungseinladung erneut senden&quot; |

Die Managerrolle hat in dieser Version keinen Zugriff auf diese Funktion. Die Option ist für Teilnehmer und Manager ausgeblendet.

## Auf die Einladungsaktion zum erneuten Senden der Sitzung zugreifen

Der Speicherort der Aktion hängt von Ihrer Rolle ab.

| Rolle | Wo finde ich die Aktion? |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Administrator | Öffnen Sie den Kurs oder den Lernpfad im Katalog, wechseln Sie zu &quot;Instanzen&quot; und öffnen Sie die Instanz. Suchen Sie im Bereich &quot;Sitzungen&quot; die VC-Sitzung und wählen Sie &quot;Sitzungseinladung erneut senden&quot;. Sie benötigen die Berechtigung, den Kurs zu bearbeiten. |

## Dialogfeld erneut senden

Das Dialogfeld &quot;Einladungen zur Sitzung erneut senden&quot; enthält die folgenden Elemente:

| Element | Beschreibung |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Teilnehmer wählen | Ein Suchfeld. Geben Sie den Namen oder die E-Mail-Adresse eines Teilnehmers ein, um den Teilnehmer zu finden, und wählen Sie dann den Teilnehmer aus. Sie können mehrere Teilnehmer auswählen. In einem Hinweis wird erläutert, dass jeder ausgewählte Teilnehmer zwei E-Mails erhält: eine Sitzungsdetails-E-Mail und eine Kalendereinladung basierend auf den für das Lernobjekt konfigurierten Vorlagen. |
| Cancel | Schließt das Dialogfeld, ohne E-Mails zu senden. |
| Erneut senden | Sendet die E-Mails an die ausgewählten Teilnehmer. Die Schaltfläche ist deaktiviert, bis Sie mindestens einen Teilnehmer auswählen. |

>[!NOTE]
>
>Die Suche entspricht nur einzelnen Teilnehmern. Sie können keine Benutzergruppen suchen oder auswählen.

## Einladung zur Sitzung erneut senden

Führen Sie die folgenden Schritte als Administrator aus.

1. Melden Sie sich als Administrator an, der über die Berechtigung zum Bearbeiten des Kurses verfügt.
2. Navigieren Sie zu **Lernen** > **Kurse**.

   ![](assets/resend-session-invite1.png)

3. Öffnen Sie den Kurs, auf dessen Instanzen Sie zugreifen möchten.

   ![](assets/resend-session-invite2.png)

4. Navigieren Sie zu der Instanz, auf deren Sitzung Sie zugreifen möchten.
5. Wählen Sie im folgenden Abschnitt **Sitzungsdetails** die Option **Einladung zur Sitzung erneut senden** aus.

   ![](assets/resend-session-invite3.png)

6. Das Popup **Einladung zur Sitzung erneut senden** wird geöffnet.

   ![](assets/resend-session-invite4.png)

7. Suchen Sie nach dem Teilnehmer oder den Teilnehmern, an den Sie die Einladung erneut senden möchten.

   ![](assets/resend-session-invite5.png)

   ![](assets/resend-session-invite6.png)

8. Wählen Sie **Erneut senden**. Sie sehen eine Meldung mit der Meldung &quot;An &quot;x&quot; Teilnehmer gesendete Sitzungseinladung&quot;.

   ![](assets/resend-session-invite7.png)

9. Wenn einer der ausgewählten Teilnehmer aus einer anderen Sitzung stammt, wird eine Meldung angezeigt, die besagt: &quot;X ausgewählte Teilnehmer ist für diese Sitzung nicht registriert und wurde übersprungen.&quot;

   ![](assets/resend-session-invite8.png)

10. Nach einigen Minuten erhalten die Teilnehmer eine E-Mail mit den Sitzungsdetails einschließlich eines Links für die Teilnahme an der Sitzung.

![](assets/resend-session-invite9.png)

Der Lern-Manager überprüft, ob jeder ausgewählte Teilnehmer für die Zielsitzung registriert ist, und sendet dann die bestehende Sitzungseinladung an die berechtigten Teilnehmer.

Wenn der Lern-Manager die Anforderung akzeptiert, wird das Dialogfeld geschlossen und eine Bestätigungsmeldung wird angezeigt: &quot;Einladungs-E-Mails werden an die Teilnehmer für die Sitzung gesendet. Dies kann einige Zeit in Anspruch nehmen.&quot; Die E-Mails kommen in der Regel innerhalb weniger Minuten.

## E-Mail-Inhalte

Jeder ausgewählte Teilnehmer erhält die E-Mail mit den Sitzungsdetails und die Kalendereinladung für die Sitzung. Der Inhalt enthält den VC-Sitzungs-Join-Link, das Datum und die Uhrzeit sowie die Sitzungsdetails. Die E-Mail-Adresse ist mit der ursprünglichen Sitzungseinladung identisch, da Learning Manager dieselbe Vorlage verwendet.

## Verhalten bei mehreren Registrierungen

Das erneute Senden ist spezifisch für eine Instanz. Wenn sich ein Teilnehmer für mehr als eine Instanz registriert, wird beim erneuten Senden von einer Instanz nur die Einladung für diese Instanz gesendet. Die Einladungen für die anderen Instanzen der Teilnehmer werden nicht erneut ausgelöst.

| Teilnehmerregistrierung | Aktion | Ergebnis |
|------------------------------------------------|------------------------------------------------|----------------------------------------------------------------------------------|
| Instanz A und Instanz B | Von Instanz A erneut senden | Es wird nur die Instanz-A-Einladung gesendet. |
| Nur Instanz A | Von Instanz A erneut senden | Die Einladung Instanz A wird erneut gesendet. |
| Eine andere Instanz als die ausgewählte Sitzung | Der Teilnehmer wird in der Suche auf Kursebene angezeigt | Der Lern-Manager überspringt den Teilnehmer für die ausgewählte Sitzung und zeigt eine Warnung an. |

## Verhalten in bestimmten Szenarien

| Szenario | Verhalten |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Instanz verfügt über keine VC-Sitzungen. | Die Aktion &quot;Einladung zur Sitzung erneut senden&quot; ist nicht verfügbar. |
| Die Sitzung wurde bereits ausgeführt. | Die Aktion ist nicht verfügbar. Learning Manager unterstützt nur aktuelle und zukünftige Sitzungen. |
| Sie wählen einen Teilnehmer aus, der nicht für die Sitzung registriert ist | Die Teilnehmersuche deckt den gesamten Kurs ab, sodass Sie Teilnehmer aus anderen Instanzen finden können. Der Lern-Manager überspringt Teilnehmer, die nicht für die ausgewählte Sitzung registriert sind, sendet die Einladung an die anderen und zeigt eine Warnung an. |
| Ein Teilnehmer wird in mehreren Instanzen registriert. | Der Lern-Manager sendet die Einladung nur für die Instanz, von der Sie sie senden. Es werden keine Einladungen für die anderen Instanzen gesendet. |
| Eine Lernpfadinstanz wird ausgewählt. | Die Aktion funktioniert genauso wie für eine Kursinstanz. |

## Fehlerbehandlung

Wenn ein Fehler verhindert, dass Learning Manager die E-Mails sendet, zeigt das Dialogfeld eine der folgenden Meldungen an.

| Bedingung | Nachricht |
|---------------------------------------|------------------------------------------------------------------------|
| Die Vorlage für Einladungs-E-Mails ist deaktiviert. | E-Mail kann nicht gesendet werden: Die Vorlage für Einladungs-E-Mails ist derzeit deaktiviert. |
| Jeder andere Fehler | Beim Senden der E-Mail ist ein Fehler aufgetreten. Versuchen Sie es später erneut. |

Wenn Sie Teilnehmer auswählen, die nicht für die Sitzung registriert sind, zeigt der Lern-Manager eine Warnung an, dass die Einladung für diese Teilnehmer übersprungen wurde. Die Einladung wird weiterhin an die Teilnehmer gesendet, die registriert sind.

>[!NOTE]
>
>Der E-Mail-Dienst meldet den Übermittlungsstatus asynchron an Learning Manager, nachdem das Dialogfeld geschlossen wurde.

## Einschränkungen

* Sie können Einladungen nur für aktuelle und zukünftige Sitzungen erneut senden.
* Es werden nur die Vorlagen verwendet, die für das Lernobjekt konfiguriert sind. Sie können keine andere Vorlage auswählen.
* Sie können Einladungen für jeweils eine Sitzung erneut senden. Das gleichzeitige Senden über mehrere Instanzen wird nicht unterstützt.
* Benutzergruppen können nicht ausgewählt werden. Sie können nur einzelne Teilnehmer auswählen.
* Der Lern-Manager sendet nur Einladungen an Teilnehmer, die für die ausgewählte Sitzung registriert sind.
* Das Dialogfeld zeigt nicht den Übermittlungsstatus der E-Mails an und bietet keinen Wiederholungsversuch für einzelne Teilnehmer.
* Über das Dialogfeld können Sie keine neuen Sitzungen planen oder vorhandene Sitzungsdetails bearbeiten.

## Fehlerbehebung

| Symptom | wahrscheinliche Ursache | Aktion |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Die Aktion &quot;Einladung zur Sitzung erneut senden&quot; ist nicht sichtbar | Das Modul ist keine VC-Sitzung, die Sitzung ist bereits aufgetreten, oder Sie sind nicht berechtigt, den Kurs zu bearbeiten. | Vergewissern Sie sich, dass es sich bei der Sitzung um eine aktuelle oder zukünftige VC-Sitzung handelt. Bitten Sie einen Administrator, Ihre Kursberechtigungen zu überprüfen. |
| Nach dem Senden der E-Mails wird eine Warnung angezeigt | Mindestens ein ausgewählter Teilnehmer ist für die ausgewählte Sitzung nicht registriert. | Überprüfen Sie, welche Teilnehmer für die Sitzung registriert sind, und senden Sie die Einladung erneut aus der richtigen Sitzung oder Instanz. |
| Die Einladung wird für die falsche Instanz gesendet. | Der Teilnehmer ist in mehreren Instanzen registriert und Sie senden die Einladung erneut von einer anderen Instanz. | Öffnen Sie die Instanz, die der Teilnehmer benötigt, und senden Sie die Einladung von dort aus erneut. |
| Der Fehler &quot;Die Einladungs-E-Mail-Vorlage ist derzeit deaktiviert&quot; wird angezeigt. | Die E-Mail-Vorlage für die Einladung ist für das Lernobjekt deaktiviert. | Bitten Sie einen Administrator, die Vorlage zu aktivieren, und senden Sie dann die Einladung erneut. |
| Die aktuelle E-Mail sieht genauso aus wie die ursprüngliche Einladung | Dies wird erwartet. Der Lern-Manager verwendet die vorhandene Vorlage für die Sitzungseinladung erneut. | Es ist keine Aktion erforderlich. |
| Sie müssen Einladungen erneut über mehrere Instanzen hinweg gleichzeitig senden | Dies wird nicht unterstützt. | Senden Sie die Einladungen von jeder Instanz separat erneut. |
| Sie müssen eine Einladung für ein Klassenzimmer oder ein E-Learning-Modul erneut senden | Dies wird nicht unterstützt. Ein Retrigging ist nur für VC-Sitzungen verfügbar. | Für diese Modultypen ist keine Aktion verfügbar. |
| Ein Teilnehmer sagt, dass die E-Mail nicht angekommen ist | Die E-Mail wird noch verarbeitet, das Postfach des Teilnehmers ist voll oder die E-Mail wurde als Spam gefiltert. | Warten Sie einige Minuten, bitten Sie den Teilnehmer, den Spam-Ordner zu überprüfen und Mailbox-Speicherplatz freizugeben, und senden Sie dann die Einladung erneut. |

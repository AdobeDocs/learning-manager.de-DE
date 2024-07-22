---
description: Erfahren Sie mehr über das Bereinigen von Benutzerdaten in Learning Manager.
jcr-language: en_us
title: Benutzer bereinigen
contentowner: dvenkate
exl-id: 4449146c-6247-44fb-b695-a12023c31dc6
source-git-commit: 890775dafffd3b9d717c39507490977f51f163d4
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 75%

---

# Benutzer bereinigen

Erfahren Sie mehr über das Bereinigen von Benutzerdaten in Learning Manager.

## Übersicht {#overview}

Verwenden Sie die Funktion zur Benutzerbereinigung, um personenbezogene Daten und Lerndatensätze von Benutzenden aus Learning Manager zu entfernen. Beachten Sie, dass das Löschen und das Bereinigen von Benutzern zwei unterschiedliche Funktionen sind. Während ein gelöschter Benutzer wiederhergestellt werden kann, können Benutzerdaten und Lerndatensätze, die einem bereinigten Benutzer zugeordnet sind, nicht wiederhergestellt werden.

Das Bereinigen eines Benutzers kann diese Folgen haben:

* Wenn ein Benutzer bereinigt wird, funktionieren die Links in den Importprotokollen nicht, um den Download alter CSVs und das erneute Einbinden der Benutzerdaten in das System zu vermeiden.
* Wenn ein Autor gelöscht wird, wird sein Name durch den Namen des Administrators ersetzt, der diesen Benutzer gelöscht hat.
* Wenn Kursleiter bereinigt werden, werden sie aus den Sitzungen entfernt. Der Administrator muss Kursleiter für solche Sitzungen ersetzen/hinzufügen.
* Durch das Bereinigen eines Benutzers in Learning Manager wird der Benutzer nicht in externen Anwendungen (von Drittanbietern oder anderen von Ihnen geschriebenen Anwendungen) entfernt. Wenden Sie sich an die Eigentümer der externen Anwendung, um die Benutzer daraus zu entfernen.
* Wenn ein bereinigter Benutzer in den Konfigurationseinstellungen eines Connectors referenziert wird, wird der Connector deaktiviert. Der Connector muss vom Administrator neu konfiguriert werden, um fortzufahren.

<!---### Manage users

In this training, you will learn how to assign and remove roles, send a welcome email, and delete and purge users. 

[![button](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&sdid=4X3B8VJ2&mv=display&mv2=display#/course/7555586)

If you're unable to launch the training, write to <almacademy@adobe.com>.-->

## Benutzer bereinigen

Führen Sie die folgenden Schritte aus, um Benutzer zu bereinigen:

1. Klicken Sie als Administrator im linken Bereich auf **[!UICONTROL Benutzer]**. Die Seite **[!UICONTROL Interne Benutzer]** wird geöffnet.
1. Löschen Sie die Benutzer, die Sie bereinigen möchten. Wählen Sie dafür einen oder mehrere Benutzer über das Kontrollkästchen aus. Öffnen Sie das Dropdown-Menü **[!UICONTROL Aktion]** und wählen Sie **[!UICONTROL Benutzer löschen.]**
1. Klicken Sie im linken Bereich auf **[!UICONTROL Benutzerbereinigung]**. Die Seite **[!UICONTROL Benutzerbereinigung]** mit der Liste der gelöschten Benutzer wird angezeigt. Wählen Sie über die Optionsfelder den Benutzer aus, der bereinigt werden soll. Sie können jeweils nur einen Benutzer bereinigen.

   ![](assets/purge-1.png)

   *Benutzer zum Bereinigen auswählen*

1. Öffnen Sie das Dropdown-Menü **[!UICONTROL Aktionen]** und wählen Sie **[!UICONTROL Benutzer bereinigen]**.

   ![](assets/purge-2.png)

   *Option &quot;Benutzer bereinigen&quot; auswählen*

1. Sie werden in einem Dialogfeld zur Bestätigung der Aktion aufgefordert. Nach der Bereinigung sind alle Benutzerdaten und Lerndatensätze, die mit dem ausgewählten Benutzer verknüpft sind, dauerhaft gelöscht. Die Aktion kann nicht rückgängig gemacht werden. Klicken Sie zum Bestätigen auf **[!UICONTROL Bereinigen]**.

   ![](assets/purge-3.png)

   *Bestätigungsmeldung nach Bereinigung eines Benutzers*

1. Sobald Sie bestätigen und auf „Bereinigen“ klicken, wird die Bereinigungsanforderung akzeptiert. Sie erhalten eine Benachrichtigung, sobald die Aktion abgeschlossen ist. Eine Bereinigungsanforderungs-ID wird ebenfalls angegeben. Sie können diese ID an den CSM senden, um die Anfrage zu verfolgen.

## Massenbereinigung von Benutzern

Sie können die ersten 50 Benutzer auswählen und dann in einem einzigen Arbeitsgang bereinigen. Dadurch können Administratoren 50 Benutzer gleichzeitig auswählen und gemeinsam bereinigen. Dies unterstützt die Administratoren bei der Massenbereinigung von Benutzern. Es empfiehlt sich immer, die zum Bereinigen ausgewählten Benutzer zu überprüfen. Damit wird sichergestellt, dass nur die tatsächlich betroffenen korrekten Benutzer bereinigt werden.

![](assets/bulk-purge-users.png)

*Benutzer massenweise bereinigen*

+++Informationen zu den Ergebnissen der Aktion &quot;Benutzer bereinigen&quot;

<table>
 <tbody>
  <tr>
   <th><strong>Bereinigen über die Learning Manager-Benutzeroberfläche – Unternehmen</strong></th>
   <th> </th>
  </tr>
  <tr>
   <td>Löschen ausgewählter Benutzer aus dem anfordernden Unternehmenskonto.<br></td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Löschen aller Benutzer aus allen Testkonten, deren E-Mail-Adresse und Adobe-ID mit der E-Mail-Adresse der ausgewählten Benutzer übereinstimmt.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Löschen aller Benutzer aus allen Testkonten, deren E-Mail-Adresse und Adobe-ID mit der E-Mail-Adresse der ausgewählten Benutzer übereinstimmt und bei denen die Benutzer das Testkonto erstellt haben.</td>
   <td>Nein</td>
  </tr>
  <tr>
   <td>Löschen der E-Mail-Adresse des Benutzers aus allen anderen Feldern des anfordernden Unternehmenskontos und aller Testkonten.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Senden der Löschbestätigung an den Initiator.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td><strong>Bereinigung über die Lern-Manager-Benutzeroberfläche - keine Unternehmen</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Löschen des ausgewählten Benutzers aus dem anfordernden Testkonto.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Löschen aller Benutzer aus allen Testkonten, deren E-Mail-Adresse und Adobe-ID mit der E-Mail-Adresse der ausgewählten Benutzer übereinstimmt.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Löschen aller Benutzer aus allen Testkonten, deren E-Mail-Adresse und Adobe-ID mit der E-Mail-Adresse der ausgewählten Benutzer übereinstimmt und bei denen die Benutzer das Testkonto erstellt haben.</td>
   <td>Nein</td>
  </tr>
  <tr>
   <td>Löschen der E-Mail-Adresse des Benutzers aus allen anderen Feldern aller Testkonten.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Senden der Löschbestätigung an den Initiator.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td><strong>Bereinigung anderer Benutzer - Unternehmen (Personen, die keine internen oder externen Learning Manager-Benutzer sind)</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Löschen des ausgewählten Benutzers aus allen anderen Feldern des anfordernden Unternehmenskontos und aller Testkonten.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Löschen von Benutzern aus Konten.</td>
   <td>Nein</td>
  </tr>
  <tr>
   <td>Senden der Löschbestätigung an den Initiator. </td>
   <td>Ja</td>
  </tr>
  <tr>
   <td><strong>Bereinigung</strong> <strong>anderer Benutzer - keine Unternehmen (Personen, die keine internen oder externen Learning Manager-Benutzer sind)</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Löschen des ausgewählten Benutzers aus allen anderen Feldern aller Testkonten.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Löschen von Benutzern aus Konten.</td>
   <td>Nein</td>
  </tr>
  <tr>
   <td>Senden der Löschbestätigung an den Initiator.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td><strong>Bereinigen mit Adobe IMS – Unternehmen</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Benachrichtigen des Unternehmensadministrators über die Anfrage.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Aktivieren von E-Mail-Feldern zum Senden von Benachrichtigungen.</td>
   <td>Nein</td>
  </tr>
  <tr>
   <td><strong>Bereinigen mit Adobe IMS – keine Unternehmen</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Löschen aller Benutzer mit der angegebenen Adobe-ID/E-Mail-Adresse aus allen Testkonten.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Löschen Benutzer eines Testkontos, wenn die angegebene E-Mail-Adresse/Adobe-ID der Ersteller des Kontos war.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Löschen der ausgewählte E-Mail-ID aus allen anderen Feldern aller Testkonten.</td>
   <td>Ja</td>
  </tr>
 </tbody>
</table>

+++

Learning Manager ist jetzt mit der DS-GVO konform. Weitere Informationen zur DSGVO-Konformität finden Sie unter [Learning Manager-Konformität mit der DSGVO](../../kb/prime-gdpr.md).

## Häufig gestellte Fragen {#frequentlyaskedquestions}

+++Wie viele Tage dauert es, bis eine Bereinigungsanforderung abgeschlossen ist?

Eine Anforderung zum Bereinigen von Benutzern dauert maximal 30 Tage.
+++

+++Können Sie eine Massenbereinigung in Learning Manager durchführen?

Ja, Sie können eine Massenbereinigung durchführen. Sie können jedoch nur eine Massenbereinigung von 50 Benutzern durchführen.
+++

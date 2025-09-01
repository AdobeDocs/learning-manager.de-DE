---
jcr-language: en_us
title: Benutzerdefinierte Rollen
description: Mit der Lernpfadfunktion können Sie benutzerdefinierte Rollen definieren und einer Gruppe von Benutzern bestimmte Verantwortlichkeiten zuweisen. Mit dieser Funktion können Sie Verantwortlichkeiten zuweisen, die nicht in den Bereich der bestehenden Rolle der Person fallen.
contentowner: dvenkate
exl-id: dcc84f91-4e51-4ae2-b7cb-9eb29b398bc1
source-git-commit: 9304c303d0be20e04aad2c0bc2092d1eaffaf53e
workflow-type: tm+mt
source-wordcount: '3466'
ht-degree: 32%

---

# Benutzerdefinierte Rollen

Mit dieser Funktion können Sie benutzerdefinierte Rollen definieren und bestimmten Benutzergruppen bestimmte Verantwortlichkeiten zuweisen. Mit dieser Funktion können Sie Verantwortlichkeiten zuweisen, die nicht in den Bereich der bestehenden Rolle der Person fallen.

Sie können eine benutzerdefinierte Rolle erstellen, um Authoring-Funktionen für einen bestimmten Katalog bereitzustellen. Sie können auch eine dedizierte Rolle erstellen, um Berichterstellung zu verwalten. Solche Rollen können dann Personen zugeordnet werden, die diese spezifischen Aufgaben übernehmen sollen.

>[!NOTE]
>
>Das Hinzufügen einer neuen benutzerdefinierten Rolle hat keine Auswirkungen auf vorhandene benutzerdefinierte Benutzergruppen oder rollenbasierte Gruppen wie Alle Administratoren, Alle Autoren usw.

Administratoren haben die Möglichkeit, benutzerdefinierte Administrator- und Autorenrollen mit maßgeschneiderten Berechtigungen für jede Rolle zu erstellen. Im Folgenden finden Sie einen Überblick über die Berechtigungen, die jeder Rolle zugeordnet sind:

**Benutzerdefinierte Autorenrollenberechtigungen**

Benutzerdefinierte Autoren können die folgenden Aufgaben ausführen:

* Zugriff auf die Inhaltsbibliothek zum Hinzufügen, Bearbeiten oder Löschen von Kerninhalten.
* Erstellen, Bearbeiten und Löschen:
   * Kurse
   * Arbeitshilfen
   * Zertifizierungen
   * Lernpfade
   * Lernpläne

Administratoren und Autoren, einschließlich benutzerdefinierter Administratoren und benutzerdefinierter Autoren, haben die Möglichkeit, Lernobjekte (LOs) für extern freigegebene Kataloge freizugeben. Administratoren und Autoren sollten in der Lage sein, beim Erstellen von Lernobjekten nach extern freigegebenen Katalogen zu suchen.

**Benutzerdefinierte Administratorrollenberechtigungen**

Die benutzerdefinierte Administratorrolle repliziert eine Reihe von Administratoraufgaben, einschließlich des Zugriffs auf Berechtigungen auf Kontoebene. Benutzerdefinierte Administratoren erhalten Berechtigungen zum Verwalten wichtiger Funktionen im Zusammenhang mit Lernaktivitäten, z. B.:

* Lernpläne
* Kataloge
* Berichte
* Tags

Darüber hinaus können benutzerdefinierte Administratoren:

* Verwalten Sie Kurse und Arbeitshilfen, einschließlich der Registrierung und des Löschens von Benutzern.
* Zertifizierungen, Lernpfade und Lernpläne erstellen, bearbeiten und löschen.
* Greifen Sie auf Berichts- und Registrierungsfunktionen für alle Lernobjekte (LOs) zu.

Administratoren können jetzt in Adobe Learning Manager Berechtigungen anzeigen, die mit CSV erstellt wurden. Die Option &quot;Filtern nach&quot; filtert benutzerdefinierte Rollen nach vom Administrator erstellten und über eine CSV importierten Rollen. Nachdem Sie eine benutzerdefinierte Rolle ausgewählt haben, werden die Berechtigungen angezeigt.

![](assets/filter.png)
_Benutzerdefinierte Rollen filtern_

## Benutzerdefinierte Rolle erstellen {#create-role}

1. Melden Sie sich als Administrator an. Öffnen Sie **[!UICONTROL Benutzer]** > **[!UICONTROL Benutzerdefinierte Rolle]**.
2. Wählen Sie **[!UICONTROL Rolle erstellen]** aus. Die Registerkarte **[!UICONTROL Neue Rolle erstellen]** wird geöffnet.

   ![](assets/create-new-role.png)

   *Benutzerdefinierte Rolle erstellen*

3. Geben Sie den Namen in das Feld &quot;**[!UICONTROL Name&quot; der Rolle &quot;]**&quot; ein.
4. **[!UICONTROL Kontoberechtigungen]**: Diese Berechtigungen gewähren den Rolleneigentümern Zugriff auf bestimmte Systemkonfigurationsaspekte, die für das gesamte Konto gelten. Wählen Sie die Zugriffsberechtigungen. Der Benutzer hat die volle Kontrolle über die zugewiesenen Berechtigungen.

   Administratoren können detaillierte Berechtigungen für den Abschnitt &quot;Benutzer&quot; erteilen, der interne/externe Benutzer, Benutzergruppen und erweiterte Benutzer enthält.

   >[!NOTE]
   >
   >   Der Geltungsbereich gilt nicht für diese Berechtigungen.


   ![](assets/account-privileges.png)

   *Bereich festlegen*

5. **Funktionsberechtigungen - Kernfunktionen**: Wird verwendet, um Zugriff auf bestimmte Funktionen zum Verwalten von Lernaktivitäten zu gewähren. Über diese Option können Berechtigungen für die folgenden Funktionen erteilt werden.

   Administratoren können detaillierte Berechtigungen wie schreibgeschützte Berechtigungen zum Erstellen, Bearbeiten und Löschen von Berechtigungen für die Kataloge bereitstellen.

   * Kataloge
   * Berichte
   * Tags

   ![](assets/core-features.png)

   *Umfang für Kataloge, Berichte und Tags festlegen*

6. **Funktionsberechtigungen - Lernobjekte:** Verwenden Sie diese Option, um Zugriff auf LOs-bezogene Funktionen zu gewähren. Administratoren können detaillierte Berechtigungen für alle Lernobjekte bereitstellen, einschließlich Kursen, Lernpfaden, Zertifizierungen und Arbeitshilfen. Sie können Benutzern Berechtigungen wie Erstellen, Bearbeiten, Löschen oder schreibgeschützten Zugriff zuweisen.

   * Zertifizierungen
   * Kurse
   * Arbeitshilfen
   * Lernprogramme

   Sie können den Lernobjekten auch eine bestimmte Vorgangskontrolle zuweisen. Die Berechtigung kann eine der folgenden sein:

   * Schreibgeschützt
   * Erstellen
   * Bearbeiten
   * Löschen
   * Registrierung
   * Bericht

   Sie können auch die vollständige Kontrolle über die LOs gewähren.

   ![](assets/learningobjects.png)

   *Gewähren bestimmter Berechtigungen*

7. **Umfang für Funktionsberechtigungen:** Der Umfang der Funktionsberechtigungen, die dieser Rolle zugewiesen sind, kann auf eine bestimmte Benutzergruppe oder einen oder mehrere Kataloge beschränkt werden.

   Kataloge: Verwenden Sie das Optionsfeld, um die Kontrolle über **[!UICONTROL Alle Kataloge]** bereitzustellen, oder verwenden Sie die Option **[!UICONTROL Zugriff über Katalog festlegen]**, um den Zugriff auf bestimmte Kataloge zu ermöglichen. Sie können auch mehrere Kataloge auswählen.

   Benutzergruppen: Gewähren Sie Zugriff auf **[!UICONTROL Alle Benutzergruppen]** oder verwenden Sie die Option **[!UICONTROL Zugriff auf Benutzergruppe festlegen]**, um den Zugriff auf bestimmte Benutzergruppen zu ermöglichen. Es kann nur eine einzige Benutzergruppe angegeben werden.

   >[!NOTE]
   >
   >Wenn Sie &quot;Ankündigung&quot;, &quot;Gamifizierung&quot;, &quot;E-Mail-Vorlagen&quot;, &quot;Kenntnisse&quot; und &quot;Benutzer&quot; unter &quot;Kontoberechtigungen&quot; ausgewählt haben, wird der Benutzergruppenzugriff standardmäßig für alle Benutzergruppen bereitgestellt, und diese Option ist deaktiviert.

   Wenn Sie unter „Kontoberechtigungen“ „Lernpläne“ ausgewählt haben, wird standardmäßig der Zugriff auf alle Kataloge und Benutzergruppen bereitgestellt, und diese Optionen sind unter „Umfang“ deaktiviert.

   ![](assets/define-scope-of-privileges.png)

   *Umfang der Berechtigungen definieren*

>[!NOTE]
>
>   In Learning Manager 27.6 können Sie eine benutzerdefinierte Rolle erstellen, die über mehrere Kataloge erweitert werden soll, wobei jedem Katalog unterschiedliche Berechtigungen erteilt werden.


Führen Sie die folgenden Schritte aus, um den Katalogen verschiedene Berechtigungen zu erteilen:

1. Klicken Sie auf die Option **[!UICONTROL Zugriff pro Katalog festlegen]**.
1. Wählen Sie die Kataloge aus, und Sie können die Berechtigungsstufe für jeden Katalog anzeigen. Folgende Berechtigung stehen zur Verfügung:

   <table>
        <tbody>
        <tr>
          <td>
          <p><b>Berechtigung</b></p></td>
          <td>
          <p><b>Beschreibung</b></p></td>
        </tr>
        <tr>
          <td>
          <p>Vollständige Kontrolle</p></td>
          <td>
          <p>Gewährt volle Kontrolle auf alle Lernobjekte. Zu den Berechtigungen gehören Hinzufügen, Bearbeiten, Löschen, Lesen, Registrieren und Bericht.<br></p></td>
        </tr>
        <tr>
          <td>
          <p>Bericht</p></td>
          <td>
          <p>Erteilt nur Zugriff auf die Registerkarte „Berichte“ des Lernobjekts.</p></td>
        </tr>
        <tr>
          <td>
          <p>Registrieren</p></td>
          <td>
          <p>Erteilt die Berechtigung, sich nur für das Lernobjekt anzumelden.</p></td>
        </tr>
        <tr>
          <td>
          <p>Schreibgeschützt</p></td>
          <td>
          <p>Erteilt die Berechtigung, nur die Lernobjekte im Katalog anzuzeigen.</p></td>
        </tr>
        </tbody>
      </table>

1. Aktivieren oder deaktivieren Sie die Berechtigungen gemäß Ihren Anforderungen.
1. Um die Änderungen zu speichern, klicken Sie auf **[!UICONTROL OK]**. Klicken Sie anschließend auf **[!UICONTROL Speichern]**, um die Änderungen für die benutzerdefinierte Rolle zu speichern.

Betrachten Sie beispielsweise das folgende Szenario.

Die resultierende Berechtigung, die ein benutzerdefinierter Benutzer für ein Lernobjekt haben würde, ist eine Schnittmenge aus der Berechtigung für Lernobjekte und der Katalogberechtigung.

Ein benutzerdefinierter Benutzer verfügt über die vollständige Berechtigung für Kurse und nur über den schreibgeschützten Zugriff auf Katalog A, aber über die vollständige Berechtigung für Katalog B. Die Ergebnisse sind ein Zugriff „Schreibgeschützt“ auf die Kurse von Katalog A und volle Kontrolle über die Kurse von Katalog B.

Ein Benutzer mit einer benutzerdefinierten Rolle kann Folgendes:

* Nur Inhalte aus den Katalogen anzeigen, auf die er Zugriff hat.
* Greifen Sie auf jedes Lernobjekt zu, basierend auf den Berechtigungen des Katalogs, zu dem das Lernobjekt gehört.

  Als Administrator haben Sie folgende Möglichkeiten:

* Wählen Sie mehr als einen Katalog für eine benutzerdefinierte Rolle.
* Ändern Sie die Berechtigungen eines Katalogs jederzeit.
* Entfernen Sie die Kataloge aus einem Bereich, für den Sie keine Berechtigungen mehr erteilen möchten.
* Erteilen Sie einem Katalog implizit die Berechtigung „Schreibgeschützt“, wenn Sie Berechtigungen für den Katalog erteilen.

  Die folgende Tabelle zeigt, wie Berechtigungen erteilt werden.

  <table>
    <tbody>
     <tr>
      <td>
       <p><strong> </strong></p></td>
      <td>
       <p><strong>Genehmigung auf Katalogebene</strong></p></td>
     </tr>
     <tr>
      <td>
       <p><strong>Berechtigung auf Lernobjektebene</strong></p>
       <p><strong>(Z. B.: Kurse)</strong></p></td>
      <td>
       <p>Vollständige Kontrolle</p></td>
      <td>
       <p>Registrieren</p></td>
      <td>
       <p>Bericht</p></td>
      <td>
       <p>Schreibgeschützt</p></td>
     </tr>
     <tr>
      <td>
       <p>Vollständige Kontrolle</p></td>
      <td>
       <p>Vollständige Kontrolle</p></td>
      <td>
       <p>Registrieren</p></td>
      <td>
       <p>Bericht</p></td>
      <td>
       <p>Schreibgeschützt</p></td>
     </tr>
     <tr>
      <td>
       <p>Registrieren</p></td>
      <td>
       <p>Registrieren</p></td>
      <td>
       <p>Registrieren</p></td>
      <td>
       <p>Schreibgeschützt</p></td>
      <td>
       <p>Schreibgeschützt</p></td>
     </tr>
     <tr>
      <td>
       <p>Bearbeiten &amp; Löschen</p></td>
      <td>
       <p>Bearbeiten &amp; Löschen</p></td>
      <td>
       <p>Schreibgeschützt</p></td>
      <td>
       <p>Schreibgeschützt</p></td>
      <td>
       <p>Schreibgeschützt</p></td>
     </tr>
     <tr>
      <td>
       <p>Bericht</p></td>
      <td>
       <p>Bericht</p></td>
      <td>
       <p>Schreibgeschützt</p></td>
      <td>
       <p>Bericht</p></td>
      <td>
       <p>Schreibgeschützt</p></td>
     </tr>
    </tbody>
   </table>

1. **Benutzer:** Verwenden Sie diese Option, um festzulegen, welche Benutzer dieser Rolle zugewiesen sind. Sie können einen oder mehrere Benutzer über das Suchfeld auswählen.

   **Benutzer zu CSV-Upload für benutzerdefinierte Rolle hinzufügen:** Um Benutzer über hochgeladene CSV hinzuzufügen, fügen Sie der CSV-Datei, die der Administrator zum Importieren von Benutzern verwendet hat, eine Spalte für benutzerdefinierte Rollen hinzu. Geben Sie die Rolle des Benutzers in der Spalte Benutzerdefinierte Rolle für die Benutzer ein, denen Sie eine benutzerdefinierte Rolle zuweisen möchten. Klicken Sie zum Hochladen der CSV-Datei auf **[!UICONTROL Hinzufügen > CSV hochladen]**.

   * Sie können keine Benutzergruppen durchsuchen.
   * Sie können keine Benutzer durchsuchen, denen bereits eine Administratorrolle zugewiesen wurde.
   * Die Zuweisung einer neuen benutzerdefinierten Rolle zu einem Benutzer überschreibt die vorherige benutzerdefinierte Rolle des Benutzers.

   <!--![](assets/users.png)-->

   * Ein benutzerdefinierter Administrator, der die Berechtigung für Einstellungen hat, kann den Zeitplan für die Synchronisierung oder die Synchronisierung von Benutzern aus der Datenquelle konfigurieren, auch wenn er keine Berechtigung für die Entität &quot;Benutzer&quot; hat.
   * Wenn ein benutzerdefinierter Administrator über Berechtigungen für die Entität &quot;Benutzer&quot; verfügt, können sie sich selbst eine Administratorrolle zuweisen und ein Standardadministrator werden.

## Benutzer mehrere benutzerdefinierte Rollen zuweisen

Sie können Benutzern auf folgende Weise mehrere benutzerdefinierte Rollen zuweisen:

* Verwenden der Benutzeroberfläche: Sie können einem Benutzer direkt über die Adobe Learning Manager-Oberfläche mehr als eine benutzerdefinierte Rolle zuweisen.
* CSV-Upload verwenden: Sie können eine CSV-Datei hochladen, um mehreren Benutzern gleichzeitig mehrere benutzerdefinierte Rollen zuzuweisen.

Dies erleichtert die Verwaltung des Benutzerzugriffs und die Kontrolle der Berechtigungen im gesamten System.

### Mehrere benutzerdefinierte Rollen über die Benutzeroberfläche zuweisen

Die Zuweisung mehrerer benutzerdefinierter Rollen über die Admin Console in Adobe Learning Manager ist eine schnelle und intuitive Option, die sich ideal für Onboarding, Berechtigungsanpassungen oder kleinere Aktualisierungen eignet. Rollen können visuell zugewiesen werden, ohne dass CSV-Uploads erforderlich sind. Dadurch wird das Fehlerrisiko verringert und die Anzeige in Echtzeit verbessert. Diese Methode unterstützt schnelle Aktualisierungen, wenn sich die Zuständigkeiten ändern, und ermöglicht Rollenwechsel und Delegierung nach Bedarf.

Führen Sie die folgenden Schritte aus, um einem Benutzer mehrere benutzerdefinierte Rollen zuzuweisen:

1. Melden Sie sich als Administrator an und wählen Sie **[!UICONTROL Benutzer]**.
2. Wählen Sie im linken Bereich **[!UICONTROL Benutzerdefinierte Rollen]** aus.
3. Erstellen Sie eine neue benutzerdefinierte Rolle und fügen Sie Kontoberechtigungen, Kataloge, Lernobjekte oder Bereiche hinzu. Lesen Sie die hier aufgeführten [Schritte](#create-a-custom-role).
4. Benutzer zur benutzerdefinierten Rolle hinzufügen.

   ![](assets/add-users-in-custom-roles.png)
   _Benutzer einer benutzerdefinierten Rolle zuweisen_

5. Wählen Sie **[!UICONTROL Speichern]**.

Wählen Sie je nach Bedarf mehrere benutzerdefinierte Rollen für einen Benutzer aus. Jeder Benutzer kann bis zu 50 benutzerdefinierte Rollenzuweisungen haben. Die Anzahl der verfügbaren Rollen nimmt mit jeder Zuweisung ab.

Nachdem Sie Benutzer einer zusätzlichen benutzerdefinierten Rolle zugewiesen haben, können Sie anzeigen, wie viele Rollenzuweisungen für die einzelnen Benutzer noch verfügbar sind.

>[!NOTE]
>
>Sie können jedem Benutzer bis zu 50 Rollen zuweisen und jeder Rolle bis zu 500 Benutzer hinzufügen.

### Mit CSV mehrere benutzerdefinierte Rollen zuweisen

Das Hochladen einer CSV-Datei in Adobe Learning Manager ermöglicht die effiziente Massenzuweisung benutzerdefinierter Rollen. Dieser Prozess ist besonders nützlich für das Onboarding einer großen Anzahl von Mitarbeitern, die Neuorganisation von Teams oder die Aktualisierung des Zugriffs auf neue Schulungen. CSV-Importe sparen manuellen Aufwand, gewährleisten konsistente Zuweisungen und reduzieren Fehler. Diese Methode ist besonders bei Fusionen, abteilungsweiten Updates oder globalen Schulungen nützlich. Mit dieser Methode können Administratoren Zeit sparen, Rollen standardisieren und die Governance sicherstellen.

Sie können einem Benutzer jetzt über den CSV-Import mehrere Rollen zuweisen, indem Sie zwei Dateien in Box hochladen:

* [role.csv](assets/role.csv)
* [user_role.csv](assets/user_role.csv)

Die Datei &quot;user_role.csv&quot; enthält die Felder Benutzerdefinierte Rolle und Benutzer-IDs.

Die Datei role.csv enthält die Felder, benutzerdefinierte Rolle, Quelle der Erstellung und detaillierte Informationen für Kataloge, Benutzer, Kurse, Lernpfade und mehr.

Wenn die CSV-Datei falsche Daten enthält oder die Grenzwerte überschreitet (50 Rollen pro Benutzer und 500 Benutzer pro Rolle), wird eine Meldung mit den Fehlern angezeigt.

![](assets/error-custom-role.png)
_Fehlerbenachrichtigung für benutzerdefinierte Rollen_
Benutzer erhalten E-Mail-Benachrichtigungen, wenn Rollen zugewiesen werden, einschließlich des Namens der Rolle.

### Benutzerdefinierte Rollen verwalten

Administratoren können benutzerdefinierte Rollen für Benutzer in Adobe Learning Manager aktualisieren, hinzufügen oder entfernen, wenn sich die Zuständigkeiten ändern. Dadurch wird sichergestellt, dass der Zugriff den aktuellen Rollen entspricht, ohne den Lernverlauf oder die Registrierungsdaten zu beeinträchtigen. Auf der Seite &quot;**[!UICONTROL Benutzer]**&quot; kann der Administrator nach Benutzern suchen, deren Rollen anzeigen und diese mithilfe der Option &quot;Benutzerdefinierte Rollen verwalten&quot; anpassen. Diese geführte Oberfläche ermöglicht das einfache Hinzufügen oder Entfernen von Rollen bei gleichzeitiger Aufrechterhaltung von Governance und Sicherheit.

>[!NOTE]
>
>Benutzerdefinierte Administratoren können benutzerdefinierte Rollen nicht verwalten (benutzerdefinierte Rolle hinzufügen oder entfernen) oder sich selbst auf die Administratorrolle hochstufen.

Nachdem Sie Benutzern benutzerdefinierte Rollen zugewiesen haben, können Sie benutzerdefinierte Rollen der Seite **[!UICONTROL Benutzer]** hinzufügen oder daraus entfernen.

1. Suchen Sie auf der Seite **[!UICONTROL Benutzer]** nach einem Benutzer.

   ![](assets/search-user-role.png)
   _Benutzer auf der Benutzerseite suchen_

2. Wählen Sie den Dropdown-Pfeil am Ende der Zeile aus, in der der Benutzername angezeigt wird, und wählen Sie dann **[!UICONTROL Benutzerdefinierte Rollen verwalten]**.

   ![](assets/select-manage-custom-roles.png)
   _Auswählen von &quot;Benutzerdefinierte Rollen verwalten&quot; auf der Benutzerseite_

3. Ein Dialogfeld wird angezeigt, in dem die Liste der benutzerdefinierten Rollen angezeigt wird, die dem Benutzer zugewiesen sind. Wählen Sie **[!UICONTROL Rollen hinzufügen/entfernen]**, um dem Benutzer zugewiesene benutzerdefinierte Rollen hinzuzufügen oder zu entfernen.

   ![](assets/add-remove-roles.png)
   _Wählen Sie in der Eingabeaufforderung &quot;Benutzerdefinierte Rollen verwalten&quot; die Option &quot;Rollen hinzufügen/entfernen&quot; aus._

4. Suchen Sie nach anderen benutzerdefinierten Rollen, die dem Benutzer zugewiesen werden sollen. Wenn Sie eine Rolle gefunden haben, wählen Sie die benutzerdefinierte Rolle aus.

   ![](assets/add-new-custom-role.png)
   _Benutzerdefinierte Rolle auswählen_

5. Wählen Sie **[!UICONTROL Speichern]**. Ein Bestätigungsdialogfeld für die Änderung der benutzerdefinierten Rolle wird angezeigt. Wählen Sie **[!UICONTROL Ja]** aus.

   ![](assets/confirmation-prompt.png)
   _Wählen Sie in der Bestätigungsmeldung &quot;Ja&quot; aus._

Eine dritte benutzerdefinierte Rolle wird dem Benutzer zugewiesen.

Führen Sie die folgenden Schritte aus, um die benutzerdefinierten Rollen zu entfernen:

1. Suchen Sie auf der Seite **[!UICONTROL Benutzer]** nach einem Benutzer.
2. Wählen Sie das Dropdown-Menü neben dem Benutzer aus und wählen Sie **[!UICONTROL Benutzerdefinierte Rollen verwalten]**.
3. Wählen Sie **[!UICONTROL Rollen hinzufügen/entfernen]**, um benutzerdefinierte Rollen hinzuzufügen oder zu entfernen.
4. Wählen Sie das Symbol **[!UICONTROL Entfernen]** aus, um die benutzerdefinierte Rolle zu löschen.

   ![](assets/remove-custom-roles.png)
   _Benutzerdefinierte Rollen entfernen_

### Benutzerdefinierte Rollen wechseln

Verwenden Sie die Option **[!UICONTROL Benutzerdefinierte Rolle wechseln]**, um benutzerdefinierte Rollen anzuzeigen und auszuwählen, die Ihnen zugewiesen wurden.

![](assets/switch-roles.png)
_Benutzerdefinierte Rollen auswählen_

Benutzer erhalten E-Mail-Benachrichtigungen, wenn ihnen die benutzerdefinierten Rollen zugewiesen wurden. Die E-Mails enthalten jetzt Rollennamen, um eine bessere Übersichtlichkeit zu gewährleisten.

## Benutzerdefinierten Rollenbericht herunterladen

Administratoren können einen CSV-Bericht herunterladen, in dem alle benutzerdefinierten Rollen und die zugehörigen Berechtigungen aufgelistet sind. Der Bericht gibt an, ob jede Rolle manuell oder per CSV-Upload erstellt wurde, und enthält eine Zusammenfassung des Zugriffs und der Berechtigungen, die jeder Rolle zugewiesen wurden.

Führen Sie die folgenden Schritte aus, um den Bericht herunterzuladen:

1. Melden Sie sich als **[!UICONTROL Administrator]** an.
2. Wählen Sie **[!UICONTROL Benutzer]** > **[!UICONTROL Benutzerdefinierte Rollen]** aus.
3. Wählen Sie die Option **[!UICONTROL Download]**, um den CSV-Bericht herunterzuladen.

![](assets/download-report.png)
_Bericht über benutzerdefinierte Rollen herunterladen_

Der Bericht enthält zwei CSV-Dateien: role.csv und user_role.csv. Die Datei role.csv enthält:

* Benutzerdefinierte Rolle
* Benutzer-IDs
* Quelle der Erstellung.

Die Datei &quot;user_role.csv&quot; enthält die Felder, benutzerdefinierte Rolle, Quelle der Erstellung und detaillierte Informationen für Kataloge, Benutzer, Kurse, Lernpfade und mehr.

## Audit-Protokoll für benutzerdefinierte Rollen

Administratoren können den Audit-Bericht für benutzerdefinierte Rollen herunterladen, um alle Änderungen an den benutzerdefinierten Rollen zu verfolgen, einschließlich des Erstellens, Änderns und Löschens benutzerdefinierter Rollen sowie des zugehörigen Funktionszugriffs.

Weitere Informationen finden Sie in diesem Artikel [Prüfprotokoll für benutzerdefinierte Rollen](/help/migrated/administrators/feature-summary/reports.md#audit-trail-for-custom-roles).

## Ordnerzugriff für benutzerdefinierte Autoren einschränken {#folder-custom-author}

Learning Manager unterstützt bereits die Möglichkeit, mithilfe benutzerdefinierter Rollen Zugriff auf die Inhaltsbibliothek zu gewähren. Alle benutzerdefinierten Autoren, die bereits Zugriff auf die Inhaltsbibliothek haben, haben weiterhin Zugriff auf alle Inhaltsdateien, selbst wenn Inhaltsordner konfiguriert sind. So wird das alte Verhalten beibehalten. Administratoren müssen keine Änderungen vornehmen, wenn sie das aktuelle Verhalten fortsetzen möchten.

Wenn sie den Zugriff auf diese benutzerdefinierten Autoren einschränken möchten, müssen Administratoren die vorhandene benutzerdefinierte Rolle bearbeiten und konfigurieren, indem sie nur Zugriff auf bestimmte Inhaltsordner gewähren.

![](assets/folder-access-forcustomauthors.png)

*Ordnerzugriff für benutzerdefinierte Autoren einschränken*

Beim Erstellen eines benutzerdefinierten Autors können Sie dem Autor jetzt Inhaltsordner zuweisen. Wählen Sie die Option **Ausgewählte Ordner**.

Nachdem Sie auf die Option geklickt haben, wird ein neues Dialogfeld geöffnet, in dem Sie die Ordner dem benutzerdefinierten Autor zuweisen können.

![](assets/choose-folder.png)

*Ordner für den benutzerdefinierten Autor auswählen*

Wählen Sie die Ordner aus, und klicken Sie auf **[!UICONTROL OK]**.

## Dashboard für die Lernzusammenfassung für benutzerdefinierten Administrator {#custom-admin-dashboard}

Benutzerdefinierte Administratoren können dieselbe Ansicht wie Administratoren nutzen. Ein benutzerdefinierter Administrator kann Daten außerhalb seines Bereichs speichern. Dies gilt nur, wenn der Bereich des benutzerdefinierten Administrators nicht eingeschränkt ist. Um beim Erstellen eines benutzerdefinierten Administrators den vollen Umfang zu gewähren, aktivieren Sie im Kontoübersichtsbericht die Option **[!UICONTROL Vollständige Kontrolle]**.

![](assets/create-custom-role.png)

*Benutzerdefinierte Rolle erstellen*

Daher werden die Optionen &quot;**[!UICONTROL Alle Kataloge]**&quot; und &quot;**[!UICONTROL Alle Benutzergruppen]**&quot; ausgewählt und der Rest deaktiviert.

![](assets/scope-of-featureprivileges.png)

*Umfang der Berechtigungen definieren*

## Implizite Berechtigungen {#implicitpermissions}

Wenn einem Benutzer eine Rolle mit einer bestimmten Entität zugewiesen wird, kann es Fälle geben, in denen er Zugriff auf andere Entitäten benötigt, um Aufgaben für die gewährte Entität ausführen zu können. Wenn ein Benutzer beispielsweise Zugriff auf &quot;Erstellen&quot; für die Kurseinheit erhält, benötigt er Zugriff auf die Entitäten &quot;Kenntnisse&quot; und &quot;Tag&quot;, damit er sie mit dem erstellten Kurs verknüpfen kann. In dieser Tabelle finden Sie Informationen zu diesen impliziten Berechtigungen.

<table>
 <tbody>
  <tr>
   <th>Zugriffstyp</th>
   <th>Entitätsberechtigung, die von Admin erteilt wurde</th>
   <th>Implizite Entitätsberechtigung</th>
   <th>Implizierter Zugriff</th>
  </tr>
  <tr>
   <td>Verwalten</td>
   <td>Benutzer</td>
   <td>Gruppe</td>
   <td>Crud</td>
  </tr>
  <tr>
   <td>Registrieren</td>
   <td>Alle Lernobjekte (Kurs, Arbeitshilfe, Lernprogramm, Zertifizierung)</td>
   <td>Benutzer <br>
     Lernplan</td>
   <td>Lesen</td>
  </tr>
  <tr>
   <td>Erstellen</td>
   <td>
    <p>Inhaltsgruppe <br>
      Arbeitshilfe<br></p></td>
   <td>Tag</td>
   <td>Lesen</td>
  </tr>
  <tr>
   <td>Erstellen</td>
   <td>Kurs</td>
   <td>Inhaltsgruppe <br>
     Tag<br>
     Kenntnisse<br>
     Abzeichen<br>
     Arbeitshilfe</td>
   <td>Alles lesen</td>
  </tr>
  <tr>
   <td>Erstellen</td>
   <td>Lernprogramm <br>
     Zertifizierung<br></td>
   <td>Kurs<br>
     Tag<br>
     Kenntnisse<br>
     Ausweis</td>
   <td>Lesen</td>
  </tr>
  <tr>
   <td>Erstellen</td>
   <td>Lernplan</td>
   <td>Katalog <br>
     Gruppe<br>
     Kenntnisse<br>
     Alle Lernobjekte (Kurs, Arbeitshilfe, Lernprogramm, Zertifizierung)</td>
   <td>Lesen</td>
  </tr>
  <tr>
   <td>Erstellen</td>
   <td>Ankündigung</td>
   <td>Benutzer <br>
     Gruppe<br>
     Alle Lernobjekte (Kurs, Arbeitshilfe, Lernprogramm, Zertifizierung)</td>
   <td>Lesen</td>
  </tr>
  <tr>
   <td>Erstellen</td>
   <td>Gamification</td>
   <td>Branding</td>
   <td>Schreiben</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Benutzer</td>
   <td>Rechnungen</td>
   <td>Lesen</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Katalog</td>
   <td>Gruppe <br>
     Alle Lernobjekte (Kurs, Arbeitshilfe, Lernprogramm, Zertifizierung)</td>
   <td>Lesen</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Einstellung</td>
   <td>Branding <br>
     Benutzer</td>
   <td>Lesen</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Branding</td>
   <td>Einstellung</td>
   <td>Lesen</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Abrechnung<br>
     Gamification</td>
   <td>Benutzer</td>
   <td>Lesen</td>
  </tr>
 </tbody>
</table>

## Auf eine benutzerdefinierte Rolle zugreifen {#accessacustomrole}

Wenn ein Administrator eine benutzerdefinierte Rolle zuweist, erhalten Sie eine E-Mail-Benachrichtigung.

Hinweis: Wenn Sie bereits bei Learning Manager unter einer benutzerdefinierten Rolle angemeldet sind, müssen Sie sich erneut bei Learning Manager anmelden, um auf die neue Rolle zugreifen zu können.

Um zwischen den Rollen zu wechseln, klicken Sie auf Ihr Profilsymbol in der oberen rechten Ecke von Learning Manager und wählen Sie die Rolle aus.

## Lernpläne nach konfigurierbaren Rollen {#scopeconfigure}

In früheren Versionen von Learning Manager konnte jede benutzerdefinierte Rolle mit der Berechtigung zum Erstellen von Lernplänen den Lernplan für alle Arten von Benutzergruppen und Lernobjekten anzeigen.

Die Umfangseinstellung war früher deaktiviert, als der Zugriff auf den Lernplan gewährt wurde, wodurch der Benutzer standardmäßig auf alle Kataloge und alle Benutzergruppen zugreifen konnte.

Alle von einem Administrator erstellten Lernpläne gelten standardmäßig für alle Benutzer. Benutzern können auch beliebige Lernobjekte zugewiesen werden. Auf der anderen Seite haben Benutzer mit benutzerdefinierten Rollen Zugriff auf vollständige Bereiche, z. B. alle Kataloge, Lernobjekte oder Benutzergruppen. Dies bedeutete, dass Administratoren nicht wie erwartet benutzerdefinierte Rollen erstellen konnten, die Benutzern mit begrenztem Umfang den Zugriff auf Lernpläne ermöglichten.

In diesem Update von Learning Manager können Sie benutzerdefinierte Rollen für Lernpläne erstellen, um den Umfang für alle Benutzer und Lernobjekte festzulegen. Mit anderen Worten, Lernpläne können mit einem begrenzten Bereich erstellt werden, der vom Rollenbereich eines benutzerdefinierten Administrators abgeleitet wird.

Jetzt kann ein Administrator den Umfang definieren oder einschränken, während er Zugriff auf die Lernplanverwaltung gewährt.

Benutzerdefinierte Administratoren können Lernpläne mit einem begrenzten Umfang erstellen, der vom Umfang der konfigurierbaren Rolle des benutzerdefinierten Administrators abhängt. Solche Lernpläne sind nur für benutzerdefinierte Administratoren mit derselben Rolle zugänglich, außerdem für reguläre Administratoren. Darüber hinaus können die benutzerdefinierten Administratoren keine anderen Lernpläne im Konto sehen.

Bestehende benutzerdefinierte Administratoren, die Zugriff auf Lernpläne haben, haben (per Definition) immer den vollen Umfang. Sie haben wie normale Administratoren Zugriff auf alle Lernpläne im Konto. Neue benutzerdefinierte Rollen, die mit vollem Umfang erstellt wurden, und neue benutzerdefinierte Administratoren, die diesen Rollen hinzugefügt wurden, haben weiterhin Zugriff auf alle Lernpläne.

Lernpläne, die vom Administrator erstellt wurden, und benutzerdefinierte Administratoren mit vollem Umfang werden wie gewohnt erstellt und sind nicht durch den Umfang beschränkt.

Im Abschnitt **Umfang für Funktionsberechtigungen** gewähren Sie Zugriff auf Benutzergruppen und/oder den Katalog für die benutzerdefinierte Rolle.

![](assets/scope-for-featureprivileges.png)

*Zugriff auf Benutzergruppen und/oder den Katalog für die benutzerdefinierte Rolle gewähren*

Weisen Sie einen Benutzer der benutzerdefinierten Rolle zu.

![](assets/assign-users-to-customrole.png)

*Benutzer einer benutzerdefinierten Rolle zuweisen*

Der Benutzer meldet sich jetzt als benutzerdefinierter Administrator beim Learning Manager an und fügt einen Lernplan hinzu.

Wenn ein neuer Teilnehmer hinzugefügt wird, kann der benutzerdefinierte Administrator eine Schulung nur aus den Katalogen mit dem Umfang der konfigurierbaren Rolle auswählen.

Dieser Lernplan gilt jetzt nur für den Teilnehmer, wenn der Benutzer auch der Gruppe innerhalb der Benutzergruppe mit dem Umfang des Lernplans hinzugefügt wird. Alle anderen Teilnehmer werden von diesem Lernplan ausgenommen.

## Teilnehmer wird zu der Gruppe hinzugefügt {#learnergetsaddedtothegroup}

<!--![](assets/add-learner-to-thegroup.png)-->

Der benutzerdefinierte Administrator kann jede Benutzergruppe mit Benutzern aus der Benutzergruppe mit dem Umfang der Rolle auswählen.

Wenn ein Benutzer zur angegebenen Gruppe hinzugefügt wird, wird nur Benutzern das Lernobjekt zugewiesen, die bereits Teil der Benutzergruppe mit dem Umfang des Lernplans sind und der angegebenen Benutzergruppe hinzugefügt wurden.

## Änderung des Umfangs {#changeinscope}

Wenn der Administrator den Umfang der benutzerdefinierten Rolle ändert, wird die Änderung auch auf den benutzerdefinierten Administrator übertragen. Wenn der benutzerdefinierte Administrator einen Lernplan auswählt, der bereits im Umfang einer vorherigen benutzerdefinierten Rolle enthalten ist, wird eine Meldung angezeigt, wie unten gezeigt:

![](assets/change-scope.png)

*Meldung nach Bereichsänderungen*

Der benutzerdefinierte Administrator muss jetzt den früheren Bereich auf den neuen Bereich aktualisieren bzw. den neuen Bereich aktualisieren.

Durch Klicken auf **[!UICONTROL Umfang aktualisieren]** wird der Umfang aktualisiert. Es wird eine Warnmeldung angezeigt.

![](assets/refresh-scope-message.png)

*Warnmeldung nach dem Aktualisieren eines Bereichs*

Durch Klicken auf **[!UICONTROL Ja]** wird der Umfang aktualisiert.

## Gamification-Bericht zu einer benutzerdefinierten Rolle hinzufügen {#gamification-custom}

Ein Administrator kann Gamification-Berichte für einen benutzerdefinierten Benutzer aktivieren.

1. Geben Sie auf der Seite **[!UICONTROL Benutzerdefinierte Rollen]** den Namen der benutzerdefinierten Rolle ein.
1. Aktivieren Sie im Abschnitt **[!UICONTROL Funktionsberechtigungen: Kernfunktionen]** die Option **[!UICONTROL Vollständige Kontrolle]** für die Kategorie **[!UICONTROL Berichte]**.

1. Wählen Sie im Abschnitt **[!UICONTROL Benutzer]** den Benutzer aus, dem die neu erstellte benutzerdefinierte Rolle zugewiesen werden soll.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

Wenn sich ein Benutzer als benutzerdefinierter Administrator anmeldet und im linken Bereich auf **[!UICONTROL Berichte]** klickt, werden die Transkripte wie folgt angezeigt:

![](assets/download-gamificationtranscripts.png)

*Gamification-Transkripte herunterladen*

Klicken Sie auf **[!UICONTROL Gamification-Transkripte]**, wählen Sie einen Benutzer aus und erstellen Sie den Bericht.

Wenn ein Administrator die Stufenpunkte ändert, werden in den Berichten die Stufen entsprechend den aktuellen Punkten angezeigt.

Durch das Zurücksetzen von Gamification wird die erreichte Stufe nicht zurückgesetzt.

## Häufig gestellte Fragen {#frequentlyaskedquestions}

+++Wie erstelle ich eine benutzerdefinierte Rolle?

Eine benutzerdefinierte Rolle ist wie eine Untergruppe einer Autor- oder Administratorrolle. Erteilen Sie eine oder mehrere Berechtigungen, definieren Sie den Umfang und weisen Sie die Rolle einem Benutzer zu.

Klicken Sie auf **[!UICONTROL Benutzer]** > **[!UICONTROL Benutzerdefinierte Rollen]**. Klicken Sie auf der Seite „Benutzerdefinierte Rollen“ auf **[!UICONTROL Rolle erstellen]**. Geben Sie den Namen der benutzerdefinierten Rolle ein und legen Sie die Berechtigungen für die Rolle fest. Weitere Informationen finden Sie unter [Benutzerdefinierte Rolle erstellen](custom-role.md#create-role).
+++


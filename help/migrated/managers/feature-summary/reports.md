---
description: Erstellen und Verwalten von Berichten für Manager.
jcr-language: en_us
title: Berichte
contentowner: manochan
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '1840'
ht-degree: 0%

---



# Berichte

Erstellen und Verwalten von Berichten für Manager.

Mit dem Adobe-Lernmanager können Sie verschiedene Berichte erstellen, um die Aktivitäten der Teilnehmer zu verfolgen, zu überwachen und zu steuern. Aktivitäten von Teilnehmern werden verfolgt und automatisch in der Datenbank erfasst. Manager- und Administratorberichte werden aus der Datenbank generiert.

## Übersicht {#overview}

Berichte für Administrator und Manager werden auf die gleiche Weise erstellt. Manager können Berichte über ihre Mitarbeiter anzeigen, Administratoren hingegen alle Berichte im Unternehmen.

Berichte werden in einem Dashboard generiert. Ein Bericht muss sich in einem Dashboard befinden. A **Standard-Dashboard** ist standardmäßig auf der Berichtsseite vorhanden. Alle Berichte, die Sie hinzufügen, werden in dieses Standard-Dashboard verschoben. Um einem einzelnen Dashboard einen Bericht hinzuzufügen, wählen Sie in der Dropdownliste &quot;Bericht hinzufügen&quot;. Weitere Informationen zum Erstellen von Dashboards finden Sie im Abschnitt Dashboards auf dieser Seite.

## Manager-Dashboards {#manager-dashboards}

Ein Manager kann Informationen über sein direktes oder indirektes Team als Zusammenfassung anzeigen.

Der Manager kann dann den Bericht nach Bereichen wie Quartal, aktueller Monat, letzte drei Monate und letzte 12 Monate filtern.

## Übersicht zu Lernprogrammen {#learningsummary}

![](assets/manager-learningsummary.png)

*Lernzusammenfassung anzeigen*

![](assets/manager-dashboard.jpg)

*Lernzusammenfassung nach Datum filtern*

## Kompatibilitäts-Dashboard {#compliancedashboard}

Prüfen Sie die Compliance Ihres Teams und bei welchen Teammitgliedern die Compliance gefährdet ist. Wählen Sie die Lernobjekte aus und zeigen Sie den Status jedes Objekts an.

![](assets/compliance-dashboard.png)

*Kompatibilitäts-Dashboard anzeigen*

## Qualifikationsstatus {#skillsstatus}

Zeigen Sie für jede Qualifikation den Prozentsatz der Teilnehmer an. Wählen Sie höchstens fünf Kenntnisse aus, für die Sie die Kenntnisse für Teilnehmer anzeigen möchten. Die Visualisierung erfolgt in Form eines gestapelten Balkendiagramms. Wenn Sie den Mauszeiger über die einzelnen Balken bewegen, können Sie die Statusaufschlüsselung dieser Qualifikationen anzeigen.

![](assets/manager-skills-status.png)

*Status der Kenntnisse eines Teilnehmers anzeigen*

## Kenntnis-Tracker {#skilstracker}

Zeigen Sie eine Qualifikationsabschlussprojektion für ein Team an. Wählen Sie den Zielabschlussprozentsatz und das Datum einer Qualifikation.

Basierend auf Verlaufsdaten können Sie eine grafische Darstellung der Qualifikationsabschlussprojektion am ausgewählten Datum anzeigen.

![](assets/historical-data.png)

*Qualifikationsabschlussprojektion anzeigen*

## Erstellen von Berichten {#creatingreports}

1. Klicken Sie auf Berichte im linken Bereich. Die Seite mit der Berichtzusammenfassung wird angezeigt.\
   **Hinweis**
Standardmäßig werden mindestens drei Beispielberichte auf der Seite mit der Berichtszusammenfassung angezeigt. Sie können diese Beispielberichte nur anzeigen, um eine Vorstellung davon zu bekommen, wie Sie sie erstellen und anpassen können.

1. Klicken Sie auf der Berichtszusammenfassungsseite auf &quot;Hinzufügen&quot;. Das Dialogfeld zur Berichterstellung wird angezeigt.
1. Klicken Sie auf Speichern , um das Erstellen des Berichts abzuschließen. Ein Beispielbericht wird unten als Referenz gezeigt.

![](assets/add-report.png)

*Dialogfeld &quot;Bericht hinzufügen&quot;*

Unter Berichtstyp können Sie einen Satz vordefinierter Berichte oder benutzerdefinierte Berichte auswählen. Sie können die folgenden Berichte als Teil der vordefinierten Berichte anzeigen:

* Zugewiesene und erreichte Kenntnisse
* Kursregistrierungen und -abschlüsse
* Effektivität von Kursen
* Lernprogramme registriert und abgeschlossen
* Aufgewandte Lernzeit pro Kurs
* Aufgewandte Lernzeit pro Quartal

Mit den oben genannten Berichtstypen können Sie mehr als 300 unterschiedliche Berichtsvarianten generieren.

Berichtname Geben Sie einen Titel für Ihren Bericht ein.

**Primäre Y-Achse** Wählen Sie das erste/primäre Kriterium für Ihren Bericht aus den Dropdown-Optionen aus. Für einige der ausgewählten Kriterien haben Sie die Möglichkeit, einen oder mehrere Status aus dem angrenzenden Status-Dropdownfeld auszuwählen. Beim primären Kriterium der Statistik zur Kursregistrierung können die Status beispielsweise &quot;Abgeschlossen&quot;, &quot;Nicht abgeschlossen&quot;, &quot;Registriert&quot; usw. lauten. Daten des primären Bereichs werden im Bericht in Form von Balkendiagrammen dargestellt.

**Sekundäre Y-Achse** Wählen Sie aus den Dropdown-Optionen die Kriterien für die sekundäre Y-Achse bzw. den Bereich für Ihren Bericht aus. Wählen Sie beispielsweise bei der Option für die Registrierung für ein Lernprogramm einen oder mehrere Status aus dem Dropdown-Menü neben Status aus. Sekundäre Bereichsdaten werden in Form von Liniendiagrammen dargestellt.

**X-Achse** Wählen Sie die für Ihren Bericht geeigneten X-Achsen-Kriterien aus den Dropdown-Optionen aus. Wenn Sie das Datum als Kriterium für die x-Achse ausgewählt haben, steht eine Option zur Gruppierung des x-Achsen-Kriteriums nach Tag, Monat, Quartal und Jahr zur Verfügung.

**Datum** Wählen Sie die entsprechende Option aus dem Dropdown-Menü aus. Optionen: letzter Monat, Quartal, Jahr, QTD (letzte 90 Tage), YTD (letzte 365 Tage) und Datumsbereich. Wenn Sie einen Datumsbereich auswählen, geben Sie das Von- und Bis-Datum wie folgt an:

**Von** Wählen Sie das Startdatum, ab dem der Bericht angezeigt werden soll.

**Funktion** Wählen Sie das Enddatum Ihres Berichts aus.

## Filter {#filters}

Filter werden im Dialogfeld &quot;Bericht hinzufügen&quot; am unteren Rand basierend auf Berichtstypen angezeigt, die Sie ausgewählt haben. Einige der wichtigsten Filter sind unten aufgeführt.

**Manager** Sie können jeden der Manager basierend auf der Hierarchieebene auswählen. Bei einigen Managern können untergeordnete Manager vorhanden sein, denen wiederum mehrere Mitarbeiter unterstellt sind.

**Profil** Wählen Sie die Bezeichnung Ihres Mitarbeiters aus. Dies würde helfen, Berichte von Mitarbeitern basierend auf ihrem Profil/ihrer Einstufung anzuzeigen. Beispiel: Informatiker, Ingenieur usw.

**Benutzergruppe** Wählen Sie die Benutzergruppe aus, je nachdem, wie Sie die Berichte filtern möchten. Learning Manager ruft die Benutzergruppen auf, die für Ihr Konto definiert wurden, aus der Benutzerfunktion aus.

**Kurs** Sie können Ihren Bericht nach Kursen filtern, indem Sie diese in der Dropdownliste auswählen.

![](assets/sample-report-admin.png)

*Diagramm der Kurse anzeigen, für die Kurse registriert und abgeschlossen wurden*

>[!NOTE]
>
>Über der Legende für das Diagramm können Sie ein Zoomfeld anzeigen. Sie können den Cursor darüber bewegen, darauf klicken und das Kreuzsymbol über jeden Teil des Zoomfelds ziehen, den Sie vergrößern möchten.

Sie können die Werte der sekundären y-Achse in Form einer Linie in den Diagrammbalken anzeigen. Im obigen Beispiel können Sie beispielsweise die Werte für die Effektivität in einer grauen Linie im Graphen sehen.

## Benutzergruppenberichte {#user-group-reporting}

Verfolgen Sie nach, wie Benutzergruppen wie Abteilungen, externe Partner und Rollen im Vergleich zu anderen Benutzergruppen oder im Vergleich zu anderen Lernobjektiven funktionieren.

### Benutzergruppen {#usergroups}

Um Berichte basierend auf Benutzergruppen zu generieren, wählen Sie **Benutzergruppe** in der X-Achse aus der Liste der Dropdown-Optionen (siehe Screenshot unten).

![](assets/x-axis-reporting.png)

*Generieren von Benutzergruppenberichten*

Andere **Auswählen** neben der X-Achse mit einer Liste von Benutzergruppen angezeigt, die für Ihr Konto verfügbar sind. In diesem Dropdownmenü können Sie eine oder mehrere Benutzergruppen auswählen.

Wenn Sie mehrere Benutzergruppen ausgewählt haben, wird nach dem Speichern und Generieren dieses Berichts der Bericht mit allen Benutzergruppen generiert, die im Balkendiagramm neben jeder x-Achse dargestellt werden.

Dieser Benutzergruppebericht ermöglicht es Ihnen, die Leistung einer Abteilung/Division/Rolle mit der anderer zu vergleichen, um ihre Lernleistungen zu bewerten.

### Benutzerdefinierte Benutzergruppen/Benutzerattribute {#customusergroupsuserattributes}

Sie können benutzerdefinierte Benutzergruppen auch mit der Funktion Benutzer/Benutzergruppen hinzufügen im Lern-Manager erstellen. Nachdem Sie die Benutzergruppen erstellt haben, können Sie Berichte für diese benutzerdefinierten Benutzergruppen mithilfe einer Liste von Attributen wie Speicherort, Verzweigung usw. generieren.

Wählen Sie in der X-Achse die Benutzerattributoption und wählen Sie das Attribut aus **aussuchen** daneben. Um einen benutzerdefinierten Benutzergruppebericht basierend auf diesen Attributen zu erstellen, müssen Sie auch die entsprechende Benutzergruppe im Filter auswählen.

Manager können Benutzergruppenberichte nur für ihre eigenen Teammitglieder als Teilnehmer erstellen.

## Berichtstypen {#typesofreports}

* Statistiken zur Kursbereitstellung für Teilnehmer
* Bericht zur Effektivität von Kursen
* Kenntnisbasierter Bericht über Teilnehmer
* Statistik zur Registrierung der Lernprogramme für Teilnehmer
* Von den Teilnehmern aufgewandte Lernzeit
* Abschluss der Zertifizierung

## Meine Berichte {#myreports}

Ein Dashboard ist eine Sammlung von Berichten. Berichte können nach Ihren Wünschen in einem Dashboard gruppiert werden.

**Beispielberichte**

Klicken Sie auf diese Registerkarte, um einige Musterberichte anzuzeigen, die anhand von Beispieldaten erstellt wurden. Sehen Sie sich diese Berichte an, um zu verstehen, welche funktionsreichen Berichtsvarianten Sie mit Ihren Kontodaten generieren können.

**Meine Berichte**

Klicken Sie auf diese Dashboard-Registerkarte, um alle von Ihnen erstellten Dashboards anzuzeigen. In der Dropdown-Liste &quot;Dashboard anzeigen&quot; können Sie das Standard-Dashboard oder eines Ihrer erstellten Dashboards auswählen.

**Dashboard hinzufügen**

1. Klicken Sie rechts auf der Seite auf &quot;Dashboard hinzufügen&quot;, um eigene Dashboards zu erstellen.

   ![](assets/add-dashboard.png)

   *Eigenes Board erstellen*

1. Geben Sie den Namen und die Beschreibung des Dashboards ein und klicken Sie auf **[!UICONTROL Speichern]**.

Sie können das kürzlich erstellte Dashboard in der Liste Meine Dashboards anzeigen.

Um Ihrem Dashboard Berichte hinzuzufügen, klicken Sie in der rechten oberen Ecke Ihres Dashboard-Fensters auf die Dropdownliste und auf Bericht hinzufügen. Der so erstellte Bericht wird mit Ihrem Dashboard verknüpft.

>[!NOTE]
>
>Berichte, die Sie erstellen, indem Sie in der rechten oberen Ecke der Seite &quot;Berichte&quot; auf &quot;Hinzufügen&quot; klicken, werden Ihrem Standard-Dashboard hinzugefügt.

**Freigegebene Berichte**

Freigegebene Berichte sind eine Sammlung von Berichten, die andere Benutzer in Ihrer Organisation für Sie freigegeben haben. Wenn Sie über die Berechtigungen verfügen, können Sie die freigegebenen Berichte herunterladen oder duplizieren. Wenden Sie sich an den Administrator Ihres Unternehmens, um Download-/Duplikatzugriffsrechte für die freigegebenen Berichte zu erhalten.

**Abonnierte Berichte**

Sie können Ihre bevorzugten Berichte abonnieren, indem Sie hier Ihre E-Mail-ID angeben. Ihre abonnierten Berichte werden Ihnen per E-Mail gesendet.

Klicken Sie auf **Bearbeiten** in der rechten Ecke Ihres Berichtnamens in der Berichtliste, um Ihr Abonnement jederzeit zu ändern.

## Anzeigen von Berichten {#viewingreports}

Auf der Seite &quot;Berichtzusammenfassung&quot; können Sie alle Berichte anzeigen. Sie können jeden Bericht minimieren, indem Sie auf das Minussymbol (-) in der rechten oberen Ecke jedes Berichts klicken. Klicken Sie auf das Pluszeichen (+), um Ihren Bericht erneut anzuzeigen.

**Schnellansicht mit verschiedenen Datumswerten**

Die Datumswerte, die Sie zum Anzeigen des Berichts verwenden, sind temporär. Wenn Sie die Option &quot;Herunterladen&quot; wählen, wird diese Berichtsansicht nicht heruntergeladen. Dies ist nur eine temporäre Ansicht.

Sie können den Datumsbereich/-wert für jeden Bericht ändern und diesen schnell für ein anderes Datum anzeigen, ohne den Bericht zu ändern und zu speichern. Klicken Sie auf das Bearbeitungssymbol (wie in der Abbildung unten mit einem Pfeil gezeigt) neben dem Datumsbereich, z. B. QTD, letztes Jahr usw. Wählen Sie den neuen Wert aus dem Dropdown-Menü aus und klicken Sie auf das Häkchen, um die Änderung zu bestätigen. Sie können die Änderung abbrechen, indem Sie auf &quot;X&quot; klicken.

**Schnellansicht mit verschiedenen Managern**

Wenn Ihnen mehrere Manager unterstellt sind, können Sie die Berichte für jeden Manager schnell anzeigen. Wählen Sie den Managernamen aus der Dropdown-Liste aus, um einen eindeutigen Bericht für jeden Manager anzuzeigen.
**Berichte bearbeiten/in Dashboard verschieben/Kopie erstellen/löschen/Größe ändern** Klicken Sie auf den Dropdownpfeil in der oberen rechten Ecke jedes Berichts, um die Dropdownoptionen als &quot;Bearbeiten&quot;, &quot;Verschieben ins Dashboard&quot;, &quot;Kopie erstellen&quot;, &quot;Löschen&quot; oder &quot;Größe ändern&quot; anzuzeigen.

<!--![](assets/edit-options-dashboard-300x126.png)-->

**Bearbeiten** Klicken Sie beim Ändern von Daten auf &quot;Zurücksetzen&quot;, um zu den Anfangswerten zurückzukehren. Klicken Sie nach dem Ändern der Werte auf &quot;Speichern&quot;.

**Zum Dashboard verschieben** Sie können den aktuellen Bericht in ein anderes Dashboard verschieben, das Sie aus der Liste der Dashboards auswählen.

**Kopie erstellen** Sie können den Bericht in dasselbe oder ein anderes Dashboard kopieren, das Sie aus der Liste der Dashboards auswählen.

**Löschen** Klicken Sie auf Löschen , um den Bericht zu entfernen. Bevor Sie den Bericht löschen können, wird eine Warn- bzw. Bestätigungsmeldung angezeigt.

**Größe ändern** Sie können die Größe Ihrer Berichte ändern in 1×1 (mittel) und 2×2 (groß).

## E-Mail-Abonnements {#emailsubscriptions}

Sie erhalten Ihre Lieblingsberichte per E-Mail, indem Sie sie abonnieren.

Klicken Sie auf der Seite Berichte neben der Schaltfläche Hinzufügen in der oberen rechten Ecke der Seite auf E-Mail-Abonnement. Die Seite zum Abonnieren von Berichten wird angezeigt.

Beginnen Sie mit der Eingabe des Berichtnamens in das Feld Berichte, um den Berichtnamen aus der Dropdownliste auszuwählen. Wählen Sie die E-Mail-Häufigkeit aus, die Sie täglich, wöchentlich oder monatlich benötigen, fügen Sie den Betreff der E-Mail hinzu und klicken Sie auf &quot;Hinzufügen&quot;, um das Abonnement abzuschließen.

Klicken Sie auf Bearbeiten , um das Abonnement zu ändern. Klicken Sie auf Entfernen , um das Abonnement zu löschen.

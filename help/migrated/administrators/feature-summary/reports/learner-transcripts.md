---
description: Mit den Teilnehmertranskripten in Adobe Learning Manager (ALM) können Administratoren den Fortschritt der Teilnehmer in Kursen, Modulen, Lernpfaden und Zertifizierungen überwachen. Es unterstützt Leistungsbewertungen, Compliance-Überwachung, Audits und externe Berichte. Der Bericht bietet eine vollständige Zusammenfassung des Engagements und der Leistung eines Teilnehmers.
jcr-language: en_us
title: Teilnehmertranskripte in Adobe Learning Manager
source-git-commit: a01ec6117ad49a1f9af0b31d48ad19ddc8443dde
workflow-type: tm+mt
source-wordcount: '4221'
ht-degree: 8%

---


# Teilnehmertranskripte in Adobe Learning Manager

## Überblick

Mit den Teilnehmertranskripten in Adobe Learning Manager (ALM) können Administratoren den Fortschritt der Teilnehmer auf granularer Ebene über Kurse, Module, Lernpfade und Zertifizierungen hinweg verfolgen. Die Transkriptdaten unterstützen Performance-Überprüfungen, Compliance-Verfolgung, Audits und externe Berichtsanforderungen.

>[!NOTE]
>
>Teilnehmertranskripte können von Administratoren, benutzerdefinierten Administratoren, Managern oder Teilnehmern heruntergeladen werden.

Bei Teilnehmern müssen sie ihre Profileinstellungen starten und dann ihre Lerntranskripte als Excel-Datei herunterladen. Dieses Transkript, das für einen einzelnen Teilnehmer erstellt wurde, beschreibt seinen persönlichen Lernweg. Es enthält die Namen von Lernpfaden, Kursen, Instanzen und Modulen zusammen mit wichtigen Daten wie Registrierung, Abschluss und Fristen. Der Status wird auch nach Status, Noten, Quizpunktzahlen (einschließlich Höchstpunktzahlen und Höchstwerten) und Versuchen verfolgt. Darüber hinaus werden Schulungs-IDs, Dauern, Abmeldedaten, Preise und alle Einreichungskommentare angezeigt. Dieser Bericht bietet einen umfassenden Überblick über das Engagement und die Leistung eines einzelnen Teilnehmers.

Unternehmen können die Teilnehmertranskripte verwenden, um die Lernverhaltensdaten zu einem Enterprise Data Warehouse hinzuzufügen, in dem man möglicherweise Lerndaten mit anderen Unternehmensdaten kombinieren möchte, um die Zusammenhänge zwischen Lernverhalten und anderen Prozessdaten zu analysieren.

## Zweck und Vorteile

* Erstellt Audit-fähige Datensätze für regulatorische Anforderungen mit Zeitstempeln und Abschlussnachweisen.
* Verknüpft Lernaktivitäten mit Mitarbeiterentwicklung und Kompetenzerwerb.
* Verfolgt den Zertifizierungsstatus für Rollen, die eine obligatorische Schulung erfordern.
* Unterstützt die quantitative Messung der Effektivität von Lernprogrammen.

## Anwendungsfälle von Teilnehmertranskripten

In den Teilnehmertranskripten in Adobe Learning Manager werden Schulungen, Compliance und die Entwicklung von Fähigkeiten nachverfolgt, sodass Abteilungen den Abschluss überprüfen und die Programmeffektivität im gesamten Unternehmen bewerten können.  Im Folgenden finden Sie einige Anwendungsfälle, die im Teilnehmertranskript behandelt werden:

* Ein Finanzdienstleister muss nachweisen, dass alle kundenorientierten Mitarbeiter die obligatorische Compliance-Schulung vor Ablauf der vorgeschriebenen Frist absolviert haben.
* Die IT-Abteilung muss die aktuellen Java-Programmiermöglichkeiten anhand der zukünftigen Projektanforderungen bewerten.
* Die Personalabteilung möchte die Effektivität des neuen Mitarbeiter-Onboarding-Programms für verschiedene Abteilungen bewerten.
* Das Betriebsteam muss sicherstellen, dass alle Außendiensttechniker die erforderlichen Sicherheitszertifizierungen einhalten.

## Zugriffskontrolle und Berechtigungen

**Administratoren**

* Kann Transkripte für alle Teilnehmer in allen Katalogen generieren.
* Zugriff auf alle Berichtsfunktionen möglich, kann jedoch Beschränkungen für Kataloge oder Benutzergruppen aufweisen.
* Benutzerdefinierte Administratoren: Zugriff durch zugewiesenen Umfang und Berechtigungen beschränkt.

**Bereichsbasierte Einschränkungen**

* Benutzerdefinierte Administratoren können Transkripte für Teilnehmer nur innerhalb ihrer zugewiesenen Benutzergruppen anzeigen.
* Berichte enthalten nur Lernobjekte aus Katalogen, für deren Zugriff der Administrator berechtigt ist.

## Erstellen von Teilnehmertranskripten

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.
2. Wählen Sie im linken Navigationsmenü **[!UICONTROL Berichte]** aus.
3. Wählen Sie **[!UICONTROL Benutzerdefinierte Berichte]** in den Berichten aus, und wählen Sie dann **[!UICONTROL Excel-Berichte]** aus.
4. Wählen Sie **[!UICONTROL Teilnehmertranskripte]** aus.

   ![]()

5. Wählen Sie **[!UICONTROL Neu generieren]**.
6. Wählen Sie den Datumsbereich aus, für den das Transkript generiert werden soll. Standardmäßig ist das **[!UICONTROL Von]**-Datum das Registrierungsdatum des Teilnehmers, und das **[!UICONTROL Bis]**-Datum ist immer das aktuelle Datum. Sie können nur das Startdatum ändern, ab dem Sie die Daten benötigen.
7. Wählen Sie Folgendes aus:
a. Wählen Sie die Namen der Teilnehmer im Abschnitt **[!UICONTROL Teilnehmer auswählen]** aus. Sie können Benutzer oder Benutzergruppen auswählen oder die E-Mail-Adressen der Teilnehmer, für die Sie Transkripte generieren möchten, kopieren und einfügen. Weitere Informationen finden Sie im Abschnitt [Teilnehmertranskript ](#generate-learner-transcript-using-copy-paste) mithilfe der Funktion zum Kopieren und Einfügen generieren.
b. Wählen Sie bestimmte Kataloge aus der Dropdown-Liste **[!UICONTROL Kataloge auswählen]** aus. Das Transkript wird nur für die angegebenen Kataloge heruntergeladen.\
   c. Wählen Sie den **[!UICONTROL Registrierungsstatus]** aus. Dieses Dropdown-Menü enthält die folgenden Optionen:

       * Alle auswählen
       * Abgeschlossen
       * wird ausgeführt
       * nicht gestartet
       * Registrierung aufgehoben
   8. Erweiterte Optionen: Wählen Sie **[!UICONTROL Erweiterte Optionen]**, um die Transkripte herunterzuladen und Folgendes einzuschließen:

   a. Laden Sie Transkripte für Teilnehmer herunter, die aus einem Konto gelöscht wurden, indem Sie das Kontrollkästchen **[!UICONTROL Gelöschte Teilnehmer einschließen]** aktivieren.
b. Laden Sie Modulebeneninformationen im Teilnehmertranskript herunter, indem Sie das Kontrollkästchen **[!UICONTROL Modulebeneninformationen aktivieren]** aktivieren. In diesem Fall werden Modulnamen und die für jedes Modul aufgewendete Zeit als Teil des Transkripts abgerufen, wenn diese Option aktiviert ist.
c. Laden Sie Fertigkeitsdaten und Zusammenfassungsblätter herunter, indem Sie das Kontrollkästchen **[!UICONTROL Fertigkeitsdaten und Zusammenfassungsblätter einschließen]** aktivieren. Weitere Informationen finden Sie im Abschnitt Excel-Berichte.
9. Sie können auch die Spaltenwerte auswählen, die in Ihrem Bericht aufgefüllt werden sollen. Dies bietet Flexibilität beim Herunterladen von Berichten mit bestimmten Spaltenwerten. Wählen Sie die Spalten im Dropdown-Menü aus.

   

Transkripte werden generiert und als ZIP-Dateien auf Ihren Computer heruntergeladen, wenn die Kenntnisdaten nicht enthalten sind. Wenn das Kontrollkästchen &quot;Kenntnisdaten&quot; aktiviert ist, werden Transkripte generiert und als heruntergeladen. XLSX-Dateien.

### Teilnehmertranskript durch Kopieren und Einfügen erstellen

Das Abrufen von Teilnehmertranskripten ist ein langwieriger Vorgang, da er nur einzeln für einen Teilnehmer bzw. eine Benutzergruppe durchgeführt werden kann. Mit der Funktion zum Kopieren und Einfügen können Sie die gesamte Liste der Teilnehmer-E-Mail-IDs gleichzeitig kopieren und einfügen.

1. Wählen Sie die Registerkarte **[!UICONTROL E-Mail-IDs]** aus, um die kopierte Liste der eindeutigen E-Mail-IDs einzugeben.

   

2. Fügen Sie eindeutige E-Mail-IDs der Teilnehmer ein, die Sie hinzufügen möchten, getrennt durch Kommas, Semikolons oder Zeilenumbrüche.
3. Wählen Sie **[!UICONTROL E-Mail-IDs validieren]**, um zu überprüfen, ob die eingegebene E-Mail-ID gültig ist. Wenn die eingegebene E-Mail-ID falsch ist, wird sie zusammen mit einer Validierungsnachricht rot markiert.

   >[!NOTE]
   >
   >Die Schaltfläche Generieren bleibt deaktiviert, es sei denn, alle eingegebenen E-Mail-IDs sind korrekt.

4. Wählen Sie **[!UICONTROL Generieren]** aus, um Teilnehmertranskripte für alle genannten E-Mail-IDs zu generieren.

   >[!NOTE]
   >
   >Das Generieren von Teilnehmertranskripten kann für E-Mail-IDs kombiniert werden, die sowohl auf der Registerkarte Benutzer als auch E-Mail-IDs eingegeben wurden.

### Was enthält der Teilnehmertranskriptbericht?

Der Teilnehmertranskriptbericht ist eine Kombination aus Benutzer-, Registrierungs- und Lernobjektinformationen.
Die folgenden Tabellen beschreiben jeden Typ:

**Benutzerbezogene Informationen**

Die folgenden Spalten geben den Teilnehmer an.

| Feld | Beschreibung |
|---|---|
| Name | Name des Teilnehmers. |
| E-Mail | E-Mail-Adresse des Teilnehmers. |
| Adobe ID | Dieses Feld wird nur ausgefüllt, wenn sich Benutzer mit ihrer Adobe ID anmelden. Wenn sie über ein unternehmensdefiniertes [Single Sign-On (SSO)](/help/migrated/administrators/feature-summary/multiple-sso-logins.md) auf Adobe Learning Manager zugreifen, bleibt das Adobe ID-Feld leer. |
| Eindeutige ID des Benutzers | Eindeutige ID des Benutzers ist eine externe ID, die von Konten generiert wird, wenn sie nicht über E-Mail-IDs aller Benutzer oder eindeutige E-Mail-IDs aller Benutzer verfügen. <br>Das Feld &quot;Eindeutige ID des Benutzers&quot; ist ein optionales Feld, das für ein Konto aktiviert werden kann. Der Hauptzweck des Felds besteht darin, es Konten zu ermöglichen, jeden Benutzer mit einer eindeutigen ID zu markieren, um ihn zu verfolgen, Benutzerdatensätze über APIs zu aktualisieren, Audits durchzuführen oder Daten in automatisierten Workflows zu synchronisieren. Das Tagging der einzelnen Benutzer erfolgt über den CSV-Import der Benutzer.</br><br>Wenn sich ein Konto für die eindeutige Benutzer-ID entschieden hat, werden Berichte, wie z. B. Teilnehmertranskripte, von Adobe Learning Manager in den Berichten bereitgestellt.</br> |

**Registrierungsbezogene Informationen**

In den folgenden Spalten werden Aktivität, Fortschritt und Versuche erfasst.

| Feld | Beschreibung |
|---|---|
| Registrierungsdatum (UTC-Zeitzone) | Datum und Zeitstempel der Registrierung des Teilnehmers für den Lernobjekttyp, d. h. den Kurs, die Zertifizierung oder den Lernpfad. |
| Abgeschlossen-Datum markieren (UTC-Zeitzone) | Datum und Zeitstempel, wann ein Kursleiter eine Sitzung oder ein Modul als abgeschlossen markiert. Wenn keine Sitzung stattgefunden hat, wird die Spalte im Bericht leer angezeigt. Wenn eine Sitzung stattgefunden hat und der Kursleiter die Sitzung nicht als abgeschlossen markiert hat, wird die Spalte im Bericht leer angezeigt. |
| Startdatum (UTC-Zeitzone) | Datum und Uhrzeit, als der Teilnehmer das Lernobjekt gestartet hat. Wenn diese Spalte leer ist, hat der Teilnehmer diesen Vorgang noch nicht gestartet. |
| Abschlussdatum (UTC-Zeitzone) | Datum und Uhrzeit, zu der der Teilnehmer diesen Vorgang abgeschlossen hat. Wenn diese Spalte leer ist, hat der Teilnehmer diesen Vorgang noch nicht abgeschlossen. |
| Termin (UTC-Zeitzone) | Datum und Uhrzeit, zu der der Teilnehmer dieses Lernobjekt abschließen soll. Wenn diese Spalte leer ist, wurde keine Frist festgelegt. |
| Überfällig | Aktueller überfälliger Status des Teilnehmers, der für das Lernobjekt registriert ist. Ja//Nein |
| Status | Gibt den Status des Teilnehmers an, wenn er den Kurs, die Zertifizierung oder den Lernpfad absolviert.  Die verfügbaren Status sind &quot;Nicht gestartet&quot;, &quot;Nicht registriert&quot;, &quot;In Bearbeitung&quot; oder &quot;Abgeschlossen&quot;. |
| Fortschritt % | Aktueller Fortschritt % des Teilnehmers, der den Kurs, die Zertifizierung oder den Lernpfad absolviert. |
| Verbrachte Zeit (Minuten) | Die vom Teilnehmer im LO aufgewendete Lernzeit, die Zeilen auf Modulebene zeigen die einzelne modulweise aufgewendete Lernzeit an. Die Zeilen für den Kurs/den Lernpfad/die Zertifikatsebene zeigen die aggregierte aufgewendete Lernzeit an. |
| Bewertung | Gibt den Erfolg des Teilnehmers an. „Bestanden“, wenn der Benutzer die Erfolgskriterien erfüllt hat, ansonsten „Nicht bestanden“. |
| Quizpunktzahl | Die neueste Quizpunktzahl, die der Teilnehmer erhalten hat. Kann leer sein, wenn der Teilnehmer kein Quiz versucht hat oder der Inhalt kein Quiz enthält oder der Administrator/Kursleiter keine Punktzahl zugewiesen hat. |
| Quiz_score_max | Die neueste maximal mögliche Quizpunktzahl für das Modul. Es kann leer sein, wenn der Teilnehmer kein Quiz absolviert hat oder der Inhalt keine Quizze enthält. |
| Highest_Quiz_score | Die höchste Quizpunktzahl, die der Teilnehmer bei mehreren Versuchen erzielt hat. Kann leer sein, wenn der Teilnehmer nicht versucht hat, das Quiz durchzuführen, oder wenn der Inhalt kein Quiz enthält oder der Administrator oder Kursleiter keine Punktzahl zugewiesen hat. |
| Highest_Quiz_score_max | Die höchstmögliche Quizpunktzahl für das Modul. Es kann leer sein, wenn der Teilnehmer kein Quiz absolviert hat oder der Inhalt keine Quizze enthält. |
| Unternommene Versuche | Die Gesamtanzahl der bisherigen Versuche des Teilnehmers für dieses Modul. |
| Maximal zulässige Versuche | Die maximale Anzahl der Versuche, die der Teilnehmer hat, um das Modul zu nutzen. |
| Kommentare zur Einreichung | Kommentare vom Manager eines Teilnehmers, nachdem dieser ein Lernobjekt abgeschlossen hat.<br>Die vom Kursleiter bereitgestellten Übermittlungskommentardaten sind im Dateiübermittlungsmodul enthalten. Weitere Informationen finden Sie unter <a href="https://experienceleague.adobe.com/en/docs/learning-manager/using/instructor/modules#filesubmissionforactivitymodules">Module-Adobe Learning Manager.</a></br> |
| Abschlussquelle | <b>Hinweis:</b> Wenn ein Teilnehmer bei VC Connector-Anwesenheitsarbeitsabläufen automatisch als anwesend markiert wird, zeigt die Quelle &quot;SELF, (learner_email)&quot; an. |
| Abschlusskommentar | Die Kommentare des Administrators, wenn er einen Teilnehmer als abgeschlossen markiert, nachdem er einen Kurs, eine Zertifizierung oder einen Lernpfad abgeschlossen hat. Der Administrator kann die Abschlusskommentare für einen oder mehrere Teilnehmer hinzufügen. Weitere Informationen finden Sie unter <a href="https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/courses#completion-comments">Abschlusskommentare</a>. |

**Informationen zu Lernobjekten**

Diese beziehen sich auf Kurse, Module, Lernpfade, Zertifizierungen usw.

| Feld | Beschreibung |
|---|---|
| Name des Lernplans | Titel des Lernplans. |
| LP/Zertifizierung/Kurs | Der Titel des Lernobjekts. |
| Typ | Der Typ des Lernobjekts, bei dem der Benutzer registriert wurde. Beispiel:<ul><li>Lernplan</li><li>Zertifizierung</li><li>Kurs</li></ul> |
| Eingebetteter Pfad | Ein eingebetteter Pfad ist ein Lernpfadtyp, der als Teil eines anderen Kurses enthalten ist     oder einem Lernpfad hinzufügen. Das Feld gibt an, dass ein Teilnehmer diesen Lernpfad als Teil eines anderen Lernpfads abschließt, anstatt als eigenständige Aufgabe. |
| Kurs | Name des Kurses, für den der Benutzer registriert ist. Wenn sie leer ist, stellt die Zeile entweder einen Zertifizierungs- oder einen Lernpfad dar. <br><b>Hinweis:</b> Obwohl Lernpfade und Zertifizierungen    aus einzelnen Kursen oder verschachtelten Lernpfaden zusammengesetzt sind, behält jede Komponente ihren eigenen unabhängigen Datensatz bei. Dadurch wird sichergestellt, dass Fortschritts-, Abschluss- und Berichtsdaten sowohl für das übergeordnete als auch für das untergeordnete Element getrennt verfolgt werden.</br> |
| LO Eindeutige ID | Eindeutige ID des Lernobjekts. Sie wird benötigt, wenn der Kunde das LO in einem externen System hat, das über eine eigene ID verfügt. Dies ist hilfreich, wenn Sie die LO-ID des externen Systems und Adobe Learning Manager LO zuordnen möchten.<br>Ein Administrator kann die Option &quot;Eindeutige Lernobjekt-IDs&quot; auf der Seite &quot;Einstellungen&quot; aktivieren. Wenn diese Option aktiviert ist, weist Adobe Learning Manager einem Lernobjekt jedes Mal eine eindeutige ID zu, wenn ein Autor einen Kurs, eine Zertifizierung oder einen Lernpfad erstellt. </br> |
| Instanz | Der Name der Instanz des Lernobjekt-Benutzers, bei dem Sie registriert sind. |
| Auswahlkriterien | Grundlage für die Registrierung (Angabe, wie dieser Teilnehmer in diesem Lernobjekt registriert wurde).<br>In Adobe Learning Manager können sich Teilnehmer über verschiedene Methoden für Lernobjekte registrieren: Vom Manager nominierte Registrierung: Manager nominieren Teilnehmer für bestimmte Kurse. Teilnehmer können sich für diese Kurse nicht selbst registrieren.</br><ul><li>Von Manager genehmigte Registrierung: Teilnehmer melden sich für Kurse an, aber die Registrierung erfordert die Genehmigung des Managers.</li><li>Selbstregistrierung Teilnehmer registrieren sich selbst direkt für Kurse, ohne dass eine Genehmigung erforderlich ist.</li><li>Administrator-Registriert: Administratoren registrieren Teilnehmer manuell für Kurse.</li></ul> |
| Modul | Name des Moduls innerhalb der Kurse. Nur die Module mit dem Status Abgeschlossen oder In Bearbeitung werden im Bericht angezeigt. Wenn der Status Nicht gestartet oder Nicht registriert ist, bleibt die Spalte Modul leer.<br>Laden Sie Informationen auf Modulebene in das Teilnehmertranskript herunter, indem Sie das Kontrollkästchen <b>Informationen auf Modulebene aktivieren</b> aktivieren. In diesem Fall werden Modulnamen und die für jedes Modul aufgewendete Zeit als Teil des Transkripts abgerufen, wenn diese Option aktiviert ist.</br> |
| Modul-ID | Eindeutige ID des Moduls.<br><b>Hinweis:</b> Die Spalte &quot;Modul-ID&quot; wird im Bericht nur angezeigt, wenn Sie beim Generieren des Transkripts das Kontrollkästchen &quot;Modulinformationen einschließen&quot; aktiviert haben.</br> |
| Version | Die Modulversion bezieht sich auf die bestimmte Version eines Moduls, mit der ein Teilnehmer interagiert hat. Dies ist besonders nützlich, wenn ein Modul aktualisiert oder geändert wurde, da Administratoren so verfolgen können, auf welche Version des Moduls der Teilnehmer zugegriffen hat.<br>Wenn ein Autor eine neue Version eines Moduls hochlädt, behandelt Adobe Learning Manager diese als eine neue Version des vorhandenen Moduls. Dadurch können Inhalte aktualisiert werden, ohne dass alle Teilnehmer unterbrochen werden.</br><br>Die Version wird angezeigt, wenn beim Generieren des Berichts das Kontrollkästchen <b>Informationen auf Modulebene aktivieren</b> aktiviert wurde.</br><br>Weitere Informationen finden Sie unter <a href="https://elearning.adobe.com/2023/03/updating-the-module-in-adobe-learning-manager-how-to-replace-a-content-module-in-a-course-without-disturbing-the-users-progress" />Aktualisieren eines Moduls in Adobe Learning Manager</a>.</br> |
| Bereitstellungstyp | Gibt an, wie das Modul bereitgestellt wird: Gemischt, Klassenzimmer oder Virtuelles Klassenzimmer. |
| Sprache | Sprache, in der das Modul vom Teilnehmer verwendet wird. In dieser Spalte wird nur Wert für eLearning-Module angezeigt. |
| Überfällig | Aktueller überfälliger Status des Teilnehmers, der für das Lernobjekt registriert ist. Ja//Nein |
| Bewertung | Gibt den Erfolg des Teilnehmers an. „Bestanden“, wenn der Benutzer die Erfolgskriterien erfüllt hat, ansonsten „Nicht bestanden“. |

>[!INFO]
>
>Die folgenden Spalten sind in den Teilnehmertranskripten ausgeblendet:
>
>* Anzahl der Registrierungen
>* Anzahl Begonnen
>* Anzahl der Abschlüsse
>* Fällig in N Tagen
>* Fällig in N Tagen für Benutzer
>* Anzahl von (Fortschritt größer als N %)
>* Anzahl von (Fortschritt größer als N %) für Benutzer
>
>Diese Spalten werden nur angezeigt, wenn Sie beim Generieren des Transkripts die Option &quot;Kenntnisdaten und Zusammenfassungsblätter einbeziehen&quot; aktiviert haben. Diese Spalten werden verwendet, um die Zusammenfassungsdetails eines Teilnehmers zu berechnen, der bei einem Lernobjekt registriert ist.

| Felder | Beschreibung |
|---|---|
| Schulungs-ID | Eine vom System generierte eindeutige Kennung, die der Registrierung jedes Teilnehmers für einen bestimmten Kurs, eine Zertifikatkennung oder einen bestimmten Lernpfad zugewiesen ist. Wenn sich ein Teilnehmer erneut für denselben Kurs registriert, wird eine neue Schulungs-ID generiert. Ein Teilnehmer kann über mehrere Schulungs-IDs für denselben Kurs verfügen. |
| Dauer der Schulung oder des Moduls (Min.) | In dieser Spalte wird die erwartete Dauer (in Minuten) eines Kurses, eines Moduls oder einer Schulungsaktivität angezeigt, die beim Erstellen des Kurses definiert wurde. Es ist nicht die tatsächliche Zeit, die ein Teilnehmer verbringt, sondern die konfigurierte/zugewiesene Dauer, die angibt, wie lange die Schulung dauern soll. <br>Diese Spalte zeigt die Gesamtdauer (in Minuten) des zugewiesenen Lernelements an, bei dem es sich entweder um einen Lernpfad oder um einen einzelnen Kurs handeln kann.</br><br><b>Dauer des Lernpfads:<b> Wenn das Schulungselement ein Lernpfad ist, wird seine Dauer als die Summe der Dauer aller Kurse innerhalb des Lernpfads berechnet.</br><br>Beispiel: Wenn Kurs 1 = 50 Minuten und Kurs 2 = 60 Minuten, dann ist die Lernpfaddauer = 110 Minuten.</br><br><b>Individuelle Kursdauer:</b>Wenn es sich bei dem Schulungselement um einen individuellen Kurs (nicht um einen Teil eines Lernpfads) handelt, spiegelt die Dauer die für diesen Kurs benötigte Zeit wider.</br> |
| Embedded_Course_ID | Die ID für den Kurs, der Teil eines Lernpfads oder eines anderen Kurses ist.<br>Die Spalte wird ausgefüllt, wenn die Zeile einen Lernpfad oder eine Zertifizierung selbst darstellt. Hier werden die IDs der einzelnen Kurse angezeigt, die im Lernpfad oder in der Zertifizierung eingebettet sind. Sie wird nicht ausgefüllt, wenn die Zeile selbst ein Kurs auf ly ist, da keine eingebetteten Elemente vorhanden sind.</br> |
| ID für eingebetteten Pfad | Die ID für den Pfad, in dem der eingebettete Kurs vorhanden ist.<br>Die Spalte identifiziert die eindeutige ID eingebetteter Lernpfade. Es hilft beim Verfolgen von Kursen innerhalb von Lernpfaden und bietet Transparenz in der hierarchischen Struktur von Lernpfaden.</br> |
| Datum der Aufhebung der Registrierung (UTC-Zeitzone) | Datum der Aufhebung der Registrierung des Teilnehmers für den Lernobjekttyp. |
| Preis($) | Der Preis des Lernobjekts, für das es im Kurskatalog erworben wurde. Damit diese Spalte im Teilnehmertranskript angezeigt wird, muss der Administrator das Kontrollkästchen Preise für Kurse/Lernpfade/Zertifizierungen aktivieren in den Kontoeinstellungen aktivieren. |

## Excel-Berichte

Im Dialogfeld &quot;Teilnehmertranskripte&quot; können Sie auch Kenntnisdaten und Zusammenfassungsblätter als Excel-Dateien herunterladen. Aktivieren Sie das Kontrollkästchen **[!UICONTROL Kenntnisdaten und Zusammenfassungsblätter einschließen]** und wählen Sie dann **[!UICONTROL Generieren]** aus, um eine Excel-Datei mit den folgenden Blättern herunterzuladen:

* Übersicht zu Lernprogrammen I
* Übersicht zu Lernprogrammen II
* Compliance-Übersicht
* Kenntnis-Transkript
* Übersicht über Kenntnisse I
* Kenntnis-Übersicht II



### Was enthält das Arbeitsblatt &quot;Übersicht zu Lernprogrammen&quot;?

Verfolgen Sie Lernpfade, Kurse oder Zertifizierungen, die aktiv genutzt werden. Verfolgen Sie die laufenden Aktivitäten sowie bevorstehende Termine für Schulungen.

* Anzahl der registrierten Teilnehmer: Gibt an, wie viele Teilnehmer sich für ein bestimmtes Lernobjekt (Kurs, Lernpfad oder Zertifizierung) registriert haben, unabhängig davon, ob sie es gestartet haben.
* Anzahl der Teilnehmer, die begonnen haben: Zeigt die Anzahl der Teilnehmer, die den Kurs, die Zertifizierung oder den Lernpfad gestartet oder gestartet haben.
* Anzahl der Teilnehmer, die die Schulung abgeschlossen haben: Zeigt an, wie viele Teilnehmer die Schulung erfolgreich abgeschlossen haben und alle Abschlusskriterien erfüllen.
* Anzahl der Teilnehmer, die ≥ N% fortgeschritten sind: Gibt die Anzahl der Teilnehmer an, die mindestens den angegebenen Fortschrittsschwellenwert (z. B. 70%) in der Schulung erreicht haben, auch wenn sie sie nicht abgeschlossen haben.
* Anzahl der Teilnehmer mit Fälligkeitsdatum in N Tagen: Gibt an, wie viele Teilnehmer innerhalb der nächsten &quot;N&quot; Tage (z. B. 7 Tage) eine Schulung benötigen, was zur Identifizierung bevorstehender Fristen nützlich ist.

### Interpretation der Daten

Dieser Bericht &quot;Lernzusammenfassung I&quot; verfolgt zwei Lernpfade, die dem Teilnehmer zugewiesen wurden.
Im Beispiel



* Der Benutzer ist für zwei Lernpfade registriert und hat beide begonnen.
* Es wurde noch keiner der Lernpfade abgeschlossen.
* Der Teilnehmer hat den Schwellenwert von 70 % in keinem der beiden Pfade überschritten.
* Innerhalb der nächsten sieben Tage fallen keine Termine für eine der beiden Schulungen an.

### Was enthält das Arbeitsblatt &quot;Lernzusammenfassung II&quot;?

Verfolgen Sie die Lernaktivität pro Teilnehmer. Verfolgen Sie Anmeldungen, laufende Aktivitäten sowie Fälligkeitstermine für Teilnehmer.

* Anzahl der registrierten Lernobjekte: Gesamtzahl der Lernobjekte (LOs), für die sich der Teilnehmer für jeden Kurs, jede Zertifizierung oder jeden Lernpfad registriert hat. zählt separat .
* Anzahl der gestarteten Lernobjekte: Gibt an, wie viele der registrierten Lernobjekte der Teilnehmer gestartet oder gestartet hat.
* Anzahl abgeschlossener Lernobjekte: Zeigt, wie viele der gestarteten LOs der Teilnehmer vollständig abgeschlossen hat.
* Anzahl der Lernobjekte, die ≥ N% fortgeschritten sind: Gibt die Anzahl der LOs an, in denen der Teilnehmer mindestens den angegebenen Fortschrittsschwellenwert erreicht hat (in diesem Fall 70%).
* Anzahl Lernobjekte mit Fälligkeitsdatum in N Tagen: Identifiziert LOs, die innerhalb der nächsten festgelegten Anzahl von Tagen (in diesem Fall 7 Tage) fällig sind, um die Verfolgung näherer Fristen zu erleichtern.

### Interpretation der Daten

Im Beispiel



* Der Teilnehmer ist bei zwei Lernobjekten registriert und hat beide gestartet.
* Es wurden keine Lernobjekte abgeschlossen.
* Der Teilnehmer hat bei keinem von ihnen einen Fortschritt von 70 % erzielt.
* Keines der Lernobjekte wird in den nächsten 7 Tagen fällig.

### Was enthält die Tabelle &quot;Einhaltungsübersicht&quot;?

Verfolgen Sie Teilnehmer mit bevorstehenden Fälligkeitsdaten für wichtige Kurse, Lernpfade oder Zertifizierungen.

| Spalte | Beschreibung |
|---|---|
| Typ | Der LO-Typ, für den die Tabelle &quot;Lernzusammenfassung&quot; Daten anzeigen soll. |
| Zeilenbeschriftungen (linke Spalte) | Der Name des Teilnehmers mit der Liste der LOs, bei denen der Teilnehmer registriert ist. |

### Was enthält das Kenntnistranskriptblatt?

| Spalte | Beschreibung |
|---|---|
| Name | Vollständiger Name des Teilnehmers, der mit dem Kenntnistranskript verknüpft ist. |
| E-Mail | E-Mail-Adresse des Teilnehmers. |
| Eindeutige ID des Benutzers | Durch die Organisation definierte eindeutige Kennung für den Teilnehmer. |
| Kenntnisse | Der Name der Kenntnisse, die dem Teilnehmer zugewiesen sind (z. B. Java-Programmierung, Führung). |
| Kenntnisstufen | Der Kenntnisstand innerhalb der Kenntnisse, die der Teilnehmer erreichen soll (z. B. Anfänger, Fortgeschrittene, Fortgeschrittene). |
| Erforderliche Punktzahl | Anzahl der Lernressourcen, die zum Erreichen der zugewiesenen Kenntnisstufe benötigt werden. |
| Erhaltene Punkte | Anzahl der Credits, die der Teilnehmer für den Abschluss der zugewiesenen Kenntnisstufe gesammelt hat. |
| Abgeschlossen % | Der Prozentsatz der erforderlichen Credits, die der Teilnehmer abgeschlossen hat. |
| Zugewiesenes Datum (UTC) | Das Datum, an dem die Kenntnisse dem Teilnehmer zugewiesen wurden. |
| Erreichtes Datum (UTC) | Das Datum, an dem der Teilnehmer die erforderlichen Credits erworben und die Kriterien für die Kenntnisstufe erfüllt hat. |
| Managername | Name des Managers des Teilnehmers, der den Lernfortschritt überwacht. |

### Was enthält das Blatt &quot;Kenntnisübersicht I&quot;?

| Spalte | Beschreibung |
|---|---|
| Nachher | Gibt die Anzahl der Teilnehmer an, die Kenntnisse vor einem definierten Zeitraum (in Tagen) erworben haben, nach dessen Ablauf die Kenntnisse als veraltet gelten oder aktualisiert werden müssen. Nützlich, um Teilnehmer mit anstehenden oder abgelaufenen Qualifikationsleistungen zu identifizieren.<br>Weitere Informationen finden Sie unter <a href="https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/skills-levels">Qualifikationsstufen</a>. |
| Name | Vollständiger Name des Teilnehmers, dem die Kenntnisse zugewiesen sind. |
| Managername | Name des Berichts-Managers des Teilnehmers. |
| Zeilenbeschriftungen | Der spezifische Kenntnisname, der Teilnehmern in dieser Zeile zugewiesen ist. Wird als Gruppierungskopfzeile verwendet, um die Kenntnisdaten von Teilnehmern unter jeder Kenntniskategorie zusammenzufassen. |
| Anzahl der Benutzer, die diese Kenntnisse haben sollten | Gesamtzahl der Teilnehmer, denen die spezifische Kenntnis zugewiesen wurde. |
| Anzahl der Benutzer, die diese Kenntnisse erworben haben | Anzahl der Teilnehmer, die die erforderlichen Lernobjekte erfolgreich abgeschlossen haben, um die Kenntnisse zu erlangen. |
| Anzahl der Teilnehmer, deren Kenntnisse aufgefrischt werden müssen | Die Anzahl der Teilnehmer, deren Kenntniserreichungsdaten den definierten Aktualisierungsschwellenwert überschreiten. |
| Prozent der Compliance (Basierend auf erreichten Kenntnissen) | Die Compliance- oder Adoptionsrate für Kenntnisse. |


### Was enthält das Blatt &quot;Kenntnisübersicht II&quot;?

| Spalte | Beschreibung |
|---|---|
| Nachher | Anzahl der Kenntnisse, die der Teilnehmer vor dem definierten Aktualisierungsschwellenwert (in Tagen) erreicht hat. Dadurch werden Kenntnisse identifiziert, die möglicherweise veraltet sind und aktualisiert werden müssen. |
| Kenntnisse | Name der Kenntnisse, die Teilnehmern zugewiesen sind. Dies könnte mit einem oder mehreren Lernobjekten verknüpft sein, z. B. Kursen, Zertifizierungen oder Lernpfaden. |
| Managername | Der Name des direkten Managers des Teilnehmers. |
| Zeilenbeschriftungen | Der vollständige Name des Teilnehmers. Für jeden Teilnehmer werden die Kenntnisse und der Fortschritt in den folgenden Spalten angezeigt. |
| Anzahl der Kenntnisse, die jeder Benutzer haben sollte | Gesamtanzahl der Kenntnisse, die dem Teilnehmer zugewiesen sind. |
| Anzahl der Kenntnisse, die jeder Benutzer hat | Gesamtzahl der Kenntnisse, die der Teilnehmer durch Abschluss der zugeordneten Lernobjekte erfolgreich erworben hat. |
| Anzahl der Kenntnisse, die aktualisiert werden müssen | Die Anzahl der erreichten Kenntnisse, die die Aktualisierungsdauer überschritten haben und jetzt erneuert werden müssen. Mit diesem Wert können Sie den Erneuerungsbedarf von Schulungen im Hinblick auf Compliance oder kontinuierliche Entwicklung nachverfolgen. |
| Prozentsatz der Kompatibilität | Gibt die allgemeine Compliance-Stufe des Teilnehmers basierend auf dem erreichten Kenntnisstand an. |

## Downloadverlauf der Teilnehmertranskripte

Mit dem Verlauf der Downloads von Teilnehmertranskripten können Administratoren nachverfolgen, wer das Transkript der einzelnen Teilnehmer heruntergeladen hat und auf welche Benutzer sie zugegriffen haben. Diese Funktion ist besonders vorteilhaft in unternehmensspezifischen und Compliance-orientierten Umgebungen, in denen mehrere Stakeholder Lerndatensätze anzeigen müssen.

Nach dem Herunterladen eines Teilnehmertranskripts werden auf der Seite &quot;Teilnehmertranskripte&quot; alle Transkripte aufgeführt, die von einem Benutzer auf der Plattform generiert werden.



In der Liste werden die folgenden Attribute angezeigt:

* Von und Bis: Dauer der herunterzuladenden Transkripte.
* Generiert von: Die E-Mail-Adresse des Benutzers, der den Bericht heruntergeladen oder den Download angefordert hat.
* Teilnehmer: Teilnehmer oder Teilnehmergruppen, deren Transkripte heruntergeladen werden sollen.
* Angewendete Filter: Die Filter, die für den Registrierungsstatus angewendet wurden.
* Zusätzliche Daten enthalten: Die zusätzlichen Daten (gelöschte Teilnehmer, Modulinformationen sowie Qualifikationsdaten und Zusammenfassungsblätter), die der Administrator für die Option &quot;Erweitert&quot; im Modul &quot;Teilnehmertranskript hinzufügen&quot; angefordert hatte
* Status: Heruntergeladen, in der Warteschlange oder in Bearbeitung.
* Abbrechen : Brechen Sie die Berichterstellung jederzeit ab.

## Weitere Überlegungen zu Teilnehmertranskripten

Teilnehmertranskripte enthalten verschiedene Verhalten, die Administratoren beachten sollten:

**Anzeige von Lernpfad und Kursfortschritt**

Alle Kurse, die Teil eines Lernpfads (LP) sind, werden im Teilnehmertranskript angezeigt, auch wenn der Teilnehmer nur in einem der Kurse Fortschritte gemacht hat. Dies stellt die vollständige Sichtbarkeit eines Lernpfads sicher, auch wenn der Fortschritt teilweise abgeschlossen ist.

**Daten für gelöschte Teilnehmer**

Wenn ein Teilnehmer von der Plattform gelöscht wurde, zeigt sein Transkript seine Datensätze nicht in den Berichten an, die für die Benutzergruppe generiert wurden, zu der er gehörte. Dies bedeutet, dass die Datensätze gelöschter Teilnehmer aus gefilterten Berichten ausgeschlossen werden, die mit Benutzergruppenfiltern erstellt wurden.

Sie können jedoch weiterhin die Daten der gelöschten Teilnehmer herunterladen. Wenn Sie beim Festlegen der Filter zum Generieren des Berichts die Option **[!UICONTROL Gelöschte Teilnehmer einschließen]** ausgewählt haben, können Sie den Bericht für die gelöschten Teilnehmer herunterladen.



**Verhalten für benutzerdefinierte Administratoren**

Benutzerdefinierte Administratoren mit einem definierten Umfang (z. B. beschränkt auf bestimmte Kataloge oder Benutzergruppen) sehen gefilterte Transkriptdaten basierend auf ihrem Umfang:

* Benutzergruppenumfang: Nur Teilnehmer in der Benutzergruppe mit dem Umfang des benutzerdefinierten Administrators werden in den Bericht aufgenommen.
* Katalogbereich: Nur Lernobjekte (Kurse, Zertifizierungen und Lernpfade), die den Katalogen mit Umfang zugewiesen sind, werden in den Bericht aufgenommen.
* Gefilterte Spalten: Die Spalten bleiben unverändert. Nur die Zeilen werden basierend auf den Geltungsbereichen von Katalogen und Benutzergruppen angepasst.

Dies stellt sicher, dass benutzerdefinierte Administratoren mit Umfang nur die Daten und Lerninhalte des Teilnehmers anzeigen, für deren Verwaltung sie autorisiert sind.

**Connector-Unterstützung**

Auf den Teilnehmertranskriptbericht kann über die Administrator-Benutzeroberfläche, [FTP, Box, Job-API oder Power BI](/help/migrated/integration-admin/feature-summary/connectors.md) zugegriffen werden. Er ist nicht in den einheitlichen Berichten von Salesforce, Power BI und Marketo Engage enthalten.

Vereinheitlichte Berichte, die aus Salesforce, Marketo Engage und Power BI heruntergeladen wurden, enthalten weniger Spalten als Teilnehmertranskripte.







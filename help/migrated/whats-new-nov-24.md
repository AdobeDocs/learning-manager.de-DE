---
description: Erfahren Sie mehr über die neuen Funktionen und Verbesserungen in der Version November 2024 von Adobe Learning Manager
jcr-language: en_us
title: Überblick über die neuen Funktionen November 2024
exl-id: 4dfe0e31-d202-4a6e-8c4f-43851218699f
source-git-commit: 7b84a4565ccf109ed4789f4963d6e250f5d0a852
workflow-type: tm+mt
source-wordcount: '3264'
ht-degree: 1%

---

# Überblick über die neuen Funktionen November 2024 {#new-features-summary}

Erfahren Sie mehr über die neuen Funktionen und Verbesserungen in der Version November 2024 von Adobe Learning Manager.

* **KI-gestützte Suche:** Kombiniert lexikalische und semantische Suche nach intelligenteren, kontextsensitiven Ergebnissen.
* **Webhooks**: Integrieren Sie Webhooks, um Echtzeitinformationen an bestimmte URLs zu senden.
* **LTI (Learning Tools Interoperability)**: Unterstützt LTI für die Interoperabilität mit anderen LMS-Plattformen.
* **Credly integration**: Verwalten und teilen Sie externe Abzeichen über Credly.
* **Verbesserungen am Kompatibilitäts-Dashboard**: Freigeben von Dashboards für andere Administratoren und Festlegen von Standard-Kompatibilitäts-Widgets auf den Teilnehmer-Startseiten.
* **Unterstützung mehrerer Sprachen**: Erstellen sprachspezifischer Instanzen für Klassenzimmer- und virtuelle Klassenzimmermodule.
* **Benutzerdefinierte Rollen**: Verbesserte Kontrolle über Benutzerrollen und Berechtigungen.
* **Abschlusskommentare**: Fügen Sie Kommentare hinzu, wenn Sie Teilnehmer als abgeschlossen markieren.
* **Benutzergruppenbericht**: Verwalten von Benutzergruppen mit detaillierten Berichten.
* **Wartelistenbericht**: Laden Sie die Warteliste der Teilnehmer für Kursinstanzen herunter.
* **Verbesserungen an der Barrierefreiheit**: Unterstützung für Alternativtext für Mastertitel und Unternehmenslogos.
* **Unterstützung für Hindi**: Unterstützung der Schnittstellensprache für Hindi.
* **Höflichkeitsscheck**: Sperren Sie Social-Media-Posts mit unzulässigen Wörtern.
* **Optimierung der E-Mail-Vorlage**: Kombinierte und optimierte E-Mail-Vorlagen für Kursleiterzuweisungen und Sitzungsabbrüche.
* **MS Teams-Abschlusskriterien**: Legen Sie die Mindestteilnahmezeit für VILT-Sitzungen fest.
* **Neue Migrationsarbeitsabläufe**: Migrationsänderungen umfassen Abschlusskriterien für Kurse und Module sowie die Migration von Modulen in Ordner.

>[!NOTE]
>
>Weitere Informationen zu den neuen Funktionen in dieser Version finden Sie in diesem [Webinar](https://cdn.content.adobelearningmanageracademy.com/public/newlearner/newlearner_0dc0f1e8.html#/overviewPage?instanceId=11932477&loId=11231360&loType=course).

## KI-gestützte Suche in Adobe Learning Manager

Adobe Learning Manager verbessert die Art und Weise, wie Teilnehmer nach Kursen oder Schulungen suchen. Es wird eine KI-gestützte Suchfunktion eingeführt, die lexikalische und semantische Suche kombiniert. Die Suche ist jetzt intelligenter, da sie nach bestimmten Begriffen sucht und den Kontext und die Absicht dahinter versteht. Die erweiterte Suche versteht die Bedeutung Ihrer Abfrage und liefert relevante Ergebnisse. Es identifiziert den Hauptfokus der Suche, um Ihnen den vollständigsten Satz an Ergebnissen zu bieten.

>[!NOTE]
>
>KI-gestützte Suche ist nur für Teilnehmer verfügbar.

Weitere Informationen finden Sie in diesem Artikel [Erweiterte Suche](/help/migrated/learners/feature-summary/advanced-search.md).

## Webhooks

Adobe Learning Manager ermöglicht die Integration mit Webhooks, um Echtzeitinformationen wie Kursanmeldungen, Kurserstellung und andere Informationen an eine bestimmte URL zu senden.

Ein Webhook in ALM ermöglicht es einer Entität, Daten automatisch über HTTP an eine andere Anwendung zu senden. Dadurch kann eine Anwendung anderen Anwendungen Informationen bereitstellen, ohne ständig danach zu fragen. Wenn ein Benutzer beispielsweise einen LMS-Kurs (Learning Management System) abschließt, kann ein Webhook diese Informationen automatisch an eine andere Plattform senden, z. B. ein CRM- oder Reporting-Tool. Webhooks werden häufig in Integrationen verwendet, um Prozesse zu automatisieren und die Notwendigkeit manueller Aktualisierungen zwischen Systemen zu reduzieren. Richten Sie Webhooks ein, indem Sie eine Rückruf-URL angeben, an die Sie die Daten senden würden.

Weitere Informationen finden Sie in diesem Artikel [Webhooks](/help/migrated/integration-admin/feature-summary/webhooks.md).

## Interoperabilität der Lernwerkzeuge

Adobe Learning Manager unterstützt jetzt LTI, um die Interoperabilität zwischen Adobe Learning Manager und anderen Lernmanagementsystemen (LMS) zu verbessern.

### Was ist LTI?

LTI (Learning Tools Interoperability) ist ein Standard, mit dem Tools und Inhaltsanbieter von Drittanbietern sich mit einem Learning Management System (LMS) verbinden können. Benutzer können direkt in ihrem LMS auf externe Lerninhalte von externen Inhaltsanbietern zugreifen, ohne sich anzumelden oder zu einem anderen LMS zu navigieren.

**LTI als Toolanbieter**: LTI als Toolanbieter ermöglicht die Integration externer Systeme in ein LMS. Adobe Learning Manager fungiert als LTI-Tool-Anbieter, der anderen LMS-Plattformen den Zugriff auf Kurse, Zertifikate oder Lernpfade über die Adobe Learning Manager direkt in ihrem LMS ermöglicht.

**LTI als Tool Consumer**: LTI als Tool Consumer ermöglicht LMS die Integration externer Tools über Learning Tools Interoperability (LTI). In diesem Szenario ist LMS ein Verbraucher von Diensten, die von externen Tools bereitgestellt werden. Adobe Learning Manager fungiert als LTI Tool Consumer und ermöglicht die Integration von Drittanbieter-Lerntools. Dadurch können Adobe Learning Manager-Teilnehmer die Kurse, Zertifikate oder Lernpfade aus den Tools von Drittanbietern in der Adobe Learning Manager nutzen.

Weitere Informationen finden Sie in diesem Artikel [Interoperabilität des Lerntools](/help/migrated/integration-admin/feature-summary/learning-tools-interoperability.md).

## Credly

Mit Credly können Administratoren in ALM externe Abzeichen von der Plattform über verschiedene Social-Media-Kanäle verwalten und freigeben.

### Was ist Credly?

Credly ist eine digitale Anmeldeplattform, mit der Teilnehmer und Organisationen professionelle Leistungen wie Abzeichen oder Zertifizierungen erwerben, freigeben und verifizieren können. Die Teilnehmer können Abzeichen über ihr Credly-Profil in sozialen Medien und an anderen Orten verwalten und teilen.

### Credly Integration mit Adobe Learning Manager

Fügen Sie zunächst den Credly Connector in Adobe Learning Manager (ALM) hinzu. Als Nächstes migrieren Sie die vorhandenen Abzeichen von Credly, um die Kontinuität der Lernerfolge zu gewährleisten. Erstellen Sie zum Schluss Kenntnisse in Adobe Learning Manager, um den entsprechenden Lernpfad zu verwenden und so die Entwicklung und den Wiedererkennungswert der Teilnehmer zu verbessern.

Weitere Informationen finden Sie in diesem Artikel [Credly](/help/migrated/integration-admin/feature-summary/credly-integration.md)

## Kompatibilitäts-Dashboard

In dieser Version können Administratoren das Dashboard jetzt für andere Administratoren, benutzerdefinierte Administratoren und Store-Manager freigeben, sodass sie sofort Zugriff auf die Compliance-Dashboards haben. Sie können jetzt das Standard-Compliance-Widget auf der Startseite des Teilnehmers festlegen, sodass Teilnehmer ihre Compliance-Anforderungen verfolgen können. Weitere Informationen finden Sie in diesem Artikel [Kompatibilitäts-Dashboard](/help/migrated/administrators/feature-summary/reports.md#share-compliance-dashboard-with-admins-and-custom-admins).

## Unterstützung mehrerer Sprachen

Mit Adobe Learning Manager (ALM) können Autoren jetzt sprachspezifische Instanzen mithilfe von Sprach-Tagging für Klassenzimmer- und virtuelle Klassenzimmermodule erstellen. Teilnehmer können auf CR/VC-Module in ihrer bevorzugten Sprache zugreifen. Beispielsweise kann ein Autor ein CR/VC-Modul mit zwei Instanzen erstellen: eine auf Englisch und eine auf Französisch. Teilnehmer können die Instanzen in ihrer bevorzugten Sprache auswählen.

Weitere Informationen finden Sie in diesem Artikel [Hinzufügen von Lernobjekten in verschiedenen Gebietsschemas](/help/migrated/authors/feature-summary/add-new-language-learning-objects.md#multi-language-support-for-crvc-instances-with-language-tagging).

## Benutzerdefinierte Rollen

Mit benutzerdefinierten Rollen können Administratoren bestimmte Rollen und Verantwortlichkeiten für verschiedene Benutzergruppen definieren und so eine bessere Verwaltung und Kontrolle sicherstellen. Mit dieser Version erweitert ALM die benutzerdefinierten Rollen, indem es eine detailliertere Kontrolle über die folgenden Abschnitte bietet.

* Benutzer
* Kurse
* Lernpläne
* Zertifizierungen
* Arbeitshilfen
* Kataloge

Administratoren können basierend auf den Verantwortlichkeiten der Benutzer präzise Berechtigungen zuweisen, sodass jede Gruppe nur Zugriff auf relevante Funktionen und Inhalte hat. Diese erweiterten Steuerelemente ermöglichen eine detailliertere Verwaltung von Schlüsselabschnitten.

Melden Sie sich als Administrator an und navigieren Sie zu **[!UICONTROL Benutzer]** > **[!UICONTROL Benutzerdefinierte Rollen]**, um die benutzerdefinierten Rollen zu erstellen und zu verwalten.

Weitere Informationen finden Sie in diesem Artikel [Benutzerdefinierte Rollen](/help/migrated/administrators/feature-summary/custom-role.md).

## Abschlusskommentare

Administratoren können jetzt Kommentare hinzufügen, wenn sie Teilnehmer in Kursen, Lernpfaden oder Zertifizierungen als abgeschlossen markieren. Administratoren können Kommentare für einen oder mehrere Teilnehmer gleichzeitig hinzufügen. Die Kommentare werden im Bericht [Teilnehmertranskripte](/help/migrated/administrators/feature-summary/reports.md#learner-transcripts) angezeigt.

Weitere Informationen finden Sie in diesem Artikel [Abschlusskommentare](/help/migrated/administrators/feature-summary/courses.md#completion-comments).

## Benutzergruppebericht

Der neue **[!UICONTROL Benutzergruppenbericht von Adobe Learning Manager]** hilft bei der Verwaltung von Benutzergruppen, indem er Einblick in Gruppen bietet, die nicht verwaltet werden, wenn Administratoren das Programm verlassen. Administratoren können auf die Berichte im Abschnitt **[!UICONTROL Benutzer]** > **[!UICONTROL Benutzergruppe]** zugreifen. Er enthält detaillierte Informationen zu den einzelnen Gruppen, einschließlich:

* Benutzergruppentyp
* Gruppenname
* Beschreibung
* Erstellt von (Name)
* Erstellt von (E-Mail)
* Erstellt am (UTC-Zeitzone)
* Anzahl der Benutzer

Weitere Informationen finden Sie in diesem Artikel [Benutzergruppenbericht](/help/migrated/administrators/feature-summary/add-users-user-groups.md#user-group-report).

## Wartelistenbericht

Mit dem neuen **[!UICONTROL Wartelistenbericht]** von Adobe Learning Manager können Administratoren die Warteliste von Teilnehmern für alle Instanzen eines Kurses herunterladen. Administratoren und Kursleiter können über den Abschnitt **[!UICONTROL Warteliste]** auf der Seite **[!UICONTROL Kurs]** oder **[!UICONTROL Sitzungsübersicht]** auf diesen Bericht zugreifen. Der Wartelistenbericht kann aus den Bereichen Admin und Kursleiter heruntergeladen werden.

Die folgenden Spalten sind im Bericht &quot;Warteliste&quot; verfügbar:

* Kursname
* Instanzname
* Instanzen-ID
* Instanzenstatus
* Benutzername
* E-Mail
* Eindeutige ID des Benutzers
* Registriert am (UTC-Zeitzone)
* Status
* Warteliste Nummer
* Limit für Warteliste
* Maximale Anzahl Lizenzen

Lesen Sie diesen Artikel [Wartelistenbericht (Administrator)](/help/migrated/administrators/feature-summary/courses.md#waitlist-report) und [Wartelistenbericht (Kursleiter)](/help/migrated/instructors/feature-summary/learners.md#waitlist-report), um den Bericht aus dem Abschnitt &quot;Administrator und Kursleiter&quot; herunterzuladen.

## Barrierefreiheit auf der Teilnehmer-Startseite

Adobe Learning Manager unterstützt jetzt Alt-Text für alle Mastertitel, um die Barrierefreiheit für Teilnehmer zu verbessern. Dadurch können Teilnehmer mit besonderen Anforderungen Bildschirmleseprogramme verwenden, um den Alternativtext zu lesen und das Bild zu verstehen. Sie können mehrere Sprachen auswählen und für jede Sprache einen Alternativtext angeben. Stellen Sie sicher, dass Sie den Alternativtext in den jeweiligen Sprachen hinzufügen. Stellen Sie sicher, dass das Firmenlogo in Ihrem Konto auch Alternativtext mit dem Firmennamen enthält.
Weitere Informationen finden Sie in diesem Artikel [Ankündigung](/help/migrated/administrators/feature-summary/announcements.md#masthead).

## Unterstützung für Hindi

Adobe Learning Manager führt Hindi jetzt als eine der Schnittstellensprachen der Plattform ein und unterstützt das Wachstum der Plattform in Indien. Die Unterstützung für Hindi-Muttersprachler stellt sicher, dass alle Funktionen, Berichte und das gesamte Benutzererlebnis für die Benutzer vollständig zugänglich sind.

>[!NOTE]
>
>Abzeichenzertifikate, die vom System im PDF-Format generiert werden, unterstützen Hindi nicht.

Um die Sprache der Benutzeroberfläche zu ändern, führen Sie die folgenden Schritte aus:

1. Melden Sie sich als **[!UICONTROL Administrator]** an.
2. Wechseln Sie zu **[!UICONTROL Profileinstellungen]** > **[!UICONTROL Schnittstellensprache]**.
3. Wählen Sie **[!UICONTROL Hindi]** als Schnittstellensprache aus.


## Profanity-Check für Social-Media-Beiträge

Adobe Learning Manager blockiert jetzt Social-Media-Beiträge in der Teilnehmer-App, die unzulässige Wörter enthalten. Dies hilft, die Dinge professionell und gesetzeskonform zu halten, insbesondere in sensiblen Bereichen wie der Gesundheitsversorgung.

## Optimierung von E-Mail-Vorlagen

### E-Mail-Teilnehmer, wenn ein Kursleiter zugewiesen ist

Die vorhandenen E-Mails **[!UICONTROL Sie wurden als Kursleiter hinzugefügt]** und **[!UICONTROL VCProvider Session Details]** wurden in einer E-Mail zusammengefasst **[!UICONTROL Sie wurden als Benutzertyp hinzugefügt]**. Der **[!UICONTROL UserType]** ist je nach Rolle des Benutzers entweder **[!UICONTROL Kursleiter]** oder **[!UICONTROL Organizer]**. Diese E-Mails waren zuvor nicht in der Benutzeroberfläche verfügbar. Sie wurden jetzt in einer einzigen E-Mail zusammengefasst und der Benutzeroberfläche hinzugefügt. Administratoren können im Abschnitt **[!UICONTROL E-Mail-Vorlage]** auf diese Vorlage zugreifen. Es wird standardmäßig für alle neuen und vorhandenen Konten aktiviert, aber Administratoren können es im selben Abschnitt deaktivieren oder aktivieren. Diese E-Mail wird immer gesendet, wenn eine Sitzung erstellt wird und einem Kursleiter zugewiesen wird, unabhängig davon, ob es sich um eine Sitzung wie Zoom, Teams, Connect oder andere Dienste handelt.

### E-Mail-Teilnehmer, wenn eine Sitzung abgebrochen wird

Die Kursleiter, die aus einer Sitzung entfernt werden, erhalten jetzt nur eine E-Mail zum Abbruch der Sitzung. Zuvor erhielten sie sowohl eine Stornierungs- als auch eine Aktualisierungs-E-Mail. Kursleiter, die in einer Sitzung bleiben, erhalten eine E-Mail zur Sitzungsaktualisierung zusammen mit einer neuen Einladung zur Sitzung.

## Abschlusskriterien für MS Teams

Derzeit werden Teilnehmer als anwesend markiert, auch wenn sie nur für einige Sekunden an einer virtuellen Kursleitersitzung (VILT) teilnehmen. Mit dieser Version haben wir Abschlusskriterien für Teams-Module eingeführt, um eine genauere Teilnahme zu gewährleisten. Autoren können jetzt eine Mindestzeit festlegen, die die Teilnehmer in einer VILT-Sitzung verbringen müssen, damit ihre Anwesenheit gezählt werden kann.

Dies ist eine Backend-Funktion, die standardmäßig deaktiviert ist. Wenden Sie sich an Ihren CSM, um ihn zu aktivieren.

## Aktualisieren neuer IP-Adressen für die E-Mail-Übermittlung

Um die Zuverlässigkeit der E-Mail-Bereitstellung zu erhöhen, fügen wir unserem vorhandenen Pool neue IP-Adressen hinzu. Damit es zu keinen Unterbrechungen bei der E-Mail-Kommunikation kommt, aktualisieren Sie die E-Mail-Einstellungen Ihrer Organisation nach Bedarf.

Wir verwenden derzeit die folgenden IP-Adressen für die E-Mail-Zustellung:

* 149.72.162.66
* 167.89.5.155

Die folgenden IP-Adressen werden unserem E-Mail-Bereitstellungspool hinzugefügt:

* 159.183.228.93
* 159.183.225.26
* 159.183.218.22
* 168.245.57.144

>[!NOTE]
>
>Bei Bedarf empfehlen wir die Zusammenarbeit mit Ihrem IT-Team, um die IP-Adressen zur Liste der zulässigen URLs hinzuzufügen.

## Migrationsänderungen

Die folgenden Änderungen werden am Migrationsarbeitsablauf vorgenommen:

* Migrieren von Modulen in bestimmte Ordner.
* Es wurden Abschlusskriterien für Module hinzugefügt.
* Hinzugefügte Abschlusskriterien für Kurse

### Änderungen an der Modulmigration

Wenn Sie Module in ALM migrieren, werden sie standardmäßig im öffentlichen Ordner gespeichert. In dieser Version haben wir eine neue Spalte mit dem Namen &quot;`folder`&quot; in der Datei &quot;[module_version.csv](assets/module_version.csv)&quot; hinzugefügt. Administratoren können diese Spalte verwenden, um den Ordnernamen anzugeben, in den die Module nach der Migration verschoben werden sollen. Administratoren können ein einzelnes Modul auch in mehrere Ordner platzieren, indem sie die Ordnernamen durch Kommas getrennt auflisten.

Die Ordnerspalte verwendet den Datentyp string und es handelt sich um eine optionale Spalte. Die folgenden Bedingungen gelten für die Ordnerspalte:

* Der Ordnername, den Sie hinzufügen, sollte ein vorhandener Inhaltsordner im ALM-Konto sein.
* Die Werte sollten eine durch Kommas getrennte Zeichenfolge sein.
* Wenn Sie einen neuen Ordnernamen für ein Modul hinzufügen, das bereits in einem anderen Ordner vorhanden ist, wird der zugewiesene Ordner durch den neuen Wert nicht überschrieben oder ersetzt. Das Modul wird dem neuen Ordner hinzugefügt und bleibt auch im vorhandenen Ordner verfügbar.
* Wenn der Wert leer ist, wird standardmäßig **[!UICONTROL Öffentlich]** als Ordner verwendet.

Weitere Informationen finden Sie in der CSV-Spezifikation [&#128279;](assets/4-module_version.xlsx) für module_version.

### Änderungen an der Modulmigration - Abschlusskriterien

Administratoren können die Abschlusskriterien der Module während der Modulmigration angeben. In dieser Version haben wir die neuen Spalten &quot;`completionCriteria`&quot;, &quot;`viewPercent`&quot; und &quot;`quizData`&quot; in der Datei &quot;[module_version.csv](assets/module_version.csv)&quot; hinzugefügt.

Im Folgenden sind die Bedingungen für die neuen Spalten aufgeführt:

1. `completionCriteria`

   * Der Datentyp sollte eine Zeichenfolge sein, und die unterstützten Werte lauten:
      * `LAUNCH_CONTENT`
      * `VIEW_PERCENT`
      * `QUIZ`
      * `MARK_COMPLETE`
   * Fügen Sie Abschlusskriterien auf Modulebene nur für Modultypen zum Selbststudium hinzu.
   * Die unterstützten Werte für statischen Inhalt sind `LAUNCH_CONTENT` und `VIEW_PERCENT`.
   * Die unterstützten Werte für interaktive Inhalte sind `LAUNCH_CONTENT`, `VIEW_PERCENT` und `QUIZ`.
   * Die unterstützten Werte für den HTML5-Inhalt sind `LAUNCH_CONTENT` und `MARK_COMPLETE`.

2. `viewPercent`:

   * Der Datentyp für diese Spalte muss eine Ganzzahl sein und der Wert muss zwischen 0 und 100 liegen.
   * Wenn &quot;completeCriteria&quot; auf &quot;`VIEW_PERCENT`&quot; festgelegt ist, geben Sie den erforderlichen Ansichtsprozentsatz in diese Spalte ein, oder lassen Sie das Feld leer.

3. `quizData`:

   * Der Datentyp muss ein Zeichenfolgenwert sein. Unterstützte Werte sind `QUIZ_ATTEMPTED`, `QUIZ_PASSED` und `QUIZPASSED_OR_LIMITREACHED`.
   * Wenn `completionCriteria` auf `QUIZ` festgelegt ist, geben Sie den entsprechenden Quizwert in die Spalte `quizData` ein.

Weitere Informationen finden Sie in der CSV-Spezifikation [&#128279;](assets/4-module_version.xlsx) für module_version.

### Änderungen an der Kursmigration - Abschlusskriterien

Administratoren können die Abschlusskriterien für die Kurse während der Kursmigration angeben. In dieser Version haben wir eine neue Spalte mit dem Namen &quot;`completionCriteria`&quot; in &quot;[course.csv](assets/course.csv)&quot; hinzugefügt.

Die folgenden Bedingungen gelten für die Spalte &quot;`completionCriteria`&quot;:

* Der Datentyp sollte entweder eine Zeichenfolge oder eine Zahl sein, und es handelt sich um ein optionales Feld.
* Die Werte müssen `ALL`, `X` und `SELECTEDMODULES` sein.
* X ist ein ganzzahliger Wert, der größer als 0 und kleiner als die Gesamtzahl der Module sein sollte.
* Wenn Sie `completionCriteria` auf `SELECTEDMODULES` festlegen, müssen Sie die obligatorischen Module in der Datei [course_module.csv](assets/course_module.csv) markieren.
* Geben Sie in der Spalte &quot;`optionalCriteria`&quot; &quot;`TRUE`&quot; oder &quot;`FALSE`&quot; ein. Wenn Sie den Wert &quot;`TRUE`&quot; festlegen, ist das Modul obligatorisch.

Weitere Informationen finden Sie in der CSV-Kursspezifikation [CSV-Kursspezifikation](assets/3-course.xlsx) und in der CSV-Kursspezifikationsdatei [Kursmodul](assets/6-course_module.xlsx).

## API-Änderungen

Die API-Änderungen lauten wie folgt:

* **Such-API**:
   * Neuer Modusfilter mit Optionen: classicSearch und advancedSearch.
   * Neue Option loMetadata für snippetTypes.
* **Ankündigungs-API**:
   * Enthält das altText-Attribut für Mastertitel-Beschreibungen.
* **Instanz-APIs**:
   * Neues Gebietsschemaattribut zum Abrufen von Gebietsschemadetails.
* **Höflichkeitsprüfung**:
   * Aktualisierte APIs, um in Kommentaren und Antworten auf soziale Beiträge nach verbotenen Wörtern zu suchen:
* **RPM und Burstbegrenzung**:
   * RPM (Anforderungen pro Minute) und Burst-Grenzen für alle APIs hinzugefügt.
* **Abzeichen-APIs**:
   * Neues Attribut externalProvider zum Abrufen von Informationen über externe Abzeichen.
* **Job-API**:
   * Laden Sie den Benutzergruppenbericht und den Audit-Bericht für benutzerdefinierte Rollen mithilfe der Job-API herunter.

### Änderungen an der Such-API

Die Such-API verfügt jetzt über einen neuen Modusfilter mit zwei Optionen: `classicSearch` und `advanceSearch`. Es gibt auch eine neue `loMetadata`-Option für `snippetTypes`. Um die besten Ergebnisse zu erzielen, schließen Sie `loMetadata` im Modus `advanceSearch` in `snippetTypes` ein.

### Änderungen an der Ankündigungs-API

Das `GET /announcements API`-Attribut enthält jetzt das `altText`-Attribut, um die Mastertitel-Beschreibung bereitzustellen.

#### Beispielanforderung mit cURL:

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 12345678' 'https://abcd.adobe.com/primeapi/v2/announcements/123456'
```

#### Beispielantwort:

```
{
  "links": {
    "self": "https://abcd.adobe.com/primeapi/v2/announcements/123456"
  },
  "data": {
    "id": "12345",
    "type": "adminAnnouncement",
    "attributes": {
      "actionUrl": "google.com",
      "announcementType": "MASTHEAD",
      "expiryDate": "2038-01-19T03:14:07.000Z",
      "liveDate": "2024-07-31T11:11:30.000Z",
      "contentMetaData": [
        {
          "contentType": "IMAGE",
          "contentUrl": "https://abcd.adobe.com",
          "locale": "en-US",
          "altText": "Moonlight - english changed new",
          "thumbnailUrl": "https://abcd.adobe.com/"
        },      ]
    }
  }
}
```

### Änderungen an Instanz-APIs

Das neue `locale`-Attribut wurde den folgenden APIs hinzugefügt, um Gebietsschemadetails abzurufen.

* `GET /learningObjects/{loId}/instances/{loInstanceId}`
* `GET /learningObjects/{id}?include=instances,enrollment.loInstance`
* `GET /learningObjects?include=instances,enrollment.loInstance`
* `GET /learningObjects/{id}/relatedLOs?include=instances,enrollment.loInstance`
* `POST /learningObjects/query?include=instances,enrollment.loInstance`
* `POST /search/query?include=model.instances`
* `GET /search?include=model.instances`

#### Beispielanforderung mit cURL:

```
curl --location 'http://abcd.com/primeapi/v2/learningObjects/course:1234567/instances/course:1234567_1234567' \
```

#### Beispielanforderung:

```
{
    "links": {
        "self": "http://abcd.com/primeapi/v2/learningObjects/course:1234567/instances/course:1234567_1234567"
    },
    "data": {
        "id": "course:1234567_1234567",
        "type": "learningObjectInstance",
        "attributes": {
            "dateCreated": "2024-02-27T09:21:25.000Z",
            "isAET": false,
            "isDefault": true,
            "isFlexible": false,
            "locale": "en-US",
            "state": "Active",
            "localizedMetadata": [
                {
                    "locale": "en-US",
                    "name": "Default instance"
                }
            ]
        },
        "relationships": {
            "learningObject": {
                "data": {
                    "id": "course:1234567",
                    "type": "learningObject"
                }
            },
            "loResources": {
                "data": [
                    {
                        "id": "course:123456_1234567_1234567_1",
                        "type": "learningObjectResource"
                    }
                ]
            }
        }
    }
}
```

### Öffentliche API-Änderungen für die Überprüfung der Profanität

Die folgenden APIs wurden aktualisiert, um Profitprüfungen für Kommentare und Antworten auf Social-Media-Beiträge durchzuführen.

* `POST /boards/{id}/posts `
* `PATCH /posts/{id}`
* `POST /posts/{id}/comments`
* `PATCH /comments/{id}`
* `POST /comments/{id}/replies`
* `PATCH /replies/{id}`

Wenn ein eingeschränktes Wort im Beitrag gefunden wird, wird die folgende Antwort gesendet.

#### Beispielantwort:

```
{
  "status": "FORBIDDEN",
  "title": "BAD_WORD_FOUND",
  "source": {
    "info": "Unacceptable word found in post"
  }
}
```

### Änderungen bei der RPM- und Burstbegrenzung

In dieser Version wurden RPM (Requests Per Minute)- und Burst-Limits für alle APIs hinzugefügt. Die maximale RPM für jede API kann auf der Swagger-Seite überprüft werden.

RPM ist die Anzahl der Anforderungen, die Sie in einer Minute an den API-Server senden können. Das Burst-Limit erlaubt eine höhere Anzahl von Anfragen für eine kurze Zeit, die über das übliche Ratenlimit hinausgeht. Die `learningObject`-API lässt beispielsweise maximal 15 Anforderungen pro Minute zu. Wenn dieses Limit überschritten wird, gibt die API eine Fehlermeldung zurück.

### Änderungen an Abzeichen-APIs

Das neue Attribut &quot;`externalProvider`&quot; wurde den folgenden APIs hinzugefügt, um Informationen über externe Abzeichen abzurufen, einschließlich Abzeichen-ID und Anbietername.

* `GET /badges `
* `GET /badges/{id}`
* `GET /skills?include=levels.badge`
* `GET /skills/{id}?include=levels.badge`
* `GET /learningObjects/{loId}/instances/{loInstanceId}?include=badge`
* `GET /users/{userId}/userBadges`
* `GET /users/{userId}/userBadges/{id}`

#### Beispielanforderung mit cURL:

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 123456789' 'https://abcd.adobe.com/primeapi/v2/badges/44'
```

#### Beispielantwort:

```
{
  "links": {
    "self": "https://abcd.adobe.com/primeapi/v2/badges/44"
  },
  "data": {
    "id": "44",
    "type": "badge",
    "attributes": {
      "imageUrl": "https://abcd.com/accountassets/1/badges/download.png",
      "name": "external badge",
      "state": "Active",
      "externalProvider": {
        "id": "1234sjd-b272-4de1-9b60-1234567",
        "provider": "credly"
      }
    }
  }
}
```

### Prüfberichte für Benutzergruppen und benutzerdefinierte Rollen über die Job-API herunterladen

Der Benutzer kann den **[!UICONTROL Benutzergruppenbericht]** und den **[!UICONTROL Audit-Bericht für benutzerdefinierte Rollen]** mithilfe von `Job API` herunterladen.

#### Beispielanforderung für den Download des Benutzergruppenberichts:

```
curl -X POST --header 'Content-Type: application/vnd.api+json;charset=UTF-8' --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 12345678' -d '{ \ 
     "data": { \ 
         "type": "job", \ 
         "attributes": { \ 
             "jobType": "generateUserGroupReport" \ 
         } \ 
    } \ 
 }' 'https://abcd.adobe.com/primeapi/v2/jobs'
```

#### Beispiel für eine Anforderung zum Herunterladen eines Audit-Berichts für benutzerdefinierte Rollen:

```
curl -X POST --header 'Content-Type: application/vnd.api+json;charset=UTF-8' --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 1234567' -d '{
    "data": {
        "type": "job",
        "attributes": {
            "description": "description of your choice",
            "jobType": "generateCustomRoleAuditReport",
            "payload":{
                 "fromDate": "2020-01-01T18:30:00.000Z",
                 "toDate": "2024-09-31T18:30:00.000Z",
                 "locale":  "en-US"
            }
        }
   }
}
```

### Fehlermeldung für keinen Anforderungstext

Wir haben spezielle Fehlermeldungen für Fälle eingeführt, in denen der Anforderungstext obligatorisch ist, aber nicht in der API bereitgestellt wird.

#### Beispielfehlermeldung:

```
{
    "status": "BAD_REQUEST",
    "title": "Generic Error"
}
```

## Verbesserte Berichterstellung

Administratoren können diese Berichtsänderungen im Abschnitt **Admin** > **Berichte** finden.

### Teilnehmertranskriptbericht

Der Bericht **[!UICONTROL Teilnehmertranskripte]** enthält zwei neue Spalten:

* **[!UICONTROL Modul-ID]**: Zeigt die eindeutige Kennung für jedes Modul an. Diese neue Spalte wurde nach der vorhandenen Spalte **[!UICONTROL Module]** hinzugefügt.
* **[!UICONTROL Kursinstanz-ID]**: Zeigt die eindeutige Kennung für jede Kursinstanz an. Diese neue Spalte wurde nach der vorhandenen **[!UICONTROL Instanz]**-Spalte hinzugefügt.
* **[!UICONTROL Abschlusskommentar]**: In dieser Spalte werden die Kommentare erfasst, die der Administrator beim Markieren des Benutzerabschlusses eingegeben hat. Diese neue Spalte wurde am Ende des Berichts hinzugefügt.


### Sitzungsübersicht – Bericht

Der Bericht **[!UICONTROL Sitzungsübersicht]** enthält drei neue Spalten:

* Die Spalte **[!UICONTROL Modul-ID]** wurde vor der Spalte **[!UICONTROL Sitzungsname]** hinzugefügt.
* Die Spalte **[!UICONTROL Sitzungs-ID]** wurde vor der Spalte **[!UICONTROL Sitzungsname]** hinzugefügt.
* Die Spalte **[!UICONTROL Kursinstanzkennung]** wurde nach der Spalte **[!UICONTROL Instanzname]** hinzugefügt.
* Die Spalte **[!UICONTROL Anzahl der Abschlüsse]** wurde nach der Spalte **[!UICONTROL Anzahl der Registrierungen]** hinzugefügt.

## In diesem Update behobene Fehler

* Der Fehler, der beim Hochladen von Videos aus dem Aktivitätsmodul während der Dateiübermittlung auf Android- und iOS-Geräten aufgetreten ist, wurde behoben.
* Das Problem beim Öffnen von Kursen in der mobilen App wurde behoben. Die Webversion funktioniert ordnungsgemäß.
* Das Problem beim Anzeigen von Arbeitshilfen und anderen Ressourcen in Safari wurde behoben.
* Es wurde ein Problem behoben, das Benutzer daran hinderte, Arbeitshilfen in die mobile App herunterzuladen.
* Der Fehler in der Dokumentation für die Patch-Benutzer-API wurde behoben.
* Es wurde ein Problem behoben, durch das Organisatoren keine E-Mail-Benachrichtigungen erhielten, wenn eine Sitzung aus dem Kurs gelöscht wurde.
* Es wurde ein Problem behoben, durch das Organisatoren keine E-Mails zum Abbruch der Sitzung erhielten, wenn ein Modul aus dem Kurs entfernt und erneut veröffentlicht wurde.
* Es wurde Unterstützung für die Aufnahme von Sonderzeichen &quot;+&quot; und &quot;-&quot; in E-Mail-Adressen während der Erstellung durch externe Benutzer hinzugefügt.
* Es wurde ein Problem behoben, durch das die Synchronisierung des einheitlichen Berichts des Marketo-Connectors fehlschlug, wenn der Bericht zu Benutzerkenntnissen doppelte Anführungszeichen im CSV-Datensatzwert enthielt.
* Es wurde ein Problem behoben, durch das der Endpunkt &quot;`/skills`&quot; den richtigen Status für die Admin-API zurückgab, die Teilnehmer-API jedoch durchgehend falsche oder zwischengespeicherte Daten anzeigt.
* Es wurde ein Problem mit dem Go1-Onboarding für Freemium-Kurse behoben, das fehlschlug, wenn der Go1-Connector im Konto nicht eingerichtet war.
* Es wurde ein Problem behoben, durch das Kurse im Lernpfad (LP) nicht über die Migration zugänglich waren, wenn der Teilnehmer das LP bereits abgeschlossen hatte.
* Es wurde ein Problem behoben, durch das die inkrementelle Benutzer-CSV fehlschlug, wenn sowohl der Manager des Benutzers als auch der Manager auf Übersprungebene als SU (Super User) anstatt als Administrator festgelegt wurden und nicht in der CSV enthalten waren.
* Die Bereichsprobleme für Store Manager in Dashboard-Berichten wurden behoben.
* Es wurde das Problem behoben, dass xapi_iri nicht entfernt wurde, wenn ein Kursentwurf gelöscht wurde.
* Es wurde ein Problem behoben, das in bestimmten Szenarien das Hinzufügen einer eindeutigen LO-ID verhinderte.
* Es wurde ein Problem behoben, bei dem die IsEmbeddable-Eigenschaft im Lernplan in freigegebenen Lernplänen nicht korrekt aktualisiert wurde.
* Es wurde ein Problem behoben, das die Anzeige der Gesamtdauer von Lernpfaden in der Teilnehmeransicht betraf.
* Es wurde ein Problem behoben, durch das es Teilnehmern ermöglicht wurde, sich über Links zur Selbstregistrierung zu registrieren oder zu registrieren, selbst wenn ihre Konten gelöscht wurden.
* Es wurde das Problem behoben, dass `www` entfernt wurde, wenn während der Kurserstellung Links in der Kursbeschreibung hinzugefügt wurden.
* Es wurde ein Problem behoben, bei dem die Informationen zum Ausblenden und Herunterladen von Arbeitshilfen nicht ordnungsgemäß funktionierten.
* Es wurde ein Problem behoben, durch das Single Sign-on (SSO) nicht für neue Benutzer funktionierte, die über den Link zur Selbstregistrierung mit einer IP-ID hinzugefügt wurden.
* Es wurde ein Problem behoben, bei dem die Daten von Benachrichtigungsnachrichten nicht abgerufen wurden, nachdem eine Ankündigung gelöscht wurde.
* Es wurde das Problem behoben, dass bei der Suche nach Benutzern per E-Mail nicht genügend Suchergebnisse angezeigt wurden.

## Systemanforderungen

[Systemanforderungen für Adobe Learning Manager anzeigen](/help/migrated/system-requirements.md).

## Versionshinweise

Lesen Sie die [Versionshinweise](/help/migrated/release-note/release-notes.md) für die neuesten Versionsupdates.

## Frühere Versionen von Adobe Learning Manager

* [Version Juli 2024](/help/migrated/whats-new-july-2024.md)
* [Version März 2024](/help/migrated/whats-new-march-2024.md)

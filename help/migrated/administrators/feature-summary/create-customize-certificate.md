---
title: Zertifikat erstellen und anpassen
description: Mit benutzerdefinierten Zertifikaten in Adobe Learning Manager (ALM) können Administratoren und Autoren personalisierte Zertifikate für Teilnehmer entwerfen, verwalten und ausstellen.
jcr-language: en-us
exl-id: 99e20f00-9f8f-477f-9416-24636ed23b87
source-git-commit: 13fbdb95129ba7612e8e42d3da88ef3c6784e729
workflow-type: tm+mt
source-wordcount: '2628'
ht-degree: 0%

---

# Benutzerdefinierte Zertifikate in Adobe Learning Manager

## Einführung

Benutzerdefinierte Zertifikate in Adobe Learning Manager ändern, wie Administratoren Abschlusszertifikate entwerfen, verwalten und bereitstellen.

Administratoren haben folgende Möglichkeiten:

- Designe Zertifikate in einem visuellen Editor im Leinwandformat, anstatt Code zu schreiben.
- Fügen Sie Zertifikate mit flexiblen Standardvorgaben an Kurse, Lernpfade und Zertifizierungen an.
- Generative Hintergründe auf Basis von Adobe Firefly berücksichtigen nicht nur die Anforderungen an Markendarstellung und Compliance.
- Migrieren Sie von bestehenden HTML-Vorlagen und bleiben Sie mit den bisherigen Teilnehmerdatensätzen kompatibel.

Der Zertifizierungsprozess folgt dem bestehenden Abzeichen- und Leistungsmodell im Learning Manager, sodass das Verhalten der Teilnehmer vertraut bleibt, während Administratoren und Support-Teams weniger Zeit mit Zertifikatvorgängen verbringen.

>[!NOTE]
>
>Zertifikatfunktionen, die generative KI verwenden, unterliegen der Quote. Das Limit beträgt 10.000 Anfragen pro Kunde.

## Wichtigste Merkmale einer individuellen Zertifizierung

### Zertifikat-Designer (Canvas-Stil-Editor)

Ein Drag-and-Drop-Zertifikatdesigner bietet eine WYSIWYG-Arbeitsfläche, auf der Administratoren Designs ohne HTML- oder CSS-Kenntnisse erstellen und verwalten können.

**Visuelle Bearbeitung**

- Text und Bilder lassen sich ziehen, positionieren, skalieren, spiegeln und drehen.
- Elemente ausrichten (oben, unten, links, rechts) - Elemente nach hinten oder nach vorne ausrichten.
- Dupliziere oder klone Elemente, um das Layout zu beschleunigen.

**Unterstützte Elemente**

- Textfelder mit Steuerelementen für Schriftart, Farbe, Größe und Ausrichtung.
- Dynamische Platzhalter (z. B. Name des Teilnehmers, Name des Kurses oder der Zertifizierung, Datum, Kontofelder und aktive Benutzerfelder, bei denen nur Attribute mit einem Wert zulässig sind).
- Bilder, einschließlich Logos und Badges, bei denen die manuelle Größenanpassung dem automatischen Einpassen für ein vorhersagbares Layout vorgezogen wird.

**Hintergrund und Layout**

- Hoch- oder Querformat (nach Erstellung fixiert).
- Hintergründe in Volltonfarben oder Bilder mit anpassbarer Transparenz.
- Bildergalerie mit vordefinierten Bildern und freigegebenen Hintergründen.
- Zoomsteuerungen (50 %-150 %) und Raster- oder Ausrichtungsoptionen.

**Lokalisierung**

- Unterstützung mehrerer Gebietsschemas, wobei jedes Gebietsschema eine eigene Layoutdatei hat.
- Wenn Sie ein Gebietsschema hinzufügen, wird dessen Layout vom Standardgebietsschema kopiert und kann dann angepasst werden.
- Dropdown-Liste &quot;Sprache&quot; mit Vorschau für jedes Gebietsschema zur Entwurfszeit.

**Lebenszyklus für Entwürfe und Veröffentlichungen**

- Speichern Sie Designs als Entwürfe; Entwürfe können nicht für die Ausgabe verwendet werden.
- Nach der Veröffentlichung ist die Designstruktur gesperrt. Bei einigen Änderungen muss das Design möglicherweise stattdessen dupliziert werden.
- Echtzeitvorschau für PDF zum Überprüfen des Layouts vor der Veröffentlichung.

### Vorlagenkatalog und -auflistung

Auf der Listingseite **Zertifikatdesign** können Administratoren Zertifikatvorlagen skaliert verwalten:

- Kachelbasierter Katalog mit Registerkarten **Veröffentlicht** und **Entwurf**.
- Suche nach Zertifikatstitel; Filter nach **Ausrichtung**.
- Aktionen für jedes Design:
   - Duplizieren (für Varianten).
   - Als Standard auf der Ebene **Konto**, **Kurs**, **Lernpfad** oder **Zertifizierung** festgelegt.
   - Nicht mehr verwendete Vorlagen einstellen oder deaktivieren.
- Unterstützung für Drittanbieter-Vorlagen, die integriert und wiederverwendet werden können.

### Flexible Konfiguration und Vererbung

Administratoren können Zertifikate auf mehreren Ebenen konfigurieren:

**Standardwerte auf Kontoebene**

- Legen Sie ein Standardzertifikatdesign für alle neuen Lernobjekte fest.
- Die Standardeinstellung dient als Ausgangspunkt. Bestehende LOs werden nicht automatisch geändert, wenn sich die Standardeinstellung des Kontos ändert.

**Modifikationen auf Instanzebene**

- Konfiguration auf Instanzebene für Kurse, Zertifizierungen und Lernpfade, einschließlich:
   - Branding pro Kohorte (z. B. für unterschiedliche Regionen oder Partnerkonten).
   - Verschiedene Zertifikatdesigns für wiederkehrende Zertifizierungszyklen.

**Zertifikatauflösung und Fallback**

Wenn ein Teilnehmer die Schulung abschließt, wählt der Lern-Manager ein Design in dieser Reihenfolge aus:

- LO-Instanzkonfiguration
- LO-Konfiguration
- LO-Standardvorlage
- Standardvorlage für Konto

### Generative Hintergründe auf Adobe Firefly-Basis

Damit Kunden konsistente, markenkonforme Zertifikate in großem Umfang erstellen können, lässt sich der Designer in Adobe Firefly integrieren:

- Administratoren generieren Hintergründe aus Stichwort-Eingabeaufforderungen und einem Farbschema (z. B. &quot;minimalistisch, Healthcare, blaugrüne Palette&quot;).
- Eine kuratierte Schlüsselwortbibliothek unterstützt gängige Branchen (Versand, Gesundheitswesen und andere) für Benutzer, die keine Designer sind.
- Generierte Bilder werden der Hintergrundgalerie hinzugefügt und können in verschiedenen Vorlagen wiederverwendet werden.
- Kredit- und Stufenfunktionen für die Firefly-Nutzung im Learning Manager sind durch die Produktrichtlinie definiert.

### Migration von alten HTML-Zertifikaten

Vorhandene HTML- oder ZIP-Zertifikatvorlagen bleiben erhalten, können jedoch im neuen Designer nicht bearbeitet werden:

- Ältere Vorlagen werden mit Markierungen wie `isLegacy` / `is_active` migriert.
- Sie werden als nicht bearbeitbare Einträge angezeigt (keine WYSIWYG-Vorschau) und bleiben für die historische Verwendung gültig.
- Wenn Abzeichen mit älteren Vorlagen verknüpft waren, können Zertifikate bei der Migration weiterhin heruntergeladen werden. Wenn die Konfiguration nicht beibehalten werden kann, gelten die globalen Standardeinstellungen.

### PDF-Generierung und Vorbacken

So verbessern Sie die Laufzeitleistung und die Lernerfahrung der Teilnehmer:

- Zertifikate werden zur Abschlusszeit (wenn das LO abgeschlossen ist) vorgebacken und dann zwischengespeichert, sodass die Teilnehmer sie schnell herunterladen können.
- Vorhandene Teilnehmer-Flows für das Herunterladen von Zertifikaten über **Abzeichen** und **Erfolge** bleiben unverändert.

## Die Herausforderung

Heute hängt die Zertifikatverwaltung in Learning Manager von einem codeintensiven, unterstützungsintensiven Modell ab:

**Hohe Abhängigkeit von CSM und Support-Teams**: Administratoren stellen HTML- oder ZIP-Dateien bereit, die von CSMs oder Engineering über interne Tools hochgeladen werden. Jede Änderung (Branding, Logos, vorgeschriebener Text, Signaturen) erfordert ein internes Ticket und einen Implementierungszyklus.

**Eingeschränkte Agilität für Business-Teams**: Marketing-, Compliance- oder HR-Teams benötigen häufig häufige, lokalisierte Zertifikataktualisierungen (Sprachen, Kampagnen, länderspezifische Regeln). Der aktuelle Arbeitsablauf verlangsamt diese Aktualisierungen und verzögert Compliance-Programme.

**Fragmentierte Konfiguration und unklare Vererbung**: Legacy-HTML-Vorlagen können auf Konto-, Lernobjektstandard- und Lernobjektebene mit komplexen Fallbackregeln festgelegt werden. Ohne klare, mehrstufige, benutzerdefinierte Konfiguration kann es schwierig sein, zu erkennen, welche Vorlage wo angewendet wird.

**Einschränkungen für Abzeichenverknüpfungen** Zertifikate sind eng mit **Abzeichen** verknüpft:

- Ein Zertifikat muss mit einem Abzeichen verknüpft sein. Es gibt keine reine Zertifikatausgabe.
Diese Verknüpfung kann Design-Änderungen erschweren, wenn Administratoren Zertifikate ohne Gamification-Elemente benötigen.

**Nicht visuelles Authoring und Markeninkonsistenz**: HTML-basierte Zertifikate sind flexibel, benötigen jedoch Frontend-Kenntnisse, die viele Administratoren nicht haben. Einige Kunden vertrauen auf generische Standardzertifikate, was die Markenkonsistenz schwächt.

**Wettbewerbslücke**: Einige Lernmanagementsysteme enthalten native benutzerdefinierte Zertifikatdesigner (z. B. Docebo). Das Self-Service-Zertifikatdesign in diesem Bereich war für Adobe Learning Manager eine bekannte Lücke.

Das Ergebnis sind langsame Änderungen, hohe Supportkosten und ein Authoring-Erlebnis, das nicht den Erwartungen des Administrators an Zertifikate und Anmeldeinformationen entspricht.

## Wie benutzerdefinierte Zertifizierungen diese Herausforderungen bewältigen

### Self-Service-Workflows mit Administratorfreundlichkeit

Dies sind die Workflows:

- Die Zertifikatgestaltung und -auflistung ersetzen HTML-Upload-Skripte und die interne Bereitstellung durch eine administratorgesteuerte Erfahrung:
- Administratoren erstellen, veröffentlichen und einstellen Zertifikatdesigns im Learning Manager ohne Code- oder CSM-Beteiligung.
- Design-Aktualisierungen (z. B. saisonales oder partnerspezifisches Branding) dauern in der Benutzeroberfläche Minuten statt der Tickets und Engineering-Zyklen.
- Standardeinstellungen auf Konto- und Lernobjektebene reduzieren die sich wiederholende Konfiguration pro Objekt.

### Geringerer Support-Aufwand und geringeres operatives Risiko

Durch Konsolidieren der Zertifikatverwaltung unter **Erfolge** mit einem klaren Benutzererlebnis:

- Die Arbeitslasten für Anforderungen zum Hochladen oder Ändern meines Zertifikats werden für CSM- und Engineering-Teams verringert.
- Das Produkt wendet sichere Einschränkungen an (z. B. gesperrte Ausrichtung, nicht bearbeitbare ältere Vorlagen), um das Risiko für vorhandene Bereitstellungen zu reduzieren.
- Bei migrierten älteren Vorlagen sind historische Zertifikate ohne zusätzlichen Support verfügbar.

### Governance, Konsistenz und Markenkontrolle.

Standardeinstellungen, Firefly und Galerien helfen Kunden bei Folgendem:

- Sie müssen die Vorlagen nur einmal auf Kontoebene versenden und nur bei Bedarf überschreiben.
- Verwenden Sie Firefly-Hintergründe in Unternehmensführungslinien anstelle von Ad-hoc-Elementen aus externen Elementen.
- Steuern von Zertifikaten über den Status &quot;Veröffentlichen&quot; und &quot;Aussetzen&quot; mit vorschaubaren Entwürfen vor dem Rollout.

### Ausrichtung an vorhandenen Abzeichen- und Zertifikat-Flows

Das Design behält den aktuellen Teilnehmerpfad bei: Zertifikate werden weiterhin von **Abzeichen** und **Leistungen** heruntergeladen, was die Umschulung einschränkt.

### Performance und Skalierbarkeit

Vorkonfigurierte Zertifikate und JSON-gesteuerte Rendering-Zielleistung:

- Zertifikate werden nach der Fertigstellung generiert und gespeichert. Daher ist der Download praktisch ein statischer Abruf.
- JSON-basierte Designs bleiben für den Editor und das Rendern zur Laufzeit in großem Umfang kompakt.

## Nutzungsszenarien in der Praxis

### Kunden- und Partnerschulungen: skalierte Anmeldedaten

**Szenario:** Ein Softwareunternehmen betreibt Kunden- und Partnerakademien mit Hunderten von Programmen in verschiedenen Regionen und Marken.

- Verwenden Sie Standardvorlagen auf Kontoebene mit von Firefly generierten Hintergründen, die jeder Produktlinie zugeordnet sind.
- Fügen Sie gebietsschemaspezifische Layouts für lokalisierte Zertifizierungstitel, Haftungsausschlüsse und Unterschriften hinzu.
- Bei Premium-Partnern können Sie Basisvorlagen duplizieren und Partner-Co-Branding (Logo und rechtmäßiger Text) auf Instanzebene hinzufügen.
- Mit vorkonfigurierten PDF können Partner Zertifikate direkt nach Abschluss der Partnerzertifizierungen herunterladen, ohne den Learning Manager zu belasten.

Dieses Muster passt in Franchise- oder Multi-Brand-Ökosysteme, in denen Zertifikate den Wert der Marke und des Partners stärken (z. B. große Partnernetzwerke wie RealPage).

### Compliance- und regulatorische Schulungen: stark veränderte Umgebungen mit mehreren Standorten

**Szenario:** Ein reguliertes Unternehmen muss den Wortlaut des Konformitätszertifikats häufig nach Land und Sprache aktualisieren.

- Durch die **Bearbeitung durch den Administrator** können Rechts- oder Compliance-Teams Formulierungen und dynamische Felder ohne Engineering-Tickets ändern.
- Gebietsschemaspezifische Layouts unterstützen **länder- oder regionsspezifische Haftungsausschlüsse** und Signaturen auf einer freigegebenen Entwurfsgrundlage.
- **Die Fallback-Logik** stellt sicher, dass das System weiterhin sichere Standardwerte verwendet und Fehler vermeidet, wenn eine bestimmte LO-Instanzvorlage fehlt.

Dies gilt für das Gesundheitswesen, den Finanzsektor, den öffentlichen Sektor und andere Branchen, in denen sich der Zertifikatstext häufig ändert und geprüft wird.

### Wiederkehrende Zertifizierungen mit Peer- oder freigegebenen Kataloginhalten

**Szenario:** Ein Master-Learning Manager-Konto teilt Inhalte mit mehreren **Peer-Konten** (z. B. vielen Kundenkonten), die jeweils wiederkehrende Zertifizierungen und eigene Zertifikate aufweisen.

- Peer-Konten können **erworbene Kurse zu wiederkehrenden Zertifizierungen hinzufügen** und **lokale Zertifikatvorlagen** auf Instanzebene konfigurieren.
- Kursaktualisierungen vom Masterkonto fließen wie erwartet in Wiederholungen, während Zertifikatdesigns **pro Kunde** bleiben können.

### Interne Enablement- und Führungsprogramme.

**Szenario:** Interne Programme (z. B. Manager Accelerators oder Product Academies) wünschen **visuell getrennte Zertifikate**, die Administratoren ohne HTML aktualisieren können.

- Programmverantwortliche können **Vorlagen mit Branding für Programme** entwerfen (z. B. für eine interne Akademie oder ein visuelles Element im MAP-Stil), ohne HTML-Kenntnisse zu benötigen.
- Durch Modifikationen auf Instanzebene können verschiedene Kohorten oder Regionen Varianten verwenden (z. B. kohortenspezifisches oder regionales Branding).
- Firefly-Hintergründe unterstützen **ereignisspezifische oder kohortenspezifische** Grafiken mit weniger Abhängigkeit von Designteams.

### Übergang von älteren HTML-Zertifikaten

**Szenario:** Bestandskunden verwenden über CSMs verwaltete benutzerdefinierte HTML5-Zertifikate.

- Ältere HTML- oder ZIP-Vorlagen werden migriert und als veraltet markiert, wodurch die bisherige Nutzung und frühere Downloads beibehalten werden.
- Administratoren können im Laufe der Zeit zu designerbasierten Vorlagen wechseln, wobei Programme mit hoher Priorität den Anfang bilden.
- Wenn die Migration eine Zuordnung nicht beibehalten kann (z. B. Abzeichen, die in der Mitte deaktiviert sind), wird das System auf die globale Standardvorlage zurückgesetzt, damit die Teilnehmer nicht blockiert werden.

## Erstellen eines benutzerdefinierten Zertifikats

**Voraussetzung**

Um Bilder von Firefly verwenden zu können, muss Ihre Adobe Learning Manager-Instanz mit Firefly integriert sein.

1. Melden Sie sich bei Adobe Learning Manager als **Administrator** an.
2. Wählen Sie im Abschnitt **Konfigurieren** die Option **Erfolge** aus. Die Seite **Abzeichen** wird geöffnet.
   ![Benutzerdefiniertes Zertifikat erstellen](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate1.png)
   *Im linken Navigationsbereich zu &quot;Erfolge&quot; navigieren*

3. Wählen Sie im linken Navigationsbereich **Zertifikate**. Die Seite **Zertifikate** wird geöffnet.
   ![Benutzerdefiniertes Zertifikat erstellen](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate2.png)
   *Die Zertifikatsseite*

4. Wählen Sie im oberen rechten Bereich der Seite **Neues Zertifikat**. Das Dialogfeld **Neues Zertifikat erstellen** wird geöffnet.
5. Wählen Sie je nachdem, wie das Zertifikat aussehen soll, die Option **Querformat** oder **Hochformat** aus. Nachdem Sie eine Ausrichtung ausgewählt haben, werden eine leere Vorlage und vorgefertigte Vorlagen für diese Ausrichtung angezeigt.
   ![Benutzerdefiniertes Zertifikat erstellen](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate3.png)
   *Option &quot;Querformat&quot; oder &quot;Hochformat&quot;*

6. Wählen Sie die leere Vorlage oder eine vorhandene Vorlage aus.
7. Geben Sie einen Zertifikatsnamen ein.
8. Wählen Sie im Dropdownmenü eine Standardsprache aus.
9. Wählen Sie **Erstellen** aus. Wenn Sie die leere Vorlage auswählen, wird eine leere Arbeitsfläche unter Ihrem Zertifikatnamen angezeigt.
10. Fügen Sie Elemente hinzu: **Text**, **Image**, **Dynamischer Wert** und **Zertifikathintergrund**.
    ![Benutzerdefiniertes Zertifikat erstellen](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate4.png)
    *Elemente zum Zertifikat hinzufügen*

11. Fügen Sie für **Text** Inhalt unter **Vorformatierter Text** oder **Textvorlagen** hinzu, oder fügen Sie benutzerdefinierten Text hinzu. Der Text wird auf der Arbeitsfläche angezeigt. Wenn Text ausgewählt ist, werden Formatierungsoptionen über der Arbeitsfläche angezeigt. Um unerwünschte Inhalte zu entfernen, wählen Sie das Symbol **Löschen** in der oberen rechten Ecke der Arbeitsfläche aus.
12. Um Bilder hinzuzufügen, wählen Sie **Bild** neben **Elemente hinzufügen**. Bilder von Ihrem Computer hochladen oder Bilder aus den Kategorielisten auswählen.
13. Wählen Sie **Dynamischer Wert**, um grundlegende Details, Katalogbeschriftungen und aktive Felder hinzuzufügen.
14. Wählen Sie **Zertifikatshintergrund** aus, um Farben oder Bilder anzuwenden. Um Bilder mit Adobe Firefly zu erstellen, wählen Sie **Image generieren**.
15. Beschreiben Sie im Feld &quot;Eingabeaufforderung&quot;, was Sie möchten (bis zu 100 Zeichen), und wählen Sie **Generieren**. Je nach Aufforderung werden vier Bildoptionen angezeigt.
16. Wählen Sie das gewünschte Bild aus. Es wird als Hintergrund für das Zertifikat angewendet.
    ![Benutzerdefiniertes Zertifikat erstellen](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate5.png)
    *Bild zum Zertifikat hinzufügen*

17. Wählen Sie **Vorschau**, um das Zertifikat vor der Veröffentlichung zu überprüfen. So können Sie das Aussehen des Zertifikats besser nachvollziehen.
    ![Benutzerdefiniertes Zertifikat erstellen](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate6.png)
    *Zertifikat in der Vorschau anzeigen*

18. In der Vorschau können Sie Inhalte auf Google Drive speichern, herunterladen, drucken oder andere Optionen wie Anmerkungen oder Dokumenteigenschaften verwenden.
19. Wählen Sie **Als Entwurf speichern**, um später fortzufahren, oder wählen Sie **Publish** aus, um das Zertifikat zu veröffentlichen. Nach der Veröffentlichung können Teilnehmer das Zertifikat herunterladen, wenn sie den konfigurierten Meilenstein erreichen.

Nachdem Sie ein Zertifikat unter **Veröffentlicht** oder **Entwürfe** gespeichert haben, können Sie es bearbeiten, klonen, umbenennen oder löschen.

## Benutzerdefiniertes Zertifikat bearbeiten

1. Wählen Sie im Abschnitt **Konfigurieren** die Option **Erfolge** aus. Die Seite **Abzeichen** wird geöffnet.
2. Wählen Sie im linken Navigationsbereich **Zertifikate**. Die Seite **Zertifikate** wird geöffnet.
3. Wählen Sie die Registerkarte **Veröffentlicht** oder **Entwürfe** für das gewünschte Zertifikat aus.
4. Öffnen Sie das Aktionsmenü (**...**) für das Zertifikat, und wählen Sie **Bearbeiten** aus.
   ![Zertifikat über das Aktionsmenü bearbeiten](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0001.png)
   *Option &quot;Bearbeiten&quot; im Dropdownmenü*

5. Nimm deine Änderungen vor.
6. Wählen Sie **Publish** oder **Als Entwurf speichern**.

## Klonen eines benutzerdefinierten Zertifikats

Verwenden Sie **Clone**, wenn Sie eine Kopie eines Zertifikats für einen neuen Namen oder einen ähnlichen Anwendungsfall benötigen. Benennen Sie das Zertifikat nach dem Klonen so um, dass es einen eindeutigen Namen hat. Andernfalls kann der Name mit der Quelle übereinstimmen, selbst wenn Sie das Design geändert haben.

>[!NOTE]
>
>Sie können keinen neuen Namen festlegen, während Sie direkt nach dem Klonen speichern. Benennen Sie das Zertifikat um, nachdem es als Entwurf gespeichert wurde oder nachdem es veröffentlicht wurde.

1. Wählen Sie im Abschnitt **Konfigurieren** die Option **Erfolge** aus. Die Seite **Abzeichen** wird geöffnet.
2. Wählen Sie im linken Navigationsbereich **Zertifikate**. Die Seite **Zertifikate** wird geöffnet.
3. Wählen Sie die Registerkarte **Veröffentlicht** oder **Entwürfe** für das gewünschte Zertifikat aus.
4. Öffnen Sie das Aktionsmenü (**...**) für das Zertifikat, und wählen Sie **Clone** aus.
   ![Zertifikat über das Aktionsmenü klonen](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0002.png)
   *Kopieroption im Dropdown-Menü*

5. Nimm deine Änderungen vor.

6. Wählen Sie **Publish** oder **Als Entwurf speichern**.

7. Benennen Sie das geklonte Zertifikat mit den Schritten in [Benutzerdefiniertes Zertifikat umbenennen](#rename-a-custom-certificate) um.

## Umbenennen eines benutzerdefinierten Zertifikats

Sie können ein Zertifikat umbenennen, ohne es zu klonen.

1. Wählen Sie im Abschnitt **Konfigurieren** die Option **Erfolge** aus. Die Seite **Abzeichen** wird geöffnet.
2. Wählen Sie im linken Navigationsbereich **Zertifikate**. Die Seite **Zertifikate** wird geöffnet.
3. Wählen Sie die Registerkarte **Veröffentlicht** oder **Entwürfe** für das gewünschte Zertifikat aus.

4. Öffnen Sie das Aktionsmenü (**...**) für das Zertifikat, und wählen Sie **Umbenennen** aus.
   ![Zertifikat über das Aktionsmenü umbenennen](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0003.png)
   Option *Umbenennen im Dropdown-Menü*

5. Geben Sie im Dialogfeld &quot;**Zertifikat umbenennen**&quot; den neuen Namen ein.
   ![Dialogfeld &quot;Zertifikat umbenennen&quot;](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0004.png)
   *Geben Sie einen neuen Namen ein*

6. Wählen Sie **Speichern**. Learning Manager zeigt eine Bestätigungsmeldung an.

## Benutzerdefiniertes Zertifikat löschen

Das Löschen eines Zertifikats kann nicht rückgängig gemacht werden. Fahren Sie nur fort, wenn Sie sicher sind.

>[!NOTE]
>
>Sie können kein Zertifikat löschen, das an ein Lernobjekt oder eine Instanz angehängt ist.

1. Wählen Sie im Abschnitt **Konfigurieren** die Option **Erfolge** aus. Die Seite **Abzeichen** wird geöffnet.
2. Wählen Sie im linken Navigationsbereich **Zertifikate**. Die Seite **Zertifikate** wird geöffnet.
3. Wählen Sie die Registerkarte **Veröffentlicht** oder **Entwürfe** für das gewünschte Zertifikat aus.
4. Öffnen Sie das Aktionsmenü (**...**) für das Zertifikat, und wählen Sie **Löschen** aus. Adobe Learning Manager zeigt eine Bestätigungsmeldung an.
   ![Zertifikat aus dem Aktionsmenü löschen](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0005.png)
   Option *Löschen im Dropdown-Menü*
   ![Zertifikatbestätigung löschen](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0006.png)
   *Bestätigungsmeldung*

5. Wählen Sie **Ja** aus. Wenn das Zertifikat nicht an ein Lernobjekt oder eine Instanz angehängt ist, schließt der Lern-Manager den Löschvorgang ab und zeigt möglicherweise eine weitere Bestätigung an.

## Benutzerdefiniertes Zertifikat als Standardzertifikat festlegen

Sie können ein Zertifikat als Standard für Folgendes festlegen:

- Schulungen
- Lernpfade
- Zertifizierungen
- Alle

![Standardzertifikatoptionen](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0007.png)
*Als Standardzertifikat festgelegt*

1. Wählen Sie im Abschnitt **Konfigurieren** die Option **Erfolge** aus. Die Seite **Abzeichen** wird geöffnet.
2. Wählen Sie im linken Navigationsbereich **Zertifikate**. Die Seite **Zertifikate** wird geöffnet.
3. Wählen Sie die Registerkarte **Veröffentlicht** oder **Entwürfe** für das gewünschte Zertifikat aus.
4. Öffnen Sie das Aktionsmenü (**...**) für das Zertifikat, wählen Sie **Als Standard festlegen** und wählen Sie dann eine der vier Optionen aus. Learning Manager zeigt eine Bestätigungsmeldung an.
5. Wählen Sie **Ja** aus. Learning Manager zeigt eine weitere Bestätigung an. Das Zertifikat zeigt eine **Standard für**-Beschriftung mit der von Ihnen ausgewählten Kategorie an (z. B. **Standard für Schulungen**).
   ![Standard für Kategoriebezeichnung auf Zertifikat](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0008.png)
   *Nachdem es zum Standardzertifikat wurde*

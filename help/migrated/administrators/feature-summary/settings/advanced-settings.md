---
description: Weitere Informationen zur Konfiguration erweiterter Einstellungen in Adobe Learning Manager
jcr-language: en_us
title: Erweiterte Einstellungen in Adobe Learning Manager
exl-id: 7047c89f-5f1c-4e0a-a908-20ef0eb9667d
source-git-commit: 0862e0d042fac74377b44c3387a72336ec625161
workflow-type: tm+mt
source-wordcount: '2357'
ht-degree: 1%

---

# Erweiterte Einstellungen in Adobe Learning Manager

## Katalogbeschriftungen

Katalogbeschriftungen in Adobe Learning Manager werden verwendet, um Lernobjekte (Kurse, Zertifizierungen, Lernpfade usw.) mit Tags zu versehen mit bestimmten Feldern und Werten. Diese Beschriftungen helfen Ihnen und Autoren dabei, Inhalte effektiv zu kategorisieren und zu organisieren, sodass Sie Inhalte besser filtern, verfolgen und Berichte erstellen können.

Weitere Informationen finden Sie unter [Katalogbeschriftungen in Adobe Learning Manager](/help/migrated/administrators/feature-summary/catalog-labels.md).


>[!NOTE]
>
>* Obligatorische Labels: Sie können festlegen, dass Katalogbeschriftungen für Autoren während der Kurserstellung obligatorisch sind.
>* Arbeitsablauf für Autoren: Autoren müssen beim Erstellen oder Bearbeiten von Kursen Compliance-Beschriftungen hinzufügen, um eine ordnungsgemäße Kategorisierung sicherzustellen.

## Inhaltsordner

Inhaltsordner in Adobe Learning Manager steuern, welche Autoren Inhalte in der Inhaltsbibliothek anzeigen und darauf zugreifen können. Mit hierarchischen Inhaltsordnern können Administratoren große Inhaltsbibliotheken in bis zu drei Ebenen verschachtelter privater Ordner organisieren, sodass Inhalte in Ihrer gesamten Organisation einfacher gefunden, verwaltet und wiederverwendet werden können.

### Was ist ein Inhaltsordner?

Ein Inhaltsordner ist ein Container, der zugehörige Inhalte gruppiert und bestimmt, wer darauf zugreifen kann. Jede Inhaltsdatei in Adobe Learning Manager gehört immer zu mindestens einem Ordner.

Es gibt zwei Arten von Inhaltsordnern:

**Öffentlicher Ordner** - standardmäßig in jedem Konto vorhanden. Der öffentliche Ordner verfügt über die folgenden Eigenschaften:

* Alle Autoren im Konto können auf Inhalte im öffentlichen Ordner zugreifen.
* Inhalte im öffentlichen Ordner dürfen sich nicht in einem privaten Ordner befinden. Das Gegenteil ist auch der Fall. Inhalte in einem privaten Ordner dürfen sich nicht im öffentlichen Ordner befinden.
* Der öffentliche Ordner ist nicht Teil der rollenbasierten Zugriffskonfiguration. Wenn Sie eine benutzerdefinierte Rolle auf bestimmte private Ordner beschränken, wird der Zugriff auf den öffentlichen Ordner nicht eingeschränkt.

**Private Ordner**- erstellt von Administratoren. Private Ordner unterstützen eine Hierarchie mit drei Ebenen. Ihr Zugriff wird durch die Rollenkonfiguration gesteuert.

**Hierarchieebenen für Ordner verstehen**

Ordner für private Inhalte unterstützen bis zu drei Verschachtelungsebenen:

* **Ordner der Ebene 1** - Ordner der obersten Ebene im Stammverzeichnis Ihrer Inhaltsbibliothek

* **Ordner der Ebene 2** - Unterordner, die in einem Ordner der Ebene 1 verschachtelt sind

* **Ordner der Ebene 3** - Unterordner, die in einem Ordner der Ebene 2 verschachtelt sind

Diese Struktur gibt Organisationen die Flexibilität, die Organisation realer Inhalte nach Themenbereich, Bereitstellungstyp, Zielgruppe oder Team zu spiegeln, anstatt Tausende von Dateien in einer flachen Liste zu verwalten.

Nur Administratoren können Ordner auf jeder Ebene erstellen, bearbeiten oder löschen. Autoren und benutzerdefinierte Benutzer interagieren mit der Hierarchie, können sie jedoch nicht ändern.

### Regeln für die Ordnerbenennung

Ordnernamen müssen auf derselben Ebene unter demselben übergeordneten Ordner eindeutig sein. Konkret:

| **Szenario** | **Zulässig?** |
|----------------------------------------------------------------------------------------------|--------------------------|
| Zwei Ordner der Ebene 1 mit demselben Namen | Nein |
| Zwei Ordner der Ebene 2 unter demselben Ordner der Ebene 1 mit demselben Namen | Nein |
| Zwei Ordner der Ebene 2 unter verschiedenen Ordnern der Ebene 1 mit demselben Namen | Ja |
| Ein Ordner der Ebene 2 und ein Ordner der Ebene 3 mit demselben Namen | Ja. Ebenen sind unterschiedlich |
| Ordner der Ebene 3 und anderer Ordner der Ebene 3 unter demselben Ordner der Ebene 2 mit demselben Namen | Nein |


### Ordnerpfade anzeigen

In der Inhaltsbibliothek wird der vollständige Ordnerpfad jeder Inhaltsdatei angezeigt. Beispiel: **Schulungsprogramme** > **Onboarding** > **SCORM-Assets**. Dieser Pfad zeigt den vollständigen Speicherort des Inhalts an.

Wenn sich eine Datei in mehreren Ordnern befindet, werden alle Pfade durch Kommas getrennt angezeigt. Wenn ein Pfad lang ist, wird er am Anfang durch Auslassungspunkte (...) abgeschnitten, und der Name des tiefsten Ordners wird immer angezeigt.

### Rollenbasierter Zugriff auf Ordner

Zugriff auf private Ordner wird nur auf **Ebene 1** zugewiesen. Wenn einer benutzerdefinierten Rolle Zugriff auf einen Ordner der Ebene 1 gewährt wird, wird dieser Zugriff automatisch auf alle Unterordner der Ebenen 2 und 3 innerhalb dieses Ordners übertragen. Es gibt keine Option, um den Zugriff auf der Ebene der Unterordner unabhängig zu gewähren.

In der folgenden Tabelle wird beschrieben, wie jede Rolle mit der Ordnerhierarchie umgehen kann.

| **Rolle** | **Was sie tun können** |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Administrator | Erstellen, Umbenennen und Löschen von privaten Ordnern der Stufen 1, 2 und 3 Ordnerzugriff auf Ebene 1 für benutzerdefinierte Rollen konfigurieren |
| Benutzerdefinierter Administrator | Verwalten Sie Ordner in zugänglichen Verzweigungen der Ebene 1 vorbehaltlich der ihnen zugewiesenen Berechtigungen |
| Autor | Ordner durchsuchen, Inhalt nach Ordnern filtern, Inhalt zu Ordnern hinzufügen, Inhalt zwischen Ordnern kopieren und verschieben, Inhalt beim Hinzufügen von Modulen zu einem Kurs auswählen |
| Benutzerdefinierter Autor | Wie der Autor, aber auf Ordner beschränkt, auf die über die zugewiesenen Berechtigungen der Ebene 1 zugegriffen werden kann |

### Beschränkungen für die Ordnerstruktur

| **Limit** | **Wert** |
|---------------------------------------|-----------|
| Ordner der Ebene 1 pro Konto | Kein Limit |
| Unterordner der Ebene 2 pro Ordner der Ebene 1 | 25 |
| Unterordner der Ebene 3 pro Ordner der Ebene 2 | 25 |
| Maximale Ordnertiefe | 3 Ebenen |


### Ordnerauswahlverhalten

Wenn Sie einen Ordner auswählen, z. B. beim Filtern oder Löschen, durchläuft die Auswahl die Hierarchie wie folgt:

* Wenn Sie einen Ordner der Ebene **Ebene 1** auswählen, werden automatisch alle Ordner der Ebene 2 und der Ebene 3 darunter ausgewählt.

* Wenn Sie einen Ordner der Ebene **Ebene 2** auswählen, werden automatisch alle Ordner der Ebene 3 darunter ausgewählt. Andere Ordner der Ebene 2 unter demselben Ordner der Ebene 1 sind nicht ausgewählt.

* Wenn Sie einen Ordner der Ebene **Ebene 3** auswählen, wird nur dieser Ordner ausgewählt. Es sind keine anderen Ordner ausgewählt.

>[!NOTE]
>
>Wenn Sie einen Unterordner auswählen, ohne den übergeordneten Ordner auszuwählen, zeigt der übergeordnete Ordner keine Anzeige für teilweise oder gemischte Auswahl an. Das ist absichtlich. Da ein übergeordneter Ordner selbst Inhalt enthalten kann, nicht nur Unterordner. Wenn Sie einen übergeordneten Ordner auswählen, bedeutet dies, dass Sie &quot;den gesamten Inhalt dieses Ordners und alle darunter liegenden Inhalte einschließen&quot; müssen. Ein teilweiser Indikator würde darauf hinweisen, dass der eigene Inhalt des übergeordneten Ordners teilweise enthalten ist, was irreführend wäre. Wenn Sie nur nach einem bestimmten Unterordner filtern möchten, wählen Sie diesen Unterordner direkt aus. Wenn der gesamte Inhalt in einem übergeordneten Ordner und seinen Unterordnern enthalten sein soll, wählen Sie den übergeordneten Ordner aus.

### Verwendung einer hierarchischen Ordnerstruktur

Hierarchische Inhaltsordner sind besonders nützlich, wenn Ihre Organisation viele Inhaltsdateien verwaltet und eine strukturierte Möglichkeit benötigt, um darin zu navigieren, wiederzuverwenden und den Zugriff darauf zu steuern.

Häufige Szenarien:

* **Große Inhaltsbibliotheken**: Bei Tausenden von Inhaltsdateien können Autoren in einer Hierarchie mit drei Ebenen direkt zu den benötigten Inhalten navigieren, anstatt durch eine flache Liste zu scrollen.

* **Mehrere Teams oder Projekte**: Ordner der Ebene 1 können Team- oder Projektbereiche trennen. Ordner der Ebene 2 können nach Bereitstellungstyp organisiert werden. Ordner der Ebene 3 können einzelne Elemente enthalten.

* **Rollenbasierte Inhaltstrennung**: Wenn verschiedene Autorenteams nur auf die Inhalte zugreifen sollten, die für ihre Arbeit relevant sind, hält die Zuweisung von Ordnerzugriff auf Ebene 1 die Inhalte jedes Teams privat.

### Anwendungsbeispiele für hierarchische Inhaltsordner

**Anwendungsfall 1 - Compliance-Schulung mit rechtsspezifischen Inhalten**

Ein globales Unternehmen führt in mehreren Regionen obligatorische Compliance-Schulungen durch. Jede Region umfasst Kernmodule, die für alle gelten, sowie juristische Addendums, die sich nach Ländern oder Regionen richten, wie Datenschutzbestimmungen, lokales Arbeitsrecht und Offenlegungspflichten.

Ohne hierarchische Ordner befinden sich alle Compliance-Assets in einer flachen Liste, was es für regionale Content-Teams schwierig macht, zu erkennen, welche Dateien zu welchem Programm oder welcher Gerichtsbarkeit gehören.

mit dreistufiger Struktur:

* Ebene 1: Compliance-Schulungen

* Ebene 2: EMEA/APAC/Nord- und Südamerika (ein Unterordner pro Region)

* Ebene 3: Spezifische Module oder Assets pro Region (PDF, lokale Richtlinien, Bewertungsdateien)

Regionale Autorenteams erhalten nur Zugriff auf ihre Zweigstelle der Stufe 1 oder 2. Sie können nur die Assets finden, aktualisieren und wiederverwenden, die für ihr jeweiliges Land relevant sind, ohne den Inhalt einer anderen Region sehen oder versehentlich ändern zu müssen.

**Anwendungsfall 2 - Onboarding-Programm im großen Maßstab mit vielen Rollen**

Eine Organisation führt jährlich Tausende von Mitarbeitern in verschiedenen Rollen ein: Einzel-Anbieter, Manager, Auftragnehmer und technische Spezialisten. Jede Rolle verfügt über eine eigene Onboarding-Spur mit freigegebenen grundlegenden Inhalten und rollenspezifischen Modulen.

mit dreistufiger Struktur:

* Ebene 1: Onboarding

* Ebene 2: Rolle (einzelner Anbieter/Manager/Auftragnehmer/Technischer Spezialist)

* Ebene 3: Modultyp (SCORM-Pakete / ILT-Decks / Aktivitätsleitfäden / Bewertungen)

Autoren, die Kurse für jede Rolle erstellen, navigieren direkt zu Ebene 2 und finden die genauen Dateien für diese Spur. Wenn ein Modul für mehrere Rollen wiederverwendet wird, z. B. ein Video zu Unternehmenswerten, kann es kopiert oder in mehrere Ordner verknüpft werden, ohne Duplikate zu erstellen. Der Inhalt bleibt als Einzelquelleninhalt erhalten, erscheint jedoch in allen relevanten Zweigen.

**Anwendungsfall 3 - Bibliothek für umfangreiche technische Kenntnisse mit mehreren Content-Teams**

Ein Technologieunternehmen unterhält eine interne Schulungsbibliothek mit Tausenden von Inhaltsdateien für Produktlinien, Cloud-Infrastruktur, Entwickler-Tools, Sicherheit und Data Engineering. Mehrere Autorenteams tragen Beiträge bei, von denen jedes für einen Produktbereich verantwortlich ist. Kursmodule können 40 bis 60 Dateien pro Kurs ausführen.

Ohne Hierarchie befinden sich alle tausend Dateien in einer Handvoll von Ordnern der obersten Ebene, und Autoren aus verschiedenen Teams wählen häufig die falsche Dateiversion aus oder überschreiben versehentlich freigegebene Assets.

mit dreistufiger Struktur:

* Ebene 1: Produktbereich (Cloud / Entwicklungs-Tools / Sicherheit / Data Engineering)

* Ebene 2: Kursname

* Ebene 3: Stockmedientyp (Videos/PDF/SCORM/Quizze)

Jedem Produktteam wird nur Zugriff auf seinen Ordner der Ebene 1 gewährt. Wenn Sie ein bestimmtes Quiz für einen bestimmten Kurs finden, müssen Sie zum richtigen Ordner der Stufe 3 navigieren, anstatt in Tausenden von Dateien zu suchen. Wenn das Sicherheitsteam ein SCORM-Paket aktualisiert, weiß es, dass es sich in Sicherheit > [Kursname] > SCORM befindet und nicht versehentlich in der Zweigstelle eines anderen Teams landen kann.

### Inhaltsordner als Administrator verwalten

Als Administrator in Adobe Learning Manager erstellen und verwalten Sie die Hierarchie der Inhaltsordner, steuern, welche benutzerdefinierten Rollen Zugriff auf bestimmte Ordner haben, und verwalten Ordnernamen und Löschungen. Autoren können Inhalte zu Ordnern hinzufügen und Inhalte innerhalb der Hierarchie organisieren, aber nur Administratoren können Ordner erstellen, umbenennen oder löschen.

#### Inhaltsordner erstellen

>[!NOTE]
>
>Zwei Ordner auf derselben Ebene unter demselben übergeordneten Element können keinen Namen gemeinsam nutzen. Der gleiche Name ist in verschiedenen Zweigen oder auf verschiedenen Ebenen zulässig.

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.
2. Wählen Sie in der linken Navigation **Konfigurieren** > **Einstellungen**.
3. Wählen Sie im Abschnitt **Erweitert** die Option **Inhaltsordner** aus.
4. Wählen Sie **Hinzufügen** in der oberen rechten Ecke der Seite aus. Das Dialogfeld &quot;**Neuen Ordner hinzufügen**&quot; wird geöffnet.
5. Geben Sie einen Namen und eine optionale Beschreibung für den Ordner ein.
6. Wählen Sie **Speichern**. Der Ordner wird erstellt und in der Ordnerliste angezeigt.


#### Unterordner erstellen

1. Suchen Sie auf der Seite **Inhaltsordner** den übergeordneten Ordner.
2. Wählen Sie die Option **Unterordner erstellen** neben dem Ordnernamen aus.
3. Geben Sie einen Namen und eine optionale Beschreibung für den Unterordner ein.
4. Wählen Sie **Speichern**. Der Unterordner wird in der Ordnerliste unter dem übergeordneten Ordner eingerückt angezeigt.

>[!NOTE]
>
>Jeder Ordner kann bis zu 25 direkte Unterordner enthalten. Ebene 3 ist die maximale Tiefe. Innerhalb eines Ordners der Ebene 3 können Sie keinen Unterordner erstellen.

#### Ordner umbenennen

1. Wählen Sie auf der Seite **Inhaltsordner** den Ordner aus, den Sie umbenennen möchten. Der Ordner wird im Bearbeitungsmodus geöffnet.
2. Aktualisieren Sie den Ordnernamen und, falls erforderlich, die Beschreibung.
3. Wählen Sie **Speichern**. Der Ordner wird unter dem neuen Namen gespeichert.

#### Ordner löschen

Beachten Sie vor dem Löschen die folgenden Regeln:

* Sie können einen leeren Ordner auf jeder beliebigen Ebene löschen.
* Sie können einen Ordner nicht löschen, wenn er Inhalte enthält, die nicht mit einem anderen Ordner verknüpft sind. Verschieben Sie diesen Inhalt zuerst in einen anderen Ordner.
* Wenn Sie einen übergeordneten Ordner löschen, werden alle Unterordner gelöscht. Wenn Sie einen übergeordneten Ordner auswählen, werden automatisch alle untergeordneten Ordner ausgewählt.

#### Übergeordneten Ordner löschen

1. Aktivieren Sie auf der Seite **Inhaltsordner** das Kontrollkästchen neben jedem Ordner, den Sie löschen möchten.
2. Wählen Sie **Aktionen** > **Ordner löschen** in der oberen rechten Ecke der Seite aus.
3. Bestätigen Sie den Löschvorgang, wenn Sie dazu aufgefordert werden. Alle Unterordner innerhalb der übergeordneten Ordner werden ebenfalls gelöscht.

#### Unterordner löschen

1. Aktivieren Sie auf der Seite **Inhaltsordner** das Kontrollkästchen neben dem Unterordner, den Sie löschen möchten.
2. Wählen Sie **Aktionen** > **Ordner löschen** in der oberen rechten Ecke der Seite aus.
3. Bestätigen Sie den Löschvorgang, wenn Sie dazu aufgefordert werden. Der Unterordner wird gelöscht.

>[!CAUTION]
>
>Das Löschen eines Ordners ist endgültig. Stellen Sie vor der Bestätigung sicher, dass alle Inhalte im Ordner an einen anderen Speicherort verschoben wurden.


#### Ordnerzugriff für benutzerdefinierte Rollen konfigurieren

Sie können benutzerdefinierte Rollen auf bestimmte Ordner der Ebene 1 beschränken, sodass benutzerdefinierte Administratoren und Autoren mit diesen Rollen nur die für sie relevanten Inhalte sehen.

Der Zugriff wird nur auf Ordnerebene **Ebene 1 festgelegt**. Wenn Sie einem Ordner der Ebene 1 eine benutzerdefinierte Rolle zuweisen, erhält diese Rolle automatisch Zugriff auf alle Unterordner der Ebenen 2 und 3, die sich darin befinden. Sie können den Zugriff nicht unabhängig auf Unterordnerebene zuweisen.

1. Wählen Sie in der linken Navigation **Benutzer** > **Benutzerdefinierte Rollen**.
2. Öffnen Sie die benutzerdefinierte Rolle, die Sie konfigurieren möchten, oder erstellen Sie eine neue.
3. Suchen Sie unter **Kontoberechtigungen** den Abschnitt **Inhaltsordner**.
4. Wählen Sie **Ausgewählte Ordner** aus.
5. Wählen Sie die Ordner der Ebene 1 aus, auf die diese Rolle Zugriff haben soll.
6. Klicken Sie auf **OK**.

Benutzer mit dieser Rolle sehen nur den Inhalt in den ausgewählten Ordnern der Ebene 1 und ihren Unterordnern. Auf Inhalte in anderen privaten Ordnern und im öffentlichen Ordner kann nicht zugegriffen werden.

#### Best Practices

Die folgenden Vorgehensweisen helfen Ihnen beim Erstellen einer Ordnerstruktur, die sich gut skalieren lässt und leicht navigieren lässt.

1. **Planen Sie Ihre Struktur, bevor Sie Ordner erstellen.** Wenn Content in einer Hierarchie organisiert ist, erfordert die Umstrukturierung das Verschieben großer Inhaltsmengen. Entscheiden Sie sich bereits vor Beginn für Ihre Kategorie 1, z. B. Produktlinien, Abteilungen oder Schulungsprogramme.

2. **Verwenden Sie drei Ebenen für sinnvolle Gruppierungen.** Ein gängiges Muster ist: Stufe 1 für eine breite Domäne oder ein breites Programm, Stufe 2 für den Bereitstellungstyp oder das Team, Stufe 3 für einzelne Assets. Beispiel:

   * Ebene 1: Vertriebsschulung

   * Ebene 2: Module zum Selbststudium

   * Ebene 3: PDF von Elementen

3. **Halten Sie Namen kurz, aussagekräftig und eindeutig in der übergeordneten Organisation.** Vermeiden Sie generische Namen wie &quot;Modul 1&quot; oder &quot;Inhalt&quot;. Verwenden Sie Bezeichner, die für die Autoren, die die Bibliothek durchsuchen, sinnvoll sind.

4. **Nur auf Ebene 1 benutzerdefinierten Rollenzugriff zuweisen.** Da der Zugriff automatisch kaskadiert wird, ist die Zuweisung auf Stufe 1 ausreichend und erleichtert die Zugriffsverwaltung. Sie müssen den Zugriff nicht aktualisieren, wenn Sie Unterordner der Ebenen 2 oder 3 hinzufügen.

5. **Verschieben Sie Inhalt vor dem Löschen von Ordnern.** Wenn ein Ordner Inhalte enthält, die nirgendwo anders verknüpft sind, wird das Löschen blockiert. Gewöhne dir an, Ordnerinhalte vor dem Löschen zu überprüfen.


<!--

**Key points:**

A folder is a repository of content, which is a subset of the entire content library available in an account with the following properties:

* Only you (administrator) can create, edit, or delete a folder.
* You can control access to folders as part of defining roles only for custom administrators.
* Content must at all times be associated with at least one folder. To start with, all content will be associated with the public folder, which can later be changed.
* Content can be associated with multiple folders at the time of creation, which will also be possible by a copy operation
* All folder names must be unique within the account, otherwise there will be an error in naming a folder.

Folders only control visibility of content and don't create copies of content. Therefore, editing content will reflect in all the associated folders.

**Public folder**

A public folder is always present in an account and initially, all content will be part of this folder. Later, authors can move content out of this folder into other folders. A public folder has the following properties:

* All content associated with this folder will be accessible to all types of authors, by default.
* Any content that is a part of a public folder, cannot be part of any other folder. The converse also holds true.

This folder cannot be part of configurable role definition. Consequently, not having a public folder in configurable role definition doesn't restrict access to a public folder.

**Private folder**

Any folder created by you is a private folder.

**Add a content folder**

To add a content folder, follow the steps:

1. Select **[!UICONTROL Settings]** > **[!UICONTROL Content Folder]**.
2. Select **[!UICONTROL Add]** to create a new folder.
3. Type the name and description of the folder to be created.
 
    ![alt text](assets/advanced-settings-picture1.png)

4. Select **[!UICONTROL Save]** to create the folder.

**Folder operations**

* **[!UICONTROL Add a folder]**: To add a folder, select the folder, and then select **[!UICONTROL Add]** on the upper-right corner of the screen.
* **[!UICONTROL Delete a folder]**: To delete a folder, select the folder to delete, select the **[!UICONTROL Actions]** menu, and then select **[!UICONTROL Delete Folder]**.
-->

## Standorte für Klassenzimmer

Erstellen und verwalten Sie eine Bibliothek mit physischen oder virtuellen Schulungsräumen. Diese Standorte können von Autoren und Administratoren verwendet werden, um ILT-Veranstaltungen (Instructor-Led Training = Schulungen mit Kursleiter) einzurichten. Die Funktion stellt sicher, dass die Details zum Schulungsraum, wie z. B. Sitzbeschränkungen und Standortinformationen, vorkonfiguriert und leicht zugänglich sind.

Weitere Informationen finden Sie unter [Klassenzimmerspeicherorte in Adobe Learning Manager hinzufügen](/help/migrated/administrators/feature-summary/classroom.md).

## Berichte

In diesem Abschnitt können Sie die Kompatibilitäts- und Gruppenerfolg-Dashboards konfigurieren.

![Alternativtext](assets/advanced-settings-picture2.png)

Weitere Informationen finden Sie unter:

* [Kompatibilitäts-Dashboard](/help/migrated/administrators/feature-summary/reports.md#compliance-dashboard)
* [Dashboard für den Gruppenerfolg](/help/migrated/administrators/feature-summary/group-success-dashboard.md)

---
description: Laden Sie vorhandene Dokumente, Richtlinien oder Decks hoch, um die KI in den Inhalten Ihres Unternehmens zu erden. Entscheidet, ob die Generierung nur auf diese Dateien beschränkt werden soll, oder lässt die KI ihre allgemeinen Kenntnisse um zusätzliche Informationen ergänzen.
jcr-language: en_us
title: Verwalten von Quelldateien
source-git-commit: 9ef7ede817f226004430b4104ff78a2ebc45aec2
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---


# Verwalten von Quelldateien

Mit **Quellen verwalten** können Sie steuern, welche Inhalte der Inhaltssetzer zum Generieren Ihres Kurses verwendet. Fügen Sie einem Kurs Ihre eigenen Dokumente hinzu und wählen Sie aus, ob Sie die KI auf nur diesen Inhalt beschränken möchten oder ob Sie Ihr Material durch KI ergänzen möchten. Wenn Sie keine Dokumente hinzufügen, generiert Content Composer den Kurs anhand der vorhandenen Kenntnisse des KI-Modells.

## Generieren von Kursen mithilfe von Quellmaterial

1. Wählen Sie **Quellen verwalten** oder **Dateien hinzufügen** im Chatfenster oder in der Symbolleiste aus.
   ![](../assets/5_brief_manage_sources_prompt_updated.png)

2. Ziehen Sie eine Datei in das Dialogfeld oder wählen Sie **+ Quelldateien hinzufügen** aus, um nach Dateien zu suchen. Sie können mehrere Quelldateien hinzufügen.
   ![](../assets/6_manage_sources_no_files_added_updated.png)

3. Wählen Sie **Ausgabe auf Inhalt in Dateien beschränken**. Auf diese Weise kann Content Composer nur Quellinhalte zum Generieren des Kurses verwenden. Wenn diese Option nicht aktiviert ist, verwendet der Inhalts-Composer auch das Web, um einen Kurs zu erstellen.
   ![](../assets/7_manage_sources_file_uploading_restrict_output_updated.png)

Unterstützte Formate:

| **Format** | **Maximale Größe** |
|-------------------------|--------------|
| PDF | 100 MB |
| Markdown (.md) | 100 MB |
| PowerPoint (.ppt/.pptx) | 100 MB |
| MS Word (.doc/.docx) | 100 MB |
| Textdatei (.txt) | 100 MB |

Wählen Sie **Weiter**, um die Kursgliederung zu generieren.

### Generieren ohne Quellmaterial

Führen Sie die folgenden Schritte aus, um die Kursgliederung zu generieren, wenn Sie keine Quelldatei als Referenzdokument haben.

1. Wählen Sie **Quellen verwalten**. Das Dialogfeld &quot;**Quellen verwalten**&quot; wird geöffnet.

2. Wählen Sie **Ich habe kein Quellmaterial. Generieren Sie den Kurs ohne Quelldateien**, damit die AI Inhalte aus ihren allgemeinen Kenntnissen generieren kann. Wenn diese Option nicht ausgewählt ist und Dateien hochgeladen werden, beschränkt AI generierte Inhalte auf die hochgeladenen Dokumente.![](../assets/8_manage_sources_no_source_material_option_updated.png)

3. Wählen Sie **Weiter**, um die Kursgliederung zu generieren.

### Aktualisieren eines Kurses, wenn sich das Quellmaterial ändert

Quelldokumente können veraltet sein, nachdem ein Kurs bereits generiert wurde - eine Richtlinie wird überarbeitet, ein SOP erhält eine neue Version oder ein Pitch Deck wird aktualisiert. Verwenden Sie diesen Arbeitsablauf, um den Kurs wieder an das aktuelle Material anzupassen.

1. Wählen Sie im Chat-Bereich oder in der Symbolleiste **Quellen verwalten** aus, um das Dialogfeld erneut zu öffnen.

2. Fügen Sie die neuen oder überarbeiteten Dateien mit **+ Quelldateien hinzufügen** hinzu.

3. Entfernen oder ersetzen Sie alle veralteten Dateien, damit die Quellliste nur das aktuelle Material widerspiegelt.

4. Wählen Sie Weiter , um die aktualisierte Quellliste zu speichern.

5. Regenerieren Sie die betroffenen Lektionen im Inhaltskomposer, überprüfen Sie die Änderungen und veröffentlichen Sie den Kurs erneut. Beim erneuten Veröffentlichen wird das Update als neue Modulversion an Adobe Learning Manager gesendet - siehe Modulversionierung in ALM.

### Dateiupload bestätigen

![](../assets/9_manage_sources_file_ingested_confirmation_updated.png)

Sobald eine Datei angehängt wurde, zeigt das Dateisymbol auf der Symbolleiste eine Abzeichen-Anzahl an. Der Assistent bestätigt den Upload und bietet eine Verknüpfung **Gliederung generieren** an. Wählen Sie sie aus, oder wählen Sie **Gliederung generieren** in der oberen Symbolleiste aus.

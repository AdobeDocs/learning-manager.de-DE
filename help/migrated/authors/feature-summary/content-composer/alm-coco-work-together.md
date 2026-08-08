---
description: Erfahren Sie, wie Content Composer und Adobe Learning Manager die Verantwortung für die Erstellung und Bereitstellung von Inhalten teilen, wie ein fertiger Kurs vom Content Composer in die ALM-Inhaltsbibliothek verschoben wird und wie die Verfolgung und Berichterstellung von Teilnehmern nach der Veröffentlichung funktioniert.
jcr-language: en_us
title: Wie Content Composer und Adobe Learning Manager zusammenarbeiten
source-git-commit: 5a0f12b1ed0e5ae1bde7afbd539d70078d99f05d
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---


# Wie Adobe Learning Manager Content Composer und Adobe Learning Manager zusammenarbeiten.

Content Composer übernimmt die Inhaltserstellung. Adobe Learning Manager übernimmt Bereitstellung, Registrierung, Nachverfolgung und Reporting. Die Verbindung der beiden Produkte erfolgt in einem Schritt der Veröffentlichung. Sobald Sie Inhalte aus dem Inhaltssetzer veröffentlichen, wird der Kurs zu einem Modul in der ALM-Inhaltsbibliothek, wo er zu einem Kurs zusammengestellt und den Teilnehmern zugewiesen werden kann.

## Welche Inhaltsentwickler-Steuerelemente

- Lektion und Themenstruktur

- Kursinhalte - Text, Bilder, Videos, Komponenten und Wissensüberprüfungen

- Quizze am Ende der Lektion, einschließlich Fragentypen und Antwortoptionen

- Visuelles Design

- Abschlusskriterien und Erfolgskriterien

- SCORM-Version für Berichterstellung verwendet

## Was Adobe Learning Manager steuert

- Teilnehmerregistrierung und Zugriff

- Modulmetadaten - Dauer, Tags, eindeutige IDs, Ablauf

- Kursaufbau - Kombinieren von Inhaltsausgabe-Modulen mit anderen Lerninhalten

- Tracking, Berichterstattung und Transkripte für Teilnehmer

- Kursversionierung

- Benachrichtigungen und Erinnerungen

## Von der Kurserstellung bis zum Abschluss

1. **Erstellen Sie den Kurs in Content Composer**: Erstellen Sie Ihren Kurs in Content Composer, einschließlich Lektionen, Themen, Themen, Tests und Abschlusseinstellungen. Konfigurieren Sie die Kurseinstellungen - Abschlusskriterien, Erfolgskriterien und Quizpunktzahl - vor der Veröffentlichung.
Weitere Informationen finden Sie unter [Kurseinstellungen konfigurieren](#settings).

2. **Publish zu Adobe Learning Manager:** Verbinden Sie Content Composer nach Abschluss der Erstellung über die **Exporteinstellungen** mit Ihrem ALM-Konto, und veröffentlichen Sie den Kurs. Content Composer sendet den Kurs als SCORM-kompatibles Modul an die ALM-Inhaltsbibliothek.
   ![Ein veröffentlichter Kurs mit einer benutzerdefinierten Kopfzeile, einem Logo und einem angewendeten Schriftdesign](../assets/49_published_course_custom_branding_header_updated.png)

3. **Konfigurieren Sie das Modul in ALM:**. Nach der Veröffentlichung wird der Kurs als Modul in der ALM-Inhaltsbibliothek angezeigt. Ein ALM-Autor konfiguriert Modulmetadaten - einschließlich Dauer, Tags, eindeutigen IDs und Ablaufeinstellungen - und fügt das Modul zusammen mit anderen Lerninhalten einem ALM-Kurs hinzu.
   ![Felder für Modulmetadaten und Abschlusskriterien](../assets/50_alm_add_content_composer_module_metadata_updated.png)

>[!NOTE]
>
>Wenn Sie Abschluss- und Erfolgskriterien in Adobe Learning Manager (ALM) festlegen, haben diese Einstellungen Vorrang vor den in Content Composer definierten.

4.**Publish des ALM-Kurses:** Ein ALM-Autor fügt das Modul zu einem ALM-Kurs zusammen, fügt Kursbilder und -einstellungen hinzu und veröffentlicht ihn. Erst nach diesem Schritt können Teilnehmer registriert werden.

Weitere Informationen finden Sie unter [Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/get-started/getting-started-author).
![ Die Inhaltsbibliothek in Adobe Learning Manager, die veröffentlichte Module und Verarbeitungsmodule anzeigt](../assets/51_alm_content_library_list_view_updated.png)

Weitere Informationen finden Sie unter [Kurserstellung als Autor auf ALM](https://experienceleague.adobe.com/en/docs/learning-manager/using/authors/courses).

5.**Die Teilnehmer schließen den Kurs ab:** Teilnehmer greifen über Adobe Learning Manager auf den Kurs zu, starten das Inhaltserstellungsmodul, absolvieren Lektionen und Tests und erhalten Punktzahlen basierend auf den Abschluss- und Erfolgskriterien, die Sie in Schritt 1 konfiguriert haben.

Weitere Informationen finden Sie unter [Zugriff auf den Kurs als Teilnehmer](https://experienceleague.adobe.com/en/docs/learning-manager/using/get-started/getting-started-learner).

&#x200B;6. ALM zeichnet den Teilnehmerfortschritt auf: Abschlussstatus, Quizergebnisse und Teilnehmerdaten werden in ALM aufgezeichnet und über Teilnehmertranskripte und administrative Berichte zur Verfügung gestellt.

7.**Kurs mit Versionierung aktualisieren**: Wenn Sie Inhalte in Content Composer aktualisieren und erneut veröffentlichen, erstellt ALM eine neue Version des Moduls. ALM-Autoren können vorhandene Kurse aktualisieren, um die neueste Version zu verwenden.

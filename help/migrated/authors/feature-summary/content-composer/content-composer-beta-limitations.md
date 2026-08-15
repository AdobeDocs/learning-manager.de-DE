---
description: Überprüfen Sie die Beta-Einschränkungen von Content Composer - reine Dialogbearbeitung, MCQ-/True-False-Tests, feste Konturen - mit Umgehungslösungen für jede dieser Einschränkungen.
jcr-language: en_us
title: Beta-Einschränkungen für Content Composer
source-git-commit: 68d15fa96588b2569c9b1cdb480e2ba9f31a1cf6
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---


# Beta-Einschränkungen für Adobe Learning Manager Content Composer

Eine vollständige Liste der aktuellen Beta-Einschränkungen für Content Composer mit Beschreibungen und Problemumgehungen, sofern verfügbar.

## Aktuelle Einschränkungen

Die folgende Tabelle zeigt alle bekannten Einschränkungen in der aktuellen Beta-Version.

| **Einschränkung** | **Beschreibung** | **Problemumgehung** |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Die Gliederungsbearbeitung ist nur konversativ** | Sie können auf der Arbeitsfläche keine Lektion oder kein Thema auswählen, um sie umzubenennen, neu anzuordnen oder zu löschen. Alle Änderungen an der Gliederung müssen über das Assistant-Chat-Fenster vorgenommen werden. | Fragen Sie die Assistenzkraft: &quot;Benennen Sie Lektion 2 in &#39;Kennworthygiene&#39; um&quot; oder &quot;Verschieben Sie Thema 1.3 in Lektion 2&quot;. |
| **Die Gliederungshierarchie ist behoben** | Die Kursstruktur wurde als &quot;Lektionen&quot; > &quot;Themen&quot; festgelegt. Sie können keine Unterthemen, zusätzlichen Hierarchieebenen oder benutzerdefinierten Strukturen erstellen. | Verwenden Sie die verfügbaren Komponenten, um innerhalb eines Themas Tiefe hinzuzufügen. |
| **Die Kontur kann nach der Kurserstellung nicht direkt bearbeitet werden** | Sobald ein Kurs generiert wurde, bleiben Themennamen und Lektionsnamen Teil der Gliederungsstruktur. Sie müssen zu Unterhaltungen auf Gliederungsebene zurückkehren, um sie zu ändern. Sie können sie nicht umbenennen, indem Sie eine Überschrift im Kurseditor auswählen. | Fragen Sie den Assistenten im Kurseditor: &quot;Benennen Sie Lektion 3 in &#39;Problembehandlung&#39; um.&quot; |
| **Bewertungstypen: Nur MCQ und True/False** | Die aktuelle Beta-Version unterstützt nur Multiple-Choice-Fragen (**MCQ**) und True-/False-Fragen. Andere Bewertungsarten sind nicht verfügbar. | - |
| **Fragenbanken sind nicht verfügbar** | Sie können keine Bank mit zuvor erstellten Fragen importieren oder verwalten. | Zusätzliche Fragen im Gespräch erstellen: &quot;Fügen Sie dem Quiz für Lektion 1 zwei weitere Fragen hinzu.&quot; |
| **Wissensüberprüfungen werden nicht bewertet** | In Lektionen eingebettete Wissensüberprüfungen werden nicht bewertet. Nur Quizbewertungen am Ende des Unterrichts werden bewertet und aufgezeichnet. | Verwenden Sie Quizze (keine Wissensüberprüfungen) für alle Bewertungen, die einen Abschluss- oder Punktedatensatz erstellen müssen. |
| **Konversationale Aktionen auf unterstützte Funktionen beschränkt** | Der Assistent kann frei diskutieren und Brainstorming durchführen, tatsächliche Kursänderungen sind jedoch auf vom Produkt unterstützte Funktionen beschränkt. Anforderungen zum Generieren nicht unterstützter Inhaltsstrukturen oder Formate sind möglicherweise nicht erfolgreich. | Wenn eine Anfrage nicht funktioniert, bitten Sie die Assistenzkraft zu erklären, was sie stattdessen tun kann. |
| **Generierung mit Dokumenteneinschränkung** | Wenn **Ausgabe auf Inhalt in Dateien beschränken** aktiviert ist, generiert Content Composer nur Inhalte aus den hochgeladenen Quelldokumenten. Es werden keine Informationen eingeführt, die über diese Quellen hinausgehen. | Deaktivieren Sie den Schalter, damit die KI allgemeine Kenntnisse ergänzen kann. |
| **Features für die Zusammenarbeit werden weiterentwickelt** | &quot;Für Review und Kommentieren freigeben&quot; und &quot;Für Teilnehmer freigeben&quot; befinden sich beide in der aktiven Entwicklung. Die Einzelheiten der Implementierung können sich vor der allgemeinen Verfügbarkeit ändern. | Verwenden Sie **Link kopieren**, um einen Vorschaulink für die informelle Überprüfung freizugeben. Koordinieren Sie bei der gemeinsamen Bearbeitung die Wendungen mit den Mitarbeitern. Gleichzeitiges Co-Editing wird nicht unterstützt. |
| **Der produktinterne Assistent ist kein Produkthilfe-System**. | Der Conversational Assistant ist für Kursbearbeitungsaufgaben wie das Generieren und Ändern von Inhalten konzipiert. Antworten auf Fragen zur Produktnutzung können unzuverlässig sein, da dieses Verhalten noch nicht explizit entwickelt wurde. | Verwenden Sie bei Fragen zur Vorgehensweise die vorhandene Hilfedokumentation, anstatt den produktinternen Assistenten zu fragen. |

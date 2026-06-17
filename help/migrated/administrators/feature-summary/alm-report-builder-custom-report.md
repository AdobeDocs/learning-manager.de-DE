---
jcr-language: en_us
title: Erstellen eines benutzerdefinierten Berichts im Report Builder
description: Erstellen Sie einen vollständig benutzerdefinierten Bericht in Adobe Learning Manager Report Builder, indem Sie Ihre eigenen Spalten, Filter, Einstellungen für Gruppen und eine leere Arbeitsfläche auswählen.
contentowner: mmanuel
source-git-commit: b4540c4c23ad496c8fff01095be6715d18aa0512
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 2%

---


# Erstellen eines benutzerdefinierten Berichts im Report Builder

Das Erstellen von Grund auf neu funktioniert am besten, wenn Sie ein klares Bild der erforderlichen Spalten und Ausgaben haben und keine vorhandene Vorlage Ihrem Anwendungsfall entspricht. Wenn du zum ersten Mal mit Report Builder arbeitest, kannst du auch mit einer Vorlage beginnen.

In diesem Beispiel identifizieren Sie die Teilnehmer unter jedem Manager, die für Compliance-Kurse gefährdet sind.

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.
2. Wählen Sie **Berichte** und anschließend **Report Builder** aus.
3. Wählen Sie die Registerkarte **Berichte** aus, und wählen Sie dann **Bericht erstellen** aus.
4. Geben Sie einen Namen für den Bericht ein. Ein Name ist erforderlich. Optional können Sie eine Beschreibung eingeben.
   ![](assets/image011.png)
5. Wählen Sie im Spaltenfenster die folgenden Datasets aus und erweitern Sie sie:
a. Benutzer
b. Lernobjekt
c. Benutzerkonformitätsstatus
6. Wählen Sie **+** neben den folgenden Spalten aus, die Sie einschließen möchten. Ausgewählte Spalten werden auf der Berichtsarbeitsfläche angezeigt.
a. Benutzer\Name
b. Benutzer-\Managername
c. Lernobjekt-/Lernobjektname
d. Benutzerkonformitätsstatus/Abschluss %
e. Benutzerkonformitätsstatus/Konformität %
!   2[](assets/image012.png)
7. Ordnen Sie Spalten neu an, indem Sie sie auf die Arbeitsfläche ziehen.
8. Um eine Spalte umzubenennen, geben Sie einen Namen in das Aliasfeld der Spalte ein. Der Alias wird als Spaltenüberschrift in der heruntergeladenen Datei angezeigt.
9. Wählen Sie **Bericht speichern**.

## Bericht herunterladen

1. Wählen Sie in der oberen rechten Ecke **Aktionen** aus.
   ![](assets/image013.png)
2. Wählen Sie Herunterladen. Sie können den Bericht über das Benachrichtigungssymbol herunterladen, wenn er fertig ist.

Der heruntergeladene Bericht in der CSV-Dateierweiterung enthält die folgenden Spalten:

1. name
2. managerName
3. name
4. completePct
5. compliancePct

## Anwenden von Gruppe nach, Filtern und Sortieren

### Filter

Nachdem Sie den Bericht heruntergeladen haben, wenden Sie einen Filter an, bei dem &quot;completePct OR compliancePct&quot; den Wert 100 hat.

1. Öffnen Sie den Bericht, und wählen Sie in der oberen rechten Ecke **Bearbeiten** aus.
2. Wählen Sie &quot;**Filter hinzufügen**&quot; aus und suchen Sie die Spalten, in denen Sie die Filter anwenden möchten.
   ![](assets/image014.png)
3. Wählen Sie **Hinzufügen** aus.
4. Kombinieren der Filter mit der UND/ODER-Logik; den Operator zwischen den Filterzeilen umschalten.
   ![](assets/image015.png)
5. Wählen Sie **Bericht speichern**, und laden Sie den Bericht herunter.

Der heruntergeladene Bericht enthält Datensätze, bei denen &quot;completePct OR compliancePct&quot; den Wert 100 hat.

### Gruppieren nach

Datensätze nach Manager gruppieren in:

* Aggregieren von Teilnehmerdaten nach Manager
* Durchschnittswerte auf Managerebene berechnen
* Anzahl der Teilnehmer unter jedem Manager

1. Öffnen Sie den Bericht, und wählen Sie in der oberen rechten Ecke **Bearbeiten** aus.
2. Wählen Sie **Gruppe nach:Select** und anschließend die Spalte **Name des Benutzer-Managers** aus.
   ![](assets/image016.png)
3. Aggregieren Sie die folgenden Spalten:
a. Benutzer\Name
b. Lernobjekt-/Lernobjektname
4. Wählen Sie **Count** als Aggregatfunktion für die Spalten aus.
   ![](assets/image017.png)
5. Wiederholen Sie diesen Vorgang für Lernobjekt-/Lernobjektname.
   ![](assets/image018.png)
6. Wählen Sie **Bericht speichern**, und laden Sie den Bericht herunter.

Der heruntergeladene Bericht enthält eine verwaltungsmäßige Zusammenfassung der Leistung der Teilnehmerschulung. Es zeigt die durchschnittliche Abschlussrate, die durchschnittliche Compliance-Punktzahl und die Gesamtzahl der Teilnehmer für jeden Manager an. Die Daten weisen auf einen universellen Schulungsabschluss in allen Gruppen hin, während die Compliance-Leistung zwischen den Managern erheblich variiert.

### Sortieren

Sortieren Sie den Bericht in absteigender Reihenfolge nach der Anzahl der Teilnehmer für jeden Manager.

1. Öffnen Sie den Bericht, und wählen Sie in der oberen rechten Ecke **Bearbeiten** aus.
2. Wählen Sie **Sortierung hinzufügen**.
3. Suchen Sie nach dem Benutzernamen und wählen Sie **Benutzer\Name**.
4. Wählen Sie **Absteigend**.
   ![](assets/image019.png)
5. Wählen Sie **Hinzufügen** aus.
6. Wählen Sie **Bericht speichern**, und laden Sie den Bericht herunter.

Der heruntergeladene Bericht enthält die Anzahl der Teilnehmer pro Manager in absteigender Reihenfolge.

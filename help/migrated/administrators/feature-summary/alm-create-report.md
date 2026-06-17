---
jcr-language: en_us
title: Erste Schritte mit einer Report Builder-Vorlage
description: Erstellen Sie schnell einen Bericht in Adobe Learning Manager Report Builder, indem Sie mit einer vordefinierten Vorlage für gängige Anwendungsfälle beginnen.
contentowner: mmanuel
source-git-commit: b4540c4c23ad496c8fff01095be6715d18aa0512
workflow-type: tm+mt
source-wordcount: '818'
ht-degree: 1%

---


# Erste Schritte mit einer Report Builder-Vorlage

Vorlagen sind gebrauchsfertige Berichtskonfigurationen, die von Adobe Learning Manager bereitgestellt werden. Jede Vorlage ist für einen bestimmten Anwendungsfall konzipiert, z. B. Registrierung und Abschlussverfolgung, Compliance-Berichte oder die Leistung von Kursleitern. Sie können eine Vorlage direkt herunterladen oder duplizieren, um eine bearbeitbare Kopie zu erstellen.

1. Melden Sie sich bei Adobe Learning Manager als Administrator an.
2. Wählen Sie im linken Fensterbereich **Berichte** und anschließend **Report Builder** aus.
3. Wählen Sie die Registerkarte **Vorlagen** aus.
4. Durchsuchen Sie die verfügbaren Vorlagen. Jede Vorlage wird nach ihrem Anwendungsfall benannt.
   ![](assets/image007.png)
5. Wählen Sie einen Vorlagennamen aus, um die schreibgeschützte Vorschau zu öffnen. Wählen Sie in diesem Beispiel neben der Vorlage &quot;Catalog Wise - Course Count MoM&quot; die Option Duplicate (Duplizieren). Überprüfen Sie die Spalten, angewendeten Filter und die Sortierreihenfolge. Wenn Sie eine Vorlage duplizieren, öffnet der Report Builder eine bearbeitbare Kopie mit der bereits vorhandenen Vorlagenkonfiguration. Der Name, die Beschreibung, die Spalten, die Filter und die Sortierung des Berichts können vor dem Speichern bearbeitet werden.

## Benennen und Beschreiben des Berichts

1. Ersetzen Sie im Feld **Name** den Standardnamen (z. B. _Kopie von Catalog Wise_ - _Kursanzahl MoM_) durch einen eindeutigen Namen für Ihren Bericht. Ein Name ist erforderlich.
2. Geben Sie im Feld **Beschreibung** eine kurze Zusammenfassung des Inhalts des Berichts ein. Dies hilft anderen Administratoren, den Zweck des Berichts beim Anzeigen oder Bearbeiten zu verstehen.

## Spalten hinzufügen und konfigurieren

Der Abschnitt **Spalten** verfügt über zwei Bereiche: **Spalten** links auswählen und **Ausgewählte Spalten** rechts auswählen.

### Hinzufügen einer Spalte

1. Erweitern Sie im Bereich **Spalten** auswählen ein Dataset, indem Sie seinen Namen auswählen. Beispiel: **Katalog** oder **Gruppe aktiver Feldbenutzer**.
2. Wählen Sie das Symbol **+** neben der Spalte aus, die Sie hinzufügen möchten. Die Spalte wird im Bereich **Ausgewählte Spalten** auf der rechten Seite angezeigt.
   ![](assets/image009.png)
3. Um dieselbe Spalte mehrmals hinzuzufügen. Sie können beispielsweise zwei verschiedene Aggregate auf ein und dasselbe Feld anwenden. Wählen Sie **+** erneut für diese Spalte aus.

### Neuordnen von Spalten

Ziehen Sie den Griff links neben einer beliebigen Spaltenzeile im Bedienfeld &quot;**Ausgewählte Spalten**&quot;, um sie an eine andere Position zu verschieben. Die Spaltenreihenfolge im Bereich stimmt mit der im heruntergeladenen Bericht überein.

### Umbenennen einer Spalte

1. Wählen Sie das Symbol **Bearbeiten** (Bleistift) in einer Spaltenzeile aus.
   ![](assets/image011.png)
2. Geben Sie einen Alias ein. Der Alias wird im heruntergeladenen Bericht als Spaltenüberschrift anstelle des Standardfeldnamens angezeigt.
   ![](assets/image013.png)

### Entfernen einer Spalte

Wählen Sie das Symbol **×** in einer Spaltenzeile aus, um sie aus dem Bericht zu entfernen.

## Gruppe anwenden nach

Das Steuerelement **Gruppe nach** wird oben im Bereich **Ausgewählte Spalten** angezeigt.

1. Wählen Sie **Gruppieren nach: Wählen Sie** aus.
   ![](assets/image015.png)
2. Wählen Sie die Spalten aus, nach denen gruppiert werden soll. Sie können mehrere auswählen. Im Screenshot ist der Bericht nach _Katalog_ und _Erstellungsmonat_ gruppiert.
3. Jede ausgewählte Spalte in Gruppen wird als Tag unter dem Steuerelement Gruppieren nach angezeigt. Um eine Gruppe nach Spalte zu entfernen, wählen Sie im Tag **×** aus.

>[!NOTE]
>
>Wenn group by angewendet wird, muss auf jede Spalte, die keine group by -Spalte ist, eine Aggregatfunktion angewendet werden. Eine Spalte ohne Aggregat verursacht einen Fehler.

## Anwenden von Aggregaten auf Spalten

1. Wählen Sie in einer beliebigen Spalte, die nicht gruppiert ist, im Bereich **Ausgewählte Spalten** die Option **Aggregieren nach** aus.
2. Wählen Sie eine Funktion aus der Dropdown-Liste aus. Im Screenshot verwendet **Lernobjekt** - **Lernobjekt-ID** **Count Distinct**, alias ount_of_course.

Verfügbare Aggregatfunktionen:

| Funktion | Was zurückgegeben wird |
|----------|-----------------|
| Count | Gesamtanzahl der Zeilen in der Gruppe |
| Eindeutige Werte zählen | Anzahl der eindeutigen Werte in der Gruppe |
| Zählen wenn | Anzahl der Zeilen, die einem von Ihnen angegebenen Wert entsprechen |
| Summe | Summe eines numerischen Felds in der Gruppe |
| Min. | Niedrigster Wert in der Gruppe |
| Max. | Höchster Wert in der Gruppe |
| Mittelmäßig | Mittlerer Wert innerhalb der Gruppe |

## Filter anwenden

Der Abschnitt **Filter** befindet sich unter dem Abschnitt **Spalten**. Filter beschränken, welche Zeilen im Bericht angezeigt werden.

1. Um einen Filter hinzuzufügen, wählen Sie das Symbol **+** rechts neben dem Abschnitt &quot;Filter&quot; aus.
2. Wählen Sie das Feld aus, nach dem gefiltert werden soll.
   ![](assets/image017.png)
3. Wählen Sie einen Operator und geben Sie einen Wert ein bzw. wählen Sie einen Wert.

Um einen vorhandenen Filter zu bearbeiten, wählen Sie das Symbol **Stift** in der Filterzeile aus. Um eine verschachtelte Filtergruppe hinzuzufügen, wählen Sie das Symbol &quot;+&quot; mit Klammern rechts neben einer Filterzeile aus.

## Sortierung konfigurieren

Der Abschnitt Sortieren befindet sich unter dem Abschnitt Filter.

1. Wählen Sie **+ Sortierung hinzufügen**, um eine Sortierung hinzuzufügen.
2. Wählen Sie die Spalte aus, nach der sortiert werden soll, und wählen Sie **Aufsteigend** oder **Absteigend** aus.
   ![](assets/image020.png)
3. Wiederhole den Vorgang, um eine zweite Sortierfolge hinzuzufügen. Ziehen Sie den Griff links neben jeder Sortierzeile, um die Priorität zu ändern.

>[!TIP]
>
>Wenden Sie immer mindestens eine Sortierung an. Ohne Sortierung kann die Zeilenreihenfolge bei den Downloads desselben Berichts abweichen.

## Bericht speichern

Wählen Sie in der oberen rechten Ecke **Bericht speichern** aus. Der Bericht wird auf der Registerkarte **Berichte** gespeichert und kann jetzt heruntergeladen werden.

## Best Practices

* Verwenden Sie Aliase in jeder Spalte, damit der heruntergeladene Bericht aussagekräftige Kopfzeilen anstelle von Feldnamen wie _Lernobjekt_ - _Lernobjekt-ID_ enthält.
* Verwenden Sie &quot;Unterschiedliche zählen&quot; anstelle von &quot;Anzahl&quot;, wenn Sie eindeutige Datensätze wünschen, z. B. unterschiedliche Kurse pro Katalog anstelle von Gesamtzeilen.
* Sortieren Sie sie vor dem Speichern, insbesondere für Berichte, die Sie freigeben oder abonnieren.
* Halten Sie die Beschreibung auf dem neuesten Stand. Andere Administratoren verlassen sich darauf, dass sie den Umfang des Berichts verstehen, ohne ihn zu öffnen.

---
jcr-language: en_us
title: Duplizierte Report Builder-Vorlage anpassen
description: Bearbeiten Sie eine Adobe Learning Manager-Report Builder-Vorlage, um sie Ihren spezifischen Spalten, Filtern und Sortieranforderungen anzupassen.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---


# Duplizierte Report Builder-Vorlage anpassen

Nach dem Duplizieren einer Vorlage können Sie Spalten hinzufügen oder entfernen, Filter aktualisieren, Spalten umbenennen und die Sortierung anpassen, bevor Sie sie speichern und herunterladen\. Dieser Artikel behandelt jeden Anpassungsschritt\.

Duplizieren Sie zunächst eine Vorlage auf der Registerkarte **Vorlagen**.

## Spalten hinzufügen und entfernen

1. Suchen Sie in der Bearbeitungsansicht den Datensatz, der die hinzuzufügende Spalte enthält.
2. Wählen Sie **+** neben dem Spaltennamen aus. Die Spalte wird auf der Berichtsarbeitsfläche angezeigt.
3. Um dieselbe Spalte mehrmals hinzuzufügen, z. B. um zwei verschiedene Statuswerte zu zählen. Wählen Sie **+** erneut für diese Spalte aus.
4. Um eine Spalte zu entfernen, wählen Sie sie auf der Arbeitsfläche aus und klicken Sie dann auf das Symbol &quot;Entfernen&quot; .

## Spalten neu anordnen und umbenennen

1. Ziehen Sie eine Spalte auf die gewünschte Position auf der Arbeitsfläche. Die Reihenfolge auf der Arbeitsfläche entspricht der Spaltenreihenfolge in der heruntergeladenen Datei.
2. Um eine Spalte umzubenennen, wählen Sie ihr Aliasfeld aus und geben Sie den Namen ein, der als Spaltenüberschrift im Bericht angezeigt werden soll.

## Aktualisierungsfilter

1. Um einen vorhandenen Filterwert zu ändern, wählen Sie die Filterzeile aus, bearbeiten den Wert und bestätigen ihn.
2. Um einen neuen Filter hinzuzufügen, wählen Sie **Filter hinzufügen**.
3. Wählen Sie das Feld aus, nach dem Sie filtern möchten.
4. Wählen Sie einen Operator. Die verfügbaren Operatoren hängen vom Datentyp des Felds ab.
5. Geben Sie einen Wert ein oder wählen Sie einen aus:
   * Geben Sie bei Zeichenfolgenfeldern ein, nach denen gesucht werden soll, und wählen Sie Vorschläge aus.
   * Wählen Sie für Listenfelder einen oder mehrere Werte aus der Auswahl aus.
   * Geben Sie als Datumsfelder ein Datum ein oder wählen Sie einen relativen Bereich aus, z. B. die letzten 90 Tage.
6. Um einen Filter zu entfernen, wählen Sie das Löschsymbol in dieser Filterzeile aus.

## Sortierung aktualisieren

1. Wählen Sie in der Spalte, nach der sortiert werden soll, das Sortiersymbol aus.
2. Wählen Sie **Aufsteigend** oder **Absteigend**.
3. Wenn Sie nach weiteren Spalten sortieren möchten, wiederholen Sie die Schritte für jede Spalte. Die erste sortierte Spalte ist primär. zusätzliche Sortierungen gelten innerhalb von Verbindungen.

>[!TIP]
>
>Wenden Sie immer mindestens eine Sortierung an. Ohne Sortierung kann die Zeilenreihenfolge bei den Downloads desselben Berichts abweichen.

## Speichern und herunterladen

1. Wählen Sie Speichern aus, um Ihre Änderungen auf der Registerkarte **Berichte** zu speichern.
2. Wählen Sie **Download**, um den Bericht zu generieren. Sie erhalten eine In-App-Benachrichtigung, wenn die Datei bereit ist.

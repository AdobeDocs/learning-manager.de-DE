---
jcr-language: en_us
title: Hinzufügen und Kombinieren von Filtern in einem Bericht
description: Beschränken Sie Berichtsdaten in Adobe Learning Manager Report Builder mit einzelnen Filtern, AND/OR-Logik und verschachtelten Filtergruppen.
contentowner: mmanuel
source-git-commit: 8823a5481bc3b34266f7ec36a8f3c26cb923e1ce
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---


# Hinzufügen und Kombinieren von Filtern in einem Bericht

## Übersicht

Mit Filtern können Sie den Umfang Ihres Berichts genau an die Datensätze anpassen, die Sie benötigen. Sie können einen einzelnen Filter anwenden, mehrere Filter mit UND- oder ODER-Logik kombinieren und verschachtelte Gruppen für komplexe Bedingungen erstellen.

## Filter hinzufügen.

Verwenden Sie Filter, um den Bericht auf einen bestimmten Teil der Daten zu beschränken, anstatt alles anzuzeigen.

Beispielsweise möchten Sie möglicherweise wissen, wie viele Teilnehmer sich in den letzten 365 Tagen für Kurse registriert haben. In diesem Fall wenden Sie einen Datumsfilter auf das Registrierungsdatum an, um nur die letzten Aktivitäten einzuschließen.

1. Starten Sie den Report Builder, und wählen Sie **Bericht erstellen**.
2. Geben Sie den Namen und die Beschreibung des Berichts ein.
3. Wählen Sie die folgenden Spalten aus: <dataset>:<column name>

   * Registrierung - Registrierungsdatum
   * Benutzer - Name

   ![](assets/report-builder-0024.png)

4. Wählen Sie im Abschnitt &quot;Berichte&quot; **Filter hinzufügen**.
5. Suchen Sie nach dem Feld, nach dem Sie filtern möchten, oder navigieren Sie zu diesem Feld. Wählen Sie in diesem Beispiel **Registrierung - Registrierungsdatum**.

   ![](assets/report-builder-0025.png)

6. Wählen Sie **Hinzufügen** aus.
7. Wählen Sie einen Operator. Die verfügbaren Operatoren hängen vom Datentyp des Felds ab:

   * Zeichenfolgenfelder - enthält, entspricht, beginnt mit
   * Numerische Felder - größer als, kleiner als, gleich, zwischen
   * Datumsfelder - ist gleich, vorher, nachher, zwischen, letzte N Tage
   * Listenfelder (enum) - ist in, ist nicht in

8. In diesem Fall wählen Sie **innerhalb des letzten Jahres**.

   ![](assets/report-builder-0026.png)

9. Wählen Sie **Bericht speichern** aus, und wählen Sie **Aktionen** > **Download** aus, um den Bericht herunterzuladen.

Der heruntergeladene Bericht listet alle Benutzer auf, die sich in den letzten 365 Tagen für ein Lernobjekt registriert haben.

## Hinzufügen mehrerer Filter mit UND/ODER-Logik

Wenn Sie einen zweiten Filter hinzufügen, lautet die Standardbeziehung zwischen Filtern AND; Beide Bedingungen müssen wahr sein, damit eine Zeile angezeigt wird.

Beispielsweise können Sie Teilnehmer identifizieren, die sich in den letzten 365 Tagen für Kurse registriert haben UND einen Bericht an einen bestimmten Manager senden. In diesem Fall müssen beide Bedingungen wahr sein, d. h., Filter werden mithilfe der UND-Logik kombiniert.

1. Starten Sie den Report Builder, und wählen Sie **Bericht erstellen**.
2. Geben Sie den Namen und die Beschreibung des Berichts ein.
3. Wählen Sie die folgenden Spalten aus: <dataset>:<column name>

   * Benutzer - Name
   * Benutzer - Name des Managers
   * <span class="mark">Registrierung - Registrierungsdatum</span>

4. Gruppieren Sie nach der Spalte &quot;**Benutzer-Manager-Name**&quot;.
5. Wählen Sie im Abschnitt Filter die folgenden Filter aus:

   * Registrierung - Registrierungsdatum i **s innerhalb des letzten Jahres**
   * Benutzer - Managername **beginnt mit** N
   * Benutzer - Der Name &quot;**&quot; des Managers ist nicht leer.**

     ![](assets/report-builder-0027.png)

6. Wählen Sie **Bericht speichern** aus, und wählen Sie **Aktionen** > **Download** aus, um den Bericht herunterzuladen.

Der heruntergeladene Bericht listet alle Benutzer auf, die sich in den letzten 365 Tagen **und** für ein Lernobjekt registriert haben, und meldet sich bei einem Manager an, dessen Name mit N beginnt.

## Verschachtelte Filtergruppen erstellen

Mit verschachtelten Gruppen können Sie Bedingungen mit mehreren logischen Ebenen erstellen, die Klammern in einer Formel entsprechen. Beispiel: (Katalog = Sicherheit ODER Katalog = Hygiene) UND Ausfülldatum sind die letzten 90 Tage.

Verwenden Sie verschachtelte Filtergruppen, wenn Ihre Logik eine Mischung aus AND- und OR-Bedingungen enthält, die zusammen ausgewertet werden müssen.

Verwenden Sie beispielsweise eine verschachtelte Filterlogik, um unvollständige Registrierungen zu identifizieren, bei denen die Teilnehmer einen Fortschritt von unter 50 % oder eine überfällige Schulung haben, was zeigt, wie UND- und ODER-Bedingungen zusammenwirken.

1. Starten Sie den Report Builder, und wählen Sie **Bericht erstellen**.
2. Geben Sie den Namen und die Beschreibung des Berichts ein.
3. Wählen Sie die folgenden Spalten aus: <dataset>:<column name>

   * Registrierung - Status
   * Registrierung - Fortschritt in Prozent
   * Registrierung - Überfällig

     ![](assets/report-builder-0028.png)

4. Wählen Sie im Abschnitt **Filter** die folgenden Filter aus:

   * Registrierung - Der Status &quot;**&quot; ist nicht gleich &quot;** Completed&quot;.
   * Wählen Sie +.
   * Suchen Sie nach &quot;Enrollment-Progress Percent&quot;.
   * Wählen Sie den Filter aus.
   * Wählen Sie **Als Gruppe hinzufügen**.

     ![](assets/report-builder-0029.png)

5. Registrierung hinzufügen - Fortschritt Prozent **kleiner als** 50.

   ![](assets/report-builder-0030.png)

6. Wählen Sie +.
7. Suchen Sie nach &quot;**Enrollment-Overdue**&quot;.
8. Wählen Sie den Filter aus.
9. Wählen Sie **Als Gruppe hinzufügen**.

   ![](assets/report-builder-0031.png)

10. &quot;Überfällige Einschreibung hinzufügen&quot; ist gleich &quot;TRUE&quot;.
11. Ändern Sie das verschachtelte AND in OR.

    ![](assets/report-builder-0032.png)

12. Wählen Sie **Bericht speichern** aus, und wählen Sie **Aktionen** > **Download** aus, um den Bericht herunterzuladen.

Der heruntergeladene Bericht listet alle Registrierungen auf, die ausgeführt werden oder nicht gestartet wurden, deren Fortschritt in Prozent weniger als 50 % beträgt oder überfällig sind.

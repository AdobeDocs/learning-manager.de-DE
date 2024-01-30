---
title: Empfehlungen in Adobe Learning Manager
description: Der Kern der Empfehlungs-Engine basiert auf dem neuen Kurs-Ranking-Algorithmus von Learning Manager. Der Algorithmus verwendet 50 Millionen Datenpunkte und fünf Jahre aggregierter Lerndaten über Millionen von Benutzern, um Kurse basierend auf ihrer Wahrscheinlichkeit einer Registrierung zu bewerten. Diese Einstufung stellt sicher, dass die Kurse mit den meisten Registrierungen den Teilnehmenden als erste angezeigt werden.
source-git-commit: 40f6732147b7babeb1f11ce52045e6baf6338ce1
workflow-type: tm+mt
source-wordcount: '1435'
ht-degree: 60%

---



# Empfehlungen in Adobe Learning Manager

Adobe Learning Manager hat ein neues und überarbeitetes Empfehlungssystem für Kurse eingeführt. Diese Empfehlungsfunktion nutzt KI-Algorithmen und Nutzerinteressen wie Produkte, Rollen und Stufen, um personalisierte Inhaltsempfehlungen bereitzustellen.

Mit dem neuen Empfehlungssystem können Sie benutzerdefinierte Parameter erstellen, die die Teilnehmenden auswählen können, um personalisierte Empfehlungen zu erhalten. Diese Empfehlungen werden den Teilnehmenden im Feed ihrer Homepage als Kurse, Lernpfade und Zertifizierungen angezeigt.

Um mit dieser Funktion zu beginnen, müssen Sie die Funktion in der Admin-App aktivieren.

## Empfehlungen aktivieren und konfigurieren

1. Laden Sie die Kurs- und Benutzerdaten hoch (optional).
1. Aktivieren Sie die Änderungen.
1. Laden Sie nach dem Aktivieren und Konfigurieren der Empfehlungen die Daten in den Adobe Learning Manager hoch, damit die Empfehlungen funktionieren. Diese Daten umfassen:

   * Kursdaten
   * Benutzerdaten (optional)

## Algorithmus für die Kursrangliste

Der Kern der Empfehlungs-Engine basiert auf den neuen **[!UICONTROL Algorithmus für die Kursrangfolge]**. Der Algorithmus verwendet 50 Millionen Datenpunkte und fünf Jahre aggregierter Lerndaten über Millionen von Benutzern, um Kurse basierend auf ihrer Wahrscheinlichkeit einer Registrierung zu bewerten. Diese Einstufung stellt sicher, dass die Kurse mit den meisten Registrierungen den Teilnehmenden als erste angezeigt werden.

## Schlüsselbegriffe

Die neue AI-basierte Empfehlungs-Engine von Learning Manager bietet Lernenden ein konfigurierbares, parameterbasiertes Empfehlungssystem für die Erstellung eines personalisierten Erlebnisses für Teilnehmer.

Die Parameter sind: **Produkte/Themen**, **Rollen** und **Stufen**. Darüber hinaus können diese Parameter Ihren Anforderungen entsprechend umbenannt werden. So können &quot;Produkte&quot; zu &quot;Themen&quot; oder &quot;Rollen&quot; zu &quot;Region&quot; werden.

## Einrichten des Empfehlungssystems

Die neue Empfehlungs-Engine von Adobe Learning Manager vereinfacht den Admin-Arbeitsablauf beim Einrichten personalisierter Empfehlungen, da Daten zu Produkten und Rollen, die mit einem Kunden/Partner verknüpft sind, in der Regel Administratoren zur Verfügung stehen (z. B. aus Kaufunterlagen).

Bei der Einrichtung der neuen Empfehlungs-Engine gibt es hauptsächlich drei Arbeitsabläufe:

* Administration
* Autor
* Teilnehmer

Die Parameterwerte für Produkte, Rollen und Stufen des Kontos werden durch die Administration konfiguriert. Ein IT-Lösungsanbieter mit Banken als Hauptkundenbasis kann beispielsweise den Parameter &quot;Product&quot; so konfigurieren, dass Werte wie Payment Gateway, Secure Cloud Storage, Fraud Detection System, Trading Platform usw. und den Parameter &quot;Role&quot; Werte wie Integration Specialist, Network Administrator, Risk Analyst, Compliance Officer usw. aufweisen.

Administratoren erhalten in Learning Manager einen geführten Arbeitsablauf, mit dem sie die Empfehlungs-Engine optimal einrichten und die Engine basierend auf dem Anwendungsfall des Kontos anpassen können. Darüber hinaus hat die Administration auch die Möglichkeit, PRL-Empfehlungen über einen einmaligen CSV-Upload einzurichten.

1. Auswählen **[!UICONTROL Recommendations]** in der Admin-App.

   ![Wählen Sie Recommendations in der Admin-App aus.](assets/image831538.png)

   *Wählen Sie die Option Recommendations*

1. Klicken Sie auf **[!UICONTROL Aktualisieren]**.

   ![Upgrade auf das neue System](assets/image784236.png)

   *Wählen Sie die Upgrade-Option aus*

1. Klicken Sie auf **[!UICONTROL Fortfahren]**, um auf das neue Empfehlungssystem zu aktualisieren.

   ![Zum neuen System wechseln](assets/image521152.png)
   *Schaltfläche &quot;Fortfahren&quot; auswählen*

1. Erstellen Sie die Empfehlungsparameter für Produkte und Rollen.

   ![Erstellen der Parameter](assets/image43406.png)
   *Erstellen von Parametern für Empfehlungen*

1. Klicken Sie auf **[!UICONTROL Weitere Werte hinzufügen]**.
1. Fügen Sie die Produkte hinzu. Geben Sie den Namen eines Produkts ein und drücken Sie die Eingabetaste.

   Sie müssen mindestens zwei Produkte hinzufügen, damit Sie beginnen können.

   ![Produkte hinzufügen](assets/image623058.png)
   *Produkte hinzufügen*

1. Fügen Sie die Rollen hinzu. Geben Sie die Namen der Rollen ein und drücken Sie die Eingabetaste.

   ![Rollen hinzufügen](assets/image156786.png)
   *Rollen hinzufügen*

1. Klicken Sie auf **[!UICONTROL Fortfahren]**.

   Die Produkte und Rollen sind jetzt in der Liste der Parameter enthalten.

   ![Produkte und Rollen](assets/image266930.png)
   *Liste der Produkte und Rollen*

## Datenvorbereitung

Die Interessensdaten der Benutzer, das Produkt, die Rollen und die Stufen müssen hochgeladen werden, damit die Empfehlungen ordnungsgemäß funktionieren.

**Datenoptionen hochladen**

Die Empfehlungsfunktion ist konfigurierbar. Anstelle von &quot;products/roles/levels&quot; können Sie &quot;topics/roles/level&quot; verwenden oder eine der folgenden Optionen auswählen: &quot;product/topics only&quot;, &quot;roles only&quot;, &quot;product/topics and roles only&quot;, &quot;roles-levels&quot; oder &quot;products-levels&quot;.

Ändern Sie Ihre Datenblätter entsprechend der von Ihnen gewählten Empfehlungskonfiguration.

Im folgenden Abschnitt wird die umfassendste Option zur Verwendung von Produkten, Rollen und Stufen erläutert.

Die/der Administrator(in) muss Benutzer(innen)daten in einem vordefinierten Format hochladen. Die hochgeladenen Daten werden dann in den Empfehlungsalgorithmus eingespeist, sodass Teilnehmende Empfehlungen für die richtigen Kurse basierend auf ihren Rollen und Stufen erhalten.

**Voraussetzungen**

Um die Daten hochzuladen, damit die Empfehlungen funktionieren, tragen Sie die Produkte, Rollen und Stufen in die RecommendationLO-CSVs ein.

Im Rahmen der Datenvorbereitung stellen wir zwei CSV-Vorlagen zur Verfügung:

**RecUser.csv**

* Benutzer-ID
* Produkte
* Rollen
* Stufen (Anfänger, Fortgeschrittene oder Experten)

Im Folgenden finden Sie ein Beispiel für Datensätze in der CSV-Datei:

| Benutzer-ID | Produkte | Rollen | Stufen |
|--- |--- |--- |--- |
| 123 | Data Science | Analyst | Analyst: Fortgeschritten |
| 456 | Luft- und Raumfahrttechnik | Techniker | Techniker: Fortgeschritten |

**RecLO.csv**

* Kurs/Lernpfad
* Schulungstyp
* Schulungsname
* Produkte
* Rollen
* Stufen
* Tags
* Kenntnisse

Im Folgenden finden Sie ein Beispiel für Datensätze in der CSV-Datei:

| Schulungs-ID | Schulungstyp | Schulungsname | Produkte | Rollen | Stufen | Tags | Kenntnisse |
|---|---|---|---|---|---|---|---|
| 111 | KURS | Python 101 | Data Science | Analyst | Analyst: Fortgeschritten | data | Allgemein |
| 222 | KURS | Julia 101 | Data Science | Analyst | Analyst: Fortgeschritten | data | Allgemein |

Füllen Sie diese CSVs aus und wenden Sie sich an Ihr Customer Success Team, um die Formate herunterzuladen und diese CSVs hochzuladen.

## Umsetzung der Empfehlungen

Nachdem beide CSV hochgeladen wurden, klicken Sie auf &quot;Go live&quot; (Live loslegen). Dadurch wird das neue Empfehlungssystem für die Teilnehmenden sichtbar.

![live gehen](assets/computerdescription-automatically.png)
*Empfehlungen live schalten.*

Das Empfehlungssystem ist jetzt für Ihre Teilnehmenden verfügbar.

## Parameter bearbeiten

1. Wählen Sie in der Parameterliste das Drei-Punkte-Symbol und dann **[!UICONTROL Parameternamen bearbeiten]**.

   ![Parameter bearbeiten](assets/edit-parameter.png)

1. Ändern Sie den Namen des Parameters und klicken Sie auf **[!UICONTROL Speichern]**.

   ![Ergebnisse](assets/image688522.png)
   *Parameter bearbeiten*

## Parameter löschen

1. Wählen Sie in der Parameterliste das Drei-Punkte-Symbol und dann **[!UICONTROL Parameter löschen]**.

![Löschparameter](assets/delete-parameter.png)
*Parameter löschen*

## Seite &quot;Kurseinstellungen&quot;

Auf der Einstellungsseite eines Kurses werden die Empfehlungen für Produkte und Rollen aufgeführt. Teilnehmenden wird dieser Kurs empfohlen, wenn sie Interesse an diesen Produkten und Rollen gezeigt haben.

![Einstellbild](assets/course-settings-image.png)
*Seite &quot;Kurseinstellungen&quot;*

## Teilnehmendenansicht

Bei einem Konto mit PRL-basierten Empfehlungen werden Teilnehmende, die sich bei der Lernplattform anmelden, durch einen geführten Arbeitsablauf bei der Einrichtung von Empfehlungen basierend auf dem Produkt, der Rolle und der gewünschten Stufe unterstützt. So wird das Teilnehmerprofil erstellt, das von der Empfehlungs-Engine analysiert werden kann.

Teilnehmende mit Konten, die auf das neue Empfehlungssystem umgestellt wurden, können die empfohlenen Kurse und Schulungen anzeigen.

Die Teilnehmenden können Folgendes sehen:

* Produkte, Rollen - Stufen: Die Teilnehmenden werden aufgefordert, zuerst Produkte, Rollen und dann Stufen für jede der ausgewählten Rollen auszuwählen.
* Produkt – Stufen: Die Teilnehmenden werden aufgefordert, zuerst Produkte und dann Stufen für jedes der ausgewählten Produkte auszuwählen.
* Rollen – Stufen: Die Teilnehmenden werden aufgefordert, zuerst Rollen und dann Stufen für jede der ausgewählten Rollen auszuwählen.
* Produkte und Rollen: Die Teilnehmenden werden aufgefordert, zuerst Produkte und dann Rollen auszuwählen.
* Produkte: Die Teilnehmenden werden aufgefordert, nur Produkte auszuwählen.
* Rollen: Die Teilnehmenden werden aufgefordert, nur Rollen auszuwählen.

Nachdem Teilnehmende im linken Bereich „Empfehlungen“ ausgewählt haben, wird ein Popup-Fenster angezeigt, in dem die Empfehlungen eingerichtet werden können.

![Einrichtungsempfehlungen](assets/image575540.png)
*Teilnehmer richtet Empfehlung ein*

Durch Klicken auf &quot;Empfehlungen einrichten&quot; gelangen die Teilnehmenden zum Popup für die Produktauswahl.

![Popup-Fenster für Produktauswahl](assets/product-selection-popup.png)
*Produkte auswählen*

Im nächsten Popup können die Teilnehmenden die Rolle auswählen.

![auserwählte Rolle](assets/image270860.png)
*Rollen auswählen*

Die Teilnehmenden können dann die Stufen hinzufügen.

![Stufen hinzufügen](assets/image650040.png)
*Ebenen auswählen*

## Lernstreifen in der Teilnehmer-App

Teilnehmende können die folgenden Streifen in der App sehen:

* „Eigenes Lernen“-Streifen
* Streifen mit Kalender-, Sozial- und Gamification-Widget
* „Von mir gespeichert“-Streifen
* „Super relevant„-Streifen
* Produktstreifen – 1
* Produktstreifen – 2
* Erkennungsstreifen
* „Vom Administrator empfohlen“-Streifen
* „Nach Katalogstreifen durchsuchen“-Streifen

### Karten auf meinem Lernstreifen

![Lernstreifen-Karten](assets/image770606.png)
*Karten auf dem Lernstreifen*

Jede Karte verfügt über die Schaltflächen „Bewertung“, „Kartenbild“, „Titel“, „Kenntnisse“, „Veröffentlichungsdatum“, „Autor“, „Dauer“, „Fortschrittsleiste“ und „Fortfahren“ oder „Entdecken“.

### Karten auf gespeichert von mir Streifen

![gespeicherte Karten](assets/cards-saved-by-me.png)
*Gespeicherte Karten*

Jede Karte verfügt über die Schaltflächen „Bewertung“, „Kartenbild“, „Titel“, „Kenntnisse“, „Veröffentlichungsdatum“, „Autor“, „Dauer“, „Fortschrittsleiste“ und „Start“ oder „Entdecken“ oder „Fortfahren“ oder „Erneut aufrufen“.

Es gibt keine Fortschrittsleiste auf der Karte, nachdem Teilnehmende den Kurs gestartet haben. Teilnehmende können das Speichern des Kurses auch aufheben.

### Karten auf superrelevantem Streifen

![superrelevante Streifenkarten](assets/super-relevant-cards.png)
*Relevante Karten*

Jede Karte verfügt über die Schaltflächen „Bewertung“, „Kartenbild“, „Titel“, „Kenntnisse“, „Veröffentlichungsdatum“, „Autor“, „Dauer“, „Fortschrittsleiste“ und „Start“ oder „Entdecken“ oder „Fortfahren“ oder „Erneut aufrufen“.

Es gibt keine Fortschrittsleiste auf der Karte, nachdem Teilnehmende den Kurs gestartet haben.

Das Menü enthält zwei Optionen: **[!UICONTROL Speichern]** und **[!UICONTROL Empfehlen Sie das nicht]**. Wenn der Teilnehmer auf **[!UICONTROL Speichern]**, der Kurs wird im Streifen &quot;Gespeichert von mir&quot; gespeichert. Wenn der Teilnehmer auf **[!UICONTROL Empfehlen Sie das nicht]** klicken, wird die empfohlene Schulung aus der Liste entfernt.

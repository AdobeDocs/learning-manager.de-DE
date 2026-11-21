---
description: Erfahren Sie, wie Autoren E-Mails auf Kurs- und Instanzebene in Email Builder mit einem Administrator-Layout anpassen und häufige Probleme beheben
jcr-language: en_us
title: Kurs- und Instanz-E-Mails in Email Builder anpassen
exl-id: 06499e3f-0610-4983-83f2-3e8b578fc8bf
source-git-commit: 05691364449234a4782e2de5d4752c7b277f5fd4
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%
---

## Kurs- und Instanz-E-Mails in Email Builder anpassen

Passen Sie E-Mails auf Kurs- und Instanzebene in Adobe Learning Manager mit Email Builder und einem Layout an, das Ihr Administrator bereitstellt.

Als Autor können Sie E-Mails für einen Kurs oder für eine bestimmte Instanz eines Kurses anpassen. Beide Verfahren beginnen mit einem Layout, das Ihr Administrator bereitstellt.

### Anpassen einer E-Mail auf Kursebene

1. Öffnen Sie den Kurs.
2. Wählen Sie **E-Mail-Vorlagen** aus.
3. Wählen Sie **Layout für Kurs-E-Mail** aus.
4. E-Mail-Inhalte anpassen. So legen Sie Schriftarten, Farben, Zeilen und Schaltflächen fest:
5. Speichern Sie die Vorlage.
6. Publish.

### Anpassen einer E-Mail auf Instanzebene

Verwenden Sie eine E-Mail auf Instanzebene, wenn verschiedene Kohorten unterschiedliche Nachrichten benötigen. Sie verwalten diese Kohorten über Kursinstanzen.

1. Öffnen Sie die Kursinstanz.
2. Öffnen Sie **Email Builder**.
3. Wählen Sie ein verfügbares Layout aus oder übernehmen Sie das Layout, das die Instanz bereits verwendet.
4. Aktualisieren Sie den Nachrichteninhalt.
5. Speichern Sie die Vorlage.

>[!NOTE]
>
>Wenn beide vorhanden sind, überschreiben E-Mails auf Instanzebene die Vorlagen auf Kursebene.

### Verwenden der Variable &quot;Titel&quot; und eines Bildes für E-Mail-Header

Verwenden Sie die Variable &quot;Titel&quot; mit einer Image-Komponente, um anstelle der Banner-Komponente die E-Mail-Kopfzeile zu erstellen. Das Bild der Banner-Komponente wird in einigen E-Mail-Clients, z. B. Outlook, nicht angezeigt.

Die Variable &quot;Titel&quot;, &quot;EmailTitle&quot;, funktioniert wie die vorhandene Variable &quot;ChannelName&quot;. Jede E-Mail hat einen eigenen Standardtitel.

So fügen Sie eine Titelüberschrift hinzu:

1. Fügen Sie eine Image-Komponente für das Titelbild hinzu.
2. Fügen Sie eine Textkomponente hinzu und fügen Sie die Titelvariable aus dem Dropdown-Menü &quot;Variablen&quot; im Konfigurationsbereich der Komponente ein.
3. Richten Sie die Textkomponente zentriert aus. Platzieren Sie es im globalen Layout in der oberen Kopfzeile.

Einzelne E-Mails verwenden standardmäßig den Header aus dem globalen Layout. In einer einzelnen E-Mail können Sie die Textkomponente wie folgt bearbeiten:

1. Ersetzen der Variablen durch benutzerdefinierten Text
2. Text vor oder nach der Variablen hinzufügen und `EmailTitle` beibehalten

Wenn Sie ein Bild zur Banner-Komponente hinzufügen, zeigt Email Builder eine Warnung an, dass das Bild in einigen E-Mail-Clients möglicherweise nicht korrekt angezeigt wird. In der Warnung wird empfohlen, stattdessen eine Image-Komponente und die Titelvariable zu verwenden.

### Fehlerbehebung

**Sie können kein Layout auswählen.**
Die Vererbung des Layouts hängt von den verfügbaren übergeordneten Layouts ab. Bitten Sie Ihren Administrator, ein Konto-Layout zu erstellen.

**Ihre E-Mail zeigt keine aktuellen Layoutänderungen an.**
Möglicherweise ist die Verknüpfung der Vorlage mit ihrem Layout aufgehoben. Nicht verknüpfte Vorlagen erhalten keine Layoutaktualisierungen mehr.

**Teilnehmer in einer Instanz erhalten eine andere E-Mail als die Kurs-E-Mail.**
E-Mails auf Instanzebene setzen Kursvorlagen außer Kraft. Überprüfen Sie die Vorlage auf Instanzebene.

**Sie sehen den E-Mail-Generator für Ihre Kurs- oder Instanz-E-Mails nicht.**
Adobe aktiviert Email Builder in mehreren Phasen. Bitten Sie Ihren Administrator, die Aktivierung von Email Builder für Ihr Konto zu bestätigen.

**Ihr Bannerbild wird nicht in der E-Mail angezeigt.**
Einige E-Mail-Clients, z. B. Outlook, zeigen das Bild der Banner-Komponente nicht an. Entfernen Sie die Banner-Komponente, fügen Sie eine Bildkomponente hinzu, und fügen Sie eine Textkomponente hinzu, die die Titelvariable verwendet.

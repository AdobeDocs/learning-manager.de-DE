---
description: Administratoren können eine Sitzung starten, bei der sie anstelle eines anderen Benutzers in ihrem Konto eine Anmeldung in ihren Teilnehmer- und Managerrollen vornehmen können.
jcr-language: en_us
title: Identitätswechsel des Teilnehmers und Managers
contentowner: saghosh
source-git-commit: d59e748472c77527c22b286aea5412f776f6441b
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 0%

---



# Identitätswechsel des Teilnehmers und Managers {#impersonation-of-learner-and-manager}

In großen Unternehmen benötigen Mitarbeiter des Kunden-Supports Identitätswechsel, um Probleme der Teilnehmer zu beheben.

Mit dieser Möglichkeit, die Identität anderer Benutzer anzunehmen, können Administratoren und benutzerdefinierte Administratoren alle Aktivitäten von Teilnehmern und Managern ihres Unternehmens identifizieren und ausführen.

## Und so funktioniert&#39;s

Administratoren (und/oder benutzerdefinierte Administratoren) können nach einem Benutzer suchen (intern oder extern) und dann die Identität eines Benutzers annehmen. Der Administrator wird dann zur Seite des Benutzers (Manager-App, falls zutreffend, oder zur Teilnehmer-App) umgeleitet und meldet den Administrator dann von seiner Sitzung ab. Der Administrator wird dann zur Seite Profil abschließen weitergeleitet, falls diese für den Benutzer eingerichtet wurde, für den der Administrator die Identität eines anderen Administrators übernommen hat.

Wenn ein benutzerdefinierter Administrator über die Berechtigung verfügt, auf die Seite eines Benutzers zuzugreifen, kann er nach Benutzern suchen, für die er sich ausgeben möchte.

Das müssen Sie beim Nachahmen der Identität eines Benutzers beachten:

* Alle Administratoren sehen diese Funktion standardmäßig.
* Nur aktive Benutzer im Konto können die Identität annehmen.
* Ein Administrator kann sich nicht selbst als Administrator ausgeben.
* Ein benutzerdefinierter Administrator, der Zugriff auf die Seite &quot;Benutzer&quot; hat, kann die Identität eines Benutzers annehmen.
* Ein Administrator/benutzerdefinierter Administrator kann die Identität nur 60 Minuten lang annehmen.

## Die Identität eines Benutzers annehmen

Um die Identität eines Benutzers zu übernehmen, führen Sie die folgenden Schritte aus:

1. Melden Sie sich bei der App als Administrator an.
1. Wählen Sie Profil > Identität eines Benutzers annehmen.

   Sie können jeweils nur die Identität eines Benutzers annehmen.

1. Suchen Sie im Suchfeld des Modals nach einem Benutzer (intern/extern). Sie können jeweils nur die Identität eines Benutzers annehmen. Wählen Sie Fortfahren.

   Sie können auch mit Benutzer-E-Mail, UUID usw. suchen.

1. Es wird eine Meldung mit der Bestätigung angezeigt, dass Sie die Identität eines Benutzers annehmen.

   Wählen Sie Fortfahren.

   Eine Bestätigungsmeldung mit dem Titel &quot;Identitätswechsel-Modus: Sie sind als &quot;Benutzername (Benutzer-E-Mail-Adresse)&quot; angemeldet. &quot;Abmelden&quot; wird in der Kopfzeile der Seite angezeigt.

**Eine imitierte Sitzung dauert 60 Minuten.**

Beim Wechsel zu einer Teilnehmer- oder Managerrolle wird eine Meldung angezeigt, die darauf hinweist, dass sich der Administrator/benutzerdefinierte Administrator in einem Identitätswechselmodus des Benutzers befindet.

## Anmelde- und Zugriffsbericht

Die Anmeldung und der Zugriff eines Administrators werden im Anmelde- und Zugriffsbericht erfasst. Für jeden Benutzer, für den der Administrator die Identität eines Benutzers annehmen kann, wird im Bericht ein Datensatz erstellt.

Die Spalten, die Teil dieser Funktion sind:

* Identitätswechsel durch Benutzername
* Identitätswechsel durch Benutzer-E-Mail

Diese Spalten werden am Ende des Berichts hinzugefügt.

Jede Anmeldung wird im Bericht separat gezählt.

## Was nicht unterstützt wird

* Die Identität von AEM Komponenten.
* Identitätswechsel in der Mobile App.
* Immersive Imitation für Mobilgeräte.
* Imitation von immersiven Apps. Sie gilt nur für ALM-Apps.

## Häufig gestellte Fragen

+++Kann ich mich beim Adobe Learning Manager anmelden, auch wenn ich selbst die Identität eines Benutzers annehmen muss?

Ja, die Anmeldung eines Benutzers ist unabhängig vom Identitätswechsel.
+++

+++Werden Identitätswechsel in einzigartiger Weise erfasst?

Ja, jeder Anmeldezugriff/Besuch durch den Administrator während des Identitätswechsels wird separat gezählt.
+++

+++Was ist das Zeitlimit für Identitätswechsel?

Es sind 60 Minuten. Wenn ein Benutzer, der die Identität annehmen möchte, das Browser-Fenster schließt und dann innerhalb von 60 Minuten zu einer beliebigen Prime-URL navigiert, wird die Identitätswechselaktivität fortgesetzt und die Banner-Meldung muss angezeigt werden.
+++

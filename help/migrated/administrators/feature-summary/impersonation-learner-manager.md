---
description: Administratoren können eine Sitzung starten, in der sie die Identität eines beliebigen Benutzers in ihrem Konto in der Teilnehmer- und Manager-Rolle übernehmen können.
jcr-language: en_us
title: Annehmen der Identität eines Teilnehmers und Managers
contentowner: saghosh
exl-id: 0306f255-283f-43b9-9494-11b3dc3765da
source-git-commit: f44f44ab34acc42edb79d66588ad986d629734ff
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 59%

---

# Annehmen der Identität eines Teilnehmers und Managers {#impersonation-of-learner-and-manager}

In großen Unternehmen benötigen Mitarbeiter des Kunden-Supports Identitätswechsel, um Probleme der Teilnehmer zu beheben.

Mit dieser Möglichkeit, die Identität anderer Benutzer anzunehmen, können Administratoren alle Aktivitäten von Teilnehmern und Managern ihres Unternehmens identifizieren und ausführen.

>[!NOTE]
>
>Benutzerdefinierte Administratoren haben nicht die Möglichkeit, die Identität eines Benutzers anzunehmen. Nur Administratoren können die Identität eines Benutzers ändern.

## Funktionsweise

Administratoren können nach einem Benutzer suchen (intern oder extern) und dann die Identität eines Benutzers annehmen. Der Administrator wird dann zur Seite des Benutzers (Manager-App, falls zutreffend, ansonsten Teilnehmer-App) umgeleitet und von seiner eigenen Sitzung abgemeldet. Der Administrator wird dann zur Seite „Profil abschließen“ weitergeleitet, falls diese für den Benutzer eingerichtet wurde, dessen Identität der Administrator übernommen hat.

Das müssen Sie beim Nachahmen der Identität eines Benutzers beachten:

* Diese Funktion wird allen Administratoren standardmäßig angezeigt.
* Es kann nur die Identität von aktiven Benutzern im Konto angenommen werden.
* Ein Administrator kann nicht seine eigene Identität annehmen.
* Ein benutzerdefinierter Administrator, der über Zugriff auf die Seite „Benutzer“ verfügt, kann die Identität eines Benutzers annehmen.
* Ein Administrator/benutzerdefinierter Administrator kann die Identität nur 60 Minuten lang annehmen.
* Ein benutzerdefinierter Administrator mit schreibgeschütztem Zugriff kann keine Identität für Benutzer annehmen.

## Annehmen der Identität eines Benutzers

Um die Identität eines Benutzers anzunehmen, gehen Sie wie folgt vor:

1. Melden Sie sich bei der App als Administrator an.
1. Wählen Sie Profil > Identität eines Benutzers annehmen.

   Sie können jeweils nur die Identität eines Benutzers annehmen.

1. Suchen Sie im Suchfeld des modalen Fensters nach einem Benutzer (intern/extern). Sie können nur die Identität von jeweils einem Benutzer annehmen. Wählen Sie „Fortfahren“.

   Sie können auch mit Benutzer-E-Mail, UUID usw. suchen.

1. Es wird eine Meldung mit der Bestätigung angezeigt, dass Sie die Identität eines Benutzers annehmen.

   Wählen Sie „Fortfahren“.

   Eine Bestätigungsmeldung mit dem Titel &quot;Identitätswechsel-Modus: Sie sind als &quot;Benutzername (Benutzer-E-Mail-Adresse)&quot; angemeldet. &quot;Abmelden&quot; wird in der Kopfzeile der Seite angezeigt.

**Eine imitierte Sitzung dauert 60 Minuten.**

Beim Wechsel zu einer Teilnehmer- oder Managerrolle wird eine Meldung angezeigt, die darauf hinweist, dass sich der Administrator in einem Identitätswechselmodus des Benutzers befindet.

## Anmelde- und Zugriffsbericht

Die Anmeldung und der Zugriff eines Administrators werden im Anmelde- und Zugriffsbericht erfasst. Für jeden Benutzer, dessen Identität der Administrator annimmt, wird im Bericht ein Eintrag erstellt.

Folgende Spalten gehören zu dieser Funktion:

* Identitätswechsel durch Benutzername
* Identitätswechsel durch Benutzer-E-Mail

Diese Spalten werden am Ende des Berichts hinzugefügt.

Jede Anmeldung wird im Bericht separat gezählt.

## Nicht unterstützte Vorgänge

* Annahme der Identität von AEM-Komponenten.
* Identitätswechsel in der mobilen App.
* Identitätswechsel in der immersiven Umgebung für Mobilgeräte.
* Annahme der Identität immersiver Apps. Gilt nur für ALM-Apps.

## Häufig gestellte Fragen

+++Kann ich mich bei Adobe Learning Manager anmelden, auch wenn ich die Identität eines anderen Nutzers annehmen muss?

Ja, die Anmeldung eines Benutzers ist unabhängig vom Identitätswechsel.
+++

+++Werden Identitätswechsel in einzigartiger Weise erfasst?

Ja, jeder Anmeldezugriff/Besuch durch den Administrator während des Identitätswechsels wird separat gezählt.
+++

+++Was ist das Zeitlimit für Identitätswechsel?

60 Minuten. Wenn ein Benutzer, der eine andere Identität annimmt, das Browser-Fenster schließt und dann innerhalb von 60 Minuten zu einer beliebigen Prime-URL navigiert, wird die Identitätswechselaktivität fortgesetzt und die Banner-Meldung muss angezeigt werden.
+++

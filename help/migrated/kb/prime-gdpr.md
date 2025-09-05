---
jcr-language: en_us
title: Learning Manager – Konformität mit der DSGVO
description: Adobe Learning Manager-Konformität mit der DSGVO
contentowner: dvenkate
exl-id: 8ea31464-b4ce-49e8-b471-5630f0216aa4
source-git-commit: a01ec6117ad49a1f9af0b31d48ad19ddc8443dde
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 39%

---

# Learning Manager – Konformität mit der DSGVO

>[!IMPORTANT]
>
>Der Inhalt dieses Dokuments ist keine Rechtsberatung und soll keine Rechtsberatung ersetzen. Bitte wenden Sie sich an die Rechtsabteilung Ihres Unternehmens bezüglich Beratung zur DS-GVO.

Adobe Learning Manager hält an der Einhaltung der DSGVO fest und stellt sicher, dass Anwenderdaten sicher und transparent verwaltet werden. Es bietet wichtige DSGVO-Funktionen wie die Möglichkeit, Benutzer zu bereinigen (alle personenbezogenen Daten dauerhaft zu löschen) und ermöglicht es Administratoren, Teilnehmertranskripte zu erstellen, um Informationen auf Anfrage an Benutzer weiterzugeben.

Alle Benutzerdaten werden während der Übertragung und Speicherung mit starker Verschlüsselung unter Verwendung von Standards wie SHA-256 geschützt. Bei einigen Integrationen müssen sich die Teilnehmer authentifizieren, um sicherzustellen, dass ihre Zustimmung eingeholt wird, bevor sie Daten freigeben. Diese Datenschutz- und Sicherheitskontrollen helfen Unternehmen, die Adobe Learning Manager verwenden, dabei, die DSGVO einzuhalten und die Informationen der Teilnehmer zu schützen.

+++Was ist die DS-GVO?

Die DSGVO ist eine neue Verordnung der Europäischen Union, die am 25. Mai 2018 in Kraft tritt. Sie bietet eine starke Datenschutzkontrolle und ermöglicht es den Endbenutzern, ihre personenbezogenen Daten zu verwalten.

+++

+++Wie oder warum gilt sie für Sie als Adobe Learning Manager-Kunde?

Die DSGVO ist eine EU-Verordnung, sie gilt jedoch weltweit für Unternehmen, die personenbezogene Informationen für jeden Benutzer erfassen, der in der EU ansässig ist.  Als Learning Manager-Kunde sollten Sie prüfen, ob die DSGVO für Ihr Unternehmen gilt.

+++

+++Welche Rolle spielt Adobe dabei als Anbieter von Learning Manager?

Gemäß DSGVO werden Sie als [Datenverantwortlicher](https://gdpr-info.eu/art-24-gdpr/) betrachtet, wenn Ihr Unternehmen ein Produkt oder eine Dienstleistung für EU-Bürger anbietet und bestimmt, wie und warum deren Daten erfasst, verfolgt und überwacht werden. Wenn Sie als Adobe Learning Manager-Kunde eine dieser Aktivitäten ausführen, gelten Sie als Datenverantwortlicher.

Unternehmen, die Daten im Namen von Controllern verarbeiten, gelten als [Datenverarbeiter](https://gdpr-info.eu/art-28-gdpr/). Als Anbieter von Cloud-gehostetem LMS Adobe Learning Manager spielt Adobe die Rolle des Datenverarbeiters. Hier sind einige weitere Details zu [der DSGVO und Ihrem Unternehmen](https://www.adobe.com/privacy/general-data-protection-regulation.html).

+++

+++Wie ermöglicht Learning Manager Ihnen die Einhaltung der DS-GVO?

Learning Manager verfügt über die folgenden Tools und Prozesse, die Sie bei der Einhaltung der DS-GVO unterstützen. Um Prozesse zu unterstützen, die über die vollständige Konformität des Produkts mit der Verordnung hinausgehen, müssen Sie möglicherweise trotzdem mit Ihrem Compliance-Team eine Bewertung vornehmen.

**Recht auf Vergessenwerden - In Bezug auf den Datenverantwortlichen:** Die DSGVO erfordert, dass Datenverantwortliche eine Funktion für das Recht auf Vergessenwerden für ihre Benutzer unterstützen. Dies bedeutet, dass jeder Benutzer das Recht hat, den für die Verarbeitung Verantwortlichen aufzufordern, alle für diesen Benutzer gespeicherten personenbezogenen Daten unwiderruflich zu löschen. Wenn Sie eine solche Anfrage erhalten und deren Gültigkeit bestätigen, wird diese Funktion nun in Learning Manager über die Funktion [Benutzer bereinigen](../administrators/feature-summary/purge-users.md) bereitgestellt. Mit dieser Funktion kann der Administrator ein permanentes Löschen der mit einer bestimmten Person in Verbindung stehenden Daten veranlassen, sodass Learning Manager die Daten umgehend aus der zugehörigen Datenbank löscht. Die Bereinigung der Sicherungsprotokolle (die zur Wiederherstellung des Systems dienen) erfolgt ebenfalls automatisch.

**Recht auf Vergessen - Kontaktieren des Datenverarbeiters**: Der Endbenutzer kann auch selbst Adobe kontaktieren, um seine personenbezogenen Daten zu löschen. In diesem Fall erkennt Learning Manager automatisch, welche Konten die Daten für diesen Benutzer besitzen, und Adobe benachrichtigt den Administrator sofort über eine solche Anfrage. Der Administrator kann dann die Gültigkeit der Anforderung bewerten und die Anforderung über die Funktion &quot;Benutzer bereinigen&quot; anrufen.

**Zugriffsrecht:** Die DSGVO gibt dem Endbenutzer das Recht, Daten anzufordern, die ein Controller möglicherweise für diesen Endbenutzer gespeichert hat. Um diese Anforderung zu unterstützen, ermöglicht der Lern-Manager dem Administrator, selbst ein Teilnehmertranskript zu generieren, das dem Benutzer freigegeben werden kann.

**Datenschutz durch Design, Datenverschlüsselung:** Wir verarbeiten Daten sowohl während der Übertragung als auch im Ruhezustand unter Verwendung der besten Verschlüsselungsstandards, um die Datensicherheit zu gewährleisten. Als Verschlüsselungsalgorithmen werden SHA-256 verwendet. Dies stellt sicher, dass alle Daten, die Sie speichern, ausreichend geschützt sind, damit sie nicht in falsche Hände geraten.

+++

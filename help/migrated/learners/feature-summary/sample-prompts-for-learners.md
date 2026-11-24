---
description: Hier finden Sie Beispielaufforderungen, die Teilnehmer in Claude oder ChatGPT Enterprise bitten können, Kurse zu suchen, Anmeldungen zu überprüfen und Lernpfade zu erstellen
jcr-language: en_us
title: Beispielaufforderungen für Adobe Learning Manager-Teilnehmer
exl-id: e5d64ac4-03e9-49bc-95d0-bb074d55987f
source-git-commit: 89aa1b5ab02eed8a61507ab162fcbbd384e6c5fc
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%
---

# Beispielaufforderungen für Adobe Learning Manager-Teilnehmer

Verwenden Sie diese Eingabeaufforderungen in Claude oder ChatGPT Enterprise, um Kurse zu suchen, Anmeldungen zu überprüfen und Lernpfade zu erstellen.

Verbinde zuerst deinen AI-Client. Weitere Informationen über [Verbinden Ihres AI-Clients mit Adobe Learning Manager](/help/migrated/learners/feature-summary/connect-ai-client-to-alm-learner.md). Jede Eingabeaufforderung ist einem Tool in der [Teilnehmertools-Referenz](/help/migrated/learners/feature-summary/learner-tools-reference.md) zugeordnet.

>[!TIP]
>
>Benennen Sie die benötigten Informationen, z. B. ein Thema, einen Kursstatus oder einen Abgabetermin. Spezifische Anforderungen helfen dem AI-Client, das richtige Tool auszuwählen.

## Registrierungen

| **Eingabeaufforderung** | **Tool** |
|------------------------------------------|------------------------------|
| Für welche Kurse bin ich registriert? | list_my_learning_enrollments |
| Welche meiner Kurse laufen demnächst ab? | list_my_learning_enrollments |

## Suchen

| **Eingabeaufforderung** | **Tool** |
|-----------------------------------------|-----------------------|
| Welche Führungskurse gibt es? | search_learning_items |
| Zeigt mir verfügbare Sicherheitsschulungen an. | search_learning_items |

## Wissen

| **Eingabeaufforderung** | **Tool** |
|----|----|
| Was bedeutet Management von Lieferkettenrisiken in FedRAMP? | answer_learning_content_question |
| Erläutern Sie die Anforderungen in meinem Compliance-Kurs. | answer_learning_content_question |

## Lernpfade

| **Eingabeaufforderung** | **Tool** |
|----|----|
| Helfen Sie mir, eine Reihe von Kursen zu finden, die Kenntnisse im Projektmanagement erweitern. | personalized_learning_path |
| Speichern Sie diesen Lernpfad. | personalized_learning_path |

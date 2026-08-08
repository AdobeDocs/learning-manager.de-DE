---
description: Informieren Sie sich über den Unterschied zwischen Abschluss- und Erfolgskriterien in Content Composer, wie diese konfiguriert werden und warum dieser Unterschied ausschlaggebend für die exakte Verfolgung und Berichterstellung von Teilnehmern in Adobe Learning Manager ist.
jcr-language: en_us
title: Abschluss- und Erfolgskriterien festlegen
source-git-commit: f8687710f5b73e8b7cf8d56057cac25483f38cdc
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---


# Abschluss- und Erfolgskriterien festlegen

## Abschlusskriterien

**Abschlusskriterien**: Wählen Sie die Dropdown-Liste aus und wählen Sie aus, wann der Kurs als abgeschlossen markiert ist.

- **Start:** markiert den Kurs als abgeschlossen, sobald er von einem Teilnehmer geöffnet wird, unabhängig davon, wie viel er angezeigt wird.
  ![](../assets/21_completion_criteria_dropdown_launch_minview_quiz_updated.png)

- **Min. Ansicht %:** markiert den Kurs als abgeschlossen, sobald ein Teilnehmer den angegebenen Prozentsatz des Kursinhalts anzeigt.
  ![](../assets/22_completion_criteria_minview_percent_field_updated.png)

- **Quiz: markiert den Kurs als abgeschlossen basierend auf der Quizaktivität des Teilnehmers. Quizbedingung auswählen:**

  - **Bei Versuch:** markiert den Abschluss, sobald der Teilnehmer das Quiz versucht, unabhängig vom Ergebnis.

  - **Bei Bestehen:** wird nur als abgeschlossen markiert, wenn der Teilnehmer das Quiz besteht.

  - **Bei Bestehen oder Limit erreicht:** markiert den Abschluss, wenn der Teilnehmer das Quiz besteht, oder die maximale Anzahl der zulässigen Versuche erreicht, je nachdem, was zuerst eintritt.
    ![](../assets/23_completion_criteria_quiz_condition_dropdown_updated.png)

## Erfolgskriterien

**Erfolgskriterien** bestimmen, ob ein Teilnehmer nach der Teilnahme am Kurs als bestanden oder als nicht bestanden markiert wird. Im Gegensatz zu Abschlusskriterien werden Erfolgskriterien auf Punktebasis erstellt.

>[!NOTE]
>
>Die verfügbaren Optionen hängen von der SCORM-Version ab, die unter **Exporteinstellungen** ausgewählt wurde. Wenn Sie **SCORM 1.2** auswählen, werden Abschluss- und Erfolgskriterien in einer einzigen Einstellung zusammengefasst. Wenn Sie **SCORM 2004** auswählen, werden Abschluss- und Erfolgskriterien wie unten beschrieben als separate Einstellungen angezeigt.*

- **Erfolgskriterien**: Wählen Sie in der Dropdown-Liste aus, wie der Kurs den Erfolg misst.

- **Start:** markiert den Teilnehmer als bestanden, indem er den Kurs startet.
  ![](../assets/24_success_criteria_dropdown_launch_minview_quiz_updated.png)

- **Min. Ansicht %**: markiert den Teilnehmer als bestanden, sobald er den angegebenen Prozentsatz des Inhalts angezeigt hat. Geben Sie beispielsweise 80 ein, damit die Teilnehmer mindestens 80 % des Kurses sehen müssen.
  ![](../assets/25_success_criteria_minview_percent_field_updated.png)

- **Quiz:** markiert den Teilnehmer als bestanden oder fehlgeschlagen, je nachdem, ob seine Quizpunktzahl den Schwellenwert für die Mindestpunktzahl für das Bestehen erfüllt. Quizbedingung auswählen:

  - **Bei Versuch: markiert den erfolgreichen Test, sobald der Teilnehmer das Quiz absolviert.**

  - **Durchgang: nur dann als erfolgreich markiert, wenn der Teilnehmer das Quiz besteht.**

  - **Bei Bestehen oder Limit erreicht: als erfolgreich markiert, wenn der Teilnehmer die maximal zulässigen Versuche besteht oder erreicht.**

  ![](../assets/26_success_criteria_quiz_condition_dropdown_updated.png)

>[!NOTE]
>
>Ein Teilnehmer kann einen Kurs abschließen, aber dennoch fehlschlagen, z. B. wenn er den gesamten Inhalt abgeschlossen hat, aber beim Quiz nicht gut genug abschneidet. Abschluss- und Erfolgskriterien sind unabhängig; Legen Sie beides sorgfältig fest, je nachdem, wie Sie den Fortschritt des Teilnehmers und die Leistung verfolgen möchten. Wenn Sie &quot;Quiz&quot; für eines der beiden Kriterien auswählen, konfigurieren Sie Quizwiederholungen und übergeben Sie die Punktzahl auf der Registerkarte **Quizeinstellungen**.


## Warum Abschluss- und Erfolgskriterien für die Berichterstattung wichtig sind

- Abschlusskriterien steuern, wann sich der Status eines Teilnehmers in ALM-Transkripten, Abschluss-Dashboards und allen Compliance- oder Audit-Exporten, die aus dem LMS abgerufen werden, in &quot;Abgeschlossen&quot; ändert. Sie messen den Fortschritt, nicht die Leistung.

- Erfolgskriterien steuern den Wert &quot;Bestanden/Nicht bestanden&quot;, der zusammen mit dem Abschlussstatus aufgezeichnet wird - dem Wert, auf den die meisten Compliance- und Zertifizierungsberichte angewiesen sind.

- Wenn Abschluss- und Erfolgskriterien auch in der **Adobe Learning Manager**-Inhaltsbibliothek für dasselbe Modul konfiguriert sind, haben diese Einstellungen Vorrang vor den Einstellungen, die in Content Composer festgelegt wurden. Überlegt euch frühzeitig, für welches Produkt diese Regeln gelten sollen, und vermeidet es, widersprüchliche Werte an beiden Stellen festzulegen.

- Passen Sie die Kriterien an das an, was Sie nachweisen müssen: Die Start- oder Min-Ansicht % reicht für den Inhalt der Sensibilisierung aus, während Quizkriterien Ihnen einen vertretbaren Datensatz bieten, dass ein Teilnehmer Wissen demonstriert hat - nicht nur, dass er den Kurs geöffnet hat.

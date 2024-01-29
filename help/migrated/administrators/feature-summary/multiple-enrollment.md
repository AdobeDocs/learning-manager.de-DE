---
title: Mehrere Registrierungen für den Adobe Learning Manager
description: Als Kontoadministrator ist es eine Ihrer Hauptaufgaben, verschiedene Instanzen von VILT-Sitzungen in verschiedenen Zeitzonen zu erstellen und möglicherweise Sitzungen für bestimmte Benutzergruppen zu erstellen.
source-git-commit: fc5b5afd8dd42ac3aa0e5190d6f421035df41a89
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# Mehrere Registrierungen für den Adobe Learning Manager

Im Adobe-Lernmanager kann jeder Kurs verschiedene Instanzen haben. Als Kontoadministrator ist es eine Ihrer Hauptaufgaben, verschiedene Instanzen von VILT-Sitzungen in verschiedenen Zeitzonen zu erstellen und möglicherweise Sitzungen für bestimmte Benutzergruppen zu erstellen.

Wenn ein Administrator einen Teilnehmer vor der Version vom Juli 2023 registriert hat, konnten sie sich nur in einer Instanz registrieren. Wenn ein Teilnehmer einen Kurs in verschiedenen Instanzen absolvieren möchte, erstellt der Administrator viele Kurse, einen für jede Instanz.

Die Funktion für mehrere Registrierungen des Adobe Learning Managers hilft einem Administrator, solche Szenarien zu vermeiden.

## Was ist Mehrfacheinschreibung?

Mehrere Registrierungen registrieren einen Teilnehmer mehrmals in einem Kurs über verschiedene verfügbare Instanzen.  Ein Teilnehmer kann sich in mehreren Kursinstanzen registrieren, unabhängig davon, in welchem Status er sich registriert, abgeschlossen oder noch nicht gestartet hat. Wenn der Autor die Option [!UICONTROL Mehrfachregistrierung] umschalten, kann sich ein Teilnehmer dann für mehrere Instanzen des Kurses registrieren.

![Bild mit mehreren Registrierungen](assets/multi-enrollment-author.png)
*Starten der Mehrfachregistrierung über die Einstellungen*

Der Fortschritt jeder Instanz kann einzeln verfolgt werden, und ein Bericht kann exportiert werden, um den Fortschritt jeder Instanz zu verfolgen.

## Wichtige Aspekte

* Eine Mehrfachregistrierung ist nur bei einem Kurs mit mehreren Instanzen möglich.
* Sobald die Option für mehrere Registrierungen aktiviert ist und Benutzer in mehreren Instanzen registriert sind, werden neue Zeilen für jeden Kurs im Teilnehmertranskriptbericht erstellt (eine Zeile für jede Instanz und jeden Teilnehmer).
* Wenn die Berichtsautomatisierung eingerichtet ist, die nur eine Zeile pro Kurs vorwegnimmt, müssen Sie die erforderlichen Anpassungen an der Berichtsautomatisierung vornehmen, bevor Sie die Funktion zur Mehrfacheinschreibung aktivieren.

## Aktivieren der Mehrfacheinschreibung

1. Melden Sie sich bei Ihrem Adobe Learning Manager-Konto als Autor an.
1. Wählen Sie den Kurs aus, für den sich die Teilnehmer mehrmals registrieren sollen.
1. Wählen Sie im linken Bereich **[!UICONTROL Einstellungen]** > **[!UICONTROL Bearbeiten]** > **[!UICONTROL Instanzkonfiguration]** > **[!UICONTROL Mehrfache Registrierung aktivieren]**.

![Bild mit mehreren Registrierungen](assets/multi-enrollment-author.png)
*Aktivieren Sie die Mehrfacheinschreibung.*

>[!NOTE]
>
>Als Autor können Sie nicht gleichzeitig den Instanzwechsel und die Mehrfacheinschreibung aktivieren.

## Teilnehmeransicht

Mehrere Registrierungen sind hilfreich, wenn sich ein Teilnehmer für einen Klassenzimmer- oder VC-Kurs anmelden oder einen Kurs erneut abschließen möchte, bevor er zu einem anderen Kurs wechselt.

Wenn Teilnehmer sich nicht registriert haben und einen Kurs auswählen, wird der Bildschirm unter dem Kurs mit mehreren Instanzen angezeigt. Dann können sie jede Instanz auswählen und sich registrieren.

![Bild der Teilnehmeransicht](assets/learner-view.png)
*Instanzen anzeigen*

Nach der Registrierung für eine Instanz können sie sich für andere Instanzen registrieren, indem sie im rechten Bereich die Option Alle Instanzen anzeigen auswählen.

![Kursbild mit mehreren Registrierungen](assets/enroll-instance.png)
*Bei einer Instanz registrieren*

Der Fortschritt jeder Instanz kann wie folgt verfolgt werden:

![Bearbeitungsstatus verfolgen](assets/check-progress.png)
*Status jeder Instanz verfolgen.*

## Änderungen an mehreren Registrierungen im Administrator

**Registrierung:**

Während der Registrierung der Teilnehmer können Sie das folgende Kontrollkästchen aktivieren:

*&quot;Ausgewählte Teilnehmer sind möglicherweise bereits bei anderen Instanzen dieses Kurses registriert. Lassen Sie zu, dass diese Teilnehmer auch für die Instanz registriert werden ...&quot;*

![Änderungen des Administrators](assets/admin-changes.png)
*Registrierungsoption für Administratoren*

Wenn der Teilnehmer bereits in einer Instanz registriert ist und Sie als Administrator versuchen, den Teilnehmer in einer anderen Kursinstanz zu registrieren, wählen Sie &quot;Ja&quot;.

## Berichte

Für einen Teilnehmer, der sich für zwei Instanzen desselben Kurses registriert, werden für jede Kursinstanz zwei Zeilen erstellt. Der Bericht zeigt auch den Fortschritt der Instanzen an.

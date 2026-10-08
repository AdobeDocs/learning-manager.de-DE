---
jcr-language: en_us
title: Credly
description: Erfahren Sie mehr über die Credly Integration mit ALM, um externe Abzeichen von der Plattform über verschiedene Social Media-Kanäle zu verwalten und freizugeben
contentowner: chandrum
exl-id: 168f7ff8-51f5-4962-bf76-af909fc5565b
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%
---
# Credly

[Credly](https://info.credly.com/) ist eine digitale Anmeldeplattform, mit der Teilnehmer und Organisationen professionelle Leistungen wie Abzeichen oder Zertifizierungen erwerben, freigeben und überprüfen können. Die Teilnehmer können Abzeichen über ihr Credly-Profil in sozialen Medien und an anderen Orten verwalten und teilen.

## Voraussetzung

Richten Sie ein Credly-Konto für Ihre Organisation ein. Fügen Sie Teilnehmer Credly mit ihrer E-Mail-IDs in Adobe Learning Manager hinzu. Dadurch können die Teilnehmer die Abzeichen auf Credly und Adobe Learning Manager sehen.

## Credly-Verbindung zu Adobe Learning Manager hinzufügen

Führen Sie die folgenden Schritte aus, um die Credly-Verbindung zu Adobe Learning Manager hinzuzufügen:

1. Melden Sie sich als **[!UICONTROL Integrationsadministrator]** an.
2. Wählen Sie **[!UICONTROL Credly]** > **Connect** aus, um die **[!UICONTROL Credly]**-Verbindung zu Adobe Learning Manager hinzuzufügen.

   ![](assets/connector-credly.png)
   _Credly Verbindung hinzufügen_

3. Geben Sie den **[!UICONTROL Verbindungsnamen]** ein.
4. Geben Sie die **[!UICONTROL Organisations-ID]** und das **[!UICONTROL Autorisierungstoken]** ein.

   >[!NOTE]
   >
   >Jedes Abzeichen in Credly wird mit einer Organisations-ID und einem Autorisierungs-Token geliefert. Kopieren Sie diese Werte von Credly.

5. Geben Sie den **[!UICONTROL Hostnamen]** ein, und wählen Sie **[!UICONTROL Verbinden]** aus.

## Abzeichen von Credly migrieren

Mit der Datei &quot;badge.csv&quot; in Adobe Learning Manager können Sie Abzeichen von bestehenden LMS- oder externen Systemen migrieren. Die Datei &quot;badge.csv&quot; wurde mit zwei neuen Spalten aktualisiert:

* externalBadgeId
* externalBadgeProvider

Die ID des externen Abzeichens bezieht sich auf die ID der Abzeichenvorlage in der Credly-Plattform, und der externe Abzeichenanbieter ist Credly. Fügen Sie diese Werte in badge.csv hinzu und führen Sie die im [Migrationshandbuch](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/migration-manual#migrationprocedure) genannten Schritte aus, um die CSV-Datei zu migrieren.

## Kenntnisse erstellen - Administrator

Sobald das Abzeichen in Adobe Learning Manager importiert wurde, kann der Administrator dieses Abzeichen als Kenntnisse erstellen. Weitere Informationen zum Erstellen von Kenntnissen finden Sie unter [Kenntnisse erstellen und ändern](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/skills-levels).

### Weisen Sie die Kenntnisse/das Abzeichen dem Lernobjekt zu - Autor

Der Autor/Administrator kann diese Credly importierten ALM-Abzeichen einem Kurs, einem Lernpfad oder einer Zertifizierung (nicht nur Kenntnissen) zuweisen, und beim Verbrauch dieser Lernobjekte wird das Abzeichen erreicht und kann auf Credly und ALM App angezeigt werden.

Teilnehmer können sich bei Credly anmelden und die Abzeichen in der Credly-Plattform sehen. Von Credly aus können sie die Abzeichen auf externen Plattformen wie LinkedIn und anderen sozialen Medien teilen.

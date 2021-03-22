---
description: De statische dossiers van inhoudsbrongegevens worden betreden slechts door de Server van het Platform.
seo-description: De statische dossiers van inhoudsbrongegevens worden betreden slechts door de Server van het Platform.
seo-title: Statische brongegevens van inhoud
solution: Experience Manager
title: Statische brongegevens van inhoud
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder,praktijkgericht
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Statische inhoudsbrongegevens{#static-content-source-data}

De statische dossiers van inhoudsbrongegevens worden betreden slechts door de Server van het Platform.

Het pad voor bestanden met statische inhoudsgegevens wordt als volgt opgelost:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

De server combineert padsegmenten van rechts naar links totdat een absoluut bestandspad is ingesteld.

Alle ` *[!DNL rootPath]*` segmenten kunnen lege, relatieve, of absolute wegsegmenten zijn.

` *[!DNL catalogPath]*` is een absoluut of relatief bestandspad/-naam. *[!DNL requestPath]* moet een relatief bestandspad/-naam zijn.

Meerdere `PS::staticContent.rootPaths`-waarden kunnen worden gedefinieerd in [!DNL PlatformServer.conf]. Hierdoor kunnen brongegevensbestanden over meerdere bestandssystemen worden verspreid. De server van het Platform zal afwisselende wegen in de gespecificeerde orde proberen tot het gegevensdossier wordt gevonden.

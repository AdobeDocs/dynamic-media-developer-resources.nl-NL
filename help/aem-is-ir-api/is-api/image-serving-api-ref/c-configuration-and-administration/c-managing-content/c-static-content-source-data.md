---
description: De statische dossiers van inhoudsbrongegevens worden betreden slechts door de Server van het Platform.
seo-description: De statische dossiers van inhoudsbrongegevens worden betreden slechts door de Server van het Platform.
seo-title: Statische brongegevens van inhoud
solution: Experience Manager
title: Statische brongegevens van inhoud
topic: Scene7 Image Serving - Image Rendering API
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Statische brongegevens van inhoud{#static-content-source-data}

De statische dossiers van inhoudsbrongegevens worden betreden slechts door de Server van het Platform.

Het pad voor bestanden met statische inhoudsgegevens wordt als volgt opgelost:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

De server combineert padsegmenten van rechts naar links totdat een absoluut bestandspad is ingesteld.

Alle ` *[!DNL rootPath]*` segmenten kunnen lege, relatieve of absolute padsegmenten zijn.

` *[!DNL catalogPath]*` is een absoluut of relatief bestandspad/-naam. *[!DNL requestPath]* moet een relatief bestandspad/-naam zijn.

U kunt meerdere `PS::staticContent.rootPaths` waarden definiëren in [!DNL PlatformServer.conf]. Hierdoor kunnen brongegevensbestanden over meerdere bestandssystemen worden verspreid. De server van het Platform zal afwisselende wegen in de gespecificeerde orde proberen tot het gegevensdossier wordt gevonden.

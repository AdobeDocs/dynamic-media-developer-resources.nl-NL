---
description: De statische dossiers van inhoudsbrongegevens worden betreden slechts door de Server van het Platform.
solution: Experience Manager
title: Statische brongegevens van inhoud
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
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

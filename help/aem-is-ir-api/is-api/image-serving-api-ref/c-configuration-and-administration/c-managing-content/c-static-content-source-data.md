---
description: De statische dossiers van inhoudsbrongegevens worden betreden slechts door de Server van het Platform.
solution: Experience Manager
title: Statische brongegevens van inhoud
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Statische brongegevens van inhoud{#static-content-source-data}

De statische dossiers van inhoudsbrongegevens worden betreden slechts door de Server van het Platform.

Het pad voor bestanden met statische inhoudsgegevens wordt als volgt opgelost:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

De server combineert padsegmenten van rechts naar links totdat een absoluut bestandspad is ingesteld.

Alle ` *[!DNL rootPath]*` segmenten kunnen lege, relatieve, of absolute wegsegmenten zijn.

` *[!DNL catalogPath]*` is een absoluut of relatief bestandspad/-naam. *[!DNL requestPath]* moet een relatief bestandspad/-naam zijn.

Meerdere `PS::staticContent.rootPaths`-waarden kunnen worden gedefinieerd in [!DNL PlatformServer.conf]. Hierdoor kunnen brongegevensbestanden over meerdere bestandssystemen worden verspreid. De server van het Platform zal afwisselende wegen in de gespecificeerde orde proberen tot het gegevensdossier wordt gevonden.

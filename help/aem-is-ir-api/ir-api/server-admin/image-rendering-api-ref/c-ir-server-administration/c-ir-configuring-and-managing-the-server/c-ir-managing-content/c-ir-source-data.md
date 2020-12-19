---
description: Brongegevensbestanden voor het renderen van afbeeldingen zijn onder andere vignetbestanden, materiaalbestanden (afbeeldingen voor herhaalbare structuren en decals, maar ook bestanden met CAB's en vensters die stijlbestanden bedekken) en ICC-profielen.
seo-description: Brongegevensbestanden voor het renderen van afbeeldingen zijn onder andere vignetbestanden, materiaalbestanden (afbeeldingen voor herhaalbare structuren en decals, maar ook bestanden met CAB's en vensters die stijlbestanden bedekken) en ICC-profielen.
seo-title: Brongegevens
solution: Experience Manager
title: Brongegevens
topic: Scene7 Image Serving - Image Rendering API
uuid: 76c6419c-613e-4eff-b30f-9fea2a7daf5b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---


# Brongegevens{#source-data}

Brongegevensbestanden voor het renderen van afbeeldingen zijn onder andere vignetbestanden, materiaalbestanden (afbeeldingen voor herhaalbare structuren en decals, maar ook bestanden met CAB&#39;s en vensters die stijlbestanden bedekken) en ICC-profielen.

Alle brongegevensbestanden moeten toegankelijk zijn voor de native code-component van Image Rendering (samen met de Image Server).

Als er een materiaalcatalogus is, wordt het bestand dat is opgegeven in de materiaalcatalogus (met `vignette::Path`, `catalog::Path` of `icc::ProfilePath`) als volgt opgezocht door de Render-server:

* Als het pad absoluut is, wordt het ongewijzigd gebruikt.
* Als het pad relatief is, wordt het voorafgegaan door `catalog::RootPath` (uit een benoemde materiaalcatalogus).
* Als het pad absoluut is, wordt het gebruikt; anders, wordt het geprefixeerd met `default::RootPath` (van de standaardcatalogus).
* Als het pad absoluut is, wordt het gebruikt; anders, combineert de server het met de weg die in [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2) wordt gespecificeerd.
* Als het pad nu absoluut is, wordt het gebruikt; anders, wordt het verondersteld om met betrekking tot [!DNL *[!DNL install_folder]*] te zijn.

Als er geen afbeeldingscatalogus bij betrokken is, wordt het pad gecombineerd met `default::RootPath` en vervolgens verwerkt zoals hierboven.

De fysieke locatie van brongegevensbestanden wordt doorgaans opgegeven met [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). U kunt meerdere waarden opgeven om brongegevensbestanden over meerdere bestandssystemen te kunnen verspreiden. De renderserver probeert elk pad in de opgegeven volgorde totdat het gegevensbestand wordt gevonden.

U kunt op elk moment nieuwe gegevensbestanden toevoegen zonder de server te stoppen.

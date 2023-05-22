---
description: Brongegevensbestanden voor het renderen van afbeeldingen zijn onder andere vignetbestanden, materiaalbestanden (afbeeldingen voor herhaalbare structuren en decals, maar ook bestanden met CAB's en vensters die stijlbestanden bedekken) en ICC-profielen.
solution: Experience Manager
title: Brongegevens
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# Brongegevens{#source-data}

Brongegevensbestanden voor het renderen van afbeeldingen zijn onder andere vignetbestanden, materiaalbestanden (afbeeldingen voor herhaalbare structuren en decals, maar ook bestanden met CAB&#39;s en vensters die stijlbestanden bedekken) en ICC-profielen.

Alle brongegevensbestanden moeten toegankelijk zijn voor de native code-component van Image Rendering (samen met de Image Server).

Als het een materiaalcatalogus betreft, het bestand dat in de materiaalcatalogus is opgegeven (met `vignette::Path`, `catalog::Path`, of `icc::ProfilePath`) wordt als volgt opgezocht door de Render-server:

* Als het pad absoluut is, wordt het ongewijzigd gebruikt.
* Als het pad relatief is, heeft het pad een voorvoegsel `catalog::RootPath` (uit een benoemde materiaalcatalogus).
* Als het pad absoluut is, wordt het gebruikt; anders wordt het vooraf bepaald `default::RootPath` (uit de standaardcatalogus).
* Als het pad absoluut is, wordt het gebruikt; anders, combineert de server het met de weg die in wordt gespecificeerd [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* Als het pad nu absoluut is, wordt het gebruikt; anders wordt ervan uitgegaan dat dit relatief is ten opzichte van [!DNL  *[!DNL install_folder]*].

Als er geen afbeeldingscatalogus bij betrokken is, wordt het pad gecombineerd met `default::RootPath` en vervolgens op de hierboven aangegeven wijze worden verwerkt.

De fysieke locatie van brongegevensbestanden wordt meestal opgegeven met [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). U kunt meerdere waarden opgeven om brongegevensbestanden over meerdere bestandssystemen te kunnen verspreiden. De renderserver probeert elk pad in de opgegeven volgorde totdat het gegevensbestand wordt gevonden.

U kunt op elk moment nieuwe gegevensbestanden toevoegen zonder de server te stoppen.

---
description: Waarschuwing of foutdetails voor een gebruikersupdate in een batchSetAssetMetadata-bewerking.
seo-description: Waarschuwing of foutdetails voor een gebruikersupdate in een batchSetAssetMetadata-bewerking.
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
topic: Scene7 Image Production System API
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---


# SetMetadataFault{#setmetadatafault}

Waarschuwing of foutdetails voor een gebruikersupdate in een batchSetAssetMetadata-bewerking.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Het element waarvan de metagegevens niet correct zijn ingesteld. |
| ` *`fieldHandle`*` | `xsd:string` | De greep naar het metagegevensveld waarvan de waarde niet correct is ingesteld. |
| ` *`code`*` | `xsd:int` | Foutcode. |
| ` *`reden`*` | `xsd:string` | Foutbeschrijving (normale tekst). |


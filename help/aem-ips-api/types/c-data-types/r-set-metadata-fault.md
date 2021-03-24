---
description: Waarschuwing of foutdetails voor een gebruikersupdate in een batchSetAssetMetadata-bewerking.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,metagegevens
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 0%

---


# SetMetadataFault{#setmetadatafault}

Waarschuwing of foutdetails voor een gebruikersupdate in een batchSetAssetMetadata-bewerking.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Het element waarvan de metagegevens niet correct zijn ingesteld. |
| `*`fieldHandle`*` | `xsd:string` | De greep naar het metagegevensveld waarvan de waarde niet correct is ingesteld. |
| `*`code`*` | `xsd:int` | Foutcode. |
| `*`reden`*` | `xsd:string` | Foutbeschrijving (normale tekst). |


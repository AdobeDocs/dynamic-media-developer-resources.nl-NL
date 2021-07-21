---
description: Waarschuwing of foutdetails voor een gebruikersupdate in een batchSetAssetMetadata-bewerking.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,metagegevens
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '64'
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

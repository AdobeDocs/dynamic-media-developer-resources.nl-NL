---
description: Retourneert definities van metagegevensvelden voor opgegeven elementtypen.
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 0%

---

# AssetMetadataFields{#assetmetadatafields}

Retourneert definities van metagegevensvelden voor opgegeven elementtypen.

Syntaxis

## Parameters {#section-5ad771540c5f40c187b35e34aac19305}

| Naam | Type | Beschrijving |
|---|---|---|
| `*`assetType`*` | `xsd:string` | Type actief gekoppeld aan velddefinities (zie &quot;Elementen&quot; voor waarden). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | Array met definities van metagegevensvelden die zijn gekoppeld aan het elementtype dat is opgegeven in `assetType`. |

---
title: AssetMetadataFields
description: Retourneert definities van metagegevensvelden voor opgegeven elementtypen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 0%

---

# [!DNL AssetMetadataFields]{#assetmetadatafields}

Retourneert definities van metagegevensvelden voor opgegeven elementtypen.

Syntaxis

## Parameters {#section-5ad771540c5f40c187b35e34aac19305}

| Naam | Type | Beschrijving |
|---|---|---|
| assetType | `xsd:string` | Type actief gekoppeld aan velddefinities (zie &quot;Elementen&quot; voor waarden). |
| fieldArray | `types:MetadataFieldArray` | Array van definities van metagegevensvelden die zijn gekoppeld aan het elementtype dat is opgegeven in `assetType`. |

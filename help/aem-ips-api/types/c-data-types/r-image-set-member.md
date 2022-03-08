---
description: Elementen die bij een afbeeldingsset horen.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 0%

---

# ImageSetMember{#imagesetmember}

Elementen die bij een afbeeldingsset horen.

Pagina opnieuw instellen betekent dat een [!DNL eCatalog] moet een nieuwe pagina beginnen. `RenderSet` geeft aan dat het deel uitmaakt van een `RenderSet` staal. De waarde wordt geforceerd om `true` for `eCatalog` en `RenderSet` sets.

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| element | `type:Asset` | Elementen in de array met afbeeldingssets. |
| pageReset | `xsd:boolean` | Hiermee wordt een nieuwe pagina gestart. Instelling wordt genegeerd en de waarde wordt geforceerd naar `true` for `eCatalog` en `RenderSet` sets. |

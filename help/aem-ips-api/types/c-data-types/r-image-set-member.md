---
description: Elementen die bij een afbeeldingsset horen.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Afbeeldingssets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# ImageSetMember{#imagesetmember}

Elementen die bij een afbeeldingsset horen.

Pagina opnieuw instellen betekent dat een [!DNL eCatalog] een nieuwe pagina moet starten. `RenderSet` Hiermee wordt aangegeven dat het onderdeel is van een  `RenderSet` staal. De waarde wordt gedwongen aan `true` voor `eCatalog` en `RenderSet` reeksen.

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| `*`element`*` | `type:Asset` | Elementen in de array met afbeeldingssets. |
| `*`pageReset`*` | `xsd:boolean` | Hiermee wordt een nieuwe pagina gestart. Instelling wordt genegeerd en waarde wordt geforceerd naar `true` voor `eCatalog`- en `RenderSet`-sets. |

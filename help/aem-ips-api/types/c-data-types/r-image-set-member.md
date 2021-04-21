---
description: Elementen die bij een afbeeldingsset horen.
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '78'
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


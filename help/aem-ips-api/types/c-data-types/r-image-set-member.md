---
description: Elementen die bij een afbeeldingsset horen.
seo-description: Elementen die bij een afbeeldingsset horen.
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
feature: Dynamic Media Classic,SDK/API,Afbeeldingssets
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '86'
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


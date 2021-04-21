---
description: Eigenschappen voor laagweergave.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 0%

---


# LayerViewInfo{#layerviewinfo}

Eigenschappen voor laagweergave.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| `*`url`*` | `xsd:string` | URL afbeeldingsserver die de sjabloon vertegenwoordigt. Hiermee combineert u `urlModifier`- en `urlPostAp- plyModifier`-velden. |
| `*`urlModifier`*` | `xsd:string` | Afbeelding met protocolopdrachten die moeten worden toegepast vóór aanvraag of `urlPostApplyModifier`-opdrachten. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Beeld die protocolbevelen dienen om na `urlModifier` en verzoekbevelen van toepassing te zijn. |


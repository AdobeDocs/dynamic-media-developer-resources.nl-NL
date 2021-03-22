---
description: Eigenschappen voor laagweergave.
seo-description: Eigenschappen voor laagweergave.
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '58'
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


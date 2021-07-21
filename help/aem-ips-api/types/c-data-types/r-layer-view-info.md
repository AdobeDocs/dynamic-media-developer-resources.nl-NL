---
description: Eigenschappen voor laagweergave.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '52'
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

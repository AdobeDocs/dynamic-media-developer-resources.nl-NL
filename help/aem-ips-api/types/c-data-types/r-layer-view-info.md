---
description: Eigenschappen voor laagweergave.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 0%

---

# [!DNL LayerViewInfo]{#layerviewinfo}

Eigenschappen voor laagweergave.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| url | `xsd:string` | URL afbeeldingsserver die de sjabloon vertegenwoordigt. Combinaties `urlModifier` en `urlPostAp- plyModifier` velden. |
| urlModifier | `xsd:string` | Afbeelding met protocolopdrachten die moeten worden toegepast voordat u een aanvraag indient of `urlPostApplyModifier` opdrachten. |
| urlPostApplyModifier | `xsd:string` | Afbeelding met protocolopdrachten die moeten worden toegepast na `urlModifier` en verzoek opdrachten. |

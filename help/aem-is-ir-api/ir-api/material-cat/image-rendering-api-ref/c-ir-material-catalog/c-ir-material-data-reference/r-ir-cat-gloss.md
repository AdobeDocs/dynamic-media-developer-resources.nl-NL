---
description: Oppervlakglansheid Hiermee bepaalt u de relatieve glansheid van het oppervlak van het materiaal.
seo-description: Oppervlakglansheid Hiermee bepaalt u de relatieve glansheid van het oppervlak van het materiaal.
seo-title: Glans
solution: Experience Manager
title: Glans
topic: Scene7 Image Serving - Image Rendering API
uuid: 7db83f99-15ab-4c43-adfb-07ad0b0c9707
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# Glans{#gloss}

Oppervlakglansheid Hiermee bepaalt u de relatieve glansheid van het oppervlak van het materiaal.

Deze waarde wordt door de renderer gebruikt voor de volgende doeleinden:

* Selecteer de verlichtingskaart wanneer `catalog::Illum` -1 is.
* Bepaalt het glanseffect (spiegelende spiegeling) samen met `catalog::Type`.
* Bepaalt de rendereffecten van 3D-spiegeling in combinatie met `catalog::Type` en `catalog::Roughness`.

## Eigenschappen {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Geheel getal. Percentage in het bereik 0...100. Optioneel voor alle materialen. Wordt alleen gebruikt voor vignetten met meerdere spiegelingstoewijzingen of vignetten met 3D-reflectiemogelijkheid. Laat leeg of stel de waarde -1 in als dit niet bekend is of niet nodig is.

## Standaard {#section-2352721073524f1a8d461f64a363aac9}

Het vignet levert een standaardwaarde op als deze waarde is ingesteld op -1.

## Zie ook {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) ,  [catalog::Ruwheid](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99),  [catalogus::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)

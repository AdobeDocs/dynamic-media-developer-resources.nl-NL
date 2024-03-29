---
description: Oppervlakglansheid Hiermee bepaalt u de relatieve glansheid van het oppervlak van het materiaal.
solution: Experience Manager
title: Glans
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72c5d2f9-a7e6-4ad3-aebe-6a1b1fa5453f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# Glans{#gloss}

Oppervlakglansheid Hiermee bepaalt u de relatieve glansheid van het oppervlak van het materiaal.

Deze waarde wordt door de renderer gebruikt voor de volgende doeleinden:

* Selecteer de verlichtingskaart wanneer `catalog::Illum` is -1.
* Bepaalt het glanseffect (spiegelende spiegeling) dat wordt gerenderd in combinatie met `catalog::Type`.
* Bepaalt 3D-spiegelrendereffecten in combinatie met `catalog::Type` en `catalog::Roughness`.

## Eigenschappen {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Geheel getal. Percentage in het bereik 0...100. Optioneel voor alle materialen. Wordt alleen gebruikt voor vignetten met meerdere spiegelingstoewijzingen of vignetten met 3D-reflectiemogelijkheid. Laat leeg of stel de waarde -1 in als dit niet bekend is of niet nodig is.

## Standaard {#section-2352721073524f1a8d461f64a363aac9}

Het vignet levert een standaardwaarde op als deze waarde is ingesteld op -1.

## Zie ook {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catalogus::Ruwheid](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catalogus::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)

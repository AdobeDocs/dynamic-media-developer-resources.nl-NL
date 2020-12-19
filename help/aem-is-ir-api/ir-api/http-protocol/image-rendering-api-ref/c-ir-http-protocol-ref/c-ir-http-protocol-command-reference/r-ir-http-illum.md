---
description: Selector van belichtingskaart. Hiermee geeft u de belichtingsafbeelding op waarmee dit materiaal liever wordt gerenderd.
seo-description: Selector van belichtingskaart. Hiermee geeft u de belichtingsafbeelding op waarmee dit materiaal liever wordt gerenderd.
seo-title: illusie
solution: Experience Manager
title: illusie
topic: Scene7 Image Serving - Image Rendering API
uuid: 16c7144f-7f16-47d1-8140-fd679e702660
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# illum{#illum}

Selector van belichtingskaart. Hiermee geeft u de belichtingsafbeelding op waarmee dit materiaal liever wordt gerenderd.

`illum=-1|0|1|2`

Als de opgegeven verlichtingskaart niet beschikbaar is in het doelvignet, wordt in plaats daarvan de dichtstbijzijnde beschikbare kaart gebruikt.

`illum=-1` Hiermee geeft u op dat de verlichtingsafbeelding automatisch wordt geselecteerd op basis van de  `gloss=` waarde.

## Eigenschappen {#section-aace8466566e4cf1a0c5a6c0167245c9}

Materiaalkenmerk. Genegeerd als in het vignet geen meerdere verlichtingstoewijzingen zijn gedefinieerd.

## Standaard {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Zie ook {#section-9132e60381c64aa3a8ed1319690db55e}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)

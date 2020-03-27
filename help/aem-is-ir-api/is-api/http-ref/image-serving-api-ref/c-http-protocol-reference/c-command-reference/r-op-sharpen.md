---
description: Afbeelding verscherpen. Past een standaard verscherpingsfilter op de laag of op het definitieve meningsbeeld toe, na al het schrapen, als layer=comp.
seo-description: Afbeelding verscherpen. Past een standaard verscherpingsfilter op de laag of op het definitieve meningsbeeld toe, na al het schrapen, als layer=comp.
seo-title: op_scherpen
solution: Experience Manager
title: op_scherpen
topic: Scene7 Image Serving - Image Rendering API
uuid: 1a00c60a-0d5c-4a99-a649-f29ebd710cf3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_scherpen{#op-sharpen}

Afbeelding verscherpen. Past een standaard verscherpingsfilter op de laag of op het definitieve meningsbeeld toe, na al het schrapen, als layer=comp.

`op_sharpen=0|1`

Het laagmasker of het samengestelde masker wordt ook verscherpt.

## Eigenschappen {#section-b27f3f6a27c34233b3f76805e18b2aa7}

Kenmerk of weergavekenmerk van laag. Is van toepassing op de huidige laag of op de uiteindelijke weergaveafbeelding, indien van toepassing `layer=comp`. Genegeerd door effectlagen.

## Standaard {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`, voor geen verscherpingseffect.

## Voorbeeld {#section-3202122df5db4e14b358ecabfb6d8b85}

Hiermee compenseert u de lichte vervaging die wordt veroorzaakt door het resamplen van de afbeelding. De JPEG-kwaliteit neemt ook toe om extra JPEG-artefacten langs de verscherpte randen te voorkomen.

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## Zie ook {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)

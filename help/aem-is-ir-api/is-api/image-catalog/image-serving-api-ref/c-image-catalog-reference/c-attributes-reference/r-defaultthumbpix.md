---
description: Standaardminiatuurgrootte. Wordt gebruikt in plaats van het kenmerk DefaultPix voor aanvragen van miniaturen (req=tmb).
seo-description: Standaardminiatuurgrootte. Wordt gebruikt in plaats van het kenmerk DefaultPix voor aanvragen van miniaturen (req=tmb).
seo-title: DefaultThumbPix
solution: Experience Manager
title: DefaultThumbPix
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7b310aab-6d38-45f3-a3e7-b074a8e7a795
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# DefaultThumbPix{#defaultthumbpix}

Standaardminiatuurgrootte. Wordt gebruikt in plaats van kenmerk::DefaultPix voor aanvragen van miniaturen (req=tmb).

De server beperkt antwoordafbeeldingen tot maximaal deze breedte en hoogte als in een miniatuuraanvraag ( `req=tmb`) niet expliciet de grootte van de weergave wordt opgegeven met `wid=`, `hei=` of `scl=`.

## Eigenschappen {#section-650d9b1194fb4c47a03c6809e6b4af0e}

Twee gehele getallen, 0 of groter, gescheiden door een komma. Breedte en hoogte in pixels. Een van beide of beide waarden kunnen op 0 worden ingesteld om ze onbeperkt te houden.

Is niet van toepassing op geneste/ingesloten aanvragen.

## Standaard {#section-2c4a4f14540449638822913513170ff1}

Overgenomen van `default::DefaultThumbPix` indien niet gedefinieerd of indien leeg.

## Zie ook {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [kenmerk::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)

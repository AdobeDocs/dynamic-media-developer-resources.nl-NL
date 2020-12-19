---
description: Render-intentie kleurconversie. Biedt de standaard rendering intent voor kleurconversies wanneer de render intent niet is opgegeven met icc=.
seo-description: Render-intentie kleurconversie. Biedt de standaard rendering intent voor kleurconversies wanneer de render intent niet is opgegeven met icc=.
seo-title: IccRenderIntent
solution: Experience Manager
title: IccRenderIntent
topic: Scene7 Image Serving - Image Rendering API
uuid: a9648405-32c3-4762-bbb2-11e97d4f8374
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# IccRenderIntent{#iccrenderintent}

Render-intentie kleurconversie. Biedt de standaard rendering intent voor kleurconversies wanneer de render intent niet is opgegeven met icc=.

## Eigenschappen {#section-0a38c60e1525426185616c42824aee2c}

Enum. Stel dit in op 0 voor perceptueel, 1 voor relatief colorimetrisch, 2 voor verzadiging en 3 voor absoluut colorimetrisch. Houd leeg of stel een andere waarde in om de standaard rendering intent te gebruiken die in het kleurprofiel is gedefinieerd.

## Standaard {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Overgenomen van `default::IccRenderIntent`indien niet gedefinieerd. Als deze leeg is, wordt &#39;relatief colorimetrisch&#39; toegepast.

## Zie ook {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[kenmerk::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) ,  [kenmerk::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0),  [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)

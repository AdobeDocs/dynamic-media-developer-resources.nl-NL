---
title: IccRenderIntent
description: Kleuromzetting-rendering intent. De methode biedt de standaard rendering intent voor kleurconversies wanneer de render-intentie niet is opgegeven met ` icc='.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---

# IccRenderIntent{#iccrenderintent}

Kleuromzetting-rendering intent. Biedt de standaard rendering intent voor kleurconversies wanneer de render-intentie niet is opgegeven met `icc=`.

## Eigenschappen {#section-0a38c60e1525426185616c42824aee2c}

Enum. Stel dit in op 0 voor perceptueel, 1 voor relatief colorimetrisch, 2 voor verzadiging en 3 voor absoluut colorimetrisch. Houd leeg of stel een andere waarde in, zodat u de standaard rendering intent kunt gebruiken die in het kleurprofiel is gedefinieerd.

## Standaard {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Overgenomen van `default::IccRenderIntent`indien niet gedefinieerd. Als deze leeg is, wordt &#39;relatief colorimetrisch&#39; toegepast.

## Zie ook {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[kenmerk::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) , [kenmerk::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0), [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)

---
title: IccRenderIntent
description: Render-intentie kleurconversie. Deze methode biedt de standaard rendering intent voor kleurconversies wanneer &grave; icc=&grave; niet is opgegeven voor de render-intentie.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 732b1935-6556-4420-a056-4e00cb3ed152
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# IccRenderIntent{#iccrenderintent}

Render-intentie kleurconversie. Biedt de standaard rendering intent voor kleurconversies wanneer de render-intentie niet is opgegeven met `icc=`.

## Eigenschappen {#section-2540099fb2fc47d29b04642da4f5922a}

Enum. Stel dit in op 0 voor perceptueel, 1 voor relatief colorimetrisch, 2 voor verzadiging en 3 voor absoluut colorimetrisch.

## Standaard {#section-61a05067905b44099c228e15de279dbd}

Overgenomen van `default::IccRenderIntent` indien niet gedefinieerd of leeg.

## Zie ook {#section-7da9ff3038ca452a9f7375a1ca0581af}

[kenmerk::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) &#42;, [kenmerk::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [`icc=`](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)

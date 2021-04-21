---
description: Limiet voor afbeeldingsgrootte beantwoorden. Maximale breedte en hoogte van reactieafbeelding die aan de client kunnen worden geretourneerd.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# MaxPix{#maxpix}

Limiet voor afbeeldingsgrootte beantwoorden. Maximale breedte en hoogte van reactieafbeelding die aan de client kunnen worden geretourneerd.

De server retourneert een fout als een aanvraag een antwoordafbeelding zou veroorzaken waarvan de breedte en/of hoogte groter is dan `attribute::MaxSize`.

## Eigenschappen {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

Twee gehele getallen, groter dan 0, gescheiden door een komma. Breedte en hoogte in pixels. Kan ook worden ingesteld op 0,0 om een willekeurige antwoordafbeeldingsgrootte zonder beperkingen toe te staan.

## Standaard {#section-45b38dc661854d11b97df5709f4f3434}

Overgenomen van standaard::MaxPix indien niet gedefinieerd of leeg.

## Zie ook {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)

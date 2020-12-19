---
description: Limiet voor afbeeldingsgrootte beantwoorden. Maximale breedte en hoogte van reactieafbeelding die aan de client kunnen worden geretourneerd.
seo-description: Limiet voor afbeeldingsgrootte beantwoorden. Maximale breedte en hoogte van reactieafbeelding die aan de client kunnen worden geretourneerd.
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 8fc5e032-cfbb-40b5-9c3a-a2ec1bc4c3e2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
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

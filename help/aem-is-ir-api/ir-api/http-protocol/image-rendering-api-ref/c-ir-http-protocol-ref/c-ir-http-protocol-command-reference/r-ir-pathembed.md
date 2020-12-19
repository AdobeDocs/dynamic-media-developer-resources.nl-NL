---
description: Paden insluiten. Hiermee geeft u aan of Photoshop-paden die zijn ingesloten in het vignet, moeten worden opgenomen in de reactieafbeelding.
seo-description: Paden insluiten. Hiermee geeft u aan of Photoshop-paden die zijn ingesloten in het vignet, moeten worden opgenomen in de reactieafbeelding.
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: d40ea1b5-f2d3-4f81-b96f-abb4eb7eb2b3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# pathEmbed{#pathembed}

Paden insluiten. Hiermee geeft u aan of Photoshop-paden die zijn ingesloten in het vignet, moeten worden opgenomen in de reactieafbeelding.

`pathEmbed=0|1`

## Eigenschappen {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Request-kenmerk. Wordt genegeerd als het vignet geen padgegevens bevat. De padgegevens worden zo nodig geschaald naar `wid=` en/of `hei=`.

Genegeerd als de indeling van de uitvoerafbeelding het insluiten van paden niet ondersteunt. Raadpleeg de beschrijving van `fmt=` voor een lijst met uitvoerafbeeldingsindelingen die paden insluiten ondersteunen.

## Standaard {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, voor het niet insluiten van paden in uitvoerafbeeldingen.

## Zie ook {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)

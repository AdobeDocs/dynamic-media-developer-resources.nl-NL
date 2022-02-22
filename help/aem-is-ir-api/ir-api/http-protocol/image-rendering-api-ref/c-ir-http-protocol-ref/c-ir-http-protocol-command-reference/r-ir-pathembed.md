---
title: pathEmbed
description: Paden insluiten. Hiermee geeft u aan of Photoshop-paden die zijn ingesloten in het vignet, moeten worden opgenomen in de reactieafbeelding.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 66cc57ef-964e-4062-bb66-efeda15be744
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# pathEmbed{#pathembed}

Paden insluiten. Hiermee geeft u aan of Photoshop-paden die zijn ingesloten in het vignet, moeten worden opgenomen in de reactieafbeelding.

`pathEmbed=0|1`

## Eigenschappen {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Request-kenmerk. Wordt genegeerd als het vignet geen padgegevens bevat. De padgegevens worden geschaald naar `wid=` en/of `hei=` indien nodig.

Genegeerd als de indeling van de uitvoerafbeelding het insluiten van paden niet ondersteunt. Zie de beschrijving van `fmt=` voor een lijst met uitvoerafbeeldingsindelingen die paden insluiten ondersteunen.

## Standaard {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, voor het niet insluiten van paden in uitvoerafbeeldingen.

## Zie ook {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)

---
description: Pad voor maskerbestand. Relatief of absoluut pad en naam voor een afbeeldingsbestand met een masker dat is gekoppeld aan deze catalogusrecord.
seo-description: Pad voor maskerbestand. Relatief of absoluut pad en naam voor een afbeeldingsbestand met een masker dat is gekoppeld aan deze catalogusrecord.
seo-title: MaskPath
solution: Experience Manager
title: MaskPath
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a2d1f08a-0a26-41a6-9be2-f5cc2afb15c4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---


# MaskPath{#maskpath}

Pad voor maskerbestand. Relatief of absoluut pad en naam voor een afbeeldingsbestand met een masker dat is gekoppeld aan deze catalogusrecord.

Hiermee kunt u afzonderlijke maskers aan afbeeldingen koppelen.

De server gebruikt de regels voor padresolutie die worden beschreven in [Brongegevens beheren](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) om het gegevensbestand te zoeken.

## Eigenschappen {#section-cdc3b7e2811e41008479cd97887c01b7}

Tekstreeks. Optioneel. Indien gespecificeerd, moet het een geldig relatieve of absolute het dossierweg van de Server van het Beeld zijn. `attribute::DefaultExt` wordt toegevoegd als er geen achtervoegsel voor het bestand aanwezig is.

Als zowel een hoofdafbeelding ( `catalog::Path`) als een maskerafbeelding ( `catalog::MaskPath`) in een catalogusrecord worden gedefinieerd, moeten beide dezelfde pixelgrootte hebben. Maskerafbeeldingen moeten 8-bits grijswaarden hebben.

`mask=` in de aanvraag overschrijft  `catalog::MaskPath`.

`catalog::MaskPath` Hiermee wordt het alfakanaal in de hoofdafbeelding ( `catalog::Path`), indien aanwezig, overschreven en als het alfakanaal niet is gekoppeld (dus niet vooraf is vermenigvuldigd). Als de afbeeldings-alfa vooraf wordt vermenigvuldigd, wordt `catalog::MaskPath` genegeerd en wordt altijd het alfakanaal gebruikt.

## Standaard {#section-78533e35bfec469ba087cb68a35bb81b}

Geen.

## Zie ook {#section-68d262f5949c4959b8723ba44611d1dc}

[kenmerk::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [kenmerk::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md),  [catalogus::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c),  [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md),  [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)

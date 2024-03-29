---
description: Pad voor maskerbestand. Relatief of absoluut pad en naam voor een afbeeldingsbestand met een masker dat is gekoppeld aan deze catalogusrecord.
solution: Experience Manager
title: MaskPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# MaskPath{#maskpath}

Pad voor maskerbestand. Relatief of absoluut pad en naam voor een afbeeldingsbestand met een masker dat is gekoppeld aan deze catalogusrecord.

Hiermee kunt u afzonderlijke maskers aan afbeeldingen koppelen.

De server gebruikt de regels voor padresolutie die in [Brongegevens beheren](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) om het gegevensbestand te zoeken.

## Eigenschappen {#section-cdc3b7e2811e41008479cd97887c01b7}

Tekstreeks. Optioneel. Indien gespecificeerd, moet het een geldig relatieve of absolute het dossierweg van de Server van het Beeld zijn. `attribute::DefaultExt` wordt toegevoegd als er geen achtervoegsel voor het bestand aanwezig is.

Als beide een hoofdafbeelding ( `catalog::Path`) en een maskerafbeelding ( `catalog::MaskPath`) zijn gedefinieerd in een catalogusrecord, moeten beide exact dezelfde pixelgrootte hebben. Maskerafbeeldingen moeten 8-bits grijswaarden hebben.

`mask=` in de aanvraag overschrijft `catalog::MaskPath`.

`catalog::MaskPath` Hiermee overschrijft u het alfakanaal in de hoofdafbeelding ( `catalog::Path`), indien aanwezig, en als het alfakanaal niet is gekoppeld (dat wil zeggen niet vooraf vermenigvuldigd). Als de alfa van de afbeelding vooraf is vermenigvuldigd, `catalog::MaskPath` wordt genegeerd en wordt het alfakanaal altijd gebruikt.

## Standaard {#section-78533e35bfec469ba087cb68a35bb81b}

Geen.

## Zie ook {#section-68d262f5949c4959b8723ba44611d1dc}

[kenmerk::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [kenmerk::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [catalogus::pad](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md), [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)

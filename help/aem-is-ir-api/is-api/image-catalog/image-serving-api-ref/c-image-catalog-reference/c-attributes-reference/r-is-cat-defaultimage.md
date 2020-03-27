---
description: Standaardreactieafbeelding. Hier geeft u de afbeelding of het item in de catalogus op die moet worden gebruikt als er geen afbeeldingsbestand kan worden gevonden en defaultImage= niet is opgegeven in de aanvraag.
seo-description: Standaardreactieafbeelding. Hier geeft u de afbeelding of het item in de catalogus op die moet worden gebruikt als er geen afbeeldingsbestand kan worden gevonden en defaultImage= niet is opgegeven in de aanvraag.
seo-title: DefaultImage
solution: Experience Manager
title: DefaultImage
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f8f50af-15bb-4333-b227-3eba38653a7d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# DefaultImage{#defaultimage}

Standaardreactieafbeelding. Hier geeft u de afbeelding of het item in de catalogus op die moet worden gebruikt als er geen afbeeldingsbestand kan worden gevonden en defaultImage= niet is opgegeven in de aanvraag.

Dit kan een item uit de catalogus (inclusief een sjabloon), een relatief (ten opzichte `attribute::RootPath`) of absoluut afbeeldingsbestand zijn. Dit is handig als u ontbrekende afbeeldingen wilt vervangen door standaardafbeeldingen.

## Eigenschappen {#section-b6d8193827c34e5f948792aba8b8daaf}

Tekstreeks. Indien opgegeven, moet dit een geldige `catalog::Id` waarde in deze afbeeldingscatalogus zijn, of een relatief (ten opzichte `attribute::RootPath`) of absoluut pad naar een afbeeldingsbestand dat toegankelijk is voor de afbeeldingsserver.

## Beperkingen {#section-5d8ea872f0b0415fbd3a83410bbcf512}

Externe afbeeldingsbronnen vallen niet onder het standaardafbeeldingsmechanisme; er wordt een fout geretourneerd als een externe afbeeldingsbron niet geldig is.

## Standaard {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

Overgenomen van `default::DefaultImage` indien niet gedefinieerd. Als deze optie is gedefinieerd, maar leeg is, wordt de standaardwerking van de afbeelding uitgeschakeld, zelfs als deze `default::DefaultImage` is gedefinieerd.

## Zie ook {#section-dc0fb4e72294442882b33a479fbc2b82}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)

---
description: Selector watermerk. Hiermee geeft u de catalogus-id op van de catalogusrecord die u wilt gebruiken als watermerkafbeelding of sjabloon.
solution: Experience Manager
title: Watermerk
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# Watermerk{#watermark}

Selector watermerk. Specifies the catalog::Id of the catalog record to be used as a watermark image or template.

Indien opgegeven, past de server het watermerk toe op de gevraagde afbeeldingsgegevens voor alle afbeeldingsaanvragen ( `req=img`).

## Eigenschappen {#section-fad6ffff4c5f4b5c8010281bc1377055}

Tekstreeks. Indien opgegeven, moet dit een geldige `Catalog::Id`-waarde zijn in deze afbeeldingscatalogus (of in de standaardcatalogus, indien opgegeven in [!DNL default.ini]).

## Standaard {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Overgenomen van `default::Watermark` indien niet gedefinieerd. Indien gedefinieerd maar leeg, wordt er geen watermerk toegepast op deze afbeeldingscatalogus, zelfs niet als `default::Watermark` is gedefinieerd.

## Zie ook {#section-f15dbe31013849828d78588742dde58e}

[catalogus::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)

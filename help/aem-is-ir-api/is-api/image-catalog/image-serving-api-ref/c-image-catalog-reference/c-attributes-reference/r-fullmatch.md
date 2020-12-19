---
description: Overeenkomende optie voor catalogi.
seo-description: Overeenkomende optie voor catalogi.
seo-title: FullMatch
solution: Experience Manager
title: FullMatch
topic: Scene7 Image Serving - Image Rendering API
uuid: 0c69ba92-1411-4cb7-ac28-d26fe035222f
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---


# FullMatch{#fullmatch}

Overeenkomende optie voor catalogi.

Een catalogusitem wordt opgegeven als een ` *`rootId`*/ *`imageId`*`-paar in HTTP-aanvragen. Bij het parseren wordt een catalogus geselecteerd als ` *`rootId`*` de `attribute::RootId` waarde van de catalogus aanpast, en het catalogusverslag wordt geïdentificeerd door ` *`imageId`*` met een `catalog::Id` waarde aan te passen. Als een catalogus wordt gevonden, maar er geen catalogusitem aanwezig is dat overeenkomt met ` *`imageId`*`, kan de server een van de volgende twee dingen doen:

Als `attribute::FullMatch` niet is ingesteld, gebruikt de server de kenmerken van de overeenkomende catalogus. In dit geval wordt ` *`rootId`*` vervangen door `attribute::RootPath` (of `default::RootPath`, indien niet opgegeven in deze catalogus).

Als `attribute::FullMatch` is ingesteld, negeert de server de catalogus volledig, alsof er geen overeenkomende catalogus is gevonden, en gaat u verder met de standaardcataloguskenmerken. In dit geval blijft ` *`rootId`*` deel uitmaken van het pad (dat wordt voorafgegaan door `default::RootPath`).

## Eigenschappen {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Markering. Stel dit in op 0 voor standaardgedrag of op 1 om gedrag bij volledige overeenkomst in te schakelen.

## Standaard {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Overgenomen van `default::FullMatch` indien niet gedefinieerd of indien leeg.

## Zie ook {#section-42da0ba53e0b4c089c62108785faf5a9}

[kenmerk::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) ,  [catalogus::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)

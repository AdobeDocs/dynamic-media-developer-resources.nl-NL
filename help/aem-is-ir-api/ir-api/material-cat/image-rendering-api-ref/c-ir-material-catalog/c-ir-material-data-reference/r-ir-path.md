---
description: Pad afbeeldingsbestand. Relatief pad en naam van een structuur- of decal-afbeeldingsbestand.
solution: Experience Manager
title: Pad *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# Pad *{#path}

Pad afbeeldingsbestand. Relatief pad en naam van een structuur- of decal-afbeeldingsbestand.

De server combineert deze waarde met `attribute::RootPath` om het daadwerkelijke pad naar het afbeeldingsbestand samen te stellen. Dit kan ook een absoluut pad zijn.

Wordt gebruikt om het bestand met de structuurafbeelding op te geven voor materiaal dat structuur, kabinet en vensterbekleding bevat, en het RGB- of RGBA-afbeeldingsbestand voor materialen voor de rand van decal en wanden. Niet voor alle materiaal met een behuizing en vensterbekleding is een aparte herhaalbare structuurafbeelding vereist.

## Eigenschappen {#section-8c12ea24f21d4472be677581893e6681}

Tekstreeks. Vereist voor textuur- en decal-materialen, facultatief voor materiaal voor de bekleding van de behuizing en het venster. Indien opgegeven, moet het een geldig relatief of absoluut bestandspad zijn. Moet leeg zijn voor effen kleurmaterialen.

## Ondersteunde bestandsindelingen {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

Renderen van afbeeldingen ondersteunt dezelfde bronafbeeldingsindelingen als Dynamic Media Image Serving.

Toepassingen waarvoor afbeeldingsgegevens in meerdere resoluties nodig zijn, presteren het beste als de indeling voor meerresolutie van de Dynamic Media piramid TIFF (PTIFF) wordt gebruikt. De Beeldserver omvat het hulpmiddel van de Omzetter van het Beeld (IC) dat tot beelden PTIFF van om het even welk gesteund formaat leidt.

Raadpleeg de beschrijving van het IC-hulpprogramma in de documentatie van Image Serving voor een volledige lijst met ondersteunde bestandsindelingen.

## Standaard {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Geen.

## Zie ook {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[IC Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ,  [attribute::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md),  [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)

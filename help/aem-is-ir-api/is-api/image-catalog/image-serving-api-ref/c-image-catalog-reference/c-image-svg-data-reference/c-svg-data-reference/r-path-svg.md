---
description: Pad
solution: Experience Manager
title: Pad
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f2d17309-c4d0-477f-a8d8-b40f05a1a60b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# Pad{#path}

De server gebruikt de regels voor padresolutie die in [Brongegevens beheren](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) om het gegevensbestand te zoeken.

## Eigenschappen {#section-72d9edc532ad43349afcb4df22e1c692}

Tekstreeks. Vereist voor afbeeldings- en SVG-records is mogelijk leeg voor sjabloonrecords. Indien gespecificeerd, moet het een geldig relatieve of absolute het dossierweg van de Server van het Beeld zijn. attribute::DefaultExt wordt toegevoegd als geen dossierachtervoegsel aanwezig is.

## Ondersteunde bestandsindelingen voor afbeeldingen {#section-8d6443c883aa48aaa00316fe9661aaa8}

Raadpleeg de beschrijving van het hulpprogramma Image Converter (IC) voor een volledige lijst met ondersteunde bestandsindelingen voor afbeeldingen.

Toepassingen waarvoor afbeeldingsgegevens in meerdere resoluties nodig zijn, presteren het best als de indeling voor meerresolutie van de Dynamic Media-piramid-TIFF (PTIFF) wordt gebruikt. Het hulpprogramma IC wordt gebruikt om PTIFF-afbeeldingen te maken in elke ondersteunde afbeeldingsindeling.

## Standaard {#section-82dad83ec3f84ae8bf2f850b4139f63e}

Geen.

## Zie ook {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[IC-hulpprogramma](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [kenmerk::RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [kenmerk::DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0), [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)

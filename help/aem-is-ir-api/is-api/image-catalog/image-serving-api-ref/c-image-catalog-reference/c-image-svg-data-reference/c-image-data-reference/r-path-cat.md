---
description: Pad afbeeldingsbestand.
solution: Experience Manager
title: Pad
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Pad{#path}

Pad afbeeldingsbestand.

Relatief of absoluut pad en naam van het bronafbeeldingsbestand dat aan deze catalogusrecord is gekoppeld. De server gebruikt de regels van de wegresolutie die in het Leiden BronGegevens worden beschreven om het gegevensdossier te vinden.

## Eigenschappen {#path-properties}

Tekstreeks. Vereist voor afbeeldingsrecords is mogelijk leeg voor sjabloonrecords. Indien gespecificeerd, moet het een geldig relatieve of absolute het dossierweg van de Server van het Beeld zijn. attribute::DefaultExt wordt toegevoegd als geen dossierachtervoegsel aanwezig is.

## Ondersteunde bestandsindelingen voor afbeeldingen {#path-supported-image-file-formats}

Raadpleeg de beschrijving van het hulpprogramma Image Converter (IC) voor een volledige lijst met ondersteunde bestandsindelingen.

Toepassingen waarvoor afbeeldingsgegevens in meerdere resoluties nodig zijn, presteren het beste als de indeling voor meerresolutie van Dynamic Media piramid TIFF (PTIFF) wordt gebruikt. Het hulpprogramma IC wordt gebruikt om PTIFF-afbeeldingen te maken in elke ondersteunde afbeeldingsindeling.

## Standaard {#path-default}

Geen.

## Zie ook {#path-seealso}

[IC-hulpprogramma](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [kenmerk::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [kenmerk::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->

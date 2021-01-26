---
description: Pad afbeeldingsbestand.
solution: Experience Manager
title: Pad
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0fca88bb-de00-4eff-83ad-c0f5e3b8ece0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Pad{#path}

Pad afbeeldingsbestand.

Relatief of absoluut pad en naam van het bronafbeeldingsbestand dat aan deze catalogusrecord is gekoppeld. De server gebruikt de regels van de wegresolutie die in het Leiden BronGegevens worden beschreven om het gegevensdossier te vinden.

## Eigenschappen {#path-properties}

Tekstreeks. Vereist voor afbeeldingsrecords is mogelijk leeg voor sjabloonrecords. Indien gespecificeerd, moet het een geldig relatieve of absolute het dossierweg van de Server van het Beeld zijn. kenmerk::DefaultExt wordt toegevoegd als er geen achtervoegsel voor het bestand aanwezig is.

## Ondersteunde bestandsindelingen {#path-supported-image-file-formats}

Raadpleeg de beschrijving van het hulpprogramma Image Converter (IC) voor een volledige lijst met ondersteunde bestandsindelingen.

Toepassingen waarvoor afbeeldingsgegevens in meerdere resoluties vereist zijn, presteren het beste als de indeling voor meerresolutie van de Dynamic Media piramid TIFF (PTIFF) wordt gebruikt. Het hulpprogramma IC wordt gebruikt om PTIFF-afbeeldingen te maken in elke ondersteunde afbeeldingsindeling.

## Standaard {#path-default}

Geen.

## Zie ook {#path-seealso}

[IC Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ,  [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) ,  [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
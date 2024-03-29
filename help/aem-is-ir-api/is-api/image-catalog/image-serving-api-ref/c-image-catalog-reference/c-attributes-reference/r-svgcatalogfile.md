---
description: Paden voor gegevensbestanden SVG. Hier geeft u de bestanden op die de SVG-gegevens voor deze catalogus bevatten.
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# SvgCatalogFile{#svgcatalogfile}

Paden voor gegevensbestanden SVG. Hier geeft u de bestanden op die de SVG-gegevens voor deze catalogus bevatten.

SVG-gegevensbestanden worden na alle bestanden met afbeeldingsgegevens in de opgegeven volgorde geladen. Indien dezelfde `catalog::Id` Deze waarde treedt op in meer dan één record (in dezelfde of in verschillende afbeeldings- of SVG-catalogusbestanden). De laatste instantie heeft voorrang.

## Eigenschappen {#section-fc2d549f76474792837b2b92ec2087ea}

Een of meer tekenreekswaarden, gescheiden door komma&#39;s. Optioneel. Elke waarde moet een absoluut bestandspad of pad zijn ten opzichte van de catalogusmap.

## Standaard {#section-a4e58951f3c249599665b823566433c9}

Leeg, wat aangeeft dat deze afbeeldingscatalogus geen SVG-gegevens bevat.

## Zie ook {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Catalogusgegevens](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29), [CatalogFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)

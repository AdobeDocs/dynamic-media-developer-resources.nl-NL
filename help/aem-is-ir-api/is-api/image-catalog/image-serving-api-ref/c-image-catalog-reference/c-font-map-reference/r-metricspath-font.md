---
description: Bestandspad voor lettertypemetriek. Pad en naam van een bestand met maatgegevens voor lettertypen, inclusief bestandsachtervoegsel.
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---


# MetricsPath{#metricspath}

Bestandspad voor lettertypemetriek. Pad en naam van een bestand met maatgegevens voor lettertypen, inclusief bestandsachtervoegsel.

Wordt gebruikt voor Adobe Type 1-lettertypen. Als deze optie niet is opgegeven, zoekt de server naar een bestand met maatgegevens voor lettertypen in dezelfde map als het hoofdlettertypebestand. Er treedt een fout op als een vereist bestand voor fontmetriek niet kan worden gevonden tijdens het renderen.

## Eigenschappen {#section-955268c581574875b05253d9e14544f3}

Tekstreeks. Optioneel voor Adobe Type 1-bestanden. Moet leeg zijn of een geldig bestandspad voor afbeeldingsserver, absoluut of relatief ten opzichte van `attribute::RootPath`.

## Standaard {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Geen.

## Zie ook {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[kenmerk::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)

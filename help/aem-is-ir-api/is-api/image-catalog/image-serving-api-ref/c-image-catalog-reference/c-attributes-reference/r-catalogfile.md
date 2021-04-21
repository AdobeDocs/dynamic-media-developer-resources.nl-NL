---
description: Paden voor afbeeldingsgegevensbestanden. Hier geeft u de bestanden op die de afbeeldingsgegevens voor deze catalogus bevatten.
solution: Experience Manager
title: CatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# CatalogFile{#catalogfile}

Paden voor afbeeldingsgegevensbestanden. Hier geeft u de bestanden op die de afbeeldingsgegevens voor deze catalogus bevatten.

Afbeeldingsgegevensbestanden worden in de opgegeven volgorde geladen. Als dezelfde `catalog::Id`-waarde voorkomt in meer dan één record (in dezelfde of in verschillende catalogusbestanden), heeft de laatste instantie voorrang.

## Eigenschappen {#section-6da55f145ecd4e31a5de52637a436983}

Een of meer tekenreekswaarden, gescheiden door komma&#39;s. Optioneel. Elke waarde moet een absoluut bestandspad of pad zijn ten opzichte van de catalogusmap.

## Standaard {#section-80f91cd7a6b2479ebb310319e9c74da7}

Leeg, wat aangeeft dat deze afbeeldingscatalogus geen afbeeldingsgegevens bevat.

## Zie ook {#section-910b67c5041d44d99a105ad43ff63a37}

[Catalogusgegevensvelden](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)

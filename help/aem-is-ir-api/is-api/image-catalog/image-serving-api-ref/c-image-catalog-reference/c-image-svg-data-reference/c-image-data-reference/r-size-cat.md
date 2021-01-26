---
description: Afbeeldingsgrootte. Pixelgrootte van de afbeelding met volledige resolutie waarnaar wordt verwezen door het cataloguspad.
seo-description: Afbeeldingsgrootte. Pixelgrootte van de afbeelding met volledige resolutie waarnaar wordt verwezen door het cataloguspad.
seo-title: Grootte
solution: Experience Manager
title: Grootte
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6fe2aeb6-0dd7-4631-955f-ad74d11b613d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# Grootte{#size}

Afbeeldingsgrootte. Pixelgrootte van de afbeelding met volledige resolutie waarnaar wordt verwezen door de catalogus::Pad.

Als deze waarde is opgegeven, gebruikt Image Serving deze optie om te voorkomen dat de afbeelding moet worden geopend om de werkelijke afbeeldingsgrootte te verkrijgen.

>[!NOTE]
>
>Als `catalog::Size`niet dezelfde is als de werkelijke afbeeldingsgrootte met volledige resolutie, kan ongedefinieerd gedrag optreden.

## Eigenschappen {#section-5c914ec8b1444a8e99d811b647cd42a3}

Twee gehele getallen, elk groter dan 0, gescheiden door een komma. Optioneel.

## Standaard {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

Als het veld niet aanwezig is of als het veld leeg is, wordt de werkelijke grootte van de afbeelding gebruikt.

## Zie ook {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalogus::Pad](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) ,  [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)

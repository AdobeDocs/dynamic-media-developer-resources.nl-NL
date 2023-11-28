---
title: Fontverwerking
description: Alle lettertypen waarnaar in de RTF-tekenreeks wordt verwezen, moeten beschikbaar zijn in het bestand met lettertypetoewijzing van de standaardcatalogus of de huidige afbeeldingscatalogus. Zoniet, dan wordt een fout geretourneerd.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e8e3ce9850ab8059aed81e720574d0c93f867a22
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Fontverwerking{#font-handling}

Alle lettertypen waarnaar in de RTF-tekenreeks wordt verwezen, moeten beschikbaar zijn in het bestand met lettertypetoewijzing van de standaardcatalogus of de huidige afbeeldingscatalogus. Zoniet, dan wordt een fout geretourneerd.

De beste kwaliteit voor cursieve en vetgedrukte tekst wordt bereikt door de desbetreffende lettertypebestanden te registreren. Als deze optie niet beschikbaar is, kan de server vette en/of cursieve lettertypen samenstellen op basis van het standaardgezicht. (Zie [kenmerk:SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

Het lettertype dat is opgegeven met `attribute::DefaultFont` wordt gebruikt wanneer geen expliciet in de RTF-tekenreeks wordt opgegeven.

Image Serving ondersteunt TrueType-, OpenType®- en Adobe Type 1-lettertypen (alleen Windows).

<!-- THIS APPEARS TO BE VERY OLD OUTDATED INFORMATION; URL IS DEAD TOO ## Photofont&reg; font support {#section-74560ae898cf4708aba4c8b4093f5f00}

Photofont&reg; fonts support `textPs=`, with the following restrictions:

* `\cf` is ignored in text spans that specify a Photofont font; Photofont font faces have predefined colors 
* Synthesized font styles are not supported; use of `\b` and `\i`require corresponding font map entries, otherwise an error is returned 

* Vertical text flow is not supported 
* Photofont fonts with 16-bit images are not supported 
* Photofont fonts with multiple glyphs per image are not supported 
* Naïve color conversion is applied unless the Photofont glyph images embed color profiles; in this case, relative colorimetric render intent and blackpoint compensation are always applied

See [https://www.photofont.com](https://www.photofont.com) for additional information. -->

## Zie ook {#section-6cb8a802aa044836bbe449d559093f3a}

[Referentie lettertypetoewijzing](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [kenmerk:SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107)

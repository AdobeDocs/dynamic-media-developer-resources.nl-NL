---
description: Alle lettertypen waarnaar in de RTF-tekenreeks wordt verwezen, moeten beschikbaar zijn in het bestand met lettertypetoewijzing van de standaardcatalogus of de huidige afbeeldingscatalogus. Als dit niet het geval is, wordt een fout geretourneerd.
seo-description: Alle lettertypen waarnaar in de RTF-tekenreeks wordt verwezen, moeten beschikbaar zijn in het bestand met lettertypetoewijzing van de standaardcatalogus of de huidige afbeeldingscatalogus. Als dit niet het geval is, wordt een fout geretourneerd.
seo-title: Fontverwerking
solution: Experience Manager
title: Fontverwerking
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6a751973-5dae-472e-a908-bf24fa59d031
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# Lettertypebehandeling{#font-handling}

Alle lettertypen waarnaar in de RTF-tekenreeks wordt verwezen, moeten beschikbaar zijn in het bestand met lettertypetoewijzing van de standaardcatalogus of de huidige afbeeldingscatalogus. Als dit niet het geval is, wordt een fout geretourneerd.

De beste kwaliteit voor cursieve en vetgedrukte tekst wordt bereikt door de desbetreffende lettertypebestanden te registreren. Als deze optie niet beschikbaar is, kan de server vette en/of cursieve lettertypen samenstellen op basis van het standaardgezicht. (Zie ` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`.)

Het lettertype dat met `attribute::DefaultFont` is opgegeven, wordt gebruikt wanneer geen lettertype expliciet in de RTF-tekenreeks is opgegeven.

Image Serving ondersteunt TrueType-, OpenType- en Adobe Type 1-lettertypen (alleen Windows).

## Ondersteuning voor Photoshop®-lettertypen {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` biedt ondersteuning voor Photoshop®-lettertypen, met de volgende beperkingen:

* `\cf` wordt genegeerd in tekstreeksen waarin een fotolettertype wordt opgegeven. Fontgezichten van fotofonts hebben vooraf gedefinieerde kleuren
* Synthesized doopvontstijlen worden niet gesteund; het gebruik van `\b` en `\i`vereisen overeenkomstige ingangen van de doopvontkaart anders een fout is teruggekeerd

* Verticale tekstdoorloop wordt niet ondersteund
* Photoshop-lettertypen met 16-bits afbeeldingen worden niet ondersteund
* Photoshop-lettertypen met meerdere glyphs per afbeelding worden niet ondersteund
* Niet-actieve kleuromzetting wordt toegepast, tenzij in de Photoshop-glyph-afbeeldingen kleurprofielen worden ingesloten. in dit geval worden altijd relatieve colorimetrische render-intentie en zwartpuntcompensatie toegepast

Raadpleeg ` [www.photofont.com](http://www.photofont.com)` voor meer informatie.

## Zie ook {#section-6cb8a802aa044836bbe449d559093f3a}

[Font Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d),  [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15),  [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107),  [ [!DNL www.photofont.com] ](http://www.photofont.com)

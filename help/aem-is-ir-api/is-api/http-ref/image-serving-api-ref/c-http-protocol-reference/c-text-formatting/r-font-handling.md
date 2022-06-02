---
title: Fontverwerking
description: Alle lettertypen waarnaar in de RTF-tekenreeks wordt verwezen, moeten beschikbaar zijn in het bestand met lettertypetoewijzing van de standaardcatalogus of de huidige afbeeldingscatalogus. Als dit niet het geval is, wordt een fout geretourneerd.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e1f0f8bdac2b7a8397adac3bb9ba38d0c519f8fb
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Fontverwerking{#font-handling}

Alle lettertypen waarnaar in de RTF-tekenreeks wordt verwezen, moeten beschikbaar zijn in het bestand met lettertypetoewijzing van de standaardcatalogus of de huidige afbeeldingscatalogus. Als dit niet het geval is, wordt een fout geretourneerd.

De beste kwaliteit voor cursieve en vetgedrukte tekst wordt bereikt door de desbetreffende lettertypebestanden te registreren. Als deze optie niet beschikbaar is, kan de server vette en/of cursieve lettertypen samenstellen op basis van het standaardgezicht. (Zie [kenmerk:SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

Het lettertype dat is opgegeven met `attribute::DefaultFont` wordt gebruikt wanneer geen expliciet in de RTF-tekenreeks wordt opgegeven.

Image Serving ondersteunt TrueType-, OpenType- en Adobe Type 1-lettertypen (alleen Windows).

## Ondersteuning van Photoshop®-lettertypen {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` biedt ondersteuning voor Photoshop®-lettertypen, met de volgende beperkingen:

* `\cf` wordt genegeerd in tekstreeksen waarin een fotolettertype wordt opgegeven. Fontgezichten van fotofonts hebben vooraf gedefinieerde kleuren
* Synthesized doopvontstijlen worden niet gesteund; gebruik van `\b` en `\i`overeenkomstige items voor fonttoewijzing vereisen, anders wordt een fout geretourneerd

* Verticale tekstdoorloop wordt niet ondersteund
* Photoshop-lettertypen met 16-bits afbeeldingen worden niet ondersteund
* Photoshop-lettertypen met meerdere glyphs per afbeelding worden niet ondersteund
* Niet-actieve kleuromzetting wordt toegepast, tenzij in de Photoshop-glyph-afbeeldingen kleurprofielen worden ingesloten. in dit geval worden altijd relatieve colorimetrische render-intentie en zwartpuntcompensatie toegepast

Zie [www.photofont.com](https://www.photofont.com) voor aanvullende informatie.

## Zie ook {#section-6cb8a802aa044836bbe449d559093f3a}

[Referentie lettertypetoewijzing](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [kenmerk:SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107), [ [!DNL www.photofont.com] ](https://www.photofont.com)

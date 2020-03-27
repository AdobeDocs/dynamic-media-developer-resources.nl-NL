---
description: Image Serving implementeert een eenvoudige visuele watermerkingsfaciliteit.
seo-description: Image Serving implementeert een eenvoudige visuele watermerkingsfaciliteit.
seo-title: Watermerken
solution: Experience Manager
title: Watermerken
topic: Scene7 Image Serving - Image Rendering API
uuid: b2bbaa59-dad9-4be3-bb92-142ed44f6d65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Watermerken{#watermarks}

Image Serving implementeert een eenvoudige visuele watermerkingsfaciliteit.

Een watermerk is doorgaans een halftransparante afbeelding, maar het kan tekst zijn of een complexere, gelaagde samengestelde afbeelding. De server plaatst het watermerk in een laag boven de antwoordafbeelding nadat alle weergavekenmerken ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) zijn toegepast.

Watermerken wordt ingeschakeld door een geldig catalogusitem in te stellen dat de watermerkafbeelding of sjabloon zou bevatten. `attribute::Watermark` Als deze optie in een benoemde catalogus `attribute::Watermark` is ingesteld, voegt de server het watermerk toe aan alle verzoeken om afbeeldingen die verwijzen naar de catalogus-id in de aanvraag-URL. Als `default::Watermark` deze optie is ingesteld (in de standaardcatalogus [!DNL default.ini]), wordt het watermerk toegepast op alle afbeeldingsaanvragen, ongeacht of er naar een catalogus wordt verwezen of niet.

De watermerken worden niet toegepast op beelden die in antwoord op duimnagelverzoeken ( `req=tmb`) en bepaalde verzoeken van kijkers Scene7 zijn teruggekeerd.

## Schalen en uitlijnen {#section-89ef9e5926ae438abbd8e70332749b76}

Wanneer een watermerk is opgegeven, genereert de server eerst de samengestelde afbeelding (de *doelafbeelding*) waarop het watermerk moet worden toegepast (voordat de weergave wordt getransformeerd). De server genereert vervolgens de samengestelde afbeelding voor het watermerk, net als elke andere afbeelding (de *watermerkafbeelding*).

In tegenstelling tot standaardafbeeldingen, `sizeN=` kan dit worden opgegeven voor laag=0 of layer=comp van de watermerkafbeelding. Hierdoor kan de watermerkafbeelding worden geschaald ten opzichte van de doelafbeelding. Als `sizeN=` deze optie niet is opgegeven, blijft de pixelgrootte van de watermerkafbeelding behouden wanneer deze wordt samengevoegd met de doelafbeelding.

Aanvraagopdrachten (zoals `fmt=`) en weergaveopdrachten (zoals `wid=`) worden genegeerd in watermerkrecords, met uitzondering van `align=`. `align=` U kunt de watermerkafbeelding gebruiken om de positie te bepalen ten opzichte van de watermerkafbeelding ten opzichte van de doelafbeelding. Hierdoor kan het watermerk ten opzichte van een hoek of rand van de doelafbeelding worden geplaatst.

Na het schalen en uitlijnen zal de server de watermerkafbeelding over de doelafbeelding plaatsen met behulp van de `blendMode=` en de `opac=` waarden die voor `layer=0` of `layer=comp` van de watermerkafbeelding zijn opgegeven. Tot slot worden de verzoek en meningsbevelen die voor het doelbeeld worden gespecificeerd toegepast om het antwoordbeeld te construeren.

De watermerkafbeelding wordt nooit groter dan een lege ruimte die door de `wid=` `hei=` opdrachten en de opdrachten aan de antwoordafbeelding wordt toegevoegd.

## Voorbeeld {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Een typisch watermerk kan bestaan uit een eenvoudige RGBA-afbeelding met een logo of copyrightvermelding. We maken een record in de afbeeldingscatalogus (of de standaardcatalogus) met de `catalog::Id` set `watermark` en geven het bestand met de watermerkafbeelding op in `catalog::Path`. We willen het watermerk uitrekken zodat het in de afbeelding past (zonder het watermerk te vervormen), maar daarbij een kleine extra marge laten, en de dekking verminderen tot 20% van het oorspronkelijke watermerk, dus we stellen `catalog::Modifier` de waarde in op `sizeN=0.9,0.9&opac=20`. Als u watermerken wilt activeren, stelt u `attribute::Watermark` de id van het item voor de watermerkcatalogus in op &quot;watermerk&quot; in dit voorbeeld. We zouden met verschillende `blendMode=` keuzes kunnen experimenteren om verschillende watermerkingseffecten te bereiken.

## Zie ook {#section-4d66713abacb42c7b6a0c93cbf966a97}

[kenmerk:Watermerk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)

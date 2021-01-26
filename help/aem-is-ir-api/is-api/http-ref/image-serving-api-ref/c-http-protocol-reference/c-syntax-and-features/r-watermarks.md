---
description: Image Serving implementeert een eenvoudige visuele watermerkingsfaciliteit.
solution: Experience Manager
title: Watermerken
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---


# Watermerken{#watermarks}

Image Serving implementeert een eenvoudige visuele watermerkingsfaciliteit.

Een watermerk is doorgaans een halftransparante afbeelding, maar het kan tekst zijn of een complexere, gelaagde samengestelde afbeelding. De server plaatst het watermerk op de antwoordafbeelding nadat alle weergavekenmerken ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) zijn toegepast.

Watermerken wordt ingeschakeld door `attribute::Watermark` in te stellen op een geldig catalogusitem dat de watermerkafbeelding of sjabloon zou bevatten. Als `attribute::Watermark` is ingesteld in een benoemde catalogus, voegt de server het watermerk toe aan alle afbeeldingsaanvragen die verwijzen naar de catalogus-id in de aanvraag-URL. Als `default::Watermark` is ingesteld (in de standaardcatalogus [!DNL default.ini]), wordt het watermerk toegepast op alle afbeeldingsaanvragen, ongeacht of ze naar een catalogus verwijzen of niet.

Watermerken worden niet toegepast op afbeeldingen die worden geretourneerd als reactie op miniatuurverzoeken ( `req=tmb`) en bepaalde verzoeken van Dynamic Media-viewers.

## Schalen en uitlijnen {#section-89ef9e5926ae438abbd8e70332749b76}

Wanneer een watermerk is opgegeven, genereert de server eerst de samengestelde afbeelding (de *doelafbeelding*) waarop het watermerk moet worden toegepast (voordat de weergave wordt getransformeerd). De server genereert vervolgens de samengestelde afbeelding voor het watermerk, net als elke andere afbeelding (de *watermerkafbeelding*).

In tegenstelling tot standaardafbeeldingen kan `sizeN=` worden opgegeven voor laag=0 of layer=comp van de watermerkafbeelding. Hierdoor kan de watermerkafbeelding worden geschaald ten opzichte van de doelafbeelding. Als `sizeN=` niet is opgegeven, behoudt de watermerkafbeelding de pixelgrootte wanneer deze wordt samengevoegd met de doelafbeelding.

Aanvraagopdrachten (zoals `fmt=`) en weergaveopdrachten (zoals `wid=`) worden genegeerd in watermerkrecords, met uitzondering van `align=`. `align=` U kunt de watermerkafbeelding gebruiken om de positie te bepalen ten opzichte van de watermerkafbeelding ten opzichte van de doelafbeelding. Hierdoor kan het watermerk ten opzichte van een hoek of rand van de doelafbeelding worden geplaatst.

Na het schalen en uitlijnen zal de server de watermerkafbeelding over de doelafbeelding plaatsen met behulp van de `blendMode=`- en `opac=`-waarden die zijn opgegeven voor `layer=0` of `layer=comp` van de watermerkafbeelding. Tot slot worden de verzoek en meningsbevelen die voor het doelbeeld worden gespecificeerd toegepast om het antwoordbeeld te construeren.

De watermerkafbeelding wordt nooit groter dan een lege ruimte die door de opdrachten `wid=` en `hei=` aan de antwoordafbeelding wordt toegevoegd.

## Voorbeeld {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Een typisch watermerk kan bestaan uit een eenvoudige RGBA-afbeelding met een logo of copyrightvermelding. We maken een record in de afbeeldingscatalogus (of de standaardcatalogus) met `catalog::Id` ingesteld op `watermark` en geven het bestand met de watermerkafbeelding op in `catalog::Path`. We willen het watermerk uitrekken zodat het past in de afbeelding van de weergave (zonder het watermerk te vervormen) en daarbij een kleine extra marge behouden. Bovendien wilt u de dekking beperken tot 20% van het oorspronkelijke watermerk. Daarom stellen we `catalog::Modifier` in op `sizeN=0.9,0.9&opac=20`. Als u watermerken wilt activeren, stelt u `attribute::Watermark` in op de id van het item voor de watermerkcatalogus, &quot;watermerk&quot; in dit voorbeeld. We kunnen met verschillende `blendMode=` keuzes experimenteren om verschillende watermerkingseffecten te bereiken.

## Zie ook {#section-4d66713abacb42c7b6a0c93cbf966a97}

[kenmerk:Watermerk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)

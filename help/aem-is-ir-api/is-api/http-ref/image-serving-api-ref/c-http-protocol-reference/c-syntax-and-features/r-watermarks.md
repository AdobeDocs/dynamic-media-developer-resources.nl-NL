---
description: Image Serving implementeert een eenvoudige visuele watermerkingsfaciliteit.
solution: Experience Manager
title: Watermerken
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Watermerken{#watermarks}

Image Serving implementeert een eenvoudige visuele watermerkingsfaciliteit.

Een watermerk is doorgaans een halftransparante afbeelding, maar het kan tekst zijn of een complexere, gelaagde samengestelde afbeelding. De server laadt het watermerk over het antwoordbeeld na alle meningsattributen ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) zijn toegepast.

Watermerken wordt ingeschakeld door de instelling `attribute::Watermark` op een geldige catalogusvermelding die de watermerkafbeelding of sjabloon zou bevatten. Indien `attribute::Watermark` wordt ingesteld in een benoemde catalogus, voegt de server het watermerk toe aan alle afbeeldingsaanvragen die verwijzen naar de catalogus-id in de aanvraag-URL. Indien `default::Watermark` is ingesteld (in de standaardcatalogus, [!DNL default.ini]), wordt het watermerk toegepast op alle afbeeldingsaanvragen, ongeacht of er naar een catalogus wordt verwezen.

Watermerken worden niet toegepast op afbeeldingen die worden geretourneerd als reactie op miniatuurverzoeken ( `req=tmb`) en bepaalde verzoeken van Dynamic Media-viewers.

## Schalen en uitlijnen {#section-89ef9e5926ae438abbd8e70332749b76}

Wanneer een watermerk is opgegeven, genereert de server eerst de samengestelde afbeelding (de *doelafbeelding*) waarop het watermerk moet worden toegepast (voordat de weergave wordt getransformeerd). De server genereert vervolgens de samengestelde afbeelding voor het watermerk, net als elke andere afbeelding (de *watermerkafbeelding*).

In tegenstelling tot standaardafbeeldingen, `sizeN=` kan worden opgegeven voor laag=0 of layer=comp van de watermerkafbeelding. Hierdoor kan de watermerkafbeelding worden geschaald ten opzichte van de doelafbeelding. Indien `sizeN=` niet is opgegeven, behoudt de watermerkafbeelding de pixelgrootte wanneer deze wordt samengevoegd met de doelafbeelding.

Aanvraag (zoals `fmt=`) en weergaveopdrachten (zoals `wid=`) worden genegeerd in watermerkrecords, behalve `align=`. `align=` U kunt de watermerkafbeelding gebruiken om de positie te bepalen ten opzichte van de watermerkafbeelding ten opzichte van de doelafbeelding. Hierdoor kan het watermerk ten opzichte van een hoek of rand van de doelafbeelding worden geplaatst.

Na het schalen en uitlijnen, lagen de server de watermerkafbeelding over het doelbeeld gebruikend `blendMode=` en `opac=` opgegeven waarden voor `layer=0` of `layer=comp` van de watermerkafbeelding. Tot slot worden de verzoek en meningsbevelen die voor het doelbeeld worden gespecificeerd toegepast om het antwoordbeeld te construeren.

De watermerkafbeelding wordt nooit uitgebreid over een lege ruimte die door de `wid=` en `hei=` opdrachten.

## Voorbeeld {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Een typisch watermerk kan bestaan uit een eenvoudige RGBA-afbeelding met een logo of copyrightvermelding. We maken een record in de afbeeldingscatalogus (of de standaardcatalogus) met `catalog::Id` instellen op `watermark` en geeft u het bestand met de watermerkafbeelding op in `catalog::Path`. We willen het watermerk uitrekken zodat het in de afbeelding past (zonder het watermerk te vervormen) en daarbij een kleine extra marge laten. De dekking wordt verminderd tot 20% van het oorspronkelijke watermerk. Daarom stellen we `catalog::Modifier` tot `sizeN=0.9,0.9&opac=20`. Als u watermerken wilt activeren, stelt u `attribute::Watermark` aan de id van het item in de watermerkcatalogus: &quot;watermerk&quot; in dit voorbeeld. We willen misschien experimenteren met andere `blendMode=` keuzes om verschillende watermerkingseffecten te bereiken.

## Zie ook {#section-4d66713abacb42c7b6a0c93cbf966a97}

[kenmerk:Watermerk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)

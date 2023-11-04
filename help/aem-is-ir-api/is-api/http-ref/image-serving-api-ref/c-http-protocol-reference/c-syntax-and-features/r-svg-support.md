---
description: Afbeeldingsserver ondersteunt SVG-bestanden (Scalable Vector Graphics) als brongegevens. Conformiteit met SVG 1.1 is vereist.
solution: Experience Manager
title: SVG-ondersteuning
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# SVG-ondersteuning{#svg-support}

Afbeeldingsserver ondersteunt SVG-bestanden (Scalable Vector Graphics) als brongegevens. Conformiteit met SVG 1.1 is vereist.

De functie Afbeeldingsserver herkent alleen statische inhoud van de SVG. Animaties, scripts en andere interactieve inhoud worden niet ondersteund.

SVG kan worden opgegeven wanneer afbeeldingsbestanden zijn toegestaan (URL-pad). `src=`, en `mask=`). Nadat de inhoud van het SVG-bestand is gerasterd, wordt het net als een afbeelding verwerkt.

Net als bij afbeeldingen kunnen SVG-bestanden worden opgegeven als afbeeldingscatalogus-items of als relatieve bestandspaden.

## Vervangende variabelen {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` vervangende variabelen kunnen in het SVG-bestand worden opgenomen in de waardetekenreeksen `<text>` elementen en alle elementkenmerken.

De belangrijke Variabelen in het vraaggedeelte van ingebedde Beeld die verzoeken dienen worden niet direct vervangen. In plaats daarvan, worden alle beschikbare veranderlijke definities toegevoegd aan het verzoek, dat Beeld dat variabelen toestaat om te vervangen wanneer het ontleden van het verzoek.

Zie [Substitutievariabelen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) voor aanvullende informatie.

## Verwijzingen naar afbeeldingen {#section-a7680f9e6aca4b1a83560637cc9fac66}

Afbeeldingen kunnen in SVG worden ingevoegd met de `<image>` element. Afbeeldingen waarnaar wordt verwezen door de `xlink::href` kenmerk van de `<image>` element must be valid image serving request. Externe URL&#39;s zijn niet toegestaan.

Geef een volledige aanvraag voor de afbeeldingenservice op, te beginnen met `http://`of een relatieve URL, beginnend met `/is/image`. Wanneer een volledig HTTP-pad is opgegeven, wordt de domeinnaam uit het pad verwijderd en omgezet in de relatieve indeling. Het gebruik van een volledig HTTP-pad kan een voordeel opleveren, omdat het bestand dan kan worden voorvertoond met een SVG-renderer van een andere fabrikant.

>[!NOTE]
>
>Er is slechts beperkte ondersteuning voor het renderen van afbeeldingen in deze versie van Image Serving. Verwijzen naar afbeeldingen vanuit de SVG mag alleen worden gebruikt in situaties waarin traditionele lagen en sjabloonmechanismen voor beeldbewerking onvoldoende zijn om het gewenste resultaat te bereiken. In geen geval mag SVG worden gebruikt om composieten met meerdere afbeeldingen te genereren.

>[!NOTE]
>
>Afbeeldingen die zijn ingesloten in SVG, worden momenteel niet automatisch aangepast. Zorg ervoor dat alle afbeeldingsvoorkeuren de vereiste opdrachten in de afbeeldingsserver bevatten om de gewenste afbeeldingsgrootte in te stellen (bijvoorbeeld `wid=`). Als de afbeeldingsgrootte niet expliciet wordt ingesteld, `attribute::DefaultPix` wordt toegepast.

## Kleurbeheer {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Alle kleurwaarden die zijn ingesloten in SVG-bestanden en die via vervangende variabelen worden doorgegeven aan SVG-sjablonen, worden verondersteld te bestaan in de `sRgb` kleurruimte.

Er wordt geen kleuromzetting uitgevoerd wanneer afbeeldingen in de SVG worden ingesloten. Voor kleurgetrouwheid moet u opgeven `icc=sRgb` voor alle ingesloten afbeeldingsaanvragen.

Na het rasteren neemt de SVG-afbeelding net als elke andere afbeelding deel aan kleurbeheer.

## Voorbeeld {#section-036cdd45abd449849ee00a8f21788c28}

In de volgende SVG-sjabloon worden verwijzingen naar afbeeldingen en het gebruik van variabelen geïllustreerd.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Deze SVG-sjabloon kan als volgt worden gebruikt:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Beperkingen {#section-daa5eccd07204aaf993be41e87822d54}

SVG-bestanden moeten zelfstandig zijn en mogen niet verwijzen naar secundaire bestanden of bronnen, met uitzondering van externe afbeeldingen waarnaar wordt verwezen met verzoeken om beeldbewerking of het renderen van afbeeldingen (zie hierboven).

Alleen statische inhoud wordt weergegeven. Animatie, interactieve functies, zoals knoppen, enzovoort. kan aanwezig zijn, maar kan niet worden teruggegeven zoals verwacht.

ICC-kleurspecificaties op basis van profielen worden momenteel niet ondersteund.

`<script>` elementen kunnen aanwezig zijn, maar worden altijd genegeerd.

## Zie ook {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [SVG 1.1 Specificatie](https://www.w3.org/TR/SVG11/)

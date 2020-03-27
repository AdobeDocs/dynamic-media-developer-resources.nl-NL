---
description: De server van het beeld steunt Scalable VectorGrafieken (SVG) dossiers als brongegevens. Conformiteit met SVG 1.1 is vereist.
seo-description: De server van het beeld steunt Scalable VectorGrafieken (SVG) dossiers als brongegevens. Conformiteit met SVG 1.1 is vereist.
seo-title: SVG-ondersteuning
solution: Experience Manager
title: SVG-ondersteuning
topic: Scene7 Image Serving - Image Rendering API
uuid: 30d7b37d-fdef-4518-a4b3-4baee56fa634
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SVG-ondersteuning{#svg-support}

De server van het beeld steunt Scalable VectorGrafieken (SVG) dossiers als brongegevens. Conformiteit met SVG 1.1 is vereist.

De Beeldserver herkent slechts statische inhoud SVG; animaties, scripts en andere interactieve inhoud worden niet ondersteund.

SVG kan worden opgegeven wanneer afbeeldingsbestanden zijn toegestaan (URL-pad, `src=`en `mask=`). Nadat de inhoud van het SVG-bestand is gerasterd, wordt het net als een afbeelding verwerkt.

SVG-bestanden kunnen net als afbeeldingen worden opgegeven als afbeeldingscatalogusitems of als relatieve bestandspaden.

## Vervangende variabelen {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` substitutievariabelen kunnen in het SVG-bestand worden opgenomen in de elementen van waardetekenreeksen en in elk elementkenmerk. `<text>`

De belangrijke Variabelen in het vraaggedeelte van ingebedde Beeld die verzoeken dienen worden niet direct vervangen. In plaats daarvan, worden alle beschikbare veranderlijke definities toegevoegd aan het verzoek, dat Beeld dat variabelen toestaat om te vervangen wanneer het ontleden van het verzoek.

Zie [Vervangende Variabelen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) voor meer informatie.

## Verwijzingen naar afbeeldingen {#section-a7680f9e6aca4b1a83560637cc9fac66}

Afbeeldingen kunnen in SVG worden ingevoegd met behulp van het `<image>` element. Afbeeldingen waarnaar wordt verwezen door het `xlink::href` kenmerk van het `<image>` element, moeten geldige aanvragen voor afbeeldingsserving zijn. Externe URL&#39;s zijn niet toegestaan.

Geef een volledige aanvraag voor de afbeeldingsserver op, te beginnen met `http://`, of een relatieve URL, te beginnen met `/is/image`. Als een volledig HTTP-pad is opgegeven, wordt de domeinnaam uit het pad verwijderd en omgezet in de relatieve indeling. Het gebruik van een volledig HTTP-pad kan voordelen hebben, omdat het bestand dan kan worden voorvertoond met een externe SVG-renderer.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Er is slechts beperkte ondersteuning voor het renderen van afbeeldingen in deze versie van Image Serving. Verwijzen naar afbeeldingen vanuit SVG mag alleen worden gebruikt in situaties waarin traditionele lagen en sjabloonmechanismen voor beeldbewerking onvoldoende zijn om het gewenste resultaat te bereiken. SVG mag in geen geval worden gebruikt om composities met meerdere afbeeldingen te genereren.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Afbeeldingen die zijn ingesloten in SVG, worden momenteel niet automatisch aangepast. Zorg ervoor dat alle beeldverwijzingen de noodzakelijke bevelen van de Beeldserver van het Beeld omvatten om de gewenste beeldgrootte (b.v. `wid=`). Als de afbeeldingsgrootte niet expliciet wordt ingesteld, `attribute::DefaultPix` wordt deze toegepast.

## Kleurbeheer {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Alle kleurwaarden die zijn ingesloten in SVG-bestanden en via vervangingsvariabelen worden doorgegeven aan SVG-sjablonen, worden verondersteld te bestaan in de `sRgb` kleurruimte.

Er wordt geen kleuromzetting uitgevoerd wanneer afbeeldingen worden ingesloten in de SVG. Voor kleurgetrouwheid moet u alle aanvragen voor ingesloten afbeeldingen opgeven. `icc=sRgb`

Na het rasteren neemt de SVG-afbeelding net als elke andere afbeelding deel aan kleurbeheer.

## Voorbeeld {#section-036cdd45abd449849ee00a8f21788c28}

De volgende SVG-sjabloon illustreert verwijzingen naar afbeeldingen en het gebruik van variabelen.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Deze SVG-sjabloon kan als volgt worden gebruikt:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Beperkingen {#section-daa5eccd07204aaf993be41e87822d54}

SVG-bestanden moeten zelfstandig zijn en mogen niet verwijzen naar secundaire bestanden of bronnen, met uitzondering van externe afbeeldingen waarnaar wordt verwezen met verzoeken om beeldbewerking of het renderen van afbeeldingen (zie hierboven).

Alleen statische inhoud wordt gerenderd. Animatie, interactieve functies, zoals knoppen, enz. kan aanwezig zijn, maar kan niet worden teruggegeven zoals verwacht.

ICC-kleurspecificaties op basis van profielen worden momenteel niet ondersteund.

`<script>` elementen kunnen aanwezig zijn, maar worden altijd genegeerd.

## Zie ook {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), de Specificatie van [SVG 1.1](http://www.w3.org/TR/SVG11/)

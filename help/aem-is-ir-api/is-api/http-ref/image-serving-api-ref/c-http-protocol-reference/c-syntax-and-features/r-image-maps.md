---
description: IS biedt mechanismen om het gebruik van HTML-afbeeldingen met hyperlinks te vereenvoudigen. De op JAVA gebaseerde en op Flash gebaseerde viewers in IS bieden ook beperkte ondersteuning voor afbeeldingen met hyperlinks.
seo-description: IS biedt mechanismen om het gebruik van HTML-afbeeldingen met hyperlinks te vereenvoudigen. De op JAVA gebaseerde en op Flash gebaseerde viewers in IS bieden ook beperkte ondersteuning voor afbeeldingen met hyperlinks.
seo-title: Afbeeldingen met hyperlinks
solution: Experience Manager
title: Afbeeldingen met hyperlinks
topic: Scene7 Image Serving - Image Rendering API
uuid: 2b7b620b-712b-4110-ba38-993a354c09d3
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---


# Afbeeldingen met hyperlinks{#image-maps}

IS biedt mechanismen om het gebruik van HTML-afbeeldingen met hyperlinks te vereenvoudigen. De op JAVA gebaseerde en op Flash gebaseerde viewers in IS bieden ook beperkte ondersteuning voor afbeeldingen met hyperlinks.

De bronbeeldkaarten worden verstrekt aan IS of via `catalog::Map` of met `map=` bevel, en de verwerkte kaarten worden teruggewonnen gebruikend `req=map` bevel.

Een afbeelding met hyperlinks bestaat uit een of meer HTML-GEBIEDEN-elementen, op de juiste wijze gescheiden met &#39;&lt;&#39; en &#39;>&#39;. Indien beschikbaar via catalog::Map, worden alle pixelcoördinaatwaarden verondersteld in de oorspronkelijke afbeeldingsresolutie te staan en relatief ten opzichte van de linkerbovenhoek van de (ongewijzigde) bronafbeelding. Wanneer de coördinaatwaarden via de opdracht `map=` worden opgegeven, worden deze als laagcoördinaten ten opzichte van de linkerbovenhoek van de laag beschouwd (na `rotate=` en `extend=`).

>[!NOTE]
>
>%-coördinaten zijn momenteel niet toegestaan en kunnen onjuist worden verwerkt.

IS produceert een samengestelde beeldkaart van de bronbeeldkaarten van elke samenstellende laag door de ruimtelijke transformaties (zoals schrapen en omwenteling) op de kaartcoördinaten toe te passen, en dan de verwerkte laagkaarten in de aangewezen z-orde (voor aan achter) en met het aangewezen plaatsen samen te stellen.

De volgende opdrachten worden overwogen voor het verwerken van afbeeldingen met hyperlinks wanneer deze worden aangeboden in combinatie met `req=map` (rechtstreeks in de aanvraag, via catalogussjablonen of in `catalog::Modifier` tekenreeksen):

* `align=`
* `wid=`
* `hei=`
* `scl=`
* `crop=`
* `flip=`
* `rotate=`
* `scale=`
* `layer=`
* `size=`
* `extend=`
* `origin=`
* `pos=`
* `anchor=`
* `src=`
* `map=`

Alle andere opdrachten worden genegeerd.

De `SHAPE` en `COORDS` attributen van een `AREA` kunnen tijdens verwerking van een `req=map` verzoek worden gewijzigd, worden alle andere attributen van het `AREA` element overgegaan zonder wijziging. In de meeste gevallen betekent dit dat de `SHAPE`-waarde wordt gewijzigd van `DEFAULT` in `RECT` (dit zou ook het `COORDS`-kenmerk toevoegen) of dat de `COORDS`-waarden worden gewijzigd.

`AREA` elementen die tijdens de verwerking leeg worden, worden volledig verwijderd. Als een kaart aan `layer=comp` wordt geassocieerd wordt het geplaatst achter alle andere kaarten. De gegevens worden als of meer HTML `AREA`-elementen in tekstvorm geretourneerd. Een lege antwoordtekenreeks geeft aan dat er geen afbeelding met hyperlinks bestaat voor de opgegeven objecten.

Laagtransparantie wordt niet in overweging genomen bij kaartverwerking. Aan een volledig transparante laag kan nog steeds een afbeelding met hyperlinks zijn gekoppeld. De kaart van een gedeeltelijk transparante laag wordt niet geknipt naar de transparante gebieden.

## Zie ook {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) ,  [catalogus::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md),  [HTML 4.01-specificatie](http://www.w3.org/TR/html401/)

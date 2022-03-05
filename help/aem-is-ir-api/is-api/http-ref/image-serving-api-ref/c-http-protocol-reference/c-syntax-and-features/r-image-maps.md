---
description: IS biedt mechanismen om het gebruik van afbeeldingen met HTML-afbeeldingen te vereenvoudigen. De op JAVA gebaseerde en op Flash gebaseerde viewers in IS bieden ook beperkte ondersteuning voor afbeeldingen met hyperlinks.
solution: Experience Manager
title: Afbeeldingen met hyperlinks
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9a685f9d-205d-43b3-b5fe-3ae324fe153e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Afbeeldingen met hyperlinks{#image-maps}

IS biedt mechanismen om het gebruik van afbeeldingen met HTML-afbeeldingen te vereenvoudigen. De op JAVA gebaseerde en op Flash gebaseerde viewers in IS bieden ook beperkte ondersteuning voor afbeeldingen met hyperlinks.

Bronafbeeldingen met hyperlinks worden via `catalog::Map` of met de `map=` en verwerkte kaarten worden opgehaald met de opdracht `req=map` gebruiken.

Een afbeelding met hyperlinks bestaat uit een of meer HTML AREA-elementen, op de juiste wijze gescheiden met &#39;&lt;&#39; en &#39;>&#39;. Indien beschikbaar via catalog::Map, worden alle pixelcoördinaatwaarden verondersteld in de oorspronkelijke afbeeldingsresolutie te staan en relatief ten opzichte van de linkerbovenhoek van de (ongewijzigde) bronafbeelding. Indien verstrekt via een `map=` gebruiken, worden de coördinaatwaarden als laagcoördinaten beschouwd, relatief ten opzichte van de linkerbovenhoek van de laag (na `rotate=` en `extend=`).

>[!NOTE]
>
>%-coördinaten zijn momenteel niet toegestaan en kunnen onjuist worden verwerkt.

IS produceert een samengestelde beeldkaart van de bronbeeldkaarten van elke samenstellende laag door de ruimtelijke transformaties (zoals schrapen en omwenteling) op de kaartcoördinaten toe te passen, en dan de verwerkte laagkaarten in de aangewezen z-orde (voor aan achter) en met het aangewezen plaatsen samen te stellen.

De volgende opdrachten worden overwogen voor het verwerken van afbeeldingen met hyperlinks, mits deze opdrachten worden gecombineerd met `req=map` (rechtstreeks in de aanvraag, via catalogussjablonen of in `catalog::Modifier` tekenreeksen):

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

De `SHAPE` en `COORDS` kenmerken van een `AREA` kan tijdens de verwerking van een `req=map` verzoek, alle andere kenmerken van de `AREA` -element worden zonder wijzigingen doorgegeven. In de meeste gevallen betekent dit dat de `SHAPE` waarde van `DEFAULT` tot `RECT` (hiermee wordt ook de `COORDS` (kenmerk), of het wijzigen van `COORDS` waarden.

Alle `AREA` elementen die tijdens de verwerking leeg raken, worden volledig verwijderd. Als een kaart is gekoppeld aan `layer=comp` het wordt achter alle andere kaarten geplaatst. De gegevens worden in tekstvorm één als of meer HTML geretourneerd `AREA` elementen. Een lege antwoordtekenreeks geeft aan dat er geen afbeelding met hyperlinks bestaat voor de opgegeven objecten.

Laagtransparantie wordt niet in overweging genomen bij kaartverwerking. Aan een volledig transparante laag kan nog steeds een afbeelding met hyperlinks zijn gekoppeld. De kaart van een gedeeltelijk transparante laag wordt niet geknipt naar de transparante gebieden.

## Zie ook {#see-also}

[map=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md#reference-8f96545f196b4b7caa616e15c2363f06) , [catalogus::Kaart](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [HTML 4.01 Specificatie](https://www.w3.org/TR/html401/)

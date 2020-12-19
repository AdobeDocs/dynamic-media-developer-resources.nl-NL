---
description: Afbeelding roteren. Hiermee roteert u de afbeelding, tekst of effen kleurlaag met de opgegeven hoek.
seo-description: Afbeelding roteren. Hiermee roteert u de afbeelding, tekst of effen kleurlaag met de opgegeven hoek.
seo-title: roteren
solution: Experience Manager
title: roteren
topic: Scene7 Image Serving - Image Rendering API
uuid: 160d3c4b-3871-43bd-a17d-96198c7ea839
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# roteren{#rotate}

Afbeelding roteren. Hiermee roteert u de afbeelding, tekst of effen kleurlaag met de opgegeven hoek.

`rotate= *`hoek`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> hoek</span> </p> </td> 
  <td class="stentry"> <p>Rotatiehoek in graden (reëel). </p></td> 
 </tr> 
</table>

Positieve hoeken roteren rechtsom. Het laagankerpunt ( `anchor=` of `catalog::Anchor`) fungeert als het middelpunt van de rotatie. De laagrechthoek wordt zo nodig vergroot en rondom de geroteerde gegevens geplaatst om uitsnijden te voorkomen. Rotatie wordt toegepast nadat het achtergrondgebied van de laag is gevuld met `color=`. `bgColor=` U kunt achtergrondkleur toevoegen aan het selectiekader na het roteren.

## Eigenschappen {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

Laag, opdracht. Wordt toegepast op de huidige laag of op laag 0 als `layer=comp`. Genegeerd door effectlagen.

## Standaard {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, voor geen rotatie.

## Voorbeeld {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

Plaats een label &#39;&#39;Aan-verkoop&#39;&#39; in de linkerbovenhoek van afbeeldingen in een afbeeldingscatalogus. De grootte van de labelafbeelding is al correct voor de weergave van 300 x 300 en moet 30 graden naar links worden gedraaid. Vul het tekstvak met een witte, semi-dekkende kleur om het label te verfraaien.

`http:// *`server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

`size=` wordt toegepast op laag 0 om de weergavegrootte in te stellen in plaats van `wid=` en `hei=` te gebruiken. Hierdoor kan de grootte van `myImageId` worden aangepast zonder de uiteindelijke grootte van `labelImage` te wijzigen. Ook `scl=1` moet worden opgegeven, anders kan de samengestelde afbeelding worden geschaald naar `attribute::DefaultPix` (tenzij die is ingesteld op 0,0). `color=` Hiermee voegt u vóór de rotatie de halfdekkende achtergrondkleur toe aan het tekstvak.

De oorsprong van beide lagen wordt ingesteld op de linkerbovenhoek om de gewenste uitlijning te verkrijgen. Het oorsprongpunt voor laag 1 is van toepassing op `labelImage`nadat deze is geroteerd.

Zie [Voorbeeld A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) voor een voorbeeld van geroteerde tekst.

## Zie ook {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab),  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)

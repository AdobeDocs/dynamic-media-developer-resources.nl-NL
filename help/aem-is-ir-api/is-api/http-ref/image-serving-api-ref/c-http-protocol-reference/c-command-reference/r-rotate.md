---
title: roteren
description: Afbeelding roteren. Hiermee roteert u de afbeelding, tekst of effen kleurlaag met de opgegeven hoek.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# roteren{#rotate}

Afbeelding roteren. Hiermee roteert u de afbeelding, tekst of effen kleurlaag met de opgegeven hoek.

`rotate= *`hoek`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> hoek</span> </p> </td> 
  <td class="stentry"> <p>Rotatiehoek in graden (echt). </p></td> 
 </tr> 
</table>

Positieve hoeken roteren rechtsom. Het laagankerpunt ( `anchor=` of `catalog::Anchor`) fungeert als rotatiecentrum. De laagrechthoek wordt zo nodig vergroot en rondom de geroteerde gegevens geplaatst om uitsnijden te voorkomen. Rotatie wordt toegepast nadat het achtergrondgebied van de laag is gevuld met `color=`. De optie `bgColor=` U kunt achtergrondkleur toevoegen aan het selectiekader na het roteren.

## Eigenschappen {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

Laag, opdracht. Is van toepassing op de huidige laag of op laag 0 als `layer=comp`. Genegeerd door effectlagen.

## Standaard {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, voor geen rotatie.

## Voorbeeld {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

Plaats een label &#39;&#39;Aan-verkoop&#39;&#39; in de linkerbovenhoek van afbeeldingen in een afbeeldingscatalogus. De grootte van de labelafbeelding is al correct voor de weergave van 300 x 300 en moet 30° naar links worden gedraaid. Als u het label wilt verfraaien, vult u het tekstvak met een witte, halfdekkende kleur.

`http:// *`server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

Toepassen `size=` op laag 0 om de weergavegrootte in te stellen in plaats van te gebruiken `wid=` en `hei=`. Deze methode staat `myImageId` te vergroten of verkleinen zonder de uiteindelijke grootte van `labelImage`. Geef ook `scl=1`anders kan de samengestelde afbeelding worden geschaald naar `attribute::DefaultPix` (tenzij dit op 0,0 is ingesteld). De optie `color=` Hiermee voegt u vóór de rotatie de halfdekkende achtergrondkleur toe aan het tekstvak.

De oorsprong van beide lagen wordt ingesteld op de linkerbovenhoek om de gewenste uitlijning te verkrijgen. Het oorsprongpunt voor laag 1 is van toepassing op `labelImage`nadat deze is gedraaid.

Zie [Voorbeeld A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Sjablonen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) voor een voorbeeld van geroteerde tekst.

## Zie ook {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)

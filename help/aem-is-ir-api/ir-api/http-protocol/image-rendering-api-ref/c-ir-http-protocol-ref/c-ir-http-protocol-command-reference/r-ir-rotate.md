---
description: Materiaalrotatiehoek. Hiermee definieert u de rotatiehoek voor materialen.
seo-description: Materiaalrotatiehoek. Hiermee definieert u de rotatiehoek voor materialen.
seo-title: roteren
solution: Experience Manager
title: roteren
topic: Scene7 Image Serving - Image Rendering API
uuid: 497cd8ea-c6a4-45d2-b5e0-0898ac00913d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# roteren{#rotate}

Materiaalrotatiehoek. Hiermee definieert u de rotatiehoek voor materialen.

` rotate= *`hoek`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> hoek  </span> </p> </td> 
  <td class="stentry"> <p>Rotatiehoek in graden (reëel). </p> </td> 
 </tr> 
</table>

Roteer herhaalbare structuurmaterialen (met uitzondering van achtergronden) met veelvouden van 45 graden wanneer deze worden toegepast op vlakke objecten of vlakke objecten.

Roteer herhaalbare structuurmaterialen met willekeurige hoeken wanneer deze worden toegepast op Stroomlijn- en Schetsobjecten.

Decale materialen roteren met willekeurige hoeken.

Positieve hoeken roteren rechtsom. De structuur of het decal wordt geroteerd rond het ankerpunt ( `anchor=`); het ankerpunt blijft uitgelijnd op de oorsprong van het doelobject.

## Eigenschappen {#section-ad4d07897ca24f63af1a4062f8618e36}

Materiaalkenmerk. Genegeerd door vaste kleuren, achtergrond, kast en vensterbehandelingsmaterialen. *`angle`* moet een veelvoud van 45 zijn voor herhaalbare structuren, tenzij toegepast op Stroomlijn- of Schetsobjecten.

## Standaard {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, voor geen rotatie.

## Zie ook {#section-f73c00e9368b478dac1fd15bb4367a12}

[anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)

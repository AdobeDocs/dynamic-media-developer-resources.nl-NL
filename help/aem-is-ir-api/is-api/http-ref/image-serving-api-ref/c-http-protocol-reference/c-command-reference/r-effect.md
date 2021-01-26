---
description: Selecteer Effectlaag. Selecteert een effect laag en begint een nieuw laagsegment in het verzoekkoord, dat met de huidige laag wordt geassocieerd.
seo-description: Selecteer Effectlaag. Selecteert een effect laag en begint een nieuw laagsegment in het verzoekkoord, dat met de huidige laag wordt geassocieerd.
seo-title: effect
solution: Experience Manager
title: effect
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 622dc7ca-55b8-4a82-b9a7-65588aee87d0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# effect{#effect}

Selecteer Effectlaag. Selecteert een effect laag en begint een nieuw laagsegment in het verzoekkoord, dat met de huidige laag wordt geassocieerd.

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>Aantal effectlagen (int niet gelijk aan 0). </p></td> 
 </tr> 
</table>

Alle bevelen binnen het nieuwe segment worden toegepast op de gespecificeerde effect laag. Een segment van de effectlaag wordt geëindigd door volgende `layer=` of `effect=` bevel of tegen het eind van het verzoek.

*`n`* moet kleiner zijn dan 0 voor buitenlaageffecten (d.w.z. effecten achter de bovenliggende laag) en groter dan 0 voor binnenlaageffecten (d.w.z. effecten binnen de bovenliggende laag). Effectlaagnummers hoeven niet opeenvolgend te zijn.

Het aantal van de effect laag specificeert de z-orde, in het geval van veelvoudige effect lagen voor de zelfde ouderlaag. De lagen met een hoger nummer worden boven op de lagen met een lager nummer geplaatst.

Effectlagen kunnen worden gekoppeld aan `layer=comp`.

## Eigenschappen {#section-e11f795deff345779ce280a82cf221ca}

Effectlaag, opdracht. *`n`* mag niet 0 zijn.

## Standaard {#section-84bbe1cfe7a94040827c994323ac59d4}

Geen.

## Voorbeeld {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## Zie ook {#section-573273e9e0e64103a5764075f5e50180}

` [layer=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md#reference-0f8d7fbef64841dd855917bd8fc22e6d)`

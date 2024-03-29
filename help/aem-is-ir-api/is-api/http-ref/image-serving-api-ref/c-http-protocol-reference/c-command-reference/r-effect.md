---
title: effect
description: Selecteer Effectlaag. Selecteert een effect laag en begint een nieuw laagsegment in het verzoekkoord, dat met de huidige laag wordt geassocieerd.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '178'
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

Alle bevelen binnen het nieuwe segment worden toegepast op de gespecificeerde effect laag. Een segment van de effectlaag wordt geëindigd door volgende `layer=` of `effect=` of aan het einde van de aanvraag.

De waarde *`n`* moet kleiner zijn dan 0 voor buitenlaageffecten (dat wil zeggen effecten achter de bovenliggende laag) en groter dan 0 voor binnenlaageffecten (dat wil zeggen, effecten binnen de bovenliggende laag). Effectlaagnummers hoeven niet opeenvolgend te zijn.

Het effect laagaantal specificeert de z-orde, als er veelvoudige effect lagen voor de zelfde ouderlaag zijn. De lagen met een hoger nummer worden boven op de lagen met een lager nummer geplaatst.

Effectlagen kunnen worden gekoppeld aan `layer=comp`.

## Eigenschappen {#section-e11f795deff345779ce280a82cf221ca}

Effectlaag, opdracht. De waarde *`n`* mag niet 0 zijn.

## Standaard {#section-84bbe1cfe7a94040827c994323ac59d4}

Geen.

## Voorbeeld {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## Zie ook {#section-573273e9e0e64103a5764075f5e50180}

[layer=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)

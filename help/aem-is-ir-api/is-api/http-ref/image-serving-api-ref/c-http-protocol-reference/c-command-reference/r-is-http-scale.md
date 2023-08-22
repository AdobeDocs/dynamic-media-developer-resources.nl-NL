---
title: schalen
description: Afbeelding schalen. Hiermee schaalt u de bronafbeelding van een laag met factor ten opzichte van de afbeelding met volledige resolutie.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# schalen{#scale}

Afbeelding schalen. Hiermee schaalt u de bronafbeelding van een laag met factor ten opzichte van de afbeelding met volledige resolutie.

`scale= *`factor`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> factor</span> </p> </td> 
  <td class="stentry"> <p>Schaalfactor (reëel, groter dan 0,0). </p></td> 
 </tr> 
</table>

Er wordt geen schaling toegepast wanneer `scale=1`. *`factor`* Als de bronafbeelding kleiner is dan 1,0 en groter dan 1,0, wordt deze vergroot.

## Eigenschappen {#section-3c7eb45527394fe79b1ddba6c1fcca09}

Kenmerk van bronafbeelding/masker. Genegeerd als `size=` wordt ook opgegeven voor de huidige laag. Overschrijvingen `res=`. Is van toepassing op laag 0 indien opgegeven voor `layer=comp`. Genegeerd als de laag niet aan een afbeelding of masker is gekoppeld.

## Standaard {#section-26e64904362342a5a62c5f6598f330c4}

Indien niet opgegeven, `res=` wordt gebruikt. Indien `res=` niet is opgegeven, wordt de afbeelding gebruikt zonder schalen.

## Zie ook {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)

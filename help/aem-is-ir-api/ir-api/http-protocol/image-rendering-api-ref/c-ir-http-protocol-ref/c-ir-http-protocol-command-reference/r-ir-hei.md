---
description: Hoogte van afbeelding beantwoorden. Geeft aan dat de gerenderde afbeelding wordt geschaald, zodat de hoogte van de antwoordafbeelding niet groter is dan de opgegeven waarde, terwijl de hoogte-breedteverhouding van de afbeelding behouden blijft.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# hei{#hei}

Hoogte van afbeelding beantwoorden. Geeft aan dat de gerenderde afbeelding wordt geschaald, zodat de hoogte van de antwoordafbeelding niet groter is dan de opgegeven waarde, terwijl de hoogte-breedteverhouding van de afbeelding behouden blijft.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Hoogte van afbeelding beantwoorden in pixels (geheel getal groter dan 0). </p></td> 
 </tr> 
</table>

De afbeelding wordt niet opgevuld als zowel `wid=` als `hei=` zijn opgegeven en de breedte/hoogte verschilt van de hoogte-breedteverhouding van de afbeelding.

`wid=` en  `hei=` werken samen om de grootte te bepalen van de afbeelding die door de server wordt geretourneerd. Als `scl=` na `wid=` of `hei=` in URL komt, annuleert het die bevelen en `scl=` bepaalt de grootte van het beeld dat door de server is teruggekeerd.

Als `wid=` of `hei=` in de URL echter `scl=` krijgt, worden `scl=` en `wid=`/ `hei=` de grootte van de door de server geretourneerde afbeelding geannuleerd.

>[!NOTE]
>
>Er wordt een fout geretourneerd als de berekende of standaardgrootte van de antwoordafbeelding groter is dan `attribute::MaxPix`.

## Eigenschappen {#section-6cbc6acd37c847beab84c896ac25280c}

Kan overal binnen het verzoek voorkomen. Als u het formaat van de afbeelding wijzigt met `wid=`, `hei=` of `scl=`, verandert de waarde van de afdrukresolutie die is ingesloten in de reactieafbeelding niet. Genegeerd als `scl=` voorkomt na `wid=` en/of `hei=` in de bevelopeenvolging.

## Standaard {#section-61043f6c1f5d450883ff9e5eafd95955}

Als noch `wid=`, `hei=`, noch `scl=` worden gespecificeerd, wordt het antwoordbeeld geschraapt om binnen de grootte te passen die door `attribute::DefaultPix` wordt bepaald. Als `attribute::DefaultPix` leeg is, heeft de antwoordafbeelding dezelfde grootte als de weergaveafbeelding van het vignet.

## Zie ook {#section-7ba51379f1e2421c92d3592d20a37734}

[kenmerk::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [kenmerk::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)

---
title: hei
description: Hoogte van afbeelding beantwoorden. Geeft aan dat de gerenderde afbeelding wordt geschaald, zodat de hoogte van de antwoordafbeelding niet groter is dan de opgegeven waarde, terwijl de hoogte-breedteverhouding van de afbeelding behouden blijft.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '244'
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

De afbeelding wordt niet opgevuld als beide `wid=` en `hei=` worden opgegeven en de breedte/hoogte verschilt van de hoogte-breedteverhouding van de afbeelding.

`wid=` en `hei=` werken samen om de grootte te bepalen van de afbeelding die door de server wordt geretourneerd. Indien `scl=` komt na `wid=` of `hei=` in de URL worden deze opdrachten geannuleerd en `scl=` Hiermee definieert u de grootte van de afbeelding die door de server wordt geretourneerd.

Als `wid=` of `hei=` komt na `scl=` in de URL annuleren `scl=` en `wid=`/ `hei=` Hiermee definieert u de grootte van de afbeelding die door de server wordt geretourneerd.

>[!NOTE]
>
>Er wordt een fout geretourneerd als de berekende of standaardgrootte van de antwoordafbeelding groter is dan `attribute::MaxPix`.

## Eigenschappen {#section-6cbc6acd37c847beab84c896ac25280c}

Kan overal binnen het verzoek voorkomen. Het formaat van de afbeelding wijzigen met `wid=`, `hei=`, of `scl=` wijzigt de waarde van de afdrukresolutie die is ingesloten in de reactieafbeelding niet. Genegeerd als `scl=` komt voor na `wid=` en/of `hei=` in de opdrachtvolgorde.

## Standaard {#section-61043f6c1f5d450883ff9e5eafd95955}

Indien `wid=`, `hei=`, of `scl=` niet zijn opgegeven, wordt de antwoordafbeelding geschaald zodat deze past binnen de grootte die wordt gedefinieerd door `attribute::DefaultPix`. Indien `attribute::DefaultPix` leeg is, heeft de reactieafbeelding dezelfde grootte als de afbeelding in de weergave van het vignet.

## Zie ook {#section-7ba51379f1e2421c92d3592d20a37734}

[kenmerk::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [kenmerk::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)

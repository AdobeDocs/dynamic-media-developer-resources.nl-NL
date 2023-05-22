---
title: winderig
description: Breedte van afbeelding beantwoorden. Geeft aan dat de gerenderde afbeelding wordt geschaald, zodat de antwoordafbeelding niet groter is dan de opgegeven waarde, terwijl de hoogte-breedteverhouding van de afbeelding behouden blijft.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a77b71c3-8600-4d7a-ba52-e158cf9668eb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# winderig{#wid}

Breedte van afbeelding beantwoorden. Geeft aan dat de gerenderde afbeelding wordt geschaald, zodat de antwoordafbeelding niet groter is dan de opgegeven waarde, terwijl de hoogte-breedteverhouding van de afbeelding behouden blijft.

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Afbeeldingsbreedte in pixels (int groter dan 0). </p></td> 
 </tr> 
</table>

De afbeelding wordt niet opgevuld als beide `wid=` en `hei=` wordt opgegeven en `wid`/ `hei` verschilt van de hoogte-breedteverhouding van de afbeelding.

`wid=` en `hei=` werken samen om de grootte te bepalen van de afbeelding die door de server wordt geretourneerd. Indien `scl=` komt na `wid=` of `hei=` in de URL worden deze opdrachten geannuleerd en `scl=` Hiermee definieert u de grootte van de afbeelding die door de server wordt geretourneerd.

Als `wid=` of `hei=` komt na `scl=` in de URL annuleren `scl=` en `wid=`/ `hei=` Hiermee definieert u de grootte van de afbeelding die door de server wordt geretourneerd.

>[!NOTE]
>
>Er wordt een fout geretourneerd als de berekende of standaardgrootte van de antwoordafbeelding groter is dan `attribute::MaxPix`.

## Eigenschappen {#section-2d067c6d371748e19cb157684700a49d}

Kan overal binnen het verzoek voorkomen. Het formaat van de afbeelding wijzigen met `wid=`, `hei=`, of `scl=` wijzigt de waarde van de afdrukresolutie die is ingesloten in de reactieafbeelding niet. Genegeerd als `scl=` komt voor na `wid=` of `hei=` in de opdrachtvolgorde.

## Standaard {#section-c7c6efa03d864592a3398b6f1de5a0b0}

Indien `wid=`, `hei=`, of `scl=` niet zijn opgegeven, wordt de antwoordafbeelding geschaald zodat deze past binnen de grootte die wordt gedefinieerd door `attribute::DefaultPix`. Indien `attribute::DefaultPix` leeg is, heeft de reactieafbeelding dezelfde grootte als de afbeelding in de weergave van het vignet.

## Zie ook {#section-450dfc12b1d440e2a3172a69d91db51f}

[kenmerk::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [kenmerk::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)

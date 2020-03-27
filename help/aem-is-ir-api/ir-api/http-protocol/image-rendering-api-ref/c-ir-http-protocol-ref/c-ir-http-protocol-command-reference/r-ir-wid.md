---
description: Breedte van afbeelding beantwoorden. Geeft aan dat de gerenderde afbeelding wordt geschaald, zodat de antwoordafbeelding niet groter is dan de opgegeven waarde, terwijl de hoogte-breedteverhouding van de afbeelding behouden blijft.
seo-description: Breedte van afbeelding beantwoorden. Geeft aan dat de gerenderde afbeelding wordt geschaald, zodat de antwoordafbeelding niet groter is dan de opgegeven waarde, terwijl de hoogte-breedteverhouding van de afbeelding behouden blijft.
seo-title: winderig
solution: Experience Manager
title: winderig
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a58a5d2-43ac-44db-9959-ba166006b7df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

De afbeelding wordt niet opgevuld als zowel de afbeelding `wid=` als de afbeelding `hei=` is opgegeven en `wid`/ `hei` afwijkt van de hoogte-breedteverhouding van de afbeelding.

`wid=` en `hei=` werken samen om de grootte te bepalen van de afbeelding die door de server wordt geretourneerd. Als deze opdracht `scl=` volgt `wid=` of `hei=` in de URL staat, worden deze opdrachten geannuleerd en wordt de grootte van de afbeelding `scl=` gedefinieerd die door de server wordt geretourneerd.

Als de URL echter `wid=` of `hei=` nadat deze is geplaatst, wordt geannuleerd `scl=` en wordt de grootte van de door de server geretourneerde afbeelding `scl=` / `wid=``hei=` gedefinieerd.

>[!NOTE]
>
>Er wordt een fout geretourneerd als de berekende of standaardgrootte van de antwoordafbeelding groter is dan `attribute::MaxPix`.

## Eigenschappen {#section-2d067c6d371748e19cb157684700a49d}

Kan overal binnen het verzoek voorkomen. Als u het formaat van de afbeelding wijzigt met `wid=`, `hei=`of `scl=` wijzigt u niet de waarde voor de afdrukresolutie die is ingesloten in de reactieafbeelding. Genegeerd als `scl=` voorkomt na `wid=` `hei=` of in de bevelopeenvolging.

## Standaard {#section-c7c6efa03d864592a3398b6f1de5a0b0}

Als noch `wid=`, `hei=`noch `scl=` worden gespecificeerd, wordt het antwoordbeeld geschraapt om binnen de grootte te passen die door wordt bepaald `attribute::DefaultPix`. Als de antwoordafbeelding leeg `attribute::DefaultPix` is, heeft deze dezelfde grootte als de afbeelding in de weergave van het vignet.

## Zie ook {#section-450dfc12b1d440e2a3172a69d91db51f}

[kenmerk::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [kenmerk::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)

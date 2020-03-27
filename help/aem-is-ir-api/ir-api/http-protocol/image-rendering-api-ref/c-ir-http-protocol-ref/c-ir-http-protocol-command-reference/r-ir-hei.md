---
description: Hoogte van afbeelding beantwoorden. Geeft aan dat de gerenderde afbeelding wordt geschaald, zodat de hoogte van de antwoordafbeelding niet groter is dan de opgegeven waarde, terwijl de hoogte-breedteverhouding van de afbeelding behouden blijft.
seo-description: Hoogte van afbeelding beantwoorden. Geeft aan dat de gerenderde afbeelding wordt geschaald, zodat de hoogte van de antwoordafbeelding niet groter is dan de opgegeven waarde, terwijl de hoogte-breedteverhouding van de afbeelding behouden blijft.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 616d3306-ccbd-4400-8a94-1ff6f47b802e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# hei{#hei}

Hoogte van afbeelding beantwoorden. Geeft aan dat de gerenderde afbeelding wordt geschaald, zodat de hoogte van de antwoordafbeelding niet groter is dan de opgegeven waarde, terwijl de hoogte-breedteverhouding van de afbeelding behouden blijft.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Hoogte van afbeelding beantwoorden in pixels (geheel getal groter dan 0). </p></td> 
 </tr> 
</table>

De afbeelding wordt niet opgevuld als zowel de afbeelding `wid=` als de afbeelding `hei=` zijn opgegeven en de breedte/hoogte verschilt van de hoogte-breedteverhouding van de afbeelding.

`wid=` en `hei=` werken samen om de grootte te bepalen van de afbeelding die door de server wordt geretourneerd. Als deze opdracht `scl=` volgt `wid=` of `hei=` in de URL staat, worden deze opdrachten geannuleerd en wordt de grootte van de afbeelding `scl=` gedefinieerd die door de server wordt geretourneerd.

Als de URL echter `wid=` of `hei=` nadat deze is geplaatst, wordt geannuleerd `scl=` en wordt de grootte van de door de server geretourneerde afbeelding `scl=` / `wid=``hei=` gedefinieerd.

>[!NOTE]
>
>Er wordt een fout geretourneerd als de berekende of standaardgrootte van de antwoordafbeelding groter is dan `attribute::MaxPix`.

## Eigenschappen {#section-6cbc6acd37c847beab84c896ac25280c}

Kan overal binnen het verzoek voorkomen. Als u het formaat van de afbeelding wijzigt met `wid=`, `hei=`of `scl=` wijzigt u niet de waarde voor de afdrukresolutie die is ingesloten in de reactieafbeelding. Genegeerd als `scl=` zich voordoet na `wid=` en/of `hei=` in de opdrachtreeks.

## Standaard {#section-61043f6c1f5d450883ff9e5eafd95955}

Als noch `wid=`, `hei=`noch `scl=` worden gespecificeerd, wordt het antwoordbeeld geschraapt om binnen de grootte te passen die door wordt bepaald `attribute::DefaultPix`. Als de antwoordafbeelding leeg `attribute::DefaultPix` is, heeft deze dezelfde grootte als de afbeelding in de weergave van het vignet.

## Zie ook {#section-7ba51379f1e2421c92d3592d20a37734}

[kenmerk::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [kenmerk::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)

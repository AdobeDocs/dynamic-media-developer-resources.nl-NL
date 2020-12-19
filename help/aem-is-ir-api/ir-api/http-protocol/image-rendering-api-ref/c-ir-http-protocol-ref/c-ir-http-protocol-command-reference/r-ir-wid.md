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
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# wid{#wid}

Breedte van afbeelding beantwoorden. Geeft aan dat de gerenderde afbeelding wordt geschaald, zodat de antwoordafbeelding niet groter is dan de opgegeven waarde, terwijl de hoogte-breedteverhouding van de afbeelding behouden blijft.

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Afbeeldingsbreedte in pixels (int groter dan 0). </p></td> 
 </tr> 
</table>

De afbeelding wordt niet toegevoegd als zowel `wid=` als `hei=` is opgegeven en `wid`/ `hei` verschilt van de hoogte-breedteverhouding van de afbeelding.

`wid=` en  `hei=` werken samen om de grootte te bepalen van de afbeelding die door de server wordt geretourneerd. Als `scl=` na `wid=` of `hei=` in URL komt, annuleert het die bevelen en `scl=` bepaalt de grootte van het beeld dat door de server is teruggekeerd.

Als `wid=` of `hei=` in de URL echter `scl=` krijgt, worden `scl=` en `wid=`/ `hei=` de grootte van de door de server geretourneerde afbeelding geannuleerd.

>[!NOTE]
>
>Er wordt een fout geretourneerd als de berekende of standaardgrootte van de antwoordafbeelding groter is dan `attribute::MaxPix`.

## Eigenschappen {#section-2d067c6d371748e19cb157684700a49d}

Kan overal binnen het verzoek voorkomen. Als u het formaat van de afbeelding wijzigt met `wid=`, `hei=` of `scl=`, verandert de waarde van de afdrukresolutie die is ingesloten in de reactieafbeelding niet. Genegeerd als `scl=` voorkomt na `wid=` of `hei=` in de bevelopeenvolging.

## Standaard {#section-c7c6efa03d864592a3398b6f1de5a0b0}

Als noch `wid=`, `hei=`, noch `scl=` worden gespecificeerd, wordt het antwoordbeeld geschraapt om binnen de grootte te passen die door `attribute::DefaultPix` wordt bepaald. Als `attribute::DefaultPix` leeg is, heeft de antwoordafbeelding dezelfde grootte als de weergaveafbeelding van het vignet.

## Zie ook {#section-450dfc12b1d440e2a3172a69d91db51f}

[kenmerk::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [kenmerk::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)

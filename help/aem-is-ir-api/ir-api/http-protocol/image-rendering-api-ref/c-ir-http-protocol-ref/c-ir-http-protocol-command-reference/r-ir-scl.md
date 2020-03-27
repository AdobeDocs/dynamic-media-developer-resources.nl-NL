---
description: Schaalweergave. Hiermee schaalt u de gerenderde afbeelding met de opgegeven schaalfactor ten opzichte van het vignet met volledige resolutie.
seo-description: Schaalweergave. Hiermee schaalt u de gerenderde afbeelding met de opgegeven schaalfactor ten opzichte van het vignet met volledige resolutie.
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: 04839c44-01b6-4fa2-9eda-bbb0f2822db4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scl{#scl}

Schaalweergave. Hiermee schaalt u de gerenderde afbeelding met de opgegeven schaalfactor ten opzichte van het vignet met volledige resolutie.

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span></span> </p></td> 
  <td class="stentry"> <p>Omgekeerde schaalfactor (reëel, 1,0 of groter). </p></td> 
 </tr> 
</table>

Als deze opdracht `scl=` volgt `wid=` of `hei=` in de URL staat, worden deze opdrachten geannuleerd en wordt de grootte van de afbeelding `scl=` gedefinieerd die door de server wordt geretourneerd.

Als de URL echter `wid=` of `hei=` nadat deze is geplaatst, wordt geannuleerd `scl=` en wordt de grootte van de door de server geretourneerde afbeelding `scl=` / `wid=``hei=` gedefinieerd.

>[!NOTE]
>
>Er wordt een fout geretourneerd als de berekende of standaardgrootte van de antwoordafbeelding groter is dan `attribute::MaxPix`.

## Eigenschappen {#section-170458cbd6984bd59a3434431258b20f}

Kan overal binnen het verzoek voorkomen. Genegeerd als `wid=` of `hei=` voorkomen na `scl=` in de bevelopeenvolging.

Als u de grootte van de afbeelding wijzigt, verandert de waarde voor de afdrukresolutie die is ingesloten in de reactieafbeelding `scl=` niet.

## Standaard {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

Als noch `wid=`, `hei=` noch `scl=` worden gespecificeerd, wordt het antwoordbeeld geschraapt om binnen de grootte te passen die door wordt bepaald `attribute::DefaultPix`. Als de antwoordafbeelding leeg `attribute::DefaultPix` is, heeft deze dezelfde grootte als de afbeelding in de weergave van het vignet.

## Zie ook {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [kenmerk::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [kenmerk::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)

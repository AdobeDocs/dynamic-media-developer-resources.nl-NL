---
title: scl
description: Schaalweergave. Hiermee schaalt u de gerenderde afbeelding met de opgegeven schaalfactor ten opzichte van het vignet met volledige resolutie.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# scl{#scl}

Schaalweergave. Hiermee schaalt u de gerenderde afbeelding met de opgegeven schaalfactor ten opzichte van het vignet met volledige resolutie.

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>Omgekeerde schaalfactor (reëel, 1,0 of groter). </p></td> 
 </tr> 
</table>

Indien `scl=` komt na `wid=` of `hei=` in de URL worden deze opdrachten geannuleerd en `scl=` Hiermee definieert u de grootte van de afbeelding die door de server wordt geretourneerd.

Als `wid=` of `hei=` komt na `scl=` in de URL annuleren `scl=` en `wid=`/ `hei=` Hiermee definieert u de grootte van de afbeelding die door de server wordt geretourneerd.

>[!NOTE]
>
>Er wordt een fout geretourneerd als de berekende of standaardgrootte van de antwoordafbeelding groter is dan `attribute::MaxPix`.

## Eigenschappen {#section-170458cbd6984bd59a3434431258b20f}

Kan overal binnen het verzoek voorkomen. Genegeerd als `wid=` of `hei=` voorkomen na `scl=` in de opdrachtvolgorde.

Het formaat van de afbeelding wijzigen met `scl=` wijzigt de waarde van de afdrukresolutie die is ingesloten in de reactieafbeelding niet.

## Standaard {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

Indien `wid=`, `hei=`, of `scl=` niet zijn opgegeven, wordt de antwoordafbeelding geschaald zodat deze past binnen de grootte die wordt gedefinieerd door `attribute::DefaultPix`. Indien `attribute::DefaultPix` leeg is, heeft de reactieafbeelding dezelfde grootte als de afbeelding in de weergave van het vignet.

## Zie ook {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [kenmerk::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [kenmerk::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)

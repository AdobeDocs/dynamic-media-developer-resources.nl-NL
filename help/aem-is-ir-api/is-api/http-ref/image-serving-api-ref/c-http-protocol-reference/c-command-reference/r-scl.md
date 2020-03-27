---
description: Schaalweergave. Hiermee wordt de samengestelde afbeelding geschaald met de inverse van invFactor.
seo-description: Schaalweergave. Hiermee wordt de samengestelde afbeelding geschaald met de inverse van invFactor.
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: 10a365dc-9fc1-4236-9528-4aca04a4ca19
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scl{#scl}

Schaalweergave. Hiermee wordt de samengestelde afbeelding geschaald met de inverse van invFactor.

`scl= *`invFactor`*`

<table id="simpletable_A09F5EECAC2B4E0F8633D71C6AD36D8D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> invFactor</span> </p> </td> 
  <td class="stentry"> <p>Omgekeerde schaalfactor (reëel groter dan 0,0). </p></td> 
 </tr> 
</table>

Er wordt geen schaling toegepast wanneer `scl=1`. *`invFactor`* Als de afbeelding groter is dan 1,0 en kleiner dan 1,0, wordt de samengestelde afbeelding vergroot.

Als `scl=` wordt opgegeven en `wid=` en/of `hei=` ook aanwezig zijn, wordt de afbeelding uitgesneden tot `wid=` en/of `hei=` na het schalen.

>[!NOTE]
>
>Er wordt een fout geretourneerd als de berekende of standaardgrootte van de antwoordafbeelding groter is dan `attribute::MaxPix`.

## Eigenschappen {#section-60af012719db477db4a4703e9a6da5f5}

Kenmerk weergeven. Ongeacht de huidige laaginstelling.

## Standaard {#section-32502fa218a24e1f9c65f41c0260b56a}

Als noch `wid=`, `hei=`noch `scl=` worden gespecificeerd, zal het antwoordbeeld of de grootte van het samengestelde beeld of `attribute::DefaultPix`, welke kleiner is hebben.

## Voorbeeld {#section-a33f6239476a4b438d939656ad99aa76}

Zie het voorbeeld in [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) voor een gemeenschappelijke toepassing van `scl=`.

## Zie ook {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [kenmerk::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)

---
title: scl
description: Schaalweergave. Hiermee wordt de samengestelde afbeelding geschaald met de inverse van invFactor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 297d187c-3a52-45ff-b73d-0b0e4b956080
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

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

Indien `scl=` wordt opgegeven, en `wid=` en/of `hei=` ook aanwezig zijn, wordt de afbeelding uitgesneden tot `wid=` en/of `hei=` na het schalen.

>[!NOTE]
>
>Er wordt een fout geretourneerd als de berekende of standaardgrootte van de antwoordafbeelding groter is dan `attribute::MaxPix`.

## Eigenschappen {#section-60af012719db477db4a4703e9a6da5f5}

Kenmerk weergeven. Ongeacht de huidige laaginstelling.

## Standaard {#section-32502fa218a24e1f9c65f41c0260b56a}

Als geen van beide `wid=`, `hei=`, noch `scl=` worden opgegeven, heeft de antwoordafbeelding de grootte van de samengestelde afbeelding of `attribute::DefaultPix`, afhankelijk van welke waarde kleiner is.

## Voorbeeld {#section-a33f6239476a4b438d939656ad99aa76}

Zie het voorbeeld in [roteren=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) voor een gemeenschappelijke toepassing van `scl=`.

## Zie ook {#section-ccefd5de59924059903d66d4974ce317}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [kenmerk::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)

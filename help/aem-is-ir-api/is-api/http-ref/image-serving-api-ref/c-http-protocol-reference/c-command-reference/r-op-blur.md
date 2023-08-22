---
title: op_vervagen
description: Afbeelding vervagen. Hiermee past u een vervagend filter toe op de afbeeldingsgegevens.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# op_vervagen{#op-blur}

Afbeelding vervagen. Hiermee past u een vervagend filter toe op de afbeeldingsgegevens.

`op_blur= *`radius`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>Straal van vervagingsfilter in pixels (reëel 0..100). </p></td> 
 </tr> 
</table>

*`radius`* in pixels ten opzichte van de samengestelde afbeelding. Wordt ook gebruikt om laageffecten te doezelen.

## Eigenschappen {#section-92573fe2c07746a7bab93a81fc3d208d}

Laag, opdracht. Is van toepassing op de huidige laag of op de samengestelde afbeelding als `layer=comp`.

## Standaard {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, voor geen vervagingseffect.

## Voorbeeld {#section-1ebacde68388492eb108ae0fcd7424db}

Vervaag de achtergrond van een afbeelding. Er wordt verwezen naar een afzonderlijke maskerafbeelding door `catalog::MaskPath`. Let op: `layer=0`uitdrukkelijk moet worden gespecificeerd, anders `op_blur` wordt toegepast op de volledige samengestelde afbeelding.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`

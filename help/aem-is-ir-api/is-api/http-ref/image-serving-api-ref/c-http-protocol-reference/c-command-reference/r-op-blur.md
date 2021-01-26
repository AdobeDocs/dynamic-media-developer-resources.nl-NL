---
description: Afbeelding vervagen. Hiermee past u een vervagend filter toe op de afbeeldingsgegevens.
seo-description: Afbeelding vervagen. Hiermee past u een vervagend filter toe op de afbeeldingsgegevens.
seo-title: op_vervagen
solution: Experience Manager
title: op_vervagen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8405bbb5-fe09-412e-9b52-0af2c01f48b9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '106'
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

Laag, opdracht. Wordt toegepast op de huidige laag of op de samengestelde afbeelding als `layer=comp`.

## Standaard {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, voor geen vervagingseffect.

## Voorbeeld {#section-1ebacde68388492eb108ae0fcd7424db}

Vervaag de achtergrond van een afbeelding. Naar een afzonderlijke maskerafbeelding wordt verwezen door `catalog::MaskPath`. `layer=0`moet expliciet worden opgegeven, anders zou `op_blur` worden toegepast op de volledige samengestelde afbeelding.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`

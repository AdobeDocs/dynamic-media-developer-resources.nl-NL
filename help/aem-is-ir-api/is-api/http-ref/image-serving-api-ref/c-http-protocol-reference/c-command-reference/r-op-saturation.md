---
title: op_verzadiging
description: Pas de verzadiging aan. Hiermee wijzigt u de verzadiging van elke zichtbare pixel van de laag of samengestelde afbeelding.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd71e27e-6ccc-4ade-9bcf-af8e41bcf381
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# op_verzadiging{#op-saturation}

Pas de verzadiging aan. Hiermee wijzigt u de verzadiging van elke zichtbare pixel van de laag of samengestelde afbeelding.

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Verzadiging aanpassen (-100..+100 int). </p></td> 
 </tr> 
</table>

`op_saturation=-100` Hiermee wordt de verzadiging van de afbeelding volledig opgeheven.

## Eigenschappen {#section-9a3cc9ff060049449554dfa69d92fd53}

Laag, opdracht. Is van toepassing op de huidige laag of op de samengestelde afbeelding als `layer=comp`. Genegeerd door effectlagen.

## Standaard {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`, voor ongewijzigde verzadiging. CMYK-afbeeldingen of -lagen worden omgezet in RGB voordat de bewerking wordt toegepast.

## Voorbeeld {#section-033b272f1b7e4efeb94e841fd8095357}

Bewerk een kleurenfoto zodat u een high-key weergave krijgt:

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`

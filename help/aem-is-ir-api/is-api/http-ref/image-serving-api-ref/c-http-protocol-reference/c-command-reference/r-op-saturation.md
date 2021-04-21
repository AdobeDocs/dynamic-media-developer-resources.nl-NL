---
description: Pas de verzadiging aan. Hiermee wijzigt u de verzadiging van elke zichtbare pixel van de laag of samengestelde afbeelding.
solution: Experience Manager
title: op_verzadiging
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '98'
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

Laag, opdracht. Wordt toegepast op de huidige laag of op de samengestelde afbeelding als `layer=comp`. Genegeerd door effectlagen.

## Standaard {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`, voor ongewijzigde verzadiging. CMYK-afbeeldingen of -lagen worden omgezet in RGB voordat de bewerking wordt toegepast.

## Voorbeeld {#section-033b272f1b7e4efeb94e841fd8095357}

Bewerk een kleurenfoto om deze een &#39;high key&#39;-weergave te geven:

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`

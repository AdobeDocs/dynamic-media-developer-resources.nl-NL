---
title: ZoomView.transition
description: ZoomView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bb00a1c9-aa6f-428f-8d57-241ee1efa082
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *`tijd`*[, *`versnelling`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> tijd</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de tijd in seconden die de animatie voor een enkele zoomstap nodig heeft. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> versnelling</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee creëert u een illusie van versnelling of vertraging, waardoor de overgang er natuurlijker uitziet. U kunt versnelling instellen op een van de volgende opties: </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (automatisch) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 (lineair) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (kwadratisch) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (cubisch) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (kwart) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (quintisch) </li> 
     </ul> </p> <p>In de modus Automatisch wordt altijd een lineaire overgang gebruikt wanneer elastisch zoomen is uitgeschakeld (standaard). Anders past het een van de andere versnellingsfuncties op basis van de overgangstijd. Hoe korter de overgangstijd, hoe hoger de versnellingsfunctie wordt gebruikt om het versnellings- of vertragingseffect te versnellen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`

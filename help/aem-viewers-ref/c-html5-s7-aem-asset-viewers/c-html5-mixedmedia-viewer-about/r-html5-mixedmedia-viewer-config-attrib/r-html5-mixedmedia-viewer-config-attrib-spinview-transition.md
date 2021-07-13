---
description: SpinView.transition
solution: Experience Manager
title: SpinView.transition
feature: Dynamic Media Classic,Viewers,SDK/API,Gemengde mediasets
role: Developer,User
exl-id: fcffe282-65a5-4093-8838-71a64085b387
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *``*[, *`tijdverlies`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> tijd</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de tijd in seconden die de animatie voor een enkele zoomstap nodig heeft. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> versnelling</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee creëert u een illusie van versnelling of vertraging, waardoor de overgang er natuurlijker uitziet. U kunt versnelling instellen op een van de volgende opties: </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0 (automatisch) </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1 (lineair) </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 (kwadratisch) </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 (cubisch) </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4 (kwart) </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5 (quintisch) </li> 
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

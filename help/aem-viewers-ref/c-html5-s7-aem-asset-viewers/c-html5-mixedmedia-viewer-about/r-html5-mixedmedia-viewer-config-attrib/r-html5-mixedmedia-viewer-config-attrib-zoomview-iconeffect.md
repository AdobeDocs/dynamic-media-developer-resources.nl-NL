---
description: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
feature: Dynamic Media Classic,Viewers,SDK/API,Gemengde mediasets
role: Developer,Business Practitioner
exl-id: 40b7887d-d525-4816-8c72-9ef8f5948de3
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 1%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Hiermee wordt het iconeffect <span class="codeph"></span> boven in de afbeelding weergegeven wanneer de afbeelding is hersteld en er een actie wordt voorgesteld die beschikbaar is voor interactie met de afbeelding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> aantal</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u het maximale aantal keren op dat het iconeffect <span class="codeph"></span> wordt weergegeven en opnieuw wordt weergegeven. De waarde <span class="codeph"> -1</span> geeft aan dat het pictogram altijd voor onbepaalde tijd opnieuw wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> vervagen</span></span> </p> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u de duur van de animatie voor tonen of verbergen in seconden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Hiermee stelt u het aantal seconden in dat het iconeffect <span class="codeph"> volledig zichtbaar blijft voordat het automatisch wordt verborgen. </span> De tijd nadat de animatie voor infaden is voltooid, maar voordat de animatie voor uitfaden wordt gestart. Met de instelling <span class="codeph"> 0</span> wordt het gedrag voor automatisch verbergen uitgeschakeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`

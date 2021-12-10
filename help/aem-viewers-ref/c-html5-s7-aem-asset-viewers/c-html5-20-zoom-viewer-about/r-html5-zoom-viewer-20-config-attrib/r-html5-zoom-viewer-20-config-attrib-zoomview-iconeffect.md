---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 59d71d3b-706f-4f77-8e75-e24c5654f6e3
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 1%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`aantal`*][, *`vervagen`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Hiermee schakelt u het <span class="codeph"> iconeffect</span> om boven op de afbeelding weer te geven wanneer de afbeelding opnieuw is ingesteld en er een actie voor interactie met de afbeelding wordt voorgesteld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> aantal</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u het maximale aantal keren op dat de <span class="codeph"> iconeffect</span> verschijnt en verschijnt opnieuw. Een waarde van <span class="codeph"> -1</span> Hiermee wordt aangegeven dat het pictogram altijd voor onbepaalde tijd opnieuw wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> vervagen</span></span> </p> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u de duur van de animatie voor tonen of verbergen in seconden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Hiermee stelt u het aantal seconden in dat de <span class="codeph"> iconeffect</span> blijft volledig zichtbaar voordat deze automatisch wordt verborgen. De tijd nadat de animatie voor infaden is voltooid, maar voordat de animatie voor uitfaden wordt gestart. Een instelling van <span class="codeph"> 0</span> Hiermee schakelt u het gedrag voor automatisch verbergen uit. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`1,1,0.3,3`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`

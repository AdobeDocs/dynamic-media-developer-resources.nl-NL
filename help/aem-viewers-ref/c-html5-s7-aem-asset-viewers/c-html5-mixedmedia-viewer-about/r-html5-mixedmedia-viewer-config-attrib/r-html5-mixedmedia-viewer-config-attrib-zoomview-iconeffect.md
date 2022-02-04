---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 40b7887d-d525-4816-8c72-9ef8f5948de3
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
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

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`

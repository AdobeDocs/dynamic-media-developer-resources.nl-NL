---
title: SpinView.iconeffect
description: SpinView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e84336da-7f33-4fa9-b881-93b9db4bae8b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---

# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *`aantal`*][, *`vervagen`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Hiermee schakelt u het <span class="codeph"> iconeffect</span> om boven op de afbeelding weer te geven wanneer de afbeelding opnieuw is ingesteld en er een actie voor interactie met de afbeelding wordt voorgesteld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> aantal</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u het maximale aantal keren op dat de <span class="codeph"> iconeffect</span> wordt weergegeven en verschijnt opnieuw. Een waarde van <span class="codeph"> -1</span> Hiermee wordt aangegeven dat het pictogram altijd voor onbepaalde tijd opnieuw wordt weergegeven. </p> </td> 
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

## Eigenschappen {#section-924163cb2f6542499f49894becef7fb5}

Optioneel.

## Standaard {#section-7a2128fd488941948aff18421f533ccf}

`1,1,0.3,3`

## Voorbeeld {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`iconeffect=0`

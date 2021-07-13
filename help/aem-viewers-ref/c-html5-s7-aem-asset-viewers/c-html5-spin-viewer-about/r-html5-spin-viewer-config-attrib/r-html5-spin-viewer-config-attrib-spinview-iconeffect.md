---
description: SpinView.iconeffect
solution: Experience Manager
title: SpinView.iconeffect
feature: Dynamic Media Classic,Viewers,SDK/API,Draaiensets
role: Developer,User
exl-id: e84336da-7f33-4fa9-b881-93b9db4bae8b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---

# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

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

## Eigenschappen {#section-924163cb2f6542499f49894becef7fb5}

Optioneel.

## Standaard {#section-7a2128fd488941948aff18421f533ccf}

`1,1,0.3,3`

## Voorbeeld {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`iconeffect=0`

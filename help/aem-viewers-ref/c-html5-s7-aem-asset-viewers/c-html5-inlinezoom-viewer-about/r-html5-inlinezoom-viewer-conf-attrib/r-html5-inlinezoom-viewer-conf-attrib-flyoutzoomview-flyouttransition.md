---
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
topic: Dynamic media
uuid: 0b94956d-9ee6-409e-9b52-29c888932a0e
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|slide|faden  </span> </span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u het type op dat wordt toegepast wanneer de vervolgweergave wordt weergegeven of verborgen. Bij <span class="codeph"> geen </span> wordt de uitvliegafbeelding direct weergegeven wanneer deze wordt geactiveerd en gereed is; <span class="codeph"> dia </span> zorgt ervoor dat de dia-animatie van links naar rechts wordt afgespeeld; <span class="codeph"> vervagen </span> past een alpha- overgang op het flyout beeld toe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> Aantal seconden dat de showanimatie neemt om te voltooien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay  </span> </span> </p> </td> 
   <td colname="col2"> <p> De vertraging in seconden tussen de actie van de gebruiker die de showanimatie en het begin van showanimatie zelf in werking stelt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> bijtijd  </span> </span> </p> </td> 
   <td colname="col2"> <p> Aantal seconden dat de verbergende animatie duurt om te voltooien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> achterstallig  </span> </span> </p> </td> 
   <td colname="col2"> <p> De vertraging in seconden tussen de actie van de gebruiker die de huidenanimatie en het begin van huidenanimatie zelf in werking stelt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optioneel.

## Standaard {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## Voorbeeld {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`

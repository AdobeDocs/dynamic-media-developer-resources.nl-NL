---
title: FlyoutZoomView.flyouttransition
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 3199d4a3-4799-40a2-b0a5-0e1ee4744fbe
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---

# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *`showtime`*[, *`showdelay`*[, *`bijtijd`*[, *`achterstallig`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|slide|faden </span> </span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u het type op dat wordt toegepast wanneer de vervolgweergave wordt weergegeven of verborgen. Met <span class="codeph"> none </span>, wordt de uitvliegafbeelding onmiddellijk weergegeven wanneer deze wordt geactiveerd en gereed is; <span class="codeph"> dia </span> Hiermee wordt de animatie van de dia in de richting van links naar rechts afgespeeld. <span class="codeph"> vervagen </span> Hiermee past u een alpha-overgang toe op de vervolgafbeelding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> Aantal seconden dat de showanimatie neemt om te voltooien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay </span> </span> </p> </td> 
   <td colname="col2"> <p> De vertraging in seconden tussen de actie van de gebruiker die de showanimatie en het begin van showanimatie zelf in werking stelt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> bijtijd </span> </span> </p> </td> 
   <td colname="col2"> <p> Aantal seconden dat de verbergende animatie duurt om te voltooien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> achterstallig </span> </span> </p> </td> 
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

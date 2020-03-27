---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
topic: Dynamic media
uuid: f1a9f2bc-9a13-4980-9241-e835a0aadd2c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|slide|faden </span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u het type op dat wordt toegepast wanneer de vervolgweergave wordt weergegeven of verborgen. Bij <span class="codeph"> geen </span>wordt de uitvliegafbeelding direct weergegeven wanneer deze wordt geactiveerd en gereed is; De <span class="codeph"> dia </span> zorgt ervoor dat de dia-animatie van links naar rechts wordt afgespeeld. Met <span class="codeph"> Vervagen </span> past u een alpha-overgang toe op de vervolgafbeelding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span></span> </p> </td> 
   <td colname="col2"> <p> Aantal seconden dat de showanimatie neemt om te voltooien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay </span></span> </p> </td> 
   <td colname="col2"> <p> De vertraging in seconden tussen de actie van de gebruiker die de showanimatie en het begin van showanimatie zelf in werking stelt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidetijd </span></span> </p> </td> 
   <td colname="col2"> <p> Aantal seconden dat de verbergende animatie duurt om te voltooien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> vertraging </span></span> </p> </td> 
   <td colname="col2"> <p> De vertraging in seconden tussen de actie van de gebruiker die de huidenanimatie en het begin van huidenanimatie zelf in werking stelt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optioneel.

## Standaard {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## Voorbeeld {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1`

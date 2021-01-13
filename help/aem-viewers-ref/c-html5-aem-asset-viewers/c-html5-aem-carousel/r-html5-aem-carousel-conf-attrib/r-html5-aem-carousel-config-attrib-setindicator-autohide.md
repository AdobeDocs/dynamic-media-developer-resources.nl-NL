---
description: SetIndicator.autohide
solution: Experience Manager
title: SetIndicator.autohide
topic: Dynamic media
uuid: eb93ad7a-6176-47ed-92c6-2eb1afcac0eb
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---


# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`limiet`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> limiet</span>]</span> </p> </td> 
   <td colname="col2"> <p> Vormt gedrag voor automatisch verbergen afhankelijk van het aantal pagina's en de grootte van de uitvoeringscomponent. </p> <p> <span class="codeph"> 0</span> schakelt automatisch verbergen uit. </p> <p> <span class="codeph"> 1</span> schakelt automatisch verbergen in. De component verbergt de punten als ten minste een van de volgende voorwaarden wordt toegepast: </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">de rij met punten breder wordt dan de breedte van de uitvoeringscomponent, of </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">Het aantal pagina's dat voor deze component wordt ingesteld, overschrijdt de limiet die door de parameter <span class="codeph"><span class="varname"> limit</span></span> wordt geconfigureerd. </li> 
     </ul> </p> <p> Als u <span class="codeph"><span class="varname"> limit</span></span> instelt op <span class="codeph"> -1</span>, wordt de tweede voorwaarde voor automatisch verbergen uitgeschakeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`1,10`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`

---
title: Swatches.enabledragging
description: Swatches.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 6ae18f94-7a0f-429e-9684-eff43f523b1d
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 2%

---

# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> Hiermee schakelt u de mogelijkheid in of uit dat een gebruiker de stalen met de muis of met aanraakbewegingen kan schuiven </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> Functies binnen de <span class="codeph"> 0-1 </span> bereik. Het is een <span class="codeph"> % </span> waarde voor beweging in de verkeerde richting van de werkelijke snelheid. Als deze is ingesteld op <span class="codeph"> 1 </span>, beweegt het met de muis. Als deze is ingesteld op <span class="codeph"> 0 </span>U kunt echter helemaal niet in de verkeerde richting gaan. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enabledragging=0`

---
title: InteractiveSwatches.enabledragging
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 91c5eb52-40d9-40f6-8687-e68cb40b634e
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 1%

---

# InteractiveSwatches.enabledragging{#interactiveswatches-enabledragging}

Configuration attribute for Interactive Video Viewer.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Hiermee schakelt u de mogelijkheid in of uit dat een gebruiker de stalen met de muis of met aanraakbewegingen kan schuiven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td colname="col2"> <p> bevindt zich in de <span class="codeph"> 0-1 </span> bereik en is een procentuele waarde voor de beweging in de verkeerde richting van de werkelijke snelheid. </p> <p>Indien ingesteld op <span class="codeph"> 1 </span>, beweegt het met de muis. </p> <p>Indien ingesteld op <span class="codeph"> 0 </span>U kunt echter niet in de verkeerde richting gaan. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```

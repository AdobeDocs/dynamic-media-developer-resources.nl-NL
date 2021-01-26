---
description: Configuration attribute for Interactive Video Viewer.
seo-description: Configuration attribute for Interactive Video Viewer.
seo-title: InteractiveSwatches.enabledragging
solution: Experience Manager
title: InteractiveSwatches.enabledragging
topic: Dynamic Media
uuid: 9a93e6b3-3441-4987-b9e6-a964dbf2247d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 2%

---


# InteractiveSwatches.enabledragging{#interactiveswatches-enabledragging}

Configuration attribute for Interactive Video Viewer.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee schakelt u de mogelijkheid in of uit dat een gebruiker de stalen met de muis of met aanraakbewegingen kan schuiven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td colname="col2"> <p> Is in <span class="codeph"> 0-1 </span> waaier en het is een percentagewaarde voor de beweging in de verkeerde richting van de daadwerkelijke snelheid. </p> <p>Indien ingesteld op <span class="codeph"> 1 </span>, wordt het met de muis verplaatst. </p> <p>Als dit op <span class="codeph"> 0 </span> wordt ingesteld, kunt u niet in de verkeerde richting bewegen. </p> </td> 
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


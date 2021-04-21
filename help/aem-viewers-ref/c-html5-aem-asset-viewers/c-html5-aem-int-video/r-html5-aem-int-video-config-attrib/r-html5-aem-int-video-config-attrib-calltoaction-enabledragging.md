---
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
title: CallToAction.enabledragging
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 21db58df-b76e-4a78-afc4-5e0188cb8896
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---

# CallToAction.enabledragging{#calltoaction-enabledragging}

Configuration attribute for Interactive Video Viewer.

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee schakelt u de mogelijkheid in of uit dat een gebruiker de miniaturen met de muis of met aanraakbewegingen kan schuiven. </p> </td> 
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

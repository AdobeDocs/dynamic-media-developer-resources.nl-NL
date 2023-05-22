---
title: InteractiveSwatches.direction
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

Configuration attribute for Interactive Video Viewer.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u hoe stalen de weergave vullen. </p> <p>Instellen op <span class="codeph"> left </span> om de vulvolgorde van links naar rechts in te stellen. </p> <p>Instellen op <span class="codeph"> right </span> Hiermee draait u de volgorde om, zodat de weergave wordt gevuld in de richting van rechts naar links en van boven naar beneden. </p> <p>Wanneer <span class="codeph"> auto </span> is ingesteld, wordt de rechtermodus van de component toegepast wanneer de landinstelling is ingesteld op " <span class="codeph"> ja </span>"; anders, <span class="codeph"> left </span> wordt gebruikt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`auto`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```

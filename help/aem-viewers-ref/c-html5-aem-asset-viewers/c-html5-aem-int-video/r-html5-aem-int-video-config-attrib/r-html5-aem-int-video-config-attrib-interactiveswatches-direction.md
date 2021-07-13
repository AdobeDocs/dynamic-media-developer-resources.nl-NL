---
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
title: InteractiveSwatches.direction
feature: Dynamic Media Classic,Viewers,SDK/API,Interactieve video's
role: Developer,User
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 1%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

Configuration attribute for Interactive Video Viewer.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u hoe stalen de weergave vullen. </p> <p>Stel in op <span class="codeph"> links </span> om de vulvolgorde van links naar rechts in te stellen. </p> <p>Met de instelling <span class="codeph"> rechts </span> wordt de volgorde omgekeerd, zodat de weergave in een richting van rechts naar links en van boven naar beneden wordt gevuld. </p> <p>Wanneer <span class="codeph"> auto </span> is ingesteld, past de component de rechtermodus toe wanneer de landinstelling is ingesteld op " <span class="codeph"> ja </span>"; anders wordt <span class="codeph"> links </span> gebruikt. </p> </td> 
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

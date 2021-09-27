---
title: CallToAction.direction
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 1%

---

# CallToAction.direction{#calltoaction-direction}

Configuration attribute for Interactive Video Viewer.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u hoe miniaturen de weergave vullen. </p> <p>Stel in op <span class="codeph"> links </span> om de vulvolgorde van links naar rechts in te stellen. </p> <p>Met de instelling <span class="codeph"> rechts </span> wordt de volgorde omgekeerd, zodat de weergave in een richting van rechts naar links en van boven naar beneden wordt gevuld. </p> <p>Stel in op <span class="codeph"> auto </span> om de component de modus right te laten toepassen wanneer de landinstelling is ingesteld op <span class="codeph"> "ja" </span>; anders wordt <span class="codeph"> links </span> gebruikt. </p> </td> 
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

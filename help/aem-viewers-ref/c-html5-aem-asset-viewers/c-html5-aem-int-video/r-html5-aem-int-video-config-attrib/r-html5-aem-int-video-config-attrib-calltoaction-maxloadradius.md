---
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
title: CallToAction.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,Interactieve video's
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 1%

---


# CallToAction.maxloadradius{#calltoaction-maxloadradius}

Configuration attribute for Interactive Video Viewer.

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`voorlader`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Geeft het gedrag voor het vooraf laden van de component op. </p> <p>Wanneer ingesteld op <span class="codeph"> -1</span> worden alle miniaturen tegelijkertijd geladen wanneer de component wordt geïnitialiseerd of het element wordt gewijzigd. </p> <p>Wanneer ingesteld op <span class="codeph"> 0</span> worden alleen zichtbare miniaturen geladen. </p> <p>Stel dit in op <span class="codeph"><span class="varname"> voorlader</span></span> om te bepalen hoeveel onzichtbare rijen/kolommen rondom het zichtbare gebied worden voorgeladen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`-1`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```


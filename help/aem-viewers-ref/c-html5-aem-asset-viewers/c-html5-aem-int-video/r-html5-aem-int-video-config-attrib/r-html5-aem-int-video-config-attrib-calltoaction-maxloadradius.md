---
title: CallToAction.maxloadradius
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '68'
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

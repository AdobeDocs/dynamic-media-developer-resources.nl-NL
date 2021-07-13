---
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
title: InteractiveSwatches.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,Interactieve video's
role: Developer,User
exl-id: 16c9c70a-352d-4a21-bb14-2f9e266a83e8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 1%

---

# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

Configuration attribute for Interactive Video Viewer.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`voorlader`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> voorlaad</span></span> </p> </td> 
   <td colname="col2"> <p> Geeft het gedrag voor het vooraf laden van de component op. </p> <p>Wanneer ingesteld op <span class="codeph"> -1</span> worden alle stalen tegelijkertijd geladen wanneer de component wordt geïnitialiseerd of het element wordt gewijzigd. </p> <p>Wanneer ingesteld op <span class="codeph"> 0</span>, worden alleen zichtbare stalen geladen. </p> <p>Stel dit in op <span class="codeph"><span class="varname"> voorlader</span></span> om te bepalen hoeveel onzichtbare rijen/kolommen rondom het zichtbare gebied worden voorgeladen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`1`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```

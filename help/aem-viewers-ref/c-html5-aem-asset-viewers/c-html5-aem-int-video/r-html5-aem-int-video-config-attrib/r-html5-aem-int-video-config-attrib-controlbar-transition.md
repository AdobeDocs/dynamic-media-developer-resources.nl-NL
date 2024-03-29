---
title: ControlBar.transition
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# ControlBar.transition{#controlbar-transition}

Configuration attribute for Interactive Video Viewer.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duur`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|faden</span> </p> </td> 
   <td colname="col2"> <p> Geeft het effecttype aan dat wordt gebruikt om de besturingsbalk en de inhoud ervan weer te geven/te verbergen. </p> <p>Instellen op <span class="codeph"> none</span> bijvoorbeeld tonen/verbergen. </p> <p>Instellen op <span class="codeph"> vervagen</span> om een geleidelijk in-/uitfadeeffect te creëren. Niet ondersteund in Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de tijd in seconden tussen de laatste muis-/aanraakgebeurtenis die is geregistreerd op de besturingsbalk en de verborgen tijdbalk. Indien ingesteld op <span class="codeph"> -1</span> de component activeert nooit het automatisch verborgen effect en blijft daarom altijd zichtbaar op het scherm. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duur</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u de duur in seconden in van de animatie voor in- en uitfaden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.5`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```

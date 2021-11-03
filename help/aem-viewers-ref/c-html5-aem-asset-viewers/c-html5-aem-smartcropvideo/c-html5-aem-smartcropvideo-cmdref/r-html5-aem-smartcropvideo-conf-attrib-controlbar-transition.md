---
description: Configuration attribute for Smart Crop Video Viewer.
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 133717c7-38d9-47b6-86bb-e23ebd8f147a
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# ControlBar.transition{#controlbar-transition}

Configuration attribute for Smart Crop Video Viewer.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duur`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|faden</span> </p> </td> 
   <td colname="col2"> <p> Geeft het effecttype aan dat wordt gebruikt om de besturingsbalk en de inhoud ervan weer te geven of te verbergen. </p> <p>Gebruiken <span class="codeph"> none</span> voor onmiddellijke weergave en verbergen. Gebruiken <span class="codeph"> vervagen</span> een geleidelijk in- en uitfadeeffect te bieden. </p> <p>Vervagen wordt niet ondersteund in Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u de tijd in seconden tussen de laatste muis-/aanraakgebeurtenis die door de besturingsbalk wordt geregistreerd en de tijdbalk. </p> <p> Indien ingesteld op <span class="codeph"> -1</span> de component activeert nooit het automatisch verborgen effect en blijft altijd zichtbaar op het scherm. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duur</span> </span> </p> </td> 
   <td colname="col2"> <p>Hiermee stelt u de duur in seconden in van de animatie voor in- en uitfaden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```

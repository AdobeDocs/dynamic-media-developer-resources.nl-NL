---
description: Configuration attribute for Video360 Viewer.
seo-description: Configuration attribute for Video360 Viewer.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
uuid: e8c1da96-3533-4d31-9ad3-569a87948ac6
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR-video
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# ControlBar.transition{#controlbar-transition}

Configuration attribute for Video360 Viewer.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delay ytohideduration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|faden</span> </p> </td> 
   <td colname="col2"> <p> Geeft het effecttype aan dat wordt gebruikt om de besturingsbalk en de inhoud ervan weer te geven of te verbergen. </p> <p>Gebruik <span class="codeph"> none</span> voor onmiddellijke weergave en verbergen. Gebruik <span class="codeph"> vervagen</span> om een geleidelijk in- en uitfadeeffect te bieden. </p> <p>Vervagen wordt niet ondersteund in Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u de tijd in seconden tussen de laatste muis-/aanraakgebeurtenis die door de besturingsbalk wordt geregistreerd en de tijdbalk. </p> <p> Indien ingesteld op <span class="codeph"> -1</span>, activeert de component nooit het effect voor automatisch verbergen en blijft deze altijd zichtbaar op het scherm. </p> </td> 
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


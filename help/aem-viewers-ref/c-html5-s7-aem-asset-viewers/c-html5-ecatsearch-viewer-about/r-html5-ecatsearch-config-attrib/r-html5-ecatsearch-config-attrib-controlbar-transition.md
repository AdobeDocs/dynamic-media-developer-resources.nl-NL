---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: 30f133bd-09c7-4d70-bcc4-d961bb028e55
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delay ytohideduration`*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|faden  </span> </p> </td> 
   <td colname="col2"> <p> Geeft het effecttype aan dat wordt gebruikt om de besturingsbalk en de inhoud ervan weer te geven of te verbergen. <span class="codeph"> geen </span> gebruiken voor onmiddellijke weergave en verbergen; <span class="codeph"> vervagen </span> biedt een geleidelijk in- en uitfade-effect (niet ondersteund in Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide  </span> </span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de tijd in seconden tussen de laatste muis-/aanraakgebeurtenis die door de besturingsbalk wordt geregistreerd en de tijdbalk. </p> <p> Indien ingesteld op <span class="codeph"> -1 </span>, activeert de component nooit het automatisch verbergen-effect en blijft deze altijd zichtbaar op het scherm. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duur  </span> </span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u de duur in seconden in van de animatie voor in- en uitfaden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel. Deze opdracht wordt genegeerd op aanraakapparaten, waar de besturingsbalk voor automatisch verbergen is uitgeschakeld.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]

---
title: ControlBar.transition
description: Geeft het effecttype aan dat wordt gebruikt om de besturingsbalk en de inhoud ervan weer te geven of te verbergen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: abe8affb-cbcd-4072-b2ed-91a398b1d678
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duur`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|faden </span> </p> </td> 
   <td colname="col2"> <p> Geeft het effecttype aan dat wordt gebruikt om de besturingsbalk en de inhoud ervan weer te geven of te verbergen. Gebruiken <span class="codeph"> none </span> voor onmiddellijke tonen en verbergen; <span class="codeph"> vervagen </span> biedt een geleidelijk in- en uitfadeeffect (niet ondersteund in Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide </span> </span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de tijd in seconden tussen de laatste muis-/aanraakgebeurtenis die door de besturingsbalk wordt geregistreerd en het verbergen van de tijdbesturingsbalk. </p> <p> Indien ingesteld op <span class="codeph"> -1 </span>De component activeert echter nooit het effect Automatisch verbergen en blijft altijd zichtbaar op het scherm. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duur </span> </span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u de duur in seconden in van de animatie voor in- en uitfaden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel. Deze opdracht wordt genegeerd op aanraakapparaten, waar de besturingsbalk voor automatisch verbergen is uitgeschakeld.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`

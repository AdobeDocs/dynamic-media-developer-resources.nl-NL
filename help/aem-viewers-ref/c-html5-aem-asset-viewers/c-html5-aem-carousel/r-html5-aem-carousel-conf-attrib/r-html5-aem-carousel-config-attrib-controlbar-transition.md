---
description: Configuration attribute for Carousel Viewer.
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---

# ControlBar.transition{#controlbar-transition}

Configuration attribute for Carousel Viewer.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *``*[, *`delay ytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|faden</span> </p> </td> 
   <td colname="col2"> <p> Geeft het effecttype aan dat wordt gebruikt om de besturingsbalk en de inhoud ervan weer te geven of te verbergen. </p> <p>Stel in op <span class="codeph"> none</span> voor onmiddellijke weergave/verbergen. </p> <p>Stel in op <span class="codeph"> vervagen</span> om een geleidelijk in-/uitfadeeffect te verkrijgen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de tijd in seconden tussen de laatste muis-/aanraakgebeurtenis die is geregistreerd op de besturingsbalk en de verborgen tijdbalk. </p> <p>Indien ingesteld op <span class="codeph"> -1</span>, activeert de component nooit het effect voor automatisch verbergen en blijft deze daarom altijd zichtbaar op het scherm. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duur</span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u de duur van de in- en uitfadeanimatie in seconden in. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel. Deze opdracht wordt genegeerd op aanraakapparaten waarbij de besturingsbalk voor automatisch verbergen is uitgeschakeld.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```

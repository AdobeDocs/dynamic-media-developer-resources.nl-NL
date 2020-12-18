---
description: 'null'
seo-description: 'null'
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: 803df8d4-6fb9-49ef-a097-c883d4115fad
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delay ytohideduration`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
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

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`

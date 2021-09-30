---
title: ZoomView.iscommand
description: De opdrachtreeks voor Beeldbewerking die wordt toegepast op de zoomafbeelding.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 1c24973e-1daf-4d9d-b97c-fb6a18f506ed
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# ZoomView.iscommand{#zoomview-iscommand}

De opdrachtreeks voor Beeldbewerking die wordt toegepast op de zoomafbeelding.

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> Indien opgegeven in de URL moeten alle exemplaren van <span class="codeph"> &amp;</span> en <span class="codeph"> =</span> HTTP-gecodeerd zijn als <span class="codeph"> %26</span> respectievelijk <span class="codeph"> %3D</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

Geen.

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

Wanneer opgegeven in de URL van de viewer:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Wanneer opgegeven in de configuratiegegevens:

`iscommand=op_sharpen=1&op_colorize=0xff0000`

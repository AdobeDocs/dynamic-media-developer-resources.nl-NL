---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.iscommand
solution: Experience Manager
title: ZoomView.iscommand
topic: Dynamic media
uuid: 0befdc0b-dd58-4aae-90e6-8c578f3b6c6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.iscommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> De opdrachtreeks voor Beeldbewerking die wordt toegepast op de zoomafbeelding. Indien opgegeven in de URL, moeten alle instanties van <span class="codeph"> &amp;</span> en <span class="codeph"> =</span> HTTP-gecodeerd zijn als respectievelijk <span class="codeph"> %26</span> en <span class="codeph"> %3D</span>. </p> <p> <p>Opmerking:  Bewerkingsopdrachten voor afbeeldingsgrootte worden niet ondersteund. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-50bcd15223174bb79ce08b31ea03d682}

Optioneel.

## Standaard {#section-7564169749ff4a4996049ea1148cb2a5}

Geen.

## Voorbeeld {#section-96e69b70365f461dae4399e49044ea2f}

Wanneer opgegeven in de URL van de viewer:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Wanneer opgegeven in de configuratiegegevens:

`iscommand=op_sharpen=1&op_colorize=0xff0000`

---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.iscommand
solution: Experience Manager
title: ZoomView.iscommand
topic: Dynamic media
uuid: e2a9388d-c753-4988-9aa0-73c4d0428d67
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.iscommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> De opdrachtreeks voor Beeldbewerking die wordt toegepast op de zoomafbeelding. Indien opgegeven in de URL, moeten alle instanties van <span class="codeph"> &amp;</span> en <span class="codeph"> =</span> HTTP-gecodeerd zijn als respectievelijk <span class="codeph"> %26</span> en <span class="codeph"> %3D</span>. </p> <p> <p>Opmerking:  Bewerkingsopdrachten voor afbeeldingsgrootte worden niet ondersteund. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Geen.

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

Wanneer opgegeven in de URL van de viewer:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Wanneer opgegeven in de configuratiegegevens:

`iscommand=op_sharpen=1&op_colorize=0xff0000`

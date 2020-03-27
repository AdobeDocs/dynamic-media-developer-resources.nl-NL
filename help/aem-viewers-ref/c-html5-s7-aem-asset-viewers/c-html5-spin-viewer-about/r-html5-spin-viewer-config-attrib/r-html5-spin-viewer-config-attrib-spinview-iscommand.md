---
description: 'null'
seo-description: 'null'
seo-title: SpinView.iscommand
solution: Experience Manager
title: SpinView.iscommand
topic: Dynamic media
uuid: 791164a1-93fa-411f-9fb8-f78efb96f16b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.iscommand{#spinview-iscommand}

` [SpinView.|<containerId>_spinView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> De opdrachttekenreeks voor Beeldbewerking die wordt toegepast op de draaiafbeelding. Indien opgegeven in de URL, moeten alle instanties van <span class="codeph"> &amp;</span> en <span class="codeph"> =</span> HTTP-gecodeerd zijn als respectievelijk <span class="codeph"> %26</span> en <span class="codeph"> %3D</span>. </p> <p> <p>Opmerking:  Bewerkingsopdrachten voor afbeeldingsgrootte worden niet ondersteund. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-924163cb2f6542499f49894becef7fb5}

Optioneel.

## Standaard {#section-7a2128fd488941948aff18421f533ccf}

Geen.

## Voorbeeld {#section-622348a84fbe4ff4b5dd7eb53b044d83}

Wanneer opgegeven in de URL van de viewer:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Wanneer opgegeven in de configuratiegegevens:

`iscommand=op_sharpen=1&op_colorize=0xff0000`

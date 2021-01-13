---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
topic: Dynamic media
uuid: a7d3b93b-daa2-4d08-8e2f-52e3ea11efbd
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 1%

---


# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> De opdrachttekenreeks voor Beeldserver die wordt toegepast op alle stalen. Als deze waarde is opgegeven in de URL, moet u alle gevallen van <span class="codeph"> &amp;</span> en <span class="codeph"> =</span> coderen als <span class="codeph"> %26</span> respectievelijk <span class="codeph"> %3D</span>. </p> <p> <p>Opmerking:  Bewerkingsopdrachten voor afbeeldingsgrootte worden niet ondersteund. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optioneel.

## Standaard {#section-fcb06fd8e7e945e590094efcf9a1d510}

Geen.

## Voorbeeld {#section-3a188ab955c445bcb2efa3c49722c10d}

Wanneer opgegeven in de URL van de viewer.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Wanneer opgegeven in de configuratiegegevens.

`iscommand=op_sharpen=1&op_colorize=0xff0000`

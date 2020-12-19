---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.iscommand
solution: Experience Manager
title: FlyoutZoomView.iscommand
topic: Dynamic media
uuid: 1e8dcafb-33ef-42ea-8636-b3b7de81dfbd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 1%

---


# FlyoutZoomView.iscommand{#flyoutzoomview-iscommand}

` [FlyoutZoomView.|<containerId>_flyout.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> </p> <p>De opdrachttekenreeks voor Beeldbewerking die wordt toegepast op de hoofdafbeelding FlyoutZoomView en de ingezoomde weergave. Als deze waarde is opgegeven in de URL, moet u alle gevallen van <span class="codeph"> &amp;</span> en <span class="codeph"> =</span> coderen als <span class="codeph"> %26</span> respectievelijk <span class="codeph"> %3D</span>. </p> <p> <p>Opmerking:  Bewerkingsopdrachten voor afbeeldingsgrootte worden niet ondersteund. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optioneel.

## Standaard {#section-a08032f0fcf041c09e63c0238a339fc9}

Geen.

## Voorbeeld {#section-0338be21edd04ff1a3bed5c8319b61a4}

Wanneer opgegeven in de URL van de viewer:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Indien opgegeven in de configuratiegegevens:

`iscommand=op_sharpen=1&op_colorize=0xff0000`

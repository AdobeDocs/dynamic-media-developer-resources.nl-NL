---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,Zoomen
role: Developer,User
exl-id: e375f3ec-82f3-441d-9e01-d0ea5605bd25
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '68'
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

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

Geen.

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

Wanneer opgegeven in de URL van de viewer.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Wanneer opgegeven in de configuratiegegevens.

`iscommand=op_sharpen=1&op_colorize=0xff0000`

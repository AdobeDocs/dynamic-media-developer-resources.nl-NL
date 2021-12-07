---
title: PanoramicView.iscommand
description: Configuration attribute for Panorama Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 1%

---

# PanoramicView.iscommand{#panoramicview-iscommand}

Configuration attribute for Panorama Viewer.

` [PanoramicView.|<containerId>_panoramicView.]iscommand=isCommand `

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> De opdrachttekenreeks voor Beeldserver die op de afbeelding wordt toegepast.  Als dit in de URL is opgegeven, moet u ervoor zorgen dat alle instanties van <span class="codeph"> &amp;</span> en <span class="codeph"> =</span> als <span class="codeph"> %26</span> en <span class="codeph"> %3D</span>, respectievelijk. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

Geen standaardwaarde.

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

Wanneer opgegeven in de URL van de viewer.

```
iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000
```

Indien opgegeven in de configuratiegegevens.

```
iscommand=op_sharpen=1&op_colorize=0xff0000
```

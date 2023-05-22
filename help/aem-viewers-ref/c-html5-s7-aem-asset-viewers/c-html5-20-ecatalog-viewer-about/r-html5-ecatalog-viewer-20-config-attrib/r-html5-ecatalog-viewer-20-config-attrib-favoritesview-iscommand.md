---
title: FavoritesView.iscommand
description: De opdrachtreeks Beeldbewerking die op alle miniaturen wordt toegepast.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 1b6198f4-367d-437a-b8b1-206519567af0
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 0%

---

# FavoritesView.iscommand{#favoritesview-iscommand}

De opdrachtreeks Beeldbewerking die op alle miniaturen wordt toegepast.

` [FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Indien opgegeven in de URL, komen alle <span class="codeph"> &amp;</span> en <span class="codeph"> =</span> moet HTTP-gecodeerd zijn als <span class="codeph"> %26</span> en <span class="codeph"> %3D</span>, respectievelijk. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

Geen.

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

Wanneer opgegeven in de URL van de viewer.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Indien opgegeven in de configuratiegegevens.

`iscommand=op_sharpen=1&op_colorize=0xff0000`

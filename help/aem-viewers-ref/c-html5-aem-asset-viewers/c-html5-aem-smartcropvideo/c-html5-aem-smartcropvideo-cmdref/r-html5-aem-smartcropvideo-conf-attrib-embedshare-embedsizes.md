---
title: EmbedShare.embedsizes
description: Configuration attribute for Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 3%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

Configuration attribute for Smart Crop Video Viewer.

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *`width`*, *`height`*[,0|1][; *`width`*, *`height`*[,0|1]]`

Hiermee geeft u een lijst op met insluitgrootten voor de combinatievak Grootte in het modale dialoogvenster voor insluiten en delen.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p> Breedte insluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> height </span> </span> </p> </td> 
   <td colname="col2"> <p>Hoogte insluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Hiermee wordt opgegeven of dit lijstitem in eerste instantie moet worden geselecteerd in het keuzemenu met invoervak. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`1280,960;640,480;320,240`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
embedsizes=800,600;640,480,1
```
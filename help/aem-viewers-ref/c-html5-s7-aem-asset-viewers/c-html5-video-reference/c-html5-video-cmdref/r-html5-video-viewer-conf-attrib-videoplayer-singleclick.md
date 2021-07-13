---
description: Configuration attribute for Video Viewer.
solution: Experience Manager
title: VideoPlayer.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 1%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Configuration attribute for Video Viewer.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Vormt de afbeelding van een enkele klik/tik om afspelen/pauzeren in en uit te schakelen. Als u instelt op <span class="codeph"> none</span>, wordt een enkele klik/tik uitgeschakeld om af te spelen/te pauzeren. Als ingesteld op <span class="codeph"> playPause</span>, klikt u op de videoschakeloptie tussen het afspelen en pauzeren van de video. Op sommige apparaten kunt u native besturingselementen gebruiken. In dat geval is het gedrag <span class="codeph"> singleclick</span> uitgeschakeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```

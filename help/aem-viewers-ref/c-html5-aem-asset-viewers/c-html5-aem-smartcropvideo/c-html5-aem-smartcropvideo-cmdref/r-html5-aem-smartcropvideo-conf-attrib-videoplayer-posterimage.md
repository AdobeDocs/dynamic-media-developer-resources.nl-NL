---
title: SmartCropVideoPlayer.posterimage
description: Configuration attribute for Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# SmartCropVideoPlayer.posterimage{#smartcropvideoplayer-posterimage}

Configuration attribute for Smart Crop Video Viewer.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> De afbeelding die op het eerste frame moet worden weergegeven voordat de video wordt afgespeeld, is opgelost tegen <span class="codeph"> serverurl</span>. Indien opgegeven in de URL, codeert HTTP het volgende: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> als <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> als <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> als <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Als de <span class="codeph"><span class="varname"> image_id</span></span> waarde wordt weggelaten, probeert de component om de standaardposterafbeelding voor dat element te gebruiken. </p> <p>Wanneer de video is opgegeven als een pad, wordt de standaard posterafbeeldingencatalogus-id afgeleid van het videopad als de <span class="codeph"> catalog_id/image_id</span> paar. De <span class="codeph"> catalog_id</span> komt overeen met het eerste token in het pad en <span class="codeph"> image_id</span> Dit is de naam van de video waarvan de extensie is verwijderd. Als de afbeelding met die id niet bestaat, wordt de posterafbeelding niet weergegeven. </p> <p>Als u de standaardposterafbeelding niet wilt weergeven, geeft u <span class="codeph"> none</span> als de waarde van de posterafbeelding. Als alleen de <span class="codeph"><span class="varname"> isCommands</span></span> opgegeven, worden de opdrachten toegepast op de standaardposterafbeelding voordat de afbeelding wordt weergegeven. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

Geen.

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```

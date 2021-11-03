---
title: VideoTime.timepattern
description: Configuration attribute for Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 1fe2876c-c59a-4e0c-b429-34cc3244d920
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# VideoTime.timepattern{#videotime-timepattern}

Configuration attribute for Smart Crop Video Viewer.

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Plaatst het patroon voor de tijd die in de controlebar wordt getoond, waar <span class="codeph"> h</span> is uren, <span class="codeph"> m</span> minuten is, en <span class="codeph"> s</span> is seconden. </p> <p>Het aantal letters dat voor elke tijdeenheid wordt gebruikt, bepaalt het aantal cijfers dat voor de eenheid moet worden weergegeven. Als het getal niet in de opgegeven cijfers past, wordt de equivalente waarde weergegeven in de volgende eenheid. </p> <p>Als de huidige filmtijd bijvoorbeeld 67 minuten en 5 seconden is, wordt het tijdpatroon weergegeven <span class="codeph"> m:ss</span> wordt weergegeven als 67:05. Dezelfde tijd wordt weergegeven als 1:07:5 als het opgegeven tijdpatroon <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```

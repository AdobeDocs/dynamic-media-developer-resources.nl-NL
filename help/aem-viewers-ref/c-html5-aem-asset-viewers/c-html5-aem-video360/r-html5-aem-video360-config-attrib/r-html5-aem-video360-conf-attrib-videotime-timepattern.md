---
description: Configuration attribute for Video360 Viewer.
seo-description: Configuration attribute for Video360 Viewer.
seo-title: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
topic: Dynamic media
uuid: fe145e6f-742e-44fc-b225-187a86b6700e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoTime.timepattern{#videotime-timepattern}

Configuration attribute for Video360 Viewer.

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u het patroon in voor de tijd die wordt weergegeven op de besturingsbalk, waarbij <span class="codeph"> h</span> uren is, <span class="codeph"> m</span> minuten en <span class="codeph"> s</span> seconden. </p> <p>Het aantal letters dat voor elke tijdeenheid wordt gebruikt, bepaalt het aantal cijfers dat voor de eenheid moet worden weergegeven. Als het getal niet in de opgegeven cijfers past, wordt de equivalente waarde weergegeven in de volgende eenheid. </p> <p>Als de huidige filmtijd bijvoorbeeld 67 minuten en 5 seconden is, wordt het tijdpatroon <span class="codeph"> m:ss</span> weergegeven als 67:05. Dezelfde tijd wordt weergegeven als 1:07:5 als het opgegeven tijdpatroon <span class="codeph"> h:mm:s</span>is. </p> </td> 
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


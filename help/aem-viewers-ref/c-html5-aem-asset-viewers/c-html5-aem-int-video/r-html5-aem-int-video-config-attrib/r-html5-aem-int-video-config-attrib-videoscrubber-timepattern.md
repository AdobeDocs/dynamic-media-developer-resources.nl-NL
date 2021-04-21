---
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
title: VideoScrubber.timepattern
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: d39ddf38-9157-412a-83a4-c1af4944a904
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

Configuration attribute for Interactive Video Viewer.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Hiermee stelt u het patroon in voor de tijd die wordt weergegeven in de tijdballon, waarbij <span class="codeph"> h</span> uren, <span class="codeph"> m</span> minuten en <span class="codeph"> s</span> seconden vertegenwoordigt. </p> <p>Het aantal letters dat voor elke tijdeenheid wordt gebruikt, bepaalt het aantal cijfers dat voor de eenheid moet worden weergegeven. Als het getal niet in de opgegeven cijfers past, wordt de equivalente waarde weergegeven in de volgende eenheid. </p> <p>Als de huidige filmtijd bijvoorbeeld 67 minuten en 5 seconden is, wordt een tijdpatroon van <span class="codeph"> m:ss</span> weergegeven als 67:05. Dezelfde tijd wordt weergegeven als 1:07:5 als het tijdpatroon <span class="codeph"> h:mm:s</span> is. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`mm:s`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```

---
title: VideoScrubber.timepattern
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: d39ddf38-9157-412a-83a4-c1af4944a904
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

Configuration attribute for Interactive Video Viewer.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Hiermee wordt het patroon ingesteld voor de tijd die in de tijdballon wordt weergegeven, waarbij <span class="codeph"> h</span> vertegenwoordigt uren, <span class="codeph"> m</span> gedurende minuten, en <span class="codeph"> s</span> voor seconden. </p> <p>Het aantal letters dat voor elke tijdeenheid wordt gebruikt, bepaalt het aantal cijfers dat voor de eenheid moet worden weergegeven. Als het getal niet in de opgegeven cijfers past, wordt de equivalente waarde weergegeven in de volgende eenheid. </p> <p>Als de huidige filmtijd bijvoorbeeld 67 minuten en 5 seconden is, wordt een tijdpatroon van <span class="codeph"> m:ss</span> wordt weergegeven als 67:05. Dezelfde tijd wordt weergegeven als 1:07:5 als het tijdpatroon <span class="codeph"> h:mm:s</span>. </p> </td> 
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

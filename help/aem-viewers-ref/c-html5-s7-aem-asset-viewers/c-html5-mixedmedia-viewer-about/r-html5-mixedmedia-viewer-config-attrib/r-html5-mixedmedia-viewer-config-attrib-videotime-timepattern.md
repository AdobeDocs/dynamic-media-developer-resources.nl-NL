---
description: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
uuid: 57c86b63-7495-4f6f-bd30-8c4ebf017e36
feature: Dynamic Media Classic,Viewers,SDK/API,Mediasets mixen
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# VideoTime.timepattern{#videotime-timepattern}

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Plaatst het patroon voor de tijd die in de controlebar wordt getoond, waar <span class="codeph"> h</span> uren is, <span class="codeph"> m</span> minuten is, en <span class="codeph"> s</span> seconden is. </p> <p>Het aantal letters dat voor elke tijdeenheid wordt gebruikt, bepaalt het aantal cijfers dat voor de eenheid moet worden weergegeven. Als het getal niet in de opgegeven cijfers past, wordt de equivalente waarde weergegeven in de volgende eenheid. </p> <p>Als de huidige filmtijd bijvoorbeeld 67 minuten en 5 seconden is, wordt het tijdpatroon <span class="codeph"> m:ss</span> weergegeven als 67:05. Dezelfde tijd wordt weergegeven als 1:07:5 als het opgegeven tijdpatroon <span class="codeph"> h:mm:s</span> is. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`

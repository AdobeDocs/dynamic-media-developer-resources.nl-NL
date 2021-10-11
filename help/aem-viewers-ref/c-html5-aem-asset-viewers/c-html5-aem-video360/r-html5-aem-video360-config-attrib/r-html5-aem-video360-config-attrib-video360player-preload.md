---
title: Video360Player.preload
description: Geeft aan of de viewer begint met het laden van video-inhoud voordat het afspelen wordt gestart.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 33c28ed3-cdb3-4b14-8cc7-90f77ec9a3bb
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 5%

---

# Video360Player.preload{#video-player-preload}

Geeft aan of de viewer begint met het laden van video-inhoud voordat het afspelen wordt gestart.

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Als deze waarde wordt ingesteld op <span class="codeph"> 1 </span>, wordt de video direct gedownload nadat het element is ingesteld. Anders begint het voorladen pas nadat het afspelen is gestart door de eindgebruiker of een API-aanroep. </p> <p>Als de waarde <span class="codeph"> 0 </span> is, werken bepaalde functies mogelijk pas wanneer het afspelen wordt gestart. Met name wordt het videoframe niet bijgewerkt door de zoekbewerking. Als de posterafbeelding is uitgeschakeld, wordt de viewer weergegeven als een leeg gebied in plaats van als het eerste videoframe. </p> <p>Het uitschakelen van het vooraf laden van video kan in bepaalde versies van Internet Explorer 11 en Edge-browsers worden genegeerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`

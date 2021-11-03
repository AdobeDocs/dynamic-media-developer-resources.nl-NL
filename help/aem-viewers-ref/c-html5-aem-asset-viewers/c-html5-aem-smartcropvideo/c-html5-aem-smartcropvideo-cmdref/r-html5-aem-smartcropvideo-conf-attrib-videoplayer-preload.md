---
description: Geeft aan of de viewer begint met het laden van video-inhoud voordat het afspelen wordt gestart.
solution: Experience Manager
title: SmartCropVideoPlayer.preload
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: cee887f6-bbd9-46dd-aa41-03493596fcf4
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 1%

---

# SmartCropVideoPlayer.preload{#smartcropvideoplayer-preload}

Geeft aan of de viewer begint met het laden van video-inhoud voordat het afspelen wordt gestart.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Indien ingesteld op <span class="codeph"> 1 </span> de video wordt meteen gedownload nadat het element is ingesteld; anders, begint preload slechts nadat het playback door de eindgebruiker of een API vraag in werking wordt gesteld. </p> <p>Indien ingesteld op <span class="codeph"> 0 </span> bepaalde functies werken mogelijk pas nadat het afspelen is gestart; met name wordt het videoframe niet bijgewerkt door de zoekbewerking. Als de posterafbeelding is uitgeschakeld, wordt de viewer weergegeven als een leeg gebied in plaats van als het eerste videoframe. </p> <p>Houd er rekening mee dat het uitschakelen van het vooraf laden van video kan worden genegeerd in bepaalde versies van Internet Explorer 11 en Edge browsers. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`

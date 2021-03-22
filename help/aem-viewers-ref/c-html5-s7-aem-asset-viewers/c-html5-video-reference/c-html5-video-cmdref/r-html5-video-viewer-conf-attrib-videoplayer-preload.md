---
description: Geeft aan of de viewer begint met het laden van video-inhoud voordat het afspelen wordt gestart.
seo-description: Geeft aan of de viewer begint met het laden van video-inhoud voordat het afspelen wordt gestart.
seo-title: VideoPlayer.preload
solution: Experience Manager
title: VideoPlayer.preload
uuid: 2aaae96d-d42d-4984-aec9-86e06b3c711c
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---


# VideoPlayer.preload{#videoplayer-preload}

Geeft aan of de viewer begint met het laden van video-inhoud voordat het afspelen wordt gestart.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Indien ingesteld op <span class="codeph"> 1 </span>, wordt de video direct gedownload nadat het element is ingesteld. anders, begint preload slechts nadat het playback door de eindgebruiker of een API vraag in werking wordt gesteld. </p> <p>Indien ingesteld op <span class="codeph"> 0 </span>, werken bepaalde functies mogelijk pas wanneer het afspelen wordt gestart; met name wordt het videoframe niet bijgewerkt door de zoekbewerking. Als de posterafbeelding is uitgeschakeld, wordt de viewer weergegeven als een leeg gebied in plaats van als het eerste videoframe. </p> <p>Houd er rekening mee dat het uitschakelen van het vooraf laden van video kan worden genegeerd in bepaalde versies van Internet Explorer 11 en Edge browsers. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`

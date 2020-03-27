---
description: Geeft aan of de viewer begint met het laden van video-inhoud voordat het afspelen wordt gestart.
seo-description: Geeft aan of de viewer begint met het laden van video-inhoud voordat het afspelen wordt gestart.
seo-title: Video360Player.preload
solution: Experience Manager
title: Video360Player.preload
topic: Dynamic media
uuid: 6e3b95b8-d585-4164-8665-6211000689fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Player.preload{#video-player-preload}

Geeft aan of de viewer begint met het laden van video-inhoud voordat het afspelen wordt gestart.

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Indien ingesteld op <span class="codeph"> 1, </span> wordt de video direct gedownload nadat het element is ingesteld. anders, begint preload slechts nadat het playback door de eindgebruiker of een API vraag in werking wordt gesteld. </p> <p>Als de instelling <span class="codeph"> </span> 0 is, werken bepaalde functies mogelijk pas wanneer het afspelen wordt gestart. met name wordt het videoframe niet bijgewerkt door de zoekbewerking. Als de posterafbeelding is uitgeschakeld, wordt de viewer weergegeven als een leeg gebied in plaats van als het eerste videoframe. </p> <p>Houd er rekening mee dat het uitschakelen van het vooraf laden van video kan worden genegeerd in bepaalde versies van Internet Explorer 11 en Edge browsers. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`

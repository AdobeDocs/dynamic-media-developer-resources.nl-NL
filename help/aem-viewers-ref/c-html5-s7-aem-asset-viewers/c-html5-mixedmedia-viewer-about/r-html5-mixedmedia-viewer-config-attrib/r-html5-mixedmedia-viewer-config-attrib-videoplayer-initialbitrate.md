---
description: 'null'
seo-description: 'null'
seo-title: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
topic: Dynamic media
uuid: 11426516-8336-4186-84b4-15ce5ec7e764
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> waarde </span></span> </p> </td> 
   <td colname="col2"> <p>Stelt de videobitsnelheid in kbits per seconde of kbps in die wordt gebruikt voor de eerste weergave van video op desktops. </p> <p>Als deze bitsnelheidwaarde niet bestaat in de adaptieve videoset, start de videospeler de video met de eerstvolgende laagste bitsnelheid. </p> <p>Wanneer ingesteld op <span class="codeph"> 0, begint </span> de videospeler met de laagst mogelijke bitsnelheid. Alleen van toepassing op systemen die geen native ondersteuning bieden voor HTML5 HLS-video (Firefox-, Chrome- en Internet Explorer 11-browsers in Windows 10) en wanneer de afspeelmodus is ingesteld op <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`

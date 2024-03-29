---
title: VideoPlayer.posterimage
description: VideoPlayer.posterimage
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bcbba4c5-b758-4049-b4c2-f1c48cc2de7e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> De afbeelding die op het eerste frame moet worden weergegeven voordat de video wordt afgespeeld, is opgelost tegen <span class="codeph"> serverurl</span>. Indien opgegeven in de URL, codeert HTTP het volgende: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> als <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> als <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> als <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Als de <span class="codeph"><span class="varname"> image_id</span></span> waarde wordt weggelaten, probeert de component om de standaardposterafbeelding voor dat element te gebruiken. </p> <p>Wanneer de video is opgegeven als een pad, wordt de standaard-id van de posterafbeeldingencatalogus afgeleid van het videopad als de <span class="codeph"> catalog_id/image_id</span> paar waar <span class="codeph"> catalog_id</span> komt overeen met de eerste token in het pad. En <span class="codeph"> image_id</span> Dit is de naam van de video waarvan de extensie is verwijderd. Als de afbeelding met die id niet bestaat, wordt de posterafbeelding niet weergegeven. </p> <p>Als u de standaardposterafbeelding niet wilt weergeven, geeft u <span class="codeph"> none</span> als de waarde van de posterafbeelding. Als alleen de <span class="codeph"><span class="varname"> isCommands</span></span> opgegeven, worden de opdrachten toegepast op de standaardposterafbeelding voordat de afbeelding wordt weergegeven. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Geen.

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`

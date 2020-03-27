---
description: 'null'
seo-description: 'null'
seo-title: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
topic: Dynamic media
uuid: 28663f44-11cb-4522-bd12-d6bec17b4173
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> De afbeelding die op het eerste frame moet worden weergegeven voordat de video wordt afgespeeld, wordt omgezet in <span class="codeph"> serverURL</span>. Indien opgegeven in de URL, codeert HTTP het volgende: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> als <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> als <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> als <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Als de waarde <span class="codeph"><span class="varname"> image_id</span></span> wordt weggelaten, probeert de component om de standaardposterafbeelding voor dat element te gebruiken. </p> <p>Wanneer de video wordt opgegeven als een pad, wordt de standaard posterafbeeldingencatalogus-id afgeleid van het videopad als het <span class="codeph"> catalog_id/image_id</span> -paar, waarbij <span class="codeph"> catalog_id</span> overeenkomt met het eerste token in het pad en <span class="codeph"> image_id</span> de naam van de video is terwijl de extensie is verwijderd. Als de afbeelding met die id niet bestaat, wordt de posterafbeelding niet weergegeven. </p> <p>Als u wilt voorkomen dat de standaardposterafbeelding wordt weergegeven, geeft u <span class="codeph"> geen</span> op als waarde voor de posterafbeelding. Als alleen <span class="codeph"><span class="varname"> isCommands</span></span> worden opgegeven, worden de opdrachten toegepast op de standaardposterafbeelding voordat de afbeelding wordt weergegeven. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-65be9301796240e38f31818229da7acc}

Optioneel.

## Standaard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Geen.

## Voorbeeld {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`

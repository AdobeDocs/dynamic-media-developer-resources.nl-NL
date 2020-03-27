---
description: JavaScript API-referentie voor Video Viewer
seo-description: JavaScript API-referentie voor Video Viewer
seo-title: setVideo
solution: Experience Manager
title: setVideo
topic: Dynamic media
uuid: 0a1b3caa-ded6-4020-962c-41c3ece0a865
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setVideo{#setvideo}

JavaScript API-referentie voor Video Viewer

`setVideo(videoUrl[, data])`

Hiermee worden nieuwe externe video en optionele aanvullende videogegevens ingesteld. Kan op elk moment worden aangeroepen, zowel voor als na `init()`. Als de video na deze gebeurtenis wordt aangeroepen, wordt de video tijdens runtime omgewisseld. `init()`

Zie ook [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Parameters {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> } Een absolute URL naar de nieuwe video </span>} . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> data </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} JSON-object met de volgende optionele velden (hoofdlettergevoelig): </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> posterafbeelding </span> - Afbeelding die op het eerste frame wordt weergegeven voordat de video wordt afgespeeld. Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> bijschrift </span> - locatie van het nieuwe bijschriftbestand. Als er geen bijschriftbestand is opgegeven, wordt de knop Bijschrift niet weergegeven in de gebruikersinterface. </li> 
      <li id="li_A43A1BAB6B0F4A7981F71408F08F07D1"> <span class="codeph"> navigatie </span> - URL of pad naar WebVTT-navigatie-inhoud. Het WebVTT-bestand moet worden aangeboden door Image Serving. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Scene7SharedAssets/Glacier_Climber_MP4")
```


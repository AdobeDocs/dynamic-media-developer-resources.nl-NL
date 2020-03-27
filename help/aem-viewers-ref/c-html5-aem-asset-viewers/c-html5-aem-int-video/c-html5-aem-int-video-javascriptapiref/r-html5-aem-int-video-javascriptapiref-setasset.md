---
description: JavaScript API-referentie voor Interactive Video Viewer.
seo-description: JavaScript API-referentie voor Interactive Video Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 80c670a4-1251-47f5-a66b-8ba5019df1ce
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# setAsset{#setasset}

JavaScript API-referentie voor Interactive Video Viewer.

`setAsset(asset[, data])`

Hiermee stelt u het nieuwe element en optionele aanvullende elementgegevens in. U kunt deze parameter op elk gewenst moment aanroepen, voor of na `init()`. Als deze functie na deze gebeurtenis wordt aangeroepen, wordt het element tijdens de runtime omgewisseld. `init()`

Zie ook [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> element </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} new asset ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> data </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> JSON </span>} JSON-object met de volgende optionele velden (hoofdlettergevoelig): </p> <p> 
     <ul id="ul_924FB99ACF0F43699CD229593F1C1384"> 
      <li id="li_F3CFEF28BCB7450991EFE0BD4EB28E36"> <span class="codeph"> Voorwaardelijke afbeelding - Afbeelding die wordt weergegeven in het eerste frame voordat de video wordt afgespeeld. </span> Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-posterimage.md#reference-8e8e2b3e7e9c4ee8b6dadf90cef494f7" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_D6C3E543C70942C582020780E2DF74C8"> <span class="codeph"> bijschrift </span> - locatie van het nieuwe bijschriftbestand. Als deze optie niet is opgegeven, is de bijschriftknop niet zichtbaar in de gebruikersinterface. </li> 
      <li id="li_BF866BD7275E450EA08A0E72FAA9D3AE"> <span class="codeph"> navigatie </span> - URL of pad naar de WebVTT-navigatie-inhoud. Het WebVTT-bestand moet worden aangeboden door Image Serving. </li> 
      <li id="li_0C0EC5AB00554EC6AA01F60684A40213"> <span class="codeph"> interactiveData </span> - URL of pad naar interactieve WebVTT-gegevensinhoud. Het WebVTT-bestand moet worden aangeboden door Image Serving. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4")
```


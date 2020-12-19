---
description: JavaScript API-referentie voor gemengde media-viewer.
seo-description: JavaScript API-referentie voor gemengde media-viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 8c341a8a-25b5-4db9-ad1a-919ded79f2ed
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---


# setAsset{#setasset}

JavaScript API-referentie voor gemengde media-viewer.

` setAsset( *`element`*[,data]))`

Hiermee stelt u het nieuwe element en optionele aanvullende elementgegevens in. U kunt deze parameter op elk ogenblik roepen, of vóór of na `init()`. Als deze wordt aangeroepen na `init()`, wisselt de viewer het element tijdens runtime om.

Zie ook [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Parameters {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

` *`element`*` - { `String`} nieuwe element-id of expliciete gemengde mediaset, met optionele Image Serving-modifiers toegevoegd na  `?`.

Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer.

` *`de locatie van het nieuwe bijschriftbestand`*`  ( { `JSON`} dataLocatie).

Als deze optie niet is opgegeven, is de bijschriftknop niet zichtbaar in de gebruikersinterface. Bijschriften die met deze parameter worden opgegeven, gelden voor de video die als eerste in de gemengde mediaset wordt geplaatst. volgende video&#39;s worden zonder bijschriften afgespeeld. Deze viewer ondersteunt de volgende component-id&#39;s:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Component-id </p> </th> 
   <th colname="col2" class="entry"> <p>Naam van de klasse Viewer SDK </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posterimage  </span> </p> </td> 
   <td colname="col2"> <p>Afbeelding die op het eerste frame moet worden weergegeven voordat de video wordt afgespeeld. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bijschrift  </span> </p> </td> 
   <td colname="col2"> <p> Locatie van het nieuwe bijschriftbestand. </p> <p>Als deze optie niet is opgegeven, is de bijschriftknop niet zichtbaar in de gebruikersinterface. Bijschriften die met deze parameter worden opgegeven, worden toegepast op de video die als eerste in de mediaset wordt weergegeven. Volgende video's worden zonder bijschriften afgespeeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Verwijzing naar enkele mediaset:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

Expliciete mediaset:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

De optie Verscherpen is toegevoegd aan alle afbeeldingen in de set:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```


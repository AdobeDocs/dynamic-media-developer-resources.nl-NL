---
title: setAsset
description: JavaScript API-referentie voor Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4fc94f30-e330-4c8a-b6da-d870e4f8e4ab
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# setAsset{#setasset}

JavaScript API-referentie voor Video Viewer.

` setAsset( *`element`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> element </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} nieuwe element-id, expliciete afbeeldingsset of expliciete afbeeldingsset met frame-specifieke opties voor afbeeldingsweergave, met optionele algemene opties voor afbeeldingsweergave toegevoegd na "?". </p> <p> Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer. </p> </td> 
  </tr> 
 </tbody> 
</table>

Hiermee stelt u het nieuwe element in. U kunt deze parameter op elk gewenst moment vóór of na `init()`. Als het wordt aangeroepen na `init()`, wordt het element tijdens runtime vervangen door de viewer.

Zie ook [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Eén beeldverwijzing, als volgt:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Eén verwijzing naar een afbeeldingsset die als volgt in een catalogus is gedefinieerd:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Expliciete afbeeldingsset als volgt:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Expliciete afbeelding ingesteld met frame-specifieke opties voor afbeeldingsservers, als volgt:

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

De optie Verscherpen wordt als volgt toegevoegd aan alle afbeeldingen in de set:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```

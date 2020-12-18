---
description: JavaScript API-referentie voor de Basic Zoom Viewer.
seo-description: JavaScript API-referentie voor de Basic Zoom Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: af433f15-34a0-4867-97c5-acab47e3e008
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# setAsset{#setasset}

JavaScript API-referentie voor de Basic Zoom Viewer.

` setAsset( *`element`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> element</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} nieuwe element-id, met optionele IS-modifiers toegevoegd na "?" </p> <p> Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer. </p> </td> 
  </tr> 
 </tbody> 
</table>

Hiermee stelt u het nieuwe element in. U kunt deze parameter op elk ogenblik roepen, of vóór of na `init()`. Als deze wordt aangeroepen na `init()`, wisselt de viewer het element tijdens runtime om.

Zie ook [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Verwijzing naar één afbeelding:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

De optie Verscherpen is toegevoegd aan alle afbeeldingen in de set:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B?op_sharpen=1")
```


---
description: JavaScript API-referentie voor Video Viewer.
seo-description: JavaScript API-referentie voor Video Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: f106b3d4-880e-4ba3-ae47-a005af5c0f1b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAsset{#setasset}

JavaScript API-referentie voor Video Viewer.

` setAsset( *`element`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> actief </span></span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> } Tekenreeks </span>} nieuwe element-id, expliciete afbeeldingsset of expliciete afbeeldingsset met frame-specifieke opties voor Beeldbewerking, met optionele algemene opties voor Beeldbewerking toegevoegd na "?". </p> <p> Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer. </p> </td> 
  </tr> 
 </tbody> 
</table>

Hiermee stelt u het nieuwe element in. U kunt deze parameter op elk gewenst moment aanroepen, voor of na `init()`. Als deze functie na deze gebeurtenis wordt aangeroepen, wordt het element tijdens de runtime omgewisseld. `init()`

Zie ook [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Verwijzing naar één afbeelding:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Eén verwijzing naar een afbeeldingsset die is gedefinieerd in een catalogus:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Expliciete afbeeldingsset:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Expliciete afbeelding ingesteld met frame-specifieke opties voor afbeeldingsservers:

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

De optie Verscherpen is toegevoegd aan alle afbeeldingen in de set:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```


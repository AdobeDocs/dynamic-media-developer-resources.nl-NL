---
title: setAsset
description: JavaScript API-referentie voor Inline Zoom Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 62b46ad5-90b7-49e1-a426-87fbe956f07e
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# setAsset{#setasset}

JavaScript API-referentie voor Inline Zoom Viewer.

` setAsset( *`element`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> element</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} nieuwe element-id, expliciete afbeeldingsset of expliciete afbeelding die is ingesteld met frame-specifieke opties voor afbeeldingsweergave, met optionele algemene opties voor afbeeldingsweergave die na <span class="codeph"> ?</span>. </p> <p> Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer. </p> </td> 
  </tr> 
 </tbody> 
</table>

Hiermee stelt u het nieuwe element in. U kunt deze parameter op elk gewenst moment vóór of na `init()`. Als het wordt aangeroepen na `init()`, wordt het element tijdens runtime vervangen door de viewer.

Zie ook [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

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
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```

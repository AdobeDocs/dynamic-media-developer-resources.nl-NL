---
description: JavaScript API-referentie voor de Spin Viewer.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,Draaiensets
role: Developer,User
exl-id: c94c8db4-d448-4c1c-875a-3a33a03f7dd8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# setAsset{#setasset}

JavaScript API-referentie voor de Spin Viewer.

` setAsset( *`element`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> element</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> Tekenreeks</span>} nieuwe element-id, enkeldimensionale of multidimensionale draaiing ingesteld met optionele Image Serving modifiers toegevoegd na <span class="codeph"> ?</span>. </p> <p> Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer. </p> </td> 
  </tr> 
 </tbody> 
</table>

Hiermee stelt u het nieuwe element in. U kunt deze parameter op elk ogenblik roepen, of vóór of na `init()`. Als deze wordt aangeroepen na `init()`, wisselt de viewer het element tijdens runtime om.

Zie ook [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Eén verwijzing naar een centrifugeset die is gedefinieerd in een catalogus:

```
<instance>.setAsset("Scene7SharedAssets/SpinSet_Sample")
```

Expliciete centrifugeerset:

```
<instance>.setAsset("Scene7SharedAssets/Frame-1,Scene7SharedAssets/Frame-2,Scene7SharedAssets/Frame-3,Scene7SharedAssets/Frame-4,Scene7SharedAssets/Frame-5,Scene7SharedAssets/Frame-6,Scene7SharedAssets/Frame-7,Scene7SharedAssets/Frame-8")
```

Expliciete multidimensionale centrifuge:

```
<instance>.setAsset("((Scene7SharedAssets/ring1-25,Scene7SharedAssets/ring1-26,Scene7SharedAssets/ring1-27,Scene7SharedAssets/ring1-28,Scene7SharedAssets/ring1-29,Scene7SharedAssets/ring1-30,Scene7SharedAssets/ring1-31,Scene7SharedAssets/ring1-32,Scene7SharedAssets/ring1-33,Scene7SharedAssets/ring1-34,Scene7SharedAssets/ring1-35,Scene7SharedAssets/ring1-36),{Scene7SharedAssets/ring1-13,Scene7SharedAssets/ring1-14,Scene7SharedAssets/ring1-15,Scene7SharedAssets/ring1-16,Scene7SharedAssets/ring1-17,Scene7SharedAssets/ring1-18,Scene7SharedAssets/ring1-19,Scene7SharedAssets/ring1-20,Scene7SharedAssets/ring1-21,Scene7SharedAssets/ring1-22,Scene7SharedAssets/ring1-23,Scene7SharedAssets/ring1-24),{Scene7SharedAssets/ring1-01,Scene7SharedAssets/ring1-02,Scene7SharedAssets/ring1-03,Scene7SharedAssets/ring1-04,Scene7SharedAssets/ring1-05,Scene7SharedAssets/ring1-06,Scene7SharedAssets/ring1-07,Scene7SharedAssets/ring1-08,Scene7SharedAssets/ring1-09,Scene7SharedAssets/ring1-10,Scene7SharedAssets/ring1-11,Scene7SharedAssets/ring1-12))")
```

---
description: JavaScript API-referentie voor Carousel Viewer.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# setAsset{#setasset}

JavaScript API-referentie voor Carousel Viewer.

` setAsset( *`element`*)`

Hiermee stelt u het nieuwe element in. U kunt deze parameter op elk ogenblik roepen, of vóór of na `init()`. Als deze wordt aangeroepen na `init()`, wisselt de viewer het element tijdens runtime om.

Zie ook [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> element</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} nieuwe element-id. </p> <p>Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Verwijzing naar één afbeelding:

```
<instance>.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner")
```


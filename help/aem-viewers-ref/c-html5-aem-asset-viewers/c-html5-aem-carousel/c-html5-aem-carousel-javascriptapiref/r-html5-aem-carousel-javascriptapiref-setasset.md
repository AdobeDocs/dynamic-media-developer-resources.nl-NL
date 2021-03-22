---
description: JavaScript API-referentie voor Carousel Viewer.
seo-description: JavaScript API-referentie voor Carousel Viewer.
seo-title: setAsset
solution: Experience Manager
title: setAsset
uuid: 770cbb87-af86-48dc-88a0-e74f6716f545
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '91'
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


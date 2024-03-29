---
title: setAsset
description: JavaScript API-referentie voor Video Image Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: e5f88bc9-a880-45eb-9554-57e185937d29
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# setAsset{#setasset}

JavaScript API-referentie voor Video Image Viewer.

` setAsset( *`element`*)`

Hiermee stelt u het nieuwe element in. U kunt deze parameter op elk gewenst moment vóór of na `init()`. Als het wordt aangeroepen na `init()`, wordt het element tijdens runtime vervangen door de viewer.

Zie ook [init](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> element</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} new asset ID. </p> <p>Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud), worden niet ondersteund door deze viewer. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Verwijzing naar één afbeelding:

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg")
```

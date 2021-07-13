---
description: JavaScript API-referentie voor Video Viewer.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 5fd80f8d-321e-47f4-9fb2-65e7bd63be58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# setAsset{#setasset}

JavaScript API-referentie voor Video Viewer.

[!DNL ` setAsset( *`element`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> element  </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Tekenreeks </span>} nieuwe element-id of expliciete afbeeldingsset met optionele opties voor Beeldrendering toegevoegd na <span class="codeph"> ? </span>. </p> <p> Afbeeldingen die gebruikmaken van IR (Image Rendering) of UGC (Door de gebruiker gegenereerde inhoud) worden niet ondersteund door deze viewer. </p> </td> 
  </tr> 
 </tbody> 
</table>

Hiermee wordt een nieuw element ingesteld. U kunt deze parameter op elk ogenblik roepen, of vóór of na [!DNL `init()`]. Als deze wordt aangeroepen na [!DNL `init()`], wisselt de viewer het element tijdens runtime om.

Zie ook [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Eén verwijzing naar een afbeeldingsset die is gedefinieerd in een catalogus:

```
 <instance>.setAsset("Viewers/Pluralist")
```

Expliciete afbeeldingsset, met vooraf gecombineerde pagina&#39;s:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

Expliciete afbeeldingsset, met afzonderlijke paginaafbeeldingen:

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

De optie Verscherpen is toegevoegd aan alle afbeeldingen in de set:

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```

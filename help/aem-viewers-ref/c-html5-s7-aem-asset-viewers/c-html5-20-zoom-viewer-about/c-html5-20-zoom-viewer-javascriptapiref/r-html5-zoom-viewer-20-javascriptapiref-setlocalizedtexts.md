---
description: JavaScript API-referentie voor Video Viewer.
seo-description: JavaScript API-referentie voor Video Viewer.
seo-title: setLocalizedText
solution: Experience Manager
title: setLocalizedText
topic: Dynamic media
uuid: af1844bb-1af2-4efb-9824-2371ec91b342
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---


# setLocalizedText{#setlocalizedtexts}

JavaScript API-referentie voor Video Viewer.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Object</span>} JSON-object met lokalisatiegegevens. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Lokalisatie van gebruikersinterface-elementen</a> voor meer informatie. </p> <p>Zie ook <i>Handboek SDK van viewer</i> en het voorbeeld voor meer informatie over de inhoud van het object. </p> </td> 
  </tr> 
 </tbody> 
</table>

Hiermee stelt u de waarden voor het lokalisatiesymbool in voor een of meer landinstellingen. Deze parameter moet vóór `init()` worden geroepen.

Zie ook [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```


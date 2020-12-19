---
description: JavaScript API-referentie voor eCatalog SearchViewer.
seo-description: JavaScript API-referentie voor eCatalog SearchViewer.
seo-title: eCatalogSearchViewer
solution: Experience Manager
title: eCatalogSearchViewer
topic: Dynamic media
uuid: 304724aa-3f50-46de-97d0-48e8c81401ed
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---


# eCatalogSearchViewer{#ecatalogsearchviewer}

JavaScript API-referentie voor eCatalog SearchViewer.

[!DNL `eCatalogSearchViewer([config])`]

Constructor, maakt een nieuwe zoekviewerinstantie voor eCatalog.

## Parameters {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object}  </span> optioneel JSON-configuratieobject. Hiermee kunnen alle viewerinstellingen worden doorgegeven aan de constructor en wordt het aanroepen van afzonderlijke settermethoden vermeden. Bevat de volgende eigenschappen: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}- </span> id van de DOM-container (normaal gesproken een  <span class="codeph"> DIV  </span>) waarin de viewer wordt ingevoegd. Het is niet nodig om het containerelement te hebben dat tegen de tijd wordt gecreeerd deze methode wordt geroepen. De container moet echter bestaan wanneer <span class="codeph"> init() </span> wordt uitgevoerd. Vereist. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> params  </span> -  <span class="codeph"> {Object}  </span> JSON-object met viewerconfiguratieparameters waarbij de eigenschapnaam een viewer-specifieke configuratieoptie of een SDK-optie is en de waarde van die eigenschap een overeenkomende instellingenwaarde is. Vereist. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> handlers  </span> -  <span class="codeph"> {Object}  </span> JSON-object met callbacks voor viewergebeurtenissen, waarbij de naam van de eigenschap de naam van de ondersteunde viewergebeurtenis is en de waarde van de eigenschap een JavaScript-functieverwijzing naar een geschikte callback is. Optioneel. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-event-callbacks.md#concept-0bf5ff877043468db58ac62a92d002b6" format="dita" scope="local"> Gebeurteniscallbacks </a> voor meer informatie over viewergebeurtenissen. </p> </li> 
      <li id="li_FE5B330E98834CB08C16FCA694F31BE3"> <p> <span class="codeph"> gelokaliseerdText  </span> - { <span class="codeph"> Object  </span>} JSON-object met lokalisatiegegevens. Optioneel. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Lokalisatie van gebruikersinterface-elementen </a> voor meer informatie. </p> <p>Zie ook de <i>Gebruikershandleiding voor de SDK van de viewer</i> en het voorbeeld voor meer informatie over de inhoud van het object. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "searchserverurl":"http://s7search1.scene7.com/s7search/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"CloseButton.TOOLTIP":"Close" 
}, 
"fr":{ 
"CloseButton.TOOLTIP":"Fermer" 
}, 
defaultLocale:"en" 
} 
});
```


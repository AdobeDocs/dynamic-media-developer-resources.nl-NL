---
description: De zoekviewer voor eCatalog biedt ondersteuning voor het uit het vak bijhouden van Adobe Analytics.
solution: Experience Manager
title: Ondersteuning voor Adobe Analytics-tracking
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User,Data Engineer,Data Architect
exl-id: b35e52f5-fa08-4945-aa52-9fdf41a6081a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# Ondersteuning voor Adobe Analytics-tracking{#support-for-adobe-analytics-tracking}

De zoekviewer voor eCatalog biedt ondersteuning voor het uit het vak bijhouden van Adobe Analytics.

## Buiten-de-box-tracking {#section-ba994f079d0343c8ae48adffaa3195a3}

De eCatalog Search Viewer ondersteunt [!DNL Adobe Analytics] het volgen uit-van-de-doos. Als u het bijhouden van wijzigingen wilt inschakelen, geeft u de juiste naam van de bedrijfsvoorinstelling door als `config2` parameter.

De kijker verzendt ook één enkele het volgen HTTP- verzoek naar de gevormde Server van het Beeld met het viewertype en versieinformatie.

## Aangepaste reeksspatiëring {#section-cda48fc9730142d0bb3326bac7df3271}

Om met analysesystemen van derden te integreren, moet naar de `trackEvent` de callback van de kijker en verwerkt `eventInfo` argument van de callback functie zoals nodig. De volgende code is een voorbeeld van een dergelijke handlerfunctie:

```javascript {.line-numbers}
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
    break; 
   //additional cases for other events 
} 
} 
} 
});
```

De viewer houdt de volgende SDK-gebruikersgebeurtenissen bij:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SDK-gebruikersgebeurtenis </p> </th> 
   <th colname="col2" class="entry"> <p>Verzonden wanneer... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LADEN </span> </p> </td> 
   <td colname="col2"> <p>de viewer wordt eerst geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> WISSELEN </span> </p> </td> 
   <td colname="col2"> <p>een element wordt in de viewer gewisseld met het gereedschap <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOMEN </span> </p> </td> 
   <td colname="col2"> <p> Er is ingezoomd op een afbeelding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN </span> </p> </td> 
   <td colname="col2"> <p>een afbeelding wordt gepand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STAAL </span> </p> </td> 
   <td colname="col2"> <p> een afbeelding wordt gewijzigd door op een staal te klikken of erop te tikken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAGINA </span> </p> </td> 
   <td colname="col2"> <p> een huidig frame wordt gewijzigd in de hoofdweergave. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ITEM </span> </p> </td> 
   <td colname="col2"> <p>er wordt een pop-upvenster met informatie geactiveerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>een gebruiker naar een andere pagina navigeert omdat hij op de afbeelding met hyperlinks klikt. </p> </td> 
  </tr> 
 </tbody> 
</table>

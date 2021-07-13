---
description: De Flyout-viewer biedt ondersteuning voor het uit de verpakking bijhouden van Adobe Analytics.
solution: Experience Manager
title: Ondersteuning voor Adobe Analytics-tracking
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User,Data Engineer,Data Architect
exl-id: e5ffe8a8-6c25-4fc2-8c25-90bc7e0b416c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# Ondersteuning voor Adobe Analytics-tracking{#support-for-adobe-analytics-tracking}

De Flyout-viewer biedt ondersteuning voor het uit de verpakking bijhouden van Adobe Analytics.

## Buiten-de-box-tracking {#section-ba994f079d0343c8ae48adffaa3195a3}

De Inline zoomviewer ondersteunt [!DNL Adobe Analytics] het uit-van-de-box bijhouden. Als u reeksspatiëring wilt inschakelen, geeft u de juiste naam van de bedrijfsvoorinstelling door als `config2`-parameter.

De kijker verzendt ook één enkele het volgen HTTP- verzoek naar de gevormde Server van het Beeld met het viewertype en versieinformatie.

## Aangepaste reeksspatiëring {#section-cda48fc9730142d0bb3326bac7df3271}

Om met derdeanalysesystemen te integreren is het noodzakelijk om aan `trackEvent` kijkerscallback te luisteren en het `eventInfo` argument van de callback functie zonodig te verwerken. De volgende code is een voorbeeld van een dergelijke handlerfunctie:

```
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
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
   <td colname="col1"> <p> <span class="codeph"> LADEN  </span> </p> </td> 
   <td colname="col2"> <p>de viewer eerst wordt geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP  </span> </p> </td> 
   <td colname="col2"> <p>een element wordt in de viewer omgewisseld met <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOMEN  </span> </p> </td> 
   <td colname="col2"> <p>de flyout wordt geactiveerd of het zoomniveau wordt gewijzigd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN  </span> </p> </td> 
   <td colname="col2"> <p> een afbeelding wordt gepand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STAAL  </span> </p> </td> 
   <td colname="col2"> <p> een afbeelding wordt gewijzigd door op een staal te klikken of erop te tikken. </p> </td> 
  </tr> 
 </tbody> 
</table>

---
description: De Basic Zoom Viewer biedt ondersteuning voor het uit de verpakking bijhouden van Adobe Analytics.
seo-description: De Basic Zoom Viewer biedt ondersteuning voor het uit de verpakking bijhouden van Adobe Analytics.
seo-title: Ondersteuning voor Adobe Analytics-tracking
solution: Experience Manager
title: Ondersteuning voor Adobe Analytics-tracking
topic: Dynamic Media
uuid: f48fde77-7e48-4d56-b5c5-079a484e6d9c
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Ondersteuning voor Adobe Analytics tracking{#support-for-adobe-analytics-tracking}

De Basic Zoom Viewer biedt ondersteuning voor het uit de verpakking bijhouden van Adobe Analytics.

## Buiten-de-box tracking {#section-ba994f079d0343c8ae48adffaa3195a3}

De Basic Zoom Viewer ondersteunt [!DNL Adobe Analytics] het uit-van-de-box bijhouden. Als u reeksspatiëring wilt inschakelen, geeft u de juiste naam van de bedrijfsvoorinstelling door als `config2`-parameter.

De kijker verzendt ook één enkele het volgen HTTP- verzoek naar de gevormde Server van het Beeld met het viewertype en versieinformatie.

## Aangepaste tekstspatiëring {#section-cda48fc9730142d0bb3326bac7df3271}

Om met derdeanalysesystemen te integreren is het noodzakelijk om aan `trackEvent` kijkerscallback te luisteren en het `eventInfo` argument van de callback functie zonodig te verwerken. De volgende code is een voorbeeld van een dergelijke handlerfunctie:

```
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
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
   <td colname="col2"> <p>de viewer wordt eerst geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP  </span> </p> </td> 
   <td colname="col2"> <p>een element wordt in de viewer omgewisseld met de <span class="codeph"> setAsset() </span>-API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOMEN  </span> </p> </td> 
   <td colname="col2"> <p> ingezoomd op een afbeelding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAN  </span> </p> </td> 
   <td colname="col2"> <p>een afbeelding wordt gepand. </p> </td> 
  </tr> 
 </tbody> 
</table>


---
description: De video-viewer ondersteunt het uit de verpakking bijhouden van Adobe Analytics.
seo-description: De video-viewer ondersteunt het uit de verpakking bijhouden van Adobe Analytics.
seo-title: Ondersteuning voor Adobe Analytics-tracking
solution: Experience Manager
title: Ondersteuning voor Adobe Analytics-tracking
topic: Dynamic media
uuid: c53b3d3b-42e5-4c87-8a1e-87c73eb32341
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---


# Ondersteuning voor Adobe Analytics tracking{#support-for-adobe-analytics-tracking}

De video-viewer ondersteunt het uit de verpakking bijhouden van Adobe Analytics.

## Buiten-de-box tracking {#section-3b101fe30be943c1b679fd5c273569ca}

De video-viewer ondersteunt het uit de verpakking bijhouden van Adobe Analytics.

Als u reeksspatiëring wilt inschakelen, geeft u de juiste naam van de bedrijfsvoorinstelling door als `config2`-parameter.

De kijker verzendt ook één enkele het volgen HTTP- verzoek naar de gevormde Server van het Beeld met het viewertype en versieinformatie.

## Aangepaste tekstspatiëring {#section-ab10bd7caf184721a366cf3953071934}

Om met derdeanalysesystemen te integreren is het noodzakelijk om aan `trackEvent` kijker callback te luisteren en `eventInfo` argument van de callback functie zonodig te verwerken. De volgende code is een voorbeeld van een dergelijke handlerfunctie:

```
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
   <td colname="col2"> <p>een element wordt in de viewer omgewisseld met <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AFSPELEN  </span> </p> </td> 
   <td colname="col2"> <p>het afspelen wordt gestart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUZEREN  </span> </p> </td> 
   <td colname="col2"> <p>het afspelen is gepauzeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOPPEN  </span> </p> </td> 
   <td colname="col2"> <p>afspelen wordt gestopt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE  </span> </p> </td> 
   <td colname="col2"> <p>het afspelen een van de volgende mijlpalen bereikt: 0%, 25%, 50%, 75% en 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>


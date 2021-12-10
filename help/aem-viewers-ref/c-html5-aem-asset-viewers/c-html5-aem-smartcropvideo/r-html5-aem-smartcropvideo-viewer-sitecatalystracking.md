---
title: Ondersteuning voor Adobe Analytics-tracking
description: De Smart Crop Video Viewer ondersteunt het uit-van-de-doos traceren van Adobe Analytics.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User,Data Engineer,Data Architect
exl-id: 0d91ca94-79fc-40de-8095-0252688ebe76
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# Ondersteuning voor Adobe Analytics-tracking{#support-for-adobe-analytics-tracking}

De Smart Crop Video Viewer ondersteunt het uit-van-de-doos traceren van Adobe Analytics.

## Buiten-de-box-tracking {#section-3b101fe30be943c1b679fd5c273569ca}

De Smart Crop Video Viewer ondersteunt het uit-van-de-doos traceren van Adobe Analytics.

Als u het bijhouden van wijzigingen wilt inschakelen, geeft u de juiste naam van de bedrijfsvoorinstelling door als `config2` parameter.

De kijker verzendt ook één enkele het volgen HTTP- verzoek naar de gevormde Server van het Beeld met het viewertype en versieinformatie.

## Aangepaste reeksspatiëring {#section-ab10bd7caf184721a366cf3953071934}

Om met analysesystemen van derden te integreren, is het nodig te luisteren naar `trackEvent` callback en proces van viewer `eventInfo` argument van de callback functie zoals nodig. De volgende code is een voorbeeld van een dergelijke handlerfunctie:

```
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
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
   <td colname="col1"> <p> <span class="codeph"> LADEN </span> </p> </td> 
   <td colname="col2"> <p>de viewer wordt eerst geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>een element in de viewer wordt omgewisseld met <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AFSPELEN </span> </p> </td> 
   <td colname="col2"> <p>het afspelen wordt gestart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUZEREN </span> </p> </td> 
   <td colname="col2"> <p>het afspelen is gepauzeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOPPEN </span> </p> </td> 
   <td colname="col2"> <p>afspelen wordt gestopt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>het afspelen een van de volgende mijlpalen bereikt: 0%, 25%, 50%, 75% en 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

---
description: De HTML5 Video360 Viewer biedt ondersteuning voor het uit de verpakking bijhouden van Adobe Analytics.
seo-description: De HTML5 Video360 Viewer biedt ondersteuning voor het uit de verpakking bijhouden van Adobe Analytics.
seo-title: Ondersteuning voor Adobe Analytics-tracking
solution: Experience Manager
title: Ondersteuning voor Adobe Analytics-tracking
topic: Dynamic media
uuid: b5ab903b-3365-45e3-9542-c290c6c42670
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---


# Ondersteuning voor Adobe Analytics tracking{#support-for-adobe-analytics-tracking}

De HTML5 Video360 Viewer biedt ondersteuning voor het uit de verpakking bijhouden van Adobe Analytics.

Als u reeksspatiëring wilt inschakelen, geeft u de juiste naam van de bedrijfsvoorinstelling door als `config2`-parameter.

Door gebrek, verzendt de kijker één enkele het volgen HTTP- verzoek naar de gevormde Server van het Beeld met het viewertype en versieinformatie.

## Aangepaste tekstspatiëring {#section-cda48fc9730142d0bb3326bac7df3271}

Om met derdeanalysesystemen te integreren is het noodzakelijk om aan `trackEvent` kijkerscallback te luisteren en het `eventInfo` argument van de callback functie zonodig te verwerken. De volgende code is een voorbeeld van een dergelijke handlerfunctie:

```
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
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
   <th colname="col2" class="entry"> <p>Verzonden... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LADEN  </span> </p> </td> 
   <td colname="col2"> <p>wanneer de viewer het eerst wordt geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP  </span> </p> </td> 
   <td colname="col2"> <p>wanneer een element in de viewer wordt omgewisseld met <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AFSPELEN  </span> </p> </td> 
   <td colname="col2"> <p>wanneer het afspelen begint. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUZEREN  </span> </p> </td> 
   <td colname="col2"> <p>wanneer het afspelen is gepauzeerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> STOPPEN  </span> </p> </td> 
   <td colname="col2"> <p>wanneer het afspelen wordt gestopt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE  </span> </p> </td> 
   <td colname="col2"> <p>wanneer het afspelen een van de volgende mijlpalen bereikt: 0%, 25%, 50%, 75% of 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>


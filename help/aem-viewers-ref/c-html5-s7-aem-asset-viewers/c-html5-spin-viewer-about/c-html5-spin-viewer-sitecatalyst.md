---
description: De Draaiende Kijker steunt het volgen van Adobe Analytics uit de doos.
solution: Experience Manager
title: Ondersteuning voor Adobe Analytics-tracking
feature: Dynamic Media Classic,Viewers,SDK/API,Draaiensets
role: Developer,User,Data Engineer,Data Architect
exl-id: 30762700-6d69-4299-9492-57893232abe1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# Ondersteuning voor Adobe Analytics-tracking{#support-for-adobe-analytics-tracking}

De Draaiende Kijker steunt het volgen van Adobe Analytics uit de doos.

## Buiten-de-box-tracking {#section-d06145cfa2b9491bb485b599368d466e}

De Draaiende Viewer ondersteunt het uit-van-de-doos traceren van Adobe Analytics.

Als u reeksspatiëring wilt inschakelen, geeft u de juiste naam van de bedrijfsvoorinstelling door als `config2`-parameter.

De kijker verzendt ook één enkele het volgen HTTP- verzoek naar de gevormde Server van het Beeld met het viewertype en versieinformatie.

## Aangepaste reeksspatiëring {#section-47512156a1d64b338b50cfa39c84f4aa}

Om met derdeanalysesystemen te integreren, is het noodzakelijk om aan `trackEvent` kijkerscallback te luisteren en het `eventInfo` argument van de callback functie, zonodig te verwerken. De volgende code is een voorbeeld van een dergelijke handlerfunctie:

```
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
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
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SPIN  </span> </p> </td> 
   <td colname="col2"> <p> er wordt een centrifuge uitgevoerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

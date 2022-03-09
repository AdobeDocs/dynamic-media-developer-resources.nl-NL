---
title: Ondersteuning voor Adobe Analytics-tracking
description: Ondersteuning voor Adobe Analytics-tracking
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User,Data Engineer,Data Architect
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# Ondersteuning voor Adobe Analytics-tracking{#support-for-adobe-analytics-tracking}

Door gebrek, verzendt de kijker één enkele het volgen HTTP- verzoek naar de gevormde Server van het Beeld met viewertype en versieinformatie.

## Aangepaste reeksspatiëring {#section-cda48fc9730142d0bb3326bac7df3271}

Om met een analysesysteem van derden te kunnen integreren, moet naar `trackEvent` callback en proces van viewer `eventInfo` argument van de callback functie zoals nodig. De volgende code is een voorbeeld van een dergelijke handlerfunctie:

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
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
   <th colname="col2" class="entry"> <p>Verzonden... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LADEN </span> </p> </td> 
   <td colname="col2"> <p>wanneer de viewer het eerst wordt geladen. </p> </td> 
  </tr> 
 </tbody> 
</table>

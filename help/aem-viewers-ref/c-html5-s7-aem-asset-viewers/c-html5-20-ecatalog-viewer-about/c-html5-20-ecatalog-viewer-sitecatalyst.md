---
description: De eCatalog Viewer ondersteunt het bijhouden van Adobe-analysemogelijkheden vanuit het vak.
seo-description: De eCatalog Viewer ondersteunt het bijhouden van Adobe-analysemogelijkheden vanuit het vak.
seo-title: Ondersteuning voor het bijhouden van Adobe Analytics
solution: Experience Manager
title: Ondersteuning voor het bijhouden van Adobe Analytics
topic: Dynamic media
uuid: a96b6655-4a11-490c-8f66-3633f0ae0fee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Ondersteuning voor het bijhouden van Adobe Analytics{#support-for-adobe-analytics-tracking}

De eCatalog Viewer ondersteunt het bijhouden van Adobe-analysemogelijkheden vanuit het vak.

## Buiten-de-box-tracking {#section-ba994f079d0343c8ae48adffaa3195a3}

De eCatalog-viewer ondersteunt het [!DNL Adobe Analytics] bijhouden van wijzigingen. Als u reeksspatiëring wilt inschakelen, geeft u de juiste naam van de bedrijfsvoorinstelling als `config2` parameter door.

De kijker verzendt ook één enkele het volgen HTTP- verzoek naar de gevormde Server van het Beeld met het viewertype en versieinformatie.

## Aangepaste reeksspatiëring {#section-cda48fc9730142d0bb3326bac7df3271}

Om met derdeanalysesystemen te integreren, is het noodzakelijk om aan de kijker callback te luisteren en het `trackEvent` `eventInfo` argument van de callback functie zonodig te verwerken. De volgende code is een voorbeeld van een dergelijke handlerfunctie:

```
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
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
   <td colname="col1"> <p> <span class="codeph"> LADEN </span> </p> </td> 
   <td colname="col2"> <p>de viewer wordt eerst geladen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SWAP </span> </p> </td> 
   <td colname="col2"> <p>een element wordt omgewisseld in de viewer met de <span class="codeph"> setAsset()- </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOMEN </span> </p> </td> 
   <td colname="col2"> <p> ingezoomd op een afbeelding. </p> </td> 
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


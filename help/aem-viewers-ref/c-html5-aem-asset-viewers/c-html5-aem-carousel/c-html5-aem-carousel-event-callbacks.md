---
description: 'null'
seo-description: 'null'
seo-title: Gebeurteniscallbacks
solution: Experience Manager
title: Gebeurteniscallbacks
topic: Dynamic media
uuid: 7280a391-3ead-470b-89e9-5faa082e0202
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Gebeurteniscallbacks{#event-callbacks}

De viewer ondersteunt JavaScript-gebeurteniscallbacks die de webpagina gebruikt om het initialisatieproces of het runtimegedrag van de viewer bij te houden.

Callback-handlers worden toegewezen door gebeurtenisnamen en bijbehorende handlerfuncties met de `handlers` eigenschap door te geven aan `config` JSON-object in de constructor van de viewer. U kunt ook de `setHandlers()` API-methode gebruiken.

Tot de ondersteunde viewergebeurtenissen behoren:

<table id="table_D4A2035B65B140F882F550B711BD3160"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Viewer-gebeurtenis </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> initComplete </span> </p> </td> 
   <td colname="col2"> <p>De gebeurtenis wordt geactiveerd wanneer de viewer-initialisatie is voltooid en alle interne componenten zijn gemaakt, zodat de <span class="codeph"> getComponent()- </span> API kan worden gebruikt. De callback-handler neemt geen argumenten aan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trackEvent </span> </p> </td> 
   <td colname="col2"> <p> Elke keer dat een gebeurtenis zich binnen de viewer voordoet, wordt deze gebeurtenis geactiveerd door een systeem voor het bijhouden van gebeurtenissen, zoals Adobe Analytics. De callback-handler accepteert de volgende argumenten: </p> <p> 
     <ul id="ul_8A5F409E32E94063AE8D3AB158A0E13D"> 
      <li id="li_1311D5DDD4454FBC9116BA8E2CB003B1"> <p> <span class="codeph"> objID {String} </span> - wordt momenteel niet gebruikt. </p> </li> 
      <li id="li_C2ABD13097FA40A7B9801C0B7592FB59"> <p> <span class="codeph"> compClass {String} </span> - wordt momenteel niet gebruikt. </p> </li> 
      <li id="li_3BE8001365714C3FAC32C9B2CFFD5DCE"> <p> <span class="codeph"> instName {String} </span> - een instantienaam van de Viewer SDK-component die de gebeurtenis heeft geactiveerd. </p> </li> 
      <li id="li_755DDE84B1CC4B4D8A3FA0C774CBA666"> <p> <span class="codeph"> timeStamp {Number} </span> - tijdstempel van de gebeurtenis. </p> </li> 
      <li id="li_05A1C45826AC4D1192CB72FE07EE4C29"> <p> <span class="codeph"> eventInfo {String} </span> - gebeurtenislading. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> quickViewActivate </span> </p> </td> 
   <td colname="col2"> <p> De gebeurtenis wordt geactiveerd wanneer de gebruiker een hotspot activeert met daaraan gekoppelde Quick View-gegevens. De callback manager neemt het volgende argument: </p> <p> 
     <ul id="ul_171110934BD54839B371FAD8D2AD467B"> 
      <li id="li_7B14C3BA432B43E392AC103926807E88"> <p> <span class="codeph"> data {Object} </span> - een JSON-object dat gegevens bevat van de hotspot-definitie. De <span class="codeph"> skin van het veld </span> is verplicht, terwijl andere velden optioneel zijn en afhankelijk zijn van de definitie van de bronhotspot. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Zie ook [CarouselViewer**](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-carouselviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) en [setHandlers**](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).

---
title: setHandlers
description: JavaScript API-referentie voor Panoramische Viewer
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 90775d4a-386b-4b56-b75e-8afafe749645
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# setHandlers{#sethandlers}

JavaScript API-referentie voor Panoramische Viewer

`setHandlers(handlers)`

Geeft nul of meer callback-handlers aan. Een vraag aan deze methode beschrijft volledig gebeurtenismanagers die eerder voor die kijkersinstantie werden toegewezen. Moet eerder worden aangeroepen `init()`.

## Parameter {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> handlers </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> JSON-object met callbacks voor viewergebeurtenissen, waarbij de eigenschapsnaam de naam van de ondersteunde viewergebeurtenis is en de eigenschapswaarde een JavaScript-functieverwijzing naar een geschikte callback is. </p> <p>Raadpleeg de sectie Gebeurteniscallbacks voor meer informatie over viewergebeurtenissen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```

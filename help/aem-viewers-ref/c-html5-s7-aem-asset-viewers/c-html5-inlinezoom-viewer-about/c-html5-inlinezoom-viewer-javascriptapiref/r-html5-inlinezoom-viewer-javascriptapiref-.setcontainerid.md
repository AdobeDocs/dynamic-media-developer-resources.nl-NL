---
title: setContainerId
description: JavaScript API-referentie voor Inline Zoom Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: ab3359f0-0c58-4984-815a-e0246728100e
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# setContainerId{#setcontainerid}

JavaScript API-referentie voor Inline Zoom Viewer.

` setContainerId( *`containerId`*)`

Hiermee wordt de id van de DOM-container ingesteld (gewoonlijk een `DIV`) waarin de viewer wordt ingevoegd. Het is niet nodig om het containerelement te hebben dat tegen de tijd wordt gecreeerd deze methode wordt geroepen. De container moet echter bestaan wanneer `init()` wordt uitgevoerd. Het moet eerder worden opgeroepen `init()`. Deze methode is optioneel als de configuratiegegevens van de viewer worden doorgegeven met `config` JSON-object naar de constructor.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> ID van container. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

---
title: setContainerId
description: JavaScript API-referentie voor de Basic Zoom Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: dae07170-24bb-4e8c-86d6-5313db33736f
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---

# setContainerId{#setcontainerid}

JavaScript API-referentie voor de Basic Zoom Viewer.

` setContainerId( *`containerId`*)`

Hiermee stelt u de id in van de DOM-container (normaal gesproken een DIV) waarin de viewer wordt ingevoegd. Het is niet nodig om het containerelement te hebben dat tegen de tijd wordt gecreeerd deze methode wordt geroepen. De container moet echter bestaan wanneer `init()` wordt uitgevoerd. Het moet eerder worden opgeroepen `init()`.

Deze methode is optioneel als de configuratiegegevens van de viewer zijn doorgegeven met `config` JSON-object naar constructor.

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

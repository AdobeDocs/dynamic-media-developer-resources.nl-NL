---
description: JavaScript API-referentie voor de Basic Zoom Viewer.
seo-description: JavaScript API-referentie voor de Basic Zoom Viewer.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: 064ebb0c-088a-4b8b-b623-c29363232cc4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setContainerId{#setcontainerid}

JavaScript API-referentie voor de Basic Zoom Viewer.

` setContainerId( *`containerId`*)`

Hiermee stelt u de id in van de DOM-container (normaal gesproken een DIV) waarin de viewer wordt ingevoegd. Het is niet nodig om het containerelement te hebben dat tegen de tijd wordt gecreeerd deze methode wordt geroepen. De container moet echter bestaan wanneer `init()` deze wordt uitgevoerd. Het moet eerder worden opgeroepen `init()`.

Deze methode is optioneel als de configuratiegegevens van de viewer samen met het JSON-object aan de constructor zijn doorgegeven. `config`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> -id van container. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourneert {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Geen.

## Voorbeeld {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```


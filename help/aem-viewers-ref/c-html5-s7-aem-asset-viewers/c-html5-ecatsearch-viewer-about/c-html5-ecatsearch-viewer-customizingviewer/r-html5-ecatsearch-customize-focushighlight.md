---
description: Focusmarkering voor invoer wordt weergegeven rondom het interface-element voor de doelviewer.
seo-description: Focusmarkering voor invoer wordt weergegeven rondom het interface-element voor de doelviewer.
seo-title: Focus markeren
solution: Experience Manager
title: Focus markeren
uuid: 0bd36795-e663-4f0e-8310-a57c2ffae4a2
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# Focus markeren{#focus-highlight}

Focusmarkering voor invoer wordt weergegeven rondom het interface-element voor de doelviewer.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

De vormgeving van de focusmarkering wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogviewer *:focus
```

**CSS-eigenschappen van focusmarkering**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> overzicht  </span> </p> </td> 
   <td colname="col2"> <p> Focus markeerstijl. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u de standaardfocusmarkering voor de browser wilt uitschakelen voor alle gebruikersinterface-elementen van de viewer, voegt u de volgende CSS-kiezer toe aan de stijlpagina van de viewer:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```


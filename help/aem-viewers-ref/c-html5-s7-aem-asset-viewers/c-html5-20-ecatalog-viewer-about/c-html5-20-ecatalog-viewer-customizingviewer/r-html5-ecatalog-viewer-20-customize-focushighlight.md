---
title: Focus markeren
description: Focusmarkering voor invoer wordt weergegeven rondom het interface-element voor de doelviewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5737d7-1295-46a9-9b84-c43269e5a914
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '74'
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
   <td colname="col1"> <p> <span class="codeph"> overzicht </span> </p> </td> 
   <td colname="col2"> <p> Focus markeerstijl. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - Als u de standaardfocusmarkering voor de browser wilt uitschakelen voor alle gebruikersinterface-elementen van de viewer, voegt u de volgende CSS-kiezer toe aan de stijlpagina van de viewer:

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```

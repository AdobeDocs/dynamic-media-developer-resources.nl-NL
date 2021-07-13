---
description: Focusmarkering voor invoer wordt weergegeven rondom het interface-element voor de doelviewer.
solution: Experience Manager
title: Focus markeren
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 949b8a8b-5f59-415e-acc1-bf8cea77cbd9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
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

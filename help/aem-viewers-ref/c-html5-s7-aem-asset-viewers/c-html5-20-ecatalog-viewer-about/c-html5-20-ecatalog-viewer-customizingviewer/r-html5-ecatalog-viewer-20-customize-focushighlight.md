---
description: Focusmarkering voor invoer wordt weergegeven rondom het interface-element voor de doelviewer.
seo-description: Focusmarkering voor invoer wordt weergegeven rondom het interface-element voor de doelviewer.
seo-title: Focus markeren
solution: Experience Manager
title: Focus markeren
topic: Dynamic Media
uuid: 50411b68-8d01-4240-b548-a6c51374a8c6
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '87'
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


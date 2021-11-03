---
title: Hoofdviewergebied
description: Het hoofdweergavegebied wordt ingenomen door de video voor slimme uitsnijden. Deze wordt meestal ingesteld op het beschikbare apparaatscherm wanneer geen grootte is opgegeven.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 7d1379c1-7746-4f61-92df-e8ac4ab7d506
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# Hoofdviewergebied{#main-viewer-area}

Het hoofdweergavegebied wordt ingenomen door de video. Deze wordt meestal ingesteld op het beschikbare apparaatscherm wanneer geen grootte is opgegeven.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De volgende CSS-klassenkiezer bepaalt de weergave van het weergavegebied:

```
.s7smartcropvideoviewer 
```

## CSS-eigenschappen van het hoofdviewergebied {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur in hexadecimale notatie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorbeeld {#section-e8caea0a303c425a8a637c2a47c06355}

U stelt als volgt een viewer voor slimme-uitsnijdvideo met een witte achtergrond (#FFFFFF) in en maakt de grootte hiervan 512 x 288 pixels:

```
.s7smartcropvideoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

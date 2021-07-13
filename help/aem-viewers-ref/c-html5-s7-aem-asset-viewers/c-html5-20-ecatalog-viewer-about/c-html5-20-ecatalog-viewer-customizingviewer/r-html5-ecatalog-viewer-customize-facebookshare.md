---
description: Het facebook-gereedschap Delen bestaat uit een knop die is toegevoegd aan het deelvenster Delen via sociale media. Wanneer op de knop wordt geklikt, wordt de gebruiker omgeleid naar een dialoogvenster voor delen dat door een sociale service wordt aangeboden. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.
solution: Experience Manager
title: Facebook share
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 0525bfd0-ce38-4fd1-a5cc-e6b5acab1651
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Facebook share{#facebook-share}

Het facebook-gereedschap Delen bestaat uit een knop die is toegevoegd aan het deelvenster Delen via sociale media. Wanneer op de knop wordt geklikt, wordt de gebruiker omgeleid naar een dialoogvenster voor delen dat door een sociale service wordt aangeboden. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

De vormgeving van de deelknop Facebook wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogviewer .s7facebookshare
```

**CSS-eigenschappen van het Facebook-gereedschap Delen**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knopbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p> De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoop steunt `state` attributenselecteur, die kan worden gebruikt om verschillende huiden op verschillende knoopstaten toe te passen.

Het is mogelijk om de knop uit het deelvenster Sociaal delen te verwijderen door de CSS-eigenschap `display:none` in te stellen op de CSS-klasse.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - voor het instellen van een Facebook-deelknop van 28 x 28 pixels en het weergeven van een andere afbeelding voor elk van de vier verschillende knopstatussen:

```
.s7ecatalogviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7ecatalogviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7ecatalogviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7ecatalogviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```

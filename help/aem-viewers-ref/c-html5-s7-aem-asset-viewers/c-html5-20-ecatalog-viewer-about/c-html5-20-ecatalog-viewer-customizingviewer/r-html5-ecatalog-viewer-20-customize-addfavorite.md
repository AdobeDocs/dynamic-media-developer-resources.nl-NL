---
title: Knop Favoriet toevoegen
description: De positie van de Add knoop van de Favorieten wordt volledig beheerd door het menu van Favorieten.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3602fa7b-d654-4976-a62d-d959898cb530
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Knop Favoriet toevoegen{#add-favorite-button}

De positie van de Add knoop van de Favorieten wordt volledig beheerd door het menu van Favorieten.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De vormgeving van de knop Favoriet toevoegen wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogviewer .s7addfavoritebutton
```

**CSS-eigenschappen van de knop Favoriet toevoegen**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p> De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de knop. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt beide `state` en `selected` kenmerkkiezers, die kunnen worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden. Met name: `selected='true'` komt overeen met de status wanneer een gebruiker een nieuw pictogram Favoriet kan toevoegen door te selecteren of te tikken. Het kenmerk `selected='false'` komt overeen met de normale bewerkingsmodus wanneer een gebruiker pagina&#39;s kan inzoomen, pannen en omwisselen.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie .

Voorbeeld - Een knop Favorieten toevoegen van 28 x 28 pixels instellen. En er wordt een andere afbeelding weergegeven voor elk van de vier verschillende knoptoestanden, indien geselecteerd of niet.

```
.s7ecatalogviewer .s7addfavoritebutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7addfavoritebutton[selected='false'][state='up'] { 
background-image:url(images/v2/AddFavoriteButton_dark_up.png); 
} 
.s7ecatalogviewer .s7addfavoritebutton[selected='false'][state='over'] { 
background-image:url(images/v2/AddFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7addfavoritebutton[selected='false'][state='down'] { 
background-image:url(images/v2/AddFavoriteButton_dark_down.png); 
} 
.s7ecatalogviewer .s7addfavoritebutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/AddFavoriteButton_dark_disabled.png); 
} 
.s7ecatalogviewer .s7addfavoritebutton[selected='true'][state='up'] { 
background-image:url(images/v2/AddFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7addfavoritebutton[selected='true'][state='over'] { 
background-image:url(images/v2/AddFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7addfavoritebutton[selected='true'][state='down'] { 
background-image:url(images/v2/AddFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7addfavoritebutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/AddFavoriteButton_dark_disabled.png); 
}
```

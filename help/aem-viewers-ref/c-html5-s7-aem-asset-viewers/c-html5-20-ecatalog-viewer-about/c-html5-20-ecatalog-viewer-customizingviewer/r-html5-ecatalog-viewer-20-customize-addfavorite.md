---
description: De positie van de Add knoop van de Favorieten wordt volledig beheerd door het menu van Favorieten.
seo-description: De positie van de Add knoop van de Favorieten wordt volledig beheerd door het menu van Favorieten.
seo-title: Knop Favoriet toevoegen
solution: Experience Manager
title: Knop Favoriet toevoegen
topic: Dynamic media
uuid: 0e2f7187-d5a9-42a4-b918-e4782d62be6c
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

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
>Deze knop ondersteunt zowel de selectors `state` als `selected` kenmerken, die kunnen worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden. Dit komt met name overeen met de toestand waarin een gebruiker een nieuw pictogram Favoriet kan toevoegen door te klikken of te tikken. `selected='true'` `selected='false'` komt overeen met de normale bewerkingsmodus wanneer een gebruiker pagina&#39;s kan inzoomen, pannen en omwisselen.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - om een knop Favoriet toevoegen in te stellen van 28 x 28 pixels en een andere afbeelding weer te geven voor elk van de vier verschillende knopstatussen, indien geselecteerd of niet geselecteerd.

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


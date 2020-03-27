---
description: De positie van de Remove knoop van de Favoriet wordt volledig beheerd door het menu van Favorieten.
seo-description: De positie van de Remove knoop van de Favoriet wordt volledig beheerd door het menu van Favorieten.
seo-title: Knop Favoriet verwijderen
solution: Experience Manager
title: Knop Favoriet verwijderen
topic: Dynamic media
uuid: c2e1929d-d859-49d5-8bdc-13507e25d02c
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Knop Favoriet verwijderen{#remove-favorite-button}

De positie van de Remove knoop van de Favoriet wordt volledig beheerd door het menu van Favorieten.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De vormgeving van de knop Favoriet verwijderen wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogviewer .s7removefavoritebutton
```

**CSS-eigenschappen van de knop Favoriet verwijderen**

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

Voorbeeld: om een knop Favoriet verwijderen in te stellen van 28 x 28 pixels en een andere afbeelding weer te geven voor elk van de vier verschillende knopstatussen, indien geselecteerd of niet geselecteerd.

```
.s7ecatalogviewer .s7removefavoritebutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='false'][state='up'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_up.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='false'][state='over'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='false'][state='down'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_down.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_disabled.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='true'][state='up'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='true'][state='over'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='true'][state='down'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_disabled.png); 
}
```


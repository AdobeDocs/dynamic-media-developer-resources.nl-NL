---
title: Menu Favorieten
description: De het menudrop-down lijst van Favorieten verschijnt in de controlebar. Het bestaat uit een knop en een deelvenster dat groter wordt wanneer een gebruiker op een knop klikt of tikt. Het deelvenster bevat afzonderlijke gereedschappen voor Favorieten.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e3c90320-b6fc-4a43-b75f-d39234b1e73c
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# Menu Favorieten{#favorites-menu}

De het menudrop-down lijst van Favorieten verschijnt in de controlebar. Het bestaat uit een knop en een deelvenster dat groter wordt wanneer een gebruiker op een knop klikt of tikt. Het deelvenster bevat afzonderlijke gereedschappen voor Favorieten.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De positie en grootte van het menu Favorieten in de gebruikersinterface van de viewer worden bepaald met de volgende CSS-klassenkiezer:

```
.s7ecatalogviewer .s7favoritesmenu
```

**CSS-eigenschappen van de menuknop Favorieten**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> De verschuiving vanaf de bovenkant van de besturingsbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> De afstand aan de volgende knoop op de linkerzijde, of de linkerkant van de controlebar als dit de eerste knoop in een rij is. </p> </td> 
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

Voorbeeld - Aan opstelling een menu van Favorieten dat vier pixel van de bovenkant van de controlebar en tien pixel van de dichtste knoop aan de linkerzijde wordt geplaatst en 28 x 28 pixel wordt gerangschikt:

```
.s7ecatalogviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

De vormgeving van de menuknop Favorieten wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton
```

**CSS-eigenschappen van de knop Favorieten**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p> De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie .

Voorbeeld - Aan opstelling een de menuknoop van Favorieten die een verschillende beeld voor elk van de vier verschillende knoopstaten toont:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

De vormgeving van het deelvenster dat afzonderlijke pictogrammen voor Favorieten bevat, wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel
```

**CSS-eigenschappen van het deelvenster Favorieten**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>De achtergrondkleur van het deelvenster. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - Een deelvenster instellen voor een transparante kleur:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```

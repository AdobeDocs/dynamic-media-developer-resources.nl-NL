---
description: De het menudrop-down lijst van Favorieten verschijnt in de controlebar. Het bestaat uit een knop en een deelvenster dat groter wordt wanneer een gebruiker op een knop klikt of tikt. Het deelvenster bevat afzonderlijke gereedschappen voor Favorieten.
seo-description: De het menudrop-down lijst van Favorieten verschijnt in de controlebar. Het bestaat uit een knop en een deelvenster dat groter wordt wanneer een gebruiker op een knop klikt of tikt. Het deelvenster bevat afzonderlijke gereedschappen voor Favorieten.
seo-title: Menu Favorieten
solution: Experience Manager
title: Menu Favorieten
topic: Dynamic media
uuid: 46de2a74-690e-4010-8a71-54206dd02fd0
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Menu Favorieten{#favorites-menu}

De het menudrop-down lijst van Favorieten verschijnt in de controlebar. Het bestaat uit een knop en een deelvenster dat groter wordt wanneer een gebruiker op een knop klikt of tikt. Het deelvenster bevat afzonderlijke gereedschappen voor Favorieten.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De positie en grootte van het menu Favorieten in de gebruikersinterface van de viewer worden bepaald met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7favoritesmenu
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

Voorbeeld - stel een menu Favorieten in dat vier pixels van de bovenkant van de besturingsbalk en tien pixels van de dichtstbijzijnde knop naar links wordt gepositioneerd en dat 28 x 28 pixels groot is.

```
.s7ecatalogsearchviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

De vormgeving van de menuknop Favorieten wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton
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
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld: stel een knop in het menu Favorieten in die een andere afbeelding weergeeft voor elk van de vier verschillende knopstatussen.

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

De vormgeving van het deelvenster dat afzonderlijke pictogrammen voor Favorieten bevat, wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel
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

Voorbeeld: stel een deelvenster zo in dat het een transparante kleur heeft.

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```


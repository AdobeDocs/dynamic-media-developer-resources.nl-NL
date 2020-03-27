---
description: De weergave Favorieten bestaat uit een kolom met miniatuurafbeeldingen.
seo-description: De weergave Favorieten bestaat uit een kolom met miniatuurafbeeldingen.
seo-title: Weergave Favorieten
solution: Experience Manager
title: Weergave Favorieten
topic: Dynamic media
uuid: 6b954bec-0678-4970-b83a-c2d8fea06a25
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Weergave Favorieten{#favorites-view}

De weergave Favorieten bestaat uit een kolom met miniatuurafbeeldingen.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

De weergave van de weergavecontainer Favorieten wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogviewer .s7favoritesview
```

De positie en de hoogte van de mening van Favorieten wordt beheerd door de mening; in CSS is het alleen mogelijk om de breedte te definiëren.

**CSS-eigenschappen van de weergave Favorieten**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur van de weergave Favorieten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de weergave. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - om een weergave Favorieten in te stellen die 100 pixels breed is en een halftransparante grijze achtergrond heeft.

```
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

De afstand tussen miniaturen Favorieten wordt geregeld met de volgende CSS-klassenkiezer:

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

**CSS-eigenschappen van de miniaturen Favorieten**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p> De grootte van de verticale marge rond elke miniatuur. De werkelijke miniatuurafstand is gelijk aan de som van de boven- en ondermarge die is ingesteld voor <span class="codeph"> .s7minicel </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - om een afstand van 10 pixels in te stellen.

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

De vormgeving van afzonderlijke miniaturen wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

**CSS-eigenschappen van de miniaturen Favorieten**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de miniatuur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de miniatuur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Rand van de miniatuur. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Miniatuur ondersteunt de `state` kenmerkkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende miniatuurtoestanden. Dit komt met name `state="selected"` overeen met de miniatuur die onlangs door de gebruiker is geselecteerd. `state="default"` komt overeen met de overige miniaturen. En `state="over"` wordt gebruikt bij muisaanwijzer.

Voorbeeld: als u miniaturen wilt instellen van 75 x 75 pixels, hebt u een lichtgrijze standaardrand en een donkergrijze geselecteerde rand.

```
.s7ecatalogviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

De vormgeving van het label van de miniatuur wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogviewer .s7favoritesview .s7label
```

**CSS-eigenschappen van het label Favorieten**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> lettertypefamilie </span> </p> </td> 
   <td colname="col2"> <p>Fontnaam. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - voor het instellen van labels met een Helvetica-lettertype van 14 pixels.

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```


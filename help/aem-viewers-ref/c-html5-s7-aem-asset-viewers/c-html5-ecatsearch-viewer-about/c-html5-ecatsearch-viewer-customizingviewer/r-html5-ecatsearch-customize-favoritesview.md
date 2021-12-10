---
title: Weergave Favorieten
description: De weergave Favorieten bestaat uit een kolom met miniatuurafbeeldingen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 8daf3d19-615b-4d62-a6f5-6a153d193b88
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# Weergave Favorieten{#favorites-view}

De weergave Favorieten bestaat uit een kolom met miniatuurafbeeldingen.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

De vormgeving van de container van de folioweergave wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7favoritesview
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
.s7ecatalogsearchviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

De afstand tussen miniaturen Favorieten wordt geregeld met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell
```

**CSS-eigenschappen van de miniaturen Favorieten**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p> De grootte van de verticale marge rond elke miniatuur. De werkelijke miniatuurafstand is gelijk aan de som van de boven- en ondermarge die is ingesteld voor <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - tien pixelspatiëring instellen.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

De vormgeving van afzonderlijke miniaturen wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb
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
>De miniatuur ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende miniatuurtoestanden. Met name: `state="selected"` komt overeen met de miniatuur die onlangs door de gebruiker is geselecteerd. while `state="default"` komt overeen met de overige miniaturen. en `state="over"` wordt gebruikt bij muisaanwijzer.

Voorbeeld - Als u miniaturen wilt instellen die 75 x 75 pixels zijn, hebt u een lichtgrijze standaardrand en een donkergrijze geselecteerde rand.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

De vormgeving van het label van de miniatuur wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7favoritesview .s7label
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

Voorbeeld - voor het instellen van labels met een Helvetica®-lettertype van 14 pixels.

```
.s7ecatalogsearchviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```

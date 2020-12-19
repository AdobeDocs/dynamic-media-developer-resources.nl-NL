---
description: De hoofdweergave bestaat uit de catalogusafbeelding. U kunt een veeggebaar maken om naar een andere pagina te gaan of door te zoomen.
seo-description: De hoofdweergave bestaat uit de catalogusafbeelding. U kunt een veeggebaar maken om naar een andere pagina te gaan of door te zoomen.
seo-title: Paginaweergave
solution: Experience Manager
title: Paginaweergave
topic: Dynamic media
uuid: 5e247f56-f0da-487b-8e03-587b9d36aa39
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---


# Paginaweergave{#page-view}

De hoofdweergave bestaat uit de catalogusafbeelding. U kunt een veeggebaar maken om naar een andere pagina te gaan of door te zoomen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van het weergavegebied wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogviewer .s7pageview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur van de hoofdweergave in hexadecimale notatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>De cursor die over de hoofdweergave wordt weergegeven. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - om de hoofdweergave transparant te maken.

```
.s7ecatalogviewer .s7pageview { 
 background-color: transparent; 
}
```

Op desktopsystemen ondersteunt de component de `cursortype`-kenmerkkiezer die op de klasse `.s7pageview` kan worden toegepast en bepaalt het type cursor op basis van componentstatus en gebruikersactie. De volgende `cursortype` waarden worden ondersteund:

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Waarde </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default  </span> </p> </td> 
   <td colname="col2"> <p>Wordt weergegeven wanneer op de afbeelding niet kan worden ingezoomd vanwege een kleine afbeeldingsresolutie, componentinstellingen of beide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomine  </span> </p> </td> 
   <td colname="col2"> <p>Wordt weergegeven wanneer op de afbeelding kan worden ingezoomd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset  </span> </p> </td> 
   <td colname="col2"> <p>Wordt weergegeven wanneer de afbeelding zich op het maximale zoomniveau bevindt en kan worden teruggezet op de begintoestand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slepen  </span> </p> </td> 
   <td colname="col2"> <p>Wordt weergegeven wanneer de gebruiker de afbeelding pant waarop is ingezoomd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dia  </span> </p> </td> 
   <td colname="col2"> <p>Wordt weergegeven wanneer de gebruiker een afbeeldingswisseling uitvoert door een horizontale veegbeweging of tikken uit te voeren. </p> </td> 
  </tr> 
 </tbody> 
</table>

De paginascheidingslijn die de linker- en rechterpagina van de catalogusspread visueel van elkaar scheidt, wordt bestuurd met de volgende CSS-klassenkiezer:

`.s7ecatalogviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> De breedte van de paginascheiding. Stel in op <span class="codeph"> 0 </span> px om de scheidingslijn volledig te verbergen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p>De afbeelding die u als scheidingsteken voor de pagina wilt gebruiken. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - voor een scheidingslijn van 40 pixels breed met een halftransparante afbeelding.

```
.s7ecatalogviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>Wanneer de `frametransition` bepaling aan `turn` of `auto` (op Desktopsystemen) wordt geplaatst, wordt de verschijning van de paginaverdeler gecontroleerd met de `pageturnstyle` bepaling en de `.s7pagedivider` CSS klasse wordt genegeerd.

Het is mogelijk om de weergave van aangepaste muiscursors te configureren over het hoofdviewergebied. Dit wordt gecontroleerd met de extra kenmerkenselecteurs die op `.s7ecatalogviewer .s7pageview` CSS klasse worden toegepast:

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default  </span> </p> </td> 
   <td colname="col2"> <p> Normaal gesproken wordt een pijl weergegeven voor een afbeelding waarop niet kan worden ingezoomd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomine  </span> </p> </td> 
   <td colname="col2"> <p> Hiermee kunt u zien wanneer op een afbeelding kan worden ingezoomd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset  </span> </p> </td> 
   <td colname="col2"> <p>Toont wanneer een beeld bij maximumgezoem is en kan worden teruggesteld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slepen  </span> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt getoond wanneer de gebruiker een sleepbewerking uitvoert op ingezoomde afbeeldingen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dia  </span> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt getoond wanneer de gebruiker een afbeelding omwisselt met gebruik van diabeweging </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld: gebruik verschillende muiscursors voor elk type componentstatus.

```
.s7ecatalogviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```


---
description: Afhankelijk van de waarde van de modusparameter worden in de viewer pictogrammen voor afbeeldingen met hyperlinks in de hoofdweergave weergegeven op plaatsen waar kaarten oorspronkelijk zijn gemaakt in Dynamic Media Classic of worden exacte gebieden weergegeven die overeenkomen met de vorm van de oorspronkelijke afbeeldingen met hyperlinks.
solution: Experience Manager
title: Afbeeldingskaart, effect
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3816118f-4eb7-4436-9f54-155dde077734
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Afbeeldingskaart, effect{#image-map-effect}

Afhankelijk van de waarde van de modusparameter worden in de viewer pictogrammen voor afbeeldingen met hyperlinks in de hoofdweergave weergegeven op plaatsen waar kaarten oorspronkelijk zijn gemaakt in Dynamic Media Classic of worden exacte gebieden weergegeven die overeenkomen met de vorm van de oorspronkelijke afbeeldingen met hyperlinks.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van het afbeeldingskaartpictogram wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>De klasse `s7mapoverlay` CSS die in het verleden is gebruikt om afbeeldingskaartpictogrammen op te maken, is nu afgekeurd. gebruik in plaats hiervan `s7icon`.

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p>Pictogramafbeeldingskaart, illustraties. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van afbeeldingskaart in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte afbeeldingskaart in pixels. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het pictogram Afbeeldingskaart ondersteunt de kenmerkenkiezer `state`, die u kunt gebruiken om verschillende skins toe te passen op de pictogramstatussen `default` en `active`.

Voorbeeld: stel een pictogram voor een afbeelding met hyperlinks van 28 x 28 pixels in en geef een andere afbeelding weer voor elk van de twee verschillende pictogramstaten.

```
.s7ecatalogviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

Zie ook [Ondersteuning voor afbeeldingen met hyperlinks](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a).

De vormgeving van het gebied met afbeeldingskaart wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background  </span> </p> </td> 
   <td colname="col2"> <p> Vulkleur van gebied Afbeeldingskaart. </p> <p>Opgegeven in de indeling #RRGGBB, RGB(R,G,B) of RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Vulkleur van gebied Afbeeldingskaart. </p> <p>Opgegeven in de indeling #RRGGBB, RGB(R,G,B) of RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p> Randstijl van afbeeldingskaart. </p> <p>Opgegeven als <span class="codeph"> <span class="varname"> breedte </span> effen <span class="varname"> kleur </span> </span>, waarbij <span class="codeph"> <span class="varname"> breedte </span> </span> wordt uitgedrukt in pixels en <span class="codeph"> <span class="varname"> kleur </span> </span> is ingesteld als ingesteld #RRGGBB, RGB(R,G,B) of RGBA(R,G,B,A). </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - stel een transparant gebied voor een afbeelding met een zwarte pixelrand van `1` in:

```
.s7ecatalogviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

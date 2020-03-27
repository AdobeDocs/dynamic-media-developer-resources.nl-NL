---
description: Hoofdstalen bestaan uit een rij miniatuurafbeeldingen met optionele schuifknoppen aan de linker- en rechterkant. Schuifknoppen zijn alleen zichtbaar op het bureaublad als alle miniaturen niet in de breedte van de container passen. Op mobiele apparaten, of als de duimnagels in de containerbreedte kunnen passen, worden de rolknopen niet getoond.
seo-description: Hoofdstalen bestaan uit een rij miniatuurafbeeldingen met optionele schuifknoppen aan de linker- en rechterkant. Schuifknoppen zijn alleen zichtbaar op het bureaublad als alle miniaturen niet in de breedte van de container passen. Op mobiele apparaten, of als de duimnagels in de containerbreedte kunnen passen, worden de rolknopen niet getoond.
seo-title: Hoofdstalen
solution: Experience Manager
title: Hoofdstalen
topic: Dynamic media
uuid: a968372d-3d11-45d7-b17f-50ec998f5e88
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Hoofdstalen{#main-swatches}

Hoofdstalen bestaan uit een rij miniatuurafbeeldingen met optionele schuifknoppen aan de linker- en rechterkant. Schuifknoppen zijn alleen zichtbaar op het bureaublad als alle miniaturen niet in de breedte van de container passen. Op mobiele apparaten, of als de duimnagels in de containerbreedte kunnen passen, worden de rolknopen niet getoond.

De vormgeving van de stalencontainer wordt beheerd met de CSS-klassenkiezer:

```
.s7mixedmediaviewer .s7swatches
```

**CSS-eigenschappen van de stalen**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van de stalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>De verticale verschuiving van stalen ten opzichte van de viewercontainer. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - voor het instellen van stalen met een hoogte van 100 pixels.

```
.s7mixedmediviewer .s7swatches { 
 height: 100px;  
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De afstand tussen de staalminiaturen wordt geregeld met de volgende CSS-klassenkiezer:

`.s7mixedmediaviewer .s7swatches .s7thumbcell`

<table id="table_ECE063DB98154E099FB024F66FF877D7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p> De grootte van de horizontale en verticale marge rond elke miniatuur. De werkelijke miniatuurafstand is gelijk aan de som van de linker- en rechtermarge die is ingesteld voor <span class="codeph"> .s7minicel </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld**

U stelt de tussenruimte in op tien pixels, zowel verticaal als horizontaal.

```
.s7mixedmediaviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

De weergave van de afzonderlijke miniatuur wordt bepaald door de volgende CSS-klassenkiezer:

`.s7mixedmediaviewer .s7swatches .s7thumb`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
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
>De miniatuur ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende miniatuurtoestanden. Dit komt met name `state="selected"` overeen met de miniatuur van de afbeelding die momenteel wordt weergegeven in de hoofdweergave, `state="default"` komt overeen met de overige miniaturen en `state="over"` wordt gebruikt bij de muisaanwijzer.

Voorbeeld: als u miniaturen wilt instellen die 56 x 56 pixels zijn, hebt u een lichtgrijze standaardrand en een donkergrijze geselecteerde rand.

```
.s7mixedmediaviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7mixedmediaviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7mixedviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

Het type element wordt weergegeven als een pictogram dat boven op de miniatuurafbeelding wordt geplaatst en wordt bestuurd met de volgende CSS-klassenkiezer:

`.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay`

<table id="table_460FC57D12CC4B52B3782F4DFAC3A194"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de pictogrambedekking. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de pictogrambedekking. </p> </td> 
  </tr> 
 </tbody> 
</table>

De bedekking ondersteunt de `type` kenmerkenkiezer met de volgende mogelijke waarden: `image` (voor afzonderlijke afbeeldingen), `swatchset` (voor stalensets), `spinset` (voor centrifuges) en `video` (voor afzonderlijke video&#39;s of adaptieve videosets).

Voorbeeld - voor het instellen van pictogramoverlays voor centrifuges, stalensets en video&#39;s:

```
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="swatchset"] { 
 background-image: url(images/v2/ThumbOverlaySwatchSet.png);  
} 
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="spinset"] { 
 background-image: url(images/v2/ThumbOverlaySpinSet.png);  
} 
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="video"] { 
 background-image: url(images/v2/ThumbOverlayVideo.png);  
}
```

De vormgeving van de linker- en rechterschuifknoppen wordt bepaald door de volgende CSS-klassekiezers:

`.s7mixedmediaviewer .s7swatches .s7scrollleftbutton`

`.s7mixedmediaviewer .s7swatches .s7scrollrightbutton`

Het is niet mogelijk om rolknopen te plaatsen gebruikend CSS `top`, `left`, `bottom`, en `right` eigenschappen. In plaats daarvan worden ze automatisch door de viewerlogica geplaatst.

<table id="table_A5663C4AAC4446168CAD8DBA2894BB9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de schuifknop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de schuifknop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p>De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden: `up`, `down`, `over`en `disabled`.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) voor meer informatie.

Voorbeeld - voor het instellen van schuifknoppen met een grootte van 56 x 56 pixels en voor elke status met een andere illustratie.

```
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```


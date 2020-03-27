---
description: Stalen bestaan uit een rij miniatuurafbeeldingen met optionele schuifknoppen aan de linker- en rechterkant.
seo-description: Stalen bestaan uit een rij miniatuurafbeeldingen met optionele schuifknoppen aan de linker- en rechterkant.
seo-title: Stalen
solution: Experience Manager
title: Stalen
topic: Dynamic media
uuid: ee91385d-a0ff-4419-8a86-e2b106030f98
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Stalen{#swatches}

Stalen bestaan uit een rij miniatuurafbeeldingen met optionele schuifknoppen aan de linker- en rechterzijde.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Schuifknoppen zijn alleen zichtbaar op het bureaublad als alle miniaturen niet in de breedte van de container passen. Op mobiele apparaten, of als de duimnagels in de containerbreedte kunnen passen, worden de rolknopen niet getoond.

**CSS-eigenschappen van de stalen**

De vormgeving van de stalencontainer wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7flyoutviewer .s7swatches
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> De breedte van de stalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van de stalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p> De verticale verschuiving van stalen ten opzichte van de viewercontainer. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - voor het instellen van stalen op 460 x 100 pixels:

```
.s7flyoutviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

**CSS-eigenschappen van de tussenruimte tussen miniatuurstalen**

De ruimte tussen staalminiaturen wordt bepaald door de CSS-klassenkiezer:

```
.s7flyoutviewer .s7swatches .s7thumbcell
```

<table id="table_70FAD50E38EB4647B8FAB832F552BBB8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
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

Voorbeeld - als u een afstand van 10 pixels wilt instellen, zowel verticaal als horizontaal:

```
.s7flyoutviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

**CSS-eigenschappen van de miniatuurstalen**

De vormgeving van afzonderlijke miniaturen wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7flyoutviewer .s7swatches .s7thumb
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> De breedte van de miniatuurstalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van de miniatuurstalen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>De rand van de miniatuurstalen. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De miniatuur ondersteunt de `state` kenmerkenkiezer, die wordt gebruikt om verschillende skins toe te passen op verschillende miniatuurtoestanden. Dit komt met name `state="selected"` overeen met de miniatuur van de afbeelding die momenteel wordt weergegeven in de hoofdweergave, `state="default"` komt overeen met de rest van de miniaturen en `state="over"` wordt gebruikt bij de muisaanwijzer.

Voorbeeld - als u miniaturen wilt instellen die 56 x 56 pixels zijn, een lichtgrijze standaardrand en een donkergrijze geselecteerde rand wilt hebben:

```
.s7flyoutviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7flyoutviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7flyoutviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

**CSS-eigenschappen van de linker- en rechterschuifknoppen**

De weergave van linker- en rechterschuifknoppen wordt bepaald door de volgende CSS-klassenkiezers:

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton 
.s7flyoutviewer .s7swatches .s7scrollrightbutton
```

Het is niet mogelijk om rolknopen te plaatsen gebruikend CSS `top`, `left`, `bottom`, en `right` eigenschappen. In plaats daarvan worden ze automatisch door de viewerlogica geplaatst.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> De breedte van de schuifknop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van de schuifknop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p>De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt de `state` kenmerkenkiezer, die wordt gebruikt om verschillende skins toe te passen op knoptoestanden `up`, `down`, `over`, en `disabled`.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) voor meer informatie.

Voorbeeld - voor het instellen van schuifknoppen met een grootte van 56 x 56 pixels en voor elke status een andere illustratie:

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```


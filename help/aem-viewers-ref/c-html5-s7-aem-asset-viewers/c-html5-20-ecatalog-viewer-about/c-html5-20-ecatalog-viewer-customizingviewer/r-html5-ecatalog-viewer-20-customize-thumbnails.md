---
description: Miniaturen bestaan uit een raster van miniatuurafbeeldingen met een optionele schuifbalk aan de rechterkant om verticaal schuiven mogelijk te maken.
seo-description: Miniaturen bestaan uit een raster van miniatuurafbeeldingen met een optionele schuifbalk aan de rechterkant om verticaal schuiven mogelijk te maken.
seo-title: Miniaturen
solution: Experience Manager
title: Miniaturen
topic: Dynamic media
uuid: 340b81e0-77df-4b44-a462-b98bcc96d707
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 0%

---


# Miniaturen{#thumbnails}

Miniaturen bestaan uit een raster van miniatuurafbeeldingen met een optionele schuifbalk aan de rechterkant om verticaal schuiven mogelijk te maken.

U schakelt miniaturen in of uit door op de miniatuurknop in de hoofdbesturingsbalk te klikken. Wanneer miniaturen actief zijn, worden deze in de modale modus weergegeven boven op de gebruikersinterface van de viewer. De viewerlogica wijzigt de grootte van de miniatuurcontainer automatisch in het gehele viewergebied.

De weergave van de container met miniaturen wordt bepaald door de volgende CSS-klassenkiezer:

`.s7ecatalogviewer .s7thumbnailgridview`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> De verticale verschuiving van de container met miniaturen vanaf de bovenkant van de viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p>De bovenmarge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p>De linkermarge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge-rechts  </span> </p> </td> 
   <td colname="col2"> <p>De rechtermarge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom  </span> </p> </td> 
   <td colname="col2"> <p>De ondermarge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>De achtergrondkleur van het gebied met miniaturen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u miniaturen wilt instellen met een verschuiving van 32 pixels ten opzichte van de bovenkant, 5 pixels aan de linker- en rechterzijde en 8 pixels aan de onderzijde, met een achtergrond van `0xDDDDDD`.

```
.s7ecatalogviewer .s7thumbnailgridview { 
 top: 32px; 
 margin-left: 5px; 
 margin-right: 5px; 
 margin-bottom: 8px; 
 background-color: rgb(221, 221, 221); 
}
```

De afstand tussen miniaturen wordt geregeld met de volgende CSS-klassenkiezer:

`.s7ecatalogviewer .s7thumbnailgridview .s7thumbcell`

<table id="table_1D93AB60E57F49A8838EA825CD6B7897"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge  </span> </p> </td> 
   <td colname="col2"> <p> De grootte van de horizontale en verticale marge rond elke miniatuur. De werkelijke horizontale miniatuurafstand is gelijk aan de som van de linker- en rechtermarge die is ingesteld voor <span class="codeph"> .s7thumbcell </span>. De verticale miniatuurafstand is gelijk aan de som van de boven- en ondermarge. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - om een ruimte van 10 pixels zowel verticaal als horizontaal in te stellen.

```
.s7ecatalogviewer .s7thumbnailgridview .s7thumbcell { 
 margin: 5px; 
}
```

De vormgeving van afzonderlijke miniaturen wordt bepaald door de volgende CSS-klassenkiezer:

`.s7ecatalogviewer .s7thumbnailgridview .s7thumb`

<table id="table_1D973EA6C36947F092AAA16CFE9B44A1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>De breedte van de miniatuur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van de miniatuur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>De rand van de miniatuur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>De achtergrondkleur van de miniatuur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Als de gebruiker op aanraakapparaten wordt gedraaid in de staande modus, kan de grootte van de miniaturen de helft bedragen van de configuratie als de gebruiker besluit de catalogusspread op afzonderlijke pagina&#39;s te splitsen.

>[!NOTE]
>
>Miniatuur ondersteunt de kenmerkenkiezer `state`, die kan worden gebruikt om verschillende skins toe te passen op verschillende miniatuurtoestanden. Met name `state="selected"` komt overeen met de miniatuur van de afbeelding die momenteel wordt weergegeven in de hoofdweergave, `state="default"` komt overeen met de rest van de miniaturen en `state="over"` wordt gebruikt bij de muisaanwijzer.

Voorbeeld: als u miniaturen wilt instellen die 120 x 85 pixels zijn, hebt u een witte achtergrond, een lichtgrijze standaardrand en een donkergrijze geselecteerde rand.

```
.s7ecatalogviewer .s7thumbnailgridview .s7thumb { 
 width:120px; 
 height:85px; 
 background-color: rgb(255, 255, 255); 
 border: solid 1px #999999; 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7thumb[state="selected"]{ 
 border: solid 2px #666666; 
}
```

De vormgeving van het label van de miniatuur wordt bepaald door de volgende CSS-klassenkiezer:

`.s7ecatalogviewer .s7thumbnailgridview .s7label`

<table id="table_E242176042F247F8B51A0D5ADB645E20"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Fontnaam. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte  </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u labels wilt instellen voor gebruik van een Helvetica-lettertype van 14 pixels.

```
.s7ecatalogviewer .s7thumbnailgridview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 12px; 
}
```

Als er meer miniaturen zijn dan verticaal in de weergave passen, wordt met miniaturen de verticale schuifbalk aan de rechterkant weergegeven. De vormgeving van het gebied van de schuifbalk wordt bepaald door de volgende CSS-klassenkiezer:

`.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar`

<table id="table_F05EC87CD9A946DB9B4B2B48E0784168"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>De breedte van de schuifbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> De verticale verschuiving van de schuifbalk ten opzichte van de bovenkant van het gebied met miniaturen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>De verticale verschuiving van de schuifbalk ten opzichte van de onderkant van het gebied met miniaturen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p> De verschuiving van de horizontale schuifbalk ten opzichte van de rechterrand van het gebied met miniaturen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - om een schuifbalk in te stellen die 28 pixels breed is en een marge van 8 pixels heeft vanaf de bovenkant, de rechterkant en de onderkant van het miniatuurgebied.

```
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar { 
 top:8px; 
 bottom:8px; 
 right:8px; 
 width:28px; 
}
```

Het schuifbalkvak is het gebied tussen de bovenste en onderste schuifknop. De component stelt automatisch de positie en de hoogte van het spoor in. De track wordt bestuurd met de volgende CSS-klassenkiezer:

`.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolltrack`

<table id="table_EF1B91F9E984451EB0AB48175D917726"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>De breedte van het schuifbalkvak. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> De achtergrondkleur van het schuifbalkvak. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - voor het instellen van een schuifbalkvak met een breedte van 28 pixels en een halftransparante grijze achtergrond.

```
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

Het schuifbalkblokje beweegt verticaal binnen het gebied van het schuifvak. De verticale positie wordt volledig bepaald door de componentlogica, maar de hoogte van het blokje verandert niet dynamisch, afhankelijk van de hoeveelheid inhoud. De duimhoogte en andere aspecten worden gecontroleerd met de volgende CSS klassenselecteur:

`.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb`

<table id="table_5C791F6E90E64E7A9F1DB7C9B2FDC528"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>De breedte van het schuifbalkblokje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van de schuifbalkminiatuur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen boven  </span> </p> </td> 
   <td colname="col2"> <p>De verticale opvulling tussen de bovenkant van het schuifbalkvak. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen-onder  </span> </p> </td> 
   <td colname="col2"> <p>De verticale opvulling tussen de onderkant van het schuifbalkvak. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p>De afbeelding die voor een bepaalde duimstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Miniatuur ondersteunt de `state`-kenmerkkiezer, die kan worden gebruikt om verschillende skins toe te passen op de duimstatussen `up`, `down`, `over` en `disabled`.

Voorbeeld: als u een schuifbalkblokje van 28 x 45 pixels wilt instellen, hebt u bovenaan en onderaan een marge van 10 pixels en hebt u voor elk frame een andere illustratie.

```
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

De vormgeving van de bovenste en onderste schuifknoppen wordt bepaald door de volgende CSS-klassekiezers:

`.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton`

`.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton`

Het is niet mogelijk om de schuifknoppen te positioneren met de CSS-eigenschappen `top`, `left`, `bottom` en `right`. In plaats daarvan worden ze automatisch door de viewerlogica geplaatst.

<table id="table_89E64A138ABF463F9650BB454F22D530"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>De breedte van de knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van de knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p>De afbeelding die voor een bepaalde duimstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoppen ondersteunen de `state`-kenmerkkiezer, die kan worden gebruikt om verschillende skins toe te passen op de verschillende knopstatussen `up`, `down`, `over` en `disabled`.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - voor het instellen van schuifknoppen met een resolutie van 28 x 32 pixels en voor elke status een andere illustratie.

```
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```


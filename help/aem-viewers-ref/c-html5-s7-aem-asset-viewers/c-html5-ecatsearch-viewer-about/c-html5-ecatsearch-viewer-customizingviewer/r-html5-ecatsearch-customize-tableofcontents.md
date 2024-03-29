---
title: Inhoudsopgave
description: De inhoudsopgave is een knop op de hoofdbesturingsbalk. Als u deze optie inschakelt, wordt een vervolgkeuzelijst weergegeven met een lijst met pagina-indexen en -labels.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: bc597c68-b86c-4577-9d24-6999eccada78
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---

# Inhoudsopgave{#table-of-contents}

De inhoudsopgave is een knop op de hoofdbesturingsbalk. Als u deze optie inschakelt, wordt een vervolgkeuzelijst weergegeven met een lijst met pagina-indexen en -labels.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Gebaseerd op de configuratie, kan de lijst alle pagina&#39;s bevatten die in de catalogus aanwezig zijn of slechts die pagina&#39;s die expliciete vastgestelde etiketten hebben. Op desktopsystemen wordt rechts een schuifbalk weergegeven als de lijst langer is dan de beschikbare ruimte op het scherm.

De positie en grootte van de knop met de inhoudsopgave in de gebruikersinterface van de viewer worden bepaald met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7tableofcontents
```

**CSS-eigenschappen van de inhoudsopgave**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> De verschuiving vanaf de bovenkant van de besturingsbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> De afstand tot de volgende knoop op de linkerzijde, of de linkerkant van de controlebar als deze knoop eerste in een rij is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> De breedte van de knop voor de inhoudsopgave. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> De hoogte van de knop voor de inhoudsopgave. </p> </td> 
  </tr> 
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

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie .

Voorbeeld - Opstelling een knoop van de inhoudstafel die 4 pixel van de bodem en 43 pixel van de linkerzijde van de belangrijkste controlebar wordt geplaatst. De grootte is 28 x 28 pixels en er wordt een andere afbeelding weergegeven voor elk van de vier verschillende knopstatussen:

```
.s7ecatalogsearchviewer .s7tableofcontents { 
margin-top: 4px; 
margin-left: 10px; width: 28px; 
 height: 28px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='up'] { 
background-image:url(images/v2/TableOfContents_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='over'] { 
background-image:url(images/v2/TableOfContents_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='down'] { 
background-image:url(images/v2/TableOfContents_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='disabled'] { 
background-image:url(images/v2/TableOfContents_dark_disabled.png); 
}
```

De vormgeving van het vervolgkeuzemenu wordt bepaald door de volgende CSS-klassenkiezer:

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel
```

**CSS-eigenschappen van het vervolgkeuzemenu**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur van vervolgkeuzelijst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p> Interne verschuiving tussen de deelvenstergrenzen en de inhoud. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p> Slagschaduw rond het deelvenster. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het is niet mogelijk om de grootte of de positie van het vervolgkeuzepaneel vanuit CSS te bepalen; de component beheert zijn lay-out programmatically.

Voorbeeld - stel een vervolgkeuzelijst in met een halftransparante zwarte achtergrond, een marge van 5 pixels rondom de inhoud en een slagschaduw:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

De vormgeving van de afzonderlijke items wordt bepaald door de volgende CSS-klassenkiezer:

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item
```

**CSS-eigenschappen van het item**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Fontnaam. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van item. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Interne opvulling. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Vervolgkeuzelijstitem ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op de aanwijsstatus en de geselecteerde itemstatus.

Voorbeeld: stel een vervolgkeuzelijst in met een Helvetica®-lettertype van 14 pixels en een hoogte van 19 pixels. Een item heeft een donkergrijze achtergrond op de muisaanwijzer en een lichtgrijze achtergrond als dit is geselecteerd:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item { 
font-family: Helvetica,sans-serif; 
font-size: 14px; 
height: 19px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item[state="over"] { 
background-color: rgb(102, 102, 102); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item[state="selected"] { 
background-color: rgb(178, 178, 178); 
}
```

Een element dat de pagina-index weergeeft, wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index
```

**CSS-eigenschappen van de pagina-index**

<table id="table_FAA5072E4AAC48F4BE00B05D87FD9827"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> min-width </span> </p> </td> 
   <td colname="col2"> <p> Minimale breedte van element. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max. breedte </span> </p> </td> 
   <td colname="col2"> <p> Maximale breedte van element. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvulling rechts </span> </p> </td> 
   <td colname="col2"> <p> Afstand tussen de pagina-index en het paginalabel. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het is mogelijk de pagina-index volledig te verbergen door de instelling `display:none` voor de `s7index` CSS-klasse.

Voorbeeld 1 - stel een pagina-index in met een minimale breedte van 40 pixels, een maximale breedte van 70 pixels en een marge van 5 pixels aan de rechterkant:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

Voorbeeld 2 - pagina-index verbergen:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index { 
display: none; 
}
```

Het paginalabel wordt beheerd met de volgende CSS-klassenkiezer:

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7label
```

**CSS-eigenschappen van het paginalabel**

<table id="table_A42E372D931D4F04855EE5AB5530CB12"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> min-width </span> </p> </td> 
   <td colname="col2"> <p> Minimale breedte van element. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max. breedte </span> </p> </td> 
   <td colname="col2"> <p> Maximale breedte van element. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - stel een pagina-index in met een minimale breedte van 40 pixels en een maximale breedte van 240 pixels:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

Als er meer items zijn dan verticaal in het vervolgkeuzevenster kunnen worden geplaatst - en het systeem is een bureaublad -, wordt er aan de rechterkant van het deelvenster een verticale schuifbalk weergegeven. De vormgeving van het gebied van de schuifbalk wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar
```

**CSS-eigenschappen van de schuifbalk**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> De breedte van de schuifbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> De verticale verschuiving van de schuifbalk ten opzichte van de bovenkant van het deelvenstergebied. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p> De verticale verschuiving van de schuifbalk ten opzichte van de onderkant van het deelvenstergebied. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p> De verschuiving van de horizontale schuifbalk ten opzichte van de rechterrand van het deelvenstergebied. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - stel een schuifbalk in die 28 pixels breed is en geen marge heeft voor het boven-, rechter- of ondergebied van het deelvenster:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

Schuifbalktrack is het gebied tussen de bovenste en onderste schuifknop. De component stelt automatisch de positie en de hoogte van het spoor in. De track wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
```

**CSS-eigenschappen van de schuiftrack**

<table id="table_E49EE04B3FF64AB2948E7C09DF3EA1B7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>De spoorbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>De achtergrondkleur van de track. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - stel een schuifbalkvak in met een breedte van 28 pixels en een halftransparante grijze achtergrond:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

Het schuifbalkblokje verplaatst zich verticaal binnen het gebied van het schuifvak. De verticale positie wordt bepaald door de componentlogica. De hoogte van het blokje verandert echter niet dynamisch, afhankelijk van de hoeveelheid inhoud. U kunt de duimhoogte en andere aspecten met de volgende CSS klassenselecteur vormen:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

**CSS-eigenschappen van het schuifbalkblokje**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>De breedte van het blokje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van de duim. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen boven </span> </p> </td> 
   <td colname="col2"> <p> De verticale opvulling tussen de bovenkant van de track. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen-onder </span> </p> </td> 
   <td colname="col2"> <p>De verticale opvulling tussen de onderkant van de track. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p> De afbeelding die voor een bepaalde duimstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Miniatuur ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op de `up`, `down`, `over`, en `disabled` duimstaten.

Voorbeeld: stel een schuifbalkblokje in van 28 x 45 pixels, met een marge van 10 pixels boven en onder en met verschillende illustraties voor elk frame:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

De vormgeving van de bovenste en onderste schuifknoppen wordt bepaald door de volgende CSS-klassekiezers:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

Het is niet mogelijk om de schuifknoppen met CSS te positioneren `top`, `left`, `bottom`, en `right` eigenschappen; in plaats daarvan worden ze automatisch door de viewerlogica geplaatst.

**CSS-eigenschappen van de knop Omhoog schuiven en Omlaag schuiven**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>De knopbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>De knophoogte. </p> </td> 
  </tr> 
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
>De knop ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op de `up`, `down`, `over`, en `disabled` knopstatussen.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie .

Voorbeeld: stel schuifknoppen in met een resolutie van 28 x 32 pixels en een andere illustratie voor elke status:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```

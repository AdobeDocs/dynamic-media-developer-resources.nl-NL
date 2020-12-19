---
description: Het deelvenster met zoekresultaten bestaat uit het invoervak voor zoekopdrachten bovenaan en het hoofdgebied waar informatieve berichten of zoekresultaten worden weergegeven.
seo-description: Het deelvenster met zoekresultaten bestaat uit het invoervak voor zoekopdrachten bovenaan en het hoofdgebied waar informatieve berichten of zoekresultaten worden weergegeven.
seo-title: Deelvenster Zoekresultaten
solution: Experience Manager
title: Deelvenster Zoekresultaten
topic: Dynamic media
uuid: 43d8e003-79f7-4e41-98d7-b362ab7180ea
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '952'
ht-degree: 0%

---


# Deelvenster Zoekresultaten{#search-results-panel}

Het deelvenster met zoekresultaten bestaat uit het invoervak voor zoekopdrachten bovenaan en het hoofdgebied waar informatieve berichten of zoekresultaten worden weergegeven.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

Wanneer het deelvenster actief is, wordt de gebruikersinterface van de viewer bedekt met een halftransparante vulling. De kleur en dekking van deze vulling worden beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogviewer .s7searchpanel .s7backoverlay
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
   <td colname="col2"> <p>Kleur van de bedekking. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dekking  </span> </p> </td> 
   <td colname="col2"> <p>Dekking van de kleur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Het deelvenster met zoekresultaten neemt altijd alle beschikbare viewerhoogte in beslag. U kunt de breedte echter configureren. U kunt de breedte instellen op een absolute pixelwaarde. Dit is de standaardinstelling voor middelgrote en grote onderbrekingspunten. U kunt de breedte ook instellen op 100%, zodat het deelvenster met zoekresultaten het gehele viewergebied beslaat. De breedte van het deelvenster wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

**CSS-eigenschap van de ruimte voor zoekresultaten**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Breedte van de ruimte met zoekresultaten. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - voor het instellen van een deelvenster met zoekresultaten met een breedte van 250 pixels voor grote en middelgrote onderbrekingspunten en het gebruik van een deelvenster van volledige grootte voor kleine onderbrekingspunten:

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

De bovenkant van het paneel van onderzoeksresultaten wordt gewijd aan het vakje van de onderzoeksinput. De opvulling aan de zijkanten van het invoervak wordt bestuurd door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

**CSS-eigenschappen van de container voor zoekgegevens**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen  </span> </p> </td> 
   <td colname="col2"> <p> Opvulling rond het invoervak. </p> </td> 
  </tr> 
 </tbody> 
</table>

Het veld voor zoekinvoer wordt bestuurd door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput
```

**CSS-eigenschappen van het veld voor zoekinvoer**

<table id="table_9FB5E89847BF4C889DC22AD7E842C0F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van invoerveld voor zoekopdracht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen-links  </span> </p> </td> 
   <td colname="col2"> <p> De binnenste opvulling tussen de grenzen van het invoerveld en de invoertekst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Rand van het veld voor zoekinvoer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge  </span> </p> </td> 
   <td colname="col2"> <p>Marge van het veld voor zoekinvoer </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte  </span> </p> </td> 
   <td colname="col2"> <p>Grootte van het tekstlettertype. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - voor het instellen van een zoekinvoerveld met een hoogte van 0 pixels en een tekstlettertype van 14 pixels:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput { 
 padding-left:5px; 
 height:30px; 
 font-size:14px; 
}
```

De zoekknop links van het invoerveld voor zoekopdrachten in de vorm van het standaard &#39;uitziende glas&#39; wordt bestuurd door de volgende CSS-klassenkiezer:

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

**CSS-eigenschappen van de knop voor zoekinvoer**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de knop voor zoekinvoer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de knop voor zoekinvoer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p>De URL naar de pictogramafbeelding van het "kijkglas". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-size  </span> </p> </td> 
   <td colname="col2"> <p>De grootte van het "kijkglazen"-pictogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Rand van de knop voor zoekinvoer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge  </span> </p> </td> 
   <td colname="col2"> <p>Marge van de knop voor zoekinvoer. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld: een zoekknop instellen met het pictogram van 26 x 26 pixels voor &#39;uitziend glas&#39;; 30 pixels groot met een rand van 1 pixel:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton { 
 width:30px; 
 height:30px; 
 background-size:26px 26px; 
 background-image: url(images/v2/Search_form_field.png); 
 font-size:14px; 
 border: 1px solid #696969; 
}
```

Het deelvenster met zoekresultaten kan een tekstprompt weergeven wanneer de functie voor het eerst wordt aangeroepen. De gebruiker krijgt ook een bericht te zien wanneer zijn zoekopdracht geen resultaten heeft opgeleverd. In alle gevallen wordt de tekst weergegeven in het hoofdgedeelte van het deelvenster met zoekresultaten en wordt deze bestuurd door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

**CSS-eigenschappen van de zoekinformatie**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur  </span> </p> </td> 
   <td colname="col2"> <p> Kleur van tekst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Naam van tekstlettertype. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align  </span> </p> </td> 
   <td colname="col2"> <p>Horizontale tekstuitlijning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte  </span> </p> </td> 
   <td colname="col2"> <p>Grootte van lettertypetekst. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Dit tekstpaneel steunt `state` attributenselecteur, die kan worden gebruikt om verschillende stijlen op verschillende tekstberichten toe te passen. Met name `state='prompt'` komt overeen met de tekstprompt die wordt weergegeven wanneer het deelvenster voor de eerste keer wordt aangeroepen; `state='results'` komt overeen met de tekst met informatie over zoekresultaten; en `state='no_results'` komt overeen met de tekst die wordt weergegeven wanneer de zoekopdracht geen resultaten heeft opgeleverd.

De berichttekst kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - voor het instellen van een deelvenster met een grijs lettertype van 18 pixels:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

Zoekresultaten worden weergegeven als één kolom of één rij miniaturen voor pagina&#39;s met zoekresultaten. De afstand tussen miniaturen van zoekresultaten wordt bepaald door de volgende CSS-klassenkiezer:

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**CSS-eigenschappen van de miniatuurcellen**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge  </span> </p> </td> 
   <td colname="col2"> <p> De grootte van de verticale marge rond elke miniatuur. De werkelijke miniatuurafstand is gelijk aan de som van de boven- en ondermarge die is ingesteld voor <span class="codeph"> .s7minicel </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - voor het instellen van een afstand van 10 pixels:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

De vormgeving van afzonderlijke miniaturen wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**CSS-eigenschappen van de miniatuur**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de miniatuur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de miniatuur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Rand van de miniatuur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u miniaturen wilt instellen die 215 x 129 pixels zijn, hebt u een lichtgrijze standaardrand en een donkergrijze geselecteerde rand:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

De vormgeving van het label van de miniatuur wordt bepaald door de volgende CSS-klassenkiezer:

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

**CSS-eigenschappen van het label**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur  </span> </p> </td> 
   <td colname="col2"> <p> Tekstkleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Naam van tekstlettertype. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte  </span> </p> </td> 
   <td colname="col2"> <p>Grootte van tekstlettertype. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - voor het instellen van labels met een lettertype van 12 pixels, grijs en Helvetica:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

Op systemen die muisinvoer gebruiken, verschijnen twee rolknopen bij de bodem van het paneel van onderzoeksresultaten aan een gebruiker scroll door de onderzoeksresultaten. De vormgeving van de schuifknoppen Omhoog en Omlaag wordt bepaald door de volgende CSS-klassekiezers:

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

Het is niet mogelijk om schuifknoppen te positioneren met de CSS-eigenschappen top, left, bottom en right. In plaats daarvan worden ze automatisch door de viewerlogica geplaatst.

**CSS-eigenschappen van de knop Omhoog en Omlaag schuiven**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de schuifknop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de schuifknop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p> De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoop steunt `state` attributenselecteur, die kan worden gebruikt om verschillende huiden op `"up"`, `"down"`, `"over"`, en `"disabled"` knoopstaten toe te passen.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - Een schuifknop van 125 x 35 pixels instellen met een andere illustratie voor elke status:

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_disabled.png);
```


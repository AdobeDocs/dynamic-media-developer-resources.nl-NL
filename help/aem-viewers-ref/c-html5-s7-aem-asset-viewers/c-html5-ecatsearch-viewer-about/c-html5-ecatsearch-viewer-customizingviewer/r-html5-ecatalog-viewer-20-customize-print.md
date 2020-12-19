---
description: Het gereedschap Afdrukken bestaat uit een knop die wordt toegevoegd aan de besturingsbalk en het modale dialoogvenster dat wordt weergegeven wanneer het gereedschap wordt geactiveerd.
seo-description: Het gereedschap Afdrukken bestaat uit een knop die wordt toegevoegd aan de besturingsbalk en het modale dialoogvenster dat wordt weergegeven wanneer het gereedschap wordt geactiveerd.
seo-title: Afdrukken
solution: Experience Manager
title: Afdrukken
topic: Dynamic media
uuid: 7be047d8-d1be-4bda-90ca-6b55c749cc64
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '1493'
ht-degree: 0%

---


# Afdrukken{#print}

Het gereedschap Afdrukken bestaat uit een knop die wordt toegevoegd aan de besturingsbalk en het modale dialoogvenster dat wordt weergegeven wanneer het gereedschap wordt geactiveerd.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De weergave van de knop Afdrukken wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7print
```

**CSS-eigenschappen van de knop Afdrukken**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> De verschuiving vanaf de bovenkant van de besturingsbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> De afstand aan de volgende knoop op de linkerzijde, of de linkerkant van de controlebar als dit de eerste knoop in een rij is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de knop. </p> </td> 
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
>Deze knoop steunt `state` attributenselecteur, die kan worden gebruikt om verschillende huiden op verschillende knoopstaten toe te passen.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - Een afdrukknop van 28 x 28 pixels instellen en een andere afbeelding voor elk van de vier verschillende knopstatussen weergeven.

```
.s7ecatalogsearchviewer .s7print { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7print[state='up'] { 
background-image:url(images/v2/Print_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7print[state='over'] { 
background-image:url(images/v2/Print_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7print[state='down'] { 
background-image:url(images/v2/Print_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7print[state='disabled'] { 
background-image:url(images/v2/Print_dark_disabled.png); 
}
```

De achtergrondoverlay die de webpagina bedekt wanneer het dialoogvenster actief is, wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay
```

**CSS-eigenschappen van de backoverlay**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dekking  </span> </p> </td> 
   <td colname="col2"> <p> Dekking van achtergrondbedekking. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Kleur van achtergrondbedekking. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u een achtergrondbedekking wilt instellen die grijs is met een dekking van 70%:

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Standaard wordt het modale dialoogvenster gecentreerd weergegeven op het scherm van desktopsystemen. De positie en grootte van het dialoogvenster worden beheerd door de component Het dialoogvenster wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7kprintdialog .s7dialog
```

**CSS-eigenschappen van het dialoogvenster**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Straal rand dialoogvenster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur van dialoogvenster; </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - Een dialoogvenster instellen voor een grijze achtergrond:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialog { 
background-color: #dddddd; 
}
```

De koptekst van het dialoogvenster bestaat uit een pictogram, een titeltekst en een sluitknop. De koptekstcontainer wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader
```

**CSS-eigenschappen van de koptekst van het dialoogvenster**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen  </span> </p> </td> 
   <td colname="col2"> <p> Opvulling binnen voor koptekstinhoud. </p> </td> 
  </tr> 
 </tbody> 
</table>

Het pictogram en de titeltekst worden verpakt in een extra container die met het volgende wordt bestuurd:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline
```

**CSS-eigenschappen van de dialoogregel**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen  </span> </p> </td> 
   <td colname="col2"> <p> Opvulling binnen voor het koptekstpictogram en de titel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Koptekstpictogram wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon
```

**CSS-eigenschappen van het pictogram van de koptekst in het dialoogvenster**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Pictogrambreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte pictogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p>Pictogramafbeelding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

De titel van de koptekst wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext
```

**CSS-eigenschappen van de koptekst van het dialoogvenster**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Fontgewicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte lettertype. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Lettertypefamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen  </span> </p> </td> 
   <td colname="col2"> <p>Opvulling van interne tekst. </p> </td> 
  </tr> 
 </tbody> 
</table>

Knop Sluiten wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7printdialog .s7closebutton
```

**CSS-eigenschappen van de knop close **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Verticale knoppositie ten opzichte van koptekstcontainer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p> Horizontale knoppositie ten opzichte van koptekstcontainer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Knopbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen  </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p>Knopafbeelding voor elk frame. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoop steunt `state` attributenselecteur, die kan worden gebruikt om verschillende huiden op verschillende knoopstaten toe te passen.

De knopinfo Sluiten en de titel van het dialoogvenster kunnen worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - om een dialoogkoptekst in te stellen met opvulling, een pictogram van 22 x 22 pixels, een vette titel van 16 punten en een knop Sluiten van 28 x 28 pixels, geplaatst op twee pixels van de bovenkant en twee pixels van de rechterkant van de container van het dialoogvenster:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgprint_cap.png"); 
    height: 22px; 
    width: 22px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

De voettekst van het dialoogvenster bestaat uit de knoppen Annuleren en Verzenden naar afdrukken. De voettekstcontainer wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter
```

**CSS-eigenschappen van de voettekst van het dialoogvenster **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p> Rand die u kunt gebruiken om de voettekst visueel te scheiden van de rest van het dialoogvenster. </p> </td> 
  </tr> 
 </tbody> 
</table>

De voettekst heeft een binnencontainer die beide knoppen bevat. De klasse wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer
```

**CSS-eigenschappen van de knopcontainer van het dialoogvenster**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen  </span> </p> </td> 
   <td colname="col2"> <p> Opvulling binnen tussen de voettekst en de knoppen. </p> </td> 
  </tr> 
 </tbody> 
</table>

De knop Annuleren wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton
```

**CSS-eigenschappen van de knop cancel van het dialoogvenster**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Knopbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur  </span> </p> </td> 
   <td colname="col2"> <p> De tekstkleur van de knoop voor elke staat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur van knop voor elk frame. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoop steunt `state` attributenselecteur, die kan worden gebruikt om verschillende huiden op verschillende knoopstaten toe te passen.

De knop Verzenden naar afdrukken wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton
```

**CSS-eigenschappen van de actieknop van het dialoogvenster**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Knopbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur  </span> </p> </td> 
   <td colname="col2"> <p> De tekstkleur van de knoop voor elke staat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur van knop voor elk frame. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoop steunt `state` attributenselecteur, die kan worden gebruikt om verschillende huiden op verschillende knoopstaten toe te passen.

Bovendien hebben beide knoppen dezelfde algemene CSS-klasse die CSS-instellingen kan bevatten die hetzelfde zijn voor andere knoppen in dialoogvensters:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button
```

**CSS-eigenschappen van de knop**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Dikte van lettertype knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte  </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Lettertypefamilie knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> regelhoogte  </span> </p> </td> 
   <td colname="col2"> <p> Teksthoogte in de knop. Heeft invloed op de verticale uitlijning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow  </span> </p> </td> 
   <td colname="col2"> <p>Slagschaduw. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge-rechts  </span> </p> </td> 
   <td colname="col2"> <p>Marge rechterknop. </p> </td> 
  </tr> 
 </tbody> 
</table>

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - voor het instellen van een voettekst in het dialoogvenster met een knop Annuleren van 64 x 34 en een knop Verzenden naar afdruk van 96 x 34, waarbij de tekstkleur en de achtergrondkleur voor elke knopstatus verschillen:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton { 
 width:96px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

Het hoofddialoogvenster (tussen de kop- en voettekst) bevat inhoud van het dialoogvenster. In alle gevallen beheert de component de breedte van dit gebied. Het is niet mogelijk om dit in CSS in te stellen. Het hoofddialoogvenster wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea
```

**CSS-eigenschappen van het weergavegebied van het dialoogvenster **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> De hoogte van het gebied van het hoofddialoogvenster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>De achtergrondkleur van het gebied van het hoofddialoogvenster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge  </span> </p> </td> 
   <td colname="col2"> <p>Buitenmarge. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u een hoofddialoogvenster wilt instellen met een automatisch berekende hoogte, een marge van 10 pixels en een witte achtergrond:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:auto; 
}
```

Alle formulierinhoud (zoals labels en invoervelden) bevindt zich in een container die wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody
```

**CSS-eigenschappen van de hoofdtekst van het dialoogvenster **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen  </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u formulierinhoud wilt instellen met tien pixelopvulling:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody { 
    padding: 10px; 
}
```

Het formulier in het dialoogvenster wordt regel voor regel ingevuld, waarbij elke regel een deel van de formulierinhoud bevat (zoals een label en een tekstinvoerveld). Eén formulierregel wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**CSS-eigenschappen van de regel met dialoogvensters**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen  </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnenlijn. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u een dialoogvenster wilt instellen met tien pixelopvulling voor elke regel:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

De grootte van het blok met dialoogvenster-inhoud wordt beheerd met de volgende CSS-klassenkiezer:

```
 .s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide
```

**CSS-eigenschappen van de invoerbreedte van het dialoogvenster**

<table id="table_FFF0B02B564C443CA8713103D723C733"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Blokbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen  </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnenlijn. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u een inhoudsblok wilt instellen op 430 pixels breed en onderaan een opvulling van 10 pixels bevat:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Alle statische labels in het dialoogvenster worden beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel
```

Deze klasse is niet geschikt voor het bepalen van de grootte of positie van het label, omdat u deze kunt toepassen op tekst op verschillende plaatsen in de gebruikersinterface van het formulier.

**CSS-eigenschappen van het label van het dialoogvenster. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Breedte van lettertype label. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte  </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte label. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Lettertypefamilie label. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur  </span> </p> </td> 
   <td colname="col2"> <p>Labeltekstkleur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Labels in dialoogvensters kunnen worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - als u alle labels wilt instellen op grijs, vet en met een lettertype van negen pixels:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

De controles van de input worden verpakt in de container en met de volgende CSS klassenselecteur bestuurd:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer
```

**CSS-eigenschappen van de invoercontainer van het dialoogvenster**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen-links  </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - om een opvulling van 30 pixels in te stellen vanaf de linkerrand van het dialoogvenster.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer { 
    padding-left: 30px; 
}
```

Keuzerondjes en de bijschrifttekst worden bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption
```

**CSS-eigenschappen van de optie van het dialoogvenster**

<table id="table_3B4D85C5A0254A17A34D57F84F8200F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> De totale breedte van het keuzerondje met een bijschrift. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur  </span> </p> </td> 
   <td colname="col2"> <p>Kleur van bijschrifttekst. </p> </td> 
  </tr> 
 </tbody> 
</table>

De afstand tussen het keuzerondje en het bijschrift wordt geregeld met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoptioninput
```

**CSS-eigenschappen van de invoer van opties in het dialoogvenster**

<table id="table_BDD03247E594416D93CDF8604DCE937B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge-rechts  </span> </p> </td> 
   <td colname="col2"> <p> Tussenruimte tussen het keuzerondje en het bijschrift. </p> </td> 
  </tr> 
 </tbody> 
</table>

Numerieke kiezers voor het selecteren van het afdrukbereik worden beheerd met de volgende CSS-klassenkiezer

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange
```

**CSS-eigenschappen van het dialoogvenster: afdrukbereik**

<table id="table_35413C16F6B840EBBEEA17890F2A0490"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Breedte van de numerieke kiezer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge  </span> </p> </td> 
   <td colname="col2"> <p> De ruimte rondom de numerieke kiezer. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u alle keuzerondjes wilt instellen op 150 pixels breed met zwarte tekst, een tussenruimte van tien pixels en een numerieke kiezer van 42 pixels breed:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption { 
    color: #000000; 
    width: 150px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption input { 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange { 
    margin-left: 10px; 
    margin-right: 10px; 
    width: 42px; 
}
```

De horizontale scheidingslijn tussen de selectie van het paginabereik en de gedeelten van de afdruklay-out wordt geregeld met de volgende CSS-klassenkiezer:

```
 .s7ecatalogsearchviewer 
.s7printdialog .s7horizontaldivider
```

**CSS-eigenschappen van de horizontale scheidingslijn**

<table id="table_AB42F1DC92BB4946868F0A9FE86ABAA6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p> Rand rond scheidingslijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen  </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Scheidingsbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge  </span> </p> </td> 
   <td colname="col2"> <p>Buitenmarge </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - voor het instellen van een grijze scheidingslijn van 430 pixels breed met een verticale opvulling van 10 pixels aan beide zijden en een marge van 10 pixels aan de bovenkant:

```
.s7ecatalogsearchviewer .s7printdialog .s7horizontaldivider { 
    border-top: 1px solid #aaaaaa; 
    margin-top: 10px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 430px; 
}
```


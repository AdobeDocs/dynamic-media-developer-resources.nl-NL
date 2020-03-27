---
description: Het gereedschap E-mail delen bestaat uit een knop die wordt toegevoegd aan het deelvenster Sociaal delen en het modale dialoogvenster dat wordt weergegeven wanneer het gereedschap wordt geactiveerd. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.
seo-description: Het gereedschap E-mail delen bestaat uit een knop die wordt toegevoegd aan het deelvenster Sociaal delen en het modale dialoogvenster dat wordt weergegeven wanneer het gereedschap wordt geactiveerd. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.
seo-title: E-mailshare
solution: Experience Manager
title: E-mailshare
topic: Dynamic media
uuid: fc60dd7b-651e-458c-9057-693ca1c0afdc
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# E-mailshare{#email-share}

Het gereedschap E-mail delen bestaat uit een knop die wordt toegevoegd aan het deelvenster Sociaal delen en het modale dialoogvenster dat wordt weergegeven wanneer het gereedschap wordt geactiveerd. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De vormgeving van de knop E-mail delen wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emailshare
```

**CSS-eigenschappen van het gereedschap voor het delen van e-mail**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de knop. </p> </td> 
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

Het is mogelijk om de knop uit het deelvenster Sociaal delen te verwijderen door de `display:none` CSS-eigenschap in te stellen op de CSS-klasse.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - om een knop voor e-maildelen in te stellen van 28 x 28 pixels en die een andere afbeelding weergeeft voor elk van de vier verschillende knopstatussen.

```
.s7ecatalogsearchviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

De achtergrondoverlay die de webpagina bedekt wanneer het dialoogvenster actief is, wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7backoverlay
```

**CSS-eigenschappen van de backoverlay**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dekking </span> </p> </td> 
   <td colname="col2"> <p> Dekking van achtergrondbedekking. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Kleur van achtergrondbedekking. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u een achtergrondbedekking wilt instellen die grijs is met een dekking van 70%:

```
.s7ecatalogsearchviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Standaard wordt het modale dialoogvenster gecentreerd weergegeven op het scherm op desktopsystemen en wordt het hele webpaginagebied op aanraakapparaten weergegeven. In alle gevallen, wordt het plaatsen en het rangschikken van de dialoogdoos beheerd door de component. Het dialoogvenster wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialog
```

**CSS-eigenschappen van het dialoogvenster**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Straal van de rand van het dialoogvenster (als het dialoogvenster niet het volledige browservenster neemt); </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur van dialoogvenster; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> De instelling moet ongedaan worden gemaakt of op 100% worden ingesteld. In dat geval wordt in het dialoogvenster het hele browservenster weergegeven (deze modus heeft de voorkeur op aanraakapparaten). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> De instelling moet ongedaan worden gemaakt of op 100% worden ingesteld. In dat geval wordt in het dialoogvenster het hele browservenster weergegeven (deze modus heeft de voorkeur op aanraakapparaten). </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u een dialoogvenster wilt instellen waarin het volledige browservenster wordt gebruikt en dat een witte achtergrond heeft op aanraakapparaten:

```
.s7ecatalogsearchviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

De koptekst van het dialoogvenster bestaat uit een pictogram, een titeltekst en een sluitknop. De koptekstcontainer wordt bestuurd met de volgende CSS-klassenkiezer

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader
```

**CSS-eigenschappen van de koptekst van het dialoogvenster**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p> Opvulling binnen voor koptekstinhoud. </p> </td> 
  </tr> 
 </tbody> 
</table>

Het pictogram en de titeltekst worden verpakt in een extra container die wordt bestuurd met

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader .s7dialogline
```

**CSS-eigenschappen van de dialoogregel**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p> Opvulling binnen voor het koptekstpictogram en de titel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Koptekstpictogram wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadericon
```

**CSS-eigenschappen van het pictogram van de koptekst in het dialoogvenster**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Pictogrambreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte pictogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p>Pictogramafbeelding. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

De titel van de koptekst wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadertext
```

**CSS-eigenschappen van de koptekst van het dialoogvenster**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Fontgewicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Hoogte lettertype. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Lettertypefamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Opvulling van interne tekst. </p> </td> 
  </tr> 
 </tbody> 
</table>

Knop Sluiten wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton
```

**CSS-eigenschappen van de knop close **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Verticale knoppositie ten opzichte van koptekstcontainer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p> Horizontale knoppositie ten opzichte van koptekstcontainer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knopbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p>Knopafbeelding voor elk frame. </p> </td> 
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

De knopinfo Sluiten en de titel van het dialoogvenster kunnen worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - om een dialoogkoptekst in te stellen met opvulling, pictogram van 24 x 17 pixels, een vette 16-punts titel en een knop Sluiten van 28 x 28 pixels die zich twee pixels van de bovenkant en twee pixels van de rechterkant van de container van het dialoogvenster bevinden:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Dialoogvoettekst bestaat uit de knoppen Annuleren en E-mail verzenden. De voettekstcontainer wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter
```

**CSS-eigenschappen van de voettekst van het dialoogvenster **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> Rand die u kunt gebruiken om de voettekst visueel te scheiden van de rest van het dialoogvenster. </p> </td> 
  </tr> 
 </tbody> 
</table>

De voettekst heeft een binnencontainer die beide knoppen bevat. De klasse wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbuttoncontainer
```

**CSS-eigenschappen van de knopcontainer van het dialoogvenster**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p> Opvulling binnen tussen de voettekst en de knoppen. </p> </td> 
  </tr> 
 </tbody> 
</table>

De knop Annuleren wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton
```

**CSS-eigenschappen van de knop cancel van het dialoogvenster**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knopbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur </span> </p> </td> 
   <td colname="col2"> <p> De tekstkleur van de knoop voor elke staat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur van knop voor elk frame. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden.

De knop E-mail verzenden wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton
```

**CSS-eigenschappen van de actieknop van het dialoogvenster**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knopbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur </span> </p> </td> 
   <td colname="col2"> <p> De tekstkleur van de knoop voor elke staat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur van knop voor elk frame. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden.

Bovendien hebben beide knoppen dezelfde algemene CSS-klasse die CSS-instellingen kan bevatten die hetzelfde zijn voor andere knoppen in dialoogvensters:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter .s7button
```

**CSS-eigenschappen van de knop**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Dikte van lettertype knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Lettertypefamilie knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> regelhoogte </span> </p> </td> 
   <td colname="col2"> <p> Teksthoogte in de knop. Heeft invloed op de verticale uitlijning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p>Slagschaduw. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge-rechts </span> </p> </td> 
   <td colname="col2"> <p>Marge rechterknop. </p> </td> 
  </tr> 
 </tbody> 
</table>

U kunt de knopinfo voor deze knoppen lokaliseren. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - voor het instellen van een voettekst in het dialoogvenster met een knop Annuleren van 64 x 34 en een knop voor het verzenden van e-mail van 82 x 34, met een andere tekstkleur en achtergrondkleur voor elke knopstatus:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

Het hoofddialoogvenster (tussen de kop- en voettekst) bevat schuifbare inhoud in het dialoogvenster en het schuifvenster aan de rechterkant. In alle gevallen beheert de component de breedte van dit gebied. Het is niet mogelijk om dit in CSS in te stellen. Het hoofddialoogvenster wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogviewarea
```

**CSS-eigenschappen van het weergavegebied van het dialoogvenster **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> De hoogte van het gebied van het hoofddialoogvenster. Deze mag alleen worden opgegeven wanneer het dialoogvenster in de bureaubladmodus werkt. Deze optie is niet van toepassing wanneer de grootte van het dialoogvenster zodanig is dat het volledige browservenster wordt ingenomen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>De achtergrondkleur van het gebied van het hoofddialoogvenster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p>Buitenmarge. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Het gebied van het hoofddialoogvenster ondersteunt de optionele `state` kenmerkkiezer. De instelling is ingesteld op `sendsuccess` wanneer het e-mailformulier wordt verzonden en in het dialoogvenster een bevestigingsbericht wordt weergegeven. Zolang het bevestigingsbericht klein is, kan deze kenmerkenkiezer worden gebruikt om de hoogte van het dialoogvenster te verminderen wanneer een dergelijk bevestigingsbericht wordt weergegeven.

Voorbeeld: als u het hoofddialoogvenster wilt instellen op een hoogte van 300 pixels in eerste instantie en een hoogte van 100 pixels in het bevestigingsbericht, hebt u een marge van 10 pixels en gebruikt u een witte achtergrond:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

Alle formulierinhoud (zoals labels en invoervelden) bevindt zich in een container die wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody
```

Als de hoogte van deze container groter lijkt te zijn dan het gebied van het hoofddialoogvenster, wordt automatisch een verticaal schuiven ingeschakeld door de component.

**CSS-eigenschappen van de hoofdtekst van het dialoogvenster **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u formulierinhoud wilt instellen met tien pixelopvulling:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody { 
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
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
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

Alle statische labels in het dialoogvenster worden beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoglabel
```

Deze klasse is niet geschikt voor het beheren van de grootte of positie van labels, omdat u deze kunt toepassen op tekst in verschillende locaties van de gebruikersinterface van het formulier.

**CSS-eigenschappen van het label van het dialoogvenster. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Breedte van lettertype label. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte label. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Lettertypefamilie label. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur </span> </p> </td> 
   <td colname="col2"> <p>Labeltekstkleur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Labels in dialoogvensters kunnen worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - als u alle labels wilt instellen op grijs, vet en met een lettertype van negen pixels:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Alle statische labels die links van de formulierinvoervelden worden weergegeven, worden beheerd met:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputlabel
```

**CSS-eigenschappen van het invoerlabel van het dialoogvenster**

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>De breedte van het statische label. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>De horizontale tekstuitlijning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p>Statische labelmarge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Statische opvulling van label. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u invoerveldlabels wilt instellen op een breedte van 50 pixels, rechts uitgelijnd, hebt u tien pixels opvulling en een marge van tien pixels rechts:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

Elk formulierinvoerveld wordt in de container geplaatst, zodat u een aangepaste rand rond het invoerveld kunt toepassen. De klasse wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputcontainer
```

**CSS-eigenschappen van de invoercontainer van het dialoogvenster**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Rand rondom de container van het invoerveld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Invoerveldcontainer ondersteunt optionele `state` kenmerkkiezer. Deze wordt ingesteld op `verifyerror` wanneer de gebruiker een fout maakt in de indeling van de invoergegevens en inlinevalidatie mislukt. Deze kenmerkenkiezer kan worden gebruikt om onjuiste gebruikersinvoer in het formulier te markeren.

De meeste invoervelden die zich uitstrekken van het label links tot aan de rechterrand van de hoofdtekst van het dialoogvenster (waaronder het veld Van en het veld Bericht), worden bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputwide
```

**CSS-eigenschappen van het invoerbrede veld van het dialoogvenster**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van invoerveld. </p> </td> 
  </tr> 
 </tbody> 
</table>

Het veld Aan is smaller omdat er ruimte wordt toegewezen voor de knop E-mail verwijderen aan de rechterkant. De klasse wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputshort
```

**CSS-eigenschappen van het korte veld voor invoer in het dialoogvenster**

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van invoerveld. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - een formulier zo instellen dat het een grijze rand van één pixel heeft met negen pixels opvulling rond alle invoervelden. dezelfde rode rand hebben voor velden waarvoor de validatie niet is gelukt, een breedte van 250 pixels hebben in het veld Aan en de rest van de invoervelden een breedte van 300 pixels:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

Het invoerveld voor e-mailberichten wordt aangevuld met:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogmessage
```

Met deze klasse kunt u specifieke eigenschappen instellen voor het onderliggende `TEXTAREA` element.

**CSS-eigenschappen van het bericht in het dialoogvenster**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Berichthoogte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekstomloop </span> </p> </td> 
   <td colname="col2"> <p>Tekstomloopstijl. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u een e-mailbericht wilt instellen op 50 pixels hoog en tekstomloop wilt gebruiken: `break-word`

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

Met de knop Een ander e-mailadres toevoegen kan een gebruiker meer dan één adres toevoegen in een e-mailformulier. De klasse wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton
```

**CSS-eigenschappen van het dialoogvenster toevoegen, knop E-mailadres**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur </span> </p> </td> 
   <td colname="col2"> <p>De tekstkleur van de knoop voor elke staat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p>Knopafbeelding voor elk frame. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>De afbeeldingspositie van de knop binnen het knopgebied. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Dikte van lettertype knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Lettertypefamilie knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> regelhoogte </span> </p> </td> 
   <td colname="col2"> <p>Teksthoogte in de knop. Heeft invloed op de verticale uitlijning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Horizontale tekstuitlijning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld: als u de knop Een ander e-mailadres toevoegen wilt instellen op 25 pixels hoog, gebruikt u 12-punts vet lettertype met de juiste uitlijning en een andere tekstkleur en afbeelding voor elke status:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

Met de knop Verwijderen kan een gebruiker extra adressen uit het e-mailformulier verwijderen. De klasse wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton
```

**CSS-eigenschappen van het dialoogvenster verwijderen de knop E-mail**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knopbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p>Knopafbeelding voor elk frame. </p> </td> 
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

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - als u een verwijderknop wilt instellen op 25 x 25 pixels en voor elke status een andere afbeelding wilt gebruiken:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

De inhoud die wordt gedeeld, wordt onder in de hoofdtekst van het dialoogvenster weergegeven en bevat een miniatuur, titel, oorsprong-URL en beschrijving. De container wordt verpakt in een container die wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

**CSS-eigenschappen van de inhoud van het dialoogvenster **

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Containerrand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u een container onder wilt instellen met een gestippelde rand van één pixel en geen opvulling:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

De miniatuurafbeelding wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogthumbnail
```

De `background-image` eigenschap wordt ingesteld door de componentlogica.

**CSS-eigenschappen van de miniatuurafbeelding van het dialoogvenster**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte miniatuur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte miniatuur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align </span> </p> </td> 
   <td colname="col2"> <p>Miniatuur van verticale uitlijning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u een miniatuur wilt instellen op 90 x 60 pixels en de miniatuur aan de bovenzijde uitgelijnd met tien pixels opvulling:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

De titel, oorsprong en beschrijving van de inhoud worden verder gegroepeerd in een deelvenster rechts van de miniatuur van de inhoud. De klasse wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginfopanel
```

**CSS-eigenschappen van het informatievenster van het dialoogvenster**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte deelvenster. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld: als u een deelvenster met inhoudsgegevens wilt instellen op een breedte van 300 pixels:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

De titel van de inhoud wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogtitle
```

**CSS-eigenschappen van de titel van het dialoogvenster**

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p>Buitenmarge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Fontgewicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Lettertypefamilie. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u een titel voor inhoud wilt instellen voor het gebruik van een vet lettertype met een marge van 10 pixels:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

De oorsprong van de inhoud wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogorigin
```

**CSS-eigenschappen van oorsprong van inhoud in het dialoogvenster **

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p>Buitenmarge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Fontgewicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Lettertypefamilie. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u de oorsprong van de inhoud wilt instellen op een marge van 10 pixels:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

De beschrijving van de inhoud wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogdescription
```

**CSS-eigenschappen van de inhoudsbeschrijving van het dialoogvenster**

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p>Buitenmarge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Fontgewicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Lettertypefamilie. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u een inhoudsbeschrijving wilt instellen met een marge van 10 pixels en een 9-punts lettertype wilt gebruiken:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

Wanneer een gebruiker onjuiste invoergegevens invoert en inlinevalidering mislukt, of wanneer in het dialoogvenster een fout of een bevestigingsbericht moet worden weergegeven wanneer het formulier wordt verzonden, wordt een bericht weergegeven boven in de hoofdtekst van het dialoogvenster. De klasse wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage
```

**CSS-eigenschappen van het foutbericht van het dialoogvenster**

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p> Foutpictogram. Standaard is een uitroepteken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Foutpictogrampositie binnen het berichtgebied. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur </span> </p> </td> 
   <td colname="col2"> <p>Tekstkleur van bericht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Fontgewicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Lettertypefamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> regelhoogte </span> </p> </td> 
   <td colname="col2"> <p> Teksthoogte in het bericht. Heeft invloed op de verticale uitlijning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Dit bericht ondersteunt de `state` kenmerkenkiezer met de volgende mogelijke waarden: `verifyerror`, `senderror`, en `sendsuccess`. `verifyerror` wordt ingesteld wanneer een bericht wordt weergegeven als gevolg van een inline-invoervalidatiefout; wordt ingesteld wanneer een e-mailservice op de achtergrond een fout meldt; `senderror` `sendsuccess` wordt ingesteld wanneer e-mail is verzonden. Op deze manier kunt u het bericht anders opmaken afhankelijk van de status van het dialoogvenster.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - als u een bericht wilt instellen dat een lettertype van tien punten vet wordt gebruikt, dat een lijnhoogte van 25 pixels, een opvulling van 20 pixels aan de linkerkant en een uitroeptekenpictogram moeten worden gebruikt, dat rood moet worden als er een fout optreedt en dat er geen pictogram en groene tekst mogen worden weergegeven als de bewerking slaagt:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

Als verticaal schuiven nodig is, wordt de schuifbalk weergegeven in het deelvenster aan de rechterrand van het dialoogvenster, dat wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogscrollpanel
```

**CSS-eigenschappen van het schuifvenster van het dialoogvenster**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van deelvenster Schuiven. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld: als u een schuifvenster wilt instellen op een breedte van 44 pixels:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

De vormgeving van het gebied van de schuifbalk wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar
```

**CSS-eigenschappen van de schuifbalk**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> De breedte van de schuifbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> De verticale verschuiving van de schuifbalk vanaf de bovenkant van het schuifvenster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p> De verticale verschuiving van de schuifbalk vanaf de onderkant van het schuifvenster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p> De verschuiving van de horizontale schuifbalk ten opzichte van de rechterrand van het schuifvenster. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - als u een schuifbalk wilt instellen die 28 pixels breed is, een marge van 8 pixels vanaf de bovenkant, de rechterkant en de onderkant van het schuifvenster:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

Schuifbalktrack is het gebied tussen de bovenste en onderste schuifknop. De component stelt automatisch de positie en de hoogte van het spoor in. De track wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

**CSS-eigenschappen van de schuiftrack**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
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

Voorbeeld - voor het instellen van een schuifbalkvak met een breedte van 28 pixels en een grijze achtergrond:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

De schuifbalkduim beweegt verticaal binnen een schuiftrackgebied. De verticale positie wordt volledig bepaald door de componentlogica, maar de hoogte van het blokje verandert niet dynamisch afhankelijk van de hoeveelheid inhoud. U kunt de duimhoogte en andere aspecten met de volgende CSS klassenselecteur vormen:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

**CSS-eigenschappen van het blokje van de schuifbalk**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
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
   <td colname="col2"> <p> De verticale opvulling tussen de onderkant van de track. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p>De afbeelding die voor een bepaalde duimstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De duim steunt de `state` attributenselecteur, die kan worden gebruikt om verschillende huiden op verschillende duimstaten toe te passen: `up`, `down`, `over`en `disabled`.

Voorbeeld: als u een schuifbalkblokje van 28 x 45 pixels wilt instellen, hebt u een marge van 10 pixels boven en onder aan de schuifbalk en hebt u voor elke staat een andere illustratie:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

De vormgeving van de bovenste en onderste schuifknoppen wordt bepaald door de volgende CSS-klassekiezers:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton
```

Het is niet mogelijk om rolknopen te plaatsen gebruikend CSS `top`, `left`, `bottom`, en `right` eigenschappen. In plaats daarvan worden ze automatisch door de viewerlogica geplaatst.

**CSS-eigenschappen van de schuifknoppen boven en onder**

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
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
   <td colname="col2"> <p>De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoppen ondersteunen de `state` kenmerkkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden: `up`, `down`, `over`en `disabled`.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - voor het instellen van schuifknoppen met een resolutie van 28 x 32 pixels en voor elke status een andere illustratie:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```


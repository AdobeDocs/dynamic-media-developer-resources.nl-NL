---
description: Het gereedschap voor delen van koppeling bestaat uit een knop die wordt toegevoegd aan het deelvenster Sociaal delen en het modale dialoogvenster dat wordt weergegeven wanneer het gereedschap wordt geactiveerd. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.
seo-description: Het gereedschap voor delen van koppeling bestaat uit een knop die wordt toegevoegd aan het deelvenster Sociaal delen en het modale dialoogvenster dat wordt weergegeven wanneer het gereedschap wordt geactiveerd. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.
seo-title: Delen van koppeling
solution: Experience Manager
title: Delen van koppeling
topic: Dynamic media
uuid: c98cb3bd-0e94-46ef-8875-662925d3c067
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Delen van koppeling{#link-share}

Het gereedschap voor delen van koppeling bestaat uit een knop die wordt toegevoegd aan het deelvenster Sociaal delen en het modale dialoogvenster dat wordt weergegeven wanneer het gereedschap wordt geactiveerd. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

De weergave van de knop voor het delen van koppelingen wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7linkshare
```

**CSS-eigenschappen van het gereedschap voor delen van koppelingen**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
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
   <td colname="col2"> <p> De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden.

Het is mogelijk om de knop uit het deelvenster Sociaal delen te verwijderen door de `display:none` CSS-eigenschap in te stellen op de CSS-klasse.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Voorbeeld - om een knop voor het delen van koppelingen in te stellen met een grootte van 28 x 28 pixels en een andere afbeelding weer te geven voor elk van de vier verschillende knopstatussen:

```
.s7video360viewer .s7linkshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7linkshare[state='up'] { 
background-image:url(images/v2/LinkShare_dark_up.png); 
} 
.s7video360viewer .s7linkshare[state='over'] { 
background-image:url(images/v2/LinkShare_dark_over.png); 
} 
.s7video360viewer .s7linkshare[state='down'] { 
background-image:url(images/v2/LinkShare_dark_down.png); 
} 
.s7video360viewer .s7linkshare[state='disabled'] { 
background-image:url(images/v2/LinkShare_dark_disabled.png); 
}
```

De achtergrondoverlay die de webpagina bedekt wanneer het dialoogvenster actief is, wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7linkdialog .s7backoverlay
```

**CSS-eigenschappen van de achtergrondoverlay**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dekking </span> </p> </td> 
   <td colname="col2"> <p>Dekking van achtergrondbedekking. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Kleur van achtergrondbedekking. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - een achtergrondbedekking instellen die grijs is met een dekking van 70%:

```
.s7video360viewer .s7linkdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Standaard wordt het modale dialoogvenster gecentreerd weergegeven op het scherm op desktopsystemen en neemt het volledige webpaginagebied op aanraakapparaten in beslag. In alle gevallen, wordt het plaatsen en het rangschikken van de dialoogdoos beheerd door de component. Het dialoogvenster wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7linkdialog .s7dialog
```

**CSS-eigenschappen van het dialoogvenster**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> De randstraal van het dialoogvenster voor het geval dat het dialoogvenster niet de volledige browser neemt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Achtergrondkleur van dialoogvenster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>De instelling moet ongedaan worden gemaakt of op 100% worden ingesteld. In dat geval gebruikt het dialoogvenster het volledige browservenster (deze modus heeft de voorkeur op aanraakapparaten). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>De instelling moet ongedaan worden gemaakt of op 100% worden ingesteld. In dat geval gebruikt het dialoogvenster het volledige browservenster (deze modus heeft de voorkeur op aanraakapparaten). </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - als u het dialoogvenster zo wilt instellen dat het volledige browservenster wordt gebruikt en een witte achtergrond op aanraakapparaten heeft:

```
.s7video360viewer.s7touchinput .s7linkdialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

De koptekst van het dialoogvenster bestaat uit een pictogram, een titeltekst en een sluitknop. De koptekstcontainer wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7linkdialog .s7dialogheader
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

Het pictogram en de titeltekst zijn ondergebracht in een extra container die wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7linkdialog .s7dialogheader .s7dialogline
```

**CSS-eigenschappen van de dialoogregel**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p> Opvulling binnen voor het koptekstpictogram en de titel </p> </td> 
  </tr> 
 </tbody> 
</table>

Koptekstpictogram wordt bestuurd met de volgende CSS-klassenkiezer

```
.s7video360viewer .s7linkdialog .s7dialogheadericon
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
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

De titel van de koptekst wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7linkdialog .s7dialogheadertext
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
.s7video360viewer .s7linkdialog .s7closebutton
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
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden.

De knopinfo Sluiten en de titel van het dialoogvenster kunnen worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Voorbeeld** - om een dialoogvensterkoptekst in te stellen met opvulling, pictogram van 22 x 12 pixels, vetgedrukte titel van 16 punten en een knop Sluiten van 28 x 28 pixels die twee pixels van de bovenkant en twee pixels van de rechterkant van de container van het dialoogvenster zijn geplaatst:

```
.s7video360viewer .s7linkdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlglink_cap.png"); 
    height: 12px; 
    width: 22px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7video360viewer .s7linkdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

De voettekst van het dialoogvenster bestaat uit een knop Annuleren. De voettekstcontainer wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7linkdialog .s7dialogfooter
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

De voettekst heeft een binnencontainer die de knop houdt. De klasse wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7linkdialog .s7dialogbuttoncontainer
```

**CSS-eigenschappen van de knopcontainer van het dialoogvenster**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p> Opvulling binnen tussen de voettekst en de knop. </p> </td> 
  </tr> 
 </tbody> 
</table>

De knop Alles selecteren wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7linkdialog .s7dialogactionbutton
```

De knop is alleen beschikbaar op desktopsystemen.

**CSS-eigenschappen van de knop Alles selecteren**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
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
>De knop Alles selecteren ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden.

De knop Annuleren wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7linkdialog .s7dialogcancelbutton
```

**CSS-eigenschappen van het dialoogvenster Annuleren**

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

Bovendien hebben beide knoppen dezelfde algemene CSS-klasse die CSS-instellingen kan bevatten die hetzelfde zijn voor andere knoppen in dialoogvensters:

```
.s7video360viewer .s7linkdialog .s7dialogfooter .s7button
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

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Voorbeeld** - om een dialoogvakje footer met een knoop van 64 x 34 te plaatsen annuleert, met tekstkleur en achtergrondkleuren die voor elke knoopstaat verschillend zijn:

```
.s7video360viewer .s7linkdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7video360viewer .s7linkdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

Het hoofddialoogvenster (tussen de kop- en voettekst) bevat inhoud van het dialoogvenster. In alle gevallen beheert de component de breedte van dit gebied. Het is niet mogelijk dit in te stellen in CSS. Het hoofddialoogvenster wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7linkdialog .s7dialogviewarea
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

**Voorbeeld** - als u een gebied in het hoofddialoogvenster wilt instellen op een hoogte van 300 pixels, een marge van 10 pixels en een witte achtergrond wilt gebruiken:

```
.s7video360viewer .s7linkdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Alle formulierinhoud, zoals labels en invoervelden, bevindt zich in een container die wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7linkdialog .s7dialogbody
```

**CSS-eigenschappen van de hoofdtekst van het dialoogvenster **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - instellen dat formulierinhoud 10 pixels wordt opgevuld:

```
.s7interactivevideoviewer .s7linkdialog .s7dialogbody { 
    padding: 10px; 
}
```

Alle statische labels in het dialoogvenster worden beheerd met

```
.s7video360viewer .s7linkdialog .s7dialoglabel
```

Deze klasse is niet geschikt voor het bepalen van de grootte of positie van het label, omdat u deze kunt toepassen op tekst in verschillende locaties van de gebruikersinterface van het formulier.

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

De dialoogvensterlabels kunnen worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Voorbeeld** - als u alle labels wilt instellen op grijs, vet met een lettertype van negen pixels:

```
.s7video360viewer .s7linkdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

De grootte van de tekstkopie die boven op de koppeling wordt weergegeven, wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7linkdialog .s7dialoginputwide
```

**CSS-eigenschappen van het invoerbrede veld van het dialoogvenster**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Tekstbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - als u de tekstkopie wilt instellen op 430 pixels breed en onderaan een opvulling van 10 pixels bevat:

```
.s7video360viewer .s7linkdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

De koppeling voor delen is ondergebracht in een container en wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7linkdialog .s7dialoginputcontainer
```

**CSS-eigenschappen van de invoercontainer van het dialoogvenster**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Rand rond de container voor de gedeelde koppeling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - als u een grijze rand van één pixel wilt instellen rondom de ingesloten codetekst en een opvulling van negen pixels wilt instellen:

```
.s7video360viewer .s7linkdialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
}
```

De koppeling voor delen zelf wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7linkdialog .s7dialoglink
```

**CSS-eigenschappen van het dialoogvenster delen koppeling**

<table id="table_65CF778F5BDA45118208538DCBE203FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Koppelingsbreedte delen. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - als u de koppeling voor delen wilt instellen op 450 pixels breed:

```
.s7video360viewer .s7linkdialog .s7dialoglink { 
    width: 450px; 
}
```


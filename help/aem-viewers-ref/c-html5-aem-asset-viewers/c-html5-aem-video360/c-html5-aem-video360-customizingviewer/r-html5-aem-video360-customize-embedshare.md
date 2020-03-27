---
description: Het gereedschap Delen insluiten bestaat uit een knop die wordt toegevoegd aan het deelvenster Delen via sociale media en het modale dialoogvenster dat wordt weergegeven wanneer het gereedschap wordt geactiveerd. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.
seo-description: Het gereedschap Delen insluiten bestaat uit een knop die wordt toegevoegd aan het deelvenster Delen via sociale media en het modale dialoogvenster dat wordt weergegeven wanneer het gereedschap wordt geactiveerd. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.
seo-title: Delen insluiten
solution: Experience Manager
title: Delen insluiten
topic: Dynamic media
uuid: 768e8eb5-ec35-4028-be96-268f8220fe07
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Delen insluiten{#embed-share}

Het gereedschap Delen insluiten bestaat uit een knop die wordt toegevoegd aan het deelvenster Delen via sociale media en het modale dialoogvenster dat wordt weergegeven wanneer het gereedschap wordt geactiveerd. De positie van de knop wordt volledig beheerd met het gereedschap Sociaal delen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De vormgeving van de knop Delen insluiten wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embedshare
```

**CSS-eigenschappen van het gereedschap Delen insluiten**

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
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden.

Het is mogelijk om de knop uit het deelvenster Sociaal delen te verwijderen door de `display:none` CSS-eigenschap in te stellen op de CSS-klasse.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) voor meer informatie.

**Voorbeeld** - om een insluitingsdeelknop van 28 x 28 pixels in te stellen en een andere afbeelding voor elk van de vier verschillende knopstatussen weer te geven:

```
.s7video360viewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7video360viewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7video360viewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7video360viewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

De achtergrondoverlay die de webpagina bedekt wanneer het dialoogvenster actief is, wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7backoverlay
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
.s7video360viewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Standaard wordt het modale dialoogvenster gecentreerd weergegeven op het scherm op desktopsystemen en neemt het volledige webpaginagebied op aanraakapparaten in beslag. In alle gevallen, wordt het plaatsen en het rangschikken van de dialoogdoos beheerd door de component. Het dialoogvenster wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7dialog
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
.s7video360viewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

De koptekst van het dialoogvenster bestaat uit een pictogram, een titeltekst en een sluitknop. De koptekstcontainer wordt bestuurd met

```
.s7video360viewer .s7embeddialog .s7dialogheader
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

Het pictogram en de titeltekst worden verpakt in een extra container die met het volgende wordt bestuurd:

```
.s7video360viewer .s7embeddialog .s7dialogheader .s7dialogline
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

Koptekstpictogram wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7dialogheadericon
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
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

De titel van de koptekst wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7dialogheadertext
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
.s7video360viewer .s7embeddialog .s7closebutton
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
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) voor meer informatie.

**Voorbeeld** - om een dialoogkoptekst in te stellen met opvulling, pictogram van 24 x 14 pixels, vetgedrukte titel van 16 punten en knop Sluiten van 28 x 28 pixels, op twee pixels van de bovenkant en op twee pixels van de rechterkant van de dialoogcontainer:

```
.s7video360viewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7video360viewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7video360viewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7video360viewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7video360viewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7video360viewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7video360viewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7video360viewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Dialoogvoettekst bestaat uit de knop Annuleren. De voettekstcontainer wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7dialogfooter
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

De voettekst heeft een binnencontainer waarmee de knop behouden blijft. De klasse wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7dialogbuttoncontainer
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

Selecteer Alle knoop wordt gecontroleerd met de volgende CSS klassenselecteur:

```
.s7video360viewer .s7embeddialog .s7dialogactionbutton
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
.s7video360viewer .s7embeddialog .s7dialogcancelbutton
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

Bovendien hebben beide knoppen dezelfde algemene CSS-klasse die CSS-instellingen kan bevatten die hetzelfde zijn voor andere knoppen in dialoogvensters:

```
.s7video360viewer .s7embeddialog .s7dialogfooter .s7button
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

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) voor meer informatie.

**Voorbeeld** - om een dialoogvakje footer met een knoop van 64 x 34 te plaatsen annuleert, met een tekstkleur en een achtergrondkleur die voor elke knoopstaat verschillend is:

```
.s7video360viewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7video360viewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7video360viewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
```

Het hoofddialoogvenster (tussen de kop- en voettekst) bevat schuifbare inhoud in het dialoogvenster en het schuifvenster aan de rechterkant. In alle gevallen beheert de component de breedte van dit gebied. Het is niet mogelijk om dit in CSS in te stellen. Het hoofddialoogvenster wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7dialogviewarea
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
.s7video360viewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Alle formulierinhoud (zoals labels en invoervelden) bevindt zich in een container die wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7dialogbody
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

**Voorbeeld** - instellen dat formulierinhoud tien pixels wordt opgevuld:

```
.s7video360viewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

Alle statische labels in het dialoogvenster worden beheerd met

```
.s7video360viewer .s7embeddialog .s7dialoglabel
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

Labels in dialoogvensters kunnen worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) voor meer informatie.

**Voorbeeld** - als u alle labels wilt instellen op grijs, vet met een lettertype van negen pixels:

```
.s7video360viewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

De grootte van de tekstkopie die boven op de insluitcode wordt weergegeven, wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7dialoginputwide
```

**CSS-eigenschappen van het invoerbrede veld van het dialoogvenster**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van invoerveld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - als u de tekstkopie wilt instellen op 430 pixels breed en onderaan een opvulling van 10 pixels bevat:

```
.s7video360viewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

De insluitcode wordt ondergebracht in container en bestuurd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7dialoginputcontainer
```

**CSS-eigenschappen van de invoercontainer van het dialoogvenster**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>De breedte van de container van de insluitcode. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Rand rond de insluitcodecontainer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** : als u een grijze rand van één pixel wilt instellen rondom de ingesloten codetekst, maakt u deze 430 pixels breed en hebt u een opvulling van tien pixels:

```
.s7video360viewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

De eigenlijke ingesloten codetekst wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7dialoginputcontainer
```

**CSS-eigenschappen van de invoercontainer van het dialoogvenster**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekstomloop </span> </p> </td> 
   <td colname="col2"> <p>Tekstomloopstijl. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - voor het instellen van insluitcode voor het gebruik van `break-word` tekstomloop:

```
.s7video360viewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

Label en vervolgkeuzelijst voor insluitgrootte bevinden zich onder in het dialoogvenster en worden in een container geplaatst die wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7dialogembedsizepanel
```

**CSS-eigenschappen van het dialoogvenster sluiten formaatvenster in**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Opvulling binnen. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** : als u een insluitvenster wilt instellen met tien pixels opvulling:

```
.s7video360viewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

De grootte en uitlijning van het label voor de insluitgrootte worden bepaald met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7dialogembedsizepanel
```

**CSS-eigenschappen van het dialoogvenster sluiten formaatvenster in**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align </span> </p> </td> 
   <td colname="col2"> <p>Verticale uitlijning van labels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Labelbreedte. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - om het insluitingsgroottelabel in te stellen op top-align en 80 pixels breed:

```
.s7video360viewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

De breedte van de keuzelijst met insluitgrootte wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7combobox
```

**CSS-eigenschappen van de keuzelijst met invoervak**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van keuzelijst met invoervak. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De keuzelijst met invoervak ondersteunt de `expanded` kenmerkkiezer met mogelijke waarden `true` en `false`. `true` wordt gebruikt wanneer in een keuzelijst met invoervak een van de vooraf gedefinieerde insluitgrootten wordt weergegeven. Dit betekent dat alle beschikbare breedte in beslag moet worden genomen. `false` wordt gebruikt wanneer de optie voor aangepaste grootte is geselecteerd in de keuzelijst met invoervak, zodat deze kleiner wordt zodat ruimte beschikbaar is voor invoervelden voor aangepaste breedte en hoogte.

**Voorbeeld** - om het invoervak Grootte insluiten in te stellen op 300 pixels breed bij het weergeven van een vooraf gedefinieerd item en op 110 pixels breed bij het weergeven van een aangepaste grootte:

```
.s7video360viewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7video360viewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

De hoogte van de tekst van de keuzelijst met invoervak wordt gedefinieerd door een speciaal binnenelement en wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxtext
```

**CSS-eigenschappen van de tekst van het invoervak**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Teksthoogte van keuzelijst met invoervak. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - als u de ingesloten grootte voor de teksthoogte in het invoervak wilt instellen op 40 pixels:

```
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

De keuzelijst met invoervak heeft rechts een vervolgkeuzelijst en wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**CSS-eigenschappen van de keuzelijst met invoervak**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Verticale knoppositie in de keuzelijst met invoervak. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Horizontale knoppositie binnen de keuzelijst met invoervak. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p>Knopafbeelding voor elk frame. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden.

**Voorbeeld** - om een drop-down knoop aan 28 x 28 pixel te plaatsen en een afzonderlijke beeld voor elke staat te hebben:

```
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

Het deelvenster met de lijst met insluitgrootten die wordt weergegeven wanneer de keuzelijst met invoervak wordt geopend, wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7comboboxdropdown
```

De grootte en positie van het deelvenster worden bepaald door de component. Het is niet mogelijk deze te wijzigen met CSS.

**CSS-eigenschappen van de keuzelijst met invoervak**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Rand van deelvenster. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - als u het deelvenster met invoervak wilt instellen op een grijze rand van één pixel:

```
.s7video360viewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

Eén item in een vervolgkeuzelijst dat wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7dropdownitemanchor
```

**CSS-eigenschappen van het vervolgkeuzepuntanker**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Achtergrond van item. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - als u de deelvensteritem van de keuzelijst met invoervak wilt instellen op een witte achtergrond:

```
.s7video360viewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

Een vinkje links van het geselecteerde item in het deelvenster met keuzelijst met invoervak dat wordt bestuurd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7checkmark
```

**CSS-eigenschappen van het selectievakje**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
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
   <td colname="col2"> <p>Afbeelding item. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - om het pictogram van het vinkje aan 25 x 25 pixel te plaatsen:

```
.s7video360viewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

Als de optie Aangepaste grootte is geselecteerd in de keuzelijst Grootte insluiten, worden rechts in het dialoogvenster twee extra invoervelden weergegeven waarmee de gebruiker een aangepaste insluitgrootte kan invoeren. Deze velden worden verpakt in een container die wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7dialogcustomsizepanel
```

**CSS-eigenschappen van het deelvenster Aangepaste grootte van het dialoogvenster**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p> Afstand tot het invoervak Grootte insluiten. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - als u het invoerveld voor aangepaste grootte wilt instellen op 20 pixels rechts van de keuzelijst met invoervak:

```
.s7video360viewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

Elk invoerveld met een aangepaste grootte wordt verpakt in een container die een rand rendert en de marge tussen de velden instelt. De klasse wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7dialogcustomsize
```

**CSS-eigenschappen van de aangepaste grootte van het dialoogvenster**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Rand rond het invoerveld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Breedte van invoerveld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge </span> </p> </td> 
   <td colname="col2"> <p> Invoerveldmarge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p> Opvulling invoerveld. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - als u wilt dat de invoervelden voor aangepaste grootten een grijze rand, marge, opvulling van één pixel hebben en een breedte van 70 pixels hebben:

```
.s7video360viewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

Als verticaal schuiven nodig is, wordt de schuifbalk weergegeven in het deelvenster aan de rechterrand van het dialoogvenster, dat wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7dialogscrollpanel
```

**CSS-eigenschappen van het schuifvenster van het dialoogvenster**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van deelvenster Schuiven. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** : een schuifvenster instellen op een breedte van 44 pixels

```
.s7video360viewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

De vormgeving van het gebied van de schuifbalk wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7video360viewer .s7embeddialog .s7scrollbar
```

**CSS-eigenschappen van de schuifbalk**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte schuifbalk. </p> </td> 
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

**Voorbeeld** : als u een schuifbalk wilt instellen die 28 pixels breed is en een marge van 8 pixels heeft vanaf de bovenkant, de rechterkant en de onderkant van het schuifvenster:

```
.s7video360viewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

Schuifbalktrack is het gebied tussen de bovenste en onderste schuifknop. De component stelt automatisch de positie en de hoogte van het spoor in. De track wordt bestuurd met de volgende CSS-klassenkiezer

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**CSS-eigenschappen van schuifbalktrack**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Trackbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur bijhouden. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld** - Een schuifbalkvak instellen met een breedte van 28 pixels en een grijze achtergrond:

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

Het schuifbalkblokje beweegt verticaal binnen een schuiftrackgebied. De verticale positie wordt volledig bepaald door de componentlogica. De hoogte van het blokje verandert echter niet dynamisch, afhankelijk van de hoeveelheid inhoud. De duimhoogte en andere aspecten kunnen met de volgende CSS klassenselecteur worden gevormd:

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**CSS-eigenschappen van het blokje van de schuifbalk**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte duim. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte duim. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen boven </span> </p> </td> 
   <td colname="col2"> <p>De verticale opvulling tussen de bovenkant van de track. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen-onder </span> </p> </td> 
   <td colname="col2"> <p> De verticale opvulling tussen de onderkant van de track. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p> De afbeelding die wordt weergegeven voor een bepaalde staat van het blokje. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De duim steunt de `state` attributenselecteur, die kan worden gebruikt om verschillende huiden op verschillende duimstaten toe te passen: `up`, `down`, `over`en `disabled`.

**Voorbeeld** : als u een schuifbalkblokje van 28 x 45 pixels wilt instellen, hebt u een marge van 10 pixels boven en onder en heeft u voor elke staat een andere illustratie:

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

De vormgeving van de bovenste en onderste schuifknoppen wordt bepaald door de volgende CSS-klassekiezers:

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton
```

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

Het is niet mogelijk om rolknopen te plaatsen gebruikend CSS `top`, `left`, `bottom`, en `right` eigenschappen. In plaats daarvan worden ze automatisch door de viewerlogica geplaatst.

**CSS-eigenschappen van de schuifknoppen boven en onder**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
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
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoppen ondersteunen de `state` kenmerkkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden: `up`, `down`, `over`en `disabled`.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) voor meer informatie.

**Voorbeeld** - om schuifknoppen in te stellen die 28 x 32 pixels lang zijn en voor elke status een andere illustratie hebben:

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```


---
description: De hoofdweergave bestaat uit de statische afbeelding, de ingezoomde afbeelding in de vervolgweergave, het hooglichtnavigatiegebied dat boven op de statische afbeelding wordt weergegeven en het uiteindebericht dat boven op de statische afbeelding wordt weergegeven.
seo-description: De hoofdweergave bestaat uit de statische afbeelding, de ingezoomde afbeelding in de vervolgweergave, het hooglichtnavigatiegebied dat boven op de statische afbeelding wordt weergegeven en het uiteindebericht dat boven op de statische afbeelding wordt weergegeven.
seo-title: Zoomweergave flyout
solution: Experience Manager
title: Zoomweergave flyout
topic: Dynamic media
uuid: 35c60228-3044-442b-a8e2-e13d0bd306a5
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zoomweergave flyout{#flyout-zoom-view}

De hoofdweergave bestaat uit de statische afbeelding, de ingezoomde afbeelding in de vervolgweergave, het hooglichtnavigatiegebied dat boven op de statische afbeelding wordt weergegeven en het uiteindebericht dat boven op de statische afbeelding wordt weergegeven.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Als de afmetingen van de afbeelding die wordt weergegeven niet overeenkomen met de afmetingen van de zoomweergave voor uitvouwen, wordt de afbeeldingsinhoud gecentreerd in het weergavegebied van de rechthoek van de zoomweergave.

**CSS-eigenschappen van de hoofdweergave**

De vormgeving van de hoofdweergave wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7flyoutviewer .s7flyoutzoomview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> De achtergrondkleur van de hoofdweergave. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - om de hoofdweergave transparant te maken:

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**CSS-eigenschappen van de vervolgweergave**

De weergave van de flyout-weergave wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom
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
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p> De horizontale positie van de uitvliegweergave ten opzichte van de linkerbovenhoek van de hoofdweergave. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> De verticale positie van de uitvliegweergave ten opzichte van de linkerbovenhoek van de hoofdweergave. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> De breedte van de vervolgweergave. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van de vervolgweergave. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>De rand van de uitvliegweergave. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - voor het instellen van een uitvliegweergave op 600 x 400 pixels, weergegeven met 100 pixels die rechts van de hoofdweergave van 512 x 288 staan, zoals getoond in het vorige voorbeeld:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**CSS-eigenschappen van de markering in de hoofdweergave**

De vormgeving van de markering in de hoofdweergave wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

Het is mogelijk om achtergrond-, rand-, transparantie- en vergelijkbare kenmerken te beheren met CSS. De grootte en positie van het DOM-element voor markeren wordt echter beheerd door de viewerlogica. Overschrijven via CSS wordt niet ondersteund.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> De kleur van de markering. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dekking </span> </p> </td> 
   <td colname="col2"> <p> Hooglichtdekking. </p> <p>Gebruik voor Internet Explorer 8 <span class="codeph"> filter:alpha(opacity-...)); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>De markering van de rand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld: groen markeren instellen met een transparantie van 40% en een rode rand van 1 pixel:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**CSS-eigenschappen van de cursor**

Wanneer de `highlightmode` parameter wordt geplaatst aan `cursor`, zijn de hoogtepunten in de belangrijkste mening vervangen met het vaste grootte curseurkunstwerk, dat met de CSS klassenselecteur wordt bestuurd:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

U kunt de achtergrondafbeelding en -grootte bepalen met CSS.

Toepasselijke CSS-eigenschappen zijn onder andere:

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding </span> </p> </td> 
   <td colname="col2"> <p>Cursorillustratie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Cursorbreedte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van cursor. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De cursor ondersteunt de `input` kenmerkenkiezer, die kan worden gebruikt om verschillende cursorillustraties en -grootte toe te passen op verschillende apparaten. Dit komt met name overeen met `input="mouse"` de desktopsystemen en `input="touch"` komt overeen met de aanraakapparaten.

**CSS-eigenschappen van de overlay**

Wanneer de `overlay` parameter wordt ingesteld op `1`, wordt het gebied rondom het markeringsframe of de cursorafbeelding beheerd met de CSS-klassenkiezer:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7overlay
```

<table id="table_A50CA8213C3A4682A081D3D30089574C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Bedekkingskleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dekking </span> </p> </td> 
   <td colname="col2"> <p>Dekking bedekking. </p> </td> 
  </tr> 
 </tbody> 
</table>

**CSS-eigenschappen van het tip-bericht**

De vormgeving van het tip-bericht wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

Het is mogelijk lettertypestijl, vormgeving van grootte en verticale verschuiving te configureren via CSS. De horizontale uitlijning wordt echter beheerd door de viewerlogica. Het overschrijven van de eigenschap via CSS met behulp `left` van eigenschappen of `right` eigenschappen wordt niet ondersteund.

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Verschuiving vanaf de onderkant van de hoofdweergave. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur </span> </p> </td> 
   <td colname="col2"> <p>Tekstkleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Fontnaam. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen </span> </p> </td> 
   <td colname="col2"> <p>Opvulling rond de berichttekst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>De achtergrondvulkleur van berichttekst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Straal achtergrondrand van berichttekst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dekking </span> </p> </td> 
   <td colname="col2"> <p>Achtergronddekking van berichttekst. </p> <p>Gebruik voor Internet Explorer 8 <span class="codeph"> filter:alpha(opacity-...)) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Het tip-bericht kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) voor meer informatie.

Voorbeeld - voor het instellen van een half-transparant uiteindebericht met een wit lettertype van Arial 12 px, een verschuiving van 50 pixels ten opzichte van de onderkant van de hoofdweergave, opvulling en een afgeronde rand:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```


---
description: De hoofdweergave bestaat uit de statische afbeelding, de ingezoomde afbeelding die boven op de statische afbeelding wordt weergegeven in de vervolgweergave en het uiteindebericht dat boven op de statische afbeelding wordt weergegeven.
seo-description: De hoofdweergave bestaat uit de statische afbeelding, de ingezoomde afbeelding die boven op de statische afbeelding wordt weergegeven in de vervolgweergave en het uiteindebericht dat boven op de statische afbeelding wordt weergegeven.
seo-title: Zoomweergave flyout
solution: Experience Manager
title: Zoomweergave flyout
topic: Dynamic media
uuid: a918c775-a36a-44e8-9ca4-90cb8f5c3a5e
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zoomweergave flyout{#flyout-zoom-view}

De hoofdweergave bestaat uit de statische afbeelding, de ingezoomde afbeelding die boven op de statische afbeelding wordt weergegeven in de vervolgweergave en het uiteindebericht dat boven op de statische afbeelding wordt weergegeven.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

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

Het tip-bericht kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) voor meer informatie.

.

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


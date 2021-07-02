---
description: In de hoofdweergave van de inline zoommodus bestaat de ingezoomde afbeelding uit de statische afbeelding die in de uitvliegweergave boven de statische afbeelding wordt weergegeven en het uiteindebericht dat boven op de statische afbeelding wordt weergegeven.
solution: Experience Manager
title: Zoomweergave flyout
feature: Dynamic Media Classic,Viewers,SDK/API,Gemengde mediasets
role: Developer,Business Practitioner
exl-id: 46c91d1f-5809-4270-a06d-5068d20a6341
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---

# Zoomweergave flyout{#flyout-zoom-view}

In de hoofdweergave van de inline zoommodus bestaat de ingezoomde afbeelding uit de statische afbeelding die in de uitvliegweergave boven de statische afbeelding wordt weergegeven en het uiteindebericht dat boven op de statische afbeelding wordt weergegeven.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van de hoofdweergave wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7mixedmediaviewer .s7flyoutzoomview
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
   <td colname="col2"> <p> De achtergrondkleur van de hoofdweergave. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - om de hoofdweergave transparant te maken:

```
.s7mixedmediaviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

<!--<a id="section_FD07AB77593748F99DC6C42ED20A61EC"></a>-->

De vormgeving van het tip-bericht wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip
```

Het is mogelijk om lettertypestijl, vormgeving van grootte en verticale verschuiving te configureren via CSS. De horizontale uitlijning wordt echter beheerd door de viewerlogica. Het overschrijven van een item via CSS met de eigenschappen `left` of `right` wordt niet ondersteund.

**CSS-eigenschappen van het tip-bericht**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Achtergrondvulkleur van bericht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Straal achtergrondrand van bericht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p> Verschuiving vanaf de onderkant van de hoofdweergave. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur  </span> </p> </td> 
   <td colname="col2"> <p>Tekstkleur uiteinde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte  </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Lettertypefamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dekking  </span> </p> </td> 
   <td colname="col2"> <p> Achtergronddekking van bericht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opvullen  </span> </p> </td> 
   <td colname="col2"> <p> Opvulling rond de berichttekst. </p> </td> 
  </tr> 
 </tbody> 
</table>

Het tip-bericht kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) voor meer informatie.

Voorbeeld - Als u een half-transparant uiteindebericht wilt instellen met een wit lettertype van Arial 12 px, worden 50 pixels van de onderkant van de hoofdweergave verschoven, wordt de tekst opgevuld en wordt de rand afgerond:

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip { 
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

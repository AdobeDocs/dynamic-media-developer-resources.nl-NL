---
title: Indicator instellen
description: De indicator Set is een reeks punten die onder aan de viewer worden weergegeven. De huidige positie in de set wordt weergegeven.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 7d0827c5-f420-4804-983c-5298ee92b276
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Indicator instellen{#set-indicator}

De indicator Set is een reeks punten die onder aan de viewer worden weergegeven. De huidige positie in de set wordt weergegeven.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van de setindicator**

De vormgeving van de setindicatorcontainer wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7carouselviewer .s7setindicator
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
   <td colname="col2"> <p>De achtergrondkleur in hexadecimale notatie van de setindicator. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>De indicator Set ondersteunt de selector van het moduskenmerk, waarmee u verschillende stijlen kunt toepassen voor de modi dotted en Numeric. Met name: `mode="numeric"` komt overeen met de numerieke bedrijfsmodus; `mode="dotted"` komt overeen met de standaardpuntstatus.

Stel dat u een setindicator met een witte achtergrond wilt instellen:

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

De vormgeving van een individuele set-indicator punt wordt bepaald door de CSS-klassenkiezer. De optie is van toepassing op items in zowel de modus Stippel als de modus Numeriek.

`.s7carouselviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van punt van indicator instellen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van punt van de ingestelde indicator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p>Linkermarge in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p>Bovenmarge in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marge-rechts </span> </p> </td> 
   <td colname="col2"> <p>Rechtermarge in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom </span> </p> </td> 
   <td colname="col2"> <p>Ondermarge in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Randstraal in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Achtergrondkleur in hexadecimale notatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Naam van lettertype. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Grootte van lettertype. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur </span> </p> </td> 
   <td colname="col2"> <p>Kleur van lettertype. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align </span> </p> </td> 
   <td colname="col2"> <p>Verticale uitlijning van de bannerindex. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> regelhoogte </span> </p> </td> 
   <td colname="col2"> <p>Teksthoogte voor de bannerindex. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Indicatie-items instellen ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende miniatuurtoestanden. Met name: `state="selected"` overeenstemt met het huidige element in de reeks; `state="unselected"` komt overeen met de status van het standaarditem.

Stel dat u een instellingsindicator wilt instellen in de stippelmodus voor desktopsystemen. U wilt dat het 20 pixels van de onderkant van de viewer verwijderd is. En niet-geselecteerde stippen moeten zwart zijn met 50% transparantie en 15 x 15 pixels met 7 pixels afgeronde hoeken. Geselecteerde stippen zijn zwart met 90% transparantie, 18 x 18 pixels met negen pixels afgeronde hoeken. De ruimte tussen stippen is vijf pixels.

```
.s7carouselviewer.s7mouseinput .s7setindicator { 
 bottom: 20px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot{ 
 width:15px; 
 height:15px; 
 margin-left:2.5px; 
 margin-right:2.5px; 
 margin-top:2.5px; 
 margin-bottom:2.5px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='selected'] {  
 width:18px; 
 height:18px; 
 background-color: #000000; 
 opacity: 0.9; 
 border-radius:9px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='unselected'] {  
 width:15px; 
 height:15px; 
 background-color: #000000; 
 opacity: 0.5; 
 border-radius:7px; 
}
```

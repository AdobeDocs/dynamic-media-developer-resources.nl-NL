---
title: Indicator instellen
description: De indicator Set is een reeks punten die boven op stalen worden weergegeven wanneer een viewer wordt gebruikt op een aanraakapparaat. Met de puntjes kunnen gebruikers door pagina's met miniaturen navigeren wanneer er geen schuifknoppen beschikbaar zijn.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: b1e6734e-a341-45d7-b771-daeb0527cd00
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# Indicator instellen{#set-indicator}

De indicator Set is een reeks punten die boven op stalen worden weergegeven wanneer een viewer wordt gebruikt op een aanraakapparaat. Met de puntjes kunnen gebruikers door pagina&#39;s met miniaturen navigeren wanneer er geen schuifknoppen beschikbaar zijn.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van de setindicator**

De vormgeving van de setindicatorcontainer wordt beheerd met de volgende CSS-klassenkiezer:

```
.s7zoomviewer .s7setindicator
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

Voorbeeld - Een setindicator met een witte achtergrond maken:

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

De vormgeving van een individuele set-indicator punt wordt bepaald door de CSS-klassenkiezer:

`.s7zoomviewer .s7setindicator .s7dot`

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
 </tbody> 
</table>

>[!NOTE]
>
>Punt van indicator instellen ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende miniatuurtoestanden. Met name: `state="selected"` komt overeen met de huidige pagina met miniaturen, `state="unselected"` komt overeen met de standaardpuntstatus.

Voorbeeld - Als u een ingestelde indicatorpunt wilt maken met een waarde van 15 x 15 pixels, met 2 pixels horizontale marge, 5 pixels bovenste marge, 1 pixel onderste marge, 12 pixels radius, #D5D3D3 standaardkleur en #939393 actieve kleur:

```
.s7zoomviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7zoomviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```

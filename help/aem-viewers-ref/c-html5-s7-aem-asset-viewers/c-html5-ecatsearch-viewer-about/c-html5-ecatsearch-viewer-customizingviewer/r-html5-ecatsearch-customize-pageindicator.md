---
title: Pagina-indicator
description: Pagina-indicator geeft de huidige pagina-index en het totale aantal pagina's weer. Het verschijnt in belangrijkste controlebar op Desktopsystemen en tablet, op mobiele telefoons wordt het toegevoegd aan secundaire controlebar. De pagina-indicator kan door CSS worden vergroot of verkleind, van een skin worden voorzien en worden geplaatst.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 38241e96-ee7f-4dc1-a2a6-4a76e25b00dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# Pagina-indicator{#page-indicator}

Pagina-indicator geeft de huidige pagina-index en het totale aantal pagina&#39;s weer. Het verschijnt in belangrijkste controlebar op Desktopsystemen en tablet, op mobiele telefoons wordt het toegevoegd aan secundaire controlebar. De pagina-indicator kan door CSS worden vergroot of verkleind, van een skin worden voorzien en worden geplaatst.

De indicator voor de weergavepagina wordt beheerd met de volgende CSS-klassenkiezer:

`.s7ecatalogsearchviewer .s7pageindicator`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Plaats vanaf de bovenrand van de hoofdbesturingsbalk (op desktopsystemen en tablets) of de secundaire besturingsbalk (op mobiele telefoons), inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de rechterrand van de hoofdbesturingsbalk (op desktopsystemen en tablets) of de secundaire besturingsbalk (op mobiele telefoons), inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de linkerrand van de hoofdbesturingsbalk (op desktopsystemen en tablets) of de secundaire besturingsbalk (op mobiele telefoons), inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Plaats vanaf de onderrand van de hoofdbesturingsbalk (op desktopsystemen en tablets) of de secundaire besturingsbalk (op mobiele telefoons), inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de pagina-indicator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de pagina-indicator. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kleur </span> </p> </td> 
   <td colname="col2"> <p>Fontkleur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Fontnaam. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tekengrootte </span> </p> </td> 
   <td colname="col2"> <p>Tekengrootte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - voor het instellen van een pagina-indicator van 56 x 28 pixels, horizontaal gecentreerd en gepositioneerd 4 pixels vanaf de onderkant van de hoofdbesturingsbalk, en het gebruik van een Helvetica®-lettertype van 14 pixels.

```
.s7ecatalogsearchviewer  .s7pageindicator { 
 position:absolute; 
 bottom: 4px; 
 margin-left: -28px;  
 left: 50%; 
 width:56px; 
 height:28px; 
 font-family: Helvetica; 
 font-size:14px; 
}
```

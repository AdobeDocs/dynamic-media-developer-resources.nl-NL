---
description: De secundaire besturingsbalk is het rechthoekige gebied met de knoppen Eerste en Laatste pagina en een pagina-indicator wanneer deze beschikbaar worden gemaakt in CSS.
seo-description: De secundaire besturingsbalk is het rechthoekige gebied met de knoppen Eerste en Laatste pagina en een pagina-indicator wanneer deze beschikbaar worden gemaakt in CSS.
seo-title: Secundaire besturingsbalk
solution: Experience Manager
title: Secundaire besturingsbalk
topic: Dynamic media
uuid: 9a91da6b-0d9b-4b4c-9659-86a64e624947
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Secundaire besturingsbalk{#secondary-control-bar}

De secundaire besturingsbalk is het rechthoekige gebied met de knoppen Eerste en Laatste pagina en een pagina-indicator wanneer deze beschikbaar worden gemaakt in CSS.

Standaard wordt de presentatie alleen weergegeven op mobiele telefoons en bevindt deze zich onder aan de viewer. De viewerbreedte neemt altijd de volledige beschikbare viewerbreedte in beslag. Het is mogelijk de kleur, hoogte en verticale positie ervan te wijzigen met CSS ten opzichte van de viewercontainer.

De weergave van de secundaire besturingsbalk wordt bepaald door de volgende CSS-klassenkiezer:

`.s7ecatalogviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Positie boven aan de viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Positie onder aan de viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van de hoofdbesturingsbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>De achtergrondkleur van de secundaire besturingsbalk. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - voor het instellen van een grijze secundaire besturingsbalk die 72 pixels hoog is en onder aan de viewercontainer wordt geplaatst.

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```


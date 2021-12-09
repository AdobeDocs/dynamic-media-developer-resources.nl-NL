---
title: Knop Zoomen opnieuw instellen
description: Als u deze knop selecteert of tikt, wordt een afbeelding in de hoofdweergave opnieuw ingesteld. Deze knop wordt weergegeven in de hoofdbesturingsbalk op desktopsystemen en tablets. Op mobiele telefoons wordt deze knop in het midden onder op de afbeelding weergegeven. De voorinstelling wordt echter niet weergegeven wanneer de afbeelding is hersteld. U kunt deze knop vergroten, verkleinen, verkleinen en plaatsen met CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 6f0e22cd-12bd-4997-b874-539962504d3e
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Knop Zoomen opnieuw instellen{#zoom-reset-button}

Als u deze knop selecteert of tikt, wordt een afbeelding in de hoofdweergave opnieuw ingesteld. Deze knop wordt weergegeven in de hoofdbesturingsbalk op desktopsystemen en tablets. Op mobiele telefoons wordt deze knop in het midden onder op de afbeelding weergegeven. De voorinstelling wordt echter niet weergegeven wanneer de afbeelding is hersteld. U kunt deze knop vergroten, verkleinen, verkleinen en plaatsen met CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van de knop wordt bepaald door de volgende CSS-klassenkiezer:

`.s7ecatalogviewer .s7zoomresetbutton`

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
   <td colname="col2"> <p>Plaats vanaf de bovenrand van de hoofdbesturingsbalk (op desktops en tablets) of viewer (op mobiele telefoons), inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Plaats vanaf de rechterrand van de hoofdbesturingsbalk (op desktops en tablets) of viewer (op mobiele telefoons), inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de linkerrand van de hoofdbesturingsbalk (op desktops en tablets) of viewer (op mobiele telefoons), inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Plaats vanaf de onderrand van de hoofdbesturingsbalk (op desktops en tablets) of viewer (op mobiele telefoons), inclusief opvulling. </p> </td> 
  </tr> 
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
   <td colname="col2"> <p>De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie .

Voorbeeld - Een knop voor het opnieuw instellen van zoomen instellen van 28 x 28 pixels en gepositioneerd (op het bureaublad) 4 pixels van de onderrand en 47 pixels van de rechterrand van de hoofdbesturingsbalk. En tenslotte, toont een verschillend beeld voor elk van de vier verschillende knoopstaten.

```
.s7ecatalogviewer .s7zoomresetbutton { 
bottom:4px; 
right:47px; 
width:28px; 
height:28px; 
} 
.s7ecatalogviewer .s7zoomresetbutton [state='up'] { 
background-image:url(images/v2/ZoomResetButton_dark_up.png); 
} 
.s7ecatalogviewer .s7zoomresetbutton [state='over'] {  
background-image:url(images/v2/ZoomResettButton_dark_over.png); 
} 
.s7ecatalogviewer .s7zoomresetbutton [state='down'] {  
background-image:url(images/v2/ZoomResetButton_dark_down.png); 
} 
.s7ecatalogviewer .s7zoomresetbutton [state='disabled'] { 
background-image:url(images/v2/ZoomResetButton_dark_disabled.png); 
}
```

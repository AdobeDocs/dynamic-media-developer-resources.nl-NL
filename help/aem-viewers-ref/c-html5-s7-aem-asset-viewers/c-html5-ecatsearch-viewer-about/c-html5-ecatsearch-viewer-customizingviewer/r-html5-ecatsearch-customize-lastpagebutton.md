---
title: Knop Laatste pagina
description: Als u deze knop selecteert, komt de gebruiker op de laatste pagina in de catalogus te staan. Deze knop wordt weergegeven in de hoofdbesturingsbalk op desktopsystemen en tablets. op mobiele telefoons wordt het toegevoegd aan een secundaire besturingsbalk. U kunt deze knop vergroten, verkleinen, verkleinen en plaatsen met CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fa1ff52c-6fb1-47e7-b3d4-216fea02bbd8
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Knop Laatste pagina{#last-page-button}

Als u deze knop selecteert, komt de gebruiker op de laatste pagina in de catalogus te staan. Deze knop wordt weergegeven in de hoofdbesturingsbalk op desktopsystemen en tablets. op mobiele telefoons wordt het toegevoegd aan een secundaire besturingsbalk. U kunt deze knop vergroten, verkleinen, verkleinen en plaatsen met CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van de knop wordt bepaald door de volgende CSS-klassenkiezer:

`.s7ecatalogsearchviewer .s7lastpagebutton .s7panleftbutton`

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
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt de `state` kenmerkenkiezer, die kan worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie .

Voorbeeld - Aan opstelling een laatste paginaknoop die 28 x 28 pixel is, en gepositioneerd 4 pixel van de bodem en 220 pixel van de linkerrand van de belangrijkste controlebar. En tenslotte, toont een verschillend beeld voor elk van de vier verschillende knoopstaten.

```
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton { 
bottom:4px; 
right:220px; 
width:32px; 
height:32px; 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='up'] { 
background-image:url(images/v2/LastPageButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='over'] {  
background-image:url(images/v2/LastPageButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='down'] {  
background-image:url(images/v2/LastPageButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='disabled'] { 
background-image:url(images/v2/LastPageButton_dark_disabled.png); 
}
```

---
title: Knop Grote vorige pagina
description: Als u deze knop selecteert, komt de gebruiker naar de vorige pagina in de catalogus. Deze knop wordt weergegeven in de hoofdbesturingsbalk. Deze knop wordt niet weergegeven op mobiele telefoons om de schermruimte op te slaan. U kunt deze knop vergroten, verkleinen, verkleinen en plaatsen met CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 39bf9f23-1950-4920-877e-b07e8df18bdc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Knop Grote vorige pagina{#large-previous-page-button}

Als u deze knop selecteert, komt de gebruiker naar de vorige pagina in de catalogus. Deze knop wordt weergegeven in de hoofdbesturingsbalk. Deze knop wordt niet weergegeven op mobiele telefoons om de schermruimte op te slaan. U kunt deze knop vergroten, verkleinen, verkleinen en plaatsen met CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van de knop wordt bepaald door de volgende CSS-klassenkiezer:

`.s7ecatalogsearchviewer .s7ecatleftbutton .s7panleftbutton`

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
   <td colname="col2"> <p>Positie vanaf de bovenrand van de hoofdbesturingsbalk, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de rechterrand van de hoofdbesturingsbalk, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de linkerrand van de hoofdbesturingsbalk, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de onderrand van de hoofdbesturingsbalk, inclusief opvulling. </p> </td> 
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

Voorbeeld - voor het instellen van een grote knop voor vorige pagina van 56 x 56 pixels, verticaal gecentreerd en verankerd aan de linkerviewerrand, en voor het weergeven van een andere afbeelding voor elk van de vier verschillende knopstatussen.

```
.s7ecatalogsearchviewer .s7ecatleftbutton .s7panleftbutton { 
bottom:50%; 
margin-bottom:-28px; 
left:0px; 
width:56px; 
height:56px; 
} 
.s7ecatalogsearchviewer .s7ecatleftbutton .s7panleftbutton [state='up'] { 
background-image:url(images/v2/LeftButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7ecatleftbutton .s7panleftbutton [state='over'] {  
background-image:url(images/v2/LeftButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7ecatleftbutton .s7panleftbutton [state='down'] {  
background-image:url(images/v2/LeftButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7ecatleftbutton .s7panleftbutton [state='disabled'] { 
background-image:url(images/v2/LeftButton_dark_disabled.png); 
}
```

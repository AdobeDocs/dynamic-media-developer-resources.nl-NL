---
description: Als u op deze knop klikt of erop tikt, wordt de afbeelding in de hoofdweergave links gecentreerd. Deze knop wordt niet weergegeven op mobiele telefoons om de schermruimte op te slaan. De knop is ook verborgen wanneer een multidimensionale centrifugeset wordt gebruikt. U kunt de grootte, de huid, en de positie van de knoop gebruikend CSS.
seo-description: Als u op deze knop klikt of erop tikt, wordt de afbeelding in de hoofdweergave links gecentreerd. Deze knop wordt niet weergegeven op mobiele telefoons om de schermruimte op te slaan. De knop is ook verborgen wanneer een multidimensionale centrifugeset wordt gebruikt. U kunt de grootte, de huid, en de positie van de knoop gebruikend CSS.
seo-title: Linkerkant draaien, knop
solution: Experience Manager
title: Linkerkant draaien, knop
topic: Dynamic media
uuid: 742a912b-7ca1-43d4-aae6-a809e01d34b9
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---


# Linkerknop draaien{#spin-left-button}

Als u op deze knop klikt of erop tikt, wordt de afbeelding in de hoofdweergave links gecentreerd. Deze knop wordt niet weergegeven op mobiele telefoons om de schermruimte op te slaan. De knop is ook verborgen wanneer een multidimensionale centrifugeset wordt gebruikt. U kunt de grootte, de huid, en de positie van de knoop gebruikend CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van de centrifugeknoppen**

De knop wordt toegevoegd aan een interne container die wordt beheerd met de CSS-klassenkiezer:

```
.s7mixedmediaviewer .s7spinbuttons
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
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de bovenrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de rechterrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de linkerrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de onderrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de knop. </p> </td> 
  </tr> 
 </tbody> 
</table>

De weergave van deze knop in de container wordt bepaald door de CSS-klassenkiezer:

```
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton
```

<table id="table_3EC45539877A479DB83E8FC69142450B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de bovenrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de rechterrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de linkerrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de onderrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p>De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoop steunt `state` attributenselecteur, die kan worden gebruikt om verschillende huiden op verschillende knoopstaten toe te passen.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) voor meer informatie.

Voorbeeld - om een centrifuge linkerknoop op te zetten die 28 x 28 pixel is, die op de linkerrand van binnencontainer wordt geplaatst, en die een verschillend beeld voor elk van de vier verschillende knoopstaten toont:

```
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton { 
 position:absolute; 
 left: 0px; 
 width:28px; 
 height:28px; 
 background-size:contain; 
 } 
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton[state='up'] { 
background-image:url(images/v2/SpinLeftButton_light_up.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton[state='over'] { 
background-image:url(images/v2/SpinLeftButton_light_over.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton[state='down'] { 
background-image:url(images/v2/SpinLeftButton_light_down.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton[state='disabled'] { 
background-image:url(images/v2/SpinLeftButton_light_disabled.png); 
}
```


---
description: Als u op deze knop klikt of erop tikt, zoomt u in op een afbeelding in de hoofdweergave. Deze knop wordt niet weergegeven op mobiele telefoons om de schermruimte op te slaan. U kunt deze knop vergroten, verkleinen, verkleinen en plaatsen met CSS.
seo-description: Als u op deze knop klikt of erop tikt, zoomt u in op een afbeelding in de hoofdweergave. Deze knop wordt niet weergegeven op mobiele telefoons om de schermruimte op te slaan. U kunt deze knop vergroten, verkleinen, verkleinen en plaatsen met CSS.
seo-title: Knop Inzoomen
solution: Experience Manager
title: Knop Inzoomen
topic: Dynamic Media
uuid: 35b7797c-e0d2-4ce4-bf69-0fe20ab4c8f1
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---


# Knop Inzoomen{#zoom-in-button}

Als u op deze knop klikt of erop tikt, zoomt u in op een afbeelding in de hoofdweergave. Deze knop wordt niet weergegeven op mobiele telefoons om de schermruimte op te slaan. U kunt deze knop vergroten, verkleinen, verkleinen en plaatsen met CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van de knop wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7zoomviewer .s7zoominbutton
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
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p>De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoop steunt `state` attributenselecteur, die kan worden gebruikt om verschillende huiden op verschillende knoopstaten toe te passen.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Voorbeeld: om een inzoomknop van 32 x 32 pixels in te stellen, die zes pixels van de boven- en rechterrand van de viewer is geplaatst, en een andere afbeelding weer te geven voor elk van de vier verschillende knopstatussen.

```
.s7zoomviewer .s7zoominbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7zoomviewer .s7zoominbutton [state='up'] { 
background-image:url(images/v2/ZoomInButton_dark_up.png); 
} 
.s7zoomviewer .s7zoominbutton [state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png); 
} 
.s7zoomviewer .s7zoominbutton [state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png); 
} 
.s7zoomviewer .s7zoominbutton [state='disabled'] { 
background-image:url(images/v2/ZoomInButton_dark_disabled.png); 
}
```


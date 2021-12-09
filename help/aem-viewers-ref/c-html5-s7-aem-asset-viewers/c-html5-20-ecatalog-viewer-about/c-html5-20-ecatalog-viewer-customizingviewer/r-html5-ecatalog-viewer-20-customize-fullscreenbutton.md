---
title: Knop Volledig scherm
description: Hiermee gaat de viewer naar de modus Volledig scherm of wordt deze afgesloten wanneer deze door de gebruiker is geselecteerd. Deze knop wordt weergegeven in de hoofdbesturingsbalk. Deze knop wordt niet weergegeven als de viewer werkt in de pop-upmodus en het systeem geen native volledig scherm ondersteunt. U kunt de grootte, de huid, en de plaats van de knoop door CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3f56fbd2-4d2e-4cfa-bc97-350bc2bb708e
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Knop Volledig scherm{#full-screen-button}

Hiermee gaat de viewer naar de modus Volledig scherm of wordt deze afgesloten wanneer deze door de gebruiker is geselecteerd. Deze knop wordt weergegeven in de hoofdbesturingsbalk. Deze knop wordt niet weergegeven als de viewer werkt in de pop-upmodus en het systeem geen native volledig scherm ondersteunt. U kunt de grootte, de huid, en de plaats van de knoop door CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van de knop wordt bepaald door de volgende CSS-klassenkiezer:

`.s7ecatalogviewer .s7fullscreenbutton`

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
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knop ondersteunt beide `state` en `selected` kenmerkkiezers, die kunnen worden gebruikt om verschillende skins toe te passen op verschillende knoptoestanden. Met name: `selected='true'` komt overeen met de toestand &quot;Volledig scherm&quot; en `selected='false'` komt overeen met de toestand &quot;normaal&quot;.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie .

Voorbeeld - Een knop voor volledig scherm instellen met een afstand van 28 x 28 pixels vanaf de onderkant en 5 pixels vanaf de rechterrand van de hoofdbesturingsbalk. En ten slotte wordt voor elk van de vier verschillende knoptoestanden een andere afbeelding weergegeven wanneer deze is geselecteerd of niet.

```
.s7ecatalogviewer .s7fullscreenbutton { 
bottom:4px; 
right:5px; 
width:28px; 
height:28px; 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7ecatalogviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```

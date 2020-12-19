---
description: Als u op deze knop klikt of erop tikt, wordt de viewer tussen de hoofdweergave en de miniaturen geschakeld. Deze knop wordt weergegeven in de hoofdbesturingsbalk. U kunt deze knop vergroten, verkleinen, verkleinen en plaatsen met CSS.
seo-description: Als u op deze knop klikt of erop tikt, wordt de viewer tussen de hoofdweergave en de miniaturen geschakeld. Deze knop wordt weergegeven in de hoofdbesturingsbalk. U kunt deze knop vergroten, verkleinen, verkleinen en plaatsen met CSS.
seo-title: Knop Miniaturen
solution: Experience Manager
title: Knop Miniaturen
topic: Dynamic media
uuid: a1a7f4b0-672e-4b83-9b21-0b8c6fc3f24a
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%

---


# Knop Miniaturen{#thumbnails-button}

Als u op deze knop klikt of erop tikt, wordt de viewer tussen de hoofdweergave en de miniaturen geschakeld. Deze knop wordt weergegeven in de hoofdbesturingsbalk. U kunt deze knop vergroten, verkleinen, verkleinen en plaatsen met CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van de knop wordt bepaald door de volgende CSS-klassenkiezer:

`.s7ecatalogviewer .s7thumbnailpagebutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> De verschuiving vanaf de bovenkant van de besturingsbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> De afstand aan de volgende knoop op de linkerzijde, of de linkerkant van de controlebar als dit de eerste knoop in een rij is. </p> </td> 
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
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoop steunt zowel `state` als `selected` attribuutselecteurs, die kunnen worden gebruikt om verschillende huiden op verschillende knoopstaten toe te passen. Met name `selected='true'` komt overeen met de viewerstatus wanneer de miniatuurmodus actief is en `selected='false'` overeenkomt met de standaardstatus bij de hoofdweergave.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - om een knop met miniaturen in te stellen van 28 x 28 pixels, op 4 pixels van de onderkant en 5 pixels van de linkerrand van de hoofdbesturingsbalk, en een andere afbeelding weer te geven voor elk van de vier verschillende knopstatussen, al dan niet geselecteerd.

```
.s7ecatalogviewer .s7thumbnailpagebutton{ 
margin-top: 4px; 
margin-left: 5px; width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='false'][state='up'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_up.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='false'][state='over'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='false'][state='down'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_down.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='false'][state='disabled'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_disabled.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='true'][state='up'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='true'][state='over'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='true'][state='down'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='true'][state='disabled'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_disabled.png); 
}
```


---
description: Knop Zoeken
solution: Experience Manager
title: Knop Zoeken
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# Knop Zoeken{#search-button}

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van de knop wordt bepaald door de volgende CSS-klassenkiezer:

`.s7ecatalogsearchviewer .s7searchbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-eigenschap </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breedte van de knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Hoogte van de knop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> De verschuiving vanaf de bovenkant van de besturingsbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> De afstand aan de volgende knoop op de linkerzijde, of de linkerkant van de controlebar als dit de eerste knoop in een rij is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p>De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoop steunt `state` en `selected` attribuutselecteurs, die kunnen worden gebruikt om verschillende huiden op verschillende knoopstaten toe te passen.
>
>Met name `selected='false'` komt overeen met de eerste status van de schuifknop en `selected='true'` komt overeen met de status wanneer het zoekdeelvenster actief is.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld: om een zoekknop in te stellen van 28 x 28 pixels en een andere afbeelding weer te geven voor elk van de vier verschillende knopstatussen, indien geselecteerd of niet geselecteerd.

```
.s7ecatalogsearchviewer .s7searchbutton{ 
 margin-top: 4px; 
 margin-left: 10px; 
 width:28px; 
 height:28px;  
 display: inline-block; 
 background-size:contain; 
} 
 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/Search_dark_up.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/Search_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/Search_dark_down.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/Search_dark_disabled.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/Search_dark_over.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/Search_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/Search_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/Search_dark_disabled.png);  
}
```


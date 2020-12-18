---
description: Het gereedschap voor sociaal delen wordt standaard in de linkerbovenhoek weergegeven. Het bestaat uit een knop en een deelvenster dat groter wordt wanneer de gebruiker op een knop klikt of tikt en dat afzonderlijke gereedschappen voor delen bevat.
seo-description: Het gereedschap voor sociaal delen wordt standaard in de linkerbovenhoek weergegeven. Het bestaat uit een knop en een deelvenster dat groter wordt wanneer de gebruiker op een knop klikt of tikt en dat afzonderlijke gereedschappen voor delen bevat.
seo-title: Sociaal aandeel
solution: Experience Manager
title: Sociaal aandeel
topic: Dynamic media
uuid: 6d463eb1-c6bf-4f1c-90e4-b5ef1e5a1538
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---


# Sociaal delen{#social-share}

Het gereedschap voor sociaal delen wordt standaard in de linkerbovenhoek weergegeven. Het bestaat uit een knop en een deelvenster dat groter wordt wanneer de gebruiker op een knop klikt of tikt en dat afzonderlijke gereedschappen voor delen bevat.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De positie en grootte van het gereedschap voor sociaal delen in de gebruikersinterface van de viewer worden als volgt bepaald:

```
.s7ecatalogsearchviewer .s7socialshare
```

**CSS-eigenschappen van het gereedschap voor sociaal delen**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> De verschuiving vanaf de bovenkant van de besturingsbalk. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin=left  </span> </p> </td> 
   <td colname="col2"> <p> De afstand aan de volgende knoop op de linkerzijde, of de linkerkant van de controlebar als dit de eerste knoop in een rij is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> De breedte van het gereedschap voor sociaal delen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van het gereedschap voor sociaal delen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld: stel een gereedschap voor sociaal delen in dat zich vier pixels van de bovenkant en vijf pixels van de rechterkant van de viewercontainer bevindt en dat een formaat heeft van 28 x 28 pixels.

```
.s7ecatalogsearchviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

De vormgeving van de knop voor het gereedschap Sociaal delen wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton
```

**CSS-eigenschappen van de sociale knop**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p> De afbeelding die voor een bepaalde knopstatus wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie ook <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoop steunt `state` attributenselecteur, die kan worden gebruikt om verschillende huiden op verschillende knoopstaten toe te passen.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

Voorbeeld - stel een knop voor een gereedschap voor sociaal delen in, waarmee een andere afbeelding wordt weergegeven voor elk van de vier verschillende knopstatussen.

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

De weergave van het deelvenster met de afzonderlijke pictogrammen voor sociaal delen wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel
```

**CSS-eigenschappen van het deelvenster voor sociaal delen**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>De achtergrondkleur van het deelvenster. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - een deelvenster instellen om een transparante kleur te krijgen:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```


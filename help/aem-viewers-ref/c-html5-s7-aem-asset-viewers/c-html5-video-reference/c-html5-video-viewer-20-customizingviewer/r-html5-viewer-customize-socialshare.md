---
description: Het gereedschap voor sociaal delen wordt standaard in de rechterbovenhoek weergegeven. Het bestaat uit een knop en een deelvenster dat groter wordt wanneer de gebruiker op een knop klikt of tikt en dat afzonderlijke gereedschappen voor delen bevat.
seo-description: Het gereedschap voor sociaal delen wordt standaard in de rechterbovenhoek weergegeven. Het bestaat uit een knop en een deelvenster dat groter wordt wanneer de gebruiker op een knop klikt of tikt en dat afzonderlijke gereedschappen voor delen bevat.
seo-title: Sociaal aandeel
solution: Experience Manager
title: Sociaal aandeel
topic: Dynamic media
uuid: 5c1ce7b4-54bf-486f-8b57-1d6d0cec119e
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---


# Sociaal delen{#social-share}

Het gereedschap voor sociaal delen wordt standaard in de rechterbovenhoek weergegeven. Het bestaat uit een knop en een deelvenster dat groter wordt wanneer de gebruiker op een knop klikt of tikt en dat afzonderlijke gereedschappen voor delen bevat.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

De positie en grootte van het gereedschap voor sociaal delen in de gebruikersinterface van de viewer worden als volgt bepaald:

```
.s7videoviewer .s7socialshare
```

**CSS-eigenschappen van het gereedschap voor sociaal delen**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Verticale positie van het gereedschap voor sociaal delen ten opzichte van de viewercontainer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p> Horizontale positie van het gereedschap voor sociaal delen ten opzichte van de viewercontainer. </p> </td> 
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
.s7videoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

De vormgeving van de knop voor het gereedschap Sociaal delen wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7videoviewer .s7socialshare .s7socialbutton
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
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoop steunt `state` attributenselecteur, die kan worden gebruikt om verschillende huiden op verschillende knoopstaten toe te passen.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) voor meer informatie.

Voorbeeld - stel een knop voor een gereedschap voor sociaal delen in, waarmee een andere afbeelding wordt weergegeven voor elk van de vier verschillende knopstatussen.

```
.s7videoviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7videoviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

De weergave van het deelvenster met de afzonderlijke pictogrammen voor sociaal delen wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7videoviewer .s7socialshare .s7socialsharepanel
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
.s7videoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```


---
description: De knop Volledig scherm zorgt ervoor dat de videospeler de modus Volledig scherm opent of sluit wanneer de gebruiker erop klikt.
solution: Experience Manager
title: Knop Volledig scherm
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: ed9c9d37-f871-4094-9c6e-931d0f6edff1
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Knop Volledig scherm{#full-screen-button}

De knop Volledig scherm zorgt ervoor dat de videospeler de modus Volledig scherm opent of sluit wanneer de gebruiker erop klikt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

U kunt de grootte, de huid, en de positie van de volledige het schermknoop, met betrekking tot de controlebar die het bevat, door CSS rangschikken.

De weergave van de knop Volledig scherm wordt bepaald door de CSS-klassenkiezer:

```
.s7interactivevideoviewer .s7fullscreenbutton
```

**CSS-eigenschappen van de knop Volledig scherm**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Positie vanaf de bovenrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p> Positie vanaf de rechterrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p> Positie vanaf de linkerrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Positie vanaf de onderrand, inclusief opvulling. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> De breedte van de knop Volledig scherm. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>De hoogte van de knop Volledig scherm. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> achtergrondafbeelding  </span> </p> </td> 
   <td colname="col2"> <p> De weergegeven afbeelding voor een bepaalde knopstatus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Positie binnen illustratie-sprite, als CSS-sprites worden gebruikt. </p> <p>Zie <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Deze knoop steunt zowel `state` als `selected` attribuutselecteurs, die kunnen worden gebruikt om verschillende huiden op verschillende knoopstaten toe te passen. Met name `selected='true'` komt overeen met de status &quot;volledig scherm&quot; en `selected='false'` komt overeen met de status &quot;normaal&quot;.

De knopinfo kan worden gelokaliseerd. Zie [Lokalisatie van gebruikersinterface-elementen](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) voor meer informatie.

## Voorbeeld {#section-e8caea0a303c425a8a637c2a47c06355}

Aan opstelling een volledig het schermknoop die 32 x 32 pixel is, en geplaatst 6 pixel van de bovenkant en de juiste rand van de controlebar. Geef ook een andere afbeelding weer voor elk van de vier verschillende knoptoestanden, indien geselecteerd of niet.

```
.s7interactivevideoviewer . s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7interactivevideoviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7interactivevideoviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7interactivevideoviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7interactivevideoviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7interactivevideoviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7interactivevideoviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7interactivevideoviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7interactivevideoviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```

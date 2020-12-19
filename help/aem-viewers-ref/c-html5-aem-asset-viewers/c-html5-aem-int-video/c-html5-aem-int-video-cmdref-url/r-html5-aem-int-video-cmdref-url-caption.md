---
description: URL-opdracht voor interactieve video-viewer.
seo-description: URL-opdracht voor interactieve video-viewer.
seo-title: bijschrift
solution: Experience Manager
title: bijschrift
topic: Dynamic media
uuid: 602c8f64-e018-4916-8141-09b36003a99d
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---


# caption{#caption}

URL-opdracht voor interactieve video-viewer.

` caption= *`file`*[,0|1]`

De viewer ondersteunt ondertiteling via gehoste WebVTT-bestanden. Overlappende cues en gebieden worden niet ondersteund. Tot de ondersteunde operatoren voor actiepunten behoren:

<table id="table_62D89A06EC9E4E7983D1F26A2C85A621"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sleutel </p> </th> 
   <th colname="col2" class="entry"> <p>Naam </p> </th> 
   <th colname="col3" class="entry"> <p>Waarde </p> </th> 
   <th colname="col4" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A  </span> </p> </td> 
   <td colname="col2"> <p>tekst uitlijnen </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|start|end  </span> </p> </td> 
   <td colname="col4"> <p> Tekstuitlijning bepalen. </p> <p>De standaardwaarde is <span class="codeph"> midden </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T  </span> </p> </td> 
   <td colname="col2"> <p>tekstpositie </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentage van inzet in de component VideoPlayer voor het begin van de bijschrifttekst. </p> <p>De standaardwaarde is 0%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S  </span> </p> </td> 
   <td colname="col2"> <p>lijngrootte </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentage van videobreedte dat wordt gebruikt voor bijschriften. </p> <p>De standaardwaarde is 100%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L  </span> </p> </td> 
   <td colname="col2"> <p>lijnpositie </p> </td> 
   <td colname="col3"> <p> 0%-100%|geheel getal </p> </td> 
   <td colname="col4"> <p> Bepaalt de regelpositie op de pagina. </p> <p>Als de waarde wordt uitgedrukt als een geheel getal (geen procentteken), is dit het aantal regels vanaf de bovenkant waar de tekst wordt weergegeven. </p> <p>Als het een percentage is (het procentteken is het laatste teken), wordt de bijschrifttekst weergegeven met dat percentage in het weergavegebied. </p> <p>De standaardwaarde is 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

Andere WebVTT-functies in het WebVTT-bestand worden niet ondersteund, maar onderbreken de ondertiteling niet.

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file  </span> </span> </p> </td> 
   <td colname="col2"> <p> Hiermee wordt een URL of pad naar de WebVTT-bijschriftinhoud opgegeven. Geef het WebVTT-bestand door Beeldverwerking. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Geeft de standaardondertitelingsstatus aan (ingeschakeld is <span class="codeph"> 1 </span>). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

Geen.

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.caption.vtt,1
```


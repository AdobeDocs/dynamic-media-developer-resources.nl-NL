---
description: De hoofdweergave bestaat uit de afbeelding waarop kan worden ingezoomd.
solution: Experience Manager
title: Zoomweergave
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---


# Zoomweergave{#zoom-view}

De hoofdweergave bestaat uit de afbeelding waarop kan worden ingezoomd.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van het weergavegebied wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7basiczoomviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur in hexadecimale notatie van de hoofdweergave. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>De cursor wordt weergegeven over de hoofdweergave. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - om de hoofdweergave transparant te maken.

```
.s7basiczoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Op desktopsystemen ondersteunt de component de `cursortype`-kenmerkkiezer die op de klasse `.s7zoomview` kan worden toegepast en bestuurt het cursortype op basis van de componentstatus en gebruikersactie. De volgende `cursortype` waarden worden ondersteund:

<table id="table_BC9FC40DA27B4A85995F4E9431AABF33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Waarde </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default  </span> </p> </td> 
   <td colname="col2"> <p>Wordt weergegeven wanneer op de afbeelding niet kan worden ingezoomd vanwege een kleine afbeeldingsresolutie, componentinstellingen of beide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomine  </span> </p> </td> 
   <td colname="col2"> <p>Wordt weergegeven wanneer op de afbeelding kan worden ingezoomd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset  </span> </p> </td> 
   <td colname="col2"> <p>Wordt weergegeven wanneer de afbeelding op het maximale zoomniveau is en kan worden teruggezet op de oorspronkelijke toestand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slepen  </span> </p> </td> 
   <td colname="col2"> <p>Wordt weergegeven wanneer een gebruiker de afbeelding pant waarop is ingezoomd. </p> </td> 
  </tr> 
 </tbody> 
</table>


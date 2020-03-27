---
description: De hoofdweergave bestaat uit de afbeelding waarop kan worden ingezoomd.
seo-description: De hoofdweergave bestaat uit de afbeelding waarop kan worden ingezoomd.
seo-title: Zoomweergave
solution: Experience Manager
title: Zoomweergave
topic: Dynamic media
uuid: 34cb6c80-77eb-42b0-91dd-ae0369ea2881
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zoomweergave{#zoom-view}

De hoofdweergave bestaat uit de afbeelding waarop kan worden ingezoomd.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van het weergavegebied wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7zoomviewer .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Achtergrondkleur in hexadecimale notatie van de hoofdweergave. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>De cursor wordt weergegeven over de hoofdweergave. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voorbeeld - om de hoofdweergave transparant te maken.

```
.s7zoomviewer .s7zoomview { 
 background-color: transparent; 
}
```

Op desktopsystemen ondersteunt de component `cursortype` kenmerkkiezer die op de `.s7zoomview` klasse kan worden toegepast. Het controleert het type van de curseur die op componentenstaat en gebruikersactie wordt gebaseerd. De volgende `cursortype` waarden worden ondersteund:

* `default`

   Wordt weergegeven wanneer op de afbeelding niet kan worden ingezoomd vanwege een kleine afbeeldingsresolutie, componentinstellingen of beide.

* `zoomin`

   Wordt weergegeven wanneer op de afbeelding kan worden ingezoomd.

* `reset`

   Wordt weergegeven wanneer de afbeelding op het maximale zoomniveau is en kan worden teruggezet op de oorspronkelijke toestand.

* `drag`

   Wordt weergegeven wanneer de gebruiker de afbeelding pant die is ingezoomd.

* `slide`

   Wordt weergegeven wanneer de gebruiker de afbeelding omwisselt door een horizontale veegbeweging of tikbeweging uit te voeren.


---
description: In de modus voor ononderbroken zoomen bestaat de hoofdweergave uit een afbeelding waarop kan worden ingezoomd wanneer het huidige element één afbeelding is.
solution: Experience Manager
title: Zoomweergave
feature: Dynamic Media Classic,Viewers,SDK/API,Gemengde mediasets
role: Developer,Business Practitioner
exl-id: 0252436b-ba96-4273-b796-d1772fc093b0
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# Zoomweergave{#zoom-view}

In de modus voor ononderbroken zoomen bestaat de hoofdweergave uit een afbeelding waarop kan worden ingezoomd wanneer het huidige element één afbeelding is.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-eigenschappen van het hoofdviewergebied**

De vormgeving van het weergavegebied wordt bepaald door de volgende CSS-klassenkiezer:

```
.s7mixedmediaviewer .s7zoomview
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

Voorbeeld - om de zoomweergave transparant te maken.

```
.s7mixedmediaviewer .s7zoomview { 
 background-color: transparent; 
}
```

Op desktopsystemen ondersteunt de component `cursortype`-kenmerkkiezer die op de `.s7zoomview`-klasse kan worden toegepast. Het controleert het type van de curseur die op componentenstaat en gebruikersactie wordt gebaseerd. De volgende `cursortype` waarden worden ondersteund:

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

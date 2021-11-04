---
title: SocialShare.bearing
description: Configuration attribute for Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# SocialShare.bearing{#socialshare-bearing}

Configuration attribute for Smart Crop Video Viewer.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateraal</span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de richting van de dianavigatie voor de knoppencontainer. </p> <p> Wanneer ingesteld op <span class="codeph"> omhoog</span>, <span class="codeph"> omlaag</span>, <span class="codeph"> left</span>, of <span class="codeph"> right</span>wordt het deelvenster in een bepaalde richting weergegeven zonder dat er een extra controle op de grenzen plaatsvindt. Dit kan ertoe leiden dat het deelvenster door een buitencontainer wordt bijgesneden. </p> <p>Wanneer ingesteld op <span class="codeph"> verticaal passend</span>De component verschuift eerst de positie van het basisdeelvenster naar de onderkant van SocialShare en probeert het deelvenster van de onderkant, de rechterkant of de linkerkant van de basislocatie uit te rollen. Bij elke poging controleert de component of het deelvenster is bijgesneden door een buitencontainer. Als alle pogingen mislukken, probeert de component om de positie van het basispaneel naar de bovenkant te verschuiven en rollout pogingen in de bovenkant, de juiste, en linkerrichting te herhalen. </p> <p>Wanneer ingesteld op <span class="codeph"> monteerbaar</span>, gebruikt de component een vergelijkbare logica. Nochtans verschuift het basis eerst naar rechts, probeert het recht, onderaan, en omhoog rollout richtingen, en dan verschuift de basis naar links, probeert linker, onderaan, en omhoog rollout richtingen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f42369774e2740dcb399626a0e4e930e}

Optioneel.

## Standaard {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Voorbeeld {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```

---
description: Configuration attribute for Video360 Viewer.
seo-description: Configuration attribute for Video360 Viewer.
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic media
uuid: 43217e2e-71c5-4c58-94e0-c6ed38e25a5b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---


# SocialShare.bearing{#socialshare-bearing}

Configuration attribute for Video360 Viewer.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateraal</span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de richting van de dianavigatie voor de knoppencontainer. </p> <p> Wanneer ingesteld op <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span>, of <span class="codeph"> right</span>, rolt het paneel uit in een gespecificeerde richting zonder een extra grenscontrole, die in paneeluitknippen door een buitencontainer kan resulteren. </p> <p>Wanneer ingesteld op <span class="codeph"> fit-vertical</span>, verschuift de component eerst de positie van het basispaneel naar de bodem van SocialShare en probeert het paneel van de bodem, het recht, of verlaten van dergelijke basisplaats uit te rollen. Bij elke poging controleert de component of het deelvenster is bijgesneden door een buitencontainer. Als alle pogingen mislukken, probeert de component om de positie van het basispaneel naar de bovenkant te verschuiven en rollopouten in de bovenkant, de juiste, en linkerrichting te herhalen. </p> <p>Wanneer ingesteld op <span class="codeph"> fit-lateraal</span>, gebruikt de component een gelijkaardige logica. Nochtans verschuift het basis eerst naar rechts, probeert het recht, onderaan, en omhoog rollout richtingen, en dan verschuift de basis naar links, probeert linker, onderaan, en omhoog rollout richtingen. </p> </td> 
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


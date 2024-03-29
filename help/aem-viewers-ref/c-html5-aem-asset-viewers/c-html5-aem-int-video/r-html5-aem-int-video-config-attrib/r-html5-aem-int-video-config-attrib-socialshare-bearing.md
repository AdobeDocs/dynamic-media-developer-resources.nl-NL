---
title: SocialShare.bearing
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# SocialShare.bearing{#socialshare-bearing}

Configuration attribute for Interactive Video Viewer.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateraal</span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de richting van de dianavigatie voor de knoppencontainer. Wanneer ingesteld op <span class="codeph"> omhoog</span>, <span class="codeph"> omlaag</span>, <span class="codeph"> left</span>, of <span class="codeph"> right</span>, wordt het deelvenster in de opgegeven richting uitgelijnd zonder extra controle van de grenzen. Dit kan ertoe leiden dat het deelvenster wordt bijgesneden door een buitencontainer. </p> <p>Wanneer ingesteld op <span class="codeph"> verticaal passend</span>, verschuift de component eerst de positie van het basispaneel naar de onderkant van SocialShare. Vervolgens wordt geprobeerd het deelvenster in een van de volgende richtingen vanuit een dergelijke basislocatie uit te rollen: onder, rechts, links. Bij elke poging controleert de component of het deelvenster is bijgesneden door een buitencontainer. Als alle pogingen mislukken, probeert de component om de positie van het basispaneel naar de bovenkant te verschuiven en herhaalt de rollout pogingen van een bovenkant, juist, en linkerrichting. </p> <p>Wanneer ingesteld op <span class="codeph"> monteerbaar</span>, gebruikt de component een gelijkaardige logica, maar verschuift de basis naar het recht eerst, probeert recht, onderaan, en omhoog rollout richtingen. Vervolgens verschuift het de basis naar links, waarbij de rollout-richting naar links, omlaag en omhoog wordt geprobeerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-1e637b22e8a44d759d588e47576891e6}

Optioneel.

## Standaard {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## Voorbeeld {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```

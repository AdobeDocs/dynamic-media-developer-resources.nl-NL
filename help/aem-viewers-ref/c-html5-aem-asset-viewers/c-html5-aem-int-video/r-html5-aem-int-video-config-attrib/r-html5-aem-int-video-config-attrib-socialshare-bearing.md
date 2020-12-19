---
description: Configuration attribute for Interactive Video Viewer.
seo-description: Configuration attribute for Interactive Video Viewer.
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic media
uuid: b3978280-7826-44c0-bd25-357e145121f8
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---


# SocialShare.bearing{#socialshare-bearing}

Configuration attribute for Interactive Video Viewer.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateraal</span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de richting van de dianavigatie voor de knoppencontainer. Wanneer ingesteld op <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span>, of <span class="codeph"> right</span>, rolt het paneel uit in de gespecificeerde richting zonder enige extra grenzen het controleren, die in het paneel kan resulteren dat door een buitencontainer wordt geknipt. </p> <p>Wanneer ingesteld op <span class="codeph"> fit-vertical</span>, verplaatst de component eerst de positie van het basispaneel naar de bodem van SocialShare en probeert het paneel in één van de volgende richtingen van zulk een basisplaats uit te rollen: onder, rechts, links. Bij elke poging controleert de component of het deelvenster is bijgesneden door een buitencontainer. Als alle pogingen mislukken, probeert de component om de positie van het basispaneel naar de bovenkant te verschuiven en herhaalt de uitrolpogingen van een bovenkant, juiste, en linkerrichting. </p> <p>Wanneer ingesteld op <span class="codeph"> fit-lateraal</span>, gebruikt de component een gelijkaardige logica, maar verschuift de basis eerst naar rechts, die recht probeert, onderaan, en omhoog roloutrichtingen. Vervolgens verschuift het de basis naar links, waarbij de rollout-richting naar links, omlaag en omhoog wordt geprobeerd. </p> </td> 
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


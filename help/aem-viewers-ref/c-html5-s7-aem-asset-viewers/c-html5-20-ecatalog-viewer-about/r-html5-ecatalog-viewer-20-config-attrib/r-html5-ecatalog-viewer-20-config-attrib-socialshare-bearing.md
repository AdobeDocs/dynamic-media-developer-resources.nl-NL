---
title: SocialShare.bearing
description: SocialShare.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateraal </span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de richting van de dianavigatie voor de knoppencontainer. </p> <p> Wanneer ingesteld op <span class="codeph"> omhoog </span>, <span class="codeph"> omlaag </span>, <span class="codeph"> left </span>, of <span class="codeph"> right </span>, wordt het deelvenster in een opgegeven richting weergegeven zonder dat er een extra grenscontrole wordt uitgevoerd. Dit gedrag kan ertoe leiden dat het deelvenster wordt bijgesneden door een buitencontainer. </p> <p>Wanneer ingesteld op <span class="codeph"> verticaal passend </span>De component verschuift eerst de positie van het basisdeelvenster naar de onderkant van SocialShare en probeert het deelvenster vanaf de onderkant, rechts of links uit te rollen. Bij elke poging controleert de component of het deelvenster is bijgesneden door een buitencontainer. Als alle pogingen mislukken, probeert de component om de positie van het basispaneel naar de bovenkant te verschuiven en de rollout pogingen van de bovenkant, juiste, en linkerrichting te herhalen. </p> <p>Wanneer ingesteld op <span class="codeph"> monteerbaar </span>, gebruikt de component een zelfde logica zoals met fit-vertical. Nochtans, verschuift het de basis naar het juiste eerste-proberen recht, onderaan, en omhoog rolt richtingen-en dan verschuift de basis naar links, het proberen van links, onderaan, en omhoog rollout richtingen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-8e843b967237426e9a8b3cd0f27b9820}

Optioneel.

## Standaard {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Voorbeeld {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`

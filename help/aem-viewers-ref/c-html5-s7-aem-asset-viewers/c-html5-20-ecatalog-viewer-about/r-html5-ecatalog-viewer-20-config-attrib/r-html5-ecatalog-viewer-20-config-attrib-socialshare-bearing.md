---
description: 'null'
seo-description: 'null'
seo-title: SocialShare.iling
solution: Experience Manager
title: SocialShare.iling
topic: Dynamic media
uuid: e48b39bb-c23d-42ce-9dc6-6e8b0d9b04ea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SocialShare.iling{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateraal </span> </p> </td> 
   <td colname="col2"> <p> Hiermee bepaalt u de richting van de dianavigatie voor de knoppencontainer. </p> <p> Wanneer het deelvenster is ingesteld op <span class="codeph"> Omhoog </span>, <span class="codeph"> Omlaag </span>, <span class="codeph"> Links </span>of <span class="codeph"> rechts </span>, wordt het in een opgegeven richting weergegeven zonder dat er een extra grenscontrole wordt uitgevoerd. Dit gedrag kan ertoe leiden dat het deelvenster wordt bijgesneden door een buitencontainer. </p> <p>Wanneer ingesteld op <span class="codeph"> passend maken-verticaal </span>, verschuift de component eerst de positie van het basisdeelvenster naar de onderkant van SocialShare en probeert u het deelvenster vanaf de onderkant, rechts of links uit te rollen. Bij elke poging controleert de component of het deelvenster is bijgesneden door een buitencontainer. Als alle pogingen mislukken, probeert de component om de positie van het basispaneel naar de bovenkant te verschuiven en de uitrolpogingen van de bovenkant, juiste, en linkerrichting te herhalen. </p> <p>Wanneer geplaatst aan <span class="codeph"> zijkant </span>, gebruikt de component een gelijkaardige logica zoals met fit-verticaal, maar in plaats daarvan verschuift de basis naar het recht eerste-proberen recht, onderaan, en omhoog rolt richtingen-en dan verschuift de basis naar links, het proberen links, onderaan, en omhoog rolt richtingen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-8e843b967237426e9a8b3cd0f27b9820}

Optioneel.

## Standaard {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Voorbeeld {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`

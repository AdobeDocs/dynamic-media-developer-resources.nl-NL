---
description: ruwheid van het materiaaloppervlak. Hiermee bepaalt u de relatieve ruwheid van het materiaaloppervlak.
seo-description: ruwheid van het materiaaloppervlak. Hiermee bepaalt u de relatieve ruwheid van het materiaaloppervlak.
seo-title: ruw
solution: Experience Manager
title: ruw
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d3b4ece1-cc2a-4012-ad81-2f313d3a370b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---


# grof{#rough}

ruwheid van het materiaaloppervlak. Hiermee bepaalt u de relatieve ruwheid van het materiaaloppervlak.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Oppervlakruwheid (0...100 percenten) of -1 om de standaardruwheid te selecteren. </p> </td> 
 </tr> 
</table>

Wordt gebruikt om het 3D-spiegelrendereffect te bepalen. Lagere waarden voor ruwheid produceren doorgaans vloeiender reflectie-effecten. Bij hogere waarden wordt de gereflecteerde afbeelding gerandomiseerd en verspreid.

Elk materiaaltype ( `type=`) bepaalt een minimum en een maximumreflectie teruggeeft effect dat op ruwheid wordt gebaseerd. Voor sommige materiaalsoorten (bijvoorbeeld wandpapier) heeft `rough=` nauwelijks invloed op het uiterlijk van de reflectie, terwijl voor andere materiaalsoorten (bijvoorbeeld steen of keramiek) het effect aanzienlijk groter is.

`rough=-1` stelt de ruwheid in op een server-interne standaardwaarde (40% voor typische materiaaltypen).

## Eigenschappen {#section-515375758b254c80af576271bdb61bb8}

Materiaalkenmerk. Genegeerd als het vignet geen 3D-reflectiemogelijkheid heeft, als er geen 3D-geometrie aan het doelobject is gekoppeld of als het doelobject geen andere objecten in de scène spiegelt.

## Standaard {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` als het materiaal op een catalogusvermelding is gebaseerd, anders ongeveer 40%.

## Zie ook {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) ,  [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)

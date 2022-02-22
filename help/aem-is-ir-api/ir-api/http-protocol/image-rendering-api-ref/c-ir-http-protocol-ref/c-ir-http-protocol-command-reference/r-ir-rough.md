---
title: ruw
description: ruwheid van het materiaaloppervlak. Hiermee bepaalt u de relatieve ruwheid van het materiaaloppervlak.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# ruw{#rough}

ruwheid van het materiaaloppervlak. Hiermee bepaalt u de relatieve ruwheid van het materiaaloppervlak.

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Oppervlakruwheid (0...100 percenten) of -1 om de standaardruwheid te selecteren. </p> </td> 
 </tr> 
</table>

Wordt gebruikt om het 3D-spiegelrendereffect te bepalen. Lagere waarden voor ruwheid produceren doorgaans vloeiender reflectie-effecten. Bij hogere waarden wordt de gereflecteerde afbeelding gerandomiseerd en verspreid.

Elk materiaaltype ( `type=`) definieert een minimum- en een maximumrendereffect voor spiegeling op basis van ruwheid. Voor sommige materiaalsoorten (bijvoorbeeld wandpapier): `rough=` heeft een minimale invloed op het uiterlijk van de reflectie, terwijl het effect voor andere materiaalsoorten (bijvoorbeeld steen of keramiek) aanzienlijk groter is.

`rough=-1` Stelt de ruwheid in op een server-interne standaardwaarde (40% voor typische materiaaltypen).

## Eigenschappen {#section-515375758b254c80af576271bdb61bb8}

Materiaalkenmerk. Genegeerd als het vignet geen 3D-reflectiemogelijkheid heeft, als er geen 3D-geometrie aan het doelobject is gekoppeld of als het doelobject geen andere objecten in de scène spiegelt.

## Standaard {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` Als het materiaal op een catalogusingang gebaseerd is, anders ongeveer 40%.

## Zie ook {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)

---
title: illusie
description: Selector van belichtingskaart. Geeft de belichtingsafbeelding aan waarmee dit materiaal liever wordt gerenderd.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e1af2397-8eae-4b77-abb1-61ba8cb866f3
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# illusie{#illum}

Selector van belichtingskaart. Geeft de belichtingsafbeelding aan waarmee dit materiaal liever wordt gerenderd.

`illum=-1|0|1|2`

Als de opgegeven verlichtingskaart niet beschikbaar is in het doelvignet, wordt in plaats daarvan de dichtstbijzijnde beschikbare kaart gebruikt.

`illum=-1` Hiermee wordt opgegeven dat de verlichtingsafbeelding automatisch wordt geselecteerd op basis van de optie `gloss=` waarde.

## Eigenschappen {#section-aace8466566e4cf1a0c5a6c0167245c9}

Materiaalkenmerk. Genegeerd als in het vignet geen meerdere verlichtingstoewijzingen zijn gedefinieerd.

## Standaard {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Zie ook {#section-9132e60381c64aa3a8ed1319690db55e}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)

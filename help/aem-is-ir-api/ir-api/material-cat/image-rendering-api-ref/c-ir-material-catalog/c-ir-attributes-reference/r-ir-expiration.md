---
description: De standaardtijd voor de clientcache om te live gaan. Verstrekt een standaardvervalinterval voor het geval dat een bepaalde catalogusverslag geen geldige catalogusVervalwaarde of waarde van de Vervaldatum van het vignet bevat, of als een vignetdossier of materiaaldossier direct, eerder dan via een catalogusverslag wordt betreden.
solution: Experience Manager
title: Verlopen
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Vervaldatum{#expiration}

De standaardtijd voor de clientcache om te live gaan. Verstrekt een standaardvervalinterval voor het geval dat een bepaalde catalogusverslag geen geldige catalogus bevat::Vervaldatum of vignet::De waarde van de Vervalsing, of als een vignetdossier of een materiaaldossier direct, eerder dan via een catalogusverslag wordt betreden.

## Eigenschappen {#section-8e2bade105ec4905ae5c4911f500279f}

Reëel getal, 0 of hoger. Aantal uren tot het verstrijken van de antwoordgegevens. Reeks aan 0 om altijd het antwoordbeeld onmiddellijk te verlopen, dat effectief cliënt caching onbruikbaar maakt. Stel de waarde in op -1 om te markeren als *never expired*.

## Standaard {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Overgenomen van standaard::Verlopen indien niet gedefinieerd of indien leeg.

## Zie ook {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalogus::Verlopen](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ,  [vignet::Verlopen](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)

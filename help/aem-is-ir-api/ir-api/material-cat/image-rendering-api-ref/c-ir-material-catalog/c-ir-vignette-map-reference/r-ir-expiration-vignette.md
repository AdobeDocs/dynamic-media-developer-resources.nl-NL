---
description: Cachetijd client om te live gaan. Aantal uren tot vervaldatum. Wordt gebruikt om client- en proxyserver-caching te beheren.
solution: Experience Manager
title: Verlopen
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# Vervaldatum{#expiration}

Cachetijd client om te live gaan. Aantal uren tot vervaldatum. Wordt gebruikt om client- en proxyserver-caching te beheren.

Zie ` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)` voor meer informatie.

## Eigenschappen {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Reëel getal, -2, -1, 0 of hoger. Aantal uren tot aan het verstrijken van de responsimage. Stel de waarde in op 0 om de reactie-afbeelding altijd onmiddellijk te laten verlopen. Hierdoor wordt het in cache plaatsen van clients uitgeschakeld. Ingesteld op -1 om te markeren als `never expire`; in dit geval retourneert de server altijd 403 status als reactie op voorwaardelijke `GET`-aanvragen zonder te controleren of het bestand daadwerkelijk is gewijzigd. Stel de waarde in op -2 om de standaardinstelling van `attribute::Expiration` te gebruiken.

## Standaard {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` wordt gebruikt als het veld niet aanwezig is, als de waarde -2 is of als het veld leeg is.

## Zie ook {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)

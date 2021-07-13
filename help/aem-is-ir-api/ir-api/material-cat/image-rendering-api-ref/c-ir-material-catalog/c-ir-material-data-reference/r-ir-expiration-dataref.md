---
description: Cachetijd client om te live gaan. Aantal uren tot vervaldatum. Wordt gebruikt om client- en proxyserver-caching te beheren.
solution: Experience Manager
title: Verlopen
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Verlopen{#expiration}

Cachetijd client om te live gaan. Aantal uren tot vervaldatum. Wordt gebruikt om client- en proxyserver-caching te beheren.

De server berekent de vervaltijd/de datum van de NTTP reactiegegevens door deze waarde aan de tijd/de datum van transmissie toe te voegen.

Browsers beheren caches met de vervaltijden van bestanden. Voordat een aanvraag aan de server wordt doorgegeven, controleert de browser de cache om te controleren of het bestand al is gedownload. Als dat het geval is en als het bestand nog niet is verlopen, verzendt de browser een voorwaardelijke aanvraag (bijvoorbeeld met de if-Modified-Since HTTP-aanvraagheader) in plaats van een normale GET. De server heeft de mogelijkheid om te reageren met de status &#39;304&#39; en de afbeelding niet te verzenden. De browser laadt het bestand vervolgens uit de cache. Dit kan de algemene prestaties voor vaak toegankelijke gegevens aanzienlijk verhogen.

De server stelt de header van de HTTP-reactie voor verlopen in op de huidige datum/tijd plus het kleinste vignet::Verlopen en alle catalogus::Vervalwaarden voor het vignet en alle materialen die bij de renderbewerking zijn betrokken.

De vervaldatum wordt voornamelijk ingesteld voor reacties op afbeeldingsgegevens. Bepaalde typen reacties worden altijd gemarkeerd voor onmiddellijke vervaldatum (of gecodeerd als niet-cachebaar), inclusief alle reacties op fouten of reacties op eigenschappen.

## Eigenschappen {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

Reëel getal, -2, -1, 0 of hoger. Aantal uren tot aan het verstrijken van de responsimage. Stel de waarde in op 0 om de reactie-afbeelding altijd onmiddellijk te laten verlopen. Hierdoor wordt het in cache plaatsen van clients uitgeschakeld. Ingesteld op -1 om te markeren als `never expire`. In dit geval retourneert de server altijd de 304-status (niet gewijzigd) als reactie op voorwaardelijke `GET`-aanvragen zonder te controleren of het bestand daadwerkelijk is gewijzigd. Stel de waarde in op -2 om de standaardinstelling van `attribute::Expiration` te gebruiken.

## Standaard {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` wordt gebruikt als het veld niet aanwezig is, als de waarde -2 is of als het veld leeg is.

## Zie ook {#section-9d46a9d346fe42f3911edb3bd79f4121}

[kenmerk::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [vignet::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)

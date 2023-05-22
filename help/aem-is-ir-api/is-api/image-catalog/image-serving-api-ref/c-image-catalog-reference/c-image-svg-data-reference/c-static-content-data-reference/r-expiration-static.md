---
description: Verlopen
solution: Experience Manager
title: Verlopen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 064dab12-5f58-4e19-a6b1-fbd20182e3aa
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Verlopen{#expiration}

Wordt gebruikt om client- en proxyserver-caching te beheren. De server berekent de vervaltijd/datum van de HTTP-responsgegevens door deze waarde toe te voegen aan de tijd/datum van de verzending.

Browsers beheren caches met de vervaltijden van bestanden. Voordat een aanvraag aan de server wordt doorgegeven, controleert de browser of het bestand al is gedownload. Als dat het geval is en als het bestand nog niet is verlopen, verzendt de browser een voorwaardelijk verzoek (bijvoorbeeld met het veld Indien-Gewijzigd-Sinds ingesteld in de aanvraagkoptekst) in plaats van een normale GET-aanvraag. De server heeft de mogelijkheid om te reageren met de status &#39;304&#39; en de afbeelding niet te verzenden. De browser laadt het bestand vervolgens uit de cache. Dit kan de algemene prestaties voor vaak toegankelijke gegevens aanzienlijk verhogen.

Verlopen wordt gebruikt voor deze responstypen:

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

Bepaalde typen reacties (bijvoorbeeld reacties op fouten) worden altijd gemarkeerd voor directe vervaldatum (of gecodeerd als niet-cachebaar), terwijl andere (bijvoorbeeld eigenschappen of standaardafbeeldingsreacties) speciale vervalinstellingen gebruiken ( `attribute::NonImgExpiration` en `attribute::DefaultExpiration`).

## Eigenschappen {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

Reëel getal, -2, -1 of 0 of hoger. Aantal uren tot aan het verstrijken van de responsimage. Reeks aan 0 om altijd het antwoordbeeld onmiddellijk te verlopen, dat effectief cliënt caching onbruikbaar maakt. Instellen op -1 om te markeren als *`never expire`*. In dit geval retourneert de server altijd de 304-status (niet gewijzigd) als reactie op voorwaardelijke GET-aanvragen, zonder te controleren of het bestand daadwerkelijk is gewijzigd. Stel in op -2 om de standaardinstelling te gebruiken die wordt geboden door `attribute::Expiration`.

## Standaard {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` wordt gebruikt als het veld niet aanwezig is, als de waarde -2 is of als het veld leeg is.

## Zie ook {#section-0e5e8595aad641c689726828712a8902}

[kenmerk::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7), [kenmerk::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [kenmerk::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d), [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)

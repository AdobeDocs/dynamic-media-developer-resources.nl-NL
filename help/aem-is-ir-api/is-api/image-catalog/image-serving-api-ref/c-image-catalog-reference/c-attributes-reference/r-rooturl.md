---
description: URL van hoofdmap voor relatieve afbeeldings-URL's. Hiermee geeft u de basis-URL op voor relatieve afbeeldings-URL's.
solution: Experience Manager
title: RootUrl
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72560180-53e5-4293-9dd3-c0cd196551dc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# RootUrl{#rooturl}

URL van hoofdmap voor relatieve afbeeldings-URL&#39;s. Hiermee geeft u de basis-URL op voor relatieve afbeeldings-URL&#39;s.

`attribute::RootUrl` wordt gebruikt in plaats van `attribute::RootPath` wanneer een `src=` of `mask=` De waarde wordt ingesloten door {accolades} of (ronde haakjes).

## Eigenschappen {#section-fe02269b4b724319a5d1f2cfcae31cba}

Tekstreeks. Absoluut URL-hoofdpad, inclusief de id van het voorafgaande protocol. De volgende protocollen worden ondersteund: HTTP, HTTPS en FTP.

## Standaard {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

Overgenomen van `default::RootUrl` indien niet gedefinieerd. Indien gedefinieerd maar leeg, worden relatieve URL&#39;s niet ondersteund door deze afbeeldingscatalogus.

## Zie ook {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [kenmerk:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [ruleset:PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)

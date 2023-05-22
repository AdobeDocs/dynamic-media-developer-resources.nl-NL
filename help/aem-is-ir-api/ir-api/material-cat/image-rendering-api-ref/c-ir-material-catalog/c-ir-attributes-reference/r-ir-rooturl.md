---
title: RootUrl
description: URL van hoofdmap voor relatieve afbeeldings-URL's. Hiermee geeft u de basis-URL op voor relatieve afbeeldings-URL's.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# RootUrl{#rooturl}

URL van hoofdmap voor relatieve afbeeldings-URL&#39;s. Hiermee geeft u de basis-URL op voor relatieve afbeeldings-URL&#39;s. De`attribute::RootUrl` wordt gebruikt in plaats van `attribute::RootPath` wanneer een `src=` value is enclosed by { curly braces }.

## Eigenschappen {#section-69cd0f71ea614770a8778c745d23197a}

Tekstreeks. Absoluut URL-hoofdpad, inclusief de id van het voorafgaande protocol. De volgende protocollen worden ondersteund: HTTP, HTTPS en FTP.

## Standaard {#section-7a81569728474725a70f3a2cc4d48e85}

Overgenomen van `default::RootUrl` indien niet gedefinieerd. Indien gedefinieerd maar leeg, worden relatieve URL&#39;s niet ondersteund door deze materiaalcatalogus.

## Zie ook {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [kenmerk:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)

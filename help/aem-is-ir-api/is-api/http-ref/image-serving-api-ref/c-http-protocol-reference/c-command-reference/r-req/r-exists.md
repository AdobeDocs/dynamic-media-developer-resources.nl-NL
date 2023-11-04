---
description: Afbeelding bestaat.
solution: Experience Manager
title: exists
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# exists{#exists}

Afbeelding bestaat.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* unieke aanvraag-id

Retourneert één benoemde eigenschap `catalogRecord.exists`. De eigenschapswaarde wordt ingesteld op &quot;1&quot; als het opgegeven catalogusitem voorkomt in de afbeelding of de standaardcatalogus. Als dit niet het geval is, wordt het item ingesteld op &quot;0&quot;. `req=exists` verzoeken tegen de `/is/content` context geeft aan of een opgegeven record al dan niet aanwezig is in de statische inhoudscatalogus.

Andere opdrachten in de tekenreeks request worden genegeerd. De HTTP-respons is cacheable met de TTL op basis van `attribute::NonImgExpiration`.

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. Standaard is `s7jsonResponse`.

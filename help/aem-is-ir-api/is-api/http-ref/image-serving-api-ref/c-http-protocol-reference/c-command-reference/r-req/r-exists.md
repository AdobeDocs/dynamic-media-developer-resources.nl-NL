---
description: Afbeelding bestaat.
seo-description: Afbeelding bestaat.
seo-title: exists
solution: Experience Manager
title: exists
topic: Scene7 Image Serving - Image Rendering API
uuid: 5490e4c7-b52a-4b2e-b002-34afaa242c08
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# exists{#exists}

Afbeelding bestaat.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* unieke aanvraag-id

Retourneert één eigenschap met de naam `catalogRecord.exists`. De eigenschapswaarde wordt ingesteld op &quot;1&quot; als het opgegeven catalogusitem voorkomt in de afbeelding of de standaardcatalogus. Als dit niet het geval is, wordt het item ingesteld op &quot;0&quot;. `req=exists` in verzoeken over de `/is/content` context wordt aangegeven of een opgegeven record al dan niet aanwezig is in de statische inhoudscatalogus.

Andere opdrachten in de tekenreeks request worden genegeerd. De reactie van HTTP is cacheable met TTL gebaseerd op `attribute::NonImgExpiration`.

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. Standaard is dit `s7jsonResponse`.

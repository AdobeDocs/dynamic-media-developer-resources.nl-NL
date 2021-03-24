---
description: Afbeelding bestaat.
solution: Experience Manager
title: exists
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# exists{#exists}

Afbeelding bestaat.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* unieke aanvraag-id

Retourneert één eigenschap met de naam `catalogRecord.exists`. De eigenschapswaarde wordt ingesteld op &quot;1&quot; als het opgegeven catalogusitem voorkomt in de afbeelding of de standaardcatalogus. Als dit niet het geval is, wordt het item ingesteld op &quot;0&quot;. `req=exists` in verzoeken over de  `/is/content` context wordt aangegeven of een opgegeven record al dan niet aanwezig is in de statische inhoudscatalogus.

Andere opdrachten in de tekenreeks request worden genegeerd. De reactie van HTTP is cacheable met TTL die op `attribute::NonImgExpiration` wordt gebaseerd.

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. De standaardwaarde is `s7jsonResponse`.

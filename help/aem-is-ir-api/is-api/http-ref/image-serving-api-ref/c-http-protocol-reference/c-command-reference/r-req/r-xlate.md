---
description: Beschikbare landspecifieke versies. Retourneert een lijst met beschikbare landspecifieke versies van de catalogus-id die is opgegeven in het aanvraagpad.
seo-description: Beschikbare landspecifieke versies. Retourneert een lijst met beschikbare landspecifieke versies van de catalogus-id die is opgegeven in het aanvraagpad.
seo-title: xlate
solution: Experience Manager
title: xlate
topic: Scene7 Image Serving - Image Rendering API
uuid: 4c2370e5-1d46-4242-89bb-a5ce416ef63c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---


# xlate{#xlate}

Beschikbare landspecifieke versies. Retourneert een lijst met beschikbare landspecifieke versies van de catalogus-id die is opgegeven in het aanvraagpad.

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Unieke aanvraag-id. </p></td> 
 </tr> 
</table>

Zie [Vertaling van object-id](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414).

Bijvoorbeeld:

`xlate.translatedIds=image,image_fr,image_de`

De reactie van HTTP is cacheable met TTL die op `catalog::Expiration` wordt gebaseerd.

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. De standaardwaarde is `s7jsonResponse`.

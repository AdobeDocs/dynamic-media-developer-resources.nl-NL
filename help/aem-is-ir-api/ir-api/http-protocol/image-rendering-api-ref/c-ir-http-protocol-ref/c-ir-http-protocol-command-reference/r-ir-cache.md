---
title: cachegeheugen
description: Cachebeheer. Hiermee wordt het selectief uitschakelen van caching op de client (browser, proxyservers, netwerkcaching-systemen) en het in cache plaatsen op de interne [!DNL Platform Server] cache.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# cachegeheugen {#cache}

Cachebeheer. Hiermee kunt u het in cache plaatsen op de client (browser, proxyservers, systemen voor het in cache plaatsen van netwerken) en het in cache plaatsen van items op de interne server selectief uitschakelen [!DNL Platform Server] cache.

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>op | korting | validate </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>op | korting </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>op | korting </p></td> 
 </tr> 
</table>

Als slechts één *`cacheControl`* waarde wordt opgegeven, wordt deze toegepast op zowel client- als servercache.

De &#39; `validate`Met het trefwoord &#39; kunnen vermeldingen in de servercache worden bijgewerkt nadat structuur- of vignetbestanden zijn gewijzigd, zonder dat de cachegegevens hoeven te worden afgewacht totdat de ingevoerde gegevens automatisch verlopen. Het in cache plaatsen van clients wordt niet beïnvloed door deze opdracht.

Indien opgegeven in een geneste aanvraag, `cache=on` maakt het mogelijk de afbeelding die door de geneste aanvraag wordt gegenereerd, permanent in cache op de server te plaatsen. Zorg ervoor dat u caching voor genestelde verzoeken slechts toelaat wanneer het zelfde genestelde verzoek herhaaldelijk met de zelfde parameters wordt geroepen.

## Eigenschappen {#section-0dcbd62e1122400e8c347f408f2d937e}

Kan overal in het verzoek voorkomen. Genegeerd wanneer het verzoek geen antwoordbeeld terugkeert. De eigenschap *`clientControl`* wordt genegeerd wanneer caching op de client is uitgeschakeld door de materiaalcatalogus (als `attribute::Expiration` heeft een negatieve waarde). De eigenschap *`serverControl`* wordt genegeerd als het in cache plaatsen van servers is uitgeschakeld ( `PlatformServer::cache.enable`).

## Standaard {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` Voor HTTP-aanvragen `cache=off` voor geneste/ingesloten aanvragen.

## Zie ook {#section-2f5853751dab49579e97418fa766bdf9}

[catalogus::Verlopen](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)

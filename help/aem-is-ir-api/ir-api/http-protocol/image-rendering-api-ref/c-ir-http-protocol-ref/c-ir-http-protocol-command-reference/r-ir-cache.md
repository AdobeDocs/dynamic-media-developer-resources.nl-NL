---
description: Cachebeheer. Staat selectief toe onbruikbaar makend cliënt-zijcaching (browser, volmachtsservers, netwerk caching systemen) en caching in het interne geheime voorgeheugen van de Server van het Platform.
seo-description: Cachebeheer. Staat selectief toe onbruikbaar makend cliënt-zijcaching (browser, volmachtsservers, netwerk caching systemen) en caching in het interne geheime voorgeheugen van de Server van het Platform.
seo-title: cachegeheugen
solution: Experience Manager
title: cachegeheugen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8af89b67-39d5-43e5-a58d-2cd509a1e373
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---


# cache{#cache}

Cachebeheer. Staat selectief toe onbruikbaar makend cliënt-zijcaching (browser, volmachtsservers, netwerk caching systemen) en caching in het interne geheime voorgeheugen van de Server van het Platform.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControllerServerControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>op | korting | validate </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl  </span> </p> </td> 
  <td class="stentry"> <p>op | korting </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl  </span> </p></td> 
  <td class="stentry"> <p>op | korting </p></td> 
 </tr> 
</table>

Als slechts één *`cacheControl`* waarde wordt gespecificeerd, wordt het toegepast op zowel cliënt als servergeheime voorgeheugens.

Met het trefwoord &#39; `validate`&#39; kunnen vermeldingen in de servercache worden bijgewerkt nadat de structuur- of vignetbestanden zijn gewijzigd, zonder dat de cachegegevens automatisch hoeven te worden verlopen. Het in cache plaatsen van clients wordt niet beïnvloed door deze opdracht.

Als `cache=on` in een geneste aanvraag wordt opgegeven, wordt de afbeelding die door de geneste aanvraag wordt gegenereerd, permanent in cache op de server geplaatst. Zorg ervoor dat caching alleen mogelijk is voor geneste aanvragen wanneer hetzelfde geneste verzoek herhaaldelijk moet worden aangeroepen met exact dezelfde parameters.

## Eigenschappen {#section-0dcbd62e1122400e8c347f408f2d937e}

Kan overal in het verzoek voorkomen. Genegeerd wanneer het verzoek geen antwoordbeeld terugkeert. *`clientControl`* wordt genegeerd wanneer caching aan de clientzijde door de materiaalcatalogus wordt uitgeschakeld (als  `attribute::Expiration` een negatieve waarde heeft). *`serverControl`* wordt genegeerd als het in cache plaatsen van servers is uitgeschakeld (  `PlatformServer::cache.enable`).

## Standaard {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` voor HTTP-aanvragen,  `cache=off` voor geneste/ingesloten aanvragen.

## Zie ook {#section-2f5853751dab49579e97418fa766bdf9}

[catalogus::Verlopen](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)

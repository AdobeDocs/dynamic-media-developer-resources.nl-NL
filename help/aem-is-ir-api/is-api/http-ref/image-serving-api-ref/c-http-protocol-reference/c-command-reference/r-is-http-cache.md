---
description: Cachebeheer. Staat selectief toe onbruikbaar makend cliënt-zijcaching (browser, volmachtsservers, netwerk caching systemen) en caching in het interne geheime voorgeheugen van de Server van het Platform.
seo-description: Cachebeheer. Staat selectief toe onbruikbaar makend cliënt-zijcaching (browser, volmachtsservers, netwerk caching systemen) en caching in het interne geheime voorgeheugen van de Server van het Platform.
seo-title: cachegeheugen
solution: Experience Manager
title: cachegeheugen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 08f4e4d0-0f7d-48fe-956c-284af97c902e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---


# cache{#cache}

Cachebeheer. Staat selectief toe onbruikbaar makend cliënt-zijcaching (browser, volmachtsservers, netwerk caching systemen) en caching in het interne geheime voorgeheugen van de Server van het Platform.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControllerServerControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off|validate|update</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

Als slechts één `*`cacheControl`*` waarde wordt gespecificeerd, wordt het toegepast op zowel cliënt als servergeheime voorgeheugens.

Met het trefwoord `validate` kunt u cachemaringangen bijwerken nadat afbeeldingsbestanden zijn gewijzigd, zonder dat u hoeft te wachten tot de cachevermelding automatisch verloopt. Het in cache plaatsen van clients wordt niet beïnvloed door deze opdracht.

Met het trefwoord `update` kunt u het bijwerken van cachemarkeringen op de server forceren. Dit is handig nadat bronnen zijn gewijzigd die niet rechtstreeks worden bijgehouden door het mechanisme voor cachevalidatie, bijvoorbeeld wanneer een lettertypebestand wordt gewijzigd zonder de bestandsnaam of de bijbehorende lettertype-id te wijzigen.

Als `cache=on` in een geneste aanvraag wordt opgegeven, wordt de afbeelding die door de geneste aanvraag wordt gegenereerd, permanent in cache op de server geplaatst. Zorg ervoor dat caching alleen mogelijk is voor geneste aanvragen wanneer hetzelfde geneste verzoek herhaaldelijk moet worden aangeroepen met exact dezelfde parameters.

## Eigenschappen {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Request-kenmerk. Ongeacht de huidige laaginstelling. Genegeerd wanneer het verzoek geen antwoordbeeld terugkeert. *`clientControl`*wordt genegeerd wanneer het in cache plaatsen op de client door de afbeeldingscatalogus wordt uitgeschakeld (als `catalog::Expiration` een negatieve waarde heeft).

Cachebeheer op de client-side ( `on` en `off` alleen) is ook beschikbaar voor aanvragen voor statische inhoud op [!DNL /is/content/].

## Standaard {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` voor HTTP-aanvragen,  `cache=off` voor geneste/ingesloten aanvragen,  `cache=on` voor statische inhoudsaanvragen.

## Zie ook {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalogus::Verlopen](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)

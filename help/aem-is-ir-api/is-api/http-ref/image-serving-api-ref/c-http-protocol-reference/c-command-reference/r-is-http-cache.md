---
description: Cachebeheer. Hiermee wordt het selectief uitschakelen van caching op de client (browser, proxyservers, netwerkcaching-systemen) en het in cache plaatsen op de interne [!DNL Platform Server] cache.
solution: Experience Manager
title: cachegeheugen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# cachegeheugen{#cache}

Cachebeheer. Hiermee wordt het selectief uitschakelen van caching op de client (browser, proxyservers, netwerkcaching-systemen) en het in cache plaatsen op de interne [!DNL Platform Server] cache.

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

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

Als slechts één `*`cacheControl`*` waarde wordt opgegeven, wordt deze toegepast op zowel client- als servercache.

De `validate` met trefwoorden kunnen cachemarangen worden bijgewerkt nadat afbeeldingsbestanden zijn gewijzigd, zonder dat hoeft te worden gewacht tot de cachegegevens automatisch verlopen. Het in cache plaatsen van clients wordt niet beïnvloed door deze opdracht.

De `update` het sleutelwoord kan worden gebruikt om het bijwerken server-zijgeheim voorgeheugeningangen te dwingen. Dit is handig nadat bronnen zijn gewijzigd die niet rechtstreeks worden bijgehouden door het mechanisme voor cachevalidatie, bijvoorbeeld wanneer een lettertypebestand wordt gewijzigd zonder de bestandsnaam of de bijbehorende lettertype-id te wijzigen.

Indien opgegeven in een geneste aanvraag, `cache=on` maakt het mogelijk de afbeelding die door de geneste aanvraag wordt gegenereerd, permanent in cache op de server te plaatsen. Zorg ervoor dat caching alleen mogelijk is voor geneste aanvragen wanneer hetzelfde geneste verzoek herhaaldelijk moet worden aangeroepen met exact dezelfde parameters.

## Eigenschappen {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Request-kenmerk. Ongeacht de huidige laaginstelling. Genegeerd wanneer het verzoek geen antwoordbeeld terugkeert. *`clientControl`*wordt genegeerd als caching op de client is uitgeschakeld in de afbeeldingscatalogus (als `catalog::Expiration` heeft een negatieve waarde).

Cachebeheer op de client ( `on` en `off` alleen) is ook beschikbaar voor aanvragen voor statische inhoud op [!DNL /is/content/].

## Standaard {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` voor HTTP-aanvragen, `cache=off` voor geneste/ingesloten aanvragen, `cache=on` voor verzoeken om statische inhoud.

## Zie ook {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalogus::Verlopen](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)

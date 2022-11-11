---
description: Cachebeheer. Hiermee wordt het selectief uitschakelen van caching op de client (browser, proxyservers, netwerkcaching-systemen) en het in cache plaatsen op de interne [!DNL Platform Server] cache.
solution: Experience Manager
title: cachegeheugen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# cachegeheugen{#cache}

Cachebeheer. Hiermee wordt het selectief uitschakelen van caching op de client (browser, proxyservers, netwerkcaching-systemen) en het in cache plaatsen op de interne [!DNL Platform Server] cache.

`&cache= *`cacheControl`*`

`&cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
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

Als slechts één *`cacheControl`* waarde wordt opgegeven, wordt deze toegepast op zowel client- als servercache.

Request-kenmerk. Genegeerd wanneer het verzoek geen antwoordbeeld terugkeert. *`clientControl`* wordt genegeerd wanneer caching op de client is uitgeschakeld door de afbeeldingscatalogus (als `catalog::Expiration` heeft een negatieve waarde).

Standaardwaarden: `cache=on,on`.

---
description: Cachebeheer. Staat selectief toe onbruikbaar makend cliënt-zijcaching (browser, volmachtsservers, netwerk caching systemen) en caching in het interne geheime voorgeheugen van de Server van het Platform.
solution: Experience Manager
title: cachegeheugen
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# cache{#cache}

Cachebeheer. Staat selectief toe onbruikbaar makend cliënt-zijcaching (browser, volmachtsservers, netwerk caching systemen) en caching in het interne geheime voorgeheugen van de Server van het Platform.

`&cache= *`cacheControl`*`

`&cache= *``*, *`clientControllerServerControl`*`

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

Als slechts één *`cacheControl`* waarde wordt gespecificeerd, wordt het toegepast op zowel cliënt als servergeheime voorgeheugens.

Request-kenmerk. Genegeerd wanneer het verzoek geen antwoordbeeld terugkeert. *`clientControl`* wordt genegeerd wanneer caching aan de clientzijde door de afbeeldingscatalogus wordt uitgeschakeld (als de waarde een negatieve waarde  `catalog::Expiration` heeft).

Wordt standaard ingesteld op `cache=on,on`.

---
description: Opdrachtwaarden moeten http-gecodeerd zijn met gebruik van %xx escape-reeksen, zodat de waardetekenreeksen de gereserveerde tekens '=', '&' en '%' niet bevatten.
seo-description: Opdrachtwaarden moeten http-gecodeerd zijn met gebruik van %xx escape-reeksen, zodat de waardetekenreeksen de gereserveerde tekens '=', '&' en '%' niet bevatten.
seo-title: HTTP-codering voor het renderen van afbeeldingen
solution: Experience Manager
title: HTTP-codering voor het renderen van afbeeldingen
topic: Scene7 Image Serving - Image Rendering API
uuid: 37bd0040-7bad-4548-ab39-7f598a217732
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# HTTP-codering voor het renderen van afbeeldingen{#image-rendering-http-encoding}

Opdrachtwaarden moeten http-gecodeerd zijn met gebruik van %xx escape-reeksen, zodat de waardetekenreeksen de gereserveerde tekens &#39;=&#39;, &#39;&amp;&#39; en &#39;%&#39; niet bevatten.

Anders zijn de standaard HTTP-coderingsregels van toepassing. De HTTP-specificatie vereist codering van de onveilige tekens zoals &#39; &#39; (space), &#39;&#39;&#39; (dubbel aanhalingsteken), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; en &#39;>&#39;, en van alle besturingstekens, zoals `<return>` en `<tab>`.

**Let op:** accolades { } die worden gebruikt als scheidingstekens voor het nesten van aanvragen, mogen niet worden gecodeerd. Bepaalde e-mailclients coderen helaas accolades in ingesloten HTTP-aanvraag. Mocht dit een probleem zijn, dan is bij het renderen van afbeeldingen het gebruik van haakjes ( ) in plaats van accolades toegestaan.

## Voorbeeld {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

Het bovenstaande aanvraagfragment moet als volgt worden gecodeerd:

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Zie ook {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1-specificatie (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)

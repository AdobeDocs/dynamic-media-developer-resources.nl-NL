---
description: De connectortag in server.xml ondersteunt een ciphers-attribuut om de ciphers te beperken die kunnen worden gekozen voor een SSL-verbinding.
seo-description: De connectortag in server.xml ondersteunt een ciphers-attribuut om de ciphers te beperken die kunnen worden gekozen voor een SSL-verbinding.
seo-title: SSL-ciphers definiëren
solution: Experience Manager
title: SSL-ciphers definiëren
topic: Scene7 Image Serving - Image Rendering API
uuid: 9490fb9a-5abb-4f5e-b660-b7af0a5e4b4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# SSL-ciphers definiëren{#defining-ssl-ciphers}

De connectortag in server.xml ondersteunt een ciphers-attribuut om de ciphers te beperken die kunnen worden gekozen voor een SSL-verbinding.

Standaard zijn alle ciphers beschikbaar. De lijst wordt gescheiden door komma&#39;s en kan een van de volgende waarden bevatten:

`SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_DSS_WITH_DES_CBC_SHA`

`SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_RSA_EXPORT_WITH_RC4_40_MD5`

`SSL_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

`TLS_RSA_WITH_AES_128_CBC_SHA`

Als een van de waarden verkeerd is, zal Tomcat elke enkele cipher toelaten. Het is dus van essentieel belang om met een extern hulpmiddel na configuratie te controleren om te zien welke ciphers eigenlijk worden toegelaten.

Als voorbeeld zal de volgende configuratie slechts de &quot;128-bits&quot;cijfersuites en hierboven toelaten:

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,SSL_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA,TLS_RSA_WITH_AES_128_CBC_SHA"`

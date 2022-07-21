---
description: De connectortag in server.xml ondersteunt een ciphers-attribuut om de ciphers te beperken die kunnen worden gekozen voor een SSL-verbinding.
solution: Experience Manager
title: SSL-ciphers definiëren
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 7734ba02-4442-4a3d-acbf-e14d8ad66279
source-git-commit: 370444b85cb2636d109df4e2681e3e078d6f1e1a
workflow-type: tm+mt
source-wordcount: '113'
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

<!-- WEAK CQDOC-19433 `SSL_RSA_WITH_3DES_EDE_CBC_SHA` -->

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

<!-- WEAK CQDOC-19433 `TLS_RSA_WITH_AES_128_CBC_SHA` -->

Als een van de waarden verkeerd is, zal Tomcat elke enkele cipher toelaten. Het is dus van essentieel belang om met een extern hulpmiddel na configuratie te controleren om te zien welke ciphers eigenlijk worden toegelaten.

Als voorbeeld laat de volgende configuratie alleen de &quot;128-bits&quot; cdersuites en hoger toe:

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA"`

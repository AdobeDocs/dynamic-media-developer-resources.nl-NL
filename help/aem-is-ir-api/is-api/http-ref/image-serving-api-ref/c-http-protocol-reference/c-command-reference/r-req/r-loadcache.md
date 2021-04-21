---
description: Servercache vooraf laden. Voert het verzoek uit enkel zoals req=img, maar in plaats van het terugkeren van het beeld, keert de server de lengte van het antwoordbeeld (image.length) terug, die als tekstgegevens met MIME type tekst/onbewerkt wordt geformatteerd.
solution: Experience Manager
title: loadcache
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# loadcache{#loadcache}

Servercache vooraf laden. Voert het verzoek uit enkel zoals req=img, maar in plaats van het terugkeren van het beeld, keert de server de lengte van het antwoordbeeld (image.length) terug, die als tekstgegevens met MIME type tekst/onbewerkt wordt geformatteerd.

`req=loadcache`

De HTTP-respons is niet cacheable.

Andere opdrachten in de aanvraag zijn van toepassing zoals wordt beschreven.

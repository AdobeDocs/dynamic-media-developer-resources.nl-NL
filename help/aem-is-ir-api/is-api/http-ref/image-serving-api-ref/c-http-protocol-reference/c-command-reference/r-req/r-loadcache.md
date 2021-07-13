---
description: Servercache vooraf laden. Voert het verzoek uit enkel zoals req=img, maar in plaats van het terugkeren van het beeld, keert de server de lengte van het antwoordbeeld (image.length) terug, die als tekstgegevens met MIME type tekst/onbewerkt wordt geformatteerd.
solution: Experience Manager
title: loadcache
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 653842e9-bed1-462a-bb1f-39ac1ac9512c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# loadcache{#loadcache}

Servercache vooraf laden. Voert het verzoek uit enkel zoals req=img, maar in plaats van het terugkeren van het beeld, keert de server de lengte van het antwoordbeeld (image.length) terug, die als tekstgegevens met MIME type tekst/onbewerkt wordt geformatteerd.

`req=loadcache`

De HTTP-respons is niet cacheable.

Andere opdrachten in de aanvraag zijn van toepassing zoals wordt beschreven.

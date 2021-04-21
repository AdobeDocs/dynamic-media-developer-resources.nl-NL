---
description: Miniatuurafbeelding. Verzoekt afbeeldingsgegevens die zijn opgemaakt en gesorteerd aan de hand van de criteria voor catalogusminiaturen.
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---


# tmb{#tmb}

Miniatuurafbeelding. Verzoekt afbeeldingsgegevens die zijn opgemaakt en gesorteerd aan de hand van de criteria voor catalogusminiaturen.

`req=tmb`

De indeling van de antwoordgegevens en het MIME-type van de reactie worden bepaald door `fmt=`. Ondersteunt alle opdrachten behalve `fit=`.

Zie [Miniatuurschaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

De reactie van HTTP kan met TTL worden in het voorgeheugen ondergebracht dat op `catalog::Expiration` wordt gebaseerd.

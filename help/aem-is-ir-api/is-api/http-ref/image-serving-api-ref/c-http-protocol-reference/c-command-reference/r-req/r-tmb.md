---
description: Miniatuurafbeelding. Verzoekt afbeeldingsgegevens die zijn opgemaakt en gesorteerd aan de hand van de criteria voor catalogusminiaturen.
seo-description: Miniatuurafbeelding. Verzoekt afbeeldingsgegevens die zijn opgemaakt en gesorteerd aan de hand van de criteria voor catalogusminiaturen.
seo-title: tmb
solution: Experience Manager
title: tmb
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---


# tmb{#tmb}

Miniatuurafbeelding. Verzoekt afbeeldingsgegevens die zijn opgemaakt en gesorteerd aan de hand van de criteria voor catalogusminiaturen.

`req=tmb`

De indeling van de antwoordgegevens en het MIME-type van de reactie worden bepaald door `fmt=`. Ondersteunt alle opdrachten behalve `fit=`.

Zie [Miniatuurschaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

De reactie van HTTP kan met TTL worden in het voorgeheugen ondergebracht dat op `catalog::Expiration` wordt gebaseerd.

---
description: Miniatuurafbeelding. Verzoekt afbeeldingsgegevens die zijn opgemaakt en gesorteerd aan de hand van de criteria voor catalogusminiaturen.
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# tmb{#tmb}

Miniatuurafbeelding. Verzoekt afbeeldingsgegevens die zijn opgemaakt en gesorteerd aan de hand van de criteria voor catalogusminiaturen.

`req=tmb`

De indeling van de antwoordgegevens en het MIME-type van de reactie worden bepaald door `fmt=`. Ondersteunt alle opdrachten behalve `fit=`.

Zie [Miniatuurschaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

De reactie van HTTP kan met TTL worden in het voorgeheugen ondergebracht dat op `catalog::Expiration` wordt gebaseerd.

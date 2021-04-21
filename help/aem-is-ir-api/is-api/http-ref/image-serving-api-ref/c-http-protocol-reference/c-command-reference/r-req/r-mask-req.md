---
description: Afbeeldingsmasker. Verzoekt de maskergegevens (alfakanaal).
solution: Experience Manager
title: masker
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# mask{#mask}

Afbeeldingsmasker. Verzoekt de maskergegevens (alfakanaal).

`req=mask`

Ondersteunt dezelfde opdrachten als `req=img`. Deze wordt op dezelfde manier door de server verwerkt, maar in plaats van de RGB- of RGBA-gegevens te retourneren, verwijdert de server de kleurinformatie en retourneert alleen de maskergegevens (alfakanaal). De indeling van de antwoordgegevens en het MIME-type van de reactie worden bepaald door `fmt=`.

De reactie van HTTP is cacheable met TTL die op `catalog::Expiration` wordt gebaseerd.

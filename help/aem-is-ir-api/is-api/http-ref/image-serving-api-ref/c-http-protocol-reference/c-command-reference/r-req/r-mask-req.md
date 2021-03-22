---
description: Afbeeldingsmasker. Verzoekt de maskergegevens (alfakanaal).
seo-description: Afbeeldingsmasker. Verzoekt de maskergegevens (alfakanaal).
seo-title: masker
solution: Experience Manager
title: masker
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# mask{#mask}

Afbeeldingsmasker. Verzoekt de maskergegevens (alfakanaal).

`req=mask`

Ondersteunt dezelfde opdrachten als `req=img` en wordt door de server op dezelfde manier verwerkt, maar in plaats van de RGB- of RGBA-gegevens te retourneren, verwijdert de server de kleurinformatie en retourneert alleen de maskergegevens (alfakanaal). De indeling van de antwoordgegevens en het MIME-type van de reactie worden bepaald door `fmt=`.

De reactie van HTTP is cacheable met TTL die op `catalog::Expiration` wordt gebaseerd.

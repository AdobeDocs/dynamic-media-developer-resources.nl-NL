---
description: Afbeeldingsmasker. Verzoekt de maskergegevens (alfakanaal).
solution: Experience Manager
title: masker
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# masker{#mask}

Afbeeldingsmasker. Verzoekt de maskergegevens (alfakanaal).

`req=mask`

Ondersteunt dezelfde opdrachten als `req=img`. Deze wordt op dezelfde manier door de server verwerkt, maar in plaats van de RGB- of RGBA-gegevens te retourneren, verwijdert de server de kleurinformatie en retourneert alleen de maskergegevens (alfakanaal). De indeling van de antwoordgegevens en het MIME-type van de reactie worden bepaald door `fmt=`.

De HTTP-respons is cacheable met de TTL op basis van `catalog::Expiration`.

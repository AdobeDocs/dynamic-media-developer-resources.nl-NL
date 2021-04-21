---
title: Verouderde vraag
description: API-aanroepen van het systeem voor afbeeldingsproductie en de bijbehorende parameters die niet meer in Dynamic Media worden gebruikt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# Vervangen aanroepen{#deprecated-calls}

De vraag van het Systeem API van de Productie van het beeld en hun bijbehorende parameters die niet meer worden gebruikt.

## Vervangen aanroepen {#topic-654c0466e6434fe4a95953322255b08c}

API-aanroepen van het systeem voor afbeeldingsproductie en de bijbehorende parameters die niet meer in Dynamic Media worden gebruikt.

* `addMediaPortalEvent` - Vervangen van activiteiten. Deze vraag laat u een Poortgebeurtenis van Media aan IPS toevoegen.
* `getMediaPortalEvent` - Vervangen van activiteiten. Met deze aanroep kunt u mediaportaalgebeurtenissen ophalen die aan bepaalde criteria voldoen.
* `getCdnCacheInvalidationStatus` - Vervangen van activiteiten. Deze API is nu vervangen omdat de `cdnCacheInvalidation`-API de cache bijna onmiddellijk (~5 seconden) ongeldig maakt. Daarom is opiniepeiling voor de status van ongeldigmaking niet langer vereist.


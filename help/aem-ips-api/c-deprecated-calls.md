---
title: Verouderde vraag
description: API-aanroepen van het systeem voor afbeeldingsproductie en de bijbehorende parameters die niet meer worden gebruikt of ondersteund in Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: 10eb6887663fe335be3abcc311b2d3eb4a241745
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# Verouderde vraag{#deprecated-calls}

De vraag van het Systeem API van de Productie van het beeld en hun bijbehorende parameters die niet meer worden gebruikt.

## Verouderde vraag {#topic-654c0466e6434fe4a95953322255b08c}

API-aanroepen van het systeem voor afbeeldingsproductie en de bijbehorende parameters die niet meer in Dynamic Media worden gebruikt.

* `ExcludeMasterVideoFromAVS` - Vervangen van [Gegevenstypen](/help/aem-ips-api/types/c-data-types/c-data-types.md). Deze parameter sloot de primaire video uit van de adaptieve videoset.
   >[!IMPORTANT]
   >
   >Adobe beëindigt de ondersteuning voor deze parameter op 1 september 2022. Zie ook [ExcludeMasterVideoFromAVS](/help/aem-ips-api/types/c-data-types/r-exclude-master-video-from-avs.md).
* `addMediaPortalEvent` - Vervangen van [Bewerkingen](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Met deze parameter kunt u een Media Portal-gebeurtenis toevoegen aan IPS.
* `getMediaPortalEvent` - Vervangen van [Bewerkingen](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Met deze parameter kunt u gebeurtenissen van een mediaportal ophalen die aan de opgegeven criteria voldoen.
* `getCdnCacheInvalidationStatus` - Vervangen van [Bewerkingen](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Deze parameter is nu vervangen omdat de `cdnCacheInvalidation` wordt de cache bijna onmiddellijk (~5 seconden) ongeldig gemaakt. Daarom is opiniepeiling voor de status van ongeldigmaking niet langer vereist.

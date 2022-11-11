---
title: Verouderde vraag
description: API-aanroepen van het productiesysteem van images en de bijbehorende parameters die niet meer worden gebruikt of ondersteund in [!DNL Dynamic Media].
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Verouderde vraag{#deprecated-calls}

De vraag van het Systeem API van de Productie van het beeld en hun bijbehorende parameters die niet meer worden gebruikt.

## Verouderde vraag {#topic-654c0466e6434fe4a95953322255b08c}

De vraag van het Systeem API van de Productie van het beeld en hun bijbehorende parameters die niet meer in worden gebruikt [!DNL Dynamic Media].

* `ExcludeMasterVideoFromAVS` - Vervangen van [Gegevenstypen](/help/aem-ips-api/types/c-data-types/c-data-types.md). Deze parameter sloot de primaire video uit van de adaptieve videoset. <!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` - Vervangen van [Bewerkingen](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Met deze parameter kunt u een Media Portal-gebeurtenis toevoegen aan IPS.
* `getMediaPortalEvent` - Vervangen van [Bewerkingen](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Met deze parameter kunt u gebeurtenissen van een mediaportal ophalen die aan de opgegeven criteria voldoen.
* `getCdnCacheInvalidationStatus` - Vervangen van [Bewerkingen](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Deze parameter is nu vervangen omdat de `cdnCacheInvalidation` wordt de cache bijna onmiddellijk (~5 seconden) ongeldig gemaakt. Daarom is opiniepeiling voor de status van ongeldigmaking niet langer vereist.

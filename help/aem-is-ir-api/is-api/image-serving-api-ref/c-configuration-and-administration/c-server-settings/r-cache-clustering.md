---
description: Gebruik deze serverinstellingen voor cacheclustering.
seo-description: Gebruik deze serverinstellingen voor cacheclustering.
seo-title: Cache-clustering
solution: Experience Manager
title: Cache-clustering
topic: Scene7 Image Serving - Image Rendering API
uuid: ed6335d7-26c9-45d8-95f6-6c05e788e449
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Cache-clustering{#cache-clustering}

Gebruik deze serverinstellingen voor cacheclustering.

## PS::cacheCluster.hosts - Gastheren {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Lijst met IP-adressen, gescheiden door puntkomma&#39;s. Omvat de IP adressen van alle peer servers waarvan deze gastheer geheim voorgeheugengegevens zou moeten verkrijgen. Het IP-adres van de lokale host kan voor het gemak worden opgenomen; dit staat de zelfde configuratiemontages voor alle servers in de cluster toe.

## PS::cacheCluster.updateLocalCache - Lokale cache bijwerken {#section-154c2c0af4544200a3499232bb130dde}

Stel dit in op Ja als een cacheitem dat door een peer-server wordt aangeboden, moet worden gekopieerd naar de lokale responscache.

## PS::cacheCluster.queryTimeout - Time-out voor query {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Wanneer een server een cachevermelding aanvraagt van peer-servers, wacht de server tot één server reageert op dit specifieke gegevensitem of totdat alle peer-servers hebben gereageerd dat ze het gegevensitem niet hebben of totdat de tijd die met deze instelling is opgegeven (in msec) is verlopen.

## PS::cacheCluster.fetchTimeout - Time-out ophalen {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Geeft het maximumaantal msec op dat de server wacht tot de werkelijke cachegegevens van de peer-server worden geleverd. Als de volledige gegevens niet zijn geleverd voordat de time-out is verlopen, gaat de server ervan uit dat de peer niet meer beschikbaar is. De cachevermelding wordt vervolgens lokaal gegenereerd.

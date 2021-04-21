---
description: Het groeperen van het geheime voorgeheugen staat veelvoudige lading-evenwichtige servers toe om geheim voorgeheugeningangen in het primaire reactiecache en het secundaire gegevensgeheime voorgeheugen (voor genestelde/ingebedde verzoeken) uit te wisselen, met het potentieel om serverontvankelijkheid beduidend te verhogen door de behoefte te elimineren om de zelfde geheim voorgeheugeningang op veelvoudige servers te produceren.
solution: Experience Manager
title: Cache-clustering
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# Cache clustering{#cache-clustering}

Het groeperen van het geheime voorgeheugen staat veelvoudige lading-evenwichtige servers toe om geheim voorgeheugeningangen in het primaire reactiecache en het secundaire gegevensgeheime voorgeheugen (voor genestelde/ingebedde verzoeken) uit te wisselen, met het potentieel om serverontvankelijkheid beduidend te verhogen door de behoefte te elimineren om de zelfde geheim voorgeheugeningang op veelvoudige servers te produceren.

Als zo gevormd, wanneer een server een verzoek voor een punt ontvangt dat niet in lokaal geheime voorgeheugen is, contacteert het de peer servers in de cluster. Het controleert om te zien of hebben zij reeds dat gegevenspunt alvorens de Server van het Beeld te vragen om het punt te produceren.

Het groeperen van het geheime voorgeheugen bevordert hoofdzakelijk toepassingen die hoogst cacheable inhoud impliceren. Serverbelasting moet aanzienlijk worden verminderd tijdens de eerste implementatie en bij live gaan met nieuwe inhoud.

De onderbrekingen en andere waarborgen zorgen ervoor dat het systeem bij volledige capaciteit blijft presteren zelfs wanneer één of meerdere peer servers off-line is.

De geheim voorgeheugencluster kan in één van twee basisconfiguraties werken:

* Wanneer `PS::cacheCluster.updateLocalCache` is ingeschakeld (standaard), wordt alle cachevermelding die op een peer-server wordt gevonden, naar de lokale cache gekopieerd.

   Deze configuratie vermindert verkeer tussen de peer servers. Het biedt ook de snelste responstijden ten koste van het repliceren van alle cachemarkeringen naar alle servers in de cluster. Dit is de aanbevolen configuratie.

* Wanneer `PS::cacheCluster.updateLocalCache` is uitgeschakeld, worden gegevens van andere servers niet naar de lokale cache gekopieerd.

   Hiermee wordt de beschikbare schijfruimte voor cachegegevens vermenigvuldigd. Nochtans, verhoogt het het verkeer tussen de peer servers en vermindert de algemene reactietijden. Gebruik deze configuratie slechts wanneer u lage geheim voorgeheugenklaptarieven ziet.


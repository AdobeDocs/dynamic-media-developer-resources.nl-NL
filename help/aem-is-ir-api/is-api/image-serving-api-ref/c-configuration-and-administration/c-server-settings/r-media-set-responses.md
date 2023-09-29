---
title: Reacties mediaset
description: De instellingen in deze sectie zijn van toepassing op mediasetreacties die worden verkregen door de optie req=set.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Reacties mediaset{#media-set-responses}

De instellingen in deze sectie zijn van toepassing op mediasetreacties die worden verkregen door de `req=set` modifier.

## PS::fvctx.useCatalogRecordValidation - Caching Policy {#section-9accb087d16548a988993bb30395a6f6}

This property controls the caching policy when determine whether a set response retrieve from a cache must be regenerated. Als de eigenschap is uitgeschakeld, wordt het tijdstempel van de [!DNL catalog.ini] bestand wordt gebruikt voor validatie. Als eigenschap is ingeschakeld, wordt de meest recente `catalog::LastModified` tijdstempel uit alle records waarnaar wordt verwezen, wordt gebruikt voor validatie.

## PS::fvctx.nestingLimit - Nestlimiet {#section-280210341f1647fea02590e7069934d2}

De maximale nestdiepte van een `req=set` reactie. Als deze diepte wordt overschreden, wordt een fout geretourneerd.

## PS::fvctx.brochureLimit - Brochure Limit {#section-fe36e47db49244cea7f07e9dd3639440}

Het maximumaantal e-catalogusbrochures in de `req=set` reactie die alle bijbehorende metagegevens bevat. Als deze limiet is overschreden, worden eventuele persoonlijke kaarten en gebruikersgegevens die aan het brochure-item zijn gekoppeld, onderdrukt.

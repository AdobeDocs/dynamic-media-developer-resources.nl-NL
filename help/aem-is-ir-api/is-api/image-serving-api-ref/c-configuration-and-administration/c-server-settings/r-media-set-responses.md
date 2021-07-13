---
description: De instellingen in deze sectie zijn van toepassing op mediasetreacties die worden verkregen door de optie req=set.
solution: Experience Manager
title: Reacties mediaset
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# Reacties mediaset{#media-set-responses}

De instellingen in deze sectie zijn van toepassing op mediasetreacties die worden verkregen door de optie req=set.

## PS::fvctx.useCatalogRecordValidation - Caching Policy {#section-9accb087d16548a988993bb30395a6f6}

This property controls the caching policy when determine whether or not set response retrieve from cache need-to be-generated. Als eigenschap is uitgeschakeld, wordt de tijdstempel van het [!DNL catalog.ini]-bestand gebruikt voor validatie. Als eigenschap is ingeschakeld, wordt de nieuwste `catalog::LastModified` tijdstempel van alle records waarnaar wordt verwezen, gebruikt voor validatie.

## PS::fvctx.nestingLimit - Nestlimiet {#section-280210341f1647fea02590e7069934d2}

De maximale nestdiepte van elke `req=set`-reactie. Als deze diepte wordt overschreden, wordt een fout geretourneerd.

## PS::fvctx.brochureLimit - Brochure Limit {#section-fe36e47db49244cea7f07e9dd3639440}

Het maximumaantal e-catalogusbrochures in de `req=set` reactie die alle bijbehorende meta-gegevens bevat. Als deze limiet is overschreden, worden eventuele persoonlijke kaarten en gebruikersgegevens die aan het brochure-item zijn gekoppeld, onderdrukt.

---
description: Verzendt een e-mail naar een aangewezen ontvanger in antwoord op een verrichting cdnCacheInvalidation.
seo-description: Verzendt een e-mail naar een aangewezen ontvanger in antwoord op een verrichting cdnCacheInvalidation.
seo-title: E-mailbevestiging
solution: Experience Manager
title: E-mailbevestiging
topic: Scene7 Image Production System API
uuid: c3b7aada-a03a-418d-80b2-31a86a1af786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---


# E-mailbevestiging{#emailconfirmation}

Verzendt een e-mail naar een aangewezen ontvanger in antwoord op een verrichting cdnCacheInvalidation.

Syntaxis

## Parameters {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Naam | Type | Beschrijving |
|---|---|---|
| ` *`ccOriginator`*` | `xsd:boolean` | Indien waar (true), wordt de gebruikersaccount voor de webservice van de gebruiker opgenomen. Dit is een lijst met e-mailberichten die zijn toegewezen voor het ontvangen van een e-mailbevestiging van de Scene7 CDN. |
| ` *`ccOthersArray`*` | `types:EmailArray` | Een array met e-mailadressen (maximaal 5) die is opgegeven voor het ontvangen van het bevestigingsbericht van de Scene7 CDN. |


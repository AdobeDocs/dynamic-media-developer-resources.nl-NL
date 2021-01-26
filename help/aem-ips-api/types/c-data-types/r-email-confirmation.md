---
description: Verzendt een e-mail naar een aangewezen ontvanger in antwoord op een verrichting cdnCacheInvalidation.
solution: Experience Manager
title: E-mailbevestiging
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---


# E-mailbevestiging{#emailconfirmation}

Verzendt een e-mail naar een aangewezen ontvanger in antwoord op een verrichting cdnCacheInvalidation.

Syntaxis

## Parameters {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Naam | Type | Beschrijving |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | Indien waar (true), wordt de gebruikersaccount voor de webservice van de gebruiker opgenomen. Dit is een lijst met e-mailberichten die zijn toegewezen voor het ontvangen van een e-mailbevestiging van de Dynamic Media CDN. |
| `*`ccOthersArray`*` | `types:EmailArray` | Een array met e-mailadressen (maximaal 5) die is opgegeven voor het ontvangen van het bevestigingsbericht van de Dynamic Media CDN. |


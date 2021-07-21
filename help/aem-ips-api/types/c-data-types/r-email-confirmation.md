---
description: Verzendt een e-mail naar een aangewezen ontvanger in antwoord op een verrichting cdnCacheInvalidation.
solution: Experience Manager
title: E-mailbevestiging
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '83'
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

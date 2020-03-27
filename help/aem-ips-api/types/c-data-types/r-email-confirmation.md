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

---


# E-mailbevestiging{#emailconfirmation}

Verzendt een e-mail naar een aangewezen ontvanger in antwoord op een verrichting cdnCacheInvalidation.

Syntaxis

## Parameters {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Naam | Type | Beschrijving |
|---|---|---|
| ` *`ccOriginator`*` | `xsd:boolean` | Indien waar, omvat de rekening van de de Webdienst van de gebruiker, die een lijst van e-mails is die wordt aangewezen om een e-mailbevestiging van CDN te ontvangen Scene7. |
| ` *`ccOthersArray`*` | `types:EmailArray` | Een serie van e-mailadressen (maximaal 5) die wordt aangewezen om het bevestigingsbericht van Scene7 CDN te ontvangen. |


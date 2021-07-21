---
description: Uitsluitend voor intern gebruik. Gebruikers moeten naar de sectie Referentie afbeeldingscatalogus voor afbeeldingsserver - Kenmerkverwijzing verwijzen.
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---

# getImageServingPublishSettings{#getimageservingpublishsettings}

Uitsluitend voor intern gebruik. Gebruikers moeten naar de sectie Referentie afbeeldingscatalogus voor afbeeldingsserver - Kenmerkverwijzing verwijzen.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-79f0d54acd604ad2a5c96679334f2424}

**Input (getImageServingPublishSettingsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep van het bedrijf met de afbeelding die de publicatie-instellingen voedt. |
| `*`contextHandle`*` | `xsd:string` | Ja | Verwerk de publicatiecontext. |

**Uitvoer**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`publishSettingArray`*` | `xsd:string` | Ja | Array met publicatie-instellingen van afbeeldingsserver. |

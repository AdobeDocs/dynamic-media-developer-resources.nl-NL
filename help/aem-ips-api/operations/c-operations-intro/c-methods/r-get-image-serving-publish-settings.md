---
description: Uitsluitend voor intern gebruik. Gebruikers moeten naar de sectie Referentie afbeeldingscatalogus voor afbeeldingsserver - Kenmerkverwijzing verwijzen.
seo-description: Uitsluitend voor intern gebruik. Gebruikers moeten naar de sectie Referentie afbeeldingscatalogus voor afbeeldingsserver - Kenmerkverwijzing verwijzen.
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# getImageServingPublishSettings{#getimageservingpublishsettings}

Uitsluitend voor intern gebruik. Gebruikers moeten naar de sectie Referentie afbeeldingscatalogus voor afbeeldingsserver - Kenmerkverwijzing verwijzen.

Syntaxis

## Toegestane gebruikerstypen {#section-49b7b277ba1748499121a0e90996458c}

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


---
description: Uitsluitend voor intern gebruik. Zie het gedeelte Kenmerken van materiaalcatalogus voor referentiecatalogus van afbeeldingen renderen.
seo-description: Uitsluitend voor intern gebruik. Zie het gedeelte Kenmerken van materiaalcatalogus voor referentiecatalogus van afbeeldingen renderen.
seo-title: getImageRenderingPublishSettings
solution: Experience Manager
title: getImageRenderingPublishSettings
uuid: b1c253b5-febe-4dc7-95a1-a5f4789030e7
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

Uitsluitend voor intern gebruik. Zie het gedeelte Kenmerken van materiaalcatalogus voor referentiecatalogus van afbeeldingen renderen.

Syntaxis

## Toegestane gebruikerstypen {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-4f2cb8c589384816bb2525654ec49963}

**Input (getImageRenderingPublishSettingsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep voor het bedrijf waarvan u publicatie-instellingen voor het renderen van afbeeldingen wilt ophalen. |
| `*`contextHandle`*` | `xsd:string` | Ja | Verwerk de publicatiecontext. |

**Output (getImageRenderingPublishSettingsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`publishSettingsArray`*` | `type:ConfigSettingArray` | Ja | Publicatie-instellingen voor het renderen van afbeeldingen. |


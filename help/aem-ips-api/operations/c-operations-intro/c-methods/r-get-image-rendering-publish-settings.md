---
description: Uitsluitend voor intern gebruik. Zie het gedeelte Kenmerken van materiaalcatalogus voor referentiecatalogus van afbeeldingen renderen.
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '81'
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


---
description: Hiermee worden alle configuratie-instellingen voor de viewer opgehaald die aan het opgegeven element zijn gekoppeld.
seo-description: Hiermee worden alle configuratie-instellingen voor de viewer opgehaald die aan het opgegeven element zijn gekoppeld.
seo-title: getViewerConfigSettings
solution: Experience Manager
title: getViewerConfigSettings
topic: Scene7 Image Production System API
uuid: 61fe16de-ac72-472b-8945-f1ebe8b4d11c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---


# getViewerConfigSettings{#getviewerconfigsettings}

Hiermee worden alle configuratie-instellingen voor de viewer opgehaald die aan het opgegeven element zijn gekoppeld.

Syntaxis

## Toegestane gebruikerstypen {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-7d06abf3d707494c8a1270c7fa1477f1}

**Input (getViewerConfigSettingsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handgreep aan het bedrijf. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Verwerk het element. |

**Output (getViewerConfigurationSettingsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`type`*` | `xsd:string` | Ja | Viewer type waarop de configuratie-instellingen van toepassing zijn. |
| ` *`configSettingsArray`*` | `types:ConfigSettingsArray` | Ja | Array met viewerconfiguratie-instellingen. |


---
description: Werkt de configuratie-instellingen van de SWF-viewer bij.
seo-description: Werkt de configuratie-instellingen van de SWF-viewer bij.
seo-title: updateViewerConfigSettings
solution: Experience Manager
title: updateViewerConfigSettings
uuid: ad4af874-5ca4-4182-868e-afa48b1cd2b6
feature: Dynamic Media Classic,SDK/API,Viewer-voorinstellingen
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---


# updateViewerConfigSettings{#updateviewerconfigsettings}

Werkt de configuratie-instellingen van de SWF-viewer bij.

Syntaxis

## Toegestane gebruikerstypen {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-29790d933fb24aa392d0cb2d52d1310f}

**Input (updateViewerConfigSettingsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handgreep aan het bedrijf. |
| `*`assetHandle`*` | `xsd:string` | Ja | Asset handle. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Ja | Array met configuratie-instellingen die u wilt toepassen op de viewer. |

**Output (updateViewerConfigSettingsReturn)**

IPS API keert geen reactie voor deze verrichting terug.

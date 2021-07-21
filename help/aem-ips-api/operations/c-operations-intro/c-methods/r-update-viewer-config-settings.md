---
description: Werkt de configuratie-instellingen van de SWF-viewer bij.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer-voorinstellingen
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 0%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

Werkt de configuratie-instellingen van de SWF-viewer bij.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-0dd001da1b784aefa5eb5b50c7a2c045}

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

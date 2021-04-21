---
description: Koppelt de configuratie-instellingen van de viewer aan een element. Dit kan een viewervoorinstelling zijn of het bronelement voor de viewer.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# setViewerConfigSettings{#setviewerconfigsettings}

Koppelt de configuratie-instellingen van de viewer aan een element. Dit kan een viewervoorinstelling zijn of het bronelement voor de viewer.

Syntaxis

## Toegestane gebruikerstypen {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-bcc8c83cc84141e8b1341be9133e8511}

**Input (setViewerConfigSettingsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handgreep aan het bedrijf. |
| `*`assetHandle`*` | `xsd:string` | Ja | Asset handle. |
| `*`name`*` | `xsd:string` | Ja | Elementnaam. |
| `*`type`*` | `xsd:string` | Ja | Het type element waarop u de viewerconfiguratie wilt toepassen. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Ja | De array van `ConfigSettings` die op het element wordt toegepast. |

**Output (setViewerConfigSettingsParam)**

IPS API keert geen reactie voor deze verrichting terug.

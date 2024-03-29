---
description: Koppelt de configuratie-instellingen van de viewer aan een element. Dit kan een viewervoorinstelling zijn of het bronelement voor de viewer.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# setViewerConfigSettings{#setviewerconfigsettings}

Koppelt de configuratie-instellingen van de viewer aan een element. Dit kan een viewervoorinstelling zijn of het bronelement voor de viewer.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-bcc8c83cc84141e8b1341be9133e8511}

**Input (setViewerConfigSettingsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handgreep aan het bedrijf. |
| assetHandle | `xsd:string` | Ja | Asset handle. |
| name | `xsd:string` | Ja | Elementnaam. |
| type | `xsd:string` | Ja | Het type element waarop u de viewerconfiguratie wilt toepassen. |
| configSettingArray | `types:ConfigSettingArray` | Ja | De array van `ConfigSettings` toegepast op het element.. |

**Output (setViewerConfigSettingsParam)**

IPS API keert geen reactie voor deze verrichting terug.

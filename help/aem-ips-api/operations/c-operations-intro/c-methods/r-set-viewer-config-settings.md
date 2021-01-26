---
description: Koppelt de configuratie-instellingen van de viewer aan een element. Dit kan een viewervoorinstelling zijn of het bronelement voor de viewer.
seo-description: Koppelt de configuratie-instellingen van de viewer aan een element. Dit kan een viewervoorinstelling zijn of het bronelement voor de viewer.
seo-title: setViewerConfigSettings
solution: Experience Manager
title: setViewerConfigSettings
topic: Dynamic Media Image Production System API
uuid: d83d866e-9243-479f-9b33-727aad8158e5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
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

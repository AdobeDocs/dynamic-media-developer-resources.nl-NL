---
description: Hiermee worden alle configuratie-instellingen voor de viewer opgehaald die aan het opgegeven element zijn gekoppeld.
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---

# getViewerConfigSettings{#getviewerconfigsettings}

Hiermee worden alle configuratie-instellingen voor de viewer opgehaald die aan het opgegeven element zijn gekoppeld.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameters {#section-7d06abf3d707494c8a1270c7fa1477f1}

**Input (getViewerConfigSettingsParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handgreep aan het bedrijf. |
| assetHandle | `xsd:string` | Ja | Verwerk het element. |

**Output (getViewerConfigurationSettingsReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| type | `xsd:string` | Ja | Viewer type waarop de configuratie-instellingen van toepassing zijn. |
| configSettingsArray | `types:ConfigSettingsArray` | Ja | Array met viewerconfiguratie-instellingen. |

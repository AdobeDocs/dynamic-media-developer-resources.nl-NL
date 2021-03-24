---
description: Hiermee wordt een lijst met actieve publicatiecontexten voor het opgegeven bedrijf opgehaald. Een publicatiecontext wordt als actief beschouwd als er ten minste één actieve server voor de context is gedefinieerd.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---


# getActivePublishContext{#getactivepublishcontext}

Hiermee wordt een lijst met actieve publicatiecontexten voor het opgegeven bedrijf opgehaald. Een publicatiecontext wordt als actief beschouwd als er ten minste één actieve server voor de context is gedefinieerd.

Syntaxis

## Toegestane gebruikerstypen {#section-eb22397744434dfe92a59ffa2883c2e7}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameters {#section-a4be4024e55c472fa6728faec9c5e048}

**Input (getActivePublishContextParam)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf om voor actieve te vragen publiceert contexten |

**Output (getActivePublishContextReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| `*`contextArray`*` | `types:StringArray` | Ja | De array met actieve publicatiecontexten, die nul of meer waarden uit de publicatiecontext kan bevatten. |


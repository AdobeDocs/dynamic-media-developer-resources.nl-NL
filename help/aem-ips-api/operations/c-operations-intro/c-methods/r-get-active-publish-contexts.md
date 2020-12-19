---
description: Hiermee wordt een lijst met actieve publicatiecontexten voor het opgegeven bedrijf opgehaald. Een publicatiecontext wordt als actief beschouwd als er ten minste één actieve server voor de context is gedefinieerd.
seo-description: Hiermee wordt een lijst met actieve publicatiecontexten voor het opgegeven bedrijf opgehaald. Een publicatiecontext wordt als actief beschouwd als er ten minste één actieve server voor de context is gedefinieerd.
seo-title: getActivePublishContext
solution: Experience Manager
title: getActivePublishContext
topic: Scene7 Image Production System API
uuid: 856704d1-e97b-4d2d-b80c-620450b78432
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '138'
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
| ` *`companyHandle`*` | `xsd:string` | Ja | De handgreep aan het bedrijf om voor actieve te vragen publiceert contexten |

**Output (getActivePublishContextReturn)**

| Naam | Type | Vereist | Beschrijving |
|---|---|---|---|
| ` *`contextArray`*` | `types:StringArray` | Ja | De array met actieve publicatiecontexten, die nul of meer waarden uit de publicatiecontext kan bevatten. |


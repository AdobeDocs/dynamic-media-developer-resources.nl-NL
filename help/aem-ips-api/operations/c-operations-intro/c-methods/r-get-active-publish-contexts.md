---
description: Hiermee wordt een lijst met actieve publicatiecontexten voor het opgegeven bedrijf opgehaald. Een publicatiecontext wordt als actief beschouwd als er ten minste één actieve server voor de context is gedefinieerd.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# getActivePublishContext{#getactivepublishcontext}

Hiermee wordt een lijst met actieve publicatiecontexten voor het opgegeven bedrijf opgehaald. Een publicatiecontext wordt als actief beschouwd als er ten minste één actieve server voor de context is gedefinieerd.

Syntaxis

## Geautoriseerde gebruikerstypen {#section-eb22397744434dfe92a59ffa2883c2e7}

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

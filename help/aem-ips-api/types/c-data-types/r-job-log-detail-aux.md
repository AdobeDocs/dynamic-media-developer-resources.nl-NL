---
description: Bevat aanvullende berichten die zijn gekoppeld aan het hoofdbericht van het taaklog (JobDetail). Bevat waarschuwingen en andere details die aan het momenteel verwerkte element zijn gekoppeld.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---


# JobLogDetailAux{#joblogdetailaux}

Bevat aanvullende berichten die zijn gekoppeld aan het hoofdbericht van het taaklog (JobDetail). Bevat waarschuwingen en andere details die aan het momenteel verwerkte element zijn gekoppeld.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | Een hulpbericht. |
| `*`logType`*` | `xsd:string` | Logbestandstype: `IPSJobLog.gcUploadWarning` of `IPSJobLog.gcUploadError`. |
| `*`dateCreated`*` | `xsd:dateTime` | Aanmaakdatum van extra taaklog. |


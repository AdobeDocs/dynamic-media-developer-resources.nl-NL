---
description: Bevat aanvullende berichten die zijn gekoppeld aan het hoofdbericht van het taaklog (JobDetail). Bevat waarschuwingen en andere details die aan het momenteel verwerkte element zijn gekoppeld.
seo-description: Bevat aanvullende berichten die zijn gekoppeld aan het hoofdbericht van het taaklog (JobDetail). Bevat waarschuwingen en andere details die aan het momenteel verwerkte element zijn gekoppeld.
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
topic: Dynamic Media Image Production System API
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '88'
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


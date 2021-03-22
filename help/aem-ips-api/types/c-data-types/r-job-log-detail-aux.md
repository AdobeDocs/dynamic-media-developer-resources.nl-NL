---
description: Bevat aanvullende berichten die zijn gekoppeld aan het hoofdbericht van het taaklog (JobDetail). Bevat waarschuwingen en andere details die aan het momenteel verwerkte element zijn gekoppeld.
seo-description: Bevat aanvullende berichten die zijn gekoppeld aan het hoofdbericht van het taaklog (JobDetail). Bevat waarschuwingen en andere details die aan het momenteel verwerkte element zijn gekoppeld.
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '95'
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


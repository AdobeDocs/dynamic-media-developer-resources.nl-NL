---
description: Bevat aanvullende berichten die zijn gekoppeld aan het hoofdbericht van het taaklog (JobDetail). Bevat waarschuwingen en andere details die aan het momenteel verwerkte element zijn gekoppeld.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# [!DNL JobLogDetailAux]{#joblogdetailaux}

Bevat aanvullende berichten die zijn gekoppeld aan het hoofdbericht van het taaklog (JobDetail). Bevat waarschuwingen en andere details die aan het momenteel verwerkte element zijn gekoppeld.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| logMessage | `xsd:string` | Een hulpbericht. |
| logType | `xsd:string` | Logbestandstype: `IPSJobLog.gcUploadWarning` of `IPSJobLog.gcUploadError`. |
| dateCreated | `xsd:dateTime` | Aanmaakdatum van extra taaklog. |

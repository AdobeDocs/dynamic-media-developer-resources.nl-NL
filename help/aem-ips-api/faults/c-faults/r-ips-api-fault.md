---
description: ipsApiFault
solution: Experience Manager
title: ipsApiFault
uuid: 010814a8-1d29-4b02-8449-cb26e4335e07
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '32'
ht-degree: 12%

---


# ipsApiFault{#ipsapifault}

Syntaxis

## Typen fouten {#section-425697675cac4b2ab5c48bd463956401}

| ID | Fout |
|---|---|
| 30000 | `IPS_API_FAULT_CODE_EXCEPTION` |
| 30001 | `IPS_API_FAULT_CODE_INVALID_PARAMETER` |
| 30002 | `IPS_API_FAULT_CODE_MISSING_PARAMETER` |
| 30003 | `IPS_API_FAULT_CODE_INVALID_REQUEST_XML` |

## Foutvelden {#section-37fe1aef1d5f4ca480071ca933aba826}

| Naam | Type | Beschrijving |
|---|---|---|
| `code` | `xsd:int` | ID fout |
| `reason` | `xsd:string` | Een informatief bericht waarin de fout wordt beschreven. |


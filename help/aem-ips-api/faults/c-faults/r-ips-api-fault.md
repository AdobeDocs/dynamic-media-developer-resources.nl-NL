---
description: ipsApiFault
solution: Experience Manager
title: ipsApiFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 48be47f6-4c1c-4f19-afa7-f643e504c287
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
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

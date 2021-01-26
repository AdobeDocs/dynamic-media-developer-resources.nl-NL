---
description: Wordt gegenereerd wanneer een gebruiker niet kan worden geverifieerd.
solution: Experience Manager
title: authenticationFault
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 8%

---


# authenticationFault{#authenticationfault}

Wordt gegenereerd wanneer een gebruiker niet kan worden geverifieerd.

Syntaxis

## Typen fouten {#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | Fout |
|---|---|
| 10000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 10002 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## Foutvelden {#section-1fe84846a7154b03ab49552810ee9ac3}

| Naam | Type | Beschrijving |
|---|---|---|
| `code` | `xsd:int` | ID fout |
| `reason` | `xsd:string` | Een informatief bericht waarin de fout wordt beschreven. |

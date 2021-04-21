---
description: Bevat informatie over waarschuwings of foutenvoorwaarden die tijdens een verrichting van partijactiva worden geproduceerd. De code en redengebieden beantwoorden aan de gebieden van het foutenbericht die voor de gelijkwaardige niet partijverrichting zouden geworpen hebben.
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---


# AssetOperationFault{#assetoperationfault}

Bevat informatie over waarschuwings of foutenvoorwaarden die tijdens een verrichting van partijactiva worden geproduceerd. De code en redengebieden beantwoorden aan de gebieden van het foutenbericht die voor de gelijkwaardige niet partijverrichting zouden geworpen hebben.

Syntaxis

## Parameters {#section-c906f052f43e4785ba46d92b514b0923}

| Naam | Type | Beschrijving |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Asset handle for the failed operation. |
| `*`code`*` | `xsd:int` | Foutcode van de handeling. |
| `*`reden`*` | `xsd:string` | Foutbeschrijving of reden. |


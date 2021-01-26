---
description: Bevat informatie over waarschuwings of foutenvoorwaarden die tijdens een verrichting van partijactiva worden geproduceerd. De code en redengebieden beantwoorden aan de gebieden van het foutenbericht die voor de gelijkwaardige niet partijverrichting zouden geworpen hebben.
seo-description: Bevat informatie over waarschuwings of foutenvoorwaarden die tijdens een verrichting van partijactiva worden geproduceerd. De code en redengebieden beantwoorden aan de gebieden van het foutenbericht die voor de gelijkwaardige niet partijverrichting zouden geworpen hebben.
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
topic: Dynamic Media Image Production System API
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '126'
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


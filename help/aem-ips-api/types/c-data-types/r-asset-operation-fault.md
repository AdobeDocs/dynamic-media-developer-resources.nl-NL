---
title: AssetOperationFault
description: Bevat informatie over waarschuwings of foutenvoorwaarden die tijdens een verrichting van partijactiva worden geproduceerd. De code en redengebieden beantwoorden aan de gebieden van het foutenbericht die voor de gelijkwaardige niet partijverrichting zouden geworpen hebben.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# AssetOperationFault{#assetoperationfault}

Bevat informatie over waarschuwings of foutenvoorwaarden die tijdens een verrichting van partijactiva worden geproduceerd. De code en redengebieden beantwoorden aan de gebieden van het foutenbericht die voor de gelijkwaardige niet partijverrichting zouden geworpen hebben.

Syntaxis

## Parameters {#section-c906f052f43e4785ba46d92b514b0923}

| Naam | Type | Beschrijving |
|---|---|---|
| assetHandle | `xsd:string` | Asset handle for the failed operation. |
| code | `xsd:int` | Foutcode van de handeling. |
| reden | `xsd:string` | Foutbeschrijving of reden. |

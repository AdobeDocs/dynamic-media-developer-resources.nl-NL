---
description: Taakloggegevens.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# [!DNL JobLogDetail]{#joblogdetail}

Taakloggegevens.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| logMessage | `xsd:string` | Berichten in het taaklogboek. |
| logType | `xsd:string` | Het bestandstype Taaklog. |
| assetName | `xsd:string` | Naam van element in het taaklogboek (optioneel). |
| assetType | `xsd:string` | Keuze van het type element. |
| assetHandle | `xsd:string` | Asset handle waarnaar wordt verwezen in het taaklogbestand. |
| auxArray | `types:JobLogDetailAuxArray` | Verstrekt extra gedetailleerde informatie van het baanlogboek voorbij de vijf hierboven beschreven types van baanlogboek. |

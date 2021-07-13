---
description: Hoofdpad voor saveToFile=. Relatief pad voor de hoofdmap waarnaar afbeeldingen die zijn gegenereerd met req=saveToFile, moeten worden geschreven.
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 6e2814b9-898f-4cf4-8e4f-aa972d554213
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# SavePath{#savepath}

Hoofdpad voor saveToFile=. Relatief pad voor de hoofdmap waarnaar afbeeldingen die zijn gegenereerd met req=saveToFile, moeten worden geschreven.

`SavePath` is een tekenreekswaarde.

## Eigenschappen {#section-343d1371e966491c92854a8df14c3c50}

Tekstreeks. Moet leeg zijn of een geldig relatief mappad. Altijd gecombineerd met de absolute wortelweg die met `ImageServer::SaveDirectory` wordt gevormd.

## Standaard {#section-ae751eea97654f399c6aaee3f3252cbb}

Overgenomen van `default::SavePath` indien niet gedefinieerd. Opslaan naar bestanden is uitgeschakeld als de waarde voor omzetten leeg is.

## Zie ook {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)

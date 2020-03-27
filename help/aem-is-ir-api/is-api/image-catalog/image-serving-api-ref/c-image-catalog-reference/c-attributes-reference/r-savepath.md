---
description: Hoofdpad voor saveToFile=. Relatief pad voor de hoofdmap waarnaar afbeeldingen die zijn gegenereerd met req=saveToFile, moeten worden geschreven.
seo-description: Hoofdpad voor saveToFile=. Relatief pad voor de hoofdmap waarnaar afbeeldingen die zijn gegenereerd met req=saveToFile, moeten worden geschreven.
seo-title: SavePath
solution: Experience Manager
title: SavePath
topic: Scene7 Image Serving - Image Rendering API
uuid: 02b88e83-7fee-40d4-95ea-daba9a608e8e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SavePath{#savepath}

Hoofdpad voor saveToFile=. Relatief pad voor de hoofdmap waarnaar afbeeldingen die zijn gegenereerd met req=saveToFile, moeten worden geschreven.

`SavePath` is een tekenreekswaarde.

## Eigenschappen {#section-343d1371e966491c92854a8df14c3c50}

Tekstreeks. Moet leeg zijn of een geldig relatief mappad. Altijd gecombineerd met het absolute hoofdpad dat is geconfigureerd met `ImageServer::SaveDirectory`.

## Standaard {#section-ae751eea97654f399c6aaee3f3252cbb}

Overgenomen van `default::SavePath` indien niet gedefinieerd. Opslaan naar bestanden is uitgeschakeld als de waarde voor omzetten leeg is.

## Zie ook {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)

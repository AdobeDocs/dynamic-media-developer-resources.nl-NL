---
title: pscan
description: Progressieve JPEG-scan. Met de optie Progressieve JPEG wordt een afbeelding zo weergegeven dat deze in eerste instantie een vage foto of een foto van lage kwaliteit in zijn geheel weergeeft.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---

# pscan{#pscan}

Progressieve JPEG-scan. Met de optie Progressieve JPEG wordt een afbeelding zo weergegeven dat deze in eerste instantie een vage foto of een foto van lage kwaliteit in zijn geheel weergeeft. Naarmate het scannen doorgaat, wordt het duidelijker wanneer de afbeeldingsgegevens beter worden gedownload. Met deze parameter kunt u het aantal scans instellen dat nodig is (3, 4 of 5) voor de hele afbeelding.

`pscan=auto|3|4|5`

De werkelijke snelheid van elke scan is afhankelijk van de transmissiesnelheid van het systeem van de gebruiker en van de computer die de gegevens ontvangt en decomprimeert.

`Auto` gebruikt de scaninstellingen die worden berekend door de onafhankelijke JPEG-bibliotheek en die afhankelijk zijn van het kleurmodel. De waarden van `3`, `4`, `5` komt overeen met de instelling Scan in Adobe Photoshop wanneer u een JPEG-bestand opslaat als een JPEG-bestand (progressieve JPEG).

Indien `pscan` is niet ingesteld, wordt standaard ingesteld op `auto`.

## Eigenschappen {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Request-kenmerk. Is van toepassing ongeacht de huidige laaginstelling. Wordt genegeerd als de uitvoerindeling geen progressieve JPEG is.

## Standaard {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Voorbeeld {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Zie ook {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)

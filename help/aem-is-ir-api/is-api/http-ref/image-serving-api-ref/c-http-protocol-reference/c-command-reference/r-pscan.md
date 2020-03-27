---
description: Progressieve JPEG-scan. Met progressieve JPEG wordt een afbeelding zodanig weergegeven dat deze in eerste instantie een vage foto of een foto van lage kwaliteit in zijn geheel weergeeft. Naarmate het scannen doorgaat, wordt het duidelijker wanneer de afbeeldingsgegevens beter worden gedownload. Met deze parameter kunt u het aantal scans instellen dat nodig is (3, 4 of 5) voor de hele afbeelding.
seo-description: Progressieve JPEG-scan. Met progressieve JPEG wordt een afbeelding zodanig weergegeven dat deze in eerste instantie een vage foto of een foto van lage kwaliteit in zijn geheel weergeeft. Naarmate het scannen doorgaat, wordt het duidelijker wanneer de afbeeldingsgegevens beter worden gedownload. Met deze parameter kunt u het aantal scans instellen dat nodig is (3, 4 of 5) voor de hele afbeelding.
seo-title: pscan
solution: Experience Manager
title: pscan
topic: Scene7 Image Serving - Image Rendering API
uuid: c8e1d7a9-679c-437f-aa53-67aca3f40b30
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# pscan{#pscan}

Progressieve JPEG-scan. Met progressieve JPEG wordt een afbeelding zodanig weergegeven dat deze in eerste instantie een vage foto of een foto van lage kwaliteit in zijn geheel weergeeft. Naarmate het scannen doorgaat, wordt het duidelijker wanneer de afbeeldingsgegevens beter worden gedownload. Met deze parameter kunt u het aantal scans instellen dat nodig is (3, 4 of 5) voor de hele afbeelding.

`pscan=auto|3|4|5`

De werkelijke snelheid van elke scan is afhankelijk van de transmissiesnelheid van het systeem van de gebruiker en van de computer die de gegevens ontvangt en decomprimeert.

`Auto` gebruikt de scaninstellingen die worden berekend door de onafhankelijke JPEG-bibliotheek en die afhankelijk zijn van het kleurmodel. De waarden van `3`, `4`, `5` komen overeen met de instelling Scan in Adobe Photoshop wanneer u een JPEG-bestand opslaat als een JPEG-bestand (progressieve JPEG).

Als `pscan` niet is ingesteld, wordt standaard ingesteld op `auto`.

## Eigenschappen {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Request-kenmerk. Is van toepassing ongeacht de huidige laaginstelling. Genegeerd als de uitvoerindeling geen progressieve JPEG is.

## Standaard {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Voorbeeld {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Zie ook {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)

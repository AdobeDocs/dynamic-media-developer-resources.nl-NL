---
description: XMP metagegevens insluiten. Geeft aan of XMP metagegevens moeten worden opgenomen in de reactieafbeelding.
solution: Experience Manager
title: xmpEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# xmpEmbed{#xmpembed}

XMP metagegevens insluiten. Geeft aan of XMP metagegevens moeten worden opgenomen in de reactieafbeelding.

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP gegevens worden zonder wijzigingen van de bronafbeelding naar de reactieafbeelding doorgegeven. Hierdoor kunnen onjuiste gegevens worden ingesloten in de reactieafbeelding.

## Eigenschappen {#section-27024c4272f44d9a8c264a0629193af2}

Request-kenmerk. Genegeerd als de bronafbeelding geen XMP gegevens bevat. Alleen XMP gegevens uit de bronafbeelding van `layer=0` worden verwerkt. XMP gegevens uit andere laagafbeeldingen worden genegeerd.

Genegeerd als de indeling van de uitvoerafbeelding insluiten XMP niet ondersteunt. Zie de beschrijving van `fmt=` voor een lijst met uitvoerafbeeldingsindelingen die XMP insluiten ondersteunen.

## Standaard {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, voor het niet insluiten van paden in uitvoerafbeeldingen.

## Zie ook {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)

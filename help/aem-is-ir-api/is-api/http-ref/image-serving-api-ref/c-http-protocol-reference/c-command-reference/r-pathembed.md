---
description: Paden insluiten. Hiermee geeft u op of Photoshop-paden uit het bronafbeeldingsbestand van laag 0 moeten worden opgenomen in de reactieafbeelding.
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# pathEmbed{#pathembed}

Paden insluiten. Hiermee geeft u op of Photoshop-paden uit het bronafbeeldingsbestand van laag 0 moeten worden opgenomen in de reactieafbeelding.

`pathEmbed=0|1`

## Eigenschappen {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Request-kenmerk. Wordt genegeerd als de bronafbeelding geen padgegevens bevat. De padgegevens worden net als de afbeeldingsgegevens geschaald en geroteerd. Alleen paden uit de bronafbeelding van `layer=0` worden verwerkt; paden van andere laagafbeeldingen worden genegeerd.

Genegeerd als de indeling van de uitvoerafbeelding het insluiten van paden niet ondersteunt. Raadpleeg de beschrijving van `fmt=` voor een lijst met uitvoerafbeeldingsindelingen die paden insluiten ondersteunen.

## Beperkingen {#section-697cddb79a1542bc8457d2f4f59eec69}

Open Photoshop-paden (paden die geen gesloten lussen vormen) worden momenteel niet ondersteund voor insluiting in de reactieafbeelding.

## Standaard {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, voor het niet insluiten van paden in uitvoerafbeeldingen.

## Zie ook {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)

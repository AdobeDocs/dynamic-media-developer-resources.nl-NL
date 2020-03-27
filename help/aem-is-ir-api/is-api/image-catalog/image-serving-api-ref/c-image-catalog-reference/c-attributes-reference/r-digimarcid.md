---
description: Digimarc-gebruikersgegevens. Hier geeft u de gebruikersgegevens op voor insluiten van Digimarc.
seo-description: Digimarc-gebruikersgegevens. Hier geeft u de gebruikersgegevens op voor insluiten van Digimarc.
seo-title: DigimarcId
solution: Experience Manager
title: DigimarcId
topic: Scene7 Image Serving - Image Rendering API
uuid: 23f1952f-71b7-4b2a-917d-8161ea855ac9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DigimarcId{#digimarcid}

Digimarc-gebruikersgegevens. Hier geeft u de gebruikersgegevens op voor insluiten van Digimarc.

## Eigenschappen {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

Vijf of zes door komma&#39;s gescheiden gehele getallen. Het derde en vierde getal worden niet meer gebruikt:

`creator-id, creator-pin, durability [ , chroma ]`

De service `creator-id` en `creator-pin` worden geleverd door Digimarc wanneer de service wordt aangeschaft. De ongebruikte waarden moeten leeg blijven.

`durability` Hiermee geeft u de insluitingssterkte van het Digimarc-watermerk op. Het kan 1, 2, 3, of 4 zijn, met 1 die op zwakste en 4 sterkste duurzaamheid wijst.

Stel `chroma` in op 1 om het watermerk te coderen in de chrominantiegegevens van de afbeelding of op 0 (standaardwaarde) om het watermerk te coderen in de luminantie. Deze instelling wordt genegeerd bij het uitvoeren van grijswaardenafbeeldingen.

## Standaard {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

Overgenomen van `default::DigimarcId` indien niet gedefinieerd of indien leeg.

## Voorbeeld {#section-8469ae1c27b4461da3d53fbabc32d3c5}

Geef een test op voor de maker van Digimarc met een duurzaamheid ingesteld op 4.

`DigimarcId= 404407,32,,,4`

## Zie ook {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalogus::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)

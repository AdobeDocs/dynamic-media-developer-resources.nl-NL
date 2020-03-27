---
description: IP van de cliënt adresfilter. Staat specificatie van één of meerdere IP adressen of adreswaaiers toe.
seo-description: IP van de cliënt adresfilter. Staat specificatie van één of meerdere IP adressen of adreswaaiers toe.
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Scene7 Image Serving - Image Rendering API
uuid: b68f527b-7fa7-43e3-9517-57a6c3700b06
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# ClientAddressFilter{#clientaddressfilter}

IP van de cliënt adresfilter. Staat specificatie van één of meerdere IP adressen of adreswaaiers toe.

Wanneer gespecificeerd, zullen de verzoeken aan deze beeldcatalogus die van een cliënt bij een niet vermeld IP adres voortkomen worden verworpen. `localhost` maakt altijd impliciet deel uit van de `ClientAddressFilter` definitie, zelfs als deze niet expliciet wordt opgegeven. Verzoeken van `localhost` oorsprong worden nooit afgewezen, ongeacht het `ClientAddressFilter` productdossier.

## Eigenschappen {#section-21a2992f108d42fb8660c0d65aa61e13}

Lijst met door komma&#39;s gescheiden IP-adressen met optionele netmaskers ([CIDR-notatie](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) wordt gebruikt):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* IP-adres in *[!DNL ddd.ddd.ddd.ddd]* indeling

* *[!DNL netmask]* netmasker (0...32)

Dit kenmerk wordt genegeerd wanneer een regel voor voorbewerking met een `<addressfilter>` element wordt toegepast.

## Standaard {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Overgenomen van `default::AddressFilter` indien niet gedefinieerd of indien leeg.

## Voorbeelden {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Geen toegangsbeperkingen: `0.0.0.0/0`
* Toegang verlenen tot alle adressen die beginnen met `192: 192.0.0.0/8`
* Verleent toegang tot de 512 gastheren met adressen tussen `192.168.12.0` en `192.168.13.255: 192.168.12.0/23`

* Toegang verlenen tot één IP-adres: `192.168.2.117` of `192.168.2.117/32`

## Zie ook {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)

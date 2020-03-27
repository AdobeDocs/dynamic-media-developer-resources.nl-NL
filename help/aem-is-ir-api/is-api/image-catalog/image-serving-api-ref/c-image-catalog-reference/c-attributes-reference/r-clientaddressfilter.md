---
description: IP van de cliënt adresfilter. Staat specificatie van één of meerdere IP adressen of adreswaaiers toe.
seo-description: IP van de cliënt adresfilter. Staat specificatie van één of meerdere IP adressen of adreswaaiers toe.
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a557795-0caf-4b5f-974e-fb4c1481a83c
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# ClientAddressFilter{#clientaddressfilter}

IP van de cliënt adresfilter. Staat specificatie van één of meerdere IP adressen of adreswaaiers toe.

Wanneer gespecificeerd, zullen de verzoeken aan deze beeldcatalogus die van een cliënt bij een niet vermeld IP adres voortkomen worden verworpen.

## Eigenschappen {#section-d785265988324af68835410c9ba54147}

Lijst met door komma&#39;s gescheiden IP-adressen met optionele netmaskers (CIDR-notatie wordt gebruikt):

`*`ipAddress`*` `[`/ *`netmask`*`]`*`[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p>IP-adres in de indeling <span class="varname"> ddd.ddd.ddd</span> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> netmasker</span> </p></td> 
  <td class="stentry"> <p>Netmasker (0...32). </p></td> 
 </tr> 
</table>

Dit kenmerk wordt genegeerd wanneer een voorbewerkingsregel met een `<addressfilter>` element wordt toegepast.

## Standaard {#section-de26e8c9225745e985e4beac1f03f4f6}

Overgenomen van `default::AddressFilter` indien niet gedefinieerd of indien leeg.

## Voorbeelden {#section-a955314d2b6a4213a16c12a8b18d8627}

Geen toegangsbeperkingen: `0.0.0.0/0`

Toegang verlenen tot alle adressen vanaf 192: `192.0.0.0/8`

Toegang verlenen tot de 512 hosts met adressen tussen 192.168.12.0 en 192.168.13.255: `192.168.12.0/23`

Toegang verlenen tot één IP-adres: `192.168.2.117` of `192.168.2.117/32`

## Zie ook {#section-4ea89a7d82e14a4a800487d2d8801465}

[addressfilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)

---
description: IP van de cliënt adresfilter. Staat specificatie van één of meerdere IP adressen of adreswaaiers toe.
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# ClientAddressFilter{#clientaddressfilter}

IP van de cliënt adresfilter. Staat specificatie van één of meerdere IP adressen of adreswaaiers toe.

Wanneer gespecificeerd, worden de verzoeken aan deze beeldcatalogus die van een cliënt bij een niet vermeld IP adres voortkomen verworpen.

## Eigenschappen {#section-d785265988324af68835410c9ba54147}

Lijst met door komma&#39;s gescheiden IP-adressen met optionele netmaskers (CIDR-notatie wordt gebruikt):

`*`ipAddress`*` `[`/ *`netmask`*`]`&#42; `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p>IP-adres in <span class="varname"> ddd.ddd.ddd.ddd</span> gebruiken. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> netmasker</span> </p></td> 
  <td class="stentry"> <p>Netmasker (0...32). </p></td> 
 </tr> 
</table>

Dit kenmerk wordt genegeerd wanneer een preprocessing-regel met een `<addressfilter>` element wordt toegepast.

## Standaard {#section-de26e8c9225745e985e4beac1f03f4f6}

Overgenomen van `default::AddressFilter` indien niet gedefinieerd of leeg.

## Voorbeelden {#section-a955314d2b6a4213a16c12a8b18d8627}

Geen toegangsbeperkingen: `0.0.0.0/0`

Toegang verlenen tot alle adressen vanaf 192: `192.0.0.0/8`

Toegang verlenen tot de 512 hosts met adressen tussen 192.168.12.0 en 192.168.13.255: `192.168.12.0/23`

Toegang verlenen tot één IP-adres: `192.168.2.117` of `192.168.2.117/32`

## Zie ook {#section-4ea89a7d82e14a4a800487d2d8801465}

[addressfilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)

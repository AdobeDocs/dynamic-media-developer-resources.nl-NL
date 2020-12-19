---
description: Adresfilterelement. Optioneel in elementen <rule> en <pathrule>.
seo-description: Adresfilterelement. Optioneel in elementen <rule> en <pathrule>.
seo-title: addressfilter
solution: Experience Manager
title: addressfilter
topic: Scene7 Image Serving - Image Rendering API
uuid: 677eb19f-fd1a-4f74-8d55-6045baf01bf5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# addressfilter{#addressfilter}

Adresfilterelement. Optioneel in `<rule>`- en `<pathrule>`-elementen.

Overschrijft `attribute::ClientAddressFilter` wanneer de regel wordt toegepast.

## Kenmerken {#section-31e9ad29e9934933ac154bccbc729172}

Geen.

## Gegevens {#section-c762bdfe425140d689ea5abf25e9a48a}

Lijst met door komma&#39;s gescheiden IP-adressen. Elk individueel adres kan een facultatief netmasker achtervoegsel omvatten om specificatie van IP adreswaaiers toe te staan. Zie `attribute::ClientAddressFilter` voor meer informatie.

## Beschrijving {#section-d561b2485e004ef8a2085997d0f4bca6}

De toegang tot deze beeldcatalogus kan tot één of meerdere specifieke cliëntIP adressen worden beperkt door hen in een `<addressfilter>` element te specificeren. Een fout &quot;verzoek geweigerd&quot;wordt teruggekeerd aan de cliënt als het cliëntIP adres niet wordt aangepast.

Toegang is niet beperkt als `<addressfilter>` leeg is of niet is opgegeven.

Als `<expression>` in het `<rule>` element ontbreekt of leeg is, `<addressfilter>` wordt toegepast op alle verzoeken.

## Zie ook {#section-6f51ec2218d9450bb7642f9fdad1988a}

[kenmerk::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)

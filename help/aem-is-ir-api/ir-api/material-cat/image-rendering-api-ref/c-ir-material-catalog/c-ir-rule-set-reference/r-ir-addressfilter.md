---
description: Adresfilterelement. Optioneel in elementen <rule>. Hiermee wordt het kenmerk ClientAddressFilter genegeerd wanneer de regel wordt toegepast.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# addressfilter{#addressfilter}

Adresfilterelement. Optioneel in `<rule>`-elementen. Overschrijft kenmerk::ClientAddressFilter wanneer de regel wordt toegepast.

## Kenmerken {#section-e7a0960f7f0045da91de37824aa4aeaa}

Geen.

## Gegevens {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Lijst met door komma&#39;s gescheiden IP-adressen. Elk individueel adres kan een facultatief netmasker achtervoegsel omvatten om specificatie van IP adreswaaiers toe te staan. Zie ` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)` voor meer informatie.

## Beschrijving {#section-099b7839c4be40c68cbff29dad14e7d5}

De toegang tot deze beeldcatalogus kan tot één of meerdere specifieke IP adressen worden beperkt door hen in een `<addressfilter>` element te specificeren. Een fout &quot;verzoek geweigerd&quot;wordt teruggekeerd aan de cliënt als het cliëntIP adres niet wordt aangepast.

Toegang is niet beperkt als `<addressfilter>` leeg is of niet is opgegeven.

Als `<expression>` in het `<rule>` element ontbreekt of leeg is, `<addressfilter>` wordt toegepast op alle verzoeken.

`localhost` maakt altijd impliciet deel uit van de  `ClientAddressFilter` definitie, zelfs als deze niet expliciet wordt opgegeven. Verzoeken die afkomstig zijn van `localhost` worden nooit afgewezen, ongeacht de `ClientAddressFilter`-specificatie.

## SeeaOok {#section-02056065e0c042e1b155b2f3e5b84ef7}

[kenmerk::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)

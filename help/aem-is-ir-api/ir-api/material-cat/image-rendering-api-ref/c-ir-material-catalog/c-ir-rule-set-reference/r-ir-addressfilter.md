---
description: Adresfilterelement. Optioneel in <rule> elementen. Hiermee wordt het kenmerk ClientAddressFilter genegeerd wanneer de regel wordt toegepast.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# addressfilter{#addressfilter}

Adresfilterelement. Optioneel in `<rule>` elementen. Overschrijft kenmerk::ClientAddressFilter wanneer de regel wordt toegepast.

## Attributen {#section-e7a0960f7f0045da91de37824aa4aeaa}

Geen.

## Gegevens {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Lijst met door komma&#39;s gescheiden IP-adressen. Elk individueel adres kan een facultatief netmasker achtervoegsel omvatten om specificatie van IP adreswaaiers toe te staan. Zie [kenmerk::ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md) voor meer informatie.

## Beschrijving {#section-099b7839c4be40c68cbff29dad14e7d5}

De toegang tot deze beeldcatalogus kan tot één of meerdere specifieke IP adressen worden beperkt door hen in te specificeren `<addressfilter>` element. Een fout &quot;verzoek geweigerd&quot;wordt teruggekeerd aan de cliënt als het cliëntIP adres niet wordt aangepast.

Toegang is niet beperkt als `<addressfilter>` is leeg of niet opgegeven.

Als de `<expression>` in de `<rule>` element ontbreekt of leeg is, het `<addressfilter>` wordt toegepast op alle aanvragen.

`localhost` maakt altijd impliciet deel uit van de `ClientAddressFilter` definitie, zelfs als niet uitdrukkelijk gespecificeerd. Verzoeken van `localhost` nooit worden afgewezen, ongeacht `ClientAddressFilter` specificatie.

## Seeaalso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[kenmerk::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)

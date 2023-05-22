---
description: Modifier-tekenreeks voor postfix-verzoek. Geen of meer opdrachten Afbeeldingsservice gescheiden door '&' tekens.
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# PostModifier{#postmodifier}

Modifier-tekenreeks voor postfix-verzoek. Geen of meer opdrachten Afbeeldingsservice gescheiden door &#39;&amp;&#39; tekens.

Opdrachten in dit veld overschrijven opdrachten altijd in de HTTP-aanvraag en in `catalog::Modifier`.

`catalog::PostModifier` is handig als voor bepaalde afbeeldingen speciale instellingen nodig zijn die normaal gesproken via de URL worden beheerd, zoals `qlt=` of `resmode=`. `catalog::Modifier` moet worden gebruikt voor het instellen van de meeste IS-opdrachten in de afbeeldingscatalogus.

Macro&#39;s zijn toegestaan in `catalog::PostModifier`, zolang deze in dezelfde catalogus of in de standaardcatalogus zijn gedefinieerd. Ook aangepaste variabelen kunnen worden gebruikt.

>[!NOTE]
>
>Als een aanvraag meerdere lagen betreft, wordt alleen de inhoud van `catalog::PostModifier` van laag 0 wordt toegepast. `catalog::PostModifier` van alle andere lagen wordt genegeerd.

## Eigenschappen {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Tekstreeks. Optioneel.

## Standaard {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Geen.

## Zie ook {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalogus::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)

---
description: Modifier-tekenreeks voor postfix-verzoek. Geen of meer opdrachten Afbeeldingsservice gescheiden door '&' tekens.
seo-description: Modifier-tekenreeks voor postfix-verzoek. Geen of meer opdrachten Afbeeldingsservice gescheiden door '&' tekens.
seo-title: PostModifier
solution: Experience Manager
title: PostModifier
topic: Scene7 Image Serving - Image Rendering API
uuid: 8800a9b2-e9c0-498b-b4e1-37952ba7c842
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PostModifier{#postmodifier}

Modifier-tekenreeks voor postfix-verzoek. Geen of meer opdrachten Afbeeldingsservice gescheiden door &#39;&amp;&#39; tekens.

Opdrachten in dit veld overschrijven opdrachten in de HTTP-aanvraag en in `catalog::Modifier`.

`catalog::PostModifier` Dit is handig als bepaalde afbeeldingen speciale instellingen vereisen die normaal gesproken via de URL worden beheerd, zoals `qlt=` of `resmode=`. `catalog::Modifier` moet worden gebruikt voor het instellen van de meeste IS-opdrachten in de afbeeldingscatalogus.

Macro&#39;s zijn toegestaan in, `catalog::PostModifier`zolang ze in dezelfde catalogus of in de standaardcatalogus zijn gedefinieerd. Ook aangepaste variabelen kunnen worden gebruikt.

>[!NOTE]
>
>Als een verzoek meerdere lagen betreft, wordt alleen de inhoud van laag 0 toegepast. `catalog::PostModifier` `catalog::PostModifier` van alle andere lagen wordt genegeerd.

## Eigenschappen {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Tekstreeks. Optioneel.

## Standaard {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Geen.

## Zie ook {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalogus::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)

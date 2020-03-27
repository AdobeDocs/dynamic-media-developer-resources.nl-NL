---
description: Wordt gebruikt door MetadataField/type, saveMetadataFieldParam/fieldType en createMetadataField/fieldType.
seo-description: Wordt gebruikt door MetadataField/type, saveMetadataFieldParam/fieldType en createMetadataField/fieldType.
seo-title: Metagegevensveldtypen
solution: Experience Manager
title: Metagegevensveldtypen
topic: Scene7 Image Production System API
uuid: 57d292bb-848a-4e6e-bd08-4e6af1f9fc72
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# Metagegevensveldtypen{#metadata-field-types}

Wordt gebruikt door MetadataField/type, saveMetadataFieldParam/fieldType en createMetadataField/fieldType.

Syntaxis

## Values {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: Een speciaal geval van [!DNL `SingleFixedTag`] met een niet-wijzigbaar woordenboek dat aan de waarden [!DNL `True`] en [!DNL `False`]. wordt geïnitialiseerd.

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: Nul of meer tekenreekswaarden uit een gesloten woordenboek. Alleen beheerders kunnen het woordenboek wijzigen.
* [!DNL `MultiTag`]: Nul of meer tekenreekswaarden.
* [!DNL `SingleFixedTag`]: Een enkele tekenreekswaarde uit een gesloten woordenboek. Als `setAssetMetadata` of `batchSetAssetMetadata` wordt aangeroepen met een waarde die niet in het woordenboek staat, wordt een fout geretourneerd. Alleen beheerders kunnen het woordenboek wijzigen.

* [!DNL `SingleTag`]: Elke tekenreekswaarde.
* [!DNL `String`]


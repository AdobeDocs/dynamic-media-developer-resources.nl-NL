---
description: Wordt gebruikt door MetadataField/type, saveMetadataFieldParam/fieldType en createMetadataField/fieldType.
seo-description: Wordt gebruikt door MetadataField/type, saveMetadataFieldParam/fieldType en createMetadataField/fieldType.
seo-title: Metagegevensveldtypen
solution: Experience Manager
title: Metagegevensveldtypen
uuid: 57d292bb-848a-4e6e-bd08-4e6af1f9fc72
feature: Dynamic Media Classic,SDK/API,metagegevens
role: Ontwikkelaar,beheerder
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---


# Typen metagegevensvelden{#metadata-field-types}

Wordt gebruikt door MetadataField/type, saveMetadataFieldParam/fieldType en createMetadataField/fieldType.

Syntaxis

## Waarden {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: Een speciaal geval van  [!DNL `SingleFixedTag`] met een niet-wijzigbaar woordenboek dat aan de waarden  [!DNL `True`] en  [!DNL `False`]wordt geïnitialiseerd.

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: Nul of meer tekenreekswaarden uit een gesloten woordenboek. Alleen beheerders kunnen het woordenboek wijzigen.
* [!DNL `MultiTag`]: Nul of meer tekenreekswaarden.
* [!DNL `SingleFixedTag`]: Een enkele tekenreekswaarde uit een gesloten woordenboek. Als `setAssetMetadata` of `batchSetAssetMetadata` met een waarde niet in het woordenboek worden geroepen, zal een fout worden teruggekeerd. Alleen beheerders kunnen het woordenboek wijzigen.

* [!DNL `SingleTag`]: Elke tekenreekswaarde.
* [!DNL `String`]


---
description: Wordt gebruikt door MetadataField/type, saveMetadataFieldParam/fieldType en createMetadataField/fieldType.
solution: Experience Manager
title: Metagegevensveldtypen
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# Metagegevensveldtypen{#metadata-field-types}

Wordt gebruikt door MetadataField/type, saveMetadataFieldParam/fieldType en createMetadataField/fieldType.

Syntaxis

## Waarden {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: Een speciaal geval van [!DNL `SingleFixedTag`] met een niet-wijzigbaar woordenboek dat op de waarden wordt geïnitialiseerd [!DNL `True`] en [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: Nul of meer tekenreekswaarden uit een gesloten woordenboek. Alleen beheerders kunnen het woordenboek wijzigen.
* [!DNL `MultiTag`]: Nul of meer tekenreekswaarden.
* [!DNL `SingleFixedTag`]: Een enkele tekenreekswaarde uit een gesloten woordenboek. Indien `setAssetMetadata` of `batchSetAssetMetadata` worden aangeroepen met een waarde die niet in het woordenboek voorkomt, wordt een fout geretourneerd. Alleen beheerders kunnen het woordenboek wijzigen.

* [!DNL `SingleTag`]: Elke tekenreekswaarde.
* [!DNL `String`]

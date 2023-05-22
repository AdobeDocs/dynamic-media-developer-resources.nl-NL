---
description: Id
solution: Experience Manager
title: Id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d7b37180-cc93-41cd-bf14-5c262b046fbc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Id{#id}

Gewoonlijk is dit een korte en unieke id, zoals een SKU-nummer, mogelijk met een achtervoegsel, bijvoorbeeld als een SKU meerdere afbeeldingen heeft of landspecifieke variaties heeft. Dit kan ook een complexere tekenreeks zijn die meer lijkt op een bestandspad, ter ondersteuning van het eenvoudig aanpassen van websites met Image Serving.

>[!NOTE]
>
>De afbeeldings- en SVG-tabellen worden samengevoegd in één tabel wanneer de afbeeldingscatalogus wordt geladen. Id-waarden moeten in beide tabellen uniek zijn. De SVG-record wordt genegeerd als de afbeeldingstabel een record met dezelfde id-waarde bevat. De statische inhoud wordt beheerd met een afzonderlijke lijst; Items met statische inhoud en afbeeldingen/SVG-items kunnen dus dezelfde id-waarden hebben.

## Eigenschappen {#section-874a6853f67b4b229341ca76682884ae}

Tekstreeks. Vereist. Record-id voor de tabel met afbeeldings-/SVG- of statische inhoudsgegevens. Elk `catalog::Id` De waarde in deze afbeeldingscatalogus/SVG-catalogus of in deze catalogus met statische inhoud moet uniek zijn en mag geen &#39;,&#39;-tekens bevatten.

## Standaard {#section-a26e7d83a5ee44b5918baef82ee48e14}

Geen.

## Zie ook {#section-a258d818487d4ee6b7a99a65d18471a9}

[kenmerk::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)

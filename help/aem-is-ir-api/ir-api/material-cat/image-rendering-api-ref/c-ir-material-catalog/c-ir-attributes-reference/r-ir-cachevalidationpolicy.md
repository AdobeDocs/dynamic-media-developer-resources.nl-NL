---
description: Beleid voor validatie van servercache. Hiermee geeft u op wanneer cachemaringangen op de server worden gevalideerd.
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# CacheValidationPolicy{#cachevalidationpolicy}

Beleid voor validatie van servercache. Hiermee geeft u op wanneer cachemaringangen op de server worden gevalideerd.

Bij validatie op basis van vervaldatum worden de bronmaterialen en vignetten periodiek gecontroleerd om te zien of ze zijn gewijzigd. Bij validatie op basis van een catalogus worden bronafbeeldingen alleen gecontroleerd nadat de waarde `catalog::TimeStamp` is gewijzigd.

Validatie op basis van catalogi wordt aanbevolen wanneer zowel materiaal- als vignetcatalogi worden gebruikt. Validatie op basis van verlopen moet worden gebruikt wanneer in aanvragen voor het renderen van afbeeldingen rechtstreeks naar vignetten wordt verwezen.

## Eigenschappen {#section-46e13cb341eb442c86e0d8292de23ea0}

Enum. 0 om op vervaldatum gebaseerde validatie te selecteren. 1 om op catalogus gebaseerde cachevalidatie te selecteren.

## Standaard {#section-e09f3af8b6b3497d963199988dc5345d}

Overgenomen van `default::CacheValidationPolicy` indien niet gedefinieerd of indien leeg.

## Zie ook {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalogus::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)

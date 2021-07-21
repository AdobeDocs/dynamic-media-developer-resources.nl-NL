---
description: Hiermee wordt een zoekopdrachtrecord uit een PDF-bestand opgehaald.
solution: Experience Manager
title: SearchStrings
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 3f67ba8a-12dd-4698-9502-7cbdec9cb25d
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 1%

---

# SearchStrings{#searchstrings}

Hiermee wordt een zoekopdrachtrecord uit een PDF-bestand opgehaald.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| `*`searchString`*` | `xsd:string` | Tekenreeks zoeken. |
| `*`keywordsArray`*` | `types:KeywordsArray` | Array met trefwoorden in de zoektekenreeks. |
| `*`status`*` | `xsd:boolean` | True if the search string is valid and enabled. |
| `*`x`*` | `xsd:int` | X-aspositie van de zoektekenreeks. |
| `*`y`*` | `xsd:int` | Y-aspositie van de zoektekenreeks. |
| `*`width`*` | `xsd:int` | Tekenreeksbreedte zoeken. |
| `*`height`*` | `xsd:int` | Hoogte van zoekreeks. |
| `*`fontName`*` | `xsd:string` | Naam van het lettertype dat in de zoekreeks wordt gebruikt. |
| `*`pointSize`*` | `xsd:string` | Tekengrootte. |

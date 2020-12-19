---
description: Hiermee wordt een zoekopdrachtrecord uit een PDF-bestand opgehaald.
seo-description: Hiermee wordt een zoekopdrachtrecord uit een PDF-bestand opgehaald.
seo-title: SearchStrings
solution: Experience Manager
title: SearchStrings
topic: Scene7 Image Production System API
uuid: aade2741-3e77-44c6-ab3c-0810ff034412
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 1%

---


# SearchStrings{#searchstrings}

Hiermee wordt een zoekopdrachtrecord uit een PDF-bestand opgehaald.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| ` *`searchString`*` | `xsd:string` | Tekenreeks zoeken. |
| ` *`keywordsArray`*` | `types:KeywordsArray` | Array met trefwoorden in de zoektekenreeks. |
| ` *`status`*` | `xsd:boolean` | True if the search string is valid and enabled. |
| ` *`x`*` | `xsd:int` | X-aspositie van de zoektekenreeks. |
| ` *`y`*` | `xsd:int` | Y-aspositie van de zoektekenreeks. |
| ` *`width`*` | `xsd:int` | Tekenreeksbreedte zoeken. |
| ` *`height`*` | `xsd:int` | Hoogte van zoekreeks. |
| ` *`fontName`*` | `xsd:string` | Naam van het lettertype dat in de zoekreeks wordt gebruikt. |
| ` *`pointSize`*` | `xsd:string` | Tekengrootte. |


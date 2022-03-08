---
description: Een metagegevensveld dat wordt geretourneerd door searchAssets.
solution: Experience Manager
title: Metagegevens
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 62e3e215-31ea-49fd-937e-d136fdf84aff
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 1%

---

# Metagegevens{#metadata}

Een metagegevensveld dat wordt geretourneerd door searchAssets.

Syntaxis

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Naam | Type | Beschrijving |
|---|---|---|
| name | `xsd:string` | Naam van metagegevens. |
| value | `xsd:string` | Waarde van metagegevens. |
| boolVal | `xsd:boolean` | Booleaanse metagegevenswaarde (alleen voor velden met een Booleaans type). |
| longVal | `xsd:long` | Lange metagegevenswaarde (alleen voor velden van het type int). |
| doubleVal | `xsd:double` | Dubbele metagegevenswaarde (alleen voor velden met floattype). |
| dateVal | `xsd:dateTime` | Waarde metagegevens datum (alleen voor datumvelden). |

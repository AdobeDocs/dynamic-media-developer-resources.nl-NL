---
description: Een metagegevensveld dat wordt geretourneerd door searchAssets.
solution: Experience Manager
title: Metagegevens
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 62e3e215-31ea-49fd-937e-d136fdf84aff
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 0%

---

# [!DNL Metadata]{#metadata}

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

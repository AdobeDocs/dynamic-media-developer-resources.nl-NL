---
description: Renderen van afbeeldingen ondersteunt materiaalcatalogi met ISO-8859-1- en UTF-8-codering.
seo-description: Renderen van afbeeldingen ondersteunt materiaalcatalogi met ISO-8859-1- en UTF-8-codering.
seo-title: Tekencodering
solution: Experience Manager
title: Tekencodering
topic: Dynamic Media Image Serving - Image Rendering API
uuid: efc3971b-dca1-4b47-a197-c10270ce17c9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# Tekencodering{#character-encoding}

Renderen van afbeeldingen ondersteunt materiaalcatalogi met ISO-8859-1- en UTF-8-codering.

Er wordt een BOM (byte order mark) gebruikt om de codering voor elk bestand op te geven. Voor UTF-8, is BOM de byteopeenvolging `EF BB BF`. Er wordt UTF-8-codering gebruikt wanneer deze tekensequentie helemaal aan het begin van elk materiaalcatalogusbestand wordt gedetecteerd. Bij elke andere bytevolgorde wordt het bestand geïnterpreteerd als gecodeerd volgens de ISO-8859-1-standaard.

Vele hedendaagse toepassingen, wanneer gevormd voor UTF-8, neem automatisch BOM op.

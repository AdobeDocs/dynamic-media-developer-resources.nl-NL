---
description: Renderen van afbeeldingen ondersteunt materiaalcatalogi met ISO-8859-1- en UTF-8-codering.
solution: Experience Manager
title: Tekencodering
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Tekencodering{#character-encoding}

Renderen van afbeeldingen ondersteunt materiaalcatalogi met ISO-8859-1- en UTF-8-codering.

Er wordt een BOM (byte order mark) gebruikt om de codering voor elk bestand op te geven. Voor UTF-8, is BOM de byteopeenvolging `EF BB BF`. Er wordt UTF-8-codering gebruikt wanneer deze tekensequentie helemaal aan het begin van elk materiaalcatalogusbestand wordt gedetecteerd. Bij elke andere bytevolgorde wordt het bestand geïnterpreteerd als gecodeerd volgens de ISO-8859-1-standaard.

Vele hedendaagse toepassingen, wanneer gevormd voor UTF-8, neem automatisch BOM op.

---
description: Image Serving ondersteunt afbeeldingcatalogi met ISO-8859-1- en UTF-8-codering.
seo-description: Image Serving ondersteunt afbeeldingcatalogi met ISO-8859-1- en UTF-8-codering.
seo-title: Tekencodering
solution: Experience Manager
title: Tekencodering
uuid: dfb56411-40d1-4bac-9213-9104ecba2a02
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# Tekencodering{#character-encoding}

Image Serving ondersteunt afbeeldingcatalogi met ISO-8859-1- en UTF-8-codering.

Er wordt een BOM (byte order mark) gebruikt om de codering voor elk bestand op te geven. Voor UTF-8, is BOM de byteopeenvolging `EF BB BF`. UTF-8-codering wordt gebruikt wanneer deze tekenreeks wordt gedetecteerd aan het begin van elk afbeeldingscatalogusbestand. Elke andere bytevolgorde leidt ertoe dat het bestand wordt geïnterpreteerd als gecodeerd aan de ISO-8859-1-standaard.

Vele hedendaagse toepassingen, wanneer gevormd voor UTF-8, neemt automatisch BOM op.

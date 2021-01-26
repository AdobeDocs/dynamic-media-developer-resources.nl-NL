---
description: Image Serving ondersteunt afbeeldingcatalogi met ISO-8859-1- en UTF-8-codering.
seo-description: Image Serving ondersteunt afbeeldingcatalogi met ISO-8859-1- en UTF-8-codering.
seo-title: Tekencodering
solution: Experience Manager
title: Tekencodering
topic: Dynamic Media Image Serving - Image Rendering API
uuid: dfb56411-40d1-4bac-9213-9104ecba2a02
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# Tekencodering{#character-encoding}

Image Serving ondersteunt afbeeldingcatalogi met ISO-8859-1- en UTF-8-codering.

Er wordt een BOM (byte order mark) gebruikt om de codering voor elk bestand op te geven. Voor UTF-8, is BOM de byteopeenvolging `EF BB BF`. UTF-8-codering wordt gebruikt wanneer deze tekenreeks wordt gedetecteerd aan het begin van elk afbeeldingscatalogusbestand. Elke andere bytevolgorde leidt ertoe dat het bestand wordt geïnterpreteerd als gecodeerd aan de ISO-8859-1-standaard.

Vele hedendaagse toepassingen, wanneer gevormd voor UTF-8, neemt automatisch BOM op.

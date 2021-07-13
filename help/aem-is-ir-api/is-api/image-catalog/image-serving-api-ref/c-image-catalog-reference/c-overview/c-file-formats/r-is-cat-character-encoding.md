---
description: Image Serving ondersteunt afbeeldingcatalogi met ISO-8859-1- en UTF-8-codering.
solution: Experience Manager
title: Tekencodering
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# Tekencodering{#character-encoding}

Image Serving ondersteunt afbeeldingcatalogi met ISO-8859-1- en UTF-8-codering.

Er wordt een BOM (byte order mark) gebruikt om de codering voor elk bestand op te geven. Voor UTF-8, is BOM de byteopeenvolging `EF BB BF`. UTF-8-codering wordt gebruikt wanneer deze tekenreeks wordt gedetecteerd aan het begin van elk afbeeldingscatalogusbestand. Elke andere bytevolgorde leidt ertoe dat het bestand wordt geïnterpreteerd als gecodeerd aan de ISO-8859-1-standaard.

Vele hedendaagse toepassingen, wanneer gevormd voor UTF-8, neemt automatisch BOM op.

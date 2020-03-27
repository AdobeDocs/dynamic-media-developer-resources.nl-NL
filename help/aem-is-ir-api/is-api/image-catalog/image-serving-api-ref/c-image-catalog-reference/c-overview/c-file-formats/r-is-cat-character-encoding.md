---
description: Image Serving ondersteunt afbeeldingcatalogi met ISO-8859-1- en UTF-8-codering.
seo-description: Image Serving ondersteunt afbeeldingcatalogi met ISO-8859-1- en UTF-8-codering.
seo-title: Tekencodering
solution: Experience Manager
title: Tekencodering
topic: Scene7 Image Serving - Image Rendering API
uuid: dfb56411-40d1-4bac-9213-9104ecba2a02
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Tekencodering{#character-encoding}

Image Serving ondersteunt afbeeldingcatalogi met ISO-8859-1- en UTF-8-codering.

Er wordt een BOM (byte order mark) gebruikt om de codering voor elk bestand op te geven. Voor UTF-8 is de BOM de bytevolgorde `EF BB BF`. UTF-8-codering wordt gebruikt wanneer deze tekenreeks wordt gedetecteerd aan het begin van elk afbeeldingscatalogusbestand. Elke andere bytevolgorde leidt ertoe dat het bestand wordt geïnterpreteerd als gecodeerd aan de ISO-8859-1-standaard.

Vele hedendaagse toepassingen, wanneer gevormd voor UTF-8, neemt automatisch BOM op.

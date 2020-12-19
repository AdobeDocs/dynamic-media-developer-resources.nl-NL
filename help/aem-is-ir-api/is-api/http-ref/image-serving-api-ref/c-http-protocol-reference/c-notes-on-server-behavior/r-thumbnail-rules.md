---
description: Houd rekening met deze miniatuurregels.
seo-description: Houd rekening met deze miniatuurregels.
seo-title: Miniatuurregels
solution: Experience Manager
title: Miniatuurregels
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Miniatuurregels{#thumbnail-rules}

Houd rekening met deze miniatuurregels.

1. Als `catalog::ThumbType=Crop`, dan wordt het (bebouwde) beeld geschraapt aan de kleinst mogelijke grootte terwijl nog het volledige doelrect bedekt. Als `catalog::ThumbType=Fit`, dan wordt het (bebouwde) beeld geschraapt aan de grootste mogelijke grootte terwijl nog het passen van het volledige beeld in de doelrect. Als `catalog::ThumbType=Texture`, wordt het (bebouwde) beeld geschraapt aan de verhouding van `catalog::ThumbRes` aan `catalog::Resolution`.
1. Lijn de geschaalde afbeelding op basis van `attribute::ThumbHorizAlign` en `attribute::ThumbVertAlign` uit met de doelrechthoek.
1. Snijd het resultaat bij naar de doelrechthoek.


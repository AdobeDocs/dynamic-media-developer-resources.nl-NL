---
description: Houd rekening met deze miniatuurregels.
solution: Experience Manager
title: Miniatuurregels
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# Miniatuurregels{#thumbnail-rules}

Houd rekening met deze miniatuurregels.

1. Als `catalog::ThumbType=Crop`, dan wordt het (bebouwde) beeld geschraapt aan de kleinst mogelijke grootte terwijl nog het volledige doelrect bedekt. Als `catalog::ThumbType=Fit`, dan wordt het (bebouwde) beeld geschraapt aan de grootste mogelijke grootte terwijl nog het passen van het volledige beeld in de doelrect. Als `catalog::ThumbType=Texture`, wordt het (bebouwde) beeld geschraapt aan de verhouding van `catalog::ThumbRes` aan `catalog::Resolution`.
1. Lijn de geschaalde afbeelding op basis van `attribute::ThumbHorizAlign` en `attribute::ThumbVertAlign` uit met de doelrechthoek.
1. Snijd het resultaat bij naar de doelrechthoek.


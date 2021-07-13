---
description: Houd rekening met deze miniatuurregels.
solution: Experience Manager
title: Miniatuurregels
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Miniatuurregels{#thumbnail-rules}

Houd rekening met deze miniatuurregels.

1. Als `catalog::ThumbType=Crop`, dan wordt het (bebouwde) beeld geschraapt aan de kleinst mogelijke grootte terwijl nog het volledige doelrect bedekt. Als `catalog::ThumbType=Fit`, dan wordt het (bebouwde) beeld geschraapt aan de grootste mogelijke grootte terwijl nog het passen van het volledige beeld in de doelrect. Als `catalog::ThumbType=Texture`, wordt het (bebouwde) beeld geschraapt aan de verhouding van `catalog::ThumbRes` aan `catalog::Resolution`.
1. Lijn de geschaalde afbeelding op basis van `attribute::ThumbHorizAlign` en `attribute::ThumbVertAlign` uit met de doelrechthoek.
1. Snijd het resultaat bij naar de doelrechthoek.

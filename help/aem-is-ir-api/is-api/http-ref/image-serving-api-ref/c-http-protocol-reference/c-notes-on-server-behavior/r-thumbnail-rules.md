---
description: Houd rekening met deze miniatuurregels.
solution: Experience Manager
title: Miniatuurregels
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# Miniatuurregels{#thumbnail-rules}

Houd rekening met deze miniatuurregels.

1. Indien `catalog::ThumbType=Crop`Vervolgens wordt de (uitgesneden) afbeelding zo klein mogelijk geschaald, terwijl de hele doelrechthoek nog steeds wordt bedekt. Indien `catalog::ThumbType=Fit`Vervolgens wordt de (uitgesneden) afbeelding zo groot mogelijk geschaald, terwijl de hele afbeelding wel in de doelrechthoek past. Indien `catalog::ThumbType=Texture`wordt de (uitgesneden) afbeelding geschaald naar de verhouding van `catalog::ThumbRes` tot `catalog::Resolution`.
1. De geschaalde afbeelding uitlijnen met de doelrechthoek op basis van `attribute::ThumbHorizAlign` en `attribute::ThumbVertAlign`.
1. Snijd het resultaat bij naar de doelrechthoek.

---
description: Lagen worden gepositioneerd door de oorsprong van de laag (origin=) uit te lijnen met de oorsprong van de achtergrondlaag bij een verschuiving die wordt opgegeven door pos=.
seo-description: Lagen worden gepositioneerd door de oorsprong van de laag (origin=) uit te lijnen met de oorsprong van de achtergrondlaag bij een verschuiving die wordt opgegeven door pos=.
seo-title: Laagplaatsing
solution: Experience Manager
title: Laagplaatsing
topic: Scene7 Image Serving - Image Rendering API
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# Laagplaatsing{#layer-placement}

Lagen worden gepositioneerd door de oorsprong van de laag (origin=) uit te lijnen met de oorsprong van de achtergrondlaag bij een verschuiving die wordt opgegeven door pos=.

Als de oorsprong van de laag niet expliciet is opgegeven voor een afbeeldingslaag, wordt deze als volgt berekend:

1. Bepaal het afbeeldingsanker. Gebruik `anchor=` of, indien niet opgegeven, `catalog::Anchor`.
1. Als het afbeeldingsanker is gedefinieerd, past u de laagtransformaties toe en `extend=` om de laag om te zetten in de waarde origin=.
1. Als er geen afbeeldingsanker is gedefinieerd, wordt de oorsprong van de laag in het midden van de laagrechthoek geplaatst (na toepassing van `extend=`).

![](assets/layerplacement.png)


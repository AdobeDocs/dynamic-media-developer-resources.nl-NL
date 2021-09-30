---
title: Laagplaatsing
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Laagplaatsing{#layer-placement}

Lagen worden gepositioneerd door de oorsprong van de laag (origin=) uit te lijnen met de oorsprong van de achtergrondlaag bij een verschuiving die wordt opgegeven door pos=.

Als de oorsprong van de laag niet expliciet is opgegeven voor een afbeeldingslaag, wordt deze als volgt berekend:

1. Bepaal het afbeeldingsanker. Gebruik `anchor=` of, indien niet opgegeven, `catalog::Anchor`.
1. Als het afbeeldingsanker is gedefinieerd, past u de laagtransformaties toe en `extend=` om de laag om te zetten in de waarde origin=.
1. Als er geen afbeeldingsanker is gedefinieerd, wordt de oorsprong van de laag in het midden van de laagrechthoek geplaatst (na toepassing van `extend=`).

![Laag plaatsen, afbeelding](assets/layerplacement.png)

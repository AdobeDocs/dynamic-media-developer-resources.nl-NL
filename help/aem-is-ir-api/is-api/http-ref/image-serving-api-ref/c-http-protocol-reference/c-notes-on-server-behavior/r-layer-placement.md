---
description: Lagen worden gepositioneerd door de oorsprong van de laag (origin=) uit te lijnen met de oorsprong van de achtergrondlaag bij een verschuiving die wordt opgegeven door pos=.
solution: Experience Manager
title: Laagplaatsing
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# Laagplaatsing{#layer-placement}

Lagen worden gepositioneerd door de oorsprong van de laag (origin=) uit te lijnen met de oorsprong van de achtergrondlaag bij een verschuiving die wordt opgegeven door pos=.

Als de oorsprong van de laag niet expliciet is opgegeven voor een afbeeldingslaag, wordt deze als volgt berekend:

1. Bepaal het afbeeldingsanker. Gebruik `anchor=` of, indien niet opgegeven, `catalog::Anchor`.
1. Als het afbeeldingsanker is gedefinieerd, past u de laagtransformaties toe en `extend=` om de laag om te zetten in de waarde origin=.
1. Als er geen afbeeldingsanker is gedefinieerd, wordt de oorsprong van de laag in het midden van de laagrechthoek geplaatst (na toepassing van `extend=`).

![](assets/layerplacement.png)

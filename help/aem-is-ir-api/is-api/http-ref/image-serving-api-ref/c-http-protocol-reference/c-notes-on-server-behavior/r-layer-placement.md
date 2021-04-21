---
description: Lagen worden gepositioneerd door de oorsprong van de laag (origin=) uit te lijnen met de oorsprong van de achtergrondlaag bij een verschuiving die wordt opgegeven door pos=.
solution: Experience Manager
title: Laagplaatsing
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# Laagplaatsing{#layer-placement}

Lagen worden gepositioneerd door de oorsprong van de laag (origin=) uit te lijnen met de oorsprong van de achtergrondlaag bij een verschuiving die wordt opgegeven door pos=.

Als de oorsprong van de laag niet expliciet is opgegeven voor een afbeeldingslaag, wordt deze als volgt berekend:

1. Bepaal het afbeeldingsanker. Gebruik `anchor=` of, indien niet opgegeven, `catalog::Anchor`.
1. Als het afbeeldingsanker is gedefinieerd, past u de laagtransformaties toe en `extend=` om de laag om te zetten in de waarde origin=.
1. Als er geen afbeeldingsanker is gedefinieerd, wordt de oorsprong van de laag in het midden van de laagrechthoek geplaatst (na toepassing van `extend=`).

![](assets/layerplacement.png)


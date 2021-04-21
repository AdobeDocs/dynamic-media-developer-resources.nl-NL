---
description: Stel de tekstknooppuntwaarde in voor s7 elementID.
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---


# setVal{#setval}

Stel de tekstknooppuntwaarde in voor s7:elementID.

`setVal.elementID= *[!DNL value]*`

Als voor een FXG-knooppuntelement een `s7:elementID` is gedefinieerd, kan de tekstwaarde voor dat knooppunt worden gemanipuleerd.

## Voorbeeld {#section-f574fd66dedd4a219aa537d7bdabea23}

Stel dat een `s7:elementID="paragraph1"`-kenmerk is gedefinieerd voor een `TextGraphic`-knooppunt, dan is het volgende geldig:

`&setVal.paragraph=Hello`

In dit voorbeeld wordt de tekstwaarde voor het alineaknooppunt ingesteld op &quot;Hello&quot;.

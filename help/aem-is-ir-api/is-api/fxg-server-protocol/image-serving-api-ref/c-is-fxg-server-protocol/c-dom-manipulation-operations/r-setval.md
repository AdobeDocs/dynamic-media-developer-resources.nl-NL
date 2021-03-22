---
description: Stel de tekstknooppuntwaarde in voor s7 elementID.
seo-description: Stel de tekstknooppuntwaarde in voor s7 elementID.
seo-title: setVal
solution: Experience Manager
title: setVal
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '75'
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

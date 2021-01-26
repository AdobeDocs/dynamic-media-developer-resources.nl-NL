---
description: Stel de tekstknooppuntwaarde in voor s7 elementID.
seo-description: Stel de tekstknooppuntwaarde in voor s7 elementID.
seo-title: setVal
solution: Experience Manager
title: setVal
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
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

---
description: Stel XML in op een s7 elementID.
solution: Experience Manager
title: setElement
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---


# setElement{#setelement}

Stel XML in op een s7:elementID.

`setElement.elementID=<XML>`

Als voor een FXG-knooppuntelement een `s7:elementID` is gedefinieerd, wordt de waarde `<XML>` vervangen als een onderliggend element. De `<XML>` moet worden gecodeerd.

## Voorbeeld {#section-f23a998b18994dd3b5d4e1965718db9f}

Stel dat een `s7:elementID="group2"`-kenmerk is gedefinieerd voor een `Group`-knooppunt, dan is het volgende geldig:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In dit voorbeeld worden alle onderliggende items van het knooppunt `group2`verwijderd en vervangen door het nieuwe onderliggende knooppunt `TextGraphic`.

---
description: Stel XML in op een s7 elementID.
seo-description: Stel XML in op een s7 elementID.
seo-title: setElement
solution: Experience Manager
title: setElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setElement{#setelement}

Stel XML in op een s7:elementID.

`setElement.elementID=<XML>`

Als voor een FXG-knooppuntelement een `s7:elementID` definitie is opgegeven, wordt de `<XML>` waarde vervangen als een onderliggend element. The `<XML>` must be encoded.

## Voorbeeld {#section-f23a998b18994dd3b5d4e1965718db9f}

Stel dat een `s7:elementID="group2"` kenmerk is gedefinieerd voor een `Group` knooppunt, dan is het volgende geldig:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In dit voorbeeld worden alle onderliggende items van het `group2`knooppunt verwijderd en vervangen door het nieuwe `TextGraphic` onderliggende knooppunt.

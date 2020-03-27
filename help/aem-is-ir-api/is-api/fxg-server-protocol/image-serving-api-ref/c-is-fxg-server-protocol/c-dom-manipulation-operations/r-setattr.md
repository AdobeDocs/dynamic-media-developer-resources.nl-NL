---
description: Plaats om het even welk attribuut voor bepaalde s7 elementID.
seo-description: Plaats om het even welk attribuut voor bepaalde s7 elementID.
seo-title: setAttr
solution: Experience Manager
title: setAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: 968f7496-3cd4-4670-96fc-53127bba9a83
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAttr{#setattr}

Plaats om het even welk attribuut voor bepaalde s7:elementID.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Als voor een FXG-knooppuntelement een `s7:elementID` definitie is opgegeven, kunt u de kenmerken voor dat knooppunt manipuleren. U kunt zoveel kenmerk-/waardeparen instellen als u wilt. De attributen te hoeven niet reeds in FXG worden bepaald maar het moet voor het knoopelement geldig zijn. Alle tussenliggende waarden `{}` moeten worden overgeslagen.

## Voorbeeld {#section-9c37470d5f0349e5b0a97291782cb7a6}

Stel dat een `s7:elementID="Group1"` kenmerk is gedefinieerd voor een `BitmapGraphic` knooppunt, dan is het volgende geldig:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

In dit voorbeeld worden de waarden *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* en *[!DNL scaleY]* voor de `BitmapGraphic` en overschrijft de bestaande waarden.

---
description: Plaats om het even welk attribuut voor bepaalde s7 elementID.
seo-description: Plaats om het even welk attribuut voor bepaalde s7 elementID.
seo-title: setAttr
solution: Experience Manager
title: setAttr
uuid: 968f7496-3cd4-4670-96fc-53127bba9a83
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# setAttr{#setattr}

Plaats om het even welk attribuut voor bepaalde s7:elementID.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Als voor een FXG-knooppuntelement een `s7:elementID` is gedefinieerd, kunt u de kenmerken voor dat knooppunt manipuleren. U kunt zoveel kenmerk-/waardeparen instellen als u wilt. De attributen te hoeven niet reeds in FXG worden bepaald maar het moet voor het knoopelement geldig zijn. Alle waarden tussen `{}` moeten worden overgeslagen.

## Voorbeeld {#section-9c37470d5f0349e5b0a97291782cb7a6}

Stel dat een `s7:elementID="Group1"`-kenmerk is gedefinieerd voor een `BitmapGraphic`-knooppunt, dan is het volgende geldig:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

In dit voorbeeld worden de *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* en *[!DNL scaleY]* voor `BitmapGraphic` ingesteld en worden bestaande waarden genegeerd.

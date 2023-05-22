---
description: Plaats om het even welk attribuut voor bepaalde s7 elementID.
solution: Experience Manager
title: setAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# setAttr{#setattr}

Plaats om het even welk attribuut voor bepaalde s7:elementID.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Als een FXG-knoopelement een `s7:elementID` gedefinieerd, kunt u de kenmerken voor dat knooppunt manipuleren. U kunt zoveel kenmerk-/waardeparen instellen als u wilt. De attributen te hoeven niet reeds in FXG worden bepaald maar het moet voor het knoopelement geldig zijn. Alle waarden tussen `{}` moet worden afgeschaft.

## Voorbeeld {#section-9c37470d5f0349e5b0a97291782cb7a6}

Stel een `s7:elementID="Group1"` kenmerk is gedefinieerd voor een `BitmapGraphic` node, dan is het volgende geldig:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

In dit voorbeeld wordt het *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]*, en *[!DNL scaleY]* voor de `BitmapGraphic` en overschrijft bestaande waarden.

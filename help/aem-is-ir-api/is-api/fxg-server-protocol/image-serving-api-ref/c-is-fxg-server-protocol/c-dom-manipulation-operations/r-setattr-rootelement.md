---
description: Stel kenmerken in op FXG Root-element.
solution: Experience Manager
title: setAttr.rootElement
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 0%

---


# setAttr.rootElement{#setattr-rootelement}

Stel kenmerken in op FXG Root-element.

` setAttr.rootElement={ *[!DNL attributeName]*= *[!DNL attributeValue]*%26 *[!DNL attributeName]*= *[!DNL attributeValue]*}`

Met deze opdracht kunt u kenmerken van het hoofdelement bewerken.

## Voorbeeld {#section-2758a6e316c34b99b13b02147e5973bb}

Als wij het volgende wortelelement hebben:

`<Graphic version="1.0" viewHeight="692" viewWidth="792" s7:appVersion="1.0.0.11" ai:appVersion="14.0.0.367" d:id="1" xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008">`

Nadat u de volgende opdracht hebt toegepast:

`setAttr.rootElement={viewHeight=300%26viewWidth=200}`

Het hoofdelement wordt nu gewijzigd in:

`<Graphic xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008" ai:appVersion="14.0.0.367" d:id="1" s7:appVersion="1.0.0.11" version="1.0" viewHeight="300" viewWidth="200">`

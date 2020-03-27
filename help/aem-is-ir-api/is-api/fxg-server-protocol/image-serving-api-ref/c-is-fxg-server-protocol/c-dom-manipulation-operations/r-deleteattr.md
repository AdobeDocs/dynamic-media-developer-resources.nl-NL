---
description: Schrap om het even welk attribuut voor bepaalde s7 elementID.
seo-description: Schrap om het even welk attribuut voor bepaalde s7 elementID.
seo-title: deleteAttr
solution: Experience Manager
title: deleteAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: b1176c1a-9ec3-4a95-9f91-97f9f168c252
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteAttr{#deleteattr}

Schrap om het even welk attribuut voor bepaalde s7:elementID.

`deleteAttr.elementID={attributeName%26attributeName}`

Als er voor een FXG-knooppuntelement een `s7:elementID` definitie is opgegeven, kunnen de kenmerken voor dat knooppunt met deze opdracht worden verwijderd.

## Voorbeeld {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

In dit voorbeeld worden de kenmerken *[!DNL x]*, *[!DNL y]* en *[!DNL visible]* uit het oorspronkelijke FXG-knooppunt verwijderd.

---
description: Schrap om het even welk attribuut voor bepaalde s7 elementID.
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---


# deleteAttr{#deleteattr}

Schrap om het even welk attribuut voor bepaalde s7:elementID.

`deleteAttr.elementID={attributeName%26attributeName}`

Als een FXG knoopelement `s7:elementID` bepaald heeft, kunnen de attributen voor die knoop met dit bevel worden geschrapt.

## Voorbeeld {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

In dit voorbeeld worden de kenmerken *[!DNL x]*, *[!DNL y]* en *[!DNL visible]* uit het oorspronkelijke FXG-knooppunt verwijderd.

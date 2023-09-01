---
title: setVal
description: Plaats de waarde van de tekstknoop voor s7 elementID.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 0%

---

# setVal{#setval}

Stel de tekstknooppuntwaarde in voor s7:elementID.

`setVal.elementID= *[!DNL value]*`

Als een FXG-knoopelement een `s7:elementID` gedefinieerd, kan de tekstwaarde voor dat knooppunt worden gemanipuleerd.

## Voorbeeld {#section-f574fd66dedd4a219aa537d7bdabea23}

Stel een `s7:elementID="paragraph1"` kenmerk is gedefinieerd voor een `TextGraphic` en is het volgende geldig:

`&setVal.paragraph=Hello`

In dit voorbeeld wordt de tekstwaarde voor het alineaknooppunt ingesteld op &quot;Hello&quot;.

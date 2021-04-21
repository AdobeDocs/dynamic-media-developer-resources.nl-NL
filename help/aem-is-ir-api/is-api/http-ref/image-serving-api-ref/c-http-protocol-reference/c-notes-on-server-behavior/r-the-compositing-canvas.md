---
description: Als req=img, wordt de grootte van het samengestelde canvas volledig bepaald door de grootte van laag 0.
solution: Experience Manager
title: Het samengestelde canvas
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# Het samengestelde canvas{#the-compositing-canvas}

Als req=img, wordt de grootte van het samengestelde canvas volledig bepaald door de grootte van laag 0.

Als `size=` voor laag 0 niet uitdrukkelijk wordt gespecificeerd, worden de laagtransformaties gebruikt om de grootte van het compositing canvas (zie hieronder) te berekenen.

Als `req=tmb`, de grootte van het samenstellende canvas door `size=` wordt bepaald voor laag 0 wordt gespecificeerd, of, als de grootte niet wordt gespecificeerd, wordt de het samenstellen canvasgrootte geplaatst aan de meningsrect (zie hieronder).

---
description: Als req=img, wordt de grootte van het samengestelde canvas volledig bepaald door de grootte van laag 0.
solution: Experience Manager
title: Het samengestelde canvas
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# Het samengestelde canvas{#the-compositing-canvas}

Als req=img, wordt de grootte van het samengestelde canvas volledig bepaald door de grootte van laag 0.

Als `size=` voor laag 0 niet uitdrukkelijk wordt gespecificeerd, worden de laagtransformaties gebruikt om de grootte van het compositing canvas (zie hieronder) te berekenen.

Als `req=tmb`, de grootte van het samenstellende canvas door `size=` wordt bepaald voor laag 0 wordt gespecificeerd, of, als de grootte niet wordt gespecificeerd, wordt de het samenstellen canvasgrootte geplaatst aan de meningsrect (zie hieronder).

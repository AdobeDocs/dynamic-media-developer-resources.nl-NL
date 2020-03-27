---
description: Als req=img, wordt de grootte van het samengestelde canvas volledig bepaald door de grootte van laag 0.
seo-description: Als req=img, wordt de grootte van het samengestelde canvas volledig bepaald door de grootte van laag 0.
seo-title: Het samengestelde canvas
solution: Experience Manager
title: Het samengestelde canvas
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Het samengestelde canvas{#the-compositing-canvas}

Als req=img, wordt de grootte van het samengestelde canvas volledig bepaald door de grootte van laag 0.

Als `size=` voor laag 0 niet uitdrukkelijk wordt gespecificeerd, worden de laagtransformaties gebruikt om de grootte van het compositing canvas te berekenen (zie hieronder).

Als `req=tmb`de grootte van het samengestelde canvas wordt bepaald door de `size=` opgegeven grootte voor laag 0 of, als de grootte niet is opgegeven, wordt de grootte van het samengestelde canvas ingesteld op de weergaverechthoek (zie hieronder).

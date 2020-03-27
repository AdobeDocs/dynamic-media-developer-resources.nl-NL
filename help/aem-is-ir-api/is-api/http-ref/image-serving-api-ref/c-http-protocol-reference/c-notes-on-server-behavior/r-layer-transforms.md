---
description: Transformaties worden toegepast op bronafbeeldingen en tekstlagen.
seo-description: Transformaties worden toegepast op bronafbeeldingen en tekstlagen.
seo-title: Laagtransformaties
solution: Experience Manager
title: Laagtransformaties
topic: Scene7 Image Serving - Image Rendering API
uuid: b32b5af4-66ad-474a-9bca-4b6da8f43bf9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Laagtransformaties{#layer-transforms}

Transformaties worden toegepast op bronafbeeldingen en tekstlagen.

De volgende bewerkingen worden toegepast op bronafbeeldingen, in de gegeven volgorde, om de gewenste ruimtelijke relatie met laag 0 te bereiken:

1. Pas `crop=`indien opgegeven toe.
1. Schaal gebaseerd op `size=` of, als `size=` niet is opgegeven, gebaseerd op `scale=`, of, als `scale=` dit niet is opgegeven, gebaseerd op `res=`, of, als dit niet `res=`is opgegeven, de bronafbeelding met volledige resolutie gebruiken.
1. Pas `flip=`indien opgegeven toe.
1. Pas `rotate=`indien opgegeven toe.
1. Pas `extend=`indien opgegeven toe.
1. Plaats de laag op het canvas gebaseerd op `origin=` en `pos=` (zie hieronder).

De volgende transformaties worden toegepast op tekstlagen:

1. De grootte van het tekstvak wordt bepaald door `size=`, of de breedte en hoogte van de tekst, als deze `size=` geheel of gedeeltelijk zijn opgegeven. De tekst wordt binnen het tekstvak uitgelijnd met de tekstuitlijningskenmerken van de rtf. Tekst kan door het tekstvak worden bijgesneden.
1. Schaal de tekstinhoud op basis van de resolutie die u met hebt opgegeven `textAttr=`.
1. Pas `rotate=`indien opgegeven toe.
1. Pas `extend=`indien opgegeven toe.
1. Plaats de laag op het canvas gebaseerd op `origin=` en `pos=`(zie hieronder).

Voor zowel afbeeldings- als tekstlagen geldt de laatste stap waarbij de laag in het canvas wordt geplaatst, niet voor laag 0, aangezien laag 0 in feite het canvas vormt.

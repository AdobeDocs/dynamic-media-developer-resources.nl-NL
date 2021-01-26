---
description: Transformaties worden toegepast op bronafbeeldingen en tekstlagen.
seo-description: Transformaties worden toegepast op bronafbeeldingen en tekstlagen.
seo-title: Laagtransformaties
solution: Experience Manager
title: Laagtransformaties
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b32b5af4-66ad-474a-9bca-4b6da8f43bf9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Laagtransformaties{#layer-transforms}

Transformaties worden toegepast op bronafbeeldingen en tekstlagen.

De volgende bewerkingen worden toegepast op bronafbeeldingen, in de gegeven volgorde, om de gewenste ruimtelijke relatie met laag 0 te bereiken:

1. Pas `crop=` toe, indien opgegeven.
1. Schaal gebaseerd op `size=` of, als `size=` niet is opgegeven, gebaseerd op `scale=`, of, als `scale=` niet is opgegeven, gebaseerd op `res=`, of, als `res=`niet is opgegeven, de bronafbeelding met volledige resolutie gebruiken.
1. Pas `flip=` toe, indien opgegeven.
1. Pas `rotate=` toe, indien opgegeven.
1. Pas `extend=` toe, indien opgegeven.
1. Plaats de laag in het canvas op `origin=` en `pos=` wordt gebaseerd (zie hieronder).

De volgende transformaties worden toegepast op tekstlagen:

1. De grootte van het tekstvak wordt bepaald door `size=`, of de breedte en hoogte van de tekst, als `size=` slechts gedeeltelijk of helemaal niet is opgegeven. De tekst wordt binnen het tekstvak uitgelijnd met de tekstuitlijningskenmerken van de rtf. Tekst kan door het tekstvak worden bijgesneden.
1. Schaal de tekstinhoud die op de resolutie wordt gebaseerd die met `textAttr=` wordt gespecificeerd.
1. Pas `rotate=` toe, indien opgegeven.
1. Pas `extend=` toe, indien opgegeven.
1. Plaats de laag in het canvas op `origin=` en `pos=` (zie hieronder) wordt gebaseerd die.

Voor zowel afbeeldings- als tekstlagen geldt de laatste stap waarbij de laag in het canvas wordt geplaatst, niet voor laag 0, aangezien laag 0 in feite het canvas vormt.

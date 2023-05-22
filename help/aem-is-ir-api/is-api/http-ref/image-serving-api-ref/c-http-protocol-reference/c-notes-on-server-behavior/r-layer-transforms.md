---
description: Transformaties worden toegepast op bronafbeeldingen en tekstlagen.
solution: Experience Manager
title: Laagtransformaties
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# Laagtransformaties{#layer-transforms}

Transformaties worden toegepast op bronafbeeldingen en tekstlagen.

De volgende bewerkingen worden toegepast op bronafbeeldingen, in de gegeven volgorde, om de gewenste ruimtelijke relatie met laag 0 te bereiken:

1. Toepassen `crop=`, indien opgegeven.
1. Schalen op basis van `size=` of, indien `size=` is niet opgegeven, gebaseerd op `scale=`of, indien `scale=` is niet opgegeven, gebaseerd op `res=`of, indien `res=`niet is opgegeven, gebruikt u de bronafbeelding met volledige resolutie.
1. Toepassen `flip=`, indien opgegeven.
1. Toepassen `rotate=`, indien opgegeven.
1. Toepassen `extend=`, indien opgegeven.
1. De laag op het canvas plaatsen op basis van `origin=` en `pos=` (zie hieronder).

De volgende transformaties worden toegepast op tekstlagen:

1. De grootte van het tekstvak wordt bepaald door `size=`of de tekstbreedte en -hoogte, indien `size=` wordt slechts gedeeltelijk of helemaal niet verstrekt. De tekst wordt binnen het tekstvak uitgelijnd met de tekstuitlijningskenmerken van de rtf. Tekst kan door het tekstvak worden bijgesneden.
1. De tekstinhoud schalen op basis van de resolutie die is opgegeven met `textAttr=`.
1. Toepassen `rotate=`, indien opgegeven.
1. Toepassen `extend=`, indien opgegeven.
1. De laag op het canvas plaatsen op basis van `origin=` en `pos=`(zie hieronder).

Voor zowel afbeeldings- als tekstlagen geldt de laatste stap waarbij de laag in het canvas wordt geplaatst, niet voor laag 0, aangezien laag 0 in feite het canvas vormt.

---
description: Variabele dekking wordt ondersteund voor effen kleuren en herhaalbare structuren die worden toegepast op overlappende objecten, maar ook voor decals en vensterbedekkende materialen.
solution: Experience Manager
title: Dekking van variërend materiaal
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# Dekking van variërend materiaal{#varying-material-opacity}

Variabele dekking wordt ondersteund voor effen kleuren en herhaalbare structuren die worden toegepast op overlappende objecten, maar ook voor decals en vensterbedekkende materialen.

U kunt dekkingsinformatie eenvoudig verstrekken door een RGB-afbeelding met een alfakanaal te gebruiken. Bovendien kan de algehele dekking worden gevarieerd met de opdracht `opacity=` (zowel voor RGB- als RGBA-afbeeldingen).

De grenzen van de muur steunen ook beelden RGBA, hoofdzakelijk om die-cut grenzen te steunen.

De [!DNL vnw] dossiers die vensterbekledingen bepalen kunnen een opaciteitkanaal omvatten, dat door renderer met het alpha- kanaal van de herhaalbare textuur en de `opacity=` waarde wordt gecombineerd om een volledige waaier van opaciteitgevolgen voor zuivere en doorschijnende vensterbehandelingen te verstrekken.

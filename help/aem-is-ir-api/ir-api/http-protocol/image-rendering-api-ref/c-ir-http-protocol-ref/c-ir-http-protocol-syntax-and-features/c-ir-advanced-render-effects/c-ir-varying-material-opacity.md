---
description: Variabele dekking wordt ondersteund voor effen kleuren en herhaalbare structuren die worden toegepast op overlappende objecten, maar ook voor decals en vensterbedekkende materialen.
seo-description: Variabele dekking wordt ondersteund voor effen kleuren en herhaalbare structuren die worden toegepast op overlappende objecten, maar ook voor decals en vensterbedekkende materialen.
seo-title: Dekking van variërend materiaal
solution: Experience Manager
title: Dekking van variërend materiaal
topic: Scene7 Image Serving - Image Rendering API
uuid: 6af07ea8-44ba-4253-8a26-614725af2f46
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Dekking van variërend materiaal{#varying-material-opacity}

Variabele dekking wordt ondersteund voor effen kleuren en herhaalbare structuren die worden toegepast op overlappende objecten, maar ook voor decals en vensterbedekkende materialen.

U kunt dekkingsinformatie eenvoudig verstrekken door een RGB-afbeelding met een alfakanaal te gebruiken. Bovendien kan de algehele dekking worden gevarieerd met de opdracht `opacity=` (zowel voor RGB- als RGBA-afbeeldingen).

De grenzen van de muur steunen ook beelden RGBA, hoofdzakelijk om die-cut grenzen te steunen.

De [!DNL vnw] dossiers die vensterbekledingen bepalen kunnen een opaciteitkanaal omvatten, dat door renderer met het alpha- kanaal van de herhaalbare textuur en de `opacity=` waarde wordt gecombineerd om een volledige waaier van opaciteitgevolgen voor zuivere en doorschijnende vensterbehandelingen te verstrekken.

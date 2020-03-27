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

---


# Dekking van variërend materiaal{#varying-material-opacity}

Variabele dekking wordt ondersteund voor effen kleuren en herhaalbare structuren die worden toegepast op overlappende objecten, maar ook voor decals en vensterbedekkende materialen.

U kunt dekkingsinformatie eenvoudig verstrekken door een RGB-afbeelding met een alfakanaal te gebruiken. Bovendien kan de algemene dekking worden gevarieerd met de `opacity=` opdracht (zowel voor RGB- als voor RGBA-afbeeldingen).

De grenzen van de muur steunen ook beelden RGBA, hoofdzakelijk om die-cut grenzen te steunen.

De [!DNL vnw] bestanden die vensteromslagen definiëren, kunnen een dekkingskanaal bevatten, dat door de renderer wordt gecombineerd met het alfakanaal van de herhaalbare structuur en de `opacity=` waarde om een volledig bereik van dekkingseffecten te bieden voor eenvoudige en doorschijnende vensterbehandelingen.

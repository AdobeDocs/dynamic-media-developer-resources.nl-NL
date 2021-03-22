---
description: Variabele dekking wordt ondersteund voor effen kleuren en herhaalbare structuren die worden toegepast op overlappende objecten, maar ook voor decals en vensterbedekkende materialen.
seo-description: Variabele dekking wordt ondersteund voor effen kleuren en herhaalbare structuren die worden toegepast op overlappende objecten, maar ook voor decals en vensterbedekkende materialen.
seo-title: Dekking van variërend materiaal
solution: Experience Manager
title: Dekking van variërend materiaal
uuid: 6af07ea8-44ba-4253-8a26-614725af2f46
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---


# Dekking van variërend materiaal{#varying-material-opacity}

Variabele dekking wordt ondersteund voor effen kleuren en herhaalbare structuren die worden toegepast op overlappende objecten, maar ook voor decals en vensterbedekkende materialen.

U kunt dekkingsinformatie eenvoudig verstrekken door een RGB-afbeelding met een alfakanaal te gebruiken. Bovendien kan de algehele dekking worden gevarieerd met de opdracht `opacity=` (zowel voor RGB- als RGBA-afbeeldingen).

De grenzen van de muur steunen ook beelden RGBA, hoofdzakelijk om die-cut grenzen te steunen.

De [!DNL vnw] dossiers die vensterbekledingen bepalen kunnen een opaciteitkanaal omvatten, dat door renderer met het alpha- kanaal van de herhaalbare textuur en de `opacity=` waarde wordt gecombineerd om een volledige waaier van opaciteitgevolgen voor zuivere en doorschijnende vensterbehandelingen te verstrekken.

---
description: Variabele dekking wordt ondersteund voor effen kleuren en herhaalbare structuren die worden toegepast op overlappende objecten, maar ook voor decals en vensterbedekkende materialen.
solution: Experience Manager
title: Dekking van variërend materiaal
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Dekking van variërend materiaal{#varying-material-opacity}

Variabele dekking wordt ondersteund voor effen kleuren en herhaalbare structuren die worden toegepast op overlappende objecten, maar ook voor decals en vensterbedekkende materialen.

U kunt dekkingsinformatie eenvoudig verstrekken door een RGB-afbeelding met een alfakanaal te gebruiken. Bovendien kan de algehele dekking worden gevarieerd met de opdracht `opacity=` (zowel voor RGB- als RGBA-afbeeldingen).

De grenzen van de muur steunen ook beelden RGBA, hoofdzakelijk om die-cut grenzen te steunen.

De [!DNL vnw] dossiers die vensterbekledingen bepalen kunnen een opaciteitkanaal omvatten, dat door renderer met het alpha- kanaal van de herhaalbare textuur en de `opacity=` waarde wordt gecombineerd om een volledige waaier van opaciteitgevolgen voor zuivere en doorschijnende vensterbehandelingen te verstrekken.

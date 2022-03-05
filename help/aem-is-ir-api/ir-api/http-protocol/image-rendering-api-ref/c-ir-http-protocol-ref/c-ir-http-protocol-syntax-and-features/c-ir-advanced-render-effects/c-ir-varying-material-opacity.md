---
title: Dekking van variërend materiaal
description: Variabele dekking wordt ondersteund voor effen kleuren en herhaalbare structuren die worden toegepast op overlappende objecten, maar ook voor decals en vensterbedekkende materialen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Dekking van variërend materiaal{#varying-material-opacity}

Variabele dekking wordt ondersteund voor effen kleuren en herhaalbare structuren die worden toegepast op overlappende objecten, maar ook voor decals en vensterbedekkende materialen.

U kunt dekkingsinformatie eenvoudig opgeven door een RGB-afbeelding met een alfakanaal te gebruiken. Bovendien kan de totale dekking worden gevarieerd met de `opacity=` (zowel voor RGB- als RGBA-afbeeldingen).

De grenzen van de muur steunen ook beelden RGBA, hoofdzakelijk om die-cut grenzen te steunen.

De [!DNL vnw] bestanden die vensteroverdekkingen definiëren, kunnen een dekkingskanaal bevatten. Deze wordt door de renderer gecombineerd met het alfakanaal van de herhaalbare structuur en de `opacity=` waarde om een volledige waaier van opaciteitgevolgen voor zuivere en doorzichtige vensterbehandelingen te verstrekken.

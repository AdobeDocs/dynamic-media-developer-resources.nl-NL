---
description: De meeste materialen kunnen dynamisch worden gekleurd.
seo-description: De meeste materialen kunnen dynamisch worden gekleurd.
seo-title: Materialen inkleuren
solution: Experience Manager
title: Materialen inkleuren
topic: Scene7 Image Serving - Image Rendering API
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Materialen inkleuren{#colorizing-materials}

De meeste materialen kunnen dynamisch worden gekleurd.

Het inkleuringsalgoritme is tamelijk simplistisch en werkt het beste voor materiaalafbeeldingen met een beperkt kleurtoonbereik. Als u een materiaal wilt inkleuren, trekt de renderer de waarde `bgc=` af en voegt de waarde `color=` toe aan elke pixelwaarde.

Inkleuring is uitgeschakeld als `color=` niet is opgegeven. `bgc=` wordt genegeerd door kabinetsmateriaal; in plaats daarvan wordt de basiskleurwaarde gebruikt die in het  [!DNL vnc] bestand is ingesloten.

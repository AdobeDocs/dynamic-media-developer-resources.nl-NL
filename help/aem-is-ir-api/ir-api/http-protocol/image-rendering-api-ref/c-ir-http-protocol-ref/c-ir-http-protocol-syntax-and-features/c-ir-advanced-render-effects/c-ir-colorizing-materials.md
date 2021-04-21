---
description: De meeste materialen kunnen dynamisch worden gekleurd.
solution: Experience Manager
title: Materialen inkleuren
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Materialen inkleuren{#colorizing-materials}

De meeste materialen kunnen dynamisch worden gekleurd.

Het inkleuringsalgoritme is tamelijk simplistisch en werkt het beste voor materiaalafbeeldingen met een beperkt kleurtoonbereik. Als u een materiaal wilt inkleuren, trekt de renderer de waarde `bgc=` af en voegt de waarde `color=` toe aan elke pixelwaarde.

Inkleuring is uitgeschakeld als `color=` niet is opgegeven. `bgc=` wordt genegeerd door kabinetsmateriaal; in plaats daarvan wordt de basiskleurwaarde gebruikt die in het  [!DNL vnc] bestand is ingesloten.

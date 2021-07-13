---
description: De meeste materialen kunnen dynamisch worden gekleurd.
solution: Experience Manager
title: Materialen inkleuren
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# Materialen inkleuren{#colorizing-materials}

De meeste materialen kunnen dynamisch worden gekleurd.

Het inkleuringsalgoritme is tamelijk simplistisch en werkt het beste voor materiaalafbeeldingen met een beperkt kleurtoonbereik. Als u een materiaal wilt inkleuren, trekt de renderer de waarde `bgc=` af en voegt de waarde `color=` toe aan elke pixelwaarde.

Inkleuring is uitgeschakeld als `color=` niet is opgegeven. `bgc=` wordt genegeerd door kabinetsmateriaal; in plaats daarvan wordt de basiskleurwaarde gebruikt die in het  [!DNL vnc] bestand is ingesloten.

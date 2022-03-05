---
title: Materialen inkleuren
description: De meeste materialen kunnen dynamisch worden gekleurd.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# Materialen inkleuren{#colorizing-materials}

De meeste materialen kunnen dynamisch worden gekleurd.

Het inkleuringsalgoritme is simplistisch en werkt het beste voor materiaalafbeeldingen met een beperkt kleurtoonbereik. Als u een materiaal wilt inkleuren, verwijdert de renderer het `bgc=` en voegt de `color=` aan elke pixelwaarde.

Inkleuring is uitgeschakeld als `color=` is niet opgegeven. De `bgc=` kenmerk wordt genegeerd door materiaal in het kabinet; de basiskleurwaarde die is ingesloten in het dialoogvenster [!DNL vnc] wordt gebruikt.

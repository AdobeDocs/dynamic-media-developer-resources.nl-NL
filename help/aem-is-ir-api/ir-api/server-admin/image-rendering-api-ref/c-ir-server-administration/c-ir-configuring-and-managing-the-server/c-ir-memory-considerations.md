---
description: De hoeveelheid geheugen die door het renderen van afbeeldingen wordt gebruikt, kan sterk variëren en is sterk afhankelijk van de werkelijke serverbelasting en het werkelijke gebruik (bijvoorbeeld weinig of veel verschillende vignetten, grootte en complexiteit van vignetten, enzovoort).
solution: Experience Manager
title: Geheugenoverwegingen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# Geheugenoverwegingen{#memory-considerations}

De hoeveelheid geheugen die door het renderen van afbeeldingen wordt gebruikt, kan sterk variëren en is sterk afhankelijk van de werkelijke serverbelasting en het werkelijke gebruik (bijvoorbeeld weinig of veel verschillende vignetten, grootte en complexiteit van vignetten, enzovoort).

Voor de beste prestaties moet geheugenpaginering (swapping) worden vermeden.

Het teruggeven van het beeld deelt het geheugenbeheer van de Server van het Beeld. Als u afbeeldingen rendert, moet er extra geheugen worden toegewezen. 30 tot 50% van het fysieke geheugen kan redelijk zijn.

Verwijs naar het Beeld Servend documentatie voor informatie over hoe te om de het geheugentoewijzing van de Server van het Beeld te veranderen (ImageServer::physicalMemory).

---
description: De hoeveelheid geheugen die door het renderen van afbeeldingen wordt gebruikt, kan sterk variëren en is sterk afhankelijk van de werkelijke serverbelasting en het werkelijke gebruik (bijvoorbeeld weinig of veel verschillende vignetten, grootte en complexiteit van vignetten, enzovoort).
seo-description: De hoeveelheid geheugen die door het renderen van afbeeldingen wordt gebruikt, kan sterk variëren en is sterk afhankelijk van de werkelijke serverbelasting en het werkelijke gebruik (bijvoorbeeld weinig of veel verschillende vignetten, grootte en complexiteit van vignetten, enzovoort).
seo-title: Geheugenoverwegingen
solution: Experience Manager
title: Geheugenoverwegingen
topic: Scene7 Image Serving - Image Rendering API
uuid: 21247081-ff27-4237-93da-5fc996417dfd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Geheugenoverwegingen{#memory-considerations}

De hoeveelheid geheugen die door het renderen van afbeeldingen wordt gebruikt, kan sterk variëren en is sterk afhankelijk van de werkelijke serverbelasting en het werkelijke gebruik (bijvoorbeeld weinig of veel verschillende vignetten, grootte en complexiteit van vignetten, enzovoort).

Voor de beste prestaties moet geheugenpaginering (swapping) worden vermeden.

Het teruggeven van het beeld deelt het geheugenbeheer van de Server van het Beeld. Als u afbeeldingen rendert, moet er extra geheugen worden toegewezen. 30 tot 50% van het fysieke geheugen kan redelijk zijn.

Verwijs naar het Beeld Servend documentatie voor informatie over hoe te om de het geheugentoewijzing van de Server van het Beeld te veranderen (ImageServer::physicalMemory).

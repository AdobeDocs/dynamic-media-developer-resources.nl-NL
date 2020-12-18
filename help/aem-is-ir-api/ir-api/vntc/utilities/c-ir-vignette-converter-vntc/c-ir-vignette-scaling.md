---
description: Er worden vier algemene typen productivignetten ondersteund.
seo-description: Er worden vier algemene typen productivignetten ondersteund.
seo-title: Vignet schalen
solution: Experience Manager
title: Vignet schalen
topic: Scene7 Image Serving - Image Rendering API
uuid: 08c8f826-7dce-4bcb-9323-4892262eb578
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---


# Vignetschaling{#vignette-scaling}

Er worden vier algemene typen productivignetten ondersteund.

* Eén resolutie

   Wordt alleen aanbevolen als u zeker weet dat slechts één renderafbeelding nodig is.
* Meerdere resoluties

   Aanbevolen wanneer alle gewenste grootten van de renderafbeelding bekend zijn. Biedt een betere kwaliteit en snellere rendering dan bij vignetten met één resolutie en piramidevignetten, omdat de afbeelding na het renderen niet hoeft te worden geschaald.
* Piramide

   Dit is het meest geschikt. Dit wordt aanbevolen wanneer meerdere afbeeldingsgrootten nodig zijn en de exacte grootten niet vooraf zijn bepaald en wanneer een van de Scene7 Flash-zoomviewers wordt gebruikt.
* Piramide met een of meer aanvullende resoluties

   Biedt een hoge kwaliteit voor specifieke grootten en biedt tegelijkertijd nog steeds ondersteuning voor de flexibiliteit en zoomviewer.

In feite wordt elke resolutie als een onafhankelijke weergave met een eigen afbeeldingsbreedte en -hoogte opgeslagen in het productievenster.

De weergavegrootte van een vignet met één resolutie wordt opgegeven met `-width` of `-height` of beide. Als beide waarden zijn opgegeven, wordt het vignet zo geschaald dat geen van beide dimensies groter is dan de opgegeven grootte. Als geen van beide waarden is opgegeven, heeft het uitvoervignet dezelfde grootte als het invoervignet. Er wordt geen upscaling toegepast; als de opgegeven grootte groter is dan de grootte van het invoervignet, heeft het uitvoervignet dezelfde grootte als het invoervignet.

In feite gelden dezelfde regels voor vignetten met meerdere resoluties, waarbij het eerste resolutieniveau net zo groot is als een vignet met één resolutie. De extra resoluties worden gespecificeerd met extra komma-gescheiden waarden voor of `-width` of `-height`. Waarden hoeven niet te worden gesorteerd. Als `-width` veelvoudige waarden specificeert, dan `-height` moet slechts één enkele waarde verstrekken, en vice versa, anders is een fout teruggekeerd.

Er wordt een piramidevignet gemaakt door `-pyramid` op te geven. Het grootste resolutieniveau van een dergelijk vignet wordt precies bepaald als voor een vignet met één resolutie. De extra resolutieniveaus worden automatisch bepaald door elk niveau te schalen naar 0,5x het vorige niveau, waarbij het kleinste niveau niet meer dan 128x128 pixels bedraagt.

Er kunnen extra resolutieniveaus worden opgegeven voor een piramidevignet, net als voor een vignet met meerdere resoluties.

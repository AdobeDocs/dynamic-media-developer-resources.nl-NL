---
description: De server van het Platform plaatst al antwoordbeeld en bepaalde tekstgegevens in het voorgeheugen op schijf tenzij een verzoek als niet-cacheable wordt gemerkt.
seo-description: De server van het Platform plaatst al antwoordbeeld en bepaalde tekstgegevens in het voorgeheugen op schijf tenzij een verzoek als niet-cacheable wordt gemerkt.
seo-title: Responsgegevenscache
solution: Experience Manager
title: Responsgegevenscache
topic: Scene7 Image Serving - Image Rendering API
uuid: dbfda210-3b50-4e8c-8d77-7263ae4e80a2
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# Responsgegevenscache{#response-data-cache}

De server van het Platform plaatst al antwoordbeeld en bepaalde tekstgegevens in het voorgeheugen op schijf tenzij een verzoek als niet-cacheable wordt gemerkt.

De plaats van het de schijfgeheime voorgeheugen van de Server van het Platform wordt geplaatst met `PS::cache.rootPaths`.

Voor toepassingen met hoge aanraaksnelheden in het cachegeheugen kunt u de serverprestaties en -capaciteit verhogen door de cache met responsgegevens over meerdere schijfapparaten te verdelen. U doet dit door op elke schijf een cachehoofdmap te maken en deze te registreren `PS::cache.rootPaths`.

`PS::cache.maxSize` geeft de totale grootte van alle cachemarangen aan, zonder rekening te houden met overhead van het bestandssysteem. De werkelijk vereiste hoeveelheid schijfruimte is afhankelijk van de eigenschappen van het bestandssysteem, zoals de grootte van het schijfblok en het aantal cachemarangen. Het wordt aanbevolen tweemaal zoveel schijfruimte voor de HTTP-schijfcache te reserveren als de hoeveelheid die wordt opgegeven door `PS::cache.maxSize`. Er wordt een minst recent gebruikt algoritme gebruikt om de hoeveelheid gegevens in de cache binnen de limiet te houden.

Naast `PS::cache.maxSize`, wordt het reactiecache ook beheerd door het maximumaantal geheim voorgeheugeningangen met te beperken `PS::cache.maxEntries`. Op Linux moet deze instelling een waarde opgeven die niet groter is dan het aantal beschikbare inodes op de cachepartitie.

>[!NOTE]
>
>De server van het Platform handhaaft een in-geheugengeheim voorgeheugenindex. De grootte van deze index is 32 bytes keer de waarde van `PS::cache.maxEntries`. U moet mogelijk de heapgrootte van de Server van het Platform vergroten om grotere geheime voorgeheugens aan te passen.

Het systeem gebruikt een dossier van de geheim voorgeheugenindex dat aan schijf wordt opgeslagen wanneer de server op een ordelijke manier wordt gesloten. In het geval van onverwachte gebeurtenissen zoals een stroomstoring, wordt dit bestand mogelijk niet opgeslagen. Het kan ook enkele minuten duren voordat de Platform Server gereed is.

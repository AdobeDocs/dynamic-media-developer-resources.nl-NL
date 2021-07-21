---
description: De server van het Platform plaatst al antwoordbeeld en bepaalde tekstgegevens in het voorgeheugen op schijf tenzij een verzoek als niet-cacheable wordt gemerkt.
solution: Experience Manager
title: Responsgegevenscache
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Responsgegevenscache{#response-data-cache}

De server van het Platform plaatst al antwoordbeeld en bepaalde tekstgegevens in het voorgeheugen op schijf tenzij een verzoek als niet-cacheable wordt gemerkt.

De locatie van de schijfcache van de Platform Server wordt ingesteld met `PS::cache.rootPaths`.

Voor toepassingen met hoge aanraaksnelheden in het cachegeheugen kunt u de serverprestaties en -capaciteit verhogen door de cache met responsgegevens over meerdere schijfapparaten te verdelen. U doet dit door een cachemaritrootmap op elke schijf te maken en deze te registreren in `PS::cache.rootPaths`.

`PS::cache.maxSize` geeft de totale grootte van alle cachemarangen aan, zonder rekening te houden met overhead van het bestandssysteem. De werkelijk vereiste hoeveelheid schijfruimte is afhankelijk van de eigenschappen van het bestandssysteem, zoals de grootte van het schijfblok en het aantal cachemarangen. Het wordt aanbevolen tweemaal zoveel schijfruimte voor de HTTP-schijfcache te reserveren als de hoeveelheid die wordt opgegeven door `PS::cache.maxSize`. Er wordt een minst recent gebruikt algoritme gebruikt om de hoeveelheid gegevens in de cache binnen de limiet te houden.

Naast `PS::cache.maxSize`, wordt het reactiecache ook beheerd door het maximumaantal geheim voorgeheugeningangen met `PS::cache.maxEntries` te beperken. Op Linux moet deze instelling een waarde opgeven die niet groter is dan het aantal beschikbare inodes op de cachepartitie.

>[!NOTE]
>
>De server van het Platform handhaaft een in-geheugengeheim voorgeheugenindex. De grootte van deze index is 32 bytes keer de waarde van `PS::cache.maxEntries`. U moet mogelijk de heapgrootte van de Server van het Platform vergroten om grotere geheime voorgeheugens aan te passen.

Het systeem gebruikt een dossier van de geheim voorgeheugenindex dat aan schijf wordt opgeslagen wanneer de server op een ordelijke manier wordt gesloten. In het geval van onverwachte gebeurtenissen zoals een stroomstoring, wordt dit bestand mogelijk niet opgeslagen. Het kan ook enkele minuten duren voordat de Platform Server gereed is.

---
description: De [!DNL Platform Server] plaatst al antwoordbeeld en bepaalde tekstgegevens aan schijf in cache tenzij een verzoek als niet-cacheable wordt gemerkt.
solution: Experience Manager
title: Responsgegevenscache
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Responsgegevenscache{#response-data-cache}

De [!DNL Platform Server] plaatst al antwoordbeeld en bepaalde tekstgegevens aan schijf in cache tenzij een verzoek als niet-cacheable wordt gemerkt.

De locatie van de [!DNL Platform Server]De schijfcache van `PS::cache.rootPaths`.

Voor toepassingen met hoge aanraaksnelheden in het cachegeheugen kunt u de serverprestaties en -capaciteit verhogen door de cache met responsgegevens over meerdere schijfapparaten te verdelen. U doet dit door een cachehoofdmap op elke schijf te maken en deze te registreren in `PS::cache.rootPaths`.

`PS::cache.maxSize` geeft de totale grootte van alle cachemarangen aan, zonder rekening te houden met overhead van het bestandssysteem. De werkelijk vereiste hoeveelheid schijfruimte is afhankelijk van de eigenschappen van het bestandssysteem, zoals de grootte van het schijfblok en het aantal cachemarangen. Het wordt aanbevolen tweemaal zoveel schijfruimte voor de HTTP-schijfcache te reserveren als de hoeveelheid die wordt opgegeven door `PS::cache.maxSize`. Er wordt een minst recent gebruikt algoritme gebruikt om de hoeveelheid gegevens in de cache binnen de limiet te houden.

Naast `PS::cache.maxSize`, wordt het antwoordgeheime voorgeheugen ook beheerd door het maximumaantal geheim voorgeheugeningangen met te beperken `PS::cache.maxEntries`. Op Linux moet deze instelling een waarde opgeven die niet groter is dan het aantal beschikbare inodes op de cachepartitie.

>[!NOTE]
>
>De [!DNL Platform Server] houdt een cacheindex in het geheugen bij. De grootte van deze index is 32 bytes keer de waarde van `PS::cache.maxEntries`. Het kan nodig zijn om de [!DNL Platform Server] heapgrootte voor grotere caches.

Het systeem gebruikt een dossier van de geheim voorgeheugenindex dat aan schijf wordt opgeslagen wanneer de server op een ordelijke manier wordt gesloten. In het geval van onverwachte gebeurtenissen zoals een stroomstoring, wordt dit bestand mogelijk niet opgeslagen. Het kan ook enkele minuten duren voor de [!DNL Platform Server] klaar zijn.

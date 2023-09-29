---
title: Responsgegevenscache
description: De [!DNL Platform Server] plaatst alle antwoordbeelden en bepaalde tekstgegevens aan schijf in cache tenzij een verzoek als noncacheable wordt gemerkt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Responsgegevenscache{#response-data-cache}

De [!DNL Platform Server] plaatst alle antwoordbeelden en bepaalde tekstgegevens aan schijf in cache tenzij een verzoek als niet-cacheable wordt gemerkt.

De locatie van de [!DNL Platform Server]De schijfcache van `PS::cache.rootPaths`.

Voor toepassingen met hoge aanraaksnelheden in het cachegeheugen kunt u de serverprestaties en -capaciteit verhogen door de cache met responsgegevens over meerdere schijfapparaten te verdelen. U doet dit door een cachehoofdmap op elke schijf te maken en deze te registreren in `PS::cache.rootPaths`.

De `PS::cache.maxSize` geeft de totale grootte van alle cachemarangen aan, zonder rekening te houden met overhead van het bestandssysteem. De hoeveelheid vereiste schijfruimte is afhankelijk van de eigenschappen van het bestandssysteem, zoals de grootte van het schijfblok en het aantal cachemarangen. Reserveer tweemaal zoveel schijfruimte voor de HTTP-schijfcache als de hoeveelheid die wordt opgegeven door `PS::cache.maxSize`. Er wordt een minst recent gebruikt algoritme gebruikt om de hoeveelheid gegevens in de cache binnen de limiet te houden.

Naast `PS::cache.maxSize`, wordt het antwoordgeheime voorgeheugen ook beheerd door het maximumaantal geheim voorgeheugeningangen met te beperken `PS::cache.maxEntries`. In Linux® moet deze instelling een waarde opgeven die niet groter is dan het aantal beschikbare inodes op de cachepartitie.

>[!NOTE]
>
>De [!DNL Platform Server] houdt een cacheindex in het geheugen bij. De grootte van deze index is 32 bytes keer de waarde van `PS::cache.maxEntries`. Verhoog de [!DNL Platform Server] de heapgrootte, indien nodig, voor grotere caches.

Het systeem gebruikt een dossier van de geheim voorgeheugenindex dat aan schijf wordt opgeslagen wanneer de server op een ordelijke manier wordt gesloten. Als er onverwachte gebeurtenissen zijn, zoals een stroomstoring, wordt dit bestand mogelijk niet opgeslagen. Het kan ook enkele minuten duren voor de [!DNL Platform Server] om klaar te zijn.

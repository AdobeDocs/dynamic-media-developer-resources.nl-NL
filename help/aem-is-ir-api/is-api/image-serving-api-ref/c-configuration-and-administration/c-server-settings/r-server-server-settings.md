---
description: Gebruik deze serverinstellingen om uw server te configureren.
solution: Experience Manager
title: Server
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# Server{#server}

Gebruik deze serverinstellingen om uw server te configureren.

## SV::ImageServerMode — Afbeeldingsservermodus {#section-991b287f2dde4f77a24fc69d5b32cabd}

Zowel zijn een versie met 32 en 64 bits van de Server van het Beeld beschikbaar voor Linux. Specificeer ImageServer64 wanneer geïnstalleerd op de servers van Linux met 64 bits, of ImageServer32 (gebrek) wanneer geïnstalleerd op servers met 32 bits.

>[!NOTE]
>
>De 64-bits versie van de afbeeldingsserver ondersteunt geen FlashPix-bronbestanden.

>[!NOTE]
>
>64-bits modus wordt niet ondersteund in Windows. Alleen `ImageServer32` kan worden gespecificeerd. Anders wordt de service voor het renderen van afbeeldingen niet gestart.

## SV::PsHeapSize - [!DNL Platform Server] Grootte heap {#section-fd83715948764aeda58d6b3a9f9f8be9}

De Java-heapgrootte voor de [!DNL Platform Server]. Heeft als standaardwaarde &quot; `512m`&quot; (512 MB).

## IS::TcpPort, PS::isConnection.port - poort voor het luisteren van afbeeldingsservers {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Geeft de poort aan die wordt gebruikt voor communicatie tussen de [!DNL Platform Server] en de Afbeeldingsserver. Zorg ervoor om een havenaantal te specificeren dat niet anders op het gastheersysteem wordt gebruikt.

>[!NOTE]
>
>Voor een juiste werking van de afbeeldingsserver moet dezelfde waarde worden ingesteld voor `IS::TcpPort` en `PS::isConnection.port`.

## IS::Fysiek geheugen - Limiet voor imageservergeheugen {#section-85e37aa2ac6e456eb698da716dd3247d}

De maximale waarde bij benadering voor afbeeldingsgegevens in het geheugen, uitgedrukt als percentage van het fysieke geheugen. Geldige waarden zijn 10% tot 90%. De server van het Beeld probeert om zijn gebruik van beeldgeheugen tot de gespecificeerde hoeveelheid indien mogelijk te beperken. Deze limiet kan tijdelijk worden overschreden tijdens zware verwerkingsactiviteiten.

## IS::WorkerThreads - Aantal Image Server Worker Threads {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Het maximumaantal draden de Server van het Beeld gebruikt voor de verwerking van beeldgegevens. Het gebrek is 0, dat de Server van het Beeld toestaat om de draadtelling automatisch te optimaliseren.

Sommige werkende systemen hebben het verbinden modellen met hoge context-schakelende overheadkosten. In dergelijke omstandigheden kunnen de algemene serverprestaties verbeteren wanneer een specifieke draadtelling (bijvoorbeeld, één draad per cpu) wordt geselecteerd. U moet mogelijk experimenteren om de optimale instelling te vinden. Raadpleeg de opmerkingen bij de release Image Serving en de documentatie bij het besturingssysteem voor meer informatie.

## IS::NumberOfTextServers - Aantal instanties van de tekstserver {#section-971e20a90c1a473598fba738ed95671a}

Het maximumaantal tekstrenderers dat tegelijkertijd actief is. 0 (standaardwaarde) is gelijk aan 1,5 keer het aantal beschikbare CPU-cores.

## IS::TextServerTCPPortRange - Communicatiepoorten voor tekstserver {#section-a13465de88ed4df09931e5ba840c1942}

De poorten die moeten worden gebruikt voor communicatie met tekstservers. Geef het eerste en laatste poortnummer op, gescheiden door &#39;-&#39;.

---
description: Gebruik deze serverinstellingen om uw server te configureren.
seo-description: Gebruik deze serverinstellingen om uw server te configureren.
seo-title: Server
solution: Experience Manager
title: Server
topic: Scene7 Image Serving - Image Rendering API
uuid: 50db98cc-8354-4884-9416-00808828061b
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '357'
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
>64-bits modus wordt niet ondersteund in Windows. Alleen `ImageServer32` kan worden opgegeven. Anders wordt het porteren van de afbeelding niet gestart.

## SV::PsHeapSize - Grootte heap-server voor Platform {#section-fd83715948764aeda58d6b3a9f9f8be9}

De Java-heapgrootte voor de Platform Server. De standaardwaarde is &quot; `512m`&quot; (512 MB).

## IS::TcpPort, PS::isConnection.port - poort voor het luisteren van afbeeldingsservers {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Specificeert de haven die voor communicatie tussen de Server van het Platform en de Server van het Beeld wordt gebruikt. Zorg ervoor om een havenaantal te specificeren dat niet anders op het gastheersysteem wordt gebruikt.

>[!NOTE]
>
>Voor een correcte werking van de Beelddienst moet dezelfde waarde worden ingesteld voor `IS::TcpPort` en `PS::isConnection.port`.

## IS::Fysiek geheugen - Limiet voor imageservergeheugen {#section-85e37aa2ac6e456eb698da716dd3247d}

De maximale waarde bij benadering voor afbeeldingsgegevens in het geheugen, uitgedrukt als percentage van het fysieke geheugen. Geldige waarden zijn 10% tot 90%. De server van het Beeld probeert om zijn gebruik van beeldgeheugen tot de gespecificeerde hoeveelheid indien mogelijk te beperken. Deze limiet kan tijdelijk worden overschreden tijdens zware verwerkingsactiviteiten.

## IS::WorkerThreads - Aantal verbindingen van de Worker van de Server van het Beeld {#section-e2946063b13c4f728cdf5dba3d8b4de1}

Het maximumaantal draden de Server van het Beeld gebruikt voor de verwerking van beeldgegevens. Het gebrek is 0, dat de Server van het Beeld toestaat om de draadtelling automatisch te optimaliseren.

Sommige werkende systemen hebben het verbinden modellen met hoge context-schakelende overheadkosten. In dergelijke omstandigheden kunnen de algemene serverprestaties verbeteren wanneer een specifieke draadtelling wordt geselecteerd (bijvoorbeeld één draad per cpu). U moet mogelijk experimenteren om de optimale instelling te vinden. Raadpleeg de opmerkingen bij de release Image Serving en de documentatie bij het besturingssysteem voor meer informatie.

## IS::NumberOfTextServers - Aantal instanties van de tekstserver {#section-971e20a90c1a473598fba738ed95671a}

Het maximumaantal tekstrenderers dat tegelijkertijd actief is. 0 (standaardwaarde) is gelijk aan 1,5 keer het aantal beschikbare CPU-cores.

## IS::TextServerTCPPortRange - Communicatiepoorten voor tekstserver {#section-a13465de88ed4df09931e5ba840c1942}

De poorten die moeten worden gebruikt voor communicatie met tekstservers. Geef het eerste en laatste poortnummer op, gescheiden door &#39;-&#39;.

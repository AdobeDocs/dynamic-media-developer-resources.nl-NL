---
description: Gebruik deze serverinstellingen om fouten in het logbestand met overtrekken op te sporen.
solution: Experience Manager
title: Foutopsporing_tracering vastleggen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Foutopsporing_tracering vastleggen{#debug-trace-logging}

Gebruik deze serverinstellingen om fouten in het logbestand met overtrekken op te sporen.

>[!NOTE]
>
>Het wordt aanbevolen alle logbestanden te configureren die naar dezelfde map moeten worden geschreven als `TC::directory`. Dit zorgt ervoor dat alle logboekbestanden met afbeeldingsservers deelnemen aan de automatische rotatie van het logbestand die is geconfigureerd met `TC::maxDays`, die potentiële serverinstabiliteit door uit-van-schijf-ruimteomstandigheden zal verhinderen.

## SV::log - pad naar logboekbestand voor tracering van servertoezichthouder {#section-3697bc480ff646e79cacc2812c55ef26}

De omslag en de naam van het basisdossier voor het logboekdossiers van de Supervisor van de Server. Het pad kan absoluut of relatief zijn ten opzichte van *[!DNL install_folder]*. De servertoezichthouder voegt een afbreekstreepje en de huidige datum toe ( *[!DNL -yyyy-mm-dd]*) aan de bestandsnaam (vóór het eventuele achtervoegsel van het bestand). Het wordt aanbevolen alle logbestanden naar dezelfde map te sturen als [!DNL Platform Server] logbestanden ( `PS::LogFolder`) gebruiken om gebruik te maken van het beheer van logbestanden dat door de [!DNL Platform Server] ( `PS::LogDays`). Standaard is [!DNL logs/Supervisor.log].

>[!NOTE]
>
>U moet de nieuwe map maken voordat u deze instelling wijzigt. Zorg ervoor de toegangstoestemmingen worden geplaatst zodat de Supervisor van de Server noodzakelijk creeert, leest, en schrijft voorrechten.

## SV::traclevel - het Niveau van het Logboek van het Spoor van de Supervisor van de Server {#section-36f8634741da4c618d67aa628b5fe474}

Logniveau kan 1, 2, 3 of 4 zijn. De standaardwaarde is 2.

## IS::Logboek - Pad naar foutopsporingslogbestand van afbeeldingsserver {#section-73a3f09b77f2446c9f82207b7d8aec39}

De omslag en de basisdossier - naam voor de dossiers van het het spoorlogboek van de Server van het Beeld. Het pad kan absoluut of relatief zijn ten opzichte van *[!DNL install_folder]*. De ImageServer voegt een afbreekstreepje en de huidige datum toe ( *[!DNL -yyyy-mm-dd]*) aan de bestandsnaam (vóór het eventuele achtervoegsel van het bestand). Het wordt aanbevolen om logbestanden van de Image Server naar dezelfde map te verzenden als [!DNL Platform Server] logbestanden ( `PS::LogFolder`) gebruiken om gebruik te maken van het beheer van logbestanden dat door de [!DNL Platform Server] (zie `PS::LogDays`).

>[!NOTE]
>
>U moet de nieuwe map maken voordat u deze instelling wijzigt. Zorg ervoor de toegangstoestemmingen worden geplaatst zodat het Serven van het Beeld de noodzakelijke creeer, lees, en schrijf voorrechten heeft.

## IS:TraceClient - Logniveau foutopsporing van imageserver {#section-3851f1f68e404430985c629ac80534db}

Logniveau kan 1, 2, 3 of 4 zijn (standaardwaarde is 2)

Niveau 1 registreert gebeurtenissen met betrekking tot opstarten, sluiten, en [!DNL Platform Server] verbindingen.

Niveau 2 registreert ook het verbinden met en het losmaken van bronbeelden.

Niveau 3 voegt logboekregistratie toe van verzoeken om pixelgegevens en levering van dezelfde gegevens aan de [!DNL Platform Server].

Niveau 4 registreert alle berichten die van worden ontvangen [!DNL Platform Server].

Niveau 3 en 4 zouden slechts voor zuiveringsdoeleinden moeten worden gebruikt, aangezien de logboekdossiers zeer groot kunnen worden.

## IS::TraceStatsInterval - het Interval van het Logboek van de Statistieken van de Server van het Beeld {#section-1d8df96d61044e33a5b2b2b0309c2d59}

De server van het Beeld schrijft geheugenstatistieken aan zijn dossier van het spoorlogboek bij het interval dat door dit het plaatsen wordt gespecificeerd. Geldige waarden zijn 5 tot 86.400 seconden.

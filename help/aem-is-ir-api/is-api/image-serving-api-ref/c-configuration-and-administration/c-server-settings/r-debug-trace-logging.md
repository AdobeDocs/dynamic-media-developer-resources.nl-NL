---
description: Gebruik deze serverinstellingen om fouten in het logbestand met overtrekken op te sporen.
solution: Experience Manager
title: Foutopsporing_tracering vastleggen
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder,praktijkgericht
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---


# Debug_trace registreren{#debug-trace-logging}

Gebruik deze serverinstellingen om fouten in het logbestand met overtrekken op te sporen.

>[!NOTE]
>
>Het wordt aanbevolen alle logbestanden te configureren die naar dezelfde map moeten worden geschreven als `TC::directory`. Dit zorgt ervoor dat alle Logbestanden van Image Serving deelnemen aan de automatische rotatie van het logbestand die is geconfigureerd met `TC::maxDays`, waardoor potentiële serverinstabiliteit als gevolg van onvoldoende schijfruimte wordt voorkomen.

## SV::log - Server Supervisor Trace Log File Path {#section-3697bc480ff646e79cacc2812c55ef26}

De omslag en de naam van het basisdossier voor het logboekdossiers van de Supervisor van de Server. Het pad kan absoluut of relatief ten opzichte van *[!DNL install_folder]* zijn. De servertoezichthouder voegt een afbreekstreepje en de huidige datum ( *[!DNL -yyyy-mm-dd]*) toe aan de bestandsnaam (vóór het eventuele achtervoegsel van het bestand). Het wordt aanbevolen alle logbestanden naar dezelfde map als de logbestanden van de Platform-server ( `PS::LogFolder`) te verzenden om het beheer van logbestanden dat door de Platform-server ( `PS::LogDays`) is geïmplementeerd, te benutten. De standaardwaarde is [!DNL logs/Supervisor.log].

>[!NOTE]
>
>U moet de nieuwe map maken voordat u deze instelling wijzigt. Zorg ervoor de toegangstoestemmingen worden geplaatst zodat de Supervisor van de Server noodzakelijk creeert, leest, en schrijft voorrechten.

## SV::tracelevel - het Niveau van het Logboek van het Spoor van de Supervisor van de Server {#section-36f8634741da4c618d67aa628b5fe474}

Logniveau kan 1, 2, 3 of 4 zijn. De standaardwaarde is 2.

## IS::Log - Foutopsporingspad voor foutopsporingslogbestand van afbeeldingsserver {#section-73a3f09b77f2446c9f82207b7d8aec39}

De omslag en de basisdossier - naam voor de dossiers van het het spoorlogboek van de Server van het Beeld. Het pad kan absoluut of relatief ten opzichte van *[!DNL install_folder]* zijn. De ImageServer voegt een afbreekstreepje en de huidige datum ( *[!DNL -yyyy-mm-dd]*) aan het dossier toe - noem (vóór het dossierachtervoegsel, als om het even welk). Het wordt aanbevolen om logbestanden van afbeeldingsservers naar dezelfde map als logbestanden van Platforms Server ( `PS::LogFolder`) te verzenden om het beheer van logbestanden dat door de server van het Platform is geïmplementeerd, te benutten (zie `PS::LogDays`).

>[!NOTE]
>
>U moet de nieuwe map maken voordat u deze instelling wijzigt. Zorg ervoor de toegangstoestemmingen worden geplaatst zodat het Serven van het Beeld de noodzakelijke creeer, lees, en schrijf voorrechten heeft.

## IS:TraceClient - Foutopsporingslogniveau voor imageserver {#section-3851f1f68e404430985c629ac80534db}

Logniveau kan 1, 2, 3 of 4 zijn (standaardwaarde is 2)

Niveau 1 registreert gebeurtenissen met betrekking tot opstarten, sluiten, en de verbindingen van de Server van het Platform.

Niveau 2 registreert ook het verbinden met en het losmaken van bronbeelden.

Niveau 3 voegt registreren van verzoeken om pixelgegevens en levering van het zelfde aan de Server van het Platform toe.

Niveau 4 registreert alle berichten die van de Server van het Platform worden ontvangen.

Niveau 3 en 4 zouden slechts voor zuiveringsdoeleinden moeten worden gebruikt, aangezien de logboekdossiers zeer groot kunnen worden.

## IS::TraceStatsInterval - het Interval van het Logboek van de Statistieken van de Server van het Beeld {#section-1d8df96d61044e33a5b2b2b0309c2d59}

De server van het Beeld schrijft geheugenstatistieken aan zijn dossier van het spoorlogboek bij het interval dat door dit het plaatsen wordt gespecificeerd. Geldige waarden zijn 5 tot 86.400 seconden.

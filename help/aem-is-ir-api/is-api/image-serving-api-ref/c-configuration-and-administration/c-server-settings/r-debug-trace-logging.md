---
description: Gebruik deze serverinstellingen om fouten in het logbestand met overtrekken op te sporen.
seo-description: Gebruik deze serverinstellingen om fouten in het logbestand met overtrekken op te sporen.
seo-title: Foutopsporing_tracering vastleggen
solution: Experience Manager
title: Foutopsporing_tracering vastleggen
topic: Scene7 Image Serving - Image Rendering API
uuid: 33f1d093-007d-453b-965a-9d701a845954
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Foutopsporing_tracering vastleggen{#debug-trace-logging}

Gebruik deze serverinstellingen om fouten in het logbestand met overtrekken op te sporen.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Het wordt aanbevolen alle logbestanden te configureren die naar dezelfde map als `TC::directory`moeten worden geschreven. Dit zorgt ervoor dat alle dossiers van het Logboek van het Beeld deel aan de automatische omwenteling van het logboekdossier gevormd met `TC::maxDays`, die potentiële serverinstabiliteit wegens uit-van-schijf-ruimtevoorwaarden zal verhinderen.

## SV::log - pad naar logboekbestand voor tracering van servertoezichthouder {#section-3697bc480ff646e79cacc2812c55ef26}

De omslag en de naam van het basisdossier voor het logboekdossiers van de Supervisor van de Server. Het pad kan absoluut of relatief ten opzichte van *[!DNL install_folder]* zijn. De servertoezichthouder voegt een afbreekstreepje en de huidige datum ( *[!DNL -yyyy-mm-dd]*) toe aan de bestandsnaam (vóór het eventuele achtervoegsel). Het wordt aanbevolen alle logbestanden naar dezelfde map als de logboekbestanden van de platformserver ( `PS::LogFolder`) te verzenden om het beheer van het logbestand dat door de platformserver ( `PS::LogDays`) is geïmplementeerd, te benutten. Standaard is dit [!DNL logs/Supervisor.log].

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>U moet de nieuwe map maken voordat u deze instelling wijzigt. Zorg ervoor de toegangstoestemmingen worden geplaatst zodat de Supervisor van de Server noodzakelijk creeert, leest, en schrijft voorrechten.

## SV::traclevel - het Niveau van het Logboek van het Spoor van de Supervisor van de Server {#section-36f8634741da4c618d67aa628b5fe474}

Logniveau kan 1, 2, 3 of 4 zijn. De standaardwaarde is 2.

## IS::Logboek - Pad naar foutopsporingslogbestand van afbeeldingsserver {#section-73a3f09b77f2446c9f82207b7d8aec39}

De omslag en de basisdossier - naam voor de dossiers van het het spoorlogboek van de Server van het Beeld. Het pad kan absoluut of relatief ten opzichte van *[!DNL install_folder]* zijn. De ImageServer voegt een afbreekstreepje en de huidige datum ( *[!DNL -yyyy-mm-dd]*) aan het dossier toe - noem (vóór het dossierachtervoegsel, als om het even welk). Het wordt geadviseerd om het logboekdossiers van de Server van het Beeld naar de zelfde omslag te verzenden zoals het logboekdossiers van de Server van het Platform ( `PS::LogFolder`) aan hefboomwerking het beheer van het logboekdossier dat door de Server van het Platform wordt uitgevoerd (zie `PS::LogDays`).

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>U moet de nieuwe map maken voordat u deze instelling wijzigt. Zorg ervoor de toegangstoestemmingen worden geplaatst zodat het Serven van het Beeld de noodzakelijke creeer, lees, en schrijf voorrechten heeft.

## IS:TraceClient - Logniveau foutopsporing van imageserver {#section-3851f1f68e404430985c629ac80534db}

Logniveau kan 1, 2, 3 of 4 zijn (standaardwaarde is 2)

Niveau 1 registreert gebeurtenissen met betrekking tot opstarten, sluiten, en de verbindingen van de Server van het Platform.

Niveau 2 registreert ook het verbinden met en het losmaken van bronbeelden.

Niveau 3 voegt registreren van verzoeken om pixelgegevens en levering van het zelfde aan de Server van het Platform toe.

Niveau 4 registreert alle berichten die van de Server van het Platform worden ontvangen.

Niveau 3 en 4 zouden slechts voor zuiveringsdoeleinden moeten worden gebruikt, aangezien de logboekdossiers zeer groot kunnen worden.

## IS::TraceStatsInterval - het Interval van het Logboek van de Statistieken van de Server van het Beeld {#section-1d8df96d61044e33a5b2b2b0309c2d59}

De server van het Beeld schrijft geheugenstatistieken aan zijn dossier van het spoorlogboek bij het interval dat door dit het plaatsen wordt gespecificeerd. Geldige waarden zijn 5 tot 86.400 seconden.

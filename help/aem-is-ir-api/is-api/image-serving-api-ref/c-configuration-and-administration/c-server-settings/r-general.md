---
description: Algemene serverinstellingen
solution: Experience Manager
title: Algemeen
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Algemeen{#general}

Algemene serverinstellingen

## TC::PsPort - Hoofd-luisterpoort {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Specificeert de belangrijkste luisterhaven voor de Server van het Platform. Deze poort wordt ook gebruikt voor toegang tot de documentatie en voorbeeldpagina&#39;s voor beeldbewerking, beeldweergave en Dynamic Media Viewers (indien geïnstalleerd).

## IS::CacheServerUrl - URL van hoofdmap van service in cache plaatsen {#section-bcca227a1f91453b834db4ea050968e2}

Specificeert de de wortelweg van HTTP om de Server van het Beeld toegang tot de caching dienst toe te staan. Moet worden ingesteld op [!DNL http://localhost:TC::PsPort /is/cache/secondary], met het poortnummer dat overeenkomt `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - Remote Image Source Default TTL {#section-e4c31228b459492cacd2f482d9575f71}

De TTL voor caching beelden die via HTTP van een verre bron worden verkregen gebruikend de `src={…}` constructie. Wordt alleen gebruikt wanneer de externe server geen header Expiration in de HTTP-respons bevat. Geheel getal in seconden.

## IS::RemoteUrlTimeout - Remote Image Source Timeout {#section-437646c479cc4bea81dae42100a3c50a}

De tijd de Server van het Beeld zal op een verre server wachten om het gevraagde beelddossier via HTTP te leveren alvorens een fout terug te keren. Geheel getal in seconden.

## PS::allowDefaultCatalogRequests - Standaardcatalogusverzoeken inschakelen/uitschakelen {#section-484e442a115a49b4ac269d1718b351e1}

Ingesteld op false om aanvragen zonder geldige catalogus-id in het pad te weigeren. De standaardwaarde is `true`. Wanneer ingesteld op `false`, wordt een fout geretourneerd voor aanvragen zonder catalogus-id.

>[!NOTE]
>
>`req=catalogprops` is niet onderworpen aan deze instelling.

## PS::saveToFile.saveTimeout - Time-out voor opslaan van bestand {#section-d22afd8ad86144b28684ed95a59db40e}

Standaardtime-outwaarde voor `req=saveToFile` wanneer `timeout=`niet is opgegeven. `msec`. Er wordt een fout geretourneerd als de opslagbewerking niet binnen de opgegeven tijd wordt voltooid.

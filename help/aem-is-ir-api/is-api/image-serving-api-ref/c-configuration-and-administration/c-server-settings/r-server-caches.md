---
description: Gebruik deze serverinstellingen voor servercaches.
solution: Experience Manager
title: Servercaches
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6a8d44d3-ecac-4fe0-9f81-28b1cd55e7e1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Servercaches{#server-caches}

Gebruik deze serverinstellingen voor servercaches.

## PS::cache.rootPaths - Cachegegevensmappen {#section-f0aa808304d74ecdb0c3644f11906c53}

De hoofdmap(pen) voor de [!DNL Platform Server]Schijfcache. Een of meer absolute bestandspaden of paden ten opzichte van *[!DNL install_folder]*, gescheiden door puntkomma&#39;s (;). De gegevens voor de HTTP-responscache worden gelijkmatig over alle opgegeven mappen verdeeld. De caches voor de extra caches (gecompileerde afbeeldingscatalogi en externe afbeeldingsgegevens) bevinden zich in de primaire cachemap (de eerste map in de lijst).

## PS::cache.maxSize - Grootte cache voor responsgegevens {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

De maximumgrootte van de HTTP-responscache in bytes. Deze instelling beperkt de hoeveelheid gegevens die daadwerkelijk in cache moeten worden geplaatst. er wordt geen rekening gehouden met overhead van het bestandssysteem. (Zie [Responsgegevenscache](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca).) Als er meerdere cachegegevensmappen zijn opgegeven, worden de cachegegevens gelijkmatig over alle mappen verdeeld. De waarde van `cache.maxSize` in [!DNL PlatformServer.conf] is in bytes.

## PS::cache.maxEntry - Max. items voor responscache {#section-5603e327e90542a5b50aeeb27b080410}

Het aantal items dat is toegewezen voor de HTTP response cache-index in het geheugen.

>[!NOTE]
>
>Controleer in Linux of er voldoende i-nodes zijn toegewezen voor de cachepartitie om te voorkomen dat er onvoldoende i-nodes zijn.

## IS::TempDirectory - Map Tijdelijke bestanden afbeeldingsserver {#section-42ea1e7a68c444878f7245c5bbcb1672}

De server van het Beeld moet soms middengegevens aan schijf opslaan. Het pad kan absoluut of relatief zijn ten opzichte van *[!DNL install_folder]*.

>[!NOTE]
>
>U moet de nieuwe map maken voordat u deze instelling wijzigt. Zorg ervoor de toegangstoestemmingen worden geplaatst zodat de Server van het Beeld volledige controle van de omslag heeft.

## SV::temp - map Tijdelijke bestanden voor servertoezichthouder {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

De Supervisor van de Server moet soms tussentijdse gegevens aan schijf opslaan. Het pad kan absoluut of relatief zijn ten opzichte van *[!DNL install_folder]*. Heeft als standaardwaarde [!DNL  *[!DNL install_folder]*/temp].

>[!NOTE]
>
>U moet de nieuwe map maken voordat u deze instelling wijzigt. Zorg ervoor de toegangstoestemmingen worden geplaatst zodat de Supervisor van de Server volledige controle van de omslag heeft.

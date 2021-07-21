---
description: Bevat instellingen voor het beheer van afbeeldingscatalogi.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

Bevat instellingen voor het beheer van afbeeldingscatalogi.

Dit bestand is een JAVA-eigenschappenbestand. Er moet op worden toegezien dat de desbetreffende verdragen worden nageleefd; anders kan de Server van het Platform er niet in slagen te beginnen. Gebruik een dubbele backslash &#39;\\&#39; of een enkele forward slash &#39;/&#39; in plaats van een backslash &#39;\&#39; in Windows-bestandspaden. De backslash wordt gebruikt als escape-teken in dit type bestand.

Wijzigingen in dit bestand worden van kracht kort nadat het bestand is opgeslagen.

Alleen onderstaande instellingen kunnen worden gewijzigd in [!DNL catalog-service.conf]. Als een bepaalde instelling ontbreekt, kan deze overal in het bestand worden toegevoegd. Er mag slechts één instantie van elke instelling aanwezig zijn.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`

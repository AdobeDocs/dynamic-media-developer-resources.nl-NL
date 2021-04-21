---
description: Bevat instellingen voor het beheer van afbeeldingscatalogi.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '122'
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

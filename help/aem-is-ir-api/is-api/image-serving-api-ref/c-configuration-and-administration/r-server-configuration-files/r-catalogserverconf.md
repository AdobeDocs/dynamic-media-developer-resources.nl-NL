---
description: Bevat instellingen voor het beheer van afbeeldingscatalogi.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

Bevat instellingen voor het beheer van afbeeldingscatalogi.

Dit bestand is een JAVA-eigenschappenbestand. Er moet op worden toegezien dat de desbetreffende verdragen worden nageleefd; anders [!DNL Platform Server] kan niet starten. Gebruik een dubbele backslash &#39;\\&#39; of een enkele forward slash &#39;/&#39; in plaats van een backslash &#39;\&#39; in Windows-bestandspaden. De backslash wordt gebruikt als escape-teken in dit type bestand.

Wijzigingen in dit bestand worden van kracht kort nadat het bestand is opgeslagen.

Alleen onderstaande instellingen kunnen worden gewijzigd in [!DNL catalog-service.conf]. Als een bepaalde instelling ontbreekt, kan deze overal in het bestand worden toegevoegd. Er mag slechts één instantie van elke instelling aanwezig zijn.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`

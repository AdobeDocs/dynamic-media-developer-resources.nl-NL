---
description: In deze documentatie wordt uitgelegd hoe u de Dynamic Media Image Rendering-server beheert.
solution: Experience Manager
title: Overzicht van serverbeheer
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# Overzicht van serverbeheer{#server-administration-overview}

In deze documentatie wordt uitgelegd hoe u de Dynamic Media Image Rendering-server beheert.

Renderen van afbeelding bestaat uit twee belangrijke componenten:

* Een Java-pakket wordt geïmplementeerd met de Image Serving Platform Server en beheert de clientverbinding, caching, materiaalcatalogi.
* Een native codemodule wordt opgesteld als uitbreidingsbibliotheek voor de Server van het Beeld en voert de functionaliteit van de kernbeeld het teruggeven uit.

Beide componenten worden gezamenlijk *Render Server* genoemd.

Renderen van het beeld deelt vele serverfaciliteiten met het Beeld Serven, en alle opties worden gevormd door een configuratiedossier uit te geven. Aanvullende configuratiekenmerken worden verschaft door de standaardcatalogus ( [!DNL default.ini]) of specifieke materiaalcatalogi. Zie Materiaalcatalogi voor meer informatie.

De installatiemap voor het renderen van afbeeldingen ( *[!DNL install_folder]*) is [!DNL *[!DNL install_root]*/ImageRendering]. In Windows is *[!DNL install_root]* standaard `C:\Program Files\Scene7`. Tijdens de installatie kan een andere map worden opgegeven. In Linux moet *[!DNL install_root]* altijd [!DNL /usr/local/scene7] zijn. Er mogen symbolische koppelingen worden gebruikt.

Alle bestandspaden zijn hoofdlettergevoelig in UNIX en hoofdlettergevoelig in Windows.

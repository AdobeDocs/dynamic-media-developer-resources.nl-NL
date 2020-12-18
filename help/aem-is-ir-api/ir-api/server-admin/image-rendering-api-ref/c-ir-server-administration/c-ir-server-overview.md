---
description: In deze documentatie wordt uitgelegd hoe u de Scene7 Image Rendering-server beheert.
seo-description: In deze documentatie wordt uitgelegd hoe u de Scene7 Image Rendering-server beheert.
seo-title: Overzicht van serverbeheer
solution: Experience Manager
title: Overzicht van serverbeheer
topic: Scene7 Image Serving - Image Rendering API
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---


# Overzicht van serverbeheer{#server-administration-overview}

In deze documentatie wordt uitgelegd hoe u de Scene7 Image Rendering-server beheert.

Renderen van afbeelding bestaat uit twee belangrijke componenten:

* Een Java-pakket wordt geïmplementeerd met de Image Serving Platform Server en beheert de clientverbinding, caching, materiaalcatalogi.
* Een native codemodule wordt opgesteld als uitbreidingsbibliotheek voor de Server van het Beeld en voert de functionaliteit van de kernbeeld het teruggeven uit.

Beide componenten worden gezamenlijk *Render Server* genoemd.

Renderen van het beeld deelt vele serverfaciliteiten met het Beeld Serven, en alle opties worden gevormd door een configuratiedossier uit te geven. Aanvullende configuratiekenmerken worden verschaft door de standaardcatalogus ( [!DNL default.ini]) of specifieke materiaalcatalogi. Zie Materiaalcatalogi voor meer informatie.

De installatiemap voor het renderen van afbeeldingen ( *[!DNL install_folder]*) is [!DNL *[!DNL install_root]*/ImageRendering]. In Windows is *[!DNL install_root]* standaard `C:\Program Files\Scene7`. Tijdens de installatie kan een andere map worden opgegeven. In Linux moet *[!DNL install_root]* altijd [!DNL /usr/local/scene7] zijn. Er mogen symbolische koppelingen worden gebruikt.

Alle bestandspaden zijn hoofdlettergevoelig in UNIX en hoofdlettergevoelig in Windows.

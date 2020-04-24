---
description: Deze documentatie verklaart hoe te om het Beeld te beheren Scene7 die server teruggeeft.
seo-description: Deze documentatie verklaart hoe te om het Beeld te beheren Scene7 die server teruggeeft.
seo-title: Overzicht van serverbeheer
solution: Experience Manager
title: Overzicht van serverbeheer
topic: Scene7 Image Serving - Image Rendering API
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5

---


# Overzicht van serverbeheer{#server-administration-overview}

Deze documentatie verklaart hoe te om het Beeld te beheren Scene7 die server teruggeeft.

Renderen van afbeelding bestaat uit twee belangrijke componenten:

* Een Java-pakket wordt geïmplementeerd met de Image Serving Platform Server en beheert de clientverbinding, caching, materiaalcatalogi.
* Een native codemodule wordt opgesteld als uitbreidingsbibliotheek voor de Server van het Beeld en voert de functionaliteit van de kernbeeld het teruggeven uit.

Beide componenten worden collectief genoemd de *Render Server*.

Renderen van het beeld deelt vele serverfaciliteiten met het Beeld Serven, en alle opties worden gevormd door een configuratiedossier uit te geven. De extra configuratiekenmerken worden verstrekt door de standaardcatalogus ( [!DNL default.ini]) of specifieke materiaalcatalogi. Zie Materiaalcatalogi voor meer informatie.

De installatiemap voor het renderen van afbeeldingen ( *[!DNL install_folder]*) is [!DNL *[!DNL install_root]*/ImageRendering]. In Windows *[!DNL install_root]* is de standaardwaarde `C:\Program Files\Scene7`. Tijdens de installatie kan een andere map worden opgegeven. Op Linux moet dit altijd *[!DNL install_root]* zijn [!DNL /usr/local/scene7]. Er mogen symbolische koppelingen worden gebruikt.

Alle bestandspaden zijn hoofdlettergevoelig in UNIX en hoofdlettergevoelig in Windows.

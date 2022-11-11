---
description: In deze documentatie wordt uitgelegd hoe u de Dynamic Media Image Rendering-server beheert.
solution: Experience Manager
title: Overzicht van serverbeheer
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Overzicht van serverbeheer{#server-administration-overview}

In deze documentatie wordt uitgelegd hoe u de Dynamic Media Image Rendering-server beheert.

Renderen van afbeelding bestaat uit twee belangrijke componenten:

* Een Java-pakket wordt geïmplementeerd met de Image Serving [!DNL Platform Server] en beheert de clientverbinding, caching, materiaalcatalogi.
* Een native codemodule wordt opgesteld als uitbreidingsbibliotheek voor de Server van het Beeld en voert de functionaliteit van de kernbeeld het teruggeven uit.

Beide componenten worden collectief genoemd *Server renderen*.

Renderen van het beeld deelt vele serverfaciliteiten met het Beeld Serven, en alle opties worden gevormd door een configuratiedossier uit te geven. De extra configuratiekenmerken worden verstrekt door de standaardcatalogus ( [!DNL default.ini]) of specifieke materiaalcatalogi. Zie Materiaalcatalogi voor meer informatie.

De installatiemap voor het renderen van afbeeldingen ( *[!DNL install_folder]*) is [!DNL *[!DNL install_root]*/ImageRendering]. In Windows is de standaardinstelling *[!DNL install_root]* is `C:\Program Files\Scene7`. Tijdens de installatie kan een andere map worden opgegeven. In Linux *[!DNL install_root]* moet altijd [!DNL /usr/local/scene7]. Er mogen symbolische koppelingen worden gebruikt.

Alle bestandspaden zijn hoofdlettergevoelig in UNIX en hoofdlettergevoelig in Windows.

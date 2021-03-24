---
description: Materiaalcatalogi bieden veel configuratie-instellingen voor het renderen van afbeeldingen.
solution: Experience Manager
title: Materiaalcatalogi
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder,praktijkgericht
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# Materiaalcatalogi{#material-catalogs}

Materiaalcatalogi bieden veel configuratie-instellingen voor het renderen van afbeeldingen.

In materiaalcatalogi kunt u het vignet en de materiaalid&#39;s die worden gebruikt in aanvragen voor feitelijke bestandspaden, alle metagegevens opslaan die aan materialen zijn gekoppeld en containers voor sjablonen weergeven. Ze houden ICC-profielen en opdrachtmacro&#39;s bij.

Materiaalcatalogi worden alleen benaderd door de Java-component Image Rendering (die zich op dezelfde locatie bevindt als de Platform Server). Bestanden met cataloguskenmerken moeten het achtervoegsel [!DNL .ini] hebben en in de geregistreerde catalogusmap ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)) worden geplaatst. De standaard materiaalcatalogus ( [!DNL default.ini]) moet altijd aanwezig zijn en moet met alle attributen voor het correcte functioneren van het Beeld Serven worden bevolkt.

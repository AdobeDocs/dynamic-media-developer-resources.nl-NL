---
description: Materiaalcatalogi bieden veel configuratie-instellingen voor het renderen van afbeeldingen.
seo-description: Materiaalcatalogi bieden veel configuratie-instellingen voor het renderen van afbeeldingen.
seo-title: Materiaalcatalogi
solution: Experience Manager
title: Materiaalcatalogi
uuid: 6d209019-f9ca-43e4-900b-3597c7044a79
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder,praktijkgericht
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Materiaalcatalogi{#material-catalogs}

Materiaalcatalogi bieden veel configuratie-instellingen voor het renderen van afbeeldingen.

In materiaalcatalogi kunt u het vignet en de materiaalid&#39;s die worden gebruikt in aanvragen voor feitelijke bestandspaden, alle metagegevens opslaan die aan materialen zijn gekoppeld en containers voor sjablonen weergeven. Ze houden ICC-profielen en opdrachtmacro&#39;s bij.

Materiaalcatalogi worden alleen benaderd door de Java-component Image Rendering (die zich op dezelfde locatie bevindt als de Platform Server). Bestanden met cataloguskenmerken moeten het achtervoegsel [!DNL .ini] hebben en in de geregistreerde catalogusmap ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)) worden geplaatst. De standaard materiaalcatalogus ( [!DNL default.ini]) moet altijd aanwezig zijn en moet met alle attributen voor het correcte functioneren van het Beeld Serven worden bevolkt.

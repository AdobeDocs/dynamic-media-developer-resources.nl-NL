---
description: De het Teruggeven van het beeld configuratiemontages worden opgeslagen in het de configuratiedossier van de Server van het Platform.
seo-description: De het Teruggeven van het beeld configuratiemontages worden opgeslagen in het de configuratiedossier van de Server van het Platform.
seo-title: Configuratiebestanden
solution: Experience Manager
title: Configuratiebestanden
topic: Scene7 Image Serving - Image Rendering API
uuid: ffd1c65b-e084-4a7e-9a15-600d6c5b173a
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Configuratiebestanden{#configuration-files}

De het Teruggeven van het beeld configuratiemontages worden opgeslagen in het de configuratiedossier van de Server van het Platform.

Het configuratiebestand van de platformserver bevindt zich op [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Dit bestand is een JAVA-eigenschappenbestand. De zorg moet worden genomen om de aangewezen overeenkomsten te volgen, anders zou de Server van het Platform kunnen er niet in slagen te beginnen. Een dubbele backslash (`\\`) of één enkele voorwaartse schuine streep (/) moet in plaats van een eenvoudige backslash (\) in de dossierwegen van Vensters worden gebruikt, omdat backslash als escape karakter in dit type van dossier wordt gebruikt. Het bestand bevat niet-gedocumenteerde eigenschappen die voor intern servergebruik zijn en niet mogen worden gewijzigd.

Raadpleeg de [Referentie voor configuratie-instellingen](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) voor een lijst met alle configuratie-instellingen voor het renderen van afbeeldingen.

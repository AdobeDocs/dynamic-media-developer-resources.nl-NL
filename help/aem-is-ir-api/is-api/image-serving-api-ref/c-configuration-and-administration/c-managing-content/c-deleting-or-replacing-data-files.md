---
description: Terwijl het toevoegen van nieuwe gegevensdossiers eenvoudig en recht-voorwaarts is, moet de speciale zorg worden genomen wanneer het vervangen van bestaande gegevensdossiers die actief door de server worden gebruikt. In plaats van dergelijke bestanden gewoon te vervangen, wordt aangeraden het vervangende bestand een nieuwe naam te geven (bijv. een versieachtervoegsel aan de bestandsnaam toe te voegen). Nadat het nieuwe bestand live is gemaakt, kan de oude versie worden verwijderd.
seo-description: Terwijl het toevoegen van nieuwe gegevensdossiers eenvoudig en recht-voorwaarts is, moet de speciale zorg worden genomen wanneer het vervangen van bestaande gegevensdossiers die actief door de server worden gebruikt. In plaats van dergelijke bestanden gewoon te vervangen, wordt aangeraden het vervangende bestand een nieuwe naam te geven (bijv. een versieachtervoegsel aan de bestandsnaam toe te voegen). Nadat het nieuwe bestand live is gemaakt, kan de oude versie worden verwijderd.
seo-title: Gegevensbestanden verwijderen of vervangen
solution: Experience Manager
title: Gegevensbestanden verwijderen of vervangen
topic: Scene7 Image Serving - Image Rendering API
uuid: 7b446144-48f6-4b50-93ec-0287425d932a
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---


# Gegevensbestanden verwijderen of vervangen{#deleting-or-replacing-data-files}

Terwijl het toevoegen van nieuwe gegevensdossiers eenvoudig en recht-voorwaarts is, moet de speciale zorg worden genomen wanneer het vervangen van bestaande gegevensdossiers die actief door de server worden gebruikt. In plaats van dergelijke bestanden gewoon te vervangen, wordt aangeraden het vervangende bestand een nieuwe naam te geven (bijv. een versieachtervoegsel aan de bestandsnaam toe te voegen). Nadat het nieuwe bestand live is gemaakt, kan de oude versie worden verwijderd.

>[!NOTE]
>
>Gegevensbestanden mogen tijdens actief gebruik nooit worden vervangen of verwijderd door Image Serving. Anders kunnen fouten of zelfs een servercrash optreden.

In alle gevallen, herinner me dat het geheime voorgeheugen van de Server van het Platform en de ingangen van het cliëntgeheime voorgeheugen versleten moeten worden alvorens de bijgewerkte gegevens door de cliënt zullen worden gezien. Specifieke cachemarangen kunnen direct worden bijgewerkt met de opdracht `cache=validate`.

Wijzigingen in lettertypebestanden en ICC-profielbestanden worden niet rechtstreeks door het cachebeheer bijgehouden. Als een dergelijke resource wordt gewijzigd zonder de id ervan te wijzigen, weet de servercache niet van de wijziging en zorgt `cache=validate` er niet voor dat de cache-invoer wordt bijgewerkt. `cache=update` kan worden gebruikt om het opnieuw genereren van dergelijke cachemarangen af te dwingen.

Om de complicaties bij het vervangen van bestanden te voorkomen, wordt aanbevolen een vervangend bestand een nieuwe naam te geven en de bijbehorende catalogusitems bij te werken. Hierdoor kan elk gegevensbestand worden vervangen terwijl de server actief is en worden vermeldingen in de servercache onmiddellijk en zonder extra tussenkomst verouderd. Deze aanpak kan worden gebruikt voor ICC-profielen, -lettertypen en alle afbeeldingen die door afbeeldingscatalogi worden beheerd.

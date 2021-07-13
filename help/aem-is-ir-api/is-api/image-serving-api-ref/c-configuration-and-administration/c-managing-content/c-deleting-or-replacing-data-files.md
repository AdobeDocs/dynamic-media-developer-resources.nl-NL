---
description: Terwijl het toevoegen van nieuwe gegevensdossiers eenvoudig en recht-voorwaarts is, moet de speciale zorg worden genomen wanneer het vervangen van bestaande gegevensdossiers die actief door de server worden gebruikt. In plaats van dergelijke bestanden gewoon te vervangen, wordt aangeraden het vervangende bestand een nieuwe naam te geven (bijv. een versieachtervoegsel aan de bestandsnaam toe te voegen). Nadat het nieuwe bestand live is gemaakt, kan de oude versie worden verwijderd.
solution: Experience Manager
title: Gegevensbestanden verwijderen of vervangen
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '327'
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

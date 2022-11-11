---
description: Terwijl het toevoegen van nieuwe gegevensdossiers eenvoudig en recht-voorwaarts is, moet de speciale zorg worden genomen wanneer het vervangen van bestaande gegevensdossiers die actief door de server worden gebruikt. In plaats van dergelijke bestanden gewoon te vervangen, wordt aangeraden het vervangende bestand een nieuwe naam te geven (bijv. een versieachtervoegsel aan de bestandsnaam toe te voegen). Nadat het nieuwe bestand live is gemaakt, kan de oude versie worden verwijderd.
solution: Experience Manager
title: Gegevensbestanden verwijderen of vervangen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Gegevensbestanden verwijderen of vervangen{#deleting-or-replacing-data-files}

Terwijl het toevoegen van nieuwe gegevensdossiers eenvoudig en recht-voorwaarts is, moet de speciale zorg worden genomen wanneer het vervangen van bestaande gegevensdossiers die actief door de server worden gebruikt. In plaats van dergelijke bestanden gewoon te vervangen, wordt aangeraden het vervangende bestand een nieuwe naam te geven (bijv. een versieachtervoegsel aan de bestandsnaam toe te voegen). Nadat het nieuwe bestand live is gemaakt, kan de oude versie worden verwijderd.

>[!NOTE]
>
>Gegevensbestanden mogen tijdens actief gebruik nooit worden vervangen of verwijderd door Image Serving. Anders kunnen fouten of zelfs een servercrash optreden.

Houd er in alle gevallen rekening mee dat de [!DNL Platform Server] cache en de items in de clientcache moeten verouderd zijn voordat de bijgewerkte gegevens door de client worden bekeken. Specifieke cachemarangen kunnen direct worden bijgewerkt met de functie `cache=validate` gebruiken.

Wijzigingen in lettertypebestanden en ICC-profielbestanden worden niet rechtstreeks door het cachebeheer bijgehouden. Als een dergelijke bron wordt gewijzigd zonder de id ervan te wijzigen, zal de servercache niet op de hoogte zijn van de wijziging, en `cache=validate` zorgt er niet voor dat de cachevermelding wordt bijgewerkt. `cache=update` kan worden gebruikt om het opnieuw genereren van dergelijke cachemarangen af te dwingen.

Om de complicaties bij het vervangen van bestanden te voorkomen, wordt aanbevolen een vervangend bestand een nieuwe naam te geven en de bijbehorende catalogusitems bij te werken. Hierdoor kan elk gegevensbestand worden vervangen terwijl de server actief is en worden vermeldingen in de servercache onmiddellijk en zonder extra tussenkomst verouderd. Deze aanpak kan worden gebruikt voor ICC-profielen, -lettertypen en alle afbeeldingen die door afbeeldingscatalogi worden beheerd.

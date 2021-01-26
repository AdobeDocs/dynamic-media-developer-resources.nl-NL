---
description: Vignetbestanden kunnen worden vervangen of verwijderd terwijl de server actief is door de opdracht req=release te gebruiken vlak voordat het bestand wordt overschreven.
seo-description: Vignetbestanden kunnen worden vervangen of verwijderd terwijl de server actief is door de opdracht req=release te gebruiken vlak voordat het bestand wordt overschreven.
seo-title: Brongegevensbestanden verwijderen of vervangen
solution: Experience Manager
title: Brongegevensbestanden verwijderen of vervangen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 13dc0489-7ab0-481e-b213-214affe9819e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# Brongegevensbestanden verwijderen of vervangen{#deleting-or-replacing-source-data-files}

Vignetbestanden kunnen worden vervangen of verwijderd terwijl de server actief is door de opdracht req=release te gebruiken vlak voordat het bestand wordt overschreven.

>[!NOTE]
>
>Een gegevensbestand moet niet worden vervangen of worden geschrapt terwijl de Render Server tot het toegang heeft.

Houd er rekening mee dat als u een brongegevensbestand verwijdert of vervangt, de Render Server het bestand alleen sluit tot de volgende aanvraag die toegang heeft tot dat vignet. Als een bestand veel wordt gebruikt, is het mogelijk dat meerdere pogingen nodig zijn.

De renderserver moet worden gestopt om andere gegevensbestanden te vervangen.

Cachingangen van de Server van het Platform worden automatisch ongeldig gemaakt wanneer de materiaaldossiers of de vignetten worden vervangen. Wanneer u ICC-profielbestanden vervangt, worden de cache niet ongeldig gemaakt.

Om de complicaties bij het vervangen van bestanden te voorkomen, wordt aanbevolen een vervangend bestand een nieuwe naam te geven en de bijbehorende catalogusitems bij te werken. Hierdoor kan elk gegevensbestand worden vervangen terwijl de server actief is en worden vermeldingen in de servercache automatisch verouderd zonder extra tussenkomst. Deze benadering kan voor alle gegevensdossiers worden gebruikt die door beeldcatalogi worden beheerd.

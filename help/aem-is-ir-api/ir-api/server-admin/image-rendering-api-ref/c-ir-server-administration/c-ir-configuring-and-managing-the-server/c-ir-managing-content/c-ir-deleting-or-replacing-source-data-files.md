---
description: Vignetbestanden kunnen worden vervangen of verwijderd terwijl de server actief is door de opdracht req=release te gebruiken vlak voordat het bestand wordt overschreven.
solution: Experience Manager
title: Brongegevensbestanden verwijderen of vervangen
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder,praktijkgericht
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '218'
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

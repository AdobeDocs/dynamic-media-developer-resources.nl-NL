---
description: Vignetbestanden kunnen worden vervangen of verwijderd terwijl de server actief is door de opdracht req=release te gebruiken vlak voordat het bestand wordt overschreven.
solution: Experience Manager
title: Brongegevensbestanden verwijderen of vervangen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Brongegevensbestanden verwijderen of vervangen{#deleting-or-replacing-source-data-files}

Vignetbestanden kunnen worden vervangen of verwijderd terwijl de server actief is door de opdracht req=release te gebruiken vlak voordat het bestand wordt overschreven.

>[!NOTE]
>
>Een gegevensbestand moet niet worden vervangen of worden geschrapt terwijl de Render Server tot het toegang heeft.

Houd er rekening mee dat als u een brongegevensbestand verwijdert of vervangt, de Render Server het bestand alleen sluit tot de volgende aanvraag die toegang heeft tot dat vignet. Als een bestand veel wordt gebruikt, is het mogelijk dat meerdere pogingen nodig zijn.

De renderserver moet worden gestopt om andere gegevensbestanden te vervangen.

[!DNL Platform Server] cachemarangen worden automatisch ongeldig gemaakt wanneer materiaalbestanden of vignetten worden vervangen. Wanneer u ICC-profielbestanden vervangt, worden de cache niet ongeldig gemaakt.

Om de complicaties bij het vervangen van bestanden te voorkomen, wordt aanbevolen een vervangend bestand een nieuwe naam te geven en de bijbehorende catalogusitems bij te werken. Hierdoor kan elk gegevensbestand worden vervangen terwijl de server actief is en worden vermeldingen in de servercache automatisch verouderd zonder extra tussenkomst. Deze benadering kan voor alle gegevensdossiers worden gebruikt die door beeldcatalogi worden beheerd.

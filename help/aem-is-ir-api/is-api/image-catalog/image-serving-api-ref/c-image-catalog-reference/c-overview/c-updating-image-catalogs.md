---
description: De server bewaakt voortdurend de catalogusmap en laadt automatisch een afbeeldingscatalogus, inclusief de bijbehorende bestanden met catalogusgegevens, opnieuw wanneer wordt vastgesteld dat het kenmerkbestand van de hoofdcatalogus is gewijzigd.
solution: Experience Manager
title: Afbeeldingscatalogi bijwerken
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---


# Afbeeldingscatalogi bijwerken{#updating-image-catalogs}

De server bewaakt voortdurend de catalogusmap en laadt automatisch een afbeeldingscatalogus, inclusief de bijbehorende bestanden met catalogusgegevens, opnieuw wanneer wordt vastgesteld dat het kenmerkbestand van de hoofdcatalogus is gewijzigd.

Als u afbeeldingscatalogi op de server wilt bijwerken, vervangt u eerst alle bestanden met catalogusgegevens die moeten worden gewijzigd en vervangt u het bestand met cataloguskenmerken (of &quot;tik&quot; om de bestandsdatum bij te werken) om de catalogus opnieuw te laden.

## Incrementele updates {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

Het laden en verwerken van grote afbeeldingscatalogi kan een aanzienlijke belasting voor de server betekenen en kan een negatief effect hebben op bewerkingen met live serving. Om dit effect te minimaliseren, wordt aanbevolen een mechanisme voor incrementele catalogusupdate te implementeren dat als volgt werkt:

Een primair catalogusbestand dat alle afbeeldingen bevat, wordt elke avond tijdens een lage verkeersduur geladen. Als het tijdens de dag nodig is om records in de afbeeldingscatalogus toe te voegen of te wijzigen, wordt een ander afbeeldingsgegevensbestand gemaakt dat alleen de nieuwe of gewijzigde records bevat. Dit bestand wordt geregistreerd als een bestand met secundaire afbeeldingsgegevens in `attribute::CatalogFile`. De server detecteert dat het bestand met cataloguskenmerken is gewijzigd en controleert vervolgens welke bestanden met catalogusgegevens zijn gewijzigd. Als het bestand met de hoofdafbeeldingsgegevens niet is gewijzigd, wordt alleen het incrementele gegevensbestand geladen of opnieuw geladen. Omdat dit bestand doorgaans veel kleiner is dan het hoofdcatalogusbestand, is het effect op de server veel kleiner dan wanneer u de hoofdcatalogus opnieuw laadt.

De stijgende updates kunnen effect op de server tijdens zwaar verkeer beduidend verminderen. Het wordt aanbevolen om het bestand met incrementele catalogusgegevens regelmatig tijdens minder verkeersuren samen te voegen in het hoofdbestand met catalogusgegevens om optimale serverprestaties te behouden.

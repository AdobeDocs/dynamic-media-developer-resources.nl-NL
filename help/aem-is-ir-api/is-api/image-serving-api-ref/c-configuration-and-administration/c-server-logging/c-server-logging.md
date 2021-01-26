---
description: Alle logbestanden worden naar dezelfde logmap geschreven die in de TC-map is opgegeven.
solution: Experience Manager
title: Serverregistratie
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Serverlogboekregistratie{#server-logging}

Alle logbestanden worden geschreven naar dezelfde logmap die is opgegeven met TC::directory.

Logbestanden worden meestal dagelijks gemaakt en geroteerd. Oudere logbestanden in de logmap worden na een opgegeven aantal dagen ( `TC::maxDays`) automatisch verwijderd.

Belangrijk Er moet voldoende schijfruimte worden gereserveerd voor logbestanden om te voorkomen dat er onvoldoende schijfruimte beschikbaar is. 1-2 GB/dag kan voor een sterk gebruikte server en standaardlogboekmontages worden vereist.

De Server van het Platform en de Server van het Beeld leiden tot de drie types van hieronder beschreven logboekdossiers.

Met andere onderdelen van de afbeeldingsserver en bepaalde andere Dynamic Media-pakketten, zoals de Dynamic Media Viewers, kunt u ook logbestanden maken in dezelfde map. Deze logbestanden zijn bedoeld voor intern gebruik door Dynamic Media en kunnen worden aangevraagd door technische ondersteuning van Dynamic Media voor probleemoplossing.

* [Toegangslogboek](c-access-log.md)
* [Traceerlogboek](c-trace-log.md)
* [Logboek van afbeeldingsserver](c-image-server-log.md)

## Zie ook {#section-5ff5e46031b1461c92de24e632610d6d}

[Logboekregistratie voor](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f) toegang,  [foutopsporing/tracering](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)

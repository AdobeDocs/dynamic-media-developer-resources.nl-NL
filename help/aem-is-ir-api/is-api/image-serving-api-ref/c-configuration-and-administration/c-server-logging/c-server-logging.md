---
description: Alle logbestanden worden naar dezelfde logmap geschreven die in de TC-map is opgegeven.
solution: Experience Manager
title: Serverregistratie
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# Serverregistratie{#server-logging}

Alle logbestanden worden geschreven naar dezelfde logmap die is opgegeven met TC::directory.

Logbestanden worden meestal dagelijks gemaakt en geroteerd. Oudere logbestanden in de logmap worden na een opgegeven aantal dagen automatisch verwijderd ( `TC::maxDays`).

Belangrijk Er moet voldoende schijfruimte worden gereserveerd voor logbestanden om te voorkomen dat er onvoldoende schijfruimte beschikbaar is. 1-2 GB/dag kan voor een sterk gebruikte server en standaardlogboekmontages worden vereist.

De [!DNL Platform Server] en de Server van het Beeld creeert de drie types van logboekdossiers die hieronder worden beschreven.

Met andere onderdelen van de afbeeldingsserver en bepaalde andere Dynamic Media-pakketten, zoals de Dynamic Media Viewers, kunt u ook logbestanden maken in dezelfde map. Deze logbestanden zijn bedoeld voor intern gebruik door Dynamic Media en kunnen worden aangevraagd door technische ondersteuning van Dynamic Media voor probleemoplossing.

* [Toegangslogboek](c-access-log.md)
* [Traceerlogboek](c-trace-log.md)
* [Logboek van afbeeldingsserver](c-image-server-log.md)

## Zie ook {#section-5ff5e46031b1461c92de24e632610d6d}

[Toegangsregistratie](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f), [Foutopsporing/tracering vastleggen](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)

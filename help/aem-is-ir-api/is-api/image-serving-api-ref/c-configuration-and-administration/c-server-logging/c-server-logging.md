---
description: Alle logbestanden worden naar dezelfde logmap geschreven die in de TC-map is opgegeven.
seo-description: Alle logbestanden worden naar dezelfde logmap geschreven die in de TC-map is opgegeven.
seo-title: Serverregistratie
solution: Experience Manager
title: Serverregistratie
topic: Scene7 Image Serving - Image Rendering API
uuid: f6145737-e4c3-4533-9be5-5b5a0202fe33
translation-type: tm+mt
source-git-commit: 5717550d2dea8ec086875e770ff8f200aaa75ff3

---


# Serverregistratie{#server-logging}

Alle logbestanden worden geschreven naar dezelfde logmap die is opgegeven met TC::directory.

Logbestanden worden meestal dagelijks gemaakt en geroteerd. Oudere logbestanden in de logmap worden na een opgegeven aantal dagen ( `TC::maxDays`) automatisch verwijderd.

Belangrijk Er moet voldoende schijfruimte worden gereserveerd voor logbestanden om te voorkomen dat er onvoldoende schijfruimte beschikbaar is. 1-2 GB/dag kan voor een sterk gebruikte server en standaardlogboekmontages worden vereist.

De server van het Platform en de Server van het Beeld leiden tot de drie types van logboekdossiers die hieronder worden beschreven.

Andere Beeld die componenten en bepaalde andere pakketten Scene7, zoals de Kijkers Scene7 dienen, kunnen logboekdossiers in de zelfde omslag ook tot stand brengen. Deze logboekdossiers zijn voor intern gebruik Scene7 en kunnen door Steun Scene7 voor problemen-ontspruitende doeleinden worden gevraagd.

* [Toegangslogboek](c-access-log.md)
* [Traceerlogboek](c-trace-log.md)
* [Logboek van afbeeldingsserver](c-image-server-log.md)

## Zie ook {#section-5ff5e46031b1461c92de24e632610d6d}

[Logboekregistratie voor](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f)toegang, [foutopsporing/tracering](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)

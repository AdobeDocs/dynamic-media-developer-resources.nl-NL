---
description: Gebruikersgegevens. De server retourneert de inhoud van dit veld naar de client als reactie op req=userdata.
solution: Experience Manager
title: UserData
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# UserData{#userdata}

Gebruikersgegevens. De server retourneert de inhoud van dit veld naar de client als reactie op req=userdata.

## Eigenschappen {#section-06f2002b77d54a64be07f12fff54ad13}

Tekstreeks. Het wordt aanbevolen [eigenschapsgegevens](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md)-opmaak te gebruiken. Wanneer de gegevensopmaak van de eigenschap niet wordt gebruikt, mag de tekenreeks het teken &#39;=&#39; niet bevatten.

De cliënten van de gezoem, spin, en brochure kijker veronderstellen dit gebied om het formatteren van bezitsgegevens te gebruiken. Deze clients gebruiken dit veld voor viewerconfiguratie en -aanpassing. Raadpleeg de documentatie bij de viewer voor meer informatie.

Dit veld neemt deel aan de lokalisatie van tekstreeksen. Raadpleeg [Tekstreeks lokalisatie](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in de *HTTP-protocolreferentie* voor meer informatie.

## Standaard {#section-7ee879762130467199745f2abc662f1e}

Geen.

## Zie ook {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ,  [Tekstreeks lokalisatie](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)

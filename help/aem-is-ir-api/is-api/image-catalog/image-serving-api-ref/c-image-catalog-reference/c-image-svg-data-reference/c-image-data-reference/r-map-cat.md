---
description: Afbeeldingskaartgegevens. Geen of meer volledige HTML <area> elementen, gesorteerd van voor naar achter.
solution: Experience Manager
title: Kaart
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9490b5c-0f85-4256-8590-0d6aa52a19d5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# Kaart{#map}

Afbeeldingskaartgegevens. Geen of meer volledige HTML `<AREA>` elementen, gesorteerd van voor naar achter.

De server interpreteert de kenmerken SHAPE en COORDS en kan deze wijzigen (SHAPE=CIRCLE wordt in deze versie niet ondersteund). Alle andere kenmerken van `<AREA>` zonder wijzigingen worden doorgegeven. Coördinaatwaarden die zijn opgegeven met het kenmerk COORDS, moeten pixelverschuivingen zijn ten opzichte van de linkerbovenhoek van de ongewijzigde bronafbeelding. (`%` coördinaten worden niet ondersteund in deze release en worden mogelijk niet correct verwerkt.)

## Eigenschappen {#section-f52d89fd399b4356ac05277e6c12f956}

Tekstreeks. Indien gespecificeerd moet het één of meerdere volledige HTML zijn `<AREA>` elementen.

Dit veld neemt deel aan de lokalisatie van tekstreeksen. Zie [Tekstreeks lokaliseren](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in de *HTTP-protocolreferentie* voor meer informatie.

## Standaard {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Geen.

## Zie ook {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) , [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Tekstreeks lokaliseren](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)

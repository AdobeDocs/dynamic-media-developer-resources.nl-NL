---
description: Afbeeldingskaartgegevens. Geen of meer volledige HTML <AREA>-elementen, gesorteerd van voor naar achter.
seo-description: Afbeeldingskaartgegevens. Geen of meer volledige HTML <AREA>-elementen, gesorteerd van voor naar achter.
seo-title: Kaart
solution: Experience Manager
title: Kaart
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 674a7a74-91bf-41c4-ab74-a5cb4f8abe1d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Kaart{#map}

Afbeeldingskaartgegevens. Geen of meer complete HTML `<AREA>`-elementen, gesorteerd van voor naar achter.

De server interpreteert de kenmerken SHAPE en COORDS en kan deze wijzigen. (SHAPE=CIRCLE wordt niet ondersteund in deze release.) Alle andere attributen van `<AREA>` worden overgegaan zonder wijziging. Coördinaatwaarden die zijn opgegeven met het kenmerk COORDS, moeten pixelverschuivingen zijn ten opzichte van de linkerbovenhoek van de ongewijzigde bronafbeelding. (`%` coördinaten worden niet ondersteund in deze release en worden mogelijk niet correct verwerkt.)

## Eigenschappen {#section-f52d89fd399b4356ac05277e6c12f956}

Tekstreeks. Indien opgegeven, moet het een of meer complete HTML `<AREA>`-elementen zijn.

Dit veld neemt deel aan de lokalisatie van tekstreeksen. Raadpleeg [Tekstreeks lokalisatie](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in de *HTTP-protocolreferentie* voor meer informatie.

## Standaard {#section-30c7f88929f54f7ba852c5c6c5e2c70b}

Geen.

## Zie ook {#section-d66a32e1f12f4cb0ad22ddd78be36ec4}

[map=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-map.md) ,  [req=map](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md),  [Tekstreeks lokalisatie](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)

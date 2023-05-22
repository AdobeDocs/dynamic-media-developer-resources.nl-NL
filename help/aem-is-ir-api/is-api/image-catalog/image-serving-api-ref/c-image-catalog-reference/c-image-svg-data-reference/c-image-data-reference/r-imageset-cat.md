---
description: Afbeeldingssetgegevens. Biedt een mechanisme voor het definiëren van gesorteerde sets afbeeldingen en het beheren van kenmerken die door Dynamic Media-viewers worden gebruikt.
solution: Experience Manager
title: ImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# ImageSet{#imageset}

Afbeeldingssetgegevens. Biedt een mechanisme voor het definiëren van gesorteerde sets afbeeldingen en het beheren van kenmerken die door Dynamic Media-viewers worden gebruikt.

Een afbeeldingsset bestaat uit een gesorteerde, door komma&#39;s gescheiden lijst met items, waarbij elk item bestaat uit een of meer subitems (afbeeldings-id&#39;s, stalen, paden voor mediabestanden, labels, enz.), gescheiden door puntkomma&#39;s en/of dubbele punten.

accolades `{ }` en haakjes `( )` kan worden gebruikt om bepaalde inhoud (zoals kleurwaarden) af te bakenen of geneste sets aan te geven. Accolades of ronde haakjes die op deze manier worden gebruikt, mogen niet worden gecodeerd en moeten altijd als overeenkomende paren worden weergegeven. Als dit niet het geval is, treedt er een parseringsfout op.

>[!NOTE]
>
>De volgende tekens worden gebruikt als ingestelde scheidingstekens en moeten HTTP-gecodeerd zijn wanneer ze in de set voorkomen als onderdeel van id- of tekenreekswaarden:
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



Raadpleeg de documentatie van de Image Serving Viewers voor meer informatie over de structuur en het gebruik van afbeeldingssets.

De server retourneert de inhoud van dit veld zonder wijzigingen als reactie op een `req=imageset` verzoek.

## Standaardsets {#section-5ecc8ffee7224668b63f601383665564}

De volgende vastgestelde definities worden native ondersteund door Image Serving en toegang met bepaalde viewers omvat parseren, valideren en verwerken van de set op de server. Elk settype kan worden geïdentificeerd door de corresponderende waarde in `catalog::AssetType`.

**Standaardstaalsets**

Elk item in een standaardstalenset bestaat uit een verwijzing naar een afbeeldingsrecord en een optionele aparte verwijzing naar een afbeeldingsrecord die als staal wordt gebruikt.

| `*`basicSwatchSet`*` | `*`staalItem`*&#42;[',' *`staalItem`*]` |
|---|---|
| `*`staalItem`*` | `*`imageId`*[';' *`staal`*]` |
| `*`staal`*` | `*`staalId`*|solidColorSpecifier` |
| `*`imageId`*` | IS-afbeeldingsverwijzing (catalogus/id) |
| `*`staalId`*` | IS-afbeeldingsverwijzing (catalogus/id) |
| `*`solidColorSpecifier`*` | ` '{0x' *`rrggbb`* [ *`label`*]'}'` |
| `*`rrggbb`*` | Verpakte hexadecimale RGB kleurwaarde van 6 cijfers voor effen kleurstalen |
| `*`label`*` | Optioneel tekstlabel voor effen kleurstalen |

**Hiërarchische stalensets**

Elk item in een hiërarchische stalenset kan bestaan uit een standaardstaalitem of een verwijzing naar een record in een stalenset (voor dergelijke items zijn stalen vereist).

| `*`hiërarchicalSwatchSet`*` | `*`hiërarchicalSwatchItem`* &#42;[ ',' *`hiërarchicalSwatchItem`* ]` |
|---|---|
| `*`hiërarchicalSwatchItem`*` | `*`staalItem`* | { *`basicSwatchSetId`* ';' *`staal`* }` |
| `*`basicSwatchSetId`*` | IS een verwijzing (catalogus/id) naar een catalogusrecord die een standaardstalenset definieert |

**Standaardcentrifuges**

Een basisset met centrifuges bestaat uit een eenvoudige lijst met afbeeldings-id&#39;s.

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**Tweedimensionale centraalvormige centrifuges**

Elk item in een tweedimensionale centrifuge kan bestaan uit een eenvoudige afbeelding, een verwijzing naar een elementaire centrifuge of een elementaire centrifuge die wordt begrensd door accolades. In plaats van accolades kunnen ronde haakjes worden gebruikt.

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`imageId`* | { '{' *`basicSpinSet`* '}' } | *`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | IS een verwijzing (catalogus/id) naar een catalogusrecord die een elementaire centrifugeset definieert |

**Paginasets**

Elk item in een paginaset kan bestaan uit maximaal drie pagina-afbeeldingen gescheiden met dubbele punten.

| `*`pageSet`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]` |

**Mediasets**

Elk item in een mediaset kan bestaan uit een afbeelding, een standaardstalenset, een hiërarchische stalenset, een basisspelersset, een tweedimensionale centrifugeset, een paginaset of een video-element. Elk mediaset-item kan ook een optioneel staal en type-id bevatten.

| `*`mediaSet`*` | `*`item`* &#42;[ , *`item`* ]` |
|---|---|
| `*`item`*` | ` { *`videoItem`* | *`recutItem`* | *`imageItem`*}} | *`setItem`* } [ ; [ *`ID`* ] [ ; [ *`gereserveerd`* ] ] ]` |
| `*`videoItem`*` | `*`video`* ; *`staalId`*` |
| `*`recutItem`*` | `*`recept`* ; *`staalId`*` |
| `*`imageItem`*` | `*`imageId`* ; [ *`staalId`* ]` |
| `*`setItem`*` | ` { *`setId`* | { '{' *`inlineSet`* '}' } } ; *`staalId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`staalId`*` | IS-afbeeldings-id |
| `*`video`*` | Pad van video-/animatiebestand of statische catalogus-id |
| `*`recept`*` | XML-bestandspad van definitie recut of statische catalogus-id |
| `*`imageId`*` | IS-afbeeldings-id |
| `*`setId`*` | IS verwijzing naar beeld, spin, of catalogusreeks |
| `*`inlineSet`*` | Een gealigneerde afbeelding, spin- of catalogusset |
| `*`gereserveerd`*` | Gereserveerd voor toekomstig gebruik |

**Videosets**

Een videoset bestaat uit een eenvoudige lijst met video-id&#39;s waarin elke id verwijst naar een item in de statische inhoudscatalogus.

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## Eigenschappen {#section-17c731e5c46646aa90ac21f39bb693ca}

Tekstreeks. Lijst met door komma&#39;s gescheiden `catalog::Id` waarden, absolute bestandspaden van afbeeldingsserver of bestandspaden ten opzichte van `attribute::RootPath`. In de set kan meerdere keren naar dezelfde afbeelding worden verwezen. De definiërende catalogusrecord kan op elke gewenste locatie in de set worden weergegeven.

Dit veld neemt deel aan de lokalisatie van tekstreeksen. Naast *`label`* tekenreeksen (onderdeel van de *`solidColorSpecifier`*) alle afgebakende velden zijn gelokaliseerd als ze ten minste één veld bevatten. `^loc=…^`&#39; lokalisatietoken. Zie [Tekstreeks lokaliseren](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in de *HTTP-protocolreferentie* voor meer informatie.

## Standaard {#section-c3a60e360393478284f0f2d2da5b963b}

Geen.

## Zie ook {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [kenmerk::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), [Vertaling object-id](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) , [Tekstreeks lokaliseren](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) Documentatie voor beeldweergave-viewers

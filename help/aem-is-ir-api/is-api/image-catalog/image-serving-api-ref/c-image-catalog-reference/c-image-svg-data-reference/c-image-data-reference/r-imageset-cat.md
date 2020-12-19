---
description: Afbeeldingssetgegevens. Biedt een mechanisme voor het definiëren van gesorteerde sets afbeeldingen en het beheren van kenmerken die door Scene7-viewers worden gebruikt.
seo-description: Afbeeldingssetgegevens. Biedt een mechanisme voor het definiëren van gesorteerde sets afbeeldingen en het beheren van kenmerken die door Scene7-viewers worden gebruikt.
seo-title: ImageSet
solution: Experience Manager
title: ImageSet
topic: Scene7 Image Serving - Image Rendering API
uuid: 1a34aaef-4053-4474-abb8-794331898d88
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%

---


# ImageSet{#imageset}

Afbeeldingssetgegevens. Biedt een mechanisme voor het definiëren van gesorteerde sets afbeeldingen en het beheren van kenmerken die door Scene7-viewers worden gebruikt.

Een afbeeldingsset bestaat uit een gesorteerde, door komma&#39;s gescheiden lijst met items, waarbij elk item bestaat uit een of meer subitems (afbeeldings-id&#39;s, stalen, paden voor mediabestanden, labels, enz.), gescheiden door puntkomma&#39;s en/of dubbele punten.

De accolades `{ }` en haakjes `( )` kunnen worden gebruikt om bepaalde inhoud (zoals kleurwaarden) te begrenzen of op geneste sets te wijzen. Accolades of ronde haakjes die op deze manier worden gebruikt, mogen niet worden gecodeerd en moeten altijd als overeenkomende paren worden weergegeven. Als dit niet het geval is, treedt er een parseringsfout op.

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

De server retourneert de inhoud van dit veld zonder wijzigingen in reactie op een `req=imageset`-verzoek.

## Standaardsets {#section-5ecc8ffee7224668b63f601383665564}

De volgende vastgestelde definities worden native ondersteund door Image Serving en toegang met bepaalde viewers omvat parseren, valideren en verwerken van de set op de server. Elk settype kan worden geïdentificeerd door de corresponderende waarde op te geven in `catalog::AssetType`.

**Standaardstaalsets**

Elk item in een standaardstalenset bestaat uit een verwijzing naar een afbeeldingsrecord en een optionele aparte verwijzing naar een afbeeldingsrecord die als staal wordt gebruikt.

| ` *`basicSwatchSet`*` | ` *``*&#42;[',' *`swatchItem`*]` |
|---|---|
| ` *`staalItem`*` | ` *``*[';' *`imageIdswatch`*]` |
| ` *`staal`*` | ` *`staalId`*|solidColorSpecifier` |
| ` *`imageId`*` | IS-afbeeldingsverwijzing (catalogus/id) |
| ` *`staalId`*` | IS-afbeeldingsverwijzing (catalogus/id) |
| ` *`solidColorSpecifier`*` | ` '{0x' *``* [ *`rrggbblabel`*]'}'` |
| ` *`rrggbb`*` | Verpakte hexadecimale RGB-kleurwaarde van 6 cijfers voor effen kleurstalen |
| ` *`label`*` | Optioneel tekstlabel voor effen kleurstalen |

**Hiërarchische stalensets**

Elk item in een hiërarchische stalenset kan bestaan uit een standaardstaalitem of een verwijzing naar een record in een stalenset (voor dergelijke items zijn stalen vereist).

| ` *`hiërarchicalSwatchSet`*` | ` *``* &#42;[ ',' *`hiërarchicalSwatchItemhiërarchicalSwatchItem`* ]` |
|---|---|
| ` *`hiërarchicalSwatchItem`*` | ` *``* | { *``* ';' *`swatchItembBasicSwatchSetIdswatch`* }` |
| ` *`basicSwatchSetId`*` | IS een verwijzing (catalogus/id) naar een catalogusrecord die een standaardstalenset definieert |

**Standaardcentrifuges**

Een basisset met centrifuges bestaat uit een eenvoudige lijst met afbeeldings-id&#39;s.

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**Tweedimensionale centraalvormige centrifuges**

Elk item in een tweedimensionale centrifuge kan bestaan uit een eenvoudige afbeelding, een verwijzing naar een elementaire centrifuge of een elementaire centrifuge die wordt begrensd door accolades. In plaats van accolades kunnen ronde haakjes worden gebruikt.

| ` *`2dSpinItem`*` | ` *`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| ` *`2dSpinItem`*` | ` *``* | { '{' *``* '}' } | *`imageIdbasicSpinSetbasicSpinSetId`*` |
| ` *`basicSpinSetId`*` | IS een verwijzing (catalogus/id) naar een catalogusrecord die een elementaire centrifugeset definieert |

**Paginasets**

Elk item in een paginaset kan bestaan uit maximaal drie pagina-afbeeldingen gescheiden met dubbele punten.

| ` *`pageSet`*` | ` *``* &#42;[ , *`pageItempageItem`* ]` |
|---|---|
| ` *`pageItem`*` | ` *``* [ : *``* [ : *`imageImageImageImageId`* ] ]` |

**Mediasets**

Elk item in een mediaset kan bestaan uit een afbeelding, een standaardstalenset, een hiërarchische stalenset, een basisspelersset, een tweedimensionale centrifugeset, een paginaset of een video-element. Elk mediaset-item kan ook een optioneel staal en type-id bevatten.

| ` *`mediaSet`*` | ` *``* &#42;[ , *`item`* ]` |
|---|---|
| ` *`item`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemItemImageItemSetItemIDreserved`* ] ] ]` |
| ` *`videoItem`*` | ` *``* ; *`videoswatchId`*` |
| ` *`recutItem`*` | ` *``* ; *`recutswatchId`*` |
| ` *`imageItem`*` | ` *``* ; [ *`imageIdswatchId`* ]` |
| ` *`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setLineSetSwatchId`*` |
| ` *`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| ` *`staalId`*` | IS-afbeeldings-id |
| ` *`video`*` | Pad van video-/animatiebestand of statische catalogus-id |
| ` *`recept`*` | XML-bestandspad van definitie recut of statische catalogus-id |
| ` *`imageId`*` | IS-afbeeldings-id |
| ` *`setId`*` | IS verwijzing naar beeld, spin, of catalogusreeks |
| ` *`inlineSet`*` | Een gealigneerde afbeelding, spin- of catalogusset |
| ` *`gereserveerd`*` | Gereserveerd voor toekomstig gebruik |

**Videosets**

Een videoset bestaat uit een eenvoudige lijst met video-id&#39;s waarin elke id verwijst naar een item in de statische inhoudscatalogus.

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## Eigenschappen {#section-17c731e5c46646aa90ac21f39bb693ca}

Tekstreeks. Lijst met door komma&#39;s gescheiden waarden, absolute bestandspaden voor afbeeldingsserver of bestandspaden ten opzichte van `catalog::Id`. `attribute::RootPath` In de set kan meerdere keren naar dezelfde afbeelding worden verwezen. De definiërende catalogusrecord kan op elke gewenste locatie in de set worden weergegeven.

Dit veld neemt deel aan de lokalisatie van tekstreeksen. Naast *`label`*-tekenreeksen (onderdeel van *`solidColorSpecifier`*) worden alle gescheiden velden gelokaliseerd als deze minstens één lokalisatietoken &#39; `^loc=…^`&#39; bevatten. Raadpleeg [Tekstreeks lokalisatie](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in de *HTTP-protocolreferentie* voor meer informatie.

## Standaard {#section-c3a60e360393478284f0f2d2da5b963b}

Geen.

## Zie ook {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ,  [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md),  [Object Id Translation](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) ,  [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , Image Serving Viewers Documentation

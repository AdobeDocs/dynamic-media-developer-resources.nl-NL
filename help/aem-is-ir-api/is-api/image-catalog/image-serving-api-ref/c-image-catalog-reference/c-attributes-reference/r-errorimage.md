---
description: Error response image. Als de functie Afbeeldingsservice wordt gebruikt, wordt doorgaans een foutstatus met een tekstbericht geretourneerd wanneer een fout optreedt.
seo-description: Error response image. Als de functie Afbeeldingsservice wordt gebruikt, wordt doorgaans een foutstatus met een tekstbericht geretourneerd wanneer een fout optreedt.
seo-title: ErrorImage
solution: Experience Manager
title: ErrorImage
topic: Scene7 Image Serving - Image Rendering API
uuid: b071c0cd-e7b8-422b-9b23-d93f504d9ce5
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---


# ErrorImage{#errorimage}

Error response image. Als de functie Afbeeldingsservice wordt gebruikt, wordt doorgaans een foutstatus met een tekstbericht geretourneerd wanneer een fout optreedt.

`attribute::ErrorImage` Hiermee kunt u een afbeelding, catalogusitem of sjabloon configureren die moet worden geretourneerd in geval van een fout.

>[!NOTE]
>
>Ontbrekende afbeeldingen kunnen ook worden verwerkt met `attribute::DefaultImage`.

Een Beeld dat malplaatje dient kan worden gevormd dat de tekst van het foutenbericht in het reactimage zou kunnen teruggeven. De volgende vooraf gedefinieerde variabelen kunnen worden opgenomen in de `$error.title`-sjabloon, die wordt vervangen door een korte foutbeschrijving, en `$error.message`, die wordt vervangen door een meer gedetailleerde foutbeschrijving (het detailniveau wordt geconfigureerd met `attribute::ErrorDetail`).

De HTTP-status 200 wordt geretourneerd als de afbeelding/sjabloon van de fout correct kan worden verwerkt. Als tijdens deze verwerking een fout optreedt, worden de HTTP-foutstatus en een tekstbericht geretourneerd.

## Eigenschappen {#section-f460c6c2dd1f46b29f9a79b093575f45}

Tekstreeks. Indien opgegeven, moet dit een geldige catalogus zijn::Id-waarde in een afbeeldingscatalogus of een relatief pad (naar `attribute::RootPath`) of een absoluut pad naar een afbeeldingsbestand dat toegankelijk is voor de afbeeldingsserver.

## Standaard {#section-2885f289e5714ddca665a6aee401967f}

Overgenomen van `default::ErrorImage` indien niet gedefinieerd. Als dit wel is gedefinieerd maar leeg is, wordt het gedrag van de foutafbeelding uitgeschakeld, zelfs als `default::ErrorImage` is gedefinieerd en een HTTP-foutstatus en -tekstbericht worden geretourneerd.

## Voorbeeld {#section-c92090abe1d247529542a8dd4960c2e6}

Als u reactieafbeeldingen wilt ophalen met het foutbericht dat in de afbeelding wordt weergegeven, moet u eerst de sjabloon definiëren in de afbeeldingscatalogus. In dit geval maken we een item in onze afbeeldingscatalogus met de naam `onError`, dat het volgende bevat in `catalog::Modifier`:

`size=300,300&bgc=ffffff&text=$error.message$`

De sjabloon is geregistreerd bij `attribute::ErrorImage`:

`ErrorImage=myCatalog/onError`

In dit voorbeeld wordt de tekst weergegeven met het standaardlettertype, de standaardlettertypekleur en de standaardtekengrootte.

## Zie ook {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) ,  [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)

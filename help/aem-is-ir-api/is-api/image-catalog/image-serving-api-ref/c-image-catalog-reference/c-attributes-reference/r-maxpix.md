---
description: Limiet voor afbeeldingsgrootte beantwoorden. Maximale breedte en hoogte van reactieafbeelding die aan de client kunnen worden geretourneerd.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# MaxPix{#maxpix}

Limiet voor afbeeldingsgrootte beantwoorden. Maximale breedte en hoogte van reactieafbeelding die aan de client kunnen worden geretourneerd.

De server retourneert een fout als een aanvraag een antwoordafbeelding zou veroorzaken waarvan de breedte of hoogte groter is dan `attribute::MaxPix`.

## Eigenschappen {#section-b175425b9e9f48e0b1a71640f6a9e936}

Twee gehele getallen, groter dan 0, gescheiden door een komma. Breedte en hoogte in pixels. Kan ook worden ingesteld op `0,0` om een willekeurige grootte voor de antwoordafbeelding zonder beperkingen toe te staan.

## Standaard {#section-1003537434da432fb2af100ecdbf9d72}

Overgenomen van `default::MaxPix` indien niet gedefinieerd of indien leeg.

## Zie ook {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)

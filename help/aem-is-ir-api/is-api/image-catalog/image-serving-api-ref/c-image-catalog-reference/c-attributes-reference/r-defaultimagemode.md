---
description: Standaardafbeeldingsmodus. Hiermee selecteert u hoe de standaardafbeelding wordt toegepast wanneer er geen afbeeldingen worden gevonden die in de aanvraag zijn opgegeven.
solution: Experience Manager
title: DefaultImageMode
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# DefaultImageMode{#defaultimagemode}

Standaardafbeeldingsmodus. Hiermee selecteert u hoe de standaardafbeelding wordt toegepast wanneer er geen afbeeldingen worden gevonden die in de aanvraag zijn opgegeven.

## Eigenschappen {#section-7fa8acb63540490d9f5186231b5e77c3}

Enum. &#39;0&#39; ter vervanging van de volledige samengestelde afbeelding, zelfs als de ontbrekende afbeelding slechts een van de lagen is; &#39;1&#39; om elke ontbrekende bronafbeelding van de laag te vervangen door de standaardafbeelding en de samenstelling op de gebruikelijke manier te retourneren.

## Beperkingen {#section-04cb0d50e8914564a8d226d0d4663c8b}

Beeldserver wordt teruggezet naar `DefaultImageMode=0` wanneer geneste aanvragen voor het renderen van afbeeldingen, FXG of `req=set` mislukken.

## Standaard {#section-9e318524a2a5496386901286748c7ee7}

Overgenomen van `default::DefaultImage` indien niet gedefinieerd of indien leeg.

## Zie ook {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) ,  [kenmerk::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)

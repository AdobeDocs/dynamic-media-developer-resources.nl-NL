---
description: Coördinaten van afbeeldingslocaties die door de bewerking getPhotoshopPath worden geretourneerd.
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 11%

---

# PerspectiveQuad{#perspectivequad}

Coördinaten van afbeeldingslocaties die door de bewerking getPhotoshopPath worden geretourneerd.

Syntaxis

## Parameters {#section-59792c446366456d90de7f5875bad1b0}

| Naam | Type | Beschrijving |
|---|---|---|
| x0 | `xsd:double` | Coördinaat op de x-as linksboven. |
| y0 | `xsd:double` | Coördinaat op de y-as linksboven. |
| x1 | `xsd:double` | Coördinaat op de x-as rechtsboven. |
| y1 | `xsd:double` | Y-ascoördinaat rechtsboven. |
| x2 | `xsd:double` | Coördinaat met de x-as rechtsonder. |
| y2 | `xsd:double` | Coördinaat met de y-as rechtsonder. |
| x3 | `xsd:double` | Coördinaat van de x-as linksonder. |
| y3 | `xsd:double` | Coördinaat op de y-as linksonder. |

## Voorbeeld {#section-19ed4409ff3a41c9b52a9c9424612927}

De `PerspectiveQuad` het type keert gegevens in deze orde terug:

```
<complexType name="PerspectiveQuad">
        <sequence>
            <element name="x0" type="xsd:double"/>
            <element name="y0" type="xsd:double"/>
            <element name="x1" type="xsd:double"/>
            <element name="y1" type="xsd:double"/>
            <element name="x2" type="xsd:double"/>
            <element name="y2" type="xsd:double"/>
            <element name="x3" type="xsd:double"/>
            <element name="y3" type="xsd:double"/>
        </sequence>
```

>[!MORELIKETHIS]
>
>* [getPhotoshopPath](../../operations/c-operations-intro/c-methods/r-get-photoshop-path.md#reference-545f902f84194951ac04e947fdc803b9)


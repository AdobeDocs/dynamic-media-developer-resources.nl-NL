---
description: Coördinaten van afbeeldingslocaties die door de bewerking getPhotoshopPath worden geretourneerd.
seo-description: Coördinaten van afbeeldingslocaties die door de bewerking getPhotoshopPath worden geretourneerd.
seo-title: PerspectiveQuad
solution: Experience Manager
title: PerspectiveQuad
topic: Scene7 Image Production System API
uuid: e83b7b8c-995b-4ac0-ace5-491f7e98674d
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4

---


# PerspectiveQuad{#perspectivequad}

Coördinaten van afbeeldingslocaties die door de bewerking getPhotoshopPath worden geretourneerd.

Syntaxis

## Parameters {#section-59792c446366456d90de7f5875bad1b0}

| Naam | Type | Beschrijving |
|---|---|---|
| ` *`x0`*` | `xsd:double` | Coördinaat op de x-as linksboven. |
| ` *`y0`*` | `xsd:double` | Coördinaat op de y-as linksboven. |
| ` *`x1`*` | `xsd:double` | Coördinaat op de x-as rechtsboven. |
| ` *`y1`*` | `xsd:double` | Y-ascoördinaat rechtsboven. |
| ` *`x2`*` | `xsd:double` | Coördinaat met de x-as rechtsonder. |
| ` *`y2`*` | `xsd:double` | Coördinaat met de y-as rechtsonder. |
| ` *`x3`*` | `xsd:double` | Coördinaat van de x-as linksonder. |
| ` *`y3`*` | `xsd:double` | Coördinaat op de y-as linksonder. |

## Voorbeeld {#section-19ed4409ff3a41c9b52a9c9424612927}

Het `PerspectiveQuad` type retourneert gegevens in deze volgorde:

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


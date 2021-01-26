---
description: Type aanvraag. Hier geeft u het type aanvraag op.
seo-description: Type aanvraag. Hier geeft u het type aanvraag op.
seo-title: req
solution: Experience Manager
title: req
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b888be10-89e5-4b41-a2bd-f83533ea2481
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---


# req{#req}

Type aanvraag. Hier geeft u het type aanvraag op.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`opties`*]`

* [catalogusprofielen](r-catalogprops.md)
* [exists](r-exists.md)
* [imageprops](r-imageprops.md)
* [imageset](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [map](r-map-req.md)
* [masker](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [message](r-message.md)
* [props](r-props.md)
* [oplossen](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [set](r-set.md)
* [streefdoelen](r-targets.md)
* [tmb](r-tmb.md)
* [gebruikersgegevens](r-userdata.md)
* [validate](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

Tenzij anders vermeld in de gedetailleerde beschrijvingen, zal de server `text` reacties met MIME type `text/plain` terugkeren. Bij veel aanvraagtypen kunt u een type reactie opgeven, zoals `text`. Dit is doorgaans de standaardinstelling `javascript`, `xml` of `json`. De bijbehorende MIME-typen voor reacties zijn respectievelijk `text/plain`, `text/javascript`, `text/xml` en `text/javascript`.

Tenzij anders vermeld, formatteren de reacties de reactie als reeks van `name=value` paren.

Zie [Eigenschappen](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).

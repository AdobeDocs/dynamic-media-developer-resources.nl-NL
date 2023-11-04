---
description: Type aanvraag. Hier geeft u het type aanvraag op.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '90'
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

Tenzij anders vermeld in de gedetailleerde beschrijvingen, keert de server terug `text` reacties met het MIME-type `text/plain`. Bij veel aanvraagtypen kunt u een type reactie opgeven, zoals `text` Dit is doorgaans de standaardinstelling. `javascript`, `xml`, of `json`. De bijbehorende MIME-typen voor reacties zijn `text/plain`, `text/javascript`, `text/xml`, en `text/javascript`, respectievelijk.

Tenzij anders vermeld, formatteren de reacties de reactie als reeks `name=value` paren.

Zie [Eigenschappen](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
